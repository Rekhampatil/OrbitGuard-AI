# OrbitGuard AI 🚀

### AI-Assisted Satellite Collision Risk Detection and Avoidance

## 1. Project Overview

OrbitGuard AI is a prototype that combines camera-based debris detection, satellite orbit prediction, collision-risk assessment, and maneuver planning to demonstrate how satellites could avoid potential collisions.

## 2. Problem Statement

Space debris and inactive satellites can threaten operational spacecraft. Detecting potential close approaches and planning safe maneuvers are important challenges in space sustainability.

## 3. Proposed Solution

OrbitGuard AI combines two approaches:

* **Known satellites:** Use orbital data (TLE) and SGP4 to predict satellite positions.
* **Unknown debris:** Use camera images and computer vision to detect and track visible objects.

The software assesses a selected collision scenario, displays a risk alert, and recommends a simulated avoidance maneuver.

## 4. Main Features

* Camera-based object detection
* Satellite orbit prediction
* Collision-risk assessment
* Maneuver planning
* ESP32-controlled physical satellite model
* Dashboard for alerts and simulation results

## 5. Hardware

* ESP32 DevKit
* Compatible camera module
* Servo motor
* Stepper motor and compatible driver
* LEDs, resistors, jumper wires, and breadboard
* Physical satellite model and guided orbit tracks

## 6. Software and Platforms

* Arduino IDE and ESP32
* Python and OpenCV
* YOLO for object detection, if feasible
* SGP4 and TLE data for known satellite prediction
* Streamlit and Plotly for the dashboard
* GitHub for collaboration and version control

## 7. System Workflow

Camera / orbital data → Detection and prediction → Risk assessment → Maneuver planning → ESP32 hardware response → Result dashboard

## 8. Team Contributions

Team members will work on hardware, image detection, orbit prediction, risk assessment, maneuver planning, dashboard development, testing, and presentation.

## 9. Expected Outcome

A working prototype demonstrating the connection between sensing, software-based risk assessment, simulated maneuver planning, and physical hardware movement.

## 10. Important Note

This is a prototype and simulation. A single camera image cannot determine an unknown object's complete orbit, and the physical model does not perform real orbital maneuvers.

