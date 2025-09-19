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

# Aufgaben 1 – Fragen & Antworten

**Wie setzt sich ein Pixel zusammen?**  
 Aus Rot, Grün, Blau (RGB).

**Wieviele Farben lassen sich darstellen?**  
 Ca. 16,7 Mio. (24 Bit).

**Unterschied Interlaced und Progressive?**  
Interlaced = Halbbilder, flimmert.  
Progressive = Ganzbilder, besser.

**Welche max. Bitrate und Bildwiederholrate hat 8K (UHD)?**  
680×4320, max. 100–200 Mbps, 60 Hz

**Was sind Artefakte?**  
Unerwünschte Bildfehler.

**Welche Artefakte gibt es?**  
Blöcke, Streifen, Treppen, Rauschen.

**Wozu ist der Header bei PBM?**  
Enthält Format, Grösse, Farbtiefe.

**Was passiert bei Bildgrössenänderung?**  
Das Bild wird vergrössert, verkleinert oder verzerrt.

**Was passiert bei Erhöhung der Farbtiefe?**  
Mehr Farben bzw. Graustufen, bessere Qualität.

**Wie gross ist das Bitmap pgm_6.pgm? Was stellt es dar?**  
<img width="470" height="458" alt="image" src="https://github.com/user-attachments/assets/5134d589-093b-413b-88a9-12f5b3bb0817" />

 - 825Kilobyte

**Welche Auflösung hat das Bitmap pgm_7.pgm ? Verändern Sie das P so, dass es die gleiche Farbe wie das F hat.**  
- 24 7
<img width="441" height="141" alt="image" src="https://github.com/user-attachments/assets/4263b297-2cee-47f4-b1b6-c485f8b6a810" />


**Was ist mit dem Video Truck_vs_Flash_Flood_5 passiert?**  
Das Video stockt/ruckelt, weil die hohe Auflösung und Bitrate die Wiedergabe verlangsamen

**Finden Sie heraus, wie man bei Gimp oder Pixlr die Auflösung und die Punktdichte ändert.**  
Ja, ich hoffe es.

## Tag 4 12.09.2025

### Verlustfreihe Komprssion

Kompression: Daten platzsparend darstellen, Redundanz entfernen.

Verlustfrei: Originaldaten wiederherstellbar.

Verlustbehaftet: Infos gehen verloren (Bilder, Audio, Video).

Verfahren

VLC (Variable Length Code): Unterschiedlich lange Codes → kurze für häufige Zeichen.

Morsecode: erstes Beispiel, aber mehrdeutig.

Huffman: präfixfrei, sehr effizient.

- RLE (Run Length Encoding): Wiederholungen durch Anzahl + Symbol speichern. Gut bei vielen gleichen Symbolen.

- LZW (Lempel-Ziv-Welch): Wörterbuchverfahren, Muster werden durch Referenzen ersetzt. Grundlage für ZIP, GIF, TIFF.

- BWT (Burrows-Wheeler): Vorbereitung, sortiert Daten um, damit andere Verfahren besser komprimieren.

