# ASCEND – Quadcopter Drone (Hardware Architecture)

## 📌 Overview
ASCEND (Autonomous System for Cooperative Exploration, Navigation, and Detection) is a quadcopter-based UAV designed for stable flight, hardware reliability, and autonomous mission support in GNSS-denied environments.

This repository focuses ONLY on the **hardware design, integration, and system architecture** of the drone.

---

## ⚙️ Hardware Architecture

The drone is built using a modular architecture consisting of:

- Mechanical Frame
- Propulsion System
- Flight Controller
- Power System
- Sensors
- Communication System

---

## 🧩 Components Used

### 🔹 Frame & Structure
- S450 Quadcopter Frame (X-configuration)
- 500 mm wheelbase
- Carbon fiber / reinforced composite structure

### 🔹 Propulsion System
- 4 × BLDC Motors (1000KV)
- 4 × 40A ESCs (Readytosky)
- 10×4.5 inch propellers (2 pairs)

👉 Function:
- Generates thrust for lift, roll, pitch, and yaw control

---

### 🔹 Flight Controller
- Radiolink Pixhawk 2.4.8
- Integrated IMU + Barometer

👉 Function:
- Stabilization
- Motor control
- Flight balancing

---

### 🔹 Power System
- 3S LiPo Battery (11.1V, 5200mAh)
- Power Distribution Board (PDB)
- Power Module (voltage/current sensing)
- 5V/7A UBEC (for electronics)

👉 Function:
- Supplies stable power to motors and electronics
- Separates high-current and sensitive circuits

---

### 🔹 Sensors (Hardware Only)
- PX4Flow Optical Flow Sensor
- TF Mini Plus LiDAR
- IMX219 Camera (mounted)

👉 Function:
- Motion detection
- Distance measurement
- Environmental sensing

---

### 🔹 Communication System
- Holybro SiK Telemetry Radio (433 MHz)
- FS-iA10B Receiver + FS-i6X Transmitter
- TP-Link AC600 WiFi Adapter

---

## 🔋 Power Distribution Design

The system uses **dual power architecture**:

- High-power circuit → Motors (5200mAh battery)
- Regulated circuit → Electronics via UBEC

👉 Benefit:
- Prevents voltage drops affecting sensitive components
- Improves flight stability

---

## 🛠️ Hardware Integration

The system integrates:

- Motors → ESC → PDB → Battery
- Sensors mounted for downward and forward detection
- Flight controller centrally placed for balance
- Companion electronics powered via UBEC

According to the system design (Page 8 of report), the architecture separates:
- High-level processing
- Low-level flight control
- Power systems

---

## 📊 Specifications

- Total Weight: ~1.85 kg
- Wheelbase: 450–500 mm
- Battery: 3S LiPo 5200mAh
- Flight Time: ~15–18 minutes
- Configuration: Quadcopter (X-type)

---

## 🔧 Hardware Challenges Faced

- Electromagnetic interference (EMI) from ESCs affecting sensors
- Power module voltage inconsistencies
- Sensor mounting affecting stability
- Propulsion imbalance causing drift

👉 Solutions:
- Improved wiring layout
- Isolated sensor mounting
- Balanced frame and propulsion calibration

---

## 📸 Build Images
(Add your images here)
- Frame assembly
- Wiring setup
- Sensor mounting
- Final drone

---

## 🎥 Demo
(Add YouTube link)

---

## 👨‍🔧 Contribution

**Sujal Chavan**
- Hardware assembly
- Component integration
- Flight testing support
- System reliability improvements

---

## 📎 Reference
Full project report:
