# CMOS Synthesizer – Schematics (PDF)

This folder contains all circuit schematics exported from Autodesk EAGLE, with each file representing one functional section of the synthesizer.

Click any schematic preview below to open the full-resolution PDF.  
- SVG previews are stored in [`/Media/`](../Media/) for quick online viewing.
- Editable CAD files from Autodesk EAGLE are available in [`/PCB_Files/`](../PCB_Files/).

PDFs and SVGs share identical filenames for easy cross-referencing. For a full overview of the signal flow and circuit functions, see the main [README.md](../README.md).


---

#### Gated Oscillators 1–4 (CD4093)  
[![Gated Oscillators 5–8](/Media/02_Gated_Oscillators_5-8_CD4093.svg)](/Exports/02_Gated_Oscillators_5-8_CD4093.pdf)  
*Figure 2: Schematic of gated Schmitt trigger oscillators 1–4 (CD4093).*


#### Gated Oscillators 5–8 (CD4093)  
[![Gated Oscillators 5–8](/Media/02_Gated_Oscillators_5-8_CD4093.svg)](/Exports/02_Gated_Oscillators_5-8_CD4093.pdf)  
*Figure 2: Schematic of gated Schmitt trigger oscillators 5–8 (CD4093), identical in structure to oscillators 1–4 and providing additional clock and modulation sources.*

---

#### XOR-Based Modulators (CD4070)  
[![XOR Modulators](/Media/03_XOR-based_modulators_CD4070.svg)](/Exports/03_XOR-based_modulators_CD4070.pdf)  
*Figure 3: XOR-based square-wave ring modulators (CD4070), used to combine oscillator outputs into complex harmonic and rhythmic patterns.*

---

#### Switches and Multiplexers (CD4051, CD4053)  
[![Switches and Multiplexers](/Media/04_Switches_Multiplexers_CD405x.svg)](/Exports/04_Switches_Multiplexers_CD405x.pdf)  
*Figure 4: Analog switches and multiplexers (CD4051, CD4053) used for signal routing and selection between oscillator, divider, and external inputs.*

---

#### Binary Counters / Number Generators (CD4024)  
[![Binary Counters](/Media/05_Counters_Binary_Number_Generators_CD4024.svg)](/Exports/05_Counters_Binary_Number_Generators_CD4024.pdf)  
*Figure 5: Two 7-stage binary counters (CD4024) acting as binary number generators, providing divided clock signals (÷2–÷128) for rhythmic and timing applications.*

---

#### Power Input and Regulation  
[![Power Input](/Media/06_Power_Input.svg)](/Exports/06_Power_Input.pdf)  
*Figure 6: Power input section showing the 9–12 V DC connection, filtering, and distribution to the logic and analog circuits.*

---

#### Step Sequencer (CD4022)  
[![Step Sequencer](/Media/07_Counter_step_sequencer_CD4022.svg)](/Exports/07_Counter_step_sequencer_CD4022.pdf)  
*Figure 7: Eight-step Johnson counter sequencer (CD4022) with reset and selectable clock source for step-based rhythm generation.*

---

#### Divide-by-N Pattern Generator (CD4018 + CD4011)  
[![Divide by N](/Media/08_Divide_by-N_CD4018_CD4011.svg)](/Exports/08_Divide_by-N_CD4018_CD4011.pdf)  
*Figure 8: Divide-by-odd “pattern generator” circuit using CD4018 and CD4011, configurable for divide ratios of 3, 5, 7, and 9 to create complex rhythmic divisions.*

---

#### Ungated Oscillators and Master Clock (CD40106)  
[![Schmitt Trigger Oscillators and Clock](/Media/09_Schmitt_trigger_oscillators_9-12_and_clock_CD40106.svg)](/Exports/09_Schmitt_trigger_oscillators_9-12_and_clock_CD40106.pdf)  
*Figure 9: Schmitt trigger oscillators 9–12 and master clock oscillator (CD40106), featuring open inputs for external control via touch or light sensors.*

---

#### Pseudo-Random Generator / LFSR (CD4094, CD4070)  
[![Pseudo-Random Generator](/Media/10_PRNG_CD4094_CD4070.svg)](/Exports/10_PRNG_CD4094_CD4070.pdf)  
*Figure 10: Linear feedback shift register (LFSR) built from cascaded CD4094 shift registers with XOR feedback (CD4070) and seeding logic for pseudo-random bit generation.*

---

#### Mixing Section (LM358)  
[![Mixer](/Media/11_Mixing_Section_LM358.svg)](/Exports/11_Mixing_Section_LM358.pdf)  
*Figure 11: Four-channel mixer using an LM358 dual op-amp, providing individual input level control and one master gain stage for mono or dual-mono output.*

---

#### Rotary Switch Selectors  
[![Rotary Switches](/Media/12_Rotary_Switches.svg)](/Exports/12_Rotary_Switches.pdf)  
*Figure 12: Three 1-of-8 rotary switch selectors for assigning clock or control sources (oscillators, dividers, or external signals) to the logic sections.*

---

#### LFSR Deadlock Prevention Circuit (CD4068, CD4070, CD4077)  
[![LFSR Deadlock Prevention Circuit](/Media/Deadlock_Prevention_Circuit_CD4068_CD4070_CD4077.svg)](/Exports/Deadlock_Prevention_Circuit_CD4068_CD4070_CD4077.pdf)  
*Figure 13: Schematic of the LFSR deadlock prevention circuit using CD4068, CD4077, and CD4070. The outputs of the shift registers are combined through an AND gate (CD4068), and the resulting signal interacts with the XNOR (CD4077) and XOR (CD4070) feedback path to prevent the LFSR from locking in a static all-ones state.*

---


