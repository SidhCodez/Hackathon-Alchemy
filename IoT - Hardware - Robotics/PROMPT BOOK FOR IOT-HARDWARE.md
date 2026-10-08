# Category 07: IoT / Hardware / Robotics

This category focuses on building physical computing projects using tools like **Arduino**, **Raspberry Pi**, **ESP32**, **Raspberry Pi Pico**, **Jetson Nano**, and sensors/actuators. It strips away pure software complexities and focuses purely on **hardware, sensors, firmware, connectivity, and physical-world interaction** — the foundation of every IoT/Hardware/Robotics hackathon.

Here is the exact list of documents we will prepare for the **IoT / Hardware / Robotics** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing gaps (Physical-world focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a hardware/IoT project.
3. **`TRD.md`** (Technical Requirements Document) — Defines the hardware stack (Arduino, Raspberry Pi, ESP32), sensors, and connectivity protocols.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Device → Sensor → Gateway → Cloud → User (IoT architecture).
5. **`HARDWARE_SCHEMATIC.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines components, pin mappings, wiring diagram, and power requirements.
6. **`SENSOR_SPEC.md`** — (Replaces `API_SPECIFICATION.md`) Defines each sensor's purpose, data format, calibration, and sampling rate.
7. **`FIRMWARE_RULES.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines the firmware logic, loops, interrupts, and state machines.
8. **`CONNECTIVITY_PROTOCOL.md`** — Defines WiFi, Bluetooth, MQTT, LoRa, Zigbee, or HTTP communication.
9. **`POWER_MANAGEMENT.md`** — Defines power source, battery life, and energy optimization.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Dashboard or mobile app design, device status, and user flow.
11. **`ERROR_HANDLING.md`** — What happens when a sensor fails, connection drops, or power is lost.
12. **`SECURITY.md`** — Device authentication, data encryption, and firmware protection.
13. **`TESTING.md`** — QA plan, hardware testing, sensor calibration, and edge cases.
14. **`EVALUATION.md`** — How you measure device performance (Latency, Accuracy, Power consumption).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Flashing firmware, connecting to cloud, and setting up the live demo.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
17. **`GLOSSARY.md`** — Definitions of hardware terms (GPIO, MQTT, PWM, I2C, Sensor, Actuator).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem and identify what can be solved through hardware, sensors, or robotics.
```text
I am participating in an IoT/Hardware/Robotics hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed hardware/IoT/robotics solution ideas
7. Core hardware features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential hardware platforms and tools that could be used (Arduino, Raspberry Pi, ESP32, Jetson Nano, etc.)

Do not assume I am an experienced hardware engineer.
Explain hardware concepts (GPIO, sensors, actuators, microcontrollers) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear hardware product plan with features, sensors, and scope.
```text
You are a senior hardware product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed hardware solution
7. Product goals
8. User stories
9. Functional requirements (Include hardware-specific requirements: Sensors, Actuators, Connectivity, Power)
10. Non-functional requirements (Reliability, Latency, Power efficiency, Durability)
11. Core hardware features
12. Nice-to-have features
13. User journeys (How a user interacts with the device)
14. MVP scope (Which hardware feature must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include hardware metrics: Sensor accuracy, Response time, Battery life)
17. Risks and assumptions (Include hardware risks: Component failure, Power loss, Connectivity issues)

Keep the MVP realistic for a 24-48 hour hardware hackathon.
Do not add unnecessary sensors just to make the project sound impressive.
Prioritize features that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on hardware, sensors, and connectivity.
```text
You are a senior hardware engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Hardware platform choice (Arduino, Raspberry Pi, ESP32, Jetson Nano — justify the choice)
3. Microcontroller/Processor requirements
4. Sensor requirements (Type, Model, Purpose, Interface)
5. Actuator requirements (Motors, Servos, Relays, LEDs)
6. Connectivity requirements (WiFi, Bluetooth, MQTT, LoRa, Zigbee)
7. Power requirements (Battery, USB, Solar)
8. Firmware language and framework (C++, MicroPython, Arduino IDE)
9. Cloud/IoT platform requirements (AWS IoT, Blynk, ThingSpeak, Firebase)
10. Enclosure and physical design requirements
11. Testing requirements (Sensor calibration, Range testing)
12. Deployment requirements

Keep the hardware stack simple and realistic for a 24-48 hour hackathon.
Explain all hardware concepts in beginner-friendly language.
Do not introduce unnecessary components.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic IoT architecture with clear data flow from sensor to user.
```text
Act as a senior IoT architect.
Using the following PRD and TRD, design a realistic hackathon IoT architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended hardware stack (Microcontroller, Sensors, Actuators)
2. Complete IoT architecture diagram (Text-based, showing Device → Sensor → Gateway → Cloud → Dashboard/App)
3. Device architecture (Microcontroller, Peripherals)
4. Sensor architecture (Inputs)
5. Actuator architecture (Outputs)
6. Connectivity architecture (How data travels)
7. Cloud/IoT platform architecture (Where data is stored)
8. User interface architecture (Dashboard, Mobile App, Alerts)
9. Data flow (How a sensor reading becomes a user notification)
10. Power architecture (How the device is powered)
11. Security considerations
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary components. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. HARDWARE_SCHEMATIC.md
**Purpose:** To define components, pin mappings, wiring diagram, and power requirements.
```text
Act as a senior hardware engineer.
Using the PRD and System Architecture below, design the hardware schematic for this IoT hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Bill of Materials (BOM) — All components with quantities
2. Microcontroller pin mapping (Which pin connects to what)
3. Wiring diagram (Text-based, showing connections)
4. Power distribution (Voltage, Current, Regulators)
5. Sensor connections (I2C, SPI, Analog, Digital)
6. Actuator connections (PWM, Digital, Relay)
7. Communication module connections (WiFi, Bluetooth, LoRa)
8. Grounding and noise considerations
9. Physical layout suggestions
10. A checklist for verifying hardware connections before powering on

Explain why each component is needed.
Keep the hardware simple enough for a beginner hackathon team to assemble and debug.
```

---

### 6. SENSOR_SPEC.md
**Purpose:** To define each sensor's purpose, data format, calibration, and sampling rate.
```text
You are a senior IoT sensor specialist.
Using the PRD and Hardware Schematic below, create a Sensor Specification document for this IoT hackathon project.

PRD: [PASTE PRD]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]

For each sensor, provide:
1. Sensor name and model
2. Purpose in the project
3. Interface (I2C, SPI, Analog, Digital, UART)
4. Operating voltage
5. Data format (Raw values, Units)
6. Sampling rate (How often data is read)
7. Accuracy and range
8. Calibration requirements
9. Library or driver needed (Arduino library, Python library)
10. Example reading
11. Common issues and troubleshooting tips

Explain each sensor in beginner-friendly language.
Keep the sensor setup simple and realistic for a hackathon.
```

---

### 7. FIRMWARE_RULES.md
**Purpose:** To define the firmware logic, loops, interrupts, and state machines.
```text
Act as a senior embedded systems engineer.
Using the PRD and Hardware Schematic below, create the Firmware Rules document for this IoT hackathon project.

PRD: [PASTE PRD]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]

Provide:
1. Firmware architecture (Setup, Loop, Interrupts)
2. State machine design (States, Transitions)
3. Sensor reading logic (When and how to read)
4. Actuator control logic (When and how to activate)
5. Communication logic (When to send data)
6. Timing and scheduling (Delays, Timers, Non-blocking code)
7. Interrupt handling (If applicable)
8. Error handling in firmware (Sensor failure, Connection loss)
9. Power-saving logic (Sleep modes, Duty cycling)
10. A checklist for developers to verify firmware before the demo

Explain each logic rule in beginner-friendly language.
Keep the firmware simple and easy to debug.
```

---

### 8. CONNECTIVITY_PROTOCOL.md
**Purpose:** To define WiFi, Bluetooth, MQTT, LoRa, Zigbee, or HTTP communication.
```text
You are a senior IoT connectivity engineer.
Using the PRD and System Architecture below, create a Connectivity Protocol document for this IoT hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Connectivity method (WiFi, Bluetooth, LoRa, Zigbee, Cellular)
2. Protocol choice (MQTT, HTTP, WebSocket, CoAP)
3. Justification for the choice
4. Network configuration (SSID, Password, Broker URL)
5. Data format (JSON, CSV, Binary)
6. Publish/Subscribe topics (If using MQTT)
7. Data transmission frequency
8. Payload size and optimization
9. Connection recovery (Reconnect logic)
10. Security (TLS, Authentication)
11. Example data packet
12. A checklist for developers to verify connectivity before the demo

Explain each connectivity concept in beginner-friendly language.
Keep the connectivity simple and reliable for a hackathon demo.
```

---

### 9. POWER_MANAGEMENT.md
**Purpose:** To define power source, battery life, and energy optimization.
```text
Act as a power systems engineer.
Using the Hardware Schematic and Firmware Rules below, create a Power Management document for this IoT hackathon project.

HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]
FIRMWARE_RULES: [PASTE FIRMWARE_RULES]

Provide:
1. Power source (USB, Battery, Solar, DC Adapter)
2. Voltage and current requirements per component
3. Total power consumption estimate
4. Battery capacity and expected runtime
5. Power regulators and converters (Buck, Boost, LDO)
6. Power-saving techniques (Sleep modes, Duty cycling, Peripheral shutdown)
7. Power monitoring (If applicable)
8. Safety considerations (Overvoltage, Short circuit)
9. Fallback if power runs out during the demo
10. A checklist for developers to verify power before the demo

Explain each concept in beginner-friendly language.
Keep the power management simple and realistic for a hackathon.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define the dashboard or mobile app design, device status, and user flow.
```text
Act as a senior UI/UX designer specializing in IoT dashboards.
Using the PRD and System Architecture below, create a UI Specification document for an IoT hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (Device status card, Sensor readings, Charts, Alerts)
3. Screen-by-screen breakdown (Dashboard, Device Detail, Alerts, Settings)
4. Real-time data display (Live sensor values, Gauges, Charts)
5. Device connection states (Online, Offline, Connecting)
6. Loading states (Skeletons, spinners)
7. Error states (Device offline, Sensor failure)
8. Empty states (No data yet)
9. Responsive design guidelines (Mobile and Desktop)
10. Accessibility considerations (Contrast, keyboard navigation)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core device interaction and data flow.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when a sensor fails, connection drops, or power is lost.
```text
You are a senior embedded systems engineer.
Using the Hardware Schematic and Firmware Rules below, create an Error Handling document for an IoT hackathon project.

HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]
FIRMWARE_RULES: [PASTE FIRMWARE_RULES]

Provide:
1. Common failure modes (Sensor failure, Connection loss, Power loss, Component overheating)
2. Firmware-level error handling (Fallback values, Safe states)
3. Sensor error handling (Out-of-range values, No reading)
4. Connectivity error handling (Reconnect logic, Offline buffering)
5. Actuator error handling (Safe shutdown)
6. User notification (LEDs, Buzzer, Dashboard alerts)
7. Logging errors (Serial monitor, Cloud logs)
8. Recovery procedures (Auto-restart, Manual reset)
9. A checklist for developers to verify error handling before the demo

Focus on making the device resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To secure device authentication, data encryption, and firmware protection.
```text
Act as an IoT security engineer.
Using the System Architecture and Connectivity Protocol document below, create a Security document for an IoT hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
CONNECTIVITY_PROTOCOL: [PASTE CONNECTIVITY_PROTOCOL]

Provide:
1. Device authentication (Certificates, API keys, Tokens)
2. Data encryption (TLS, AES)
3. Secure boot and firmware protection (If applicable)
4. Network security (WiFi security, Firewall)
5. Cloud security (API key storage, Access control)
6. User data privacy (What data is collected?)
7. Physical security (Tamper detection, Enclosure)
8. OTA update security (If applicable)
9. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for hardware, sensors, and edge cases.
```text
Act as a QA engineer specializing in IoT and hardware.
Using the PRD and Hardware Schematic below, create a Testing document for an IoT hackathon project.

PRD: [PASTE PRD]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]

Provide:
1. Testing strategy for hardware
2. Component testing (Does each sensor/actuator work individually?)
3. Integration testing (Do components work together?)
4. Sensor calibration testing
5. Connectivity testing (Range, Stability, Reconnect)
6. Firmware testing (Logic, Timing, State transitions)
7. Power testing (Battery life, Voltage stability)
8. Edge cases (Sensor failure, Disconnection, Low power)
9. User acceptance testing checklist
10. A manual testing checklist for the demo
11. How to document known hardware limitations for judges

Keep the testing plan simple enough for beginner hardware developers to execute under time pressure.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures device performance and prepares for judge questions.
```text
You are an IoT evaluation expert.
Using the PRD and Hardware Schematic below, create an Evaluation document for an IoT hackathon project.

PRD: [PASTE PRD]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]