[Präsentation_RLE (1).pptx](https://github.com/user-attachments/files/22420962/Prasentation_RLE.1.pptx)

## Tag 4 19.09.2025

### Verlustbehaftete Datenkompression

#### Aufgabe 1

1. **Was versteht man unter verlustloser und verlustbehafteter Kompression? In was unterscheiden sich diese? Nennen Sie Einsatzgebiete.**
Verlustlos: Originaldaten können exakt wiederhergestellt werden (z. B. ZIP, PNG, Text).

Verlustbehaftet: Originaldaten können nicht exakt wiederhergestellt werden, gewisse Infos gehen verloren (z. B. JPG, MP3, MPEG).

2. **Warum braucht es bei Multimedia (Audio/Video) verlustbehaftete Kompressionsverfahren?**
Weil Audio- und Videodaten extrem gross sind. Nur durch Weglassen von nicht wahrnehmbaren Informationen können sie ausreichend verkleinert werden, um Speicherplatz und Bandbreite zu sparen.

3. **Was ist der Kompromiss, denn man mit einer verlustbehafteten Komprimierung eingeht?**
Man spart Speicherplatz, verliert aber Qualität. Ziel ist: Datenreduktion möglichst gross, Qualitätsverlust möglichst klein.

4. **Mit welchen Verfahren erreichen Sie eine Reduktion der Bilddaten?**
Farbunterabtastung (Subsampling, z. B. 4:2:2)

Transformationen (z. B. DCT bei JPEG)

Lauflängenkodierung (RLE)

Huffman / VLC

5. **Wie kann mit Subsampling die Bilddatenmenge reduziert werden?**
Indem die Farbinformation (Chrominanz) mit geringerer Auflösung gespeichert wird, weil das menschliche Auge weniger empfindlich auf Farbdetails als auf Helligkeit reagiert.

6. **Ist Unterabtastung ein verlustloses Komprimierungsverfahren?**
Nein, es ist verlustbehaftet, weil Farbdetails unwiderruflich verloren gehen.

7. **Warum sind die Datenverluste bei Subsampling vertretbar?**
Weil das menschliche Auge Farbdetails nur schlecht unterscheiden kann, Helligkeitsinformationen aber viel wichtiger sind. Der Qualitätsverlust fällt also kaum auf.

8. **Gibt es die Unterabtastung 2:2:2?**
Nein, gebräuchlich sind Formate wie 4:4:4 (keine Unterabtastung), 4:2:2 oder 4:2:0.

9. **Ein RGB-Bild mit einer HD720 Auflösung wird mit 4:2:2 unterabgetastet. Wie gross ist die komprimierte Datei?**
RGB ohne Kompression: 3 Kanäle × 8 Bit × 1280 × 720 = 22,1 Mbit ≈ 2,76 MB
Bei 4:2:2: Luminanz bleibt voll, Farbkanäle halbiert → nur 2/3 der Daten nötig.
Ergebnis: ~1,84 MB

#### Aufgabe 2

1. **Welche Komprimierungsverfahren kommen bei JPG, WebP, BMP, TIF, GIF, HEIF und PNG zum Einsatz?**  
   - **JPG** → verlustbehaftet, DCT (Discrete Cosine Transformation) + Quantisierung + Entropiecodierung  
   - **WebP** → sowohl verlustbehaftet (DCT, Prädiktion, wie VP8) als auch verlustfrei möglich  
   - **BMP** → meist unkomprimiert, kann einfache RLE nutzen  
   - **TIF** → flexibel, kann unkomprimiert oder verlustlos (LZW, ZIP) oder verlustbehaftet (JPEG) sein  
   - **GIF** → verlustlos, basiert auf LZW, max. 256 Farben (8 Bit)  
   - **HEIF** → moderner Container, oft HEVC (H.265) als Bildkompression, verlustbehaftet oder verlustfrei  
   - **PNG** → verlustlos, basiert auf Deflate (ZIP-ähnlich)  

2. **Welche Verfahrensschritte werden bei der JPG-Komprimierung durchlaufen?**  
   1. Farbraumumwandlung (RGB → YCbCr)  
   2. Subsampling (meist 4:2:0 oder 4:2:2)  
   3. Aufteilung in 8×8 Blöcke  
   4. Diskrete Kosinustransformation (DCT) → Frequenzdarstellung  
   5. Quantisierung (Rundung, Hauptverlust)  
   6. Zickzack-Auslesen  
   7. Lauflängencodierung (RLE)  
   8. Entropiecodierung (z. B. Huffman, VLC)  


3. **Welche Verfahrensschritte führen bei JPG/DCT schlussendlich zur Datenreduktion?**  
   - **Quantisierung** (Verlust, viele Werte werden auf 0 gesetzt)  
   - **Zickzack-Auslesen + RLE + Entropiecodierung** (verlustfrei, verkleinert Dateigrösse)  


4. **Welche Nachteile kann das JPG-Komprimierungsverfahren haben?**  
   - Blockartefakte (sichtbare 8×8-Klötze bei starker Kompression)  
   - Verlust feiner Details und Kantenunschärfe  
   - Farbverfälschungen bei zu starkem Subsampling  
   - Für Texte, Logos und Grafiken ungeeignet → unscharf  


5. **Komprimierung testen – typische Ergebnisse:**  

   | Format                  | Speicher Dateigrösse | Farbtiefe | Kompressionsrate         | Artefakte                          |
   |--------------------------|---------------------|-----------|--------------------------|------------------------------------|
   | Ausgabegrösse Bildschirm | ?                   | ? Bit     | 0%                       | -                                  |
   | Nikon-D750-Shotkit-6.tif | 148.2 MB            | 48 Bit    | unkomprimiert            | -                                  |
   | Nikon-D750-Shotkit-6.RAW | 21.7 MB             | 48 Bit    | 85.1% (1:8), verlustfrei | -                                  |
   | JPEG 100%                | ~12–15 MB           | 24 Bit    | ~90%                     | keine sichtbar                     |
   | JPEG 80%                 | ~6–8 MB             | 24 Bit    | ~95%                     | leichte Artefakte an Gittern       |
   | JPEG 50%                 | ~3–5 MB             | 24 Bit    | ~97%                     | deutliche Blockartefakte           |
   | JPEG 30%                 | ~2–3 MB             | 24 Bit    | ~98%                     | starke Artefakte, unscharf         |
   | JPEG 10%                 | ~1 MB               | 24 Bit    | ~99%                     | sehr starke Artefakte              |
   | PNG ohne Verlust         | ~20–40 MB           | 48 Bit    | 60–80%                   | keine                              |
   | PNG mit Verlust          | ~10–15 MB           | 24 Bit    | 90%                      | Farbverluste, weniger schlimm als JPEG |


6. **Welche Erkenntnisse haben Sie gemacht?**  
   - **TIFF & RAW** → extrem gross, dafür höchste Qualität (Archivierung, professionelle Bildbearbeitung).  
   - **JPEG** → bei hoher Qualität kaum Unterschiede sichtbar, bei starker Kompression massive Artefakte.  
   - **PNG** → verlustfrei, ideal für Transparenz und Grafiken, aber oft grössere Dateigrösse als JPEG.  
   - **GIF** → ungeeignet für Fotos, nur für einfache Grafiken/Animationen.  
   - **WebP/HEIF** → moderner, bessere Kompressionsraten als JPEG, oft bei gleicher Qualität deutlich kleinere Dateien.  


### Aufgabe 3

1. **Im Wort «Verlustbehaftete Komprimierung» steht ja bereits der Hinweis, dass Informationen verloren gehen. Ziel ist es, im vertretbaren Bereich zu bleiben. Kann es auch übertrieben werden? Wo liegen die Grenzen?**
Informationen gehen verloren. Zu starke Kompression führt zu sichtbaren Qualitätsverlusten. Grenze: Akzeptable Bildqualität.

2. **Video sind bewegte Bilder. Wie können die dabei anfallenden Datenmengen effektiv komprimiert werden?**
Reduziert Daten durch: Unterschiede zwischen Frames speichern, Farb- und Detailreduktion, effiziente Codierung.

3. **Das Konzept "Differenzen speichern" kennen Sie in ähnlicher Weise auch aus dem IT-Bereich. Was ist wohl damit gemeint?**
Nur Veränderungen zu vorherigen Frames oder Dateien werden gespeichert, spart Speicherplatz.

4. **Was versteht man unter dem Begriff I-, B- und P-Frame?**
I-Frame: vollständiges Bild

P-Frame: Unterschiede zum vorherigen Frame

B-Frame: Unterschiede zu vorherigen und nachfolgenden Frames

5. **Was bedeutet GOP12 bezüglich I-Frames?**
I-Frame alle 12 Frames, dazwischen P- und B-Frames.

6. **Wäre GOP120 sinnvoll?**
Sehr große Abstände zwischen I-Frames, spart Speicher, aber anfällig für Artefakte; bei schnellen Bewegungen ungeeignet.

7. **Welche aktuelle GOP-Strukturen gibt es?**
Typisch 12–60 Frames, moderne Codecs nutzen flexible, variable GOPs mit hierarchischen B-Frames.


### Aufgabe 4

1. **Was ist der Unterschied zwischen einem Codec und einem Mediencontainer?**
 
Codec: Algorithmus zur Komprimierung/Dekomprimierung von Audio/Video. (z. B. H.264, H.265, AAC)
 
Container: Dateiformat, das Video, Audio und Metadaten zusammenpackt. (z. B. MP4, MKV, AVI)
 
2. **Bestimmen Sie den Codec und den Container der Dateien Truck_vs_Flash_Flood und Grundlagen_Bild-Videokompression**
 
(angenommen typische Formate, ohne MediaInfo können wir es nicht 100 % genau prüfen)
 
Datei                            Container   Video-Codec   Audio-Codec
Truck_vs_Flash_Flood             MP4         H.264         AAC
Grundlagen_Bild-Videokompression MKV         H.265         AC3
 
3. **Installieren Sie das Tool Handbrake. Welche Container, Codecs und Bildwiederholraten sind einstellbar? Finden Sie den richtigen Ort der Einstellungen.**
 
Container: MP4, MKV
 
Video-Codecs: H.264, H.265, MPEG-4, VP8/VP9
 
Audio-Codecs: AAC, MP3, AC3, FLAC
 
Framerate: 23.976, 24, 25, 29.97, 30, 50, 59.94, 60 fps oder „Same as source“
 
Ort der Einstellungen:
 
Summary → Container
 
Video → Codec & Framerate
 
Audio → Audio-Codec
 
4. **Berechnen Sie die Bandbreite in GigaBit per Second oder kurz Gbps für die Übertragung eines unkomprimierten digitalen Videosignals HD1080i50 ohne Unterabtastung und 8 Bit Auflösung pro Kanal.**
 
Daten: 1920×1080, 50 Halbbilder/s, 8 Bit/RGB (3 Kanäle)
 
Pixel pro Bild: 1920 × 1080 = 2’073’600
 
Bits pro Pixel: 8 × 3 = 24
 
Bits pro Frame: 2’073’600 × 24 = 49’766’400
 
Bits pro Sekunde: 49’766’400 × 50 = 2’488’320’000 Bit/s
 
Bandbreite: 2.488 Gbps
 
5. **Nach wie vielen Minuten unkomprimierten HD1080i50 Video wäre eine DVD-5 (Single-Layer DVD mit 4.7GB) voll?**
 
DVD-5 Kapazität: 4.7 GB = 4.7 × 1024³ Byte ≈ 37.9 Gbit (wir rechnen mit Bit)
 
Dauer = 37.9 Gbit ÷ 2.488 Gbps ≈ 15.2 Sekunden
 
Ergebnis: Nach ca. 15 Sekunden unkomprimiertem HD1080i50 Video wäre eine DVD-5 voll.
 
### Aufgabe 5
 
1. **Warum benötigt man bei einer Tonaufnahme am PC einen Analog-Digital-Wandler?**
 
Mikrofone liefern analoge Signale (Spannung variiert kontinuierlich).
 
PCs verarbeiten digitale Signale.
 
Ein ADC wandelt die analogen Signale in digitale Signale um, damit sie gespeichert oder bearbeitet werden können.
 
2. **Normalerweise besitzen PC's Mikrofon- und Lautsprecheranschlüsse. Warum braucht es hier keinen Analg-Digital- bzw. Digital-Analog-Wandler?**
 
Moderne PC-Soundkarten haben integrierte Wandler.
 
Mikrofonanschluss: ADC ist schon eingebaut, wandelt analog → digital.
 
Lautsprecheranschluss: DAC (Digital-Analog-Wandler) ist eingebaut, wandelt digital → analog.
 
Daher sieht der Benutzer keinen separaten Wandler.
 
3. **Der Analog-Digital-Wandler ihres Aufnahmegeräts hat eine Sampling-Rate von 20kHz. Sie wollen damit die Klaviervorführung ihrer grossen Schwester aufzeichnen. Kann diese Aufnahme Musikliebhaber entzücken?**
 
Nyquist-Theorem: Max. Frequenz = Sampling-Rate / 2 → 20kHz / 2 = 10 kHz
 
Klavier reicht von ~27 Hz bis ~4 kHz für Grundtöne, aber Obertöne bis ~20 kHz
 
Bei 20 kHz Sampling-Rate gehen die hohen Obertöne verloren → Aufnahme klingt gedämpft, weniger brillant
Fazit: Musikliebhaber würden die Aufnahme wahrscheinlich nicht vollständig geniessen, weil viele Details fehlen.
 
4. **Berechnen Sie den Datenstrom und den Speicherbedarf für den 90 minütigen Stereo-Audio-Track eines Films in CD-Qualität (44,1kHz bei 16Bit)**
 
Gegeben:
 
Sampling-Rate: 44.1 kHz
 
Bittiefe: 16 Bit
 
Stereo: 2 Kanäle
 
Dauer: 90 min
 
Schritt für Schritt:
 
Bits pro Sample: 16 × 2 = 32 Bit
 
Samples pro Sekunde: 44’100 × 2 Kanäle = 88’200 Samples → eigentlich besser: 44’100 Samples × 2 Kanäle = 88’200 Samples
 
Datenrate: 44’100 × 16 × 2 = 1’411’200 Bit/s ≈ 1.411 Mbps
 
Dauer: 90 min = 90 × 60 = 5’400 s
 
Speicherbedarf: 1’411’200 × 5’400 ≈ 7’619’000’000 Bit ≈ 0.95 GB
 
CD-Qualität: Datenrate ≈ 1.41 Mbps, Speicher ≈ 0.95 GB
 
5. **Berechnen Sie den Datenstrom und den Speicherbedarf für den 90 minütigen Stereo-Audio-Track eines Films in Studio-Qualität (96kHz bei 24Bit)**
 
Gegeben:
 
Sampling-Rate: 96 kHz
 
Bittiefe: 24 Bit
 
Stereo: 2 Kanäle
 
Dauer: 90 min
 
Berechnung:
 
Bits pro Sample: 24 × 2 = 48 Bit
 
Samples pro Sekunde: 96’000 × 2 Kanäle = 192’000 Samples
 
Datenrate: 96’000 × 24 × 2 = 4’608’000 Bit/s ≈ 4.608 Mbps
 
Speicherbedarf: 4’608’000 × 5’400 s ≈ 24’883’200’000 Bit ≈ 2.94 GB
 
Studio-Qualität: Datenrate ≈ 4.608 Mbps, Speicher ≈ 2.94 GB
