# Build Guides

This document covers the **hand-solder version** of the build process.

## Required Tools and Materials
- Soldering iron
- Solder wire
- Flux
- Ventilation system
- Knife or precision cutter
- Silicone adhesive or cyanoacrylate (For magnets)
- Multimeter

If working with a mouse-bited PCB, you will also need:
- Plier
- Mask
- Sandpaper

⚠️ **Note**: Be cautious when sanding PCBs. Fine dust can be hazardous.

> [!CAUTION]
> Always prioritize safety. Proper ventilation, a clean workspace, and appropriate protective equipment are **mandatory**, not optional.

## Power Switch

![Power Switch](./images/powerswitch.png)

1. Apply solder to one of the wide pads.
2. Place the switch in position and hold it while reflowing the solder to tack it in place.
3. Solder the opposite wide pad.
4. Finally, solder the three smaller legs.

Correct alignment is essential (the boss features will help position the part).

> [!CAUTION]
> Keep the switch in the **OFF position (all the way to the right)** during the entire build. This is critical.

## Reset Switch

![Reset Switch](./images/resetswitch.png)

The process is nearly identical to the power switch:

1. Pre-solder one pad.
2. Position the switch and reflow to hold it in place.
3. Solder the remaining three pads.

As with the power switch, correct alignment is important (boss features assist here).


## (Optional) LED

![LED](./images/led.png)

1. LEDs are polarized components. Even if the LEDs are of the same size, different manufacturers may indicate polarity in different ways. Refer to the corresponding datasheet to confirm the correct polarity before soldering. Align the LED according to the silkscreen markings, where the closed side represents the negative (–) terminal and the open side represents the positive (+) terminal.
2. Apply solder to one pad, then reflow it while positioning the LED to secure it in place. After that, solder the opposite pad.
3. The color of the LED may be selected and installed according to user preference. For reference, the MCU pins corresponding to each silkscreen text (R, G, B) are connected identically on both the left and right sides.

> [!CAUTION]
> LEDs are highly sensitive to heat. Ensure that you verify the proper soldering temperature and limit the soldering duration to prevent damage.

### LED Resistors

![LED Resistors](./images/led_resistors.png)

1. Install three resistors for the LEDs. These components are non-polarized and therefore have no orientation requirements.
2. Apply solder to one pad, place the resistor in position, and reflow the solder to secure it. Then proceed to solder the remaining pad.

## (Optional) ESD Protection

![ESD Protection](./images/esd_rc.png)

1. Install the capacitor and resistor for ESD protection. There are two available mounting positions, and either component (capacitor or resistor) may be placed in either location. Both are non-polarized.

2. As with previous components, apply solder to one pad, position the part, and reflow the solder to secure it. Then proceed to solder the remaining pad.


## Diodes

![Diode](./images/diodes.png)

1. Orientation is critical: align the diode’s polarity marking with the silkscreen.
2. Due to limited space (ULP switches share space originally intended for LEDs), apply a **minimal solder amount**, centered between pads.

> [!TIP]
> After soldering, temporarily place the switch above the diode to confirm there is no interference. and testing!

## Switches

![Switch](./images/switch.png)

This is often the most time-consuming step.

1. If castellated holes were not ordered, the through-holes may be damaged or deformed. Carefully trim protruding copper with a knife or nippers. Take care not to peel off the copper entirely.
2. Apply a small amount of solder to one pad.
3. Position the switch and reflow to tack it in place.
4. Solder the opposite pad, then the remaining corners (usually four points are sufficient).

![Kailh](./images/sw_back_kailh.png)
![Cherry](./images/sw_back_cherry.png)

Flip the board to solder the switch contact points:

- Ensure good contact between the switch terminals and the through-hole walls.
- Use flux and controlled heat so solder bonds properly to both.

> [!TIP]
> Above each switch are two small test pads. Use a multimeter in diode mode to confirm continuity (flow direction: right → left).

## MCU Controller

![Seeed XIAO nRF52840](./images/xiao_summary.png)

1. **Flash firmware first** to verify the MCU is functional.
   - As a quick test, short GPIO pins 4 and 5 with tweezers or wire.
   - The keyboard should register a key press (left side: **T**, right side: **Y**).

2. Position the MCU. If needed, insert header pins in the top-right and bottom-left corners for stability. (Remove after soldering)

3. Solder the castellated edges of the XIAO to the PCB pads.

⚠️ When soldering along the **outer edge (left side of the left PCB)**:
- Apply only minimal solder.
- Avoid bridges that may contact the aluminum case.

![Back MCU](./images/xiao_back.png)

4. On the PCB backside, solder the 4 additional connection points.
5. As with the switches, ensure solder bonds to both the XIAO and PCB.

![Back MCU](./images/xiao_back2.png)

6. (Optional) If you intend to use the LED, solder the additional pin located below.

## Battery

![Battery](./images/battery.png)

> [!CAUTION]
> Confirm the power switch is **OFF** before beginning.

> [!WARNING]
> Lithium-polymer (LiPo) batteries are hazardous. Even minor damage can lead to thermal runaway. Prevent shorts, punctures, or impacts. Mishandling can cause severe injury or damage to components.

1. This design does not use JST or Molex connectors. Wires are soldered directly.
2. Trim wires to length. Strip 1–2 mm of insulation and tin the exposed ends.
3. Double-check polarity (red = positive, black = negative).
4. Insulate the positive terminal with RTV silicone, Kapton tape, or another reliable method.

## (Optional) Magnet

![Magnets](./images/magnets.png)

Install magnets so that the polarity between the left and right cases is **aligned correctly**. ensuring they attract each other when closed.

Secure the magnets in place using **silicone adhesive** or **cyanoacrylate (instant glue)**.


## Case Assembly

![Assembly](./images/case_assembly.png)

1. Tilt the case slightly backward.
2. Align the rear ports first, then lower the front into place.

![Case Mount](./images/case_mounts.png)

3. Fasten the PCB to the case using screws. Tightening should be firm but not excessive.
4. If using a cover plate, place it before fastening screws.

## Finish!

![Back side](./images/back_ports.png)

Your build is now complete!