Provide:
1. Evaluation metrics (Sensor accuracy, Response time, Battery life, Connectivity reliability)
2. Evaluation methods (Manual testing, Benchmarking, Data logging)
3. Benchmarking (What is the baseline?)
4. Known limitations of the hardware or sensors
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about IoT/hardware and how to answer them

Focus on demonstrating that the team understands the device's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to flash firmware, connect to cloud, and set up the live demo.
```text
Act as an IoT deployment engineer.
Using the System Architecture and Hardware Schematic below, create a Deployment document for an IoT hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]

Provide:
1. Firmware flashing steps (Arduino IDE, PlatformIO, esptool)
2. Cloud platform setup (AWS IoT, Blynk, ThingSpeak, Firebase)
3. Device provisioning (WiFi credentials, API keys)
4. Dashboard deployment (Hosting the web dashboard)
5. Mobile app deployment (If applicable)
6. How to test the deployed system
7. Fallback plan if hardware fails during the hackathon
8. A pre-deployment checklist
9. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live demo as early as possible.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the hardware demo works perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem
3. Why the problem matters
4. Existing limitations
5. Our hardware solution
6. How it works (Sensor → Microcontroller → Cloud → Dashboard)
7. Technology (Arduino, ESP32, Sensors, MQTT)
8. Demo (The most important part — show the live device working)
9. Innovation
10. Impact
11. Future scope
12. Closing

Make the language natural and easy to speak.
Avoid corporate jargon.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Also provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Include a backup plan for hardware failure during the demo.
```

---

### 17. GLOSSARY.md
**Purpose:** To define all hardware terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Hardware Schematic, and Connectivity Protocol below, create a Glossary document for an IoT hackathon project.

PRD: [PASTE PRD]
HARDWARE_SCHEMATIC: [PASTE HARDWARE_SCHEMATIC]
CONNECTIVITY_PROTOCOL: [PASTE CONNECTIVITY_PROTOCOL]

Provide definitions for all key terms used in the project, including:
1. Hardware terms (Microcontroller, GPIO, PWM, ADC, I2C, SPI, UART)
2. Sensor terms (Analog, Digital, Calibration, Sampling Rate, Accuracy)
3. Actuator terms (Servo, Motor, Relay, Solenoid)
4. Connectivity terms (WiFi, Bluetooth, MQTT, LoRa, Zigbee, HTTP)
5. Power terms (Voltage, Current, Battery, Regulator, Sleep Mode)
6. Firmware terms (Setup, Loop, Interrupt, State Machine, Library)
7. Cloud/IoT terms (Broker, Topic, Publish, Subscribe, Dashboard)
8. Project-specific terms (Any custom terminology used in the PRD)
9. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience.
This will help all team members speak confidently to judges.
```

---

### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**

---
