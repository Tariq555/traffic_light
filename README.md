# Raspberry Pi Pico Traffic Light (MicroPython) Project

## Introduction
In this project, we will build a Raspberry Pi Pico Traffic Light using MicroPython and state machine logic. The traffic light will simulate a typical traffic light sequence, cycling through red, yellow, green, and a short yellow phase. This project aims to provide an easy-to-understand demonstration of using state machines for controlling LEDs and to have a fun and educational DIY project.

## Objective
The main purpose of this project is to create a functioning traffic light simulation using the Raspberry Pi Pico and MicroPython. By implementing state machine logic, we can effectively control the behavior of the traffic light, allowing it to change its signals in a realistic manner. This project is a great way to understand the principles of state machines and apply them to a real-world application.

## Materials Used
- Raspberry Pi Pico
- Breadboard and jumper wires
- Three LEDs (red, yellow, green)
- Three current-limiting resistors (appropriate values for the LEDs used)
- Micro USB cable for power
- Computer with the Thonny IDE installed

## Step-by-Step Instructions

### Step 1: Hardware Setup
1. Connect the three LEDs to the GPIO pins of the Raspberry Pi Pico using jumper wires.
2. Insert appropriate current-limiting resistors in series with each LED to avoid damaging them.
3. Connect the Raspberry Pi Pico to your computer using a Micro USB cable for power.

### Step 2: Writing the MicroPython Code
1. Open the Thonny IDE on your computer and create a new MicroPython script for the traffic light project.
2. Import the necessary libraries and set up the GPIO pins for the LEDs as outputs.
3. Define the states of the traffic light (e.g., RED, YELLOW, GREEN) and the transitions between them.
4. Implement the state machine logic to control the LEDs based on the defined states and transitions.
5. Add a loop to keep the traffic light running indefinitely, allowing it to cycle through the states repeatedly.

Here's an example of the code you can use:

```python
from machine import Pin
import time

RED = Pin(2, Pin.OUT)
YELLOW = Pin(3, Pin.OUT)
GREEN = Pin(4, Pin.OUT)

while True:
    RED.value(1)
    time.sleep(5)
    YELLOW.value(1)
    time.sleep(2)
    GREEN.value(1)
    RED.value(0)
    YELLOW.value(0)
    time.sleep(5)
    GREEN.value(0)
```

## Step 3: Uploading the Code to Raspberry Pi Pico
- Save the MicroPython script with an appropriate name.
- Connect the Raspberry Pi Pico to your computer via the Micro USB cable.
- Use the Thonny IDE to upload the code to the Raspberry Pi Pico.
- Once the code is uploaded, the traffic light will start simulating the traffic light sequence.

## Step 4: Testing and Adjustments
- Observe the behavior of the traffic light to ensure it cycles through the states correctly.
- If necessary, make adjustments to the timings or transitions in the code to achieve a more realistic simulation.
