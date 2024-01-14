# Blinky_esp32
Test ability to code generate imbedded application software for deployement ESP32 System-on-a-Chip (SOC) module from a UML state chart.

![SM_of_Blinky](https://github.com/smr547/Blinky_esp32/assets/4327895/9005056c-fb60-4da3-ab45-49a0c3f24e8f)


## Background
I'm inspired by the work of [Miro Samek](https://www.linkedin.com/in/samek) from [Quantum Leaps](https://www.state-machine.com/). Miro's
[Modern System Embedded Programming Course](https://www.youtube.com/watch?v=TJQmT5j1TsM&list=PLb-MsRpo_wlLW0EWRpAqnbbDsf4kxSI1x) on YouTube 
provide inspiration to any software engineer with the dream of code-generating production-ready applications from high level UML diagrams.
Quantum Leaps provides a truely [excellent set of tools](https://www.state-machine.com/products) that can be employed by Software Engineers under generous licence conditions.

## This project

This is a simple proof of concept project that aims to code-generate the LED blinking application for deployment to the [Espressif ESP Module](https://www.espressif.com/en/products/modules/esp32)
The project combines several components:

* [QM modelling tool](https://www.state-machine.com/qm/index.html) from [Quantum Leaps](https://www.state-machine.com/) -- Verison 5.2.5 (Generates code for QP/C++ version >= 7.0.0) 
* [QP/C++ port for ESP32 using Arduino Plaform SDK](https://github.com/vChavezB/qpcpp_esp32) (Based on QP/C/C++ version 7.2.2)
* [Microsoft Visual Studio Code](https://code.visualstudio.com/) -- (vscode) an excellent IDE
* [PlatformIO](https://platformio.org/) plugin for vscode that outputs to broad range of COC targets

Note: the latest [QM Modelling tool](https://www.state-machine.com/qm/index.html) (version 6.1.1) generates code which runs on QP/C/C++ version 7.3.0 which is incompatible with the current [ESP32 port](https://github.com/vChavezB/qpcpp_esp32)

## Getting started

1. Clone this repo
2. cd Blinky_esp32
3. Run ``qm`` version 5.2.5 and open the ``Blinky_esp32`` model
4. Generate the code
5. Open the Blinky_esp32 directory in vscode (with PlatformIO loaded)
6. Build and deploy the code to your ESP32 (via USB cable)

The code in this application is drawn from the examples provided by the [QP/C++ port for ESP32 using Arduino Plaform SDK](https://github.com/vChavezB/qpcpp_esp32) with some minor adaptation and a bug fix.
