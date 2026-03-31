# PSRR Injector Board

Board to allow you to measure power supply rejection ratio.

Allows you to inject an AC ripple on top of your DC power supply to measure downstream. 0dB from 100Hz+. 

**[Product page]([https://amodo-design.github.io/STAGING_AMODO_WEBSITE_SW/products/psrr-injector-board/](https://amododesign.com/products/psrr-injector-board/)) · Designed by [Amodo](https://amododesign.com)**

## How it works

A clean lab supply connects on one side, and your DUT on the other. A function generator creates a signal that is AC-coupled onto the supply rail, superimposing a small ripple on top of the DC. Large series inductance (1000 µH) between the coupling node and the supply input forms an LC filter with the injection caps (880 µF per rail), keeping the supply clean and avoiding backfeed into the supply's regulation loop.

The circuit is mirrored so you can inject on either the positive or negative rail.

Note: the input impedance of your supply may be fairly low, so you may need a power amplifier between your function generator and the PSRR board. 

## Specifications

| Parameter | Value |
|---|---|
| Max voltage | ±30 V |
| Max current | 1 A |
| Injection capacitance | 880 µF per rail |
| Series inductance | 1000 µH per rail |
| Flat band | 100 Hz – 1 MHz+ |
| Low-frequency rolloff | 20 dB/dec below 100 Hz |
| Usable range | ~1 Hz (with calibration) |
| Supply input | 4 mm banana plugs |
| DUT output | 4 mm banana plugs |
| Signal injection | SMA |

## Repo layout

```
hardware/          KiCad project — schematic, PCB layout, 3D model
simulation/        LTSpice simulation file and component models
```

## Getting started

**PCB** — Open `hardware/AMODO_PSRR_INJECTOR_CBs_1.kicad_pro` in KiCad 6+.

**Simulation** — Open `simulation/psrr.asc` in LTSpice.

## License

Open-source hardware. Gerbers, schematics, and BOM are freely available — fabricate it yourself or send to your favourite PCB house.
