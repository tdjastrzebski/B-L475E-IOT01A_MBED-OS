> git clone --recurse-submodules https://github.com/tdjastrzebski/B-L475E-IOT01A_MBED-OS

# References

* [STM32L475VG](https://www.st.com/en/microcontrollers-microprocessors/stm32l475vg.html) Ultra-low-power with FPU Arm Cortex-M4 MCU 80 MHz with 1 Mbyte of Flash memory, USB OTG, DFSDM  
* [DS10969](https://www.st.com/resource/en/datasheet/stm32l475vg.pdf) STM32L475xx Datasheet
* [RM3051](https://www.st.com/resource/en/reference_manual/rm0351-stm32l47xxx-stm32l48xxx-stm32l49xxx-and-stm32l4axxx-advanced-armbased-32bit-mcus-stmicroelectronics.pdf) STM32L47xxx, STM32L48xxx, STM32L49xxx and STM32L4Axxx advanced Arm®-based 32-bit MCUs
* [B-L475E-IOT01A](https://www.st.com/en/evaluation-tools/b-l475e-iot01a.html) STM32L4 Discovery kit IoT node, low-power wireless, BLE, NFC, SubGHz, Wi-Fi
* [UM2153](https://www.st.com/resource/en/user_manual/um2153-discovery-kit-for-iot-node-multichannel-communication-with-stm32l4-stmicroelectronics.pdf) Discovery kit for IoT node, multi-channel communication with STM32L4

# Prerequisites
* [Ninja](https://github.com/ninja-build/ninja/releases)
* [CMake](https://cmake.org/download)
* [mbed-tools](https://os.mbed.com/docs/mbed-os/v6.15/build-tools/use.html)

```
mbed-tools new .
mbed-tools import <example> <PATH>
mbed-tools configure -m DISCO_L475VG_IOT01A -t GCC_ARM
mbed-tools compile -m DISCO_L475VG_IOT01A -t GCC_ARM
```

git submodule add --depth 1 https://github.com/ARMmbed/mbed-os mbed-os
git config -f .gitmodules submodule.mbed-os.shallow true

`pyocd pack install STM32L475VGTx`

[Updating ISM 43362 WiFi module firmware on B-L475E-IOT01A board - please rescue!](https://community.st.com/s/question/0D53W00001nnSaxSAE/updating-ism-43362-wifi-module-firmware-on-bl475eiot01a-board-sos)