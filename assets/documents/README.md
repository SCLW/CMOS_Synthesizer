# IC Datasheets — Third-Party Reference Material

> Component datasheets for the [CMOS Sound Experimentation Board](../../README.md). For overall context, build guide, and licensing of original repository materials see the main README.

This folder contains unmodified manufacturer datasheets for most of the 4000-series CMOS logic ICs and the LM358 operational amplifier used on the board. They are bundled here so that anyone building, studying, or archiving this design has stable offline access to the electrical and pin-out information referenced throughout the schematics.

## Copyright and license

The PDFs in this folder are **© their respective manufacturers** (primarily Texas Instruments). They are **not** covered by the [CC BY 4.0 license](../../LICENSE.md) that applies to the original materials of this repository. They are reproduced here unmodified for educational and documentation purposes only.

If you redistribute or republish this repository, please be aware that the redistribution terms of each datasheet are set by its manufacturer, not by this project. For the authoritative, current version of any datasheet, please consult the manufacturer's website directly.

## Contents

| File | Component | Function on the board |
| --- | --- | --- |
| `cd40106b.pdf` | CD40106B | Hex Schmitt-trigger inverter (oscillators 9–12, master clock) |
| `cd4012b.pdf` | CD4012B | Dual 4-input NAND (general reference) |
| `cd4018b.pdf` | CD4018B | Presettable divide-by-N counter (pattern generator) |
| `cd4022b.pdf` | CD4022B | 8-stage Johnson counter (step sequencer) |
| `cd4051b.pdf` | CD4051B | 8-channel analog multiplexer |
| `cd4068b.pdf` | CD4068B | 8-input NAND (LFSR deadlock prevention) |
| `cd4070b.pdf` | CD4070B | Quad 2-input XOR (XOR modulator, LFSR feedback) |
| `cd4093b.pdf` | CD4093B | Quad 2-input NAND Schmitt trigger (gated oscillators 1–8) |
| `cd4094b.pdf` | CD4094B | 8-stage shift register (LFSR core) |
| `lm358.pdf` | LM358 | Dual operational amplifier (mixing section) |

The CD4011 (quad 2-input NAND, IC12 on the main board), CD4024 (7-stage binary counter), CD4053 (triple SPDT analog switch) and CD4077 (quad XNOR, on the deadlock-prevention add-on) are also used on the board but their datasheets are not bundled here; please consult the manufacturer's website for the current PDFs.
