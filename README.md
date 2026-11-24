<img width="1470" height="879" alt="Screenshot 2026-11-20 at 9 18 07 PM" src="https://github.com/user-attachments/assets/6be6c744-42a9-42ac-9ae6-0b8331a8252f" />
<img width="1470" height="956" alt="Screenshot 2026-11-21 at 12 12 47 AM" src="https://github.com/user-attachments/assets/8eba6bd4-6f2c-4695-be0f-d32c6dbf94eb" />
<img width="1136" height="949" alt="Screenshot 2026-11-21 at 8 37 08 PM" src="https://github.com/user-attachments/assets/85cf361d-3dd0-4868-ae9e-aacd3971ef3f" />
<img width="1470" height="956" alt="Screenshot 2026-11-21 at 8 34 04 PM" src="https://github.com/user-attachments/assets/80f35e72-d402-4954-a72f-0bb9a090f487" />
<img width="1600" height="882" alt="PHOTO-2026-11-18-00-02-23" src="https://github.com/user-attachments/assets/31ecf532-e180-4a81-84c9-74c7491e91a3" />
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
