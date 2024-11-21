# Mores-Code
# Morse Code Transmitter Project

## Introduction

### What is Morse Code?  
Morse code is a method used in telecommunication to encode text characters into sequences of two different signal durations:  
- **Dots** (short signals)  
- **Dashes** (long signals)  

It was named after **Samuel Morse**, one of the inventors of the telegraph, and created to transmit natural language using electrical pulses and silence over long distances via telegraph systems. 

#### Applications of Morse Code  
- Historically: Used in telegraphy.  
- Modern Uses: Radio communication, emergency signaling, aviation, and maritime communication.  
- Transmission Methods: Can be communicated via sound, light (e.g., flashlight), or vibration devices.  

### Project Overview  
In our project, we utilize a **light source** and a **sound source** to communicate in Morse code.

---

## Project Description  

### What Does Our Project Do?  
Our project acts as a Morse code **transmitter**:  
1. It receives a word from a connected phone via **Bluetooth**.  
2. Transforms the word into Morse code.  
3. Outputs the encoded word as:  
   - **Sound pulses** using a buzzer.  
   - **Light pulses** using a laser module.  

### How Does Our Project Work?  
1. **Input**: Receives the word via Bluetooth.  
2. **Processing**:  
   - Two arrays are used:  
     - First array: Contains the alphabet.  
     - Second array: Contains the corresponding Morse code.  
   - For each letter in the word:  
     - The device finds the index of the letter in the alphabet array.  
     - Retrieves the corresponding Morse code from the second array using that index.  
     - Loops through the Morse code, converting:  
       - **Dashes** into long pulses.  
       - **Dots** into short pulses.  
3. **Output**: Transmits the Morse code using:  
   - A **laser module** for light pulses.  
   - A **buzzer** for sound pulses.  

---

## Components  

### Arduino  
Serves as the **brain** of the device, connecting and managing all components.  

#### Pins Used:  
- **0,1**: TX/RX communication pins for Bluetooth module.  
- **13**: Digital signal pin for the laser module.  
- **12**: Output signal pin for the buzzer.  
- **A4**: Connected to SDA.  
- **A5**: Connected to SCL.  

### Bluetooth Module  
Enables the device to receive words via a phone as a serial monitor.  

#### Pins Used:  
- **VCC**: Provides bias voltage.  
- **GND**: Ground connection.  
- **TX**: Connected to Arduino RX.  
- **RX**: Connected to Arduino TX.  

### Laser Module  
Represents Morse code using light pulses.  

#### Pins Used:  
- **S**: Signal pin connected to Arduino pin 13.  
- **Middle Pin**: VCC connected to Arduino 5V.  
- **-**: Ground connection.  

### Buzzer  
Represents Morse code using sound pulses.  

#### Pins Used:  
- **Long Pin (+)**: Connected to Arduino pin 12.  
- **Short Pin (-)**: Connected to GND.  

### LCD Monitor  
Displays each letter and its corresponding Morse code during transmission.

---

## Summary  
This project demonstrates the use of Morse code for communication through both light and sound. By utilizing an Arduino, a laser module, and a buzzer, we created a simple yet effective way to encode and transmit text messages in Morse code.  
