# Wireless-Gesture-Controlled-Robotic-Arm

## Project Overview

The Wireless Gesture Controlled Robotic Arm is a project which is designed to control a robotic arm via natural hand movement. Rather than use a button to operate the arm or a wired controller, the user wears a glove with flex sensors. The flex sensors detect the amount of bend in the fingers and this is then used to control the arm.

The glove uses an Arduino Nano to read the flex sensor values and an nRF24L01+ wireless module to transmit the gesture data. A receiver on the robotic arm picks up the data and translates it into motor commands. This gives you a wireless human machine interface for controlling the arm.

## How It Works

1. Gesture detection: flex sensors in the glove detect when the fingers are bent.
2. Signal processing: an Arduino Nano reads the sensor values via voltage divider circuits.
3. Wireless communication: the gesture data is sent to the robotic arm via an nrf24l01+ module.
4. Motor control: the receiver takes the incoming values and maps them to arm movement.

## Hardware Design

### Glove Controller

- Five flex sensors for finger movement detection
- Arduino Nano V3
- nRF24L01+ wireless transceiver
- 10 kΩ resistors for sensor voltage-divider circuits

### Robotic Arm — Target Configuration

- Arduino Nano V3 with an nRF24L01+ receiver
- Six DS3218 servo motors, controlled through a PCA9685 PWM driver
- One NEMA 17 stepper motor with a DRV8825 driver for 360-degree base rotation
- Separate regulated power rails for the motors and control electronics
