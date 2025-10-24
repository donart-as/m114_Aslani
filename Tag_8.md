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


