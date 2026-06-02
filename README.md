# 3D Printing and Modeling Final Project: Mechanical Counter

## 1. Project Description
This project consists of the 3D design and modeling of a mechanical counter capable of counting by incrementing values by place value. The mechanism relies on gears and levers that transfer motion: with every full rotation of the ones wheel, the tens wheel advances by one position, simulating the base-10 counting system. 

The design was created in Fusion 360, adhering to strict organizational principles (naming components, structuring sketches) and is optimized for 3D printing with minimal support material. I divided the model into multiple components (case, shaft, digit wheels) to ensure proper assembly, optimal tolerances, and good mechanical resilience during use.

![Mechanical Counter](Render.png)

## 2. Project Files
All the necessary files can be found in this repository:
* `Assemble.f3z` - The source project file from Autodesk Fusion 360 (contains the entire assembly, including the motion links).
* `Final.gcode` - The G-code file ready to be sent to the 3D printer.
* `Parts/` folder - Contains the `.f3d` files for all components.
* `Slices/` folder - Contains the `.stl` files for all individually printable components.

## 3. Functionality & Video
The mechanism includes Motion Study to simulate the correct movement of the gears and the incrementation of the digits in Fusion 360. 

🎥 **https://youtu.be/JG6wwnlA_w0**

*Note: The local video file `MotionStudy.mp4` is also attached in this repository to showcase functionality.*

## 4. List of Components and Their Purpose
The project is divided into several bodies and components to facilitate printing and the independent operation of the parts:

* **Shaft:** The main support rod on which the digit wheels are mounted. It allows them to rotate independently on the axis.
* **Digit wheels:** The main display components. They are divided into three elements, representing the numerical values:
  * *Ones wheel:1* - The units wheel (incremented manually or by the main lever).
  * *Zecimal wheel:1* - The tens wheel.
  * *Hundred wheel:1* - The hundreds wheel.
* **Intermediate wheels (1 & 2):** Intermediate gears designed to take over the movement after a full rotation of a digit wheel and transfer it to the next one (transferring ones -> tens, tens -> hundreds).
* **Spur Gears 30 teeth (1 & 2):** Gears used in the mechanism to ensure the correct motion ratio between the steps.
* **Levers (1, 2, 3):** The levers used to actuate or limit the movement of the teeth on the wheels.
* **Spring Clips (1, 2, 3):** Flexible clips, essential for providing tactile feedback (a "click") and perfectly aligning the digits with each movement, preventing the wheels from spinning freely.
* **Case:** Protects the internal mechanism and exposes only the active row of digits.
  * *Bottom case* - The base of the assembly, where the shaft and mechanisms are fixed.
  * *Upper case* - The cover, provided with three viewing windows for the digits.

## 5. Resources Used
The main source of inspiration for the project and the logic of the mechanism were adapted from:
* **[Mechanical Counter — Increment by Place Value - Free 3D Print Model - MakerWorld](https://makerworld.com/en/models/1532810-mechanical-counter-increment-by-place-value#profileId-1607630)**

## 6. Printability Notes
The components were designed with printability in mind:
* The wheels have the digits modeled at a depth and tolerance suitable for a standard 0.4mm nozzle.
* The "Spring Clip" parts must be printed using an appropriate layer orientation to offer flexibility and prevent them from snapping when bent.
* The case (Bottom case and Upper case) is split in half to eliminate the need for complex support structures on the inside, allowing for a clean and easy assembly of the two parts at the end.
