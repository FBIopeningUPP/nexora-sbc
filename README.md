# Nexora SBC

Nexora SBC is a single-board computer project based on the STM32MP157. The design is in progress. The five schematic sheets have placement headings and local libraries, and the PCB is a blank starting point.

## Open the project

Open [hardware/Nexora-SBC.kicad_pro](hardware/Nexora-SBC.kicad_pro) in KiCad 10.

| Sheet | Circuits |
| --- | --- |
| 1 | STM32MP157 DDR interface and DDR3L |
| 2 | eMMC, SPI flash, microSD, boot and clocks |
| 3 | HDMI, LCD and Ethernet |
| 4 | Input power, regulators and SoC supplies |
| 5 | USB, CAN, debug and expansion |

The `Nexora` libraries contain project-specific entries and use relative paths. Generic parts and common packages use the standard KiCad 10 libraries. Set the component value and footprint to match the selected part. Use the same `+3V3` net wherever the guide shows the Rev B1 `+3.3V` / `VDD` aliases.

The STM32MP157 and DDR3L VRML files are approximate body envelopes. Some other footprints use the source project's generic package models. Seven footprints have no verified 3D model.

## Design submission files

| Location | Contents |
| --- | --- |
| `hardware/` | KiCad project, PCB, the five schematic sheets and the project-local libraries |
| `manufacturing/` | Planned home for the final `gerbers.zip` and sourcing BOM with part links |
| `docs/images/` | Planned home for images of the finished schematic, PCB and assembly |
| `firmware/` and `mechanical/` | Add project-specific firmware and assembly files if used |

The [Fallen submission guidelines](https://fallen.hackclub.com/docs/submitting) describe the evidence expected for a finished design. The manufacturing exports and design images depend on completing the schematic and board layout first.

## Credits

Circuit and project-specific library assets derive from [OLIMEX LTD's STMP157-OLinuXino-LIME2 Rev B1](https://github.com/OLIMEX/OLINUXINO/tree/master/HARDWARE/STMP157-OLinuXino-LIME2), licensed under [CC BY-SA 3.0 US](https://creativecommons.org/licenses/by-sa/3.0/us/). Library changes include migration to KiCad 10, project-local model paths, value-specific symbols for custom parts, and two replacement BGA envelopes.

Footprints sourced separately from [OLIMEX's KiCad libraries](https://github.com/OLIMEX/KiCAD) are licensed under [Apache 2.0](hardware/libraries/LICENSE-footprints.txt). The SMA footprint uses the two copper pads from the Rev B1 board.
