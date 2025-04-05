
# OpenBook – E-Reader Hardware Project

OpenBook is an open-source e-reader built around the ESP32-C6, featuring a 7.5" e-Paper display, rechargeable battery, and Wi-Fi support. Designed for low-power embedded use and comfortable digital reading.

---

##  Block Diagram

`Images/block_diagram.png`

> Diagram shows how ESP32-C6 is connected to display, battery, charging module, and buttons.

---

## 📋 Bill of Materials (BOM)


| Reference    | Value            | Device                            | Footprint      | Description                      | Link                                                                                             |
|:-------------|:-----------------|:----------------------------------|:---------------|:---------------------------------|:-------------------------------------------------------------------------------------------------|
| BOOT_BUTTON  | BUTTON_CUSYOMV1  | BUTTON_CUSYOMV1                   | MYBUTTON       | -                                | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k    |
| C1           | 100nF            | ESP32_WROVER_EAGLE-LTSPICE_CC0402 | C0402          | CAPACITOR, European symbol       | https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO                              |
| C2           | 100nF            | ESP32_WROVER_EAGLE-LTSPICE_CC0402 | C0402          | CAPACITOR, European symbol       |                                                                                                  |
| C3           | 100uF TANT       | RCL_CPOL-EUCT3528                 | CT3528         | POLARIZED CAPACITOR              |                                                                                                  |
| C10_SUPERCAP | CPH3225A         | CPH3225A                          | CAPCP3225X100N | 11 mF (EDLC) Supercapacitor 3.3V | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda                      |
| CHG_LED      | -                | ADAFRUIT_LEDCHIP-LED0603          | LED0603        | LED                              | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED                |
| D1           | USBLC6-2SC6Y     | USBLC6-2SC6Y                      | SOT23-6        | TVS Diode Array                  | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda                 |
| D2           | -                | AVX_SD0805S020S1R0                | 0805           | Schottky Diode                   | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0                                   |
| D3           | MBR0530          | MBR0530                           | SOD123         | Schottky Diode                   | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                  |
| D4           | MBR0530          | MBR0530                           | SOD123         | Schottky Diode                   | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                  |
| D5           | MBR0530          | MBR0530                           | SOD123         | Schottky Diode                   | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                  |
| D6           | PGB1010603MR     | PGB1010603MR                      | 0603           | TVS Diode Clamp                  | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                         |
| D7           | -                | AVX_SD0805S020S1R0                | 0805           | Schottky Diode                   | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0                                   |
| D8           | PGB1010603MR     | PGB1010603MR                      | 0603           | TVS Diode Clamp                  | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                         |
| D9           | PGB1010603MR     | PGB1010603MR                      | 0603           | TVS Diode Clamp                  | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                         |
| D10          | PGB1010603MR     | PGB1010603MR                      | 0603           | TVS Diode Clamp                  | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                         |
| D11          | PGB1010603MR     | PGB1010603MR                      | 0603           | TVS Diode Clamp                  | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                         |
| IC1          | BD5229G-TR       | BD5229G-TR                        | SOT23-5        | Voltage Detector                 | https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor                      |
| IC4          | XC6220A331MR-G   | XC6220A331MR-G                    | SOT23-5        | LDO Regulator                    | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                 |
| J1           | FFC 24P          | FH34SRJ-24S-0.5SH                 | 0.5mm Pitch    | FFC/FPC Connector                | https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose                         |
| J2           | USB-C            | USB4110-GF-A                      | USB4110        | USB Type-C Connector             | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY) |
| J3           | QWIIC            | QWIIC_CONNECTORJS-1MM             | JST04          | QWIIC I2C Connector              |                                                                                                  |
| J4           | SD Card          | 112A-TAAR-R03_ATTEND              | MicroSD        | MicroSD Socket                   | https://store.comet.srl.ro/Catalogue/Product/43497/                                              |
| L1           | 68uH             | 744043680                         | IND_4828       | Power Inductor                   | https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680                                   |
| PFMF.050.1   | -                | ESP32C6_VARISTOR                  | 1812           | Varistor                         | https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062                                 |
| Q1           | -                | DMG2305UX-7                       | SOT23          | P-channel MOSFET                 | https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                    |
| Q2           | -                | DMG2305UX-7                       | SOT23          | P-channel MOSFET                 |                                                                                                  |
| Q3           | SI1308EDL-T1-GE3 | SI1308EDL                         | SC70           | N-channel MOSFET                 | https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay                              |
| R1           | 10K              | ESP32_WROVER_EAGLE-LTSPICE_RR0402 | R0402          | RESISTOR                         |                                                                                                  |
| R2           | 2.2              | ESP32_WROVER_EAGLE-LTSPICE_RR0402 | R0402          | RESISTOR                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO    |

---

##  Detailed Hardware Functionality

###  Power System
- 3.7V 1800mAh Li-Po Battery (Cellevia LP584174)
- Charged via TP4056 USB module
- 3.3V provided via AMS1117 LDO regulator

###  Display
- Waveshare 7.5" e-Paper V2, SPI interface
- 800x480 resolution, ultra-low power
- Controlled by ESP32-C6 using GPIOs

###  Microcontroller – ESP32-C6
- BLE 5 + Wi-Fi 6
- Handles display updates and user input
- SPI + UART + GPIO used

###  Estimated Power Budget
| State           | Current | Est. Battery Life (1800mAh) |
|-----------------|---------|------------------------------|
| Idle            | ~20mA   | ~90 hours                    |
| Display Update  | ~120mA  | ~12–15 hours                 |

##  ESP32-C6 Pin Mapping

| Feature          | ESP32-C6 Pin | Description                |
|------------------|--------------|----------------------------|
| SPI CLK          | GPIO6        | Display SCK                |
| SPI MOSI         | GPIO7        | Display data               |
| Display CS       | GPIO10       | Chip select                |
| Display DC       | GPIO5        | Command/data               |
| Display RST      | GPIO4        | Reset                      |
| Display BUSY     | GPIO3        | Ready state                |
| Button A         | GPIO0        | Pull-down                  |
| Button B         | GPIO1        | Pull-down                  |
| UART TX          | GPIO21       | Debug                      |
| UART RX          | GPIO20       | Debug                      |


---

##  Renders & Images

 See `Images/` folder:
- `render_device.png` – Full device
- `render_pcb.png` – PCB only
- `block_diagram.png` – System layout

---

##  Design Notes
- All components were placed in Fusion 360 with correct dimensions
- PCB designed in Eagle + validated via 3D overlay
- Gerbers, BOM, and Pick & Place ready for fab
- Fusion file exported as both `.step` and `.f3d`

---

## Credits

Made with CAD, curse words, and caffeine.  