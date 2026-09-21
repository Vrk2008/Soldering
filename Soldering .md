Laboratory Experiment Report

Title

**Fabrication and Verification of a Hardware-Based Logic AND Gate Circuit**

Objective

To design, solder, and verify the operation of a logic **AND gate** using mechanical switches, a current-limiting resistor, and a Light Emitting Diode (LED) on a printed circuit board (PCB).

**Components and Equipment Required**

* **Power Supply:** 9V DC battery with a battery clip  
* **Switches (SW1, SW2):** Two single-pole single-throw (SPST) toggle or push switches  
* **Output Indicator (D1):** One standard 5mm Light Emitting Diode (LED)  
* **Resistor:** One current-limiting resistor (typically 330 $\\Omega$ to 470 $\\Omega$)  
* **Circuit Board:** General-purpose prototyping PCB (dot matrix board)  
* **Soldering Tools:** Soldering iron (25W–40W), solder wire (60/40 leaded or lead-free alloy), soldering flux, safety glasses, wire cutter, and wire stripper

Circuit Diagram and Description

**The circuit implements a basic series configuration to mimic digital logic:**

* The positive terminal of the **9V battery** connects to the first terminal of switch **SW1**.  
* The second terminal of **SW1** connects in series to the first terminal of switch **SW2**.  
* The second terminal of **SW2** connects directly to the anode (longer lead) of **LED D1**.  
* The cathode (shorter lead) of **LED D1** is placed in series with a **resistor** to limit current and prevent the LED from burning out.  
* The remaining terminal of the resistor connects back to the negative terminal of the **9V battery**, completing the closed-loop system.

Theory and Working Principle

A digital **AND gate** is a basic logic gate whose output is HIGH (1) only when all of its inputs are simultaneously HIGH (1). If any input is LOW (0), the output remains LOW (0).

**In this electrical analog implementation:**

* **Inputs:** The state of the mechanical switches represents the input values. An open switch signifies a logic **0 (OFF)**, while a closed switch signifies a logic **1 (ON)**.  
* **Output:** The physical state of the LED represents the output logic value. An unlit LED represents a logic **0 (OFF)**, and a glowing LED represents a logic **1 (ON)**.

Current flows from the positive terminal to the negative terminal only when there is an uninterrupted path. Because the switches are wired in series, both **SW1** AND **SW2** must be closed to complete the electrical path. If either switch remains open, the circuit breaks, current drops to zero, and the LED remains unlit.

Truth Table Verification

**The system operation was validated against the standard truth table for a 2-input AND logic operation:**

| Switch 1 (Input A) | Switch 2 (Input B) | LED D1 (Output Y) | Circuit State |
| :---- | :---- | :---- | :---- |
| 0 (Open) | 0 (Open) | 0 (OFF) | Incomplete path, no current flow |
| 0 (Open) | 1 (Closed) | 0 (OFF) | Broken path at SW1, no current flow |
| 1 (Closed) | 0 (Open) | 0 (OFF) | Broken path at SW2, no current flow |
| **1 (Closed)** | **1 (Closed)** | **1 (ON)** | **Complete path, current flows, LED illuminates** |

**Soldering and Assembly Procedure**

1. **Component Placement:** Insert the components (SW1, SW2, LED, and resistor) into the general-purpose PCB according to the series layout shown on the circuit schematic. Bend the component leads slightly outward on the backside of the board to hold them mechanically in place.  
2. **Joint Preparation:** Clean the soldering iron tip using a damp sponge or brass wire cleaner, then tin the tip with a small amount of fresh solder to ensure efficient heat transfer.  
3. **Soldering:** Apply the heated iron tip simultaneously to both the component lead and the copper track pad on the PCB. Introduce the solder wire to the joint until it flows evenly, forming a shiny, concave, cone-shaped fillet around the lead. Remove the solder wire first, followed immediately by the iron tip.  
4. **LED Orientation:** Take special care during the soldering of LED D1 to ensure the anode (positive terminal) faces the output of SW2 and the cathode (negative terminal) connects to the resistor.  
5. **Trimming:** Allow the joints to cool naturally without moving the components. Use wire cutters to trim excess component leads just above the apex of the soldered joints.  
6. **Inspection:** Visually inspect all soldered connections under a magnifying glass to check for dry joints, cold solder cracks, or accidental solder bridges between adjacent tracks.

**Precautions**

* **Thermal Damage:** LEDs are heat-sensitive semiconductor components. Do not apply the soldering iron tip to the LED leads for more than 2 to 3 seconds to avoid internal thermal destruction.  
* **Polarity:** Always verify the polarity of the LED before soldering, as reversing it will block current flow completely and prevent the circuit from working.  
* **Safety:** Perform all soldering operations in a well-ventilated laboratory area or under a fume extractor hood to avoid inhaling hazardous rosin or lead fumes. Always wear safety glasses to protect against flying wire clippings.

**Result**

The discrete series hardware circuit was successfully assembled and permanently soldered onto the prototyping PCB. Functional validation testing confirmed that the LED illuminates exclusively when both mechanical switches are toggled into their closed states. The physical experiment perfectly demonstrates the operational parameters and logic state characteristics of a standard digital two-input AND gate.  
<img width="900" height="1600" alt="solder" src="https://github.com/user-attachments/assets/1061aad5-c53f-466b-acae-9e162fdf3ccf" />
<img width="900" height="1600" alt="solderlight" src="https://github.com/user-attachments/assets/f25ef2a5-8d0d-4a6b-90b5-1a57ede04a7d" />

