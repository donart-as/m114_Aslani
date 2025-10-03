### Tag 6 26.09.2025

# Einführung in Kryptologie – Theorie & Übungen

## 1. Grundlagen

**Kryptologie**  
Wissenschaft vom Entwurf, der Anwendung und Analyse kryptographischer Verfahren.

**Kryptografie**  
- Ursprünglich: Verschlüsselung  
- Heute: Gesamtheit von Maßnahmen zur Informationssicherheit (Vertraulichkeit, Integrität, Authentizität)

**Wichtige Begriffe**  
- **Klartext (P / K):** lesbarer Originaltext  
- **Geheimtext (C):** verschlüsselter Text  
- **Verschlüsselung (Encryption):** Klartext → Geheimtext  
- **Entschlüsselung (Decryption):** Geheimtext → Klartext  
- **Chiffre (Cipher):** Algorithmus zum (Ent-)verschlüsseln  
- **Schlüssel (K / S):** geheime Information, die das Ergebnis steuert  
- **Hash:** fixe, kurze Darstellung (Fingerabdruck) von Daten  
- **Kryptoanalyse:** Untersuchung der Sicherheit eines Verfahrens

**Chiffrenarten**  
- **Blockchiffre:** verschlüsselt ganze Datenblöcke (z. B. 64 oder 128 Bit)  
- **Stromchiffre:** verschlüsselt Bit-/Zeichenstrom kontinuierlich, Echtzeit geeignet  
- **Symmetrisch:** gleicher Schlüssel für Ver- und Entschlüsseln  
- **Asymmetrisch:** Public/Private-Key-Paar (RSA, ECC)


## 2. Aufgaben

### 2.1 Abkürzungen

| Abkürzung | Bedeutung | Typ |
|-----------|-----------|-----|
| AES       | Advanced Encryption Standard | symmetrische Blockchiffre |
| DES       | Data Encryption Standard | symmetrische Blockchiffre |
| IDEA      | International Data Encryption Algorithm | symmetrische Blockchiffre |
| RC4       | Rivest Cipher 4 | Stromchiffre |
| XOR       | Exclusive OR (logische Operation) | Primitive/Operation |
| RSA       | Rivest–Shamir–Adleman | asymmetrisch |
| ECC       | Elliptic Curve Cryptography | asymmetrisch |
| SHA       | Secure Hash Algorithm | Hash-Funktion |

**Blockchiffren:** AES, DES, IDEA


### 2.2 ROT-/Cäsar-Chiffre

**Beispiel ROT-3:**  
- Verschlüsselung: `A → D`  
- Entschlüsselung: `D → A`

**Knack-Beispiel ROT-N:**  
- Geheimtext: `VLON ZILWY`  
- Mit ROT-20 entschlüsselt → `BRUT FORCE`

**Cäsar-Beispiel aus Skript:**  
- Geheimtext: `GHU DQJULII HUIROJW CXU WHHCHLW ...`  
- ROT-3 entschlüsselt → `DER ANGRIFF ERFOLGT ZUR TEEZEIT ...`

**ASCII-Histogramm:**  
- Zählt Häufigkeit jedes Buchstabens im Ciphertext  
- Ermöglicht Analyse monoalphabetischer Substitutionen  
- Störbar durch Polyalphabetische Verfahren oder kurze Texte


### 2.3 Vigenère-Verschlüsselung

**Formel:**  
- Verschlüsselung: `C = (P + K) mod 26`  
- Entschlüsselung: `P = (C − K) mod 26`  
- A=0, B=1, …, Z=25

**Beispiele:**  
1. Wort `BEEF` mit Schlüssel `AFFE`:  
   - B(1)+A(0)=B, E(4)+F(5)=J, E(4)+F(5)=J, F(5)+E(4)=J  
   - **Geheimtext:** `BJJJ`

2. Geheimtext `WRKXQT` mit Schlüssel `SECRET`:  
   - Entschlüsseln → `ENIGMA`

**Hinweis:** Für lange Texte Kasiski-Analyse oder CrypTool1 nutzen.


### 2.4 XOR-Stromchiffre

**Beispiel Name `MAX`, Schlüssel `ABC`:**  
- ASCII: M=0x4D, A=0x41, X=0x58  
- Schlüssel: A=0x41, B=0x42, C=0x43  
- XOR → 0x4D⊕0x41=0x0C, 0x41⊕0x42=0x03, 0x58⊕0x43=0x1B  
- **Cipher Hex:** `0C 03 1B`

**Dezimalzahl 4711 verschlüsseln:**  
- 4711 → 16-Bit Binär: `0001001001010111`  
- Schlüssel: `10001101` → wiederholen → XOR → Chiffre  
- Entschlüsselung: XOR erneut → Original

**Key-Rekonstruktion Beispiel:**  
- Klartext `IBM` + Chiffre `"[ql"` → Schlüssel 0x12 0x33 0x21  
- Entschlüsseln `V{m` → `DHL`


### 2.5 Symmetrische Verschlüsselung – Vor-/Nachteile

**Vorteile:**  
- Kurzer Schlüssel vs. lange Nachricht  
- Schnelle Verschlüsselung  
- Einfacherer sicherer Kanal für Schlüssel

**Nachteile:**  
- Schlüssel muss sicher ausgetauscht werden  
- Quadratisches Wachstum bei N Teilnehmern: `S = N*(N-1)/2`

| N | S |
|---|---|
| 2 | 1 |
| 5 | 10 |
| 10 | 45 |
| 20 | 190 |
| 100 | 4'950 |
| 200 | 19'900 |
| 300 | 44'850 |


### 2.6 Hash-Werte

**Eigenschaften:** deterministisch, feste Länge, einweg, kollisionsresistent, effizient

**Beispiele:**  
- Text: `Hello, world!`  
  - MD5: `6cd3556deb0da54bca060b4c39479839`  
  - SHA-256: `315f5bdb76d078c43b8ac0064e4a0164...`

- **Kleinste Änderung → kompletter neuer Hash** (Avalanche-Effekt)  
- Empfehlung: SHA-256 oder BLAKE2 statt MD5/SHA-1


### 2.7 Moderne symmetrische Verfahren

| Verfahren | Beschreibung | Schlüssel | Anwendung |
|-----------|--------------|----------|-----------|
| IDEA | Blockchiffre, 64-Bit Blöcke, 8 Runden, Add/Mult/XOR | 128 Bit | Historisch in PGP |
| RC4 | Stromchiffre | variabel | SSL/TLS, WEP (heute unsicher) |
| DES (CBC) | Blockchiffre, 64-Bit Block, CBC-Modus | 56 Bit (+8 Parität) | Historisch, ersetzt durch 3DES |
| AES | Blockchiffre, 128-Bit Block, 10-14 Runden | 128/192/256 Bit | Standard heute (TLS, VPN, Festplatten) |




