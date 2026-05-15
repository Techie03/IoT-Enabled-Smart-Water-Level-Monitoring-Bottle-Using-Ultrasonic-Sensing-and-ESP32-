# IoT-Based Automatic Smart Water Level Management Bottle

## Overview

The **IoT-Based Automatic Smart Water Level Management Bottle** is an embedded systems project designed to monitor and manage water levels in a bottle or container using an ultrasonic sensor and microcontroller-based alert mechanism. The system identifies minimum, normal, and maximum water-level conditions and provides real-time feedback through buzzer and LED indicators.

This project demonstrates practical experience in **embedded systems, sensor interfacing, Arduino programming, hardware prototyping, water-level automation, and IoT-oriented system design**. The prototype provides a strong foundation for future expansion into cloud-based monitoring, automatic refill alerts, dashboard visualization, and smart water management applications.

---

## Key Highlights

- Designed and implemented a real-time automatic water-level monitoring prototype using Arduino and an ultrasonic sensor.
- Integrated buzzer and LED indicators to alert users when the water level reaches minimum or maximum thresholds.
- Developed threshold-based control logic to classify water levels into minimum, normal, and maximum states.
- Built and tested a working hardware prototype using Arduino, ultrasonic sensor, buzzer, LED, breadboard, battery pack, and connecting wires.
- Implemented a simple alert-based management mechanism to support water-level awareness and prevent underfill or overfill conditions.
- Documented system architecture, experimental setup, water-level indication logic, and buzzer/LED response behavior.
- Proposed scalable IoT enhancements including ESP8266/ESP32 connectivity, Firebase integration, cloud storage, dashboards, and automatic water-level analytics.

---

## Problem Statement

Manual water-level monitoring in bottles or containers can be inconsistent, especially when users need to maintain a specific water range. Overfilling may cause spillage, while low water levels may require timely refilling. This project addresses the need for a simple, low-cost automatic water-level management system that detects water-level conditions and provides immediate alerts.

The prototype focuses on building the core sensing and alert mechanism required for a smart bottle or container-based water-level management solution.

---

## Hardware and Software Components

![Hardware and Software Components](assets/Hardware%20and%20Software%20Components.png)

### Hardware Requirements

| Component | Purpose |
|---|---|
| Arduino Board | Main microcontroller used to process ultrasonic sensor readings and control output devices |
| Ultrasonic Sensor | Measures the distance between the sensor and water surface to estimate water level |
| Buzzer | Provides audio alerts when water reaches minimum or maximum threshold levels |
| LED | Provides visual indication for alert conditions |
| Breadboard | Used for circuit prototyping and component connections |
| Connecting Wires | Used to connect the sensor, buzzer, LED, and Arduino board |
| Battery Pack / USB Power | Supplies power to the prototype circuit |

### Software Requirements

| Software | Purpose |
|---|---|
| Arduino IDE | Used to write, compile, and upload code to the Arduino board |
| Arduino C/C++ | Programming language used for sensor reading and alert-control logic |

---

## Experimental Setup

The prototype was assembled using an Arduino board, ultrasonic sensor, buzzer, LED, breadboard, and connecting wires. The ultrasonic sensor was positioned near the bottle/container opening to measure the distance between the sensor and the water surface.

![Experimental Setup](assets/Experimental%20Support.png)

---

## System Architecture

The system follows a sensor-to-actuator workflow where the ultrasonic sensor captures distance data, the Arduino processes the reading, and the buzzer/LED indicators respond based on predefined water-level thresholds.

![System Flow](assets/System%20Flow.png)

### Architecture Flow

    Power Source
        ↓
    Arduino Board
        ↓
    Ultrasonic Sensor
        ↓
    Water Level Detection
        ↓
    Threshold-Based Classification
        ↓
    Buzzer and LED Alert System

---

## Water Level Classification Logic

The system classifies the detected water level into three categories: minimum, normal, and maximum. Each condition triggers a specific buzzer and LED response.

![Water Level Indication Table](assets/Water%20Level%20Indication%20Table.png)

| Water Level Condition | Description | Buzzer Status | LED Status |
|---|---|---|---|
| Minimum Level | Water level is below the required threshold | ON - High Frequency | ON |
| Normal Level | Water level is within the acceptable range | OFF | OFF |
| Maximum Level | Water level reaches the upper threshold | ON - Low Frequency | ON |

---

## Buzzer and LED Response Analysis

The buzzer and LED provide real-time feedback based on the detected water-level condition. This alert mechanism helps users identify whether the bottle/container requires refilling, is within the normal range, or has reached the maximum level.

![Buzzer and LED Graph](assets/Buzzer%20and%20LED%20Graph.png)

---

## Working Principle

The ultrasonic sensor emits sound waves toward the water surface and receives the reflected signal. The Arduino calculates the distance based on the time taken by the signal to return.

The measured distance is compared with predefined threshold values:

- If the water level is below the minimum threshold, the buzzer turns ON at high frequency and the LED turns ON.
- If the water level is within the normal range, both buzzer and LED remain OFF.
- If the water level reaches the maximum threshold, the buzzer turns ON at low frequency and the LED turns ON.

