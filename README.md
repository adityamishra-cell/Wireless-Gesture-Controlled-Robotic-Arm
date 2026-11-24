<img width="1470" height="879" alt="Screenshot 2026-11-20 at 9 18 07 PM" src="https://github.com/user-attachments/assets/6be6c744-42a9-42ac-9ae6-0b8331a8252f" />
<img width="1470" height="956" alt="Screenshot 2026-11-21 at 12 12 47 AM" src="https://github.com/user-attachments/assets/8eba6bd4-6f2c-4695-be0f-d32c6dbf94eb" />
<img width="1136" height="949" alt="Screenshot 2026-11-21 at 8 37 08 PM" src="https://github.com/user-attachments/assets/85cf361d-3dd0-4868-ae9e-aacd3971ef3f" />
<img width="1470" height="956" alt="Screenshot 2026-11-21 at 8 34 04 PM" src="https://github.com/user-attachments/assets/80f35e72-d402-4954-a72f-0bb9a090f487" />
<img width="1600" height="882" alt="PHOTO-2026-11-18-00-02-23" src="https://github.com/user-attachments/assets/31ecf532-e180-4a81-84c9-74c7491e91a3" />
# Wireless-Gesture-Controlled-Robotic-Arm

## Project Overview

The Wireless Gesture Controlled Robotic Arm is a project which uses hand gesture to control the arm. Instead of using buttons or a controller the arm is controlled by hand gestures using the flex sensors   

The glove sense the finger movement and converts into the electrical signal which is then processed by arduino nano present in the glove and then those processed data is send to the robotic arm wirelessly through nRF24L01+ transceiver module. The other arduino nano present in the arm receives gesture data and convert it into the motor command and then robotic  arm replicate the hand movement 

The project is all about the wireless communication and human machine interaction 

## How It Works

1. Gesture detection: There are 5 flex sensors present on every finger of the glove which will give the data on the bending and on the basis of there  range 
2. Signal processing: An arduino nano will read the analog data coming from the flex sensors through voltage divider circuits 
3. Data Transmission: After the sensor Data is processed then it is transmitted wirelessly via nRF24L01+ transceiver module
4. Data Reception: The nRF24L01+ module present at the arm end will receive the data and send it to the another arduino nano of the robotic arm
5. Motor control: The received data is synced with the appropriate motor positions and movement commands
6. Arm Movement: Now, the servo motor and stepper motor will perform there movement accurately on the sync with the code.

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
