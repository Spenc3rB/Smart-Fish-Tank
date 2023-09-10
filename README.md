# Aquatech Environmental Monitoring System

## Table of Contents
- [Introduction](#introduction)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

The Aquatech Environmental Monitoring System is an ESP32-based project designed to monitor water quality and environmental conditions. This system utilizes various sensors to measure parameters such as Total Dissolved Solids (TDS) in water, temperature, and allows you to customize alert thresholds and email notifications. Additionally, it features RGB LED control and a stepper motor for feeders.

This README provides an overview of the project, including hardware and software requirements, installation instructions, usage guidelines, and configuration options.

---

## Hardware Requirements

To build and run this project, you will need the following hardware components:

- ESP32 development board
- TDS (Total Dissolved Solids) sensor
- OneWire temperature sensor
- Stepper motor and driver module
- RGB LED (Red, Green, Blue) and appropriate resistors
- Power supply for the stepper motor
- Miscellaneous components (wires, breadboard, etc.)

---

## Software Requirements

The software requirements for this project are as follows:

- [Arduino IDE](https://www.arduino.cc/en/software) with the ESP32 board manager installed.
- Libraries:
  - ESPAsyncWebServer
  - SPIFFS
  - OneWire
  - DallasTemperature

---

## Installation

Follow these steps to set up the Aquatech Environmental Monitoring System:

1. Install the Arduino IDE if you haven't already.

2. Open the Arduino IDE, go to **File > Preferences**, and in the "Additional Boards Manager URLs" field, add the following URL: https://dl.espressif.com/dl/package_esp32_index.json

3. Go to **Tools > Board > Boards Manager**, search for "ESP32," and install the "esp32" platform.

4. Install the required libraries by going to **Sketch > Include Library > Manage Libraries** and searching for each library by name (e.g., "ESPAsyncWebServer," "SPIFFS," "OneWire," "DallasTemperature"). Click the "Install" button for each library.

5. Connect the hardware components as per your setup and wiring diagram.

6. Open the project's Arduino sketch file in the Arduino IDE.

7. Select the correct board and port under **Tools > Board** and **Tools > Port**.

8. Click the upload button (right arrow) to compile and upload the code to your ESP32 board.

9. Open the Serial Monitor (Tools > Serial Monitor) to view debug messages and monitor the system's operation.

---

## Usage

Once the code is uploaded and the hardware is correctly connected, follow these usage guidelines:

1. Power on the ESP32 board.

2. Connect to the ESP32's Wi-Fi network (SSID: "Yummy House" and Password: "kachow123"). You can change these values in the code if needed.

3. Access the web interface by navigating to the ESP32's IP address in a web browser. The default IP address is typically `http://192.168.4.1`.

4. Use the web interface to monitor TDS levels, temperature, and configure various settings such as temperature threshold, email recipient, LED color, PPM threshold, and measurement frequency.

5. The system will continuously monitor environmental conditions and send email alerts (if configured) when thresholds are exceeded.

6. The stepper motor will be actuated based on the configured conditions.

---

## Configuration

You can customize various aspects of the Aquatech Environmental Monitoring System by modifying the configuration in the Arduino sketch. Here are some of the key configuration options:

- Wi-Fi SSID and password: You can change the default Wi-Fi credentials by modifying the `ssid` and `password` variables.

- Sensor pins and parameters: Adjust pins and parameters for TDS, OneWire, and DallasTemperature sensors as needed.

- Alert thresholds: Set the temperature and PPM thresholds for email alerts.

- RGB LED control: Customize the LED color and behavior based on sensor readings.

- Stepper motor settings: Configure the number of steps per revolution and stepper motor control based on conditions.

- Email recipient: Set the email address to receive alerts (if desired).

---

## Contributing

Contributions to this project are welcome! If you find issues, have ideas for improvements, or would like to add new features, please submit a pull request on the project's GitHub repository.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to adapt and extend this README as needed to provide additional details about your project, instructions for specific use cases, or any other relevant information.

