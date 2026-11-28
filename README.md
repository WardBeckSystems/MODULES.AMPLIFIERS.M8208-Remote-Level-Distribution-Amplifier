# M8208 Remote Level Distribution Amplifier · Amplifiers

Ward-Beck Systems M8208, 1995|28. Wiki page: [M8208 on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M8208.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 4 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 1 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 2 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 4 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 2 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 2 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 7 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

## Circuit description

From [1995 - M8208 - 8208-02-001 - COMPONENT LAYOUT.wp](MANUALS/1995%20-%20M8208%20-%208208-02-001%20-%20COMPONENT%20LAYOUT.wp) page 1 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

4 SA14-146 Audio Terminal Assembly 4-1

5 Connector Layout 5-1

6 Parts List 6-1 to 6-4

7 Drawings:

Schematic B 8208-02-001 Component Layout B 8208-06-001

Input Sensitivity: 0 to +10 dBm continuously variable.

Level Control Range: 65 dB.

Frequency Response: ±0.2 dB 20 Hz to 30 kHz.

Noise: 115 dB below maximum output at unity gain with zero &quot;in hand&quot;.

85 dB below the nominal +4 dBu output at unity gain with zero &quot;in hand&quot;.

Harmonic Distortion: Less than 0.25% (VCA limited) 50 Hz to 15 kHz at +14 dBu test level at unity gain with zero &quot;in hand&quot;.

Less than 0.3% 20 Hz to 20 kHz at up to +24 dBu at unity gain with zero &quot;in hand&quot;.

Less than 0.3% 20 Hz to 20 kHz at +24 dBu in with 15 dB &quot;in hand&quot;.

Input Level: 0 dBu to +8 dBu nominal for +4 dBu output. +28 dBu maximum.

Input Impedance: 30,000 Ω or greater, balanced.

Source Impedance: 600 ohms or less, balanced.

Common Mode Rejection: Better than 80 dB 20 Hz to 15 kHz.

Common Mode Voltage: +25 volts peak.

Output Level: +4 dBu nominal, +30 dBu maximum.

Output Impedance:

Output 1: 0.1 ohms or less actively balanced.

Output 2: 60 ohms resistive actively balanced.

Load Impedance: 600 ohms or greater, balanced (1 output).

Output Isolation: 40 dB, 30 Hz to 20 kHz with 60 ohm splitter network.

Remote Level: 5K linear potentiometer, up to 1000 feet (300 metres).

Phasing: The numbered terminal of the input pair and the numbered terminal of the output pair are in phase.

Power Requirements: ±22 volts DC, 65 mA.

Ambient Temperature: 0 to 50 degrees Celsius.

Dimensions: 1.00&quot; wide x 2.75&quot; high x 10.60&quot; deep.

(25.4 mm x 70.0 mm x 270.0 mm).

Weight: 0.4 lbs (175 grams).

**GENERAL**

The M8208 Remote Level Amplifier allows remote level control of an audio signal with a remotely located potentiometer.

A transformerless, actively balanced input amplifier with state of the art common mode rejection (greater than 80 dB from 20 Hz to 20 kHz); permits the M8208 to handle signals ina myriad of harsh environments with excellent results.

The signal level maybe adjusted remotely over a 65 dB range with little signal degradation. This allows the signal level to be optimally set to maintain system headroom requirements. The output stage of the M8208 is highly compliant (+30 dBu maximum output), assuring maximum dynamic range possible at line output levels. The M8208 Remote Level Amplifier has been conveniently packaged for integration into the WBS D8212 Audio Distribution System. The M8208 maybe mounted in an MF82 frame with additional M8200 series amplifiers to provide a versatile audio system. Input

The input signal to the amplifier is applied at connector pins 1 and A, and the input shield to pin B.

R1 and R2 set the amplifier input impedance to 30,000 ohms. Integrated circuit U1 with it's associated components makeup the input preamplifier circuit.

Diodes CR1 through CR4 protect the preamplifier input from excessive input signals. Trimmable capacitor C5 provides high frequency common mode rejection adjustment, while R6 provides low frequency rejection adjustment.

Sensitivity control R13 controls the feedback around preamplifier U1. The preamplifier output is coupled through C12 to the voltage controlled amplifier (VCA) consisting of U2, U3 and associated components.

The DBX2151 is a current input, current output voltage controlled amplifier. A control voltage of zero volts at pin 3 of U2 results ina current transfer ratio of 1 (i.e. no gain or loss).

For alignment purposes, this current relationship is realized by removing link LK1. A (-13) dBu signal present at U1 pin 7 is the nominal operating level. By observing the amplifier output at pins 5 and E; trim potentiometer R17 (symmetry) is adjusted for minimum distortion. Potentiometer R16 (OFFSET) is trimmed for less than 5 mV of DC output off set at U3 pin 6.

Control Amplifier

The VCA control voltage is developed by U6D. A two-slope linear approximation to a audio-taper potentiometer is provided by Q5, R46, R47, R49 and R50. This allows a standard 5K ohm linear potentiometer to be used as a level control actuator. Integrated circuit U6C provides a polarity reversal to U6D's output. Link LK1 is present to allow convenient removal of the control voltage; which is particularly useful for alignment purposes. Diode CR5 prevents the VCA from going into a positive gain operating state.

Output Amplifier

An actively balanced output amplifier is composed of two sections; the upper half comprising U4 and associated components, and the lower half consisting of U5 and it's related components.

Two direct coupled actively balanced outputs are provided at module connector pins 4 &amp; D and 5 &amp; E; output 1 and output 2 respectively.

Output 1 is a zero ohm output feed, while output 2 has a 60 ohm output impedance set by R33 and R34.

The output amplifier is capable of a maximum output of +30 dBu into abridging load of 1500 ohms or greater. A single 600 ohm load maybe driven to a +26 dBm level.

Power Supply Decoupling

The ±22 volt DC supply voltage appearing at amplifier connector pins 15 &amp; Sand 13 &amp; Pare isolated from the amplifier circuitry by fusing resistors R60 and R61. The incoming ±22 volt supplies are filtered by C38 and C39, after which they connect directly to the output amplifiers (U4 and U5). The VCA current to voltage amplifier (U3) is powered from the ±22 volt power supplies also; R22, R23, C17 and C18 further decouple the power to U3. Transistors Q6, Q7 and R62 through R66 couple the ±22 volts down to ±18 volts for use by preamplifier U1 and control amplifier U6.

Three terminal regulators U7 and U8 provide an absolute reference voltage for the control amplifier and the VCA.

The M8208 draws a quiescent 40 mA from the ±22 volt power supply. At full output into a single 600 ohm load, the supply current is 75 mA. C1 Capacitor SOT C2 &quot; 220 uF/10 V ITT 220M10 C3 &quot; 220 uF/10 V &quot; &quot;

**C4 &quot; SOT**

C5 &quot; 2-18 pF Philips 809-05003

C6 &quot; 15 pF &quot; 638-10159 C7 &quot; 4.7 uF/35 V ITT 4.7M35 C8 &quot; 15 pF Philips 638-10159 C9 &quot; 47 pF &quot; 638-34479 C10 &quot; 4.7 uF/35 V ITT 4.7M35

C11 &quot; 10 pF Philips 638-10109 C12 &quot; 10 uF/25 V ITT 10M25 C13 &quot; 10 uF/25 V &quot; &quot; C14 &quot; 10 uF/25 V &quot; &quot; C15 &quot; 22 pF Philips 638-10229

C16 &quot; 22 pF &quot; &quot; C17 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C18 &quot; 0.1 uF/100 V &quot; &quot; C19 &quot; 220 uF/10 V ITT 220M10 C20 &quot; 22 pF Philips 638-10229

C21 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C22 &quot; 0.1 uF/100 V &quot; &quot; C23 &quot; 22 pF Philips 638-10229 C24 &quot; 22 pF &quot; &quot; C25 &quot; 22 pF &quot; &quot;

C26 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C27 &quot; 0.1 uF/100 V &quot; &quot; C28 &quot; delete C29 &quot; delete C30 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN

C31 &quot; delete C32 &quot; delete C33 &quot; delete C34 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN

C35 &quot; 220 pF Philips 638-03221 C36 &quot; delete C37 &quot; delete C38 &quot; 22 uF/35 V ITT 22M35 C39 &quot; 22 uF/35 V &quot; &quot;

C40 Capacitor 10 uF/25 V ITT 10M25 C41 &quot; 10 uF/25 V &quot; &quot;

CR1-CR5 Diode Motrola 1N4148

DS1 delete DS2 delete

Q1 delete Q2 delete Q3 delete Q4 delete Q5 Transistor, NPN National 2N3906

**Q7 &quot;, PNP &quot; 2N6730**

R1 Resistor 1/4W 1% 16K2 Philips MRS25F

**R5 &quot; &quot; 8K25 &quot; &quot;**

R6 Potentiometer 5K Piher PT10V-5K R7 Resistor 1/4W 1% 75 Philips MRS25F

**R12 &quot; 1/4W 5% 3K &quot; CR25**

R13 Potentiometer 5K Piher PT10H-5K R14 Resistor 1/4W 5% 13K Philips CR25

**R15 &quot; 1/4W 1% 100K &quot; MRS25F**

R16 Potentiometer 20K Piher PT10V-20K

**R17 &quot; 50K &quot; PT10V-50K**

R18 Resistor 1/4W 5% 240K Philips CR25

**R25 * &quot; &quot; 2K4 &quot; &quot;**

R26 Resistor 1/4W 1% 75 Philips MRS25F

**R27 * &quot; 1/4W 5% 3K9 &quot; CR25**

R28 delete R29 Potentiometer delete R30 * Resistor 1/4W 5% 8K2 Philips CR25

R31 Resistor 1/4W 1% 4K75 Philips MRS25F R32 &quot; 1/4W 5% 0 ohms &quot; CR25

**R33 &quot; 1W 5% 30 &quot; PR37J**

R34 &quot; 1/4W 5% 0 ohms &quot; CR25

**R36 &quot; 1/4W 1% 4K75 &quot; MRS25F**

R37 delete

**R38 * &quot; 1/4W 5% 0 &quot; CR25**

R39 delete

**R40 * &quot; 1/4W 5% 0 &quot; CR25**

R41 delete

**R50 &quot; &quot; 9K09 &quot; &quot;**

R51 delete R52 delete R53 delete R54 delete R55 delete

R56 delete R57 delete R58 Potentiometer delete R59 delete R60 Resistor 1/2W 5% 6.8 Philips SFR25 HJ

**R65 &quot; &quot; 47 &quot; &quot;**

R66 Resistor 1/4W 5% 56K Philips CR25

**R73 &quot; &quot; 6K81 &quot; &quot;**

U1 Integrated Circuit National LM833N

**USED ON DESCRIPTION MFG MFG PART­ NUMBER**

PCB Printed Circuit Board WBS 14-278

LK1 Connector, 2P PCB MTG Berg 65645-202 LK2 Connector, 2P Aptronics 929955-06

U1-U5 8 Pin Socket Amp 640463-3

U6 14 Pin Socket &quot; 640357-3 WBS recommends the use of replacement parts made by the specified manufacturers for continued optimum equipment performance.

**REMOTE LEVEL DISTRIBUTION AMPLIFIER**

March 30, 1995

</details>

<!-- /module data -->

## Photos

_Photographs of the module itself: front, back, inside, racked._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKdFo2MUFDbWVtNk0/view?resourcekey=0-t5mT9rOoYOu4KbydnEPvMQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKdFo2MUFDbWVtNk0&resourcekey=0-t5mT9rOoYOu4KbydnEPvMQ" width="240" alt="1995 - M8208 - REMOTE LEVEL AMPLIFIER 002.jpg"></a><br><sub>1995|28 · REMOTE LEVEL AMPLIFIER 002</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcDA2TWRnbDZMb2c/view?resourcekey=0-dML9UfEOA1uMKmrAwHKXUg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcDA2TWRnbDZMb2c&resourcekey=0-dML9UfEOA1uMKmrAwHKXUg" width="240" alt="1995 - M8208 - REMOTE LEVEL AMPLIFIER 003.jpg"></a><br><sub>1995|28 · REMOTE LEVEL AMPLIFIER 003</sub></td></tr>
</table>

## Schematics

_Electrical drawings: schematics (-02-), functional diagrams (-01-), component layouts (-06-), wiring (-09-), PCB files (.pcb .dsn), and beside each scan its `(EXTRACTED).svg`: the vectors traced from it._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1mgdA89Fk11XlB0KuC3BDKfFTTM27gAaS/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1mgdA89Fk11XlB0KuC3BDKfFTTM27gAaS" width="240" alt="1996 - M8208 - DOC - 96017-01-001 - ISSUEI REMSION.jpg"></a><br><sub>1996|29 · DOC - 96017-01-001 - ISSUEI REMSION · <a href="SCHEMATICS/1996%20-%20M8208%20-%20DOC%20-%2096017-01-001%20-%20ISSUEI%20REMSION%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## Manuals and documents

_Manuals and manual pages, price lists, RTO-144 connection sheets, brochures, ads and other document scans._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKeU5IZXVCejdyWWc/view?resourcekey=0-FwkJeha9NOW07OrW6VzOuA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKeU5IZXVCejdyWWc&resourcekey=0-FwkJeha9NOW07OrW6VzOuA" width="240" alt="1995 - M8208 - REMOTE LEVEL AMPLIFIER 001.jpg"></a><br><sub>1995|28 · REMOTE LEVEL AMPLIFIER 001</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1ablzAyX5hRqSIyJLiOUdoC4xy5y68tn3/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1ablzAyX5hRqSIyJLiOUdoC4xy5y68tn3" width="240" alt="1996 - M8208 - DOC - 2021-3-16-23-22-21.jpg"></a><br><sub>1996|29 · DOC - 2021-3-16-23-22-21</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1I2WFw1jBIz4zETuZq8-guR-XkERKTwnl/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1I2WFw1jBIz4zETuZq8-guR-XkERKTwnl" width="240" alt="1996 - M8208 - DOC - Scan_20210323.jpg"></a><br><sub>1996|29 · DOC - Scan_20210323</sub></td></tr>
</table>

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [1996 - M8208 - DOC - 96017-01-001 - ISSUEI REMSION.kicad_sch](KICAD/1996%20-%20M8208%20-%20DOC%20-%2096017-01-001%20-%20ISSUEI%20REMSION.kicad_sch)
- [M8208.kicad_sym](KICAD/M8208.kicad_sym)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
