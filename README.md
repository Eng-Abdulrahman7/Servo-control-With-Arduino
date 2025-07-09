# Servo-control-With-Arduino
This project demonstrates how to control *4 servo motors* using an *Arduino Uno board

# Arduino Servo Control with 4 Servo Motors

## Overview
This project demonstrates how to control *4 servo motors* using an *Arduino Uno board. The servos are connected to the Arduino board and will move in a sweeping motion (from 0° to 90° and back to 0°). The circuit and code were created and tested in **Tinkercad* for easy simulation and prototyping.

This project uses the *Servo library* to control the servo motors connected to specific pins on the Arduino. It can be used for basic servo control or as part of a larger robotic project.

## Components Used
- *4 x Servo Motors*
- *Arduino Uno*
- *Breadboard*
- *5V Battery* or external power supply for the servos

## Circuit Diagram
The circuit shows how to connect *4 servo motors* to an *Arduino Uno* board using a *breadboard* for wiring. The following image shows the connection of the servo motors to the Arduino in *Tinkercad*:

Key Functions:
	•	myservo.write(pos): Sets the angle of the servo to the specified position (pos).
	•	delay(5): Introduces a short delay (5 milliseconds) between each servo movement to ensure smooth transitions.

Algorithm:
	1.	The program starts by moving the servos from 0° to 90°.
	2.	It then moves them back from 90° to 0°.
	3.	This process repeats continuously in a loop, causing the servos to “sweep” back and forth.

 # Humanoid Robot Walking Algorithm

## Overview
This project demonstrates how a humanoid robot can walk using 4 servo motors. The algorithm includes movement steps for both legs and hips to create a walking pattern.

## Algorithm Steps

1. *Start*:
   - Set all servo motors to 90° (neutral position).
   
2. *Move the right leg forward*:
   - Move the right hip motor to 120°.
   - Move the right knee motor to 110°.
   - Adjust the right ankle motor for balance.

3. *Shift weight to the right leg*:
   - Move the left hip motor slightly forward (80°).

4. *Move the left leg forward*:
   - Move the left hip motor to 120°.
   - Move the left knee motor to 110°.
   - Adjust the left ankle motor for balance.

5. *Shift weight to the left leg*:
   - Move the right hip motor slightly forward (80°).

6. *Repeat steps 2–5 for continuous walking*.

## Code Example
Here is an Arduino example code that moves the servos for walking.

```cpp
#include <Servo.h>

Servo rightHip;
Servo leftHip;
Servo rightKnee;
Servo leftKnee;

void setup() {
  rightHip.attach(9);
  leftHip.attach(10);
  rightKnee.attach(11);
  leftKnee.attach(12);
}

void loop() {
  // Implement walking algorithm here
}
