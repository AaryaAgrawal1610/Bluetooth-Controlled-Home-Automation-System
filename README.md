# Bluetooth Controlled Home Automation System

Control home appliances wirelessly using an **Arduino Uno** and an **HC-05 Bluetooth module**. This project enables users to switch electrical devices ON and OFF from a smartphone via Bluetooth, providing a simple and cost-effective home automation solution.

##  Features

*  Bluetooth-based appliance control
*  Real-time ON/OFF switching
*  Supports LEDs, relay modules, and household appliances
*  Simple Arduino implementation
*  Wireless communication using HC-05
  

##  Hardware Requirements

* Arduino Uno/Nano
* HC-05 Bluetooth Module
* Relay Module 
* LED (for testing)
* Jumper Wires
* Breadboard (optional)
* Android smartphone with a Bluetooth terminal app


##  Circuit Connections

### HC-05 → Arduino

| HC-05 Pin | Arduino Pin             |
| --------- | ----------------------- |
| VCC       | 5V                      |
| GND       | GND                     |
| TXD       | D10 (SoftwareSerial RX) |
| RXD       | D11 (SoftwareSerial TX) |

### Relay/LED → Arduino

| Device Pin | Arduino Pin |
| ---------- | ----------- |
| Signal     | D8          |
| VCC        | 5V          |
| GND        | GND         |


##  How It Works

1. Upload the Arduino sketch.
2. Pair your smartphone with the HC-05 module (default PIN is usually **1234** or **0000**).
3. Open a Bluetooth terminal application.
4. Connect to the HC-05 module.
5. Send the following commands:

| Command | Action             |
| ------- | ------------------ |
| `1`     | Turn appliance ON  |
| `0`     | Turn appliance OFF |

The Arduino receives the Bluetooth command and changes the state of the output pin accordingly.

## Compatible Applications

* Serial Bluetooth Terminal
* Bluetooth Terminal HC-05
* Arduino Bluetooth Controller

## Future Enhancements

* Control multiple appliances
* Voice-controlled operation
* Custom Android application
* Password-protected Bluetooth access
* Timer and scheduling features
* IoT integration using ESP32 or Wi-Fi
* Appliance status feedback

## Safety Notice

* Never connect high-voltage AC appliances directly to the Arduino.
* Always use an opto-isolated relay module for electrical safety.
* Ensure proper insulation while working with mains electricity.
