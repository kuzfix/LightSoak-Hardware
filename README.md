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
    - 1X: 