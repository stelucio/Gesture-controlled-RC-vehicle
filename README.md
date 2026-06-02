# Gesture-controlled-RC-vehicle

# IoT project:  Gesture-controlled RC vehicle

My project consists of a small remote‑controlled rover that uses a gyroscope for steering and movement. 

## Table of contents
* [Hardware and software reuirements](#hardware-and-software-requirements)
* [Project layout](#project-layout)
* [User guide](#user-guide)
* [Links](#links)

## Hardware and software requirements

### Hardware requirements
- Jumper 
- x2 NRF24L01+ PA LNA SMA Antenna 2,4 GHz
- x2 NRF adapter
- x1 ARDUINO UNO R4 WIFI
- x1 Power Bank 10400 mA 5V-2.1A
- x1 L298N Motor Driver
- x2 Battery pack 3V
- x4 5V Motors 
- x4 Tires
- chassis 
- Power Bank 5000mA
- AZDelivery AZ-Nano V3-Board
- AZDelivery AZ-Nano V3-Board case
- MPU 6050 support 
- straps
- Adhesive tape
- 5 volt benchtop generator
- Stagnator
- USB-C cables
- Screws
- Bolts

### Software requirements
- Arduino IDE
- Common libraries (...)

## Project layout
~~~
/project-root
├── README.md
├── docs/
├── firmware/
│   ├── arduino_car/
│   ├── progettoRX_TX_con_NRF04_TX_RX_RF/
│   └── TEST_FILE/
├── hardware/
├── images/
├── report/
├── .gitignore
└── LICENSE
~~~
- `docs/` contains the web page and supporting scripts used for the project presentation.
- `firmware/` contains all embedded software sources.
- `arduino_car/` contains the directory `Progetto_RX_TX` necessary to burn and run the transmitter and the receiver code
- `TEST_FILE/` includes isolated tests for motors, sensors etc...
- `hardware/` contains schematics.
- `images/` stores pictures used in documentation.


### 3. Firmware Arduino (for the car)
#### Receiver configuration and how to burn and run it
- Put to **off state** the switch of the battery to avoid unusual power consumption.
- Open `firmware/arduino_car/Progetto_RX_TX/nRF24L01_RX/nRF24L01_RX.ino`.
- Connect your **Arduino uno R4 WIFI** to your PC, compile the code and upload it on the board.
#### Transmitter configuration and how to burn and run it
- Open `firmware/arduino_car/Progetto_RX_TX/nRF24L01_RX/nRF24L01_TX.ino`.
- Connect the board **Arduino nano** to your PC, compile the code and upload it on the board.
- Put the mpu on a **plane surface** in order to calibrate the mpu correctly and open the serial monitor.
- When you see on the serial monitor the message **"Setup completato!"**, means that you have done a good wiring and now you can put to on state the switch of the battery to run the system.
- Put to **on state** the switch of the car battery and enjoy with your project.
#### MPU GESTURES CONTROL
- To drive your car sees the demo on youtube that explains all the gestures necessary to drive it.
- A cartesian visualization of the gestures is shown at [Click here](images/Mpu_gestures_cartesian_visualization.pdf).


## Team members and contributions
- Luciani Stefano - Responsible for the hardware design, component wiring and the development of the control and communication software for RC car.
Responsible for the  development of the finite state machine of the velox and its hardware design.

