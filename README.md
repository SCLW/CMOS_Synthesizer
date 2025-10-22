<!--

Photo Board with FSR

REV A

-->


# CMOS Sound Experimentation Board



<img src="/Media/CMOS_Synth_edit_c_Yunfei_Zhang.jpg" width="1080">

# About this project

This CMOS Sound Experimentation Board is a modular experiment board for hands-on exploration of sound generation using simple logic circuits.
Developed with students at the University of Arts and Design Karlsruhe (HfG) within the [Circuitry-Based Sound](https://github.com/SCLW/Circuitry-Based-Sound)  seminar, it demonstrates how CMOS logic circuits can serve as building blocks for experimental sound creation and live performance.

Unlike conventional synthesizers or digital DSP-based systems, this project relies entirely on discrete 4000-series CMOS logic ICs, all integrated on a single PCB that also serves as the user interface.
The logic chips function as square-wave oscillators, frequency dividers, sequencers, square-wave modulators, noise sources, and pattern generators.

Through prewired connections, selectable switches, and patchable female headers and sockets, users can interconnect logic-level signals with jumper wires.
This enables the exploration of rhythmic structures, grainy textures, drones, glitches, and complex noise patterns.
The result is a compact environment for rich sound experimentation and musical interaction.

The board’s modular layout encourages direct engagement with the circuitry itself, bridging the gap between circuit design, performance, and composition.

---

| **Project Title**     | CMOS Sound Experimentation Board                                                                                                            |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| **Version**           | 2.0                                                                                                                                         |
| **Board Revision**    | Rev B                                                                                                                                       |
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

The sound generator is designed as a hands-on platform for exploring CMOS logic chips as sound generators. Its circuits are prewired for immediate operation but can also be manually interconnected to create new signal paths. All major inputs and outputs are broken out to female headers, allowing flexible patching with male-to-male jumper wires. Global I/O connections make it possible to chain multiple boards together.

The instrument has been used in university seminars, collective performances, and collaborations between electronic and acoustic musicians — from workshops in Langa (Cape Town) to performances at the ZKM Karlsruhe.

*This project is part of the ongoing teaching and research initiative [**Circuitry-Based Sound**](https://github.com/SCLW/Circuitry-Based-Sound) at the HfG Karlsruhe, which explores the relationship between electronic circuitry, interaction, and sound.*



<img src="/Media/CMOS_Synth_EDIT_c_Tobias_Erhardt.jpg" width="1080">


## Disclaimer

This material is for internal and educational purposes. Although prepared with care, errors may remain. Building this synthesizer may require additional knowledge/experience in electronics and prototyping. The materials are provided to encourage exploration and adaptation.

---

### Specifications

- **PCB:** custom 2-layer board
- **Dimensions (Board):** 278 mm × 186 mm  
- **Dimensions (Populated + Base Plate):** 284 mm × 192 mm × 35 mm
- **Power Requirements:** 9–18 V DC (typical 9 V)  <!-- Keep 9–18 V consistently; change if needed -->
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


<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/Media/Overlay_functions_dark.svg">
  <img alt="Overlay" src="/Media/Overlay_functions_bright.svg">
</picture>

Functional diagram of the CMOS Sound Experimentation Board, showing the main circuit sections and their interconnections.


### GATED OSCILLATORS 1-8 [2×]

Each of the two sections contains four gated Schmitt-trigger oscillators based on the CD4093 NAND gate IC.
These circuits generate square-wave signals, each with its own frequency potentiometer, range selector, and logic gate input for gating or modulation.


### XOR MODULATOR [2×]

Two XOR-based square-wave modulators (CD4070) for logical ring modulationto create new harmonic relationships. Each modulated output is individually accessible and can be patched into other sections.


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


### OSCILLATORS 9–13

Four auxiliary Schmitt-trigger oscillators (CD40106) with sockets for touch, light-dependent, or resistive sensors. Shares the IC also used for the clock.


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

Complete circuit schematics (PDF) for all sections are in [`/Exports/`](./Exports/).  
Editable EAGLE design files are in [`/PCB_Files/`](./PCB_Files/).  
For a browsable SVG overview that links to PDFs, see [`/Exports/README.md`](./Exports/README.md).


# Build guide

The main PCB integrates all control elements (potentiometers, toggle switches, tactile buttons) directly. No separate front panel or off-board wiring is needed. One auxiliary add-on PCB prevents LFSR deadlock and mounts directly on the main board; see [LFSR Deadlock Prevention Circuit](#lfsr-deadlock-prevention-circuit-required).


## The main board


<img src="/Media/Main_Board_Top.png" alt="Main Board Top View" width="1080">  

*CAM top view of the main board showing component outlines, silkscreen labels and pad holes.*  
 


**Main Board with component outline**  

<img src="/Media/Main_Board_Component_Outlines.svg" alt="Main Component Outlines" width="1080"> 

*Top view of the main PCB showing component outlines and mounting holes. This overlay provides a visual reference for component placement.*

<details>

<summary>PCB Reference Designators and Component List (click to expand)</summary>


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
| 4      | CD4070         | DIL14       | IC4, IC14                                           | Quad 2-input XOR                             |
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

The following is a suggested sequence that outlines the build order without step-by-step detail. Refer to the schematics in `/Exports/` and the board overlays above for orientation and placement.

1. **Main PCB**
   1) SMD resistors  
   2) SMD capacitors (see [Appendix](#Appendix))  
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

<img src="cbs_c_Yunfei_Zhang_1.gif" width="1080">

## Modifications and add-on boards

### Audio output adapter (obsolete)
Earlier revisions required a small mono audio adapter (SMT 3.5 mm jack on a daughterboard).  
In the 2024 revision B, the audio section is fixed on the main PCB.



### LFSR Deadlock Prevention Circuit (required)

<img src="/Media/Deadlock_Prevention_Board.png" width="1080">

*Deadlock prevention add-on PCB (top view).*

The LFSR can lock in an all-ones state. A small SMD add-on (CD4068, CD4070, CD4077) detects the static state and injects a seed pulse. It connects to the main board via three 1×8 and one 1×3 female headers and requires two additional wires for power (VCC and GND), which can be soldered to the unused IC18 (CD4070) through-hole pads. The wire connection is shown in the photo below. For the schematic see [here](/Exports#lfsr-deadlock-prevention-circuit-cd4068-cd4070-cd4077). 

**Wire connections for powering the LFSR deadlock prevention circuit**  
<img src="/Media/20251002_160941_c_Lorenz_Schwarz.png" alt="Wire connection detail" width="1080">

<details>

<summary>PCB Reference Designators and Component List (click to expand)</summary>


| Qty | Value   | Package       | Parts                        | Description                                    |
|-----|---------|---------------|------------------------------|------------------------------------------------|
| 4   | CD4068  | SOIC-14       | IC1–IC4                      | 8-input NAND Gate                              |
| 1   | CD4070  | SOIC-14       | IC5                          | Quad Exclusive-OR Gate                         |
| 1   | CD4077  | SOIC-16       | IC6                          | Quad Exclusive-NOR Gate                        |
| 6   | 0.1 µF  | C0805         | C1, C2, C44–C47              | Decoupling Capacitor                           |
| 1   | 10 µF   | Panasonic_D   | C3                           | Polarized Electrolytic Capacitor               |
| 3   | —       | 1×08, 2.54 mm | J1–J3                        | Female Header, 8-pin, 2.54 mm, **TH long-leg** |
| 1   | —       | 1×03, 2.54 mm | J4                           | Female Header, 3-pin, 2.54 mm, **TH long-leg** |
| 2   | —       | —             | W1–W2                        | Cut wires, insulated, for board interconnect   |

</details>
 

---

## Mechanical

The potentiometers and switches are mounted vertically on the PCB, which serves as both the circuit board and the user interface; no separate front panel. The PCB is mounted on a slightly larger acrylic base plate for rigidity and protection, fixed with 8 standoffs and M3 screws.

Note: In this revision, the two central mounting holes are slightly off-axis and not perfectly symmetrical, but this does not affect assembly or stability.

For more details see [here](/Mechanical#baseplate).

**Files for laser cutting / editing**
- [/Mechanical/Base_Plate_Dimensions.svg](/Mechanical/Base_Plate_Dimensions.svg)  
- [/Mechanical/Base_Plate_Dimensions.dxf](/Mechanical/Base_Plate_Dimensions.dxf)  
- [/Mechanical/Base_Plate_Dimensions.ai](/Mechanical/Base_Plate_Dimensions.ai)  

**Assembly hardware**
- Screws: 8 × M3, length ~9 mm  
- Standoffs: 8 × for M3, length ~3 mm, inner Ø ~3.2 mm  
- Acrylic base plate (slightly larger than PCB; pre-drill ~Ø 2.5 mm, allowing M3 threads to be tapped directly into the acrylic)


## Bill of Materials

Most components are available from Mouser Electronics and Reichelt Elektronik (Germany). The rotary switches were sourced from the German supplier [Das Musikding](https://www.musikding.de/Drehschalter-1-Pole-8-Stellungen-print) (item no. 1996).

A compiled parts list with supplier links and reference information can be found here: **[/BOM/README.md](/BOM/README.md)**

Since the design uses standard SMD parts and common 4000-series CMOS ICs, most components can be substituted with equivalent parts using the same footprints. Many values are non-critical (e.g., oscillator capacitors) and may be adjusted for experimentation.

**Shopping cart PDFs/Excel**
- [/BOM/Warenkorb_Okt05_0945.pdf](/BOM/Warenkorb_Okt05_0945.pdf)  
- [/BOM/Warenkorb_Okt05_0945.xls](/BOM/Warenkorb_Okt05_0945.xls)  
- [/BOM/Das_Musikding.pdf](/BOM/Das_Musikding.pdf)  
- [/BOM/Warenkorb_Reichelt.pdf](/BOM/Warenkorb_Reichelt.pdf)


## Additional material

In addition to the components required for assembly, a few extra items are needed for patching and experimenting with the board:

- Jumper wires (male-to-male) – various lengths for interconnecting sections
- Crocodile clamps – useful for quick testing or connecting external sensors
- Light sensors (LDRs), force-sensing resistors, etc. – for interactive control experiments

## Additional EAGLE packages

- SMT audio jack (MJ-3523-SMT-TR): [/PCB_Files/MJ-3523-SMT-TR.lbr](/PCB_Files/MJ-3523-SMT-TR.lbr)  
- SP8T rotary switch: [/PCB_Files/SP8T_Rotary.lbr](/LibraPCB_Filesries/SP8T_Rotary.lbr)


## Documentation assets

| **Category**    | **Contents**                                          | **Location**                 |
| --------------- | ----------------------------------------------------- | ---------------------------- |
| **Visuals**     | Photos, schematic SVGs, PCB overlays                  | [/Media/](/Media/)           |
| **Build Files** | Gerber files, design files, and custom EAGLE packages | [/PCB_Files/](/PCB_Files/)   |
| **Reference**   | IC datasheets                                         | [/Datasheets/](/Datasheets/) |
| **Exports**     | PDF schematics, assembly drawings, overlays           | [/Exports/](/Exports/)       |
| **BOM**         | Parts lists, shopping carts, and supplier links       | [/BOM/](/BOM/)               |
| **Dimensions**  | Board and base plate drawings                         | [/Mechanical/](/Mechanical/) |


## Variants

The first version of the CMOS sound generator was developed in 2020 as an early prototype but was later abandoned.
The design was completely reworked in 2024, resulting in two hardware revisions.
Revision B (the current version) is documented in this repository.

A photo of Revision A is shown below:  
![Revision A](/Media/Revision_A.png)

The original 2020 prototype:  
![CMOS Sound Generator 2020](/Media/DSC00055_V1_c_L_Schwarz.jpg)




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

