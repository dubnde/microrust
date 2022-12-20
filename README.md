# Intro

Contains multiple build targets for getting started with the micro:bit 

# Building

```cargo build``` to build all target

```cargo build --release --bin blinking``` to build one of the targets

# Flashing

```cargo embed --release --bin blinking```

# minicomp

Note that the device might be different. Check as follows on macos

```sh 
ls -la /dev/cu.*
```

Then connect as follows

```sh
minicom -D /dev/cu.usbmodem11202 -b 115200
```

This tells minicom to open the specified serial device and set its baud rate to ```115200```. A text-based user interface (TUI) will pop out.

Can send data to the device as follows
```sh
echo 'Hello, world!' > /dev/cu.usbmodem11202

