# snappergps-pressure-sensor-daughterboard

*Author: Jonas Beuchert*

Pressure sensor daughter-board for SnapperGPS receiver (v1.0.x or v2.0.x).

## Table of contents

* [Files](#files)
* [Manufacturing](#manufacturing)
* [Components](#components)
* [Assembly](#assembly)
* [Flashing](#flashing)
* [Usage](#usage)
* [Acknowledgements](#acknowledgements)

## Files

* `gerber`: Gerber files and drill file for manufacturing the daughter-board.
* `bom.csv`: Bill of materials of the daughter-board components.
* `pcb.json`: PCB layout file of the daughter-board. Created with EasyEDA.
* `pick-and-place.csv`: Centroid / pick-and-palce file for assembly.
* `schematic.json`: Schematic file of the daughter-board. Created with EasyEDA.
* `schematic.pdf`: Schematic as PDF.

## Manufacturing

* Get some PCBs manufactured by a PCB manufacturer of your choice.
(I used [JLCPCB](https://jlcpcb.com), [Aisler](https://aisler.net/), or [PCBWay](https://www.pcbway.com/) in the past.)
For this, upload the `gerber` folder to the manufacturer's website.
Choose a two-layered PCB with size 3.56 mm x 11.68 mm.

* If you want, you can also let the manufacturer assemble the board(s) for you.

## Components

| designator   | quantity | description      | footprint | manufacturer part     | manufacturer     | supplier | supplier part | price   |
|--------------|---------:|------------------|-----------|-----------------------|------------------|----------|---------------|--------:|
| C30          | 1        | 100 nF capacitor | 0402      | CL05B104KO5NNNC       | SAMSUNG          | LCSC     | C1525         | $0.001  |
| U2           | 1        | pressure sensor  |           | MS583730BA01-50       | TE Connectivity  | LCSC     | C2887941      | $11.391 |
| R32, R34     | 2        | 10 kΩ resistor   | 0402      | 0402WGF1002TCE        | UNI-ROYAL        | LCSC     | C25744        | $0.001  |

## Assembly

* Solder the two resistors, the capacitor, and the pressure sensor on the daughterboard.
Ensure that the marked corner of the pressure sensor is aligned with the mark on the PCB.
I recommend solder paste and a hot plate (or hot air gun) for soldering.

* Solder the assembled daughter-board on a SnapperGPS receiver.
Note that only version v1.0.x and v2.0.x are compatible, **not** v2.1.x or 2.2.x).
The five pads on the back of the daughter-board should connect to the five pads on the SnapperGPS receiver.
The daughter-baord shall be orientated such that the pressure sensor sits in the corner of the SnapperGPS receiver.

* Package the whole assembly in a water/weather-proof way, which still exposes the gel-filled cavity of the pressure sensor.
For example, I used silicon potting for this, but you can also use a rigid housing with a 3.07 mm hole combined with an O-ring with inner diameter 1.8 mm and cross-section diameter 0.8 mm.

## Flashing

* Go to [https://snappergps.info/flash](https://snappergps.info/flash).
* Connect the SnapperGPS receiver to your computer via USB.
* Pair the SnapperGPS receiver.
* Select the `SnapperGPS-PressureSensor` firmware.
* Flash the firmware.

## Usage

Find instructions in the firmware repository.

<img width="1236" height="548" alt="image" src="https://github.com/user-attachments/assets/740ee711-b4c0-4feb-8932-36c4a471b9b5" />

## Acknowledgements

This SnapperGPS daughter-board was developed by
[Jonas Beuchert](https://profiles.cardiff.ac.uk/staff/beuchertj)
in the School of Computer Science and Informatics
of Cardiff University.

This repository is licensed under a
[Creative Commons Attribution 3.0 International License][cc-by].

[![CC BY 3.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/3.0/
[cc-by-image]: https://i.creativecommons.org/l/by/3.0/88x31.png
