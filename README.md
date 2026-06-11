# Automation of a Storage 

An industrial automation project focused on developing the control logic from scratch for a 3-axis ($X, Y, Z$) warehouse stacker crane model. 

This project was developed for the *Automation and Control Laboratory* course at **Politecnico di Milano**.

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
<img width="387" height="302" alt="Physical_model" src="https://github.com/user-attachments/assets/006e3300-a489-4c42-b948-6003495a94a8" />
## Getting Started

### Prerequisites
To open and run this project, you need **ABB Automation Builder** with **CoDeSys 2.3** integrated.

### Installation & Setup
1. Clone the repository:
```bash
git clone https://github.com/william-nicolussi/automation-storage-warehouse
```
2. Open the file `Warehouse/Warehouse.project` with ABB Automation Builder.

## Video
https://github.com/user-attachments/assets/b75e63d5-2820-4528-bcf3-6f4b046c7512
