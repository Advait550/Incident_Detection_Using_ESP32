🚨 IoT Based Incident Detection & Path Tracking System
<p align="center"> <img src="images/incident-detection-banner.jpeg" width="850"/> </p>
📌 Overview

The IoT-Based Incident Detection & Path Tracking System is a real-time embedded solution designed to detect accidents or abnormal motion events and immediately notify emergency contacts with GPS location details.

The system processes motion data locally using an ESP32 and triggers GSM-based alerts when threshold conditions are met.

This architecture ensures fast response, low latency, and reliable emergency communication.

🎯 Problem Statement

In road accidents or fall incidents:

Immediate medical response is critical

Victims may be unconscious or unable to call for help

Delay in location sharing can be fatal

This system automates incident detection and location transmission without requiring user intervention.

🏗️ System Architecture
🔹 Core Components

ESP32 (Main Controller)

MPU6050 (Accelerometer + Gyroscope)

NEO-6M GPS Module

SIM800L GSM Module

Power Supply System

⚙️ Working Principle
🔹 Incident Detection Logic

MPU6050 continuously reads:

Acceleration (X, Y, Z)

Angular velocity

Threshold-based algorithm monitors:

Sudden high acceleration spikes

Abnormal tilt angles

Rapid motion changes

If threshold exceeds predefined limits:

Incident flag is triggered

System enters alert mode

All processing is performed locally on the ESP32 (Edge Computing).

🔹 Alert Mechanism

Once an incident is detected:

GPS module fetches real-time coordinates.

ESP32 formats location data.

SIM800L sends SMS containing:

Emergency message

Google Maps link with coordinates

Example format:

Emergency Alert!
Possible accident detected.
Location: https://maps.google.com/?q=LATITUDE,LONGITUDE
🔧 Hardware Implementation
<p align="center"> <img src="images/hardware-setup.jpeg" width="650"/> </p>

Implementation Highlights:

I2C communication with MPU6050

UART communication with GPS module

AT-command based GSM communication

Interrupt-safe detection logic

Modular wiring for maintainability

🧠 Technical Highlights

Real-time sensor data acquisition

Threshold-based motion classification

Edge-based decision making

GPS parsing and coordinate extraction

GSM AT command handling

Low-latency emergency response system

📊 Applications

Vehicle accident detection

Elderly fall detection

Worker safety monitoring

Remote area emergency response

Personal security devices

🔬 Future Enhancements

Machine learning-based incident classification

Cloud logging of movement data

Mobile app integration

Battery optimization and sleep modes

SOS manual trigger button

🛠️ Installation & Setup
🔹 Prerequisites

Arduino IDE / ESP-IDF

ESP32 Board Support Package

Required libraries:

Wire.h

MPU6050 library

TinyGPS++ (optional)

SoftwareSerial (if applicable)

🔹 Flashing the Code

Connect ESP32 via USB.

Select correct board and COM port.

Upload firmware.

Monitor serial output for:

Sensor readings

GPS lock status

GSM module response

🏗️ Project Type

Embedded + IoT Real-Time Safety System