This enables automatic water-level monitoring and real-time alert generation.

---

## Technical Implementation

### Sensor Integration

- Interfaced the ultrasonic sensor with Arduino digital pins.
- Captured distance readings using trigger and echo signals.
- Converted distance readings into water-level conditions.

### Water-Level Management Logic

- Defined minimum and maximum threshold values.
- Classified sensor readings into minimum, normal, and maximum states.
- Triggered output devices based on the detected water-level condition.

### Alert Mechanism

- Configured buzzer output for different alert states.
- Used LED indication for visual feedback.
- Implemented condition-based control logic for minimum and maximum water levels.

### Hardware Prototyping

- Built the circuit using breadboard and jumper wires.
- Tested sensor placement and response behavior.
- Verified buzzer and LED output for different water-level scenarios.

---

## Technologies Used

### Embedded Hardware

- Arduino
- Ultrasonic Sensor
- Buzzer
- LED
- Breadboard
- Connecting Wires
- Battery Pack / USB Power

### Programming and Tools

- Arduino IDE
- Arduino C/C++
- Serial Monitor for testing and debugging

---

## Key Features

- Real-time water-level monitoring
- Ultrasonic sensor-based distance measurement
- Threshold-based water-level classification
- Automatic alert generation for minimum and maximum levels
- Buzzer indication with different frequency behavior
- LED indication for visual alert feedback
- Low-cost and easy-to-build hardware prototype
- Modular design for future IoT expansion
- Suitable for smart bottle and water-level management applications

---

## Skills Demonstrated

- Embedded systems development
- Arduino programming
- Ultrasonic sensor interfacing
- Circuit design and prototyping
- Real-time sensor data processing
- Threshold-based water-level classification
- Buzzer and LED control logic
- Hardware-software integration
- Automatic alert-system design
- IoT system design fundamentals
- Technical documentation

---

## Possible IoT Extension

This prototype can be extended into a complete IoT-based automatic water-level management system by adding wireless communication and cloud-based data storage.

Potential enhancements include:

- ESP8266 or ESP32 Wi-Fi module integration
- Firebase Realtime Database for cloud storage
- Web dashboard for live water-level monitoring
- User-wise water-level history tracking
- Daily water usage tracking
- Automatic refill notification system
- Time-series analysis of water-level patterns
- Mobile notification support

---

## Future Enhancements

- Integrate ESP8266/ESP32 for wireless data transmission.
- Store real-time water-level readings in Firebase or another cloud database.
- Build a web dashboard for visualization and monitoring.
- Add user authentication for multi-user tracking.
- Implement automatic refill reminders.
- Add water consumption trend analysis.
- Improve sensor enclosure and bottle mounting design.
- Add battery optimization for portable usage.
- Include calibration support for different bottle sizes.
- Add mobile notifications for refill and overflow alerts.

---

## Project Structure

    IoT-Based-Automatic-Smart-Water-Level-Management-Bottle/
    │
    ├── README.md
    ├── code/
    │   └── water_level_management.ino
    │
    ├── assets/
    │   ├── Buzzer and LED Graph.png
    │   ├── Experimental Support.png
    │   ├── Hardware and Software Components.png
    │   ├── System Flow.png
    │   └── Water Level Indication Table.png
    │
    └── docs/
        └── project-report.pdf

---

## How to Run

### 1. Hardware Setup

Connect the ultrasonic sensor, buzzer, and LED to the Arduino board using a breadboard and jumper wires.

Example connection:

    Ultrasonic Sensor VCC  → Arduino 5V
    Ultrasonic Sensor GND  → Arduino GND
    Ultrasonic Sensor TRIG → Arduino Digital Pin
    Ultrasonic Sensor ECHO → Arduino Digital Pin

    Buzzer Positive → Arduino Digital Pin
    Buzzer Negative → GND

    LED Positive → Arduino Digital Pin through resistor
    LED Negative → GND

### 2. Software Setup

1. Open Arduino IDE.
2. Connect the Arduino board to the system.
3. Select the correct board and COM port.
4. Upload the Arduino code.
5. Open Serial Monitor to observe sensor readings.
6. Test different water levels and verify buzzer/LED responses.

---

## Applications

- Smart water bottle monitoring
- Automatic water-level management
- Refill and overflow alert systems
- Basic IoT-based monitoring projects
- Embedded systems learning projects
- Sensor-based automation prototypes
- Low-cost liquid level monitoring systems

---

## Summary

This project demonstrates the ability to design, build, test, and document a working embedded systems prototype for automatic water-level monitoring. It highlights hands-on experience with Arduino programming, ultrasonic sensor integration, real-time condition monitoring, threshold-based control logic, and hardware-based alert mechanisms. The project also shows the ability to extend a hardware prototype into a scalable IoT solution using cloud storage, dashboards, and smart notification features.

---

## Conclusion

The **IoT-Based Automatic Smart Water Level Management Bottle** demonstrates how ultrasonic sensing and microcontroller-based control can be used to monitor water levels and generate real-time alerts. The project provides a strong foundation for developing advanced IoT-enabled water-level management systems with cloud storage, dashboard visualization, and automatic refill/overflow notifications.
