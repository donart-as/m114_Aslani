# Tag 6 — Kryptographie I

## Theorieteil

### 1. Einführung
Dieser Teil C bietet die Grundlage zur Einführung in Cyber Security (Siehe auch M182). Eine mögliche Weiterbildung nach der Lehre wäre **Cyber Security Specialist** mit eidg. Fachausweis (EFA).

#### 1.1 Was bedeutet «Geheimhaltung»?
Geheimhaltung bedeutet, dass Daten nur von berechtigten Personen eingesehen werden dürfen. Schutz vor unbefugtem Lesen.

#### 1.2 Begriffe der Kryptologie
- **Kryptologie**: Überbegriff für Kryptografie + Kryptoanalyse.
- **Kryptografie**: Schutz der Information (Verschlüsselung, Signatur, Hashing).
- **Kryptoanalyse**: Angriffe und Analyse kryptografischer Verfahren.

| Begriff | Bedeutung |
|---|---|
| Klartext (P) | Unverschlüsselte, lesbare Nachricht |
| Geheimtext (C) | Verschlüsselte Nachricht |
| Schlüssel (K) | Steuert die Verschlüsselung/Entschlüsselung |
| Cipher / Chiffre | Verschlüsselungsalgorithmus |
| Hash | Unumkehrbarer „Fingerabdruck“ einer Nachricht |

##### Akteure
- Sender (Alice)
- Empfänger (Bob)
- Angreifer (Eve)

#### 1.3 Block- und Stromchiffren
- **Blockchiffre**: Teilt Nachricht in Blöcke (z. B. 64/128 Bit). Beispiel: AES, DES, IDEA.
- **Stromchiffre**: Verschlüsselt Bit-/Zeichenweise. Beispiel: RC4.

#### 1.4 Symmetrisch vs. Asymmetrisch
| Symmetrisch | Asymmetrisch |
|---|---|
| Gleicher Schlüssel für Ver- und Entschlüsselung | Privater + Öffentlicher Schlüssel |
| Sehr schnell | Rechenaufwändiger |
| Beispiel: AES, DES, IDEA | Beispiel: RSA, ECC |

#### 1.5 Hashfunktionen
- **Keine Entschlüsselung möglich**.
- Kleine Änderungen führen zu komplett anderen Hashes (**Avalanche-Effekt**).
- Beispiele: SHA‑256, SHA‑3.

#### 1.6 Schlüsselmanagement
Wenn N Personen sicher kommunizieren wollen:
\( S = N * (N - 1) / 2 \)
(z. B.: 10 Personen → 45 Schlüssel)

## Aufgaben

### Aufgabe 1
AES, DES, IDEA und RC4 sind Verschlüsselungsalgorithmen. XOR ist eine logische Operation. AES und RSA sind heutige Standards, DES und RC4 veraltet. IDEA teils noch genutzt.

- **AES** – Advanced Encryption Standard
- **DES** – Data Encryption Standard
- **IDEA** – International Data Encryption Algorithm
- **RC4** – Rivest Cipher 4
- **XOR** – Exclusive OR
- **RSA** – Asymmetrisches Verfahren auf Basis von Primzahlfaktorisierung
- **ECC** – Elliptic Curve Cryptography
- **SHA** – Secure Hash Algorithm

**Blockchiffre:** AES (128 Bit), DES (64 Bit), IDEA (64 Bit)
**Stromchiffre:** RC4, XOR
**RSA/ECC:** Schlüsselaustausch / Signaturen
**SHA:** Hashalgorithmus

### Aufgabe 2.1
Der chiffrierte Text war **ROT-3**. Klartext:
```
DER ANGRIFF ERFOLGT ZUR TEEZEIT
DIE WUERFEL SIND GEFALLEN
ICH KAM SAH UND SIEGTE
TEILE UND HERRSCHE
```
Histogramm nutzt Häufigkeit von „E“. Analyse gelingt nur bei ausreichend langem Ciphertext. Man kann Analyse stören durch Zusatzzeichen.

### Aufgabe 2.2
- „BEEF“ + Schlüssel „AFFE“ → **BJJJ**
- „WRKXQT“ + Schlüssel „SECRET“ → **ENIGMA**
- Langer Geheimtext entschlüsselt zu Zitaten von **Ludwig XIV**.
- Häufigkeitsanalyse und Schlüssellängenanalyse notwendig.

### Aufgabe 2.3
Beispiel XOR:
- Schlüsselkonstruktion rückwärts möglich → unsicher.
- Schlüsselrekonstruktion durch XOR von Klartext und Ciphertext.

### Aufgabe 2.4
Schlüsselanzahl: \( S = N · (N - 1) / 2 \)
- 2 → 1
- 5 → 10
- 10 → 45
- 20 → 190
- 100 → 4950
- 200 → 19900
- 300 → 44850

### Aufgabe 2.5
Schon **1 Bit Änderung** erzeugt völlig neuen Hashwert. (Avalanche-Effekt)

### Aufgabe 2.6
| Verfahren | Typ | Schlüssel | Anwendung |
|---|---|---|---|
| IDEA | Blockchiffre | 128-bit | PGP historisch, noch sicher |
| RC4 | Stromchiffre | variabel | SSL früher, heute unsicher |
| DES (CBC) | Blockchiffre | 56-bit | historisch, ersetzt von AES |
| AES | Blockchiffre | 128/192/256-bit | Standard heute |
