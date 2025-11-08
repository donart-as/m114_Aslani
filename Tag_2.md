## Tag 2 29.08.2025


## Einführung Codesysteme

**Arten von Codes**

Numerisch: Zahlen im Computer (z. B. Dualcode, Graycode)

Alphanumerisch: Buchstaben/Zahlen (z. B. ASCII, Unicode)

Strichcode: Produkte identifizieren (EAN)

Leitungscode: Datenübertragung optimieren (Manchester, NRZ)

Media-Codecs: Audio/Video codieren (MP3, MPEG)

Geheimcode: Verschlüsselung

ISBN: Buchnummer

Genetisch: DNA → Aminosäuren

Nicht zu verwechseln mit: Protokollen oder Datenformaten.

**Eigenschaften von Codes**

Effizient, fehlererkennend, sicher

**Gleitkommazahlen (IEEE 754)**

Zahlen mit „beweglichem“ Komma

Bestehen aus: Vorzeichen, Exponent (Komma-Position), Mantisse (Zahlenwert)

**Formate:**

Single → 32 Bit, ~7 Dezimalstellen

Double → 64 Bit, ~15 Dezimalstellen

### Aufgabe 2

1. https://zahlensysteme-rechner.de/ieee-754-konverter/
2. https://www.h-schmidt.net/FloatConverter/IEEE754.html
- Es ergibt genau 1
- 1.9999999
- Kann die dez. Zahl 0.1 genau gespeichert werden? (Bei "Decimal Representation" 0.1 eingeben) = Nein es geht nicht = 0.100000001490116119384765625
- max. darstellbare Zahl≈3,4028235×10 hoch 38​
- Und die kleinste pos. Zahl? (knapp ≠ 0) =  2.350989e-38

### Aufgabe 3

1. Was stellen Sie fest bezüglich der Länge und Codierung der UTF-8 Zeichen gegenüber den ASCII-Zeichen?
   Bei ASCII haben alle Zeichen gleich viele Bytes, bei UTF-8 ist die Anzahl der Bytes pro Zeichen unterschiedlich.
2. € Zeichen in Verschieden Aplikationen.

HTML: € €

Windows: 20AC danach alt + x

Word: 20AC danach alt + c

Powerpoint:
 
3.
**Welche der Dateien ist nun ASCII-codiert, welche UTF-8 und welche UTF-16 BE-BOM?**
  
Textsample1 → ASCII

Textsample2 → UTF-8 (ohne oder mit optionaler BOM)

Textsample3 → UTF-16 BE mit BOM

**Alle drei Dateien enthalten denselben Text. Aus wie vielen Zeichen besteht dieser?**

68 Zeichen

**Was sind die jeweiligen Dateigrössen? (Beachten Sie, dass unter Grösse auf Datenträger jeweils 0 Bytes angegeben wird. Dies darum, weil beim Windows-Dateisystem NTFS kleine Dateien direkt in die MFT (Master File Table) geschrieben werden.) Wie erklären Sie sich die Unterschiede?**

71 Bytes (71 Bytes)


4. Bestimmen Sie zu folgende Zeichen den Code:

Steuerzeichen (ASCII):

CR  = 13

LF  = 10

TAB  = 9

Leerzeichen = 32

Zeichen (ASCII):

'0' = 48

'A' = 65

'a' = 97

Sonderzeichen (UTF-8):

§ = 194 167

£ = 194 163

© = 194 169

😀 = 240 159 152 128

### Aufgabe 4

<img width="1062" height="183" alt="image" src="https://github.com/user-attachments/assets/cfe358c7-8fdc-4ad4-b715-7a0eb6fc3a7f" />
