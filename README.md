# Bluetooth_Based_Robotic_Car

##  Project Overview
This project demonstrates a **Bluetooth-controlled robotic car** using the **8051 microcontroller (AT89S52)**.  
The car is wirelessly operated via a smartphone app, communicating through the **HC-05 Bluetooth module**.  
Commands are processed by the microcontroller to control the **L298 motor driver**, enabling forward, backward, left, right, and stop movements.

##  Components Used

- 8051 Microcontroller (AT89S52)  
- HC-05 Bluetooth Module  
- L298 Motor Driver  
- Four DC Motors + Chassis & Wheels  
- Lithium-Ion Battery  
- Crystal Oscillator (11.0592 MHz)  
- Resistors, Capacitors, LEDs, Switches  

##  Block Diagram
Smartphone → HC-05 (Bluetooth UART) → 8051 MCU → L298 Motor Driver → DC Motors  

Commands:  
- `f` → Forward  
- `b` → Backward  
- `l` → Left  
- `r` → Right  
- `s` → Stop  

##  Working Principle

1. Send Commands – Smartphone app sends characters (`f`, `b`, `l`, `r`, `s`).  
2. Receive Commands – HC-05 forwards signals to 8051 MCU.  
3. Process & Drive – MCU interprets commands and controls L298 motor driver.  
4. Movement – Car maneuvers accordingly.  

## Pseudo Code (Simplified)

void move_forward();
void move_backward();
void turn_left();
void turn_right();
void stop();

if(s == 'f') move_forward();
else if(s == 'b') move_backward();
else if(s == 'l') turn_left();
else if(s == 'r') turn_right();
else if(s == 's') stop();
