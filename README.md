[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

# CMOS Sound Experimentation Board

<img src="/assets/img/cmos-synth-edit_c_Yunfei_Zhang.jpg" width="1080">

## About this project

The board is both a teaching tool and a performance instrument: a low-threshold way to explore audio electronics and logic concepts while also functioning as a working sound source in artistic practice. Inexpensive 4000-series CMOS logic ICs, originally developed for general-purpose digital electronics such as calculators, digital clocks, timing circuits, and industrial control, serve as the sound generators, brought together on a single patchable interface that exposes rather than hides the signal flow. Although the signals are limited to square waves, with no envelopes, no MIDI, and no DSP, the board produces a wide range of sounds and sonic textures.

It was developed within the [Circuitry-Based Sound](https://github.com/SCLW/Circuitry-Based-Sound) seminar at HfG Karlsruhe as part of an ongoing inquiry into how self-built electronics shape experimental sound, collective performance, and arts pedagogy. Many boards have been built, modified, and played in ensemble settings and workshops. That repository documents the broader tradition of CMOS-based sound, related literature, and the underlying electronics.

Technically, the board integrates discrete 4000-series CMOS logic chips on a single PCB that also functions as the user interface. The chips operate as square-wave oscillators, frequency dividers, sequencers, modulators, noise sources, and pattern generators. Prewired connections, selectable switches, and patchable female headers and sockets let users interconnect logic-level signals with jumper wires to explore rhythmic structures, grainy textures, drones, glitches, and complex noise patterns.

---

| **Project Title**     | CMOS Sound Experimentation Board                                                                                                            |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| **Hardware Version**      | 2.0 (Rev B; first complete 2024 redesign of an earlier 2020 prototype now superseded)                                                   |
| **Documentation Release** | v1.0.0 (first archived release of this repository)                                                                                      |
| **Author / Designer** | Lorenz Schwarz                                                                                                                              |
| **Status**            | Completed                                                                                                                                   |
| **Start Date**        | April 2024                                                                                                                                  |
| **Completion Date**   | May 2024                                                                                                                                    |
| **License**           | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)                                                                                   |
| **Description**       | A modular experiment board built around 4000-series CMOS logic chips for sound generation, musical interaction, and circuit-based learning. |
| **Hardware**          | CMOS logic ICs (4000-series), analog multiplexers, potentiometers, slide and rotary switches                                                |
| **Keywords**          | single-PCB, patchable CMOS instrument, educational electronics, experimental sound, logic circuits                                          |


---

## About this documentation

This repository contains all the files and instructions required to build, study, or modify the CMOS Sound Experimentation Board:

- **PCB design files and schematics** (EAGLE)  
- **Assembly and mechanical drawings**  
- **Bill of Materials (BOM)**  
- **Reference tables and component data sheets**

Anyone is free to reproduce, adapt, or extend the instrument for artistic work, performance, or research.


## The instrument

The instrument is designed for hands-on use. Its circuits are prewired for immediate operation but can also be manually interconnected to create new signal paths. All major inputs and outputs are broken out to female headers, allowing flexible patching with male-to-male jumper wires. Global I/O connections make it possible to chain multiple boards together.

The instrument has been used in university seminars, collective performances, and collaborations between electronic and acoustic musicians, from workshops in Langa (Cape Town) to performances at the ZKM Karlsruhe.

*This project is part of the ongoing teaching and research initiative [**Circuitry-Based Sound**](https://github.com/SCLW/Circuitry-Based-Sound) at the HfG Karlsruhe, which explores the relationship between electronic circuitry, interaction, and sound.*



<img src="/assets/img/cmos-synth-edit_c_Tobias_Ehrhardt.jpg" width="1080">


## Performances and contexts of use

The board has been used as a shared platform across the Circuitry-Based Sound programme since 2024, including:

- **ng X — next_generation X festival**, ZKM, Karlsruhe (2024)
- **Bowed Electrons / IMMP**, !Khwa ttu San Heritage Centre, South Africa (2024)
- **SAE Cape Town workshop**, Cape Town, South Africa (2025)
- **Open M Art Fair**, OōEli Hangzhou Tianmuli, Hangzhou (2025)
- **MKULTRA Sound 2026**, HfG Karlsruhe (February 2026); board signals patched into a hacked VGA video signal generator to produce audiovisual patterns.

Boards built by participants have been used in solo and ensemble configurations, patched together via the chained clock and external-input headers. Demo video and context: <https://medienkunst-sound.de/works/cmos-synthesizer>.

---

<img src="/assets/img/IMG_5902_c_Yunfei_Zhang.webp" alt="Circuitry-Based Sound participants preparing in the ZKM Klangdom" width="1080">

*Circuitry-Based Sound participants preparing for the* next_generation X *festival performance in the ZKM Klangdom, Karlsruhe, 2024. Photo: © Yunfei Zhang.*

<br>

<img src="/assets/img/bowed-electrons-khwa-ttu-2024-trilogy_c_Clive_Pringle.webp" alt="Bowed Electrons concert performance at Khwa ttu, structured improvisation with Dizu Plaatjies" width="1080">

*Bowed Electrons / IMMP, concert at !Khwa ttu San Heritage Centre, South Africa, 2024 — structured improvisation with Dizu Plaatjies, combining electronic instruments and South African traditional instruments. Photo: © Clive Pringle.*

<br>

<img src="/assets/img/sae-cape-town-2025_c_Paul_Modler.webp" alt="Participants of the Circuitry-Based Sound workshop at SAE Cape Town working with the boards" width="1080">

*Circuitry-Based Sound workshop at SAE Cape Town, with participants working on the boards, 2025. Photo: © Paul Modler.*

<br>

<img src="/assets/img/IMG_9973_c_Yunfei_Zhang.webp" alt="Visitors inspecting the CMOS board at the Open M Art Fair, Hangzhou" width="1080">

*Visitors inspecting the CMOS Sound Experimentation Board at the Open M Art Fair, OōEli Hangzhou Tianmuli, China, 2025. Photo: © Yunfei Zhang.*

<br>

<img src="/assets/img/Konzert26_Jihye_Gebhart-23.webp" alt="Audiovisual performance with CMOS boards and a hacked VGA video signal generator" width="1080">

*MKULTRA Sound 2026, audiovisual performance by Yunfei Zhang and Xinyun Zhang at HfG Karlsruhe, February 2026. The board controls a hacked VGA video signal generator while simultaneously functioning as a sound source. Photo: © Jihye Gebhart.*

<br>

<img src="/assets/img/Konzert26_Jihye_Gebhart-25.webp" alt="Live-generated VGA visual projected on a wall at HfG Karlsruhe" width="1080">

*Live-generated VGA visual projected on a wall at HfG Karlsruhe during the same MKULTRA Sound 2026 performance by Xinyun Zhang and Yunfei Zhang. Photo: © Jihye Gebhart.*


## Disclaimer

This material is for educational and research purposes. Although prepared with care, errors may remain. Building this synthesizer may require additional knowledge/experience in electronics and prototyping. The materials are provided to encourage exploration and adaptation.

---

### Specifications

- **PCB:** custom 2-layer board
- **Dimensions (Board):** 278 mm × 186 mm  
- **Dimensions (Populated + Base Plate):** 284 mm × 192 mm × 35 mm
- **Power Requirements:** Operating range 9–18 V DC; recommended 9–12 V (typical 9 V battery). The oscillator frequency-range table in the [Appendix](#appendix) is calibrated at 10 V.
- **Component Types:**
  - **ICs:** CMOS 4000-series; mix of SMD and through-hole
  - **Passives:** SMD resistors (0805), SMD ceramic/electrolytic capacitors
  - **Electromechanical:** vertical PCB-mount potentiometers; slide/rotary switches (THT); 2.54 mm pin headers & sockets
- **Audio:**
  - Mono output, ~4 Vpp typical; up to synth/modular level with gains fully open
  - Master output pot provides attenuation toward line level
- **Connectors:**
  - **Power in:** 2-pin male header (2.54 mm); mating cable: 2-pos female socket → wire leads (~600 mm)
  - **Audio out:** 3.5 mm mono jack
  - **Expansion/control:** 2.54 mm female headers (various pin counts) for patching

---

## Circuit Elements on the CMOS Sound Experimentation Board

The board integrates a wide range of CMOS logic-based sound circuits, allowing direct experimentation with square-wave oscillators, counters, modulators, sequencers, and switches. All elements are accessible via female headers and can be interconnected using jumper wires to create complex rhythmic and sonic structures.

In total the board offers up to **13 oscillator positions**: 8 gated oscillators based on CD4093 (sections 1–8 below), 4 sensor-input oscillators based on CD40106 (sections 9–12), and 1 master clock (also CD40106, described as its own section).


<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/assets/img/overlay-functions-dark.svg">
  <img alt="Overlay" src="/assets/img/overlay-functions-light.svg">
</picture>

Functional diagram of the CMOS Sound Experimentation Board, showing the main circuit sections and their interconnections.


### GATED OSCILLATORS 1-8 [2×]

Each of the two sections contains four gated Schmitt-trigger oscillators based on the CD4093 NAND gate IC.
These circuits generate square-wave signals, each with its own frequency potentiometer, range selector, and logic gate input for gating or modulation.


### XOR MODULATOR [2×]

Two XOR-based square-wave modulators (CD4070) for logical ring modulation to create new harmonic relationships. Each modulated output is individually accessible and can be patched into other sections.


### SWITCH 1 OF 8 [2×]

Two CD4051 analog MUX/DEMUX sections acting as 1-of-8 selectors. Selection via three logic inputs, optionally driven by a CD4024 binary counter (0–7) to step through the switch positions automatically. The switch operates bidirectionally: it can either route one signal to one of eight destinations or select one of eight inputs to a common output.


### SWITCH 3 × 1 OF 2 [1×]

Built around a CD4053 triple SPDT analog switch, this circuit provides three independent 2-channel selectors. Each channel can switch between two input signals under binary logic control, which requires an additional logic control input. The switch operates bidirectionally: it can either route one signal to one of two destinations or select one of two inputs to a common output.

### FREQUENCY DIVIDER [2×]

Two 7-stage binary counters (CD4024) used as binary number generators (÷2…÷128). One pre-clocked from gated oscillator #8; the other can receive any selectable clock source via a rotary switch.


### SEQUENCER/COUNTER [1×]

Based on CD4022, an 8-stage Johnson counter acting as a step sequencer. It outputs sequential logic pulses across eight decoded outputs and includes a reset function. The sequencer clock can be selected via a rotary switch.

### DIVIDE BY 3, 5, 7, 9 [1×]

A divide-by-odd “pattern generator” implemented using CD4018 and CD4011. It generates rhythmic subdivisions by dividing the input clock into odd-numbered ratios (÷3, ÷5, ÷7, ÷9). The clock source is selectable through one of the rotary switches.


### OSCILLATORS 9–12

Four auxiliary Schmitt-trigger oscillators (CD40106) with sockets for touch, light-dependent, or resistive sensors. These share the same CD40106 IC as the master clock (see [Clock](#clock-1) below); inserting a variable resistor or sensor into the open pads activates each oscillator.


### CLOCK [1×]

One of the CD40106 Schmitt trigger inverters is configured as the master clock oscillator. The clock signal is routed via the rotary switches, allowing it to be assigned as a timing source to different logic sections, and can additionally be sent to an external output for synchronization between multiple boards.


### PSEUDO RANDOM NUMBER GENERATOR [1×]

Based on three interconnected CD4094 shift registers (24 stages) forming a linear-feedback shift register (LFSR). The circuit generates pseudo-random bit patterns and requires an additional adapter board for seeding and deadlock-prevention circuit using CD4068, CD4070, and CD4077 to ensure continuous operation. See [LFSR Deadlock Prevention Circuit](#lfsr-deadlock-prevention-circuit-required). The clock source can be selected via one of the rotary switches.


### MIXER [1×]

4-channel summing amplifier (LM358) with per-channel gain and master level. The mixed signal is available as mono output.

### ROTARY SWITCHES [3x]

Three Single Pole, 8-Throw rotary switches (SP8T) provide manual routing of oscillator and clock signals to different logic sections. Each switch selects one of eight possible sources, allowing flexible assignment of timing and modulation signals across the system.

| **Position** | **Source**       |
| :----------: | :--------------- |
|       1      | OSC1             |
|       2      | OSC2             |
|       3      | OSC3             |
|       4      | OSC4             |
|       5      | Master Clock     |
|       6      | OSC8 ÷ 4         |
|       7      | External Input 1 |
|       8      | External Input 2 |


---

## Schematics & design files

Complete circuit schematics (PDF) for all sections are in [`/assets/exports/`](./assets/exports/).  
Editable EAGLE design files are in [`/assets/pcb/`](./assets/pcb/).  
For a browsable SVG overview that links to PDFs, see [`/assets/exports/README.md`](./assets/exports/README.md).

> **Note on EAGLE.** The `.brd` and `.sch` files were created with Autodesk EAGLE (last standalone release 9.6.2, now discontinued). They can still be opened in Autodesk Fusion's Electronics workspace, or imported into KiCad via its built-in EAGLE importer.


## Build guide

The main PCB integrates all control elements (potentiometers, toggle switches, tactile buttons) directly. No separate front panel or off-board wiring is needed. One auxiliary add-on PCB prevents LFSR deadlock and mounts directly on the main board; see [LFSR Deadlock Prevention Circuit](#lfsr-deadlock-prevention-circuit-required).


## The main board


<img src="/assets/img/main-board-top.png" alt="Main Board Top View" width="1080">  

*CAM top view of the main board showing component outlines, silkscreen labels and pad holes.*  
 


**Main Board with component outline**  

<img src="/assets/img/main-board-component-outlines.svg" alt="Main Component Outlines" width="1080"> 

*Top view of the main PCB showing component outlines and mounting holes. This overlay provides a visual reference for component placement.*

<details>

<summary>PCB Reference Designators and Component List — main board (click to expand)</summary>

> This table lists the components for the **main board only**. The LFSR deadlock-prevention add-on has its own component list further down ([here](#lfsr-deadlock-prevention-circuit-required)) and its own entry in the [BOM file](/assets/bom/README.md#lfsr-deadlock-prevention-add-on-board).


| Qty    | Value          | Package     | Designators                                         | Description                                  |
| ------ | -------------- | ----------- | --------------------------------------------------- | -------------------------------------------- |
| 1      | 1 kΩ           | R0805       | R23                                                 | SMD Resistor                                 |
| 10     | 2.7 kΩ         | R0805       | R1–R8, R13, R15                                     | SMD Resistor                                 |
| 1      | 150 kΩ         | R0805       | R26                                                 | SMD Resistor                                 |
| 7      | 10 kΩ          | R0805       | R14, R16–R20, R27                                   | SMD Resistor                                 |
| 8      | 100 kΩ         | R0805       | R9–R12, R21–R22, R24–R25                            | SMD Resistor                                 |
| 17     | 10 µF          | PANASONIC_D | C1, C3–C7, C12–C13, C23, C49–C53                    | Electrolytic Capacitor (SMD, two optional positions) |
| 37     | 0.1 µF         | C0805       | C8–C11, C14–C17, C18–C22, C24–C29, C30–C41, C43–C48 | SMD Ceramic Capacitor                        |
| 14     | 100 kΩ         | POT_VER     | U$1–U$14                                            | Potentiometer, vertical                      |
| 2      | —              |             | S12–S13                                             | Tactile pushbutton (momentary, SMD)          |
| 8      | —              | THT         | S1–S8                                               | Toggle Switch, ON–ON                         |
| 1      | CD40106        | DIL14       | IC13                                                | Hex Schmitt Trigger Inverter                 |
| 1      | CD4011         | DIL14       | IC12                                                | Quad 2-input NAND                            |
| 1      | CD4018         | DIL16       | IC11                                                | Counter / Divider                            |
| 1      | CD4022         | DIL16       | IC9                                                 | Divide-by-8 Counter                          |
| 2      | CD4024         | DIL14       | IC6, IC8                                            | 7-stage Binary / Ripple Counter              |
| 2      | CD4051         | DIL16       | IC2, IC5                                            | 8-channel Analog Multiplexer                 |
| 1      | CD4053         | DIL16       | IC7                                                 | Triple 2-channel Analog Multiplexer          |
| 2      | CD4070         | DIL14       | IC4, IC14 (IC18 unpopulated)                        | Quad 2-input XOR                             |
| 2      | CD4093         | DIL14       | IC1, IC3                                            | Quad 2-input NAND Schmitt Trigger            |
| 3      | CD4094         | DIL16       | IC15–IC17                                           | 8-stage Shift Register                       |
| 1      | LM358          | DIL08       | IC10                                                | Dual Operational Amplifier                   |
| 1      | MBRS140        |             | D1                                                  | Schottky Protection Diode                    |
| 1      | MJ-3523-SMT-TR | SMD         | —                                                   | Female Jack Connector, 3.5 mm, surface-mount |
| 3      | —              | ROTARY      | S9–S11                                              | Rotary Switch                                |
| 8      | —              | DIL14       | —                                                   | IC Socket                                    |
| 1      | —              | DIL08       | —                                                   | IC Socket                                    |
| 8      | —              | DIL16       | —                                                   | IC Socket                                    |
| 5      | —              | 1×8 2.54    | —                                                   | Female Header                                |
| 2      | —              | 1×3 2.54    | —                                                   | Female Header                                |
| 1      | —              | 1×6 2.54    | —                                                   | Female Header                                |
| 6      | —              | 1×2 2.54    | —                                                   | Female Header                                |
| 1      | —              | 1×5 2.54    | —                                                   | Female Header                                |
| 2      | —              | 1×7 2.54    | —                                                   | Female Header                                |
| 11     | —              | 1×4 2.54    | —                                                   | Female Header                                |
| 1      | —              | 1×9 2.54    | —                                                   | Female Header                                |
| 4      | —              | 2×4 2.54    | —                                                   | Female Header                                |
| 1      | —              | 2×3 2.54    | —                                                   | Female Header                                |
| 4      | —              | 1×2 2.54    | —                                                   | Pin Header (Male)                            |


C1–C7, C8–C11, C12–C13, C14–C17, C18–C21, and C25–C29 act as timing capacitors for the Schmitt-trigger RC oscillators in combination with their corresponding resistors. These values can be substituted to tailor the oscillator frequency ranges (see frequency table).

</details>


### Assembly order

The following is a suggested sequence that outlines the build order without step-by-step detail. Refer to the schematics in `/assets/exports/` and the board overlays above for orientation and placement.

1. **Main PCB**
   1) SMD resistors  
   2) SMD capacitors (see [Appendix](#appendix))  
   3) IC sockets  
   4) ICs  
   5) Controls (potentiometers & switches)  
   6) Connectors (2.54 mm headers & sockets)

   **Important:** Do not solder the headers on the main board where the LFSR deadlock-prevention adapter will later be mounted. Solder these headers only on the adapter board, then plug into the main board.

2. **Audio output adapter (obsolete)**
   - For historical reference only; no longer required for audio output in 2024 revision.

3. **Deadlock prevention board for PRNG/LFSR circuit (required)**
   - Three 1×8 female headers + one 1×3 female header to the main board  
   - Two additional wires for VCC and GND

4. **Mechanical assembly**
   - Mount main PCB on acrylic base plate using 8 spacers and M3 screws  




## Modifications and add-on boards

### Audio output adapter (obsolete)
Earlier revisions required a small mono audio adapter (SMT 3.5 mm jack on a daughterboard).  
In the 2024 revision B, the audio section is fixed on the main PCB.



### LFSR Deadlock Prevention Circuit (required)

<img src="/assets/img/deadlock-prevention-board.png" width="1080">

*Deadlock prevention add-on PCB (top view).*

The LFSR can lock in an all-ones state. A small SMD add-on (CD4068, CD4070, CD4077) detects the static state and injects a seed pulse. It connects to the main board via three 1×8 and one 1×3 female headers, and requires two additional wires for power (VCC and GND).

The main board's original design included a CD4070 at position **IC18** as part of an on-board seeding circuit; in the current revision the add-on board takes over that function and IC18 is left unpopulated. Its through-hole pads are repurposed as solder points for the add-on's VCC and GND wires. (Note: the CD4070 *on the add-on* uses its own local designator **IC5**; the references to IC18 below are to the empty footprint on the main board.) The wire connection is shown in the photo below. For the schematic see [here](/assets/exports#lfsr-deadlock-prevention-circuit-cd4068-cd4070-cd4077). 

**Wire connections for powering the LFSR deadlock prevention circuit**  
<img src="/assets/img/20251002-160941_c_Lorenz_Schwarz.jpg" alt="Wire connection detail" width="1080">

<details>

<summary>PCB Reference Designators and Component List — LFSR deadlock-prevention add-on (click to expand)</summary>

> This table lists the components for the **LFSR deadlock-prevention add-on only**. These parts are **not** included in the main-board BOM; for supplier links and manufacturer numbers see [BOM → LFSR deadlock-prevention add-on board](/assets/bom/README.md#lfsr-deadlock-prevention-add-on-board).

| Qty | Value   | Package       | Parts                        | Description                                    |
|-----|---------|---------------|------------------------------|------------------------------------------------|
| 4   | CD4068  | SOIC-14       | IC1–IC4                      | 8-input NAND Gate                              |
| 1   | CD4070  | SOIC-14       | IC5                          | Quad Exclusive-OR Gate                         |
| 1   | CD4077  | SOIC-16       | IC6                          | Quad Exclusive-NOR Gate                        |
| 6   | 0.1 µF  | C0805         | C1, C2, C44–C47              | Decoupling Capacitor                           |
| 1   | 10 µF   | Panasonic_D   | C3                           | Polarized Electrolytic Capacitor               |
| 3   | —       | 1×08, 2.54 mm | J1–J3                        | **Arduino-style stackable** female header, 8-pin, 2.54 mm |
| 1   | —       | 1×03, 2.54 mm | J4                           | **Arduino-style stackable** female header, 3-pin, 2.54 mm |
| 2   | —       | —             | W1–W2                        | Cut wires, insulated, for board interconnect   |

</details>
 

---

## Mechanical

The potentiometers and switches are mounted vertically on the PCB, which serves as both the circuit board and the user interface; no separate front panel. The PCB is mounted on a slightly larger acrylic base plate for rigidity and protection, fixed with 8 standoffs and M3 screws.

Note: In this revision, the two central mounting holes are slightly off-axis and not perfectly symmetrical, but this does not affect assembly or stability.

For more details see [here](/assets/mechanical#base-plate-drawing).

**Files for laser cutting / editing**
- [/assets/mechanical/base-plate-dimensions.svg](/assets/mechanical/base-plate-dimensions.svg)  
- [/assets/mechanical/base-plate-dimensions.dxf](/assets/mechanical/base-plate-dimensions.dxf)  
- [/assets/mechanical/base-plate-dimensions.ai](/assets/mechanical/base-plate-dimensions.ai)  

**Assembly hardware**
- Screws: 8 × M3, length ~9 mm  
- Standoffs: 8 × for M3, length ~3 mm, inner Ø ~3.2 mm  
- Acrylic base plate (slightly larger than PCB; pre-drill ~Ø 2.5 mm, allowing M3 threads to be tapped directly into the acrylic)


## Bill of Materials

A complete build needs parts for **both PCBs**: the main board (mostly through-hole) and the small LFSR deadlock-prevention add-on (SMD-only). The compiled parts list contains a separate table for each — see **[/assets/bom/README.md](/assets/bom/README.md)** for:

- [Main board BOM](/assets/bom/README.md#main-board) — all components for the main PCB (resistors, capacitors, potentiometers, switches, ICs, connectors, rotary switches).
- [LFSR deadlock-prevention add-on BOM](/assets/bom/README.md#lfsr-deadlock-prevention-add-on-board) — SOIC ICs, 0805 passives, and the long-leg stacking headers that join the add-on to the main board.

Most components are available from Mouser Electronics and Reichelt Elektronik (Germany). The rotary switches were sourced from the German supplier [Das Musikding](https://www.musikding.de/Drehschalter-1-Pole-8-Stellungen-print) (item no. 1996).

Since the design uses standard SMD parts and common 4000-series CMOS ICs, most components can be substituted with equivalent parts using the same footprints. Many values are non-critical (e.g., oscillator capacitors) and may be adjusted for experimentation.

**Reference shopping carts (snapshots)**
- [/assets/bom/warenkorb-reichelt.pdf](/assets/bom/warenkorb-reichelt.pdf) — Reichelt cart (mechanical / sockets / headers)  
- [/assets/bom/das-musikding.pdf](/assets/bom/das-musikding.pdf) — Musikding cart (rotary switches)

> Mouser supplies the SMD passives and ICs. The compiled BOM at [/assets/bom/README.md](/assets/bom/README.md) lists every Mouser part number and direct product link; an online shopping cart snapshot is not bundled because Mouser's cart export embeds session-context URLs.


## Additional material

In addition to the components required for assembly, a few extra items are needed for patching and experimenting with the board:

- Jumper wires (male-to-male) – various lengths for interconnecting sections
- Crocodile clamps – useful for quick testing or connecting external sensors
- Light sensors (LDRs), force-sensing resistors, etc. – for interactive control experiments

## Additional EAGLE packages

- SMT audio jack (MJ-3523-SMT-TR): [/assets/pcb/MJ-3523-SMT-TR.lbr](/assets/pcb/MJ-3523-SMT-TR.lbr)  
- SP8T rotary switch: [/assets/pcb/SP8T_Rotary.lbr](/assets/pcb/SP8T_Rotary.lbr)


## Documentation assets

| **Category**    | **Contents**                                          | **Location**                                   |
| --------------- | ----------------------------------------------------- | ---------------------------------------------- |
| **Visuals**     | Photos, schematic SVGs, PCB overlays                  | [/assets/img/](/assets/img/)                   |
| **Build Files** | Gerber files, design files, and custom EAGLE packages | [/assets/pcb/](/assets/pcb/)                   |
| **Reference**   | IC datasheets                                         | [/assets/documents/](/assets/documents/)       |
| **Exports**     | PDF schematics, assembly drawings, overlays           | [/assets/exports/](/assets/exports/)           |
| **BOM**         | Parts lists, shopping carts, and supplier links       | [/assets/bom/](/assets/bom/)                   |
| **Dimensions**  | Board and base plate drawings                         | [/assets/mechanical/](/assets/mechanical/)     |


## Variants

The first version of the CMOS sound generator was developed in 2020 as an early prototype but was later abandoned.
The design was completely reworked in 2024, resulting in two hardware revisions.
Revision B (the current version) is documented in this repository.

A photo of Revision A is shown below:  
![Revision A](/assets/img/revision-a.jpg)

The original 2020 prototype:  
![CMOS Sound Generator 2020](/assets/img/dsc00055-v1_c_Lorenz_Schwarz.jpg)


---


## Errata / Known issues

The following issues are known to be present in this archived release (Hardware Version 2.0, Rev B). They do not prevent the board from being built or used, but are listed here for transparency and to flag items to verify before reproducing the design from scratch.

- **Off-axis mounting holes.** The two central mounting holes on the main PCB are offset by approximately 1 mm. This does not affect assembly or stability; the base-plate drawing in [`/assets/mechanical/`](./assets/mechanical/) reflects the actual positions, not the intended-symmetric ones.
- **CD40106 breakout-pad alignment.** Two of the paired open pads for oscillators 9–12 (CD40106 sensor inputs) sit slightly higher than the others and are not aligned on the same horizontal grid. This is a layout oversight; the pads are functional but visually inconsistent.
- **Silkscreen arrows on LFSR.** Two silkscreen arrows on the main board both point at the LFSR section. One is redundant; the labeling will be corrected in the next revision.

These items are listed in more detail under [Future Revisions](#future-revisions) below.

---

## Future Revisions

The following notes summarize proposed improvements and refinements for upcoming hardware revisions of the CMOS Sound Experimentation Board.
These suggestions are based on user feedback and observations from Rev B.

### 1. Frequency Range Switching

* Re-arrange the High / Low frequency range switch so that Low is on the left and High is on the right.
* Consider replacing the current SPDT switch with an SP3T to add a Mid-range frequency option.

### 2. Audio Output and Modulation

* Implement audio output modulation using a CD4066 analog switch for logic-controlled gating / amplitude modulation.

### 3. Circuit Optimization

* Add a dedicated power on-off switch.
* Evaluate whether the binary counter stage (CD4024) is necessary.
* One CD4070 XOR section may be sufficient for modulation tasks.
* Redesign the CD4093 NAND gate oscillator inputs with pull-down resistors.
* Re-evaluate the number of SP8T rotary switches and remove any that are redundant.
* Re-evaluate the CD4051 one-to-eight section if it is not needed.

### 4. Panel Design and Screen Printing

* Correct the screen print arrow labeling. Two arrows currently point to the LFSR section.

### 5. Visual Feedback and Indicators

* Add status LEDs throughout the board for clearer interaction and debugging.

  * Gate input LEDs
  * Audio output level LED
  * Power on/off LED
  * Optional LEDs per section to show logic activity or clock signals

### 6. Additional Features and Expandability

* Add a battery holder footprint.
* Add solder pads in parallel to the four open inputs of the CD40106 oscillator section. These pads could be used to attach force sensing resistors or other sensors for extended interaction possibilities.
* Correct the relative placement of the four CD40106 breakout pads. Two of the paired pads sit slightly higher due to a layout mistake and are not aligned on the same horizontal grid. This should be corrected for the next revision.
* The two central mounting holes are not perfectly centered and are offset by about 1 mm. This should be corrected in the next revision, and a new base plate should be designed according to the updated hole positions.

---

## Appendix

### Oscillator frequency ranges

Each gated Schmitt trigger oscillator (CD4093) includes a two-position slide switch that selects between a ceramic capacitor (smaller capacitance → higher frequency range), or an electrolytic capacitor (larger capacitance → lower frequency range). Builders can substitute either timing capacitor to shift the range. Each oscillator uses a 100 kΩ potentiometer and a 2.7 kΩ series resistor to avoid extremely high frequencies at the pot’s minimum.

**Approximate ranges at 10 V (min–max pot positions):**

| **C (µF)** | **Freq range (Hz)** |
|---:|:---|
| 0.01 | 1 230 – 26 000 |
| 0.1  | 123 – 2 600 |
| 0.22 | 56 – 1 200 |
| 0.47 | 26 – 560 |
| 1    | 12 – 260 |
| 10   | 1.2 – 26 |
| 22   | 0.56 – 12 |
| 47   | 0.26 – 5.6 |

*Ranges are approximate; real values vary with tolerances, temperature, and supply voltage.*

---

## How to cite

If you use the CMOS Sound Experimentation Board, its documentation, schematics, or photographs in research, teaching, or another open-hardware project, please cite this repository. A `CITATION.cff` file is provided so that GitHub's "Cite this repository" button gives a ready-to-use citation. This release is also archived on Zenodo with a persistent DOI.

Suggested citation:

> Schwarz, Lorenz. *CMOS Sound Experimentation Board* (v1.0.0). HfG Karlsruhe, 2026. DOI: [10.5281/zenodo.XXXXXXX](https://doi.org/10.5281/zenodo.XXXXXXX). Source: <https://github.com/SCLW/CMOS_Synthesizer>

<!-- After Zenodo mints the DOI, replace the two XXXXXXX placeholders above and the ones in CITATION.cff with the version DOI for v1.0.0. The concept DOI (which always resolves to the latest version) can also be added as a separate line if desired. -->


---

## License

Original materials in this repository — schematics, board layouts, mechanical drawings, written documentation, and photographs by the author — are licensed under the [Creative Commons Attribution 4.0 International license (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). The full legal text is included in [`LICENSE.md`](./LICENSE.md).

**Photographs by third parties.** Images whose filenames carry a `_c_<photographer>` credit (e.g., `IMG_5902_c_Yunfei_Zhang.webp`, `cmos-synth-edit_c_Tobias_Ehrhardt.jpg`, `bowed-electrons-khwa-ttu-2024-trilogy_c_Clive_Pringle.webp`, `sae-cape-town-2025_c_Paul_Modler.webp`, `Konzert26_Jihye_Gebhart-*.webp`) remain **© the named photographer** and are included here with their permission for documentation of the project. They are **not** covered by the CC BY 4.0 license of this repository; reuse requires attribution to the named photographer and, for uses beyond documenting this project, their direct permission.

**Manufacturer datasheets.** PDFs in [`/assets/documents/`](./assets/documents/) are copyright their respective manufacturers and are **not** covered by the CC BY 4.0 license of this repository; they are included for stable educational reference only. See [`/assets/documents/README.md`](./assets/documents/README.md).

