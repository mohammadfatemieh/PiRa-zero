![irnas_logo](https://github.com/IRNAS/PiRa-zero/blob/master/Pics/irnas_logo.png)
# PiRA zero 
## Power in Responsive Applications HAT for Raspberry Pi with RTC for power saving mode

PiRa zero is a compact shield for power scheduling on Rasppbery Pi and similar devices in solar and wirelessly powered applications. It implements the following key features:

![pira_image](https://github.com/IRNAS/PiRA-RTC-HAT/blob/master/pira-zero-pitstop.jpg)

## Features

* single cell LiPo cell charging of up to 3A (multiple 18650 cells supported) + LifePo4 support
* solar panel charging (Voltaic systems 6W panels in parallel recommended)
* USB charging, compatible with QI wireless chargers
* advanced current limiting, to support wide array of chargers
* precise charging control via i2c (BQ24296)
* battery temperature protection with thermistor
* battery reverse polarity protection and fuse (3A)
* high-current battery output mosfet (for 3G or satellite modems)
* LORA RMF95 communication module
* battery voltage precise measurement (MCP3021)
* advanced power scheduling for robust applications:
  * power timer TPL5110 for configurable scheduled boot 1s-7200s or one-time power up on charging
  * S3231 for configurable scheduled boot and timekeeping
  * nfigurable power-up sources
  * ower-up on charging
  * ower-up from power timer
  * ower-up from RTC
  * ower-up from self-enable (external CPU signal)
 
![pira_block_diagram](https://github.com/IRNAS/PiRa-zero/blob/master/Pics/pira_zero_block_diagram.jpg)

## Connector pinout

 * All ground pins connected, UART, SPI pins connected
 * Pin 1 - 3V3 - from Pi to board
 * Pin 2 - 5V - from board to Pi
 * Pin 3 - SDA
 * Pin 4 - 5V - from board to Pi
 * Pin 5 - SCL
 * Pin 7 - BCM 4 - RTC-Reset- output, reset RTC if needed
 * Pin 11 - BCM 17 - Timer-EN - input, detect wake-up from RTC
 * Pin 12 - BCM 18 - CPU self-enable - output, keep high until shutdown
 * Pin 13 - BCM 27 - Timer done - output, set high to signal timer to power off
 * Pin 15 - BCM 22 - RTC-EN - input, detect wake-up from RTC
 * Pin 16 - BCM 23 - GPO-FET - output, enable mosfet output
 * Pin 22 - BCM 25 - GPIO BCM25 - available at header
 * Pin 29 - BCM 5 - GPIO BCM 5 - available at header
 * Pin 31 - BCM 6 - GPIO BCM 6 - available at header
 * Pin 33 - BCM 13 - LORA reset

![pira_zero_con_diagram](https://github.com/IRNAS/PiRa-zero/blob/master/Pics/pira_zero_con_diagram.jpg)

## Power consumption
TODO

---

#### License

All our projects are as usefully open-source as possible.

Hardware including documentation is licensed under [CERN OHL v.1.2. license](http://www.ohwr.org/licenses/cern-ohl/v1.2)

Firmware and software originating from the project is licensed under [GNU GENERAL PUBLIC LICENSE v3](http://www.gnu.org/licenses/gpl-3.0.en.html).

Open data generated by our projects is licensed under [CC0](https://creativecommons.org/publicdomain/zero/1.0/legalcode).

All our websites and additional documentation are licensed under [Creative Commons Attribution-ShareAlike 4 .0 Unported License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

What this means is that you can use hardware, firmware, software and documentation without paying a royalty and knowing that you'll be able to use your version forever. You are also free to make changes but if you share these changes then you have to do so on the same conditions that you enjoy.

Koruza, GoodEnoughCNC and IRNAS are all names and marks of Institut IRNAS Rače. 
You may use these names and terms only to attribute the appropriate entity as required by the Open Licences referred to above. You may not use them in any other way and in particular you may not use them to imply endorsement or authorization of any hardware that you design, make or sell.
