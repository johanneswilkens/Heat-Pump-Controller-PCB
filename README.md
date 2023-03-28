# Heat Pump Controller PCB

This project is a versatile controller board designed primarily for LG Therma V heat pumps, but it may work with other systems as well. With Modbus and OpenTherm slave support, PWM input and output for a waterpump, multiple relays, and several input/output options, this board can help make the heat pump more efficient and make it easy to adjust heating curves and other settings.

This board can be programmed using the Arduino IDE or EspHome, which makes it easy to integrate with home automation systems like Home Assistant. With some modifications, the following code can run on it: https://github.com/altrnate32/esp-lg-control

In addition to the base features, this board includes several optional features, such as an isolated I2C interface, isolated UART, 5V UART, onboard temperature and humidity sensors, and a status LED. With these optional features, this board can be customized to suit a wide range of applications.

## Features

The following features are included in this controller board:

- Modbus and OpenTherm slave support
- PWM input and output for a waterpump
- 4 relays (can operate 230V AC 3A. For higher current, up to 10A PCB tracks must be reinforced with soldered on wire of sufficient cross section)
- 2 outputs that can work as high-side or low-side switches at 5V or 12V (via on board voltage converters)
- 2 inputs supporting 5V or 12V
- 4 connectors for DS18B20 sensors (several sensors can be connected to one connector)
- Optional isolated I2C interface
- Optional isolated UART
- Optional 5V UART
- Optional onboard DS18B20 and SHT40 sensor
- WS2812 LED for showing status (or regular LED if you dont need RGB)
- Powered via USB-C

## Project Status
- [x] Tested stable operation. 
- [x] Tested with LG Therma V HM143MR.U34 (14 kW three phase monoblock)
- [ ] Test on other devices
- [ ] Modify PCB for release
- [ ] Create Wiki Page

## Getting Started

To get started with this controller board, follow these steps:

1. Obtain the PCB files from the GitHub repository.
2. Use a PCB manufacturing service to manufacture the board or assemble the board yourself by soldering the components onto the board.
3. Program the ESP32 microcontroller using the Arduino IDE or other compatible software, such as Esphome. If you want to control your heat pump with Home Assistant, you can use Esphome to easily integrate the controller with Home Assistant.
4. Connect the heat pump components and other pheripherals to the appropriate connectors on the board. Make sure you use the correct connectors.
5. Power on the board using a USB-C cable.

## IO reference

| Function            | ESP32 GPIO Pin |
|---------------------|----------|
| Input1              | GPIO36   |
| Input2              | GPIO39   |
| Output1             | GPIO25   |
| Output2             | GPIO26   |
| Relay1              | GPIO27   |
| Relay2              | GPIO14   |
| Relay3              | GPIO12   |
| Relay4              | GPIO13   |
| Pump PWM In         | GPIO35   |
| Pump PWM Out        | GPIO32   |
| Open Therm In       | GPIO34   |
| Open Therm Out      | GPIO33   |
| Modbus RX           | GPIO16   |
| Modbus TX           | GPIO17   |
| Modbus Flow Control | GPIO5    |
| LED                 | GPIO23   |
| DS18B20             | GPIO15   |
| UART_ISO RX         | GPIO19   |
| UART_ISO TX         | GPIO18   |
| UART_5V RX          | GPIO2    |
| UART_5V TX          | GPIO4    |
| I2C SDA             | GPIO21   |
| I2C SCL             | GPIO22   | 


## Donating

If you find this project useful and would like to support its development, you can donate to the project using [the Ko-fi donating platform](https://ko-fi.com/johanneswilkens). Your donation will help cover the costs of developing and testing the board, as well as maintaining the project repository and providing support to users.

<a href='https://ko-fi.com/R6R7I6JZ' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>


## Support and feedback

If you need help with this project, or have any suggestions, please open an issue on the GitHub repository.


## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

