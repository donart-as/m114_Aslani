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


#### Aufgaben

**1. Wie kann ich den Public-Key verifizieren?**  
- Über das digitale Zertifikat einer vertrauenswürdigen CA.  
- Prüfen, ob das Zertifikat gültig, nicht gesperrt (CRL) und korrekt signiert ist.  
- Schlüssel-Fingerabdrücke mit offiziellen Quellen vergleichen.

**2. Was versteht man unter Public-Key-Infrastruktur?**  
- System zur sicheren Ausstellung, Verteilung und Prüfung von Public-Keys mittels Zertifikaten.  
- Stellt sicher, dass ein Public-Key wirklich der angegebenen Person oder Organisation gehört.

**3. Was bedeutet Certification-Authority (CA) und was Trust-Center (TC)?**  
- **CA:** Stellt Zertifikate aus und signiert diese digital.  
- **TC:** Prüft die Identität des Antragstellers und überwacht die ordnungsgemäße Ausstellung der Zertifikate.

**4. Untersuchen Sie die Zertifizierung des CrypTool 1. Lassen Sie sich das Zertifikat ihres RSA-Schlüsselpaares von einem KI-Bot erklären, auch die Abkürzungen.**  
- Das Zertifikat enthält u.a. CN (Common Name), Issuer (Herausgeber), Gültigkeitszeitraum, Public-Key-Infos.  
- KI-Bot oder CrypTool kann die Abkürzungen erklären, z. B. CN = Name der CA oder des Zertifikatsinhabers.

**5. Was ist ein Root-CA?**  
- Oberste, selbstsignierte Zertifizierungsstelle in einer PKI.  
- Vertrauensbasis für alle darunterliegenden Zertifikate (Sub-CAs oder Teilnehmer).  


