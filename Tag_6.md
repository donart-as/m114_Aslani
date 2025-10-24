### Tag 7 03.10.2025

## 1. Diffie-Hellman

### Theorie
- **Zweck**: Sicherer Schlüsseltausch (nicht verschlüsseln).  
- **Ablauf**:  
  - Öffentliche Basis `g` + Primzahl `p`.  
  - Jeder wählt eine geheime Zahl `a` bzw. `b`.  
  - Öffentliche Teilschlüssel:  
    - `A = g^a mod p`  
    - `B = g^b mod p`  
  - Gemeinsamer Schlüssel: `S = B^a mod p = A^b mod p`  
- **Einwegfunktion**: Leicht vorwärts, schwer rückwärts (Modulo).  
- **Anwendung**: HTTPS/TLS, E-Commerce.  

### Aufgabe 1
<img width="992" height="785" alt="image" src="https://github.com/user-attachments/assets/4b9f1d22-6e6a-4b79-a520-d8f8d0a6c417" />



## 2. RSA

### Theorie
- **Zweck**: Nachrichten verschlüsseln.  
- **Schlüsselpaar**:  
  - Public Key `(e, N)` → verschlüsseln  
  - Private Key `(d, N)` → entschlüsseln  
- **Mathematik**:  
  - Verschlüsselung: `c = k^e mod N`  
  - Entschlüsselung: `k = c^d mod N`  
- **Sicherheit**: Große Primzahlen, Faktorisierung schwierig  
- Heute: Schlüssellängen ≥ 2048 Bit  
- Langsam → meist nur für Schlüssel, nicht ganze Nachrichten  

### Aufgabe 2
<img width="588" height="676" alt="image" src="https://github.com/user-attachments/assets/a1c1fbdc-cd5e-4745-9727-c18f12a3c163" />

- Beispiel: p=11, q=29 → N=319, φ=280  
- e=17, d=33, Klartext k=65 („A“)  
- Verschlüsselung: `c = 65^17 mod 319 = 285`  
- Entschlüsselung: `285^33 mod 319 = 65`  
- Erkenntnis: Nur der richtige Private Key entschlüsselt richtig.  
- RSA arbeitet **blockweise**, darum sieht man die verschlüsselten Daten in Blöcken.  


## 3. Hybride Verfahren

### Theorie
- **Problem**:  
  - Symmetrisch (AES) → schnell, Schlüsselverteilung schwer  
  - Asymmetrisch (RSA) → sicherer Schlüssel, langsam  
- **Lösung** = Hybrid: RSA + AES  
  - AES verschlüsselt Nachricht  
  - RSA verschlüsselt Session-Key  
- Beispiele: TLS (HTTPS), PGP, S/MIME, IPsec  

### Aufgabe 3
Die Datei enthält Informationen zur Verschlüsselung des Session-Keys und des Geheimtexts.

Verwendet werden **RSA-1024** (asymmetrisch) und **AES** (symmetrisch).

Der Session-Key ist **128 Bit** lang.

Das Zertifikat **X.509v3-1996** stammt von **CrypTool (CN=CrypTool CA 2)**.

Die Datei soll entschlüsselt werden.






