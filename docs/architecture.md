# OrbitGuard AI — System Architecture

## 1. Overview

OrbitGuard AI is a prototype that combines computer vision, satellite orbit prediction, collision-risk assessment, maneuver planning, and a physical ESP32-controlled model.

## 2. System Modules

### A. Camera Detection

* Capture images of the prototype scene using a compatible camera.
* Use Python and OpenCV to process the images.
* Detect visible objects or obstacles.
* YOLO-based detection may be added if feasible.

### B. Orbit Prediction

* Use TLE (Two-Line Element) data for known satellites.
* Use the SGP4 model to estimate satellite positions.
* Compare predicted positions to study a selected collision scenario.

### C. Risk Assessment

* Evaluate the selected scenario using available position and distance information.
* Generate a prototype risk level, such as LOW, MEDIUM, or HIGH.
* Clearly label simulated or estimated results.

### D. Maneuver Planner

* Recommend a simulated avoidance action when the scenario is marked HIGH risk.
* Display the planned action and its expected effect in the prototype.
* Do not present simulated results as real spacecraft maneuver calculations.

### E. ESP32 Hardware

* Receive a movement command from the prototype software.
* Use a servo to change the model's orientation.
* Use a stepper motor and compatible driver to move the model along its guided track.
* Use LEDs to indicate warning or simulated maneuver activity.

### F. Dashboard

* Display camera detection results.
* Show orbit-prediction and risk information.
* Display the recommended simulated maneuver.
* Show the physical model's status where hardware communication is implemented.

## 3. System Workflow

1. Receive camera images or orbital data.
2. Detect visible objects or predict known satellite positions.
3. Evaluate a selected collision scenario.
4. Display the risk level.
5. Recommend a simulated avoidance action.
6. Send a movement command to the ESP32 when integration is ready.
7. Display the result on the dashboard.

## 4. Proposed Technology

* Python
* OpenCV
* SGP4 and TLE data
* Streamlit and Plotly
* ESP32 with Arduino IDE
* Servo motor, stepper motor, and LEDs
* YOLO, if feasible

## 5. Prototype Limitations

* A single camera image cannot determine an unknown object's complete orbit.
* The physical model demonstrates movement, not a real orbital maneuver.
* Prediction accuracy and risk calculations must be tested before reporting performance.
* Features that have not yet been implemented must be identified as planned.

## 6. Current Status

This document describes the proposed architecture. Implementation and testing will determine which features are completed for the final demonstration.
