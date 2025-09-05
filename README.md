# m114_Aslani

## Tag 1 22.08.2025

## Digitale Daten

Bit (b): Kleinste Informationseinheit, nur 0 oder 1.

Byte (B): 1 Byte = 8 Bit, Wertebereich 0–255.

Datenraten: Immer in Bit pro Sekunde (z. B. 100 Mb/s).

Speichergrössen: Immer in Byte (z. B. 256 GB SSD).

**SI-Präfixe (Zehner-System)**

10 Hoch 24 → [Y] → Yotta → 1024 → 1'000'000'000'000'000'000'000'000 → Quadrillion

10 Hoch 21 → [Z] → Zetta → 1021 → 1'000'000'000'000'000'000'000 → Trilliarde

10 Hoch 18 → [E] → Exa  → 1'000'000'000'000'000'000 → Trillion

10 Hoch 15 → [P] → Peta  → 1'000'000'000'000'000 → Billiarde

10 Hoch 9 → [G] → Giga  → 1'000'000'000 → Milliarde

10 Hoch 6 → [M] → Mega  → 1'000'000 → Million

10 Hoch 3 → [k] → kilo → 1'000 → Tausend

10 Hoch 0 → [-]  → 1 → Eins

10 Hoch -3 → [m] → milli  → 0.001 → Tausendstel

10 Hoch -6 → [µ] → mikro  → 0.000'001 → Millionstel

10 Hoch -9 → [n] → nano  → 0.000'000'001 → Milliardstel

10 Hoch -12 → [p] → piko  → 0.000'000'000'001 → Billionstel

10 Hoch -15 → [f] → femto  → 0.000'000'000'000'001 → Billiardstel

10 Hoch -18 → [a] → atto  → 0.000'000'000'000'000'001 → Trillionstel

**IEC-Präfixe (Zweier-System)**

2 Hoch 80 → [Yi] → Yobi → 1'208'925'819'614'629'174'706'176

2 Hoch 70 → [Zi] → Zebi → 1'180'591'620'717'411'303'424

2 Hoch 60 → [Ei] → Exbi → 1'152'921'504'606'846'976

2 Hoch 50 → [Pi] → Pebi → 1'125'899'906'842'624

2 Hoch 40 → [Ti] → Tebi → 1'099'511'627'776

2 Hoch 30 → [Gi] → Gibi → 1'073'741'824

2 Hoch 20 → [Mi] → Mebi → 1'048'576

2 Hoch 10 → [Ki] → Kibi → 1'024

### Aufgabe 1

1. 2 Mikrometer
2. 234000 liter
3. 132 Milliarden Blu-ray-Discs
4. Es ist ein PDF
   Dateigrösser: 220 KB (225’776 Bytes)
   Grösse auf Datenträger: 224 KB (229’376 Bytes)
   


## Binäre Datenspeicher & Grenzen

**Kombinationen:** Formel = 2^n (n = Anzahl Bits).

z. B. 8 Bit → 256 Kombinationen.

**Speichergrössen:**

BYTE = 8 Bit, WORD = 16 Bit, DWORD = 32 Bit, QWORD = 64 Bit.

**Signed vs. Unsigned:**

**Unsigned** = nur positive Werte.

**Signed** = negatives Vorzeichen durch MSB.

**Overflow:** Bei vollem Speicher springt der Wert zurück (z. B. BYTE: 255+1=0).

<img width="1415" height="367" alt="image" src="https://github.com/user-attachments/assets/65aaf267-174d-4d7a-a4c1-5337e1e49013" />


### Aufgabe 2

1. 2 hoch 32 = 4’294’967’296
2. | Typ              | Binär                 | Dezimal   |
| ---------------- | --------------------- | --------- |
| **signed min**   | `1000 0000 0000 0000` | `-32.768` |
| **unsigned max** | `1111 1111 1111 1111` | `65.535`  |
3. 2 hoch 9 = 512 Kombinationen
4. 2 hoch 20 = 1048576 Kombinationen
5. 2 hoch 8 = 265  2 hoch 9 = 512 also 2 hcoh 9
6. 2 hoch 11 = 2048
7. WORD: +32’767 → −32’768   DWORD: +2’147’483’647 → −2’147’483’648


## Zahlensysteme

**Binärsystem (2):** Basis 2, nur 0 und 1.

**Dezimalsystem (10):** Unser normales System.

**Hexadezimal (16):** 0–9 und A–F, praktisch für Adressen.

**Umwandlungen:**

Dez → Binär: durch 2 teilen, Reste lesen.

Dez → Hex: durch 16 teilen.

Hex ↔ Binär: jede Hex-Ziffer = 4 Bit.

### Aufgabe 3

1. 60
2. 170
3. 255
4. 31
5. 170
6. 256
7. 0000 1001
8. 0110 0100
9. 0111 1111
10. 11
11. 20
12. 250
13. 0001 0010 1001 0001
14. 1011 1110 1001 0000 1011 1101
15. E0A7
16. A0F50257


## Binäres Rechnen & Überlauf

Rechnungsprogramm: https://hexed.it/

<img width="928" height="781" alt="image" src="https://github.com/user-attachments/assets/8c498541-7580-45b4-a3be-d95fc8c6ff81" />



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

## Tag 3 05.09.2025

- **Pixel:** besteht aus Rot, Grün, Blau (RGB).  
- **Farben:** ca. 16,7 Mio. (bei 24 Bit).  
- **Interlaced vs. Progressive:**  
  - Interlaced = halbe Zeilen, flimmert.  
  - Progressive = ganzes Bild, besser.  
- **8K:** 7680×4320, bis 48 Gbit/s, 60–120 Hz.  
- **Artefakte:** Bildfehler durch Kompression.  
  - Beispiele: Blöcke, Streifen, Treppen, Rauschen.  
- **PBM-Header:** enthält Format, Größe, Farbtiefe.  
- **Bildgröße ändern:** Bild wird skaliert/verzerrt.  
- **Farbtiefe erhöhen:** mehr Graustufen/Farben.  
- **pgm_6.pgm:** kleines Graustufenbild.  
- **pgm_7.pgm:** Auflösung im Header, „P“ ändern = Farbänderung.  
- **Truck_vs_Flash_Flood_5:** Video beschädigt/Artefakte.  
- **Auflösung ändern (Gimp/Pixlr):** Menü → Bildgröße/Druckgröße ändern.  
