#  ROBOT – The Path Guider

A Raspberry Pi Pico–based robot that can **map, store, and replay predefined paths** while avoiding obstacles.  
The robot uses an **ultrasonic sensor for distance measurement**, motors for movement, and an LCD display for feedback.  
It supports two mapping modes (A–B and A–C) and can autonomously follow recorded paths after mapping.

---

##  Features
- **Path Mapping** – Record the robot’s movement sequence and timings for predefined trips (A–B or A–C).  
- **Path Replaying** – Execute stored paths automatically without manual control.  
- **Obstacle Detection** – Ultrasonic sensor ensures safe navigation by stopping and alerting with a buzzer when obstacles are too close.  
- **LCD Display** – Provides live feedback about mode selection, path mapping, and trip execution.   

---

## 🛠️ Tools & Technologies
- **Microcontroller**: Raspberry Pi Pico (MicroPython)  
- **Programming Language**: Python (MicroPython)  
- **Components Used**:  
  - Ultrasonic sensor (HC-SR04)  
  - DC motors with motor driver  
  - LCD display (16x2, 4-bit mode)  
  - Push buttons (for mode selection)  
  - Buzzer (for obstacle alerts)  

---

## ⚙️ How It Works
1. **Mapping Mode (A–B / A–C)**  
   - Controlled via UART commands (`1` = forward, `2` = backward, `3` = left, `4` = right, `5` = stop).  
   - Movements and timings are stored in a list.  

2. **Trip Mode**  
   - The robot replays the stored movement list and follows the same path.  
   - Displays trip status on LCD (`Trip A–B` or `Trip A–C`).  

3. **Obstacle Detection**  
   - If an obstacle is detected within 15 cm, the robot stops, activates the buzzer, and resumes when clear.  

---

## 📝 Project Description
**ROBOT – The Path Guider** is a robotic system built using **Python (MicroPython)** on a **Raspberry Pi Pico**.  
The robot is capable of navigating along **predefined paths** (A–B, A–C), storing them, and replaying them with high accuracy.  
Obstacle detection ensures safety, and an LCD provides real-time user feedback.  
