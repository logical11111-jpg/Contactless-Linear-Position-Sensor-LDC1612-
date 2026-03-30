<img width="1370" height="912" alt="image" src="https://github.com/user-attachments/assets/f5e8a32c-db7e-435d-81d6-77ed205dd0bb" />
# Contactless-Linear-Position-Sensor-LDC1612-
Documentation and schematic reference for the LDC1612 Dual-Coil Linear Position Sensor. A wear-free, contactless I2C digital encoder delivering 28-bit, sub-micron precision for sim-racing pedals, MIDI faders, and CNC limit switches.

# Dual-Coil Contactless Linear Position Sensor (TI LDC1612)

[![Get it on Tindie](https://img.shields.io/badge/Tindie-Buy_Evaluation_Board-blue)](https://www.tindie.com/products/led/contactless-linear-position-sensor-ldc1612/)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

Technical documentation, schematic reference, and application guide for the **Wear-Free Dual-Coil I2C Linear Position Sensor** breakout, engineered by LogicalEdges.

---

## 🚀 The Problem: Mechanical Wear and "Scratchy" Data
If you’ve ever had a sim-racing pedal flutter mid-corner, a MIDI audio fader get "scratchy," or a CNC limit switch fail due to shop dust, you know the fatal flaw of mechanical sensors: **physical contact is the enemy of precision.**
* **Potentiometers** wear out their carbon tracks and drift over time.
* **Optical Encoders** fail the moment they are exposed to oil, dust, or machining coolant.
* **Single-Coil / Hall Sensors** suffer from thermal drift and cannot differentiate between deliberate linear movement and accidental mechanical "slop" (Z-axis wobble).

## 💡 The Solution: Inductive Dual-Coil Differential Sensing
Powered by the **Texas Instruments LDC1612** Inductance-to-Digital Converter, this evaluation board replaces physical contacts with light-speed electromagnetic induction. 

By tracking the presence of a conductive target (like a piece of copper tape, aluminum, or steel) moving across the PCB, it delivers rock-solid, **28-bit digital position data** directly over I2C.

### Why Dual-Coil Geometry? (The Differential Advantage)
A standard single-coil inductive sensor is easily fooled. If your mechanical slider wiggles closer to the sensor, a single coil registers that as a change in position. **Our custom dual-coil architecture knows better.**

By measuring two adjacent coils simultaneously, we enable differential ratio metric calculations in your code:
1. **Common-Mode Noise Rejection:** A temperature spike or a mechanical Z-axis wobble affects both coils equally. By comparing the ratio between the two, this environmental noise is canceled out.
2. **Sub-Micron Precision:** You are left with a mathematically pure linear position vector, capable of sub-micron precision (depending on your target's air-gap and geometry).

---

## 🎯 Ideal Application Scenarios
This board brings industrial-grade linear encoding to the I2C bus, making it plug-and-play with Arduino, ESP32, RP2040, and Teensy microcontrollers.
* **Pro-Tier Sim-Racing Pedals:** Replace failing analog pots with high-resolution 28-bit depth for throttle, brake, and clutch telemetry.
* **Infinite-Life MIDI Audio Faders:** Build the world’s smoothest synthesizers and mixing consoles. No friction, no dust gathering—just pure I2C digital data.
* **Industrial Robotics & CNC:** A digital linear encoder that thrives in harsh environments. 100% immune to oil, dust, dirt, and machine vibration.

---

🛒 **Skip the complex coil layout and start coding today:** **[Get the Pre-Assembled Breakout Board on Tindie](https://www.tindie.com/products/led/contactless-linear-position-sensor-ldc1612/)**

---

## ⚠️ CRITICAL SAFETY & LIABILITY DISCLAIMER (READ BEFORE USE)
**Important: For R&D and Evaluation Use Only.**
This module is sold AS IS exclusively for Prototyping, Evaluation, and Research & Development purposes. It is NOT a finished product and is not intended for incorporation into final consumer, commercial, life-critical, or safety-critical systems.

* **Liability:** The user assumes full responsibility for integration, software implementation, and regulatory compliance. LogicalEdges' liability is strictly limited to manufacturing defects upon arrival, and shall not exceed the original purchase price.
* **Voiding of Warranty:** Warranty is immediately voided by user misuse, including but not limited to: over-voltage on the I2C/Power pins, physical damage to the sensing coils, or user-initiated modifications and soldering. No refunds will be issued for user-damaged components.
* **Product Revisions:** As we are constantly optimizing the differential coil geometry to maximize SNR (Signal-to-Noise Ratio), the physical board you receive may vary slightly in appearance from the product photos.

*By utilizing this documentation or purchasing the hardware, you agree to these terms.*
