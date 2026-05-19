# PicoFault

PicoFault is a compact, low-cost Electromagnetic Fault Injection tool designed for hobby and academic research.

PicoFault is a remix of [FaultyCat](https://github.com/ElectronicCats/faultycat) by Electronic Cats, which is itself a remix of [ChipSHOUTER PicoEMP](https://github.com/newaetech/chipshouter-picoemp) by Colin O'Flynn. Design changes in PicoFault are focused on a smaller form factor, improved BOM availability, and lower cost of production.

This project is built in KiCad. Tested before release, but it is a product that must be handled with care — please read the instructions for use.

**IMPORTANT**: The plastic shield is critical for safe operation. While the output itself is isolated from the input connections, you will still **easily shock yourself** on the exposed high-voltage capacitor and circuitry. **NEVER** operate the device without the shield.

**WARNING**: The high voltage will be applied across the SMA connector. If an injection tip (coil) is present, it will absorb most of the power. If you leave the SMA connector open, you will present a high voltage pulse across this SMA and could shock yourself. Do NOT touch the output SMA tip as a general best practice, and treat the output as if it has a high voltage present at all times.

## Features

- Voltage glitching
- Trigger using dedicated pins
- Trigger voltage reference for more accurate glitch timing
- Analog input to monitor target device status during glitching
- JTAG/SWD scanner

## Programming PicoFault

Follow the bootloader mode steps in the wiki to program the device. You can run other tasks on the microcontroller as well.

## Useful References

If you are new to Electromagnetic Fault Injection (EMFI), a couple of chapters of the Hardware Hacking Handbook are a good starting point. You can also find a practical demo of PicoEMP used in a real attack in the TI CC SimpleLink attack demo.

## Contributors

PicoFault stands on the shoulders of:

- Colin O'Flynn — original ChipSHOUTER PicoEMP hardware design and Python demo
- Electronic Cats — FaultyCat redesign, KiCad port, BOM modifications
- stacksmashing — C firmware for full PIO feature set
- Lennert Wouters — C improvements, first real attack demo
- @nilswiersma — triggering and C improvements

## License

PicoFault is adapted from FaultyCat by Electronic Cats, which is adapted from ChipSHOUTER PicoEMP by Colin O'Flynn. This project is licensed under **Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)**.