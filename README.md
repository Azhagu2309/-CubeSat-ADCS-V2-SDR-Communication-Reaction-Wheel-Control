# -CubeSat-ADCS-V2-SDR-Communication-Reaction-Wheel-Control

🚀 CubeSat ADCS V2 – SDR Communication & Reaction Wheel Control
A low-cost CubeSat Attitude Determination and Control System (ADCS) prototype integrating SDR-based LoRa communication, GNU Radio decoding, and a 1-axis reaction wheel mechanism, developed for Ingenium’26 conducted by National Institute of Technology Tiruchirappalli under Pragyan.

💰 Total Project Budget: ₹1100 – ₹1300
👨‍🚀 Team: Win + Space + Go

📌 Project Overview
This project represents Version 2 of our CubeSat ADCS prototype.
Unlike Version 1, which used a servo-based actuation system and basic communication setup, Version 2 focuses on:

Realistic reaction wheel implementation
SDR-based communication architecture
Signal decoding using GNU Radio
Improved mechanical design with weight optimization
Cost-efficient engineering
All relevant source code, design files, screenshots, and supporting documents are available inside this repository.

This version was not just an upgrade — it was a complete redesign from communication to control and mechanical structure.

🛰️ System Architecture
Communication Flow
LoRa (SX1278 Transmitter)
→ RTL-SDR Receiver
→ Spectrum Analysis (SDR++)
→ GNU Radio Decoding
→ Microcontroller Processing
→ Reaction Wheel Control

Control Flow
Sensor Input
→ Arduino Controller
→ ESC
→ BLDC Motor
→ Reaction Wheel
→ Roll Stabilization

System architecture diagrams and block representations are included inside the repository under the documentation folders.

📡 SDR-Based Communication System
Hardware Used
LoRa SX1278 (Transmitter)
RTL-SDR Module (Receiver)
Software Tools
SDR++ (Spectrum Analysis)
GNU Radio (Signal Decoding)
Why SDR?
Initially, we were only visualizing the spectrum of the received signal.
However, spectrum observation alone does not complete a communication system.

As communication engineers, we realized:

True communication requires decoding, not just visualization.

Therefore, we implemented GNU Radio-based decoding to interpret the transmitted data properly.

Major Challenge
The decoding stage took nearly 2–3 days of debugging.
We faced:

Incorrect block configurations
Sample rate mismatches
Flowgraph debugging issues
Successfully decoding the signal provided immense practical learning in SDR systems.

GNU Radio flowgraphs, SDR spectrum screenshots, and configuration files are included within this repository.

⚙️ ADCS – Reaction Wheel Mechanism
Why Reaction Wheel?
In Version 1, a servo actuator was used.
In Version 2, we upgraded to a real reaction wheel mechanism for 1-axis roll control.

Reaction wheels are widely used in real satellites for attitude control, making this implementation closer to practical aerospace systems.

Working Principle
When the reaction wheel accelerates in one direction,
The Cube rotates in the opposite direction (Newton’s Third Law).
This enables roll control without external torque.

Firmware source code and control implementation details are available in the repository.

🔌 ESC Challenge
A major hardware limitation emerged:

We only had a unidirectional ESC.

For proper 1-axis ADCS:

The motor must rotate in + roll and – roll directions.
However:

Our ESC required manual polarity reversal.
We searched for a bidirectional ESC:

Ritchie Street
Online platforms
College departments
It was unavailable everywhere.

Finally, we completed the system using available components.

This taught us an important engineering lesson:

Real projects are completed not with perfect resources, but with problem-solving mindset.

🧱 Mechanical Design
Design Goals
Minimum cost
Maximum functionality
Compact structure
Specifications
Cube Dimension: 15 × 15 cm
Load: ~600–700 grams
Materials Used
Sunboards (Structure)
Acrylic Sheets (Base)
DIY Plastic Shaft Material
3D Printed Bearing Holder (Only essential component printed)
Major Mechanical Challenge
Weight balancing.

With 600–700g inside a compact cube:

Improper distribution affected stability
Reaction wheel performance was impacted
After multiple iterations and redistribution techniques, stable balance was achieved.

Mechanical design notes, structural images, and documentation are included in this repository.

💰 Bill of Materials (Approximate)
Component	Estimated Cost (₹)
LoRa SX1278	250
ESC	300
BLDC Motor	250
Structural Materials	200
Miscellaneous	200
Total	₹1100–1300
Completing an SDR + Reaction Wheel ADCS system within this budget was one of our key achievements.

🔄 Version Comparison
Feature	Version 1	Version 2
Communication	Basic	SDR + GNU Radio Decoding
Actuator	Servo	Reaction Wheel
Mechanical Design	Basic Frame	Redesigned 15x15 Cube
Engineering Depth	Moderate	System-Level Integration
👨‍🚀 Team – Win + Space + Go
This project was built with the collective effort of:

Sarveswaran A
Azhagumurugan R
Radhakrishnan S
Kamalnath S
Their endless cooperation throughout the hackathon made this possible.

🎯 Lessons Learned
This hackathon taught us:

Practical SDR implementation
GNU Radio signal processing
Embedded control under constraints
Mechanical balancing techniques
Cost-optimized engineering
Hardware troubleshooting under real-world limitations
Version 2 feels less like a prototype and more like a real engineering system.

🚀 Future Improvements
Bidirectional ESC integration
Closed-loop PID control
3-Axis ADCS expansion
Telemetry feedback system
Advanced sensor fusion
📍 Event
Developed for:

Ingenium’26
Conducted by National Institute of Technology Tiruchirappalli
Under Pragyan’26
