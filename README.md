Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

# WLED Mini Controller
This board is designed to connect addressable LEDs/Neopixel strips and handle them with the WLED firmware. Other firmware can be used as well.

<img src="./Images/IMG_8542.jpeg" width="50%" height="50%">

## Dontations / Spenden
If you like my projects and want to support me for upcoming projects :smiling_face_with_three_hearts:  
- PayPal: stefan.riese@me.com
- Amazon Giftcard: https://www.amazon.de/Amazon-Gutschein-per-E-Mail-Amazon/dp/B0054PDOV8 - stefan.riese@me.com

## Features
- ESP-WROOM-02 (ESP8266)
- 5,5mm / 2,1mm barrel jack connector for input voltage
- 2 output lines for LED data and LED clock or relais
- level shifter for all 2 outputs (3.3V -> 5V )
- resistor for data line
- support for LED strips with clock signal
- connector to flash firmware with CP2104 (3.3V, TX, RX, GND, IO0, GND)
- :heavy_exclamation_mark: Maximum 5A :heavy_exclamation_mark:

## BOM
- 1 x WLED Mini Controller presoldered from https://jlcpcb.com/

|Comment|Designator|Footprint|LCSC
|---|---|---|---
1000µF|C1|Capacitor_SMD:CP_Elec_10x10|C249474
10µF|C2,C4|Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder|C19702
47µF|C3|Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder|C16780
100nF|C5,C6,C7|Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder|C14663
10K|R1,R2,R3,R4|Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder|C25804
330|R5|Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder|C23138
AMS1117-3.3|U1|Package_TO_SOT_SMD:SOT-223-3_TabPin2|C347222
ESP-WROOM-02|U2|RF_Module:ESP-WROOM-02|C529584
TXS0102DCU|U3|Package_SO:VSSOP-8_2.3x2mm_P0.5mm|C53434

- 2 x 2-pin screw terminal (https://www.amazon.de/gp/product/B08JB6SSCJ)
- 1 x Barrel Jack Adapter DS-210 (5,5mm / 2,1mm) (https://www.ebay.de/itm/182379482999)

## Wiring diagram
- https://github.com/Hasenpups/WLED_Mini_Controller_Public/blob/main/WLED_Mini_Controller.pdf

## Software
- WLED: https://github.com/Aircoookie/WLED/releases

## How to flash software
- Connect IO0 to GND
- Connect USB-UART bridge to 3.3V, TX, RX and GND
    - https://de.aliexpress.com/item/1005002689033373.html
    - https://www.makershop.de/module/kommunikation-module/micro-usb-uart-ttl/
- Open https://install.wled.me/
- Click "Install"
- Select COM port of USB-UART bridge
- Wait until finished

## WLED configuration
- OUT1 - IO2
- OUT2 - IO14

## Case

<img src="./Images/IMG_8540.JPEG" width="50%" height="50%">
<img src="./Images/IMG_8541.JPEG" width="50%" height="50%">

https://www.prusaprinters.org/prints/124222-wled-all-in-one-controller-housing
