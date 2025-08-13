> [!WARNING]
> work in progress.
 

# DELTA OMEGA

A wireless/wired 3x5+2 split keyboard using **Cherry MX ULP** switches.

## Overview

* Supports wireless and wired.
  - Hybrid: One firmware. BLE or Wired between halves. Runtime switching. BLE or USB via Host.
  - Single: BLE Firmware or Wired firmware. BLE or USB via Host or Dongle.
* Default aluminum case (other materials optional).
* ZMK firmware support.
* Choc spacing layout.
* 7mm low-profile case.

## Aluminum Case

The aluminum case has been modeled to be as cost-effective as possible, given my machining limitations.
It is designed under the assumption of **3-axis CNC machining** with minimal tool changes. ideally using a single endmill where possible.
I am not a machining expert, so if you have suggestions for improvement, please share them.

Case variants:
 - Hybrid
 - Wireless Only: without Interconnection USB-C port.

## PCB

The PCB design contains **both left and right halves** in a single file.
While it’s possible to panelize and order them as one PCB using mouse bites or v-cut, I recommend ordering them as **two separate boards** for cleaner edge finishing. The cost difference is negligible.

This design does **not** use a reversible PCB because it’s intended for a bottomless style case where the PCB is exposed.

## Why XIAO Plus?

The **Seeed XIAO nRF52840 Plus** is a recently released version with additional pins.
I chose it to enable **direct GPIO key scanning without diodes**.

While diodes could be installed inside the switch footprint, the assumption here is that if you’re using **Cherry MX ULP** switches, you’re already working with a hot plate or hot air station. so we will solder the XIAO as an SMD part directly.

## Bill of Materials 

| Item    | Quantity | Notes    |
| -------------------------------- | -------- | ------------------------------------------------------------------- |
| Seeed XIAO nRF52840 Plus   | 2        | Controller                                                          |
| PCB (Left + Right)   | 1 each   | Ordered separately for cleaner edges                                |
| Case (Left + Right)     | 1 each   | Aluminum by default                                                 |
| Cherry MX ULP switches   | 34       | -                                                                   |
| USB-C receptacle, 16-pin    | 2        | For wired version                                                   |
| Power switch MK-12C02   | 2        | For wireless version                                                |
| LiPo 3.7 V battery  | 2        | Max size: 25.2 × 17.7 × 4.2 mm (wireless)                           |
| M2 thin flat-head screws, 4 mm Length | 10       | -                                                                   |
| Reset switch (SMT, 4×4 mm)   | 2        | 0.8 mm height recommended; optional—can short with tweezers instead |
| Feet       | 8        | Any shape/size; should be taller than screw heads                   |
| BLE port cover    | 2        | Separate model available                                            |
| 4.7kΩ Resistor 0603 | 1 | For the hybrid connection between Wireless and Wired |
