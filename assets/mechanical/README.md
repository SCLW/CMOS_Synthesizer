# Dimensions and Baseplate

> Mechanical drawings and laser-cut files for the [CMOS Sound Experimentation Board](../../README.md). For overall context and the build guide see the main README.

This folder contains all mechanical information and files needed to laser-cut the acrylic baseplate for the board.

**Known issue (Rev B):** the two central mounting holes are not perfectly centered; they are offset by about 1 mm. This was an oversight in the layout process but does not affect assembly or stability. The dimension drawing below reflects the actual positions, not the symmetric ones originally intended. See [Errata](../../README.md#errata--known-issues) in the main README.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/assets/mechanical/dimensions-dark.svg">
  <img alt="Dimensions drawing" src="/assets/mechanical/dimensions-light.svg">
</picture>

*Technical dimension drawing of the main PCB showing overall dimensions and mounting hole locations. All dimensions in millimeters (mm). Drawing not to scale.*

<br><br>

## Base Plate Drawing

![Base Plate Mounting Holes and Outlines](/assets/mechanical/base-plate-dimensions.svg)  
*Drawing of the acrylic base plate showing the board outline and drill-hole positions for PCB mounting.*

## Assembly hardware

| Item | Quantity | Specification |
| --- | --- | --- |
| Acrylic base plate | 1 | Slightly larger than the PCB (see drawing for dimensions); 3 mm acrylic recommended |
| M3 screws | 8 | Pan or countersunk head, length ~9 mm |
| M3 standoffs | 8 | Length ~3 mm, inner Ø ~3.2 mm |

For the acrylic, pre-drill the mounting holes at approximately Ø 2.5 mm so that M3 threads can be tapped directly into the acrylic without a separate nut. If you prefer screwing into nuts, use clearance holes (Ø 3.2 mm) plus M3 nuts on the underside.

## File formats

| File | Purpose |
| --- | --- |
| `base-plate-dimensions.svg` | Vector drawing for laser cutting (recommended for most laser cutters) |
| `base-plate-dimensions.dxf` | Exchange format for CAD software and some laser-cutter front-ends |
| `base-plate-dimensions.ai` | Editable Adobe Illustrator source for adjusting the design |
| `dimensions-light.svg` / `dimensions-dark.svg` | PCB dimension drawings (light- and dark-mode variants) for reference |
