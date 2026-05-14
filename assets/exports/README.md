# CMOS Sound Experimentation Board — Schematics (PDF)

> Functional-block schematics for the [CMOS Sound Experimentation Board](../../README.md). For overall context, build guide, and licensing see the main README.

This folder contains all circuit schematics exported from Autodesk EAGLE, with each file representing one functional section of the board.

Click any schematic preview below to open the full-resolution PDF.  
- SVG previews are stored in [`/assets/img/`](../img/) for quick online viewing.
- Editable CAD files from Autodesk EAGLE are available in [`/assets/pcb/`](../pcb/).

PDFs and SVGs share identical filenames for easy cross-referencing. For a full overview of the signal flow and circuit functions, see the main [README.md](../../README.md).


---

#### Gated Oscillators 1–4 (CD4093)  
[![Gated Oscillators 1–4](/assets/img/01-gated-oscillators-1-4-cd4093.svg)](/assets/exports/01-gated-oscillators-1-4-cd4093.pdf)  
*Figure 1: Schematic of gated Schmitt trigger oscillators 1–4 (CD4093).*


#### Gated Oscillators 5–8 (CD4093)  
[![Gated Oscillators 5–8](/assets/img/02-gated-oscillators-5-8-cd4093.svg)](/assets/exports/02-gated-oscillators-5-8-cd4093.pdf)  
*Figure 2: Schematic of gated Schmitt trigger oscillators 5–8 (CD4093), identical in structure to oscillators 1–4 and providing additional clock and modulation sources.*

---

#### XOR-Based Modulators (CD4070)  
[![XOR Modulators](/assets/img/03-xor-based-modulators-cd4070.svg)](/assets/exports/03-xor-based-modulators-cd4070.pdf)  
*Figure 3: XOR-based square-wave ring modulators (CD4070), used to combine oscillator outputs into complex harmonic and rhythmic patterns.*

---

#### Switches and Multiplexers (CD4051, CD4053)  
[![Switches and Multiplexers](/assets/img/04-switches-multiplexers-cd405x.svg)](/assets/exports/04-switches-multiplexers-cd405x.pdf)  
*Figure 4: Analog switches and multiplexers (CD4051, CD4053) used for signal routing and selection between oscillator, divider, and external inputs.*

---

#### Binary Counters / Number Generators (CD4024)  
[![Binary Counters](/assets/img/05-counters-binary-number-generators-cd4024.svg)](/assets/exports/05-counters-binary-number-generators-cd4024.pdf)  
*Figure 5: Two 7-stage binary counters (CD4024) acting as binary number generators, providing divided clock signals (÷2–÷128) for rhythmic and timing applications.*

---

#### Power Input and Regulation  
[![Power Input](/assets/img/06-power-input.svg)](/assets/exports/06-power-input.pdf)  
*Figure 6: Power input section showing the DC connection (operating range 9–18 V, recommended 9–12 V), filtering, and distribution to the logic and analog circuits.*

---

#### Step Sequencer (CD4022)  
[![Step Sequencer](/assets/img/07-counter-step-sequencer-cd4022.svg)](/assets/exports/07-counter-step-sequencer-cd4022.pdf)  
*Figure 7: Eight-step Johnson counter sequencer (CD4022) with reset and selectable clock source for step-based rhythm generation.*

---

#### Divide-by-N Pattern Generator (CD4018 + CD4011)  
[![Divide by N](/assets/img/08-divide-by-n-cd4018-cd4011.svg)](/assets/exports/08-divide-by-n-cd4018-cd4011.pdf)  
*Figure 8: Divide-by-odd “pattern generator” circuit using CD4018 and CD4011, configurable for divide ratios of 3, 5, 7, and 9 to create complex rhythmic divisions.*

---

#### Ungated Oscillators and Master Clock (CD40106)  
[![Schmitt Trigger Oscillators and Clock](/assets/img/09-schmitt-trigger-oscillators-9-12-and-clock-cd40106.svg)](/assets/exports/09-schmitt-trigger-oscillators-9-12-and-clock-cd40106.pdf)  
*Figure 9: Schmitt trigger oscillators 9–12 and master clock oscillator (CD40106), featuring open inputs for external control via touch or light sensors.*

---

#### Pseudo-Random Generator / LFSR (CD4094, CD4070)  
[![Pseudo-Random Generator](/assets/img/10-prng-cd4094-cd4070.svg)](/assets/exports/10-prng-cd4094-cd4070.pdf)  
*Figure 10: Linear feedback shift register (LFSR) built from cascaded CD4094 shift registers with XOR feedback (CD4070) and seeding logic for pseudo-random bit generation.*

---

#### Mixing Section (LM358)  
[![Mixer](/assets/img/11-mixing-section-lm358.svg)](/assets/exports/11-mixing-section-lm358.pdf)  
*Figure 11: Four-channel mixer using an LM358 dual op-amp, providing individual input level control and one master gain stage for mono or dual-mono output.*

---

#### Rotary Switch Selectors  
[![Rotary Switches](/assets/img/12-rotary-switches.svg)](/assets/exports/12-rotary-switches.pdf)  
*Figure 12: Three 1-of-8 rotary switch selectors for assigning clock or control sources (oscillators, dividers, or external signals) to the logic sections.*

---

#### LFSR Deadlock Prevention Circuit (CD4068, CD4070, CD4077)  
[![LFSR Deadlock Prevention Circuit](/assets/img/deadlock-prevention-circuit-cd4068-cd4070-cd4077.svg)](/assets/exports/deadlock-prevention-circuit-cd4068-cd4070-cd4077.pdf)  
*Figure 13: Schematic of the LFSR deadlock prevention circuit using CD4068, CD4077, and CD4070. The outputs of the shift registers are combined through an AND gate (CD4068), and the resulting signal interacts with the XNOR (CD4077) and XOR (CD4070) feedback path to prevent the LFSR from locking in a static all-ones state.*

---


