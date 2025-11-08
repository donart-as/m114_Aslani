# m114_Aslani










## Tag 5 19.09.2025

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
