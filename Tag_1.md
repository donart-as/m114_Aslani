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
