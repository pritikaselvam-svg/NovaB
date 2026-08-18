# Firmware Architecture

## Target

ESP32-S3

## Proposed structure

``` text
main
├── bluetooth
├── audio
├── display
├── buttons
├── hall_sensor
├── power
└── ui_state
```

## Responsibilities

**Bluetooth:** pairing, connection state, control events.

**Display:** initialization, rendering, status updates.

**Buttons:** GPIO reading, debounce, action mapping.

**Hall sensor:** state detection and transitions.

**Audio:** I²S configuration and audio path.

**UI state:** HOME, NOW_PLAYING, VOLUME, BATTERY, BLUETOOTH, SETTINGS.

## Status

Architecture planned. Do not claim firmware functionality until it is
implemented and tested on hardware.

## Bring-up milestones

1.  Boot/serial.
2.  GPIO.
3.  Display.
4.  Buttons.
5.  Hall sensor.
6.  I²S.
7.  Amplifier/audio.
8.  Bluetooth.
9.  UI state machine.
10. Integrated power states.
