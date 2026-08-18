# Component Selection

  Component        Function                     Why
  ---------------- ---------------------------- ---------------------------------
  ESP32-S3-WROOM   MCU/wireless                 Wireless + flexible peripherals
  BQ24074          Li-ion charging/power path   Dedicated battery management
  AP2112K          3.3 V LDO                    Compact digital regulation
  MAX98357A        I²S amplifier                Digital audio path
  A1104xLH         Hall sensor                  Solid-state magnetic sensing
  TFT display      Ambient interface            Local contextual information
  USB-C            Power input                  Common modern connector
  Li-ion battery   Energy storage               Rechargeable portable power
  Speaker          Audio output                 Acoustic transducer
  Push buttons     User input                   Tactile controls

## Verification before fabrication

-   [ ] Verify exact ESP32 module pinout.
-   [ ] Verify BQ24074 ISET/ILIM/TS/EN1/EN2/CE configuration.
-   [ ] Verify AP2112K exact output variant and capacitor requirements.
-   [ ] Verify MAX98357A package, supply and speaker requirements.
-   [ ] Verify exact display voltage, protocol and pinout.
-   [ ] Verify Hall sensor variant and output.
-   [ ] Verify USB-C footprint and CC resistor implementation.
-   [ ] Verify battery protection requirements.
