# PSoC 6 MCU: WLAN Manufacturing Test Middleware

The WLAN Manufacturing Test Middleware application is used to validate the WLAN firmware and radio performance of the Wi-Fi device. The mfg-test middleware repo can accept the serial input byte stream from the Mfg Test application and transform the contained commands into IOVAR/IOCTL messages to the wlan firmware. It can get the response from the wlan firmware (if expected), and transport them back to the 'wl tool' running on the host.

This repo should be used with FreeRTOS and Mbed OS applications to test the wlan firmware.

The Mfg Test middleware library consists of the Mfg Test Middleware Porting layer to interface with the wlan firmware and Wi-Fi functionality across SDKs such as FreeRTOS and Mbed OS.


## Requirements

- [ModusToolbox® software](https://www.cypress.com/products/modustoolbox-software-environment) v2.2
- Programming Language: C
- Supported Toolchains: Arm® GCC, IAR
- Associated Parts: All [PSoC® 6 MCU](http://www.cypress.com/PSoC6) parts


## Validated Kits

- [PSoC 6 Wi-Fi BT Prototyping Kit](https://www.cypress.com/CY8CPROTO-062-4343W) (CY8CPROTO-062-4343W) - Default target

- [PSoC 62S2 Wi-Fi BT Pioneer Kit](https://www.cypress.com/CY8CKIT-062S2-43012) (CY8CKIT-062S2-43012)

- [PSoC 6 WiFi-BT Pioneer Kit](https://www.cypress.com/CY8CKIT-062-WIFI-BT) (CY8CKIT-062-WIFI-BT)

- [PSoC 62S1 WiFi-BT Pioneer Kit](https://www.cypress.com/CYW9P62S1-43438EVB-01) (CYW9P62S1-43438EVB-01)


## Supported Software and Tools

ToolChain     | OS
--------------|----
GCC_ARM and IAR | FreeRTOS
GCC_ARM and ARMC6 | Mbed OS|


## Integration Notes

- The Wi-Fi Manufacturing Test Middleware library works with both the Arm Mbed ecosystems and AnyCloud.

- The library is integrated into Wi-Fi manufacturing applications for both AnyCloud and Mbed OS.

- You only need to include this library in the intended ecosystem to use these utilities. Depending on the ecosystem, the relevant source files will be picked up and linked, using `COMPONENT_ model_`.


## Additional Information

- [Wi-Fi Mfg Test Utilities API reference guide](https://cypresssemiconductorco.github.io/wifi-mfg-test/api_reference_manual/html/index.html)

- [Wi-Fi Mfg Test Utilities version](./version.txt)
