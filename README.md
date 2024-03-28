This is a fork of https://github.com/pico-coder/sigrok-pico with a single change that offsets the ADC voltage to change the PulseView display to display 1/2scale (0x40) as 0V.

The chane is to accommodate the input hardware developed for Silicon Chip magazine.

Please DO NOT offer pull requests to this fork, it will be updated from time to time from the main repo.

#
# sigrok-pico
Use a raspberry pi pico (rp2040) as a logic analyzer and oscilloscope with sigrok.
This implementation uses the pico SDK CDC serial library to communicate with sigrok-cli/pulseview through a sigrok driver.

## Directories:

pico_pgen is a simple digital function generator useful for creating patterns to test.

pico_sdk_sigrok is the pico sdk C code for the PICO RP2040 device.

The latest libsigrok code exists as a fork at https://github.com/pico-coder/libsigrok

## Files
PICOBuildNotes.md - build notes for building the PICO device assuming you have gone through the PICO C SDK "getting started with PICO".

SigrokBuildNotes.md - rough libsigrok build notes which will be depracated once raspberrypi_pico is mainline

GettingStarted.md - quick run down on setting things up.

AnalyzerDetails.md - details on supported modes of the analyzer and various limitations.

SerialProtocol.md - details of the "over the wire" protocol used between the sigrok driver and the device.
