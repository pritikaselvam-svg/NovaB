# Power Architecture

``` text
USB-C VBUS
     │
     ▼
BQ24074
     ├────────► Li-ion Battery
     │
     ▼
AP2112K
     │
     ▼
3V3
 ├── ESP32-S3
 ├── Hall sensor
 ├── Display logic if compatible
 └── Other digital peripherals
```

## BQ24074

Document and verify: - ISET - ILIM - TS - EN1 - EN2 - CE - BAT - OUT -
GND/VSS

Exact resistor values and control states must be checked against the
selected BQ24074 datasheet and intended battery.

## 3.3 V

AP2112K input/output capacitors must be placed according to the
datasheet and close to the regulator pins.

## USB-C

For a USB-C power-only sink architecture, CC pins require appropriate
pull-down resistors. Verify the exact connector footprint and
implementation.

## Validation

Measure USB VBUS, charger output, battery voltage, regulator
input/output, 3V3 ripple, charging current and regulator temperature.

Do not connect a battery to a newly fabricated board until the power
path has been inspected and checked.
