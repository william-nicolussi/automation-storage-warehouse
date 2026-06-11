# Automation of a Storage Warehouse

An industrial automation project focused on developing the control logic from scratch for a 3-axis ($X, Y, Z$) warehouse stacker crane model. 

This project was developed for the *Automation and Control Laboratory* course at Politecnico di Milano.

## System Architecture

### Hardware:
* **PLC:** ABB PM554;
* **I/O Module:** ABB DC532 digital expansion module.

### Software & Environment
* **IDE:** ABB Automation Builder (for PC-to-PLC communication);
* **Control Logic:** CoDeSys 2.3 (programmed in Structured Text and SFC).

### Physical Model
* **Grid Configuration:** $3\times3$ storage slot matrix;
* **Axis Control:** 3 axes ($X, Y, Z$) driven by DC motors paired with a belt transmission system;
* **Sensor Layout:** 12 mechanical/inductive position switches, 2 physical handkeys, 1 Hall-effect sensor for pallet detection, and 2 signaling LEDs.

<div align="center">
  <img width="387" height="302" alt="Physical_model" src="https://github.com/user-attachments/assets/006e3300-a489-4c42-b948-6003495a94a8" />
</div>

## Getting Started

### Prerequisites
To open and run this project, you need **ABB Automation Builder** with **CoDeSys 2.3** integrated.

### Installation & Setup
1. Clone the repository:
```bash
git clone https://github.com/william-nicolussi/automation-storage-warehouse
```
2. Open the file `Warehouse/Warehouse.project` with ABB Automation Builder.

## Software Architecture

The general control execution and task management of the PLC program are coordinated through a multi-tier structure, organized as follows:

<div align="center">
<img width="600" alt="Software Structure" src="https://github.com/user-attachments/assets/2eca8837-9d10-4f42-a866-c5dcb25d7cdf" />
</div>

The overall program flow operates on a centralized database that tracks the warehouse layout and slot occupancy, as structured below:

<div align="center">
<img width="600" alt="Software Structure" src="https://github.com/user-attachments/assets/252c52b4-7242-4235-8906-2ad4c070f222" />
</div>

In order to bridge this digital grid mapping with the physical world, the system coordinates precise 3D spatial mapping and physical sensor tracking:

<div align="center">
<img width="600" alt="Software Structure" src="https://github.com/user-attachments/assets/15d9b793-0d7a-4576-8b73-c6e12280c1ce" />
</div>

## Graphical User Interface
It is possible to choose the work-mode of the warehouse system througt a GUI.

### Homepage
It is possible to choose the mode and it display errors changing the color of the background:
* **Green backgroud:** the system is fully operative;
* **Red background:** emergency button has been pressed;
* **Pink background:** the pins connected to the I/O module have an issue.


https://github.com/user-attachments/assets/3e6bb3f6-17bb-4644-bd18-28aff7f19ed2



https://github.com/user-attachments/assets/c8e0273f-f9bb-40e5-b921-0df8abbb1e07



### Manual Mode
It is possible to move the stacker freely. It is not possible to break the physical constraints: it is not possible to surpass the operating area and go beyond.



