# Maze-Solving MicroMouse Using STM32F103C8T6

## 🐭 Project Overview

This project implements a **maze-solving robot** (MicroMouse) using the **STM32F103C8T6 microcontroller**. The robot navigates a maze by reading distances via the **HC-SR04 ultrasonic sensor**, calculating the optimal movement with a **PID controller**, and controlling its **N20 motors** through the **TB6612 motor driver**. The system is designed for precision, efficiency, and adaptability in solving mazes.

---
Demo Video: https://www.youtube.com/watch?v=46l-LxFwiJM

---

## ✨ Key Features

- **Ultrasonic Sensing**: Real-time distance measurement to detect maze walls.  
- **PID Control**: Smooth and precise motion control for accurate navigation.  
- **Motor Driver Integration**: Efficient power management using the TB6612 driver.  
- **Algorithmic Pathfinding**: Solve mazes with optimized decision-making (future improvement for A* or Flood-Fill algorithms).  
- **Scalable Design**: Easily customizable for different mazes or challenges.  

---

## 🛠️ Technical Details

### Hardware Components
1. **Microcontroller**: STM32F103C8T6 ("Blue Pill").
2. **Ultrasonic Sensor**: HC-SR04 for wall detection.
3. **Motor Driver**: TB6612 to drive N20 DC motors.
4. **Motors**: N20 gear motors for movement and precise control.
5. **Power Supply**: 3.7V LiPo battery for compact and portable operation.

### Functional Architecture
1. **Input**:
   - HC-SR04 sensors read distances from walls.
   - PID controller computes corrections based on sensor inputs.
2. **Processing**:
   - STM32F103 processes ultrasonic readings, implements PID, and calculates motor speed.
3. **Output**:
   - Motor speeds are adjusted via PWM signals through TB6612 motor driver.

---

## ⚙️ How It Works

1. **Initialization**:
   - STM32 initializes peripherals: ultrasonic sensors, PWM for motors, and timers.
   - Default PID parameters are set.

2. **Maze Navigation**:
   - HC-SR04 sensors measure distances to walls.
   - PID controller minimizes error to keep the robot aligned within the maze path.
   - Decisions for left, right, or straight paths are made dynamically based on sensor inputs.

3. **Motor Control**:
   - Calculated PID output determines motor speed and direction.
   - PWM signals are sent to the TB6612 driver, which controls the N20 motors.

4. **Real-Time Adjustments**:
   - Continuous feedback loop adjusts robot trajectory in real time.

---

## 🔧 Hardware Requirements

- **Microcontroller**: STM32F103C8T6
- **Ultrasonic Sensors**: 2-3 HC-SR04 (depending on maze complexity)
- **Motor Driver**: TB6612
- **DC Motors**: N20 with encoder (optional for advanced feedback)
- **Power Supply**: 3.7V LiPo battery
- **Chassis**: Compact robot frame with space for components

---



