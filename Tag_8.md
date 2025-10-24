### Tag 8 24.10.2025

#### Aufgabe 1

<img width="1761" height="1061" alt="image" src="https://github.com/user-attachments/assets/5acfcacb-5c75-4b02-a550-9dac9a8cf7a1" />

4.  Digitale Signatur vs. Verschlüsselung

- **Signatur:** Hash der Nachricht wird mit dem **privaten Schlüssel des Absenders** signiert → prüfbar mit dem **öffentlichen Schlüssel**.  
  *Ziel:* Echtheit & Integrität.

- **Verschlüsselung:** Nachricht wird mit dem **öffentlichen Schlüssel des Empfängers** verschlüsselt → lesbar nur mit seinem **privaten Schlüssel**.  
  *Ziel:* Vertraulichkeit.

5.

| Vorgang | Schlüssel | Zweck |
|----------|------------|-------|
| Signieren | Privater Schlüssel (Absender) | Erzeugt Signatur |
| Prüfen | Öffentlicher Schlüssel (Absender) | Prüft Echtheit |
| Verschlüsseln | Öffentlicher Schlüssel (Empfänger) | Schützt Inhalt |
| Entschlüsseln | Privater Schlüssel (Empfänger) | Macht Inhalt lesbar |


#### Aufgabe 2

<img width="745" height="292" alt="image" src="https://github.com/user-attachments/assets/598f0941-5386-4a58-a1e5-ee04bfb8f838" />

<img width="800" height="495" alt="image" src="https://github.com/user-attachments/assets/cc47301e-b3b7-46a6-b4f1-9e36ad3d6410" />


#### Aufgabe 3

##### Theorie

**Chosen-Ciphertext-Angriff:**  
- Angreifer fängt verschlüsselte Nachricht ab und nutzt manipulierte Nachrichten, um Informationen über den privaten Schlüssel zu erhalten.  
- **Praxisregel:** Niemals unbekannte Dateien mit eigenem privaten Schlüssel signieren.

**Public-Key-Infrastruktur (PKI):**  
- System zur sicheren Ausstellung, Verteilung und Prüfung von Public-Keys mittels **Zertifikaten**.  
- Zertifikate bestätigen, dass ein Public-Key wirklich zu einer Person oder Organisation gehört.  
- Bestandteile: CA, RA, CRL, Verzeichnisdienste, Zeitstempel, Subscriber/Participant.  
- **X.509-Zertifikate:** Standardisierte digitale Zertifikate, hierarchisch von CAs signiert.

1. **Public-Key verifizieren:**  
- Über Zertifikat einer vertrauenswürdigen CA prüfen (gültig, nicht gesperrt, korrekt signiert).  

2. **Public-Key-Infrastruktur:**  
- System zur sicheren Verwaltung und Prüfung von Public-Keys.  

3. **Certification Authority (CA) / Trust-Center (TC):**  
- CA: stellt Zertifikate aus und signiert sie.  
- TC: überprüft Identität der Antragsteller vor Ausstellung.  

4. **CrypTool-Zertifikat:**  
- Enthält z. B. CN (Name), Issuer, Gültigkeit, Public-Key-Infos.  
- Root-CA: oberste, selbstsignierte Zertifizierungsstelle, Basis des Vertrauens.
