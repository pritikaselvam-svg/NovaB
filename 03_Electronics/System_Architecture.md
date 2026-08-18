# Electronics System Architecture

``` text
                         ┌────────────────────┐
                         │      ESP32-S3      │
                         │   Main Controller  │
                         └─────────┬──────────┘
                                   │
          ┌────────────────────────┼─────────────────────────┐
          │                        │                         │
          ▼                        ▼                         ▼
      TFT Display             Hall Sensor               Buttons
                                   │
                                   │
                                I/O
                                   │
ESP32-S3 ───── I²S ─────► MAX98357A ─────► Speaker

USB-C ─────► BQ24074 ─────► Battery
                  │
                  ▼
             AP2112K
                  │
                 3V3
                  │
          Digital electronics
```

## Power

USB-C provides external power. BQ24074 manages the rechargeable
battery/power path. AP2112K provides the regulated digital 3.3 V rail.

## Digital

ESP32-S3 is the central controller for wireless connectivity and
peripheral control.

## Audio

ESP32-S3 → I²S → MAX98357A → speaker.

## Display

The display is mechanically separated from the main PCB and connected
through a dedicated connector. The exact pinout must match the chosen
display module.

## Hall sensor

A Hall-effect sensor is connected to a GPIO and positioned relative to a
magnet/mechanical feature.

## Engineering note

Final pin assignments, current requirements, decoupling, charge settings
and display protocol must be verified against the exact component/module
datasheets before fabrication.
