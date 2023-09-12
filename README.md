# LightSoak Hardware
This repository contains hardware design files for LightSoak project, developed in scope of my Master's thesis. For Firmware, quick start quide and a basic hardware description, see https://github.com/mrmp17/LightSoakFW-STM. For Python data logger, see https://github.com/mrmp17/LightSoakFW-Python.

LightSoak hardware can be used standalone via a Command Line Interface over USB or with a Python data logger to implement complex measurement sequences. See quick start quide at https://github.com/mrmp17/LightSoakFW-STM for more information.

## Hardware specs

### Voltage measurement channels
- Measurement range: **0-1.5V**
- ADC resolution: **12bit (STM32G4 integrated)**
- Sample rate: **100kHz**
- Differential input resistance: **3.3MOhm +- 10%**
- Noise performance: *TBD*. Use *getnoise* CLI command to evaluate.
- Accuracy: **+-(0.25% of measurement + 0.75mV)**

#### Voltage accuracy report
![Accuracy report:](docs/calreport_5-9-2023.png)

### Current measurement channels
- Measurement ranges:
    - 1X: up to 4700uA
    - 10X: up to 400uA
    - 100X: up to 40uA
    - 1000X: up to 4uA
- ADC resolution: **12bit (STM32G4 integrated)**
- Sample rate: **100kHz** (simultaneous sampling with voltage channels)
- Noise performance: *TBD*. Use *getnoise* CLI command to evaluate.
- Accuracy: *TBD*

### Temperature control
- handled by a TEC-1091 module mounted to the main board. See https://www.meerstetter.ch/products/tec-controllers/tec-1091 for specs.

### Illumination (verification TBD)
- Light output stbility: **+-1% (With LED temperature compensation)**
- Constant current range: **10mA to 1.4A**
- Settling time: **20uS to 1%, over current range**
- See https://downloads.cree-led.com/files/ds/x/XLamp-CXA2530.pdf for LED specs
