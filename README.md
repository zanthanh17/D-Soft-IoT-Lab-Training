# D-Soft IoT Lab Intern Training

## Create Dashboard

This project involves creating a dashboard on **DBoard** to work with an **ESP32** device. The dashboard should include:

- **Push Button (Widget Power Button):** To control the LED on the device.
- **LED Indicator (Widget Led Indicator):** To synchronize and display the LED status on the device.
- **Line Chart (Widget Line Chart):** To display random **temperature** and **humidity** values from the device.

## Sync Device Status

To ensure proper synchronization of the LED status under different conditions:

### Case 1: Device Loses Network Connection
- If the network connection is lost, changes made to the LED status on the dashboard will not be received by the device.
- When the connection is restored, the device should retrieve the latest LED status from the server to synchronize correctly.

### Case 2: Device Loses Power and Network
- If the device loses power and network, it should be able to restore the previous LED status when power is back but the network is still unavailable.
- Implement a mechanism to **store the last known LED status in non-volatile memory (EEPROM or SPIFFS)** on the ESP32 so that it can retain the status after a reboot.

## Technology Stack
- **Hardware:** ESP32
- **Software:** Arduino IDE
- **IoT Platform:** ThingsBoard

## Installation and Setup
1. Install **Arduino IDE** and configure it for ESP32 development.
2. Install the required **ESP32 board libraries** via the **Board Manager** in Arduino IDE.
3. Install **ThingsBoard MQTT library** for communication.
4. Set up a **ThingsBoard dashboard** with the required widgets.
5. Upload the firmware to ESP32 and connect it to the ThingsBoard platform.

## Implementation Notes
- Use **MQTT protocol** for communication between ESP32 and ThingsBoard.
- Store **LED state** in **EEPROM or SPIFFS** to maintain status after a reboot.
- Implement **periodic status checks** to fetch updates from the server when the network is restored.

## Author
D-Soft IoT Lab Intern Training Team
