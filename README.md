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

##  OUTPUT

### Robotic Car

<img width="960" height="1280" alt="Robo_Car" src="https://github.com/user-attachments/assets/dc9df72d-4011-4ed0-b34e-9b03cc8732ce" />

###  PCB Design
#1 Schematic Layout

<img width="621" height="505" alt="schematic_Layout" src="https://github.com/user-attachments/assets/f1b5e13e-2451-4c3d-9135-f9927d657b29" />


#2 PCB Layout

<img width="516" height="533" alt="PCB_Layout" src="https://github.com/user-attachments/assets/8cda279a-fc82-4e7e-bfa4-5d9bc9c461cc" />


#3 3-D Front_Back View

<img width="651" height="679" alt="3D_Front_View" src="https://github.com/user-attachments/assets/cfe9aaa9-1bf2-4154-8b9e-3916e7a4517c" />

<img width="648" height="679" alt="3D_Back_View" src="https://github.com/user-attachments/assets/fa4fff43-6a27-4b4b-b340-9f615c8085ff" />
