# Hardware Bring-up Sequence

## Stage 1: visual inspection

-   [ ] Component orientation
-   [ ] Connector orientation
-   [ ] Battery polarity
-   [ ] USB-C footprint
-   [ ] ESP32 orientation

## Stage 2: unpowered continuity

-   [ ] GND continuity
-   [ ] 3V3-to-GND short check
-   [ ] Battery path
-   [ ] USB VBUS path
-   [ ] Critical connector pins

## Stage 3: power

Test only the charging/regulation section first.

Measure USB input, charger output, regulator input and regulator output.

## Stage 4: MCU

Only after 3V3 is confirmed: - power ESP32-S3 - flash test firmware -
verify serial output

## Stage 5: peripherals

Bring up one at a time: 1. Buttons 2. Hall sensor 3. Display 4. Audio
amplifier 5. Bluetooth/audio

## Stage 6: integration

Combine subsystems only after individual blocks work.
