# Fan-Regulator


# Fan Regulator PCB Using KiCad

## 📌 Project Overview

This project involves designing a **Fan Regulator Circuit PCB** using KiCad. The circuit controls the speed of an AC fan by varying the power delivered to the fan using a TRIAC-based phase-control technique.

The design uses a DIAC, a TRIAC, a potentiometer, resistors, and capacitors to control the TRIAC triggering point during each AC cycle. By adjusting the potentiometer, the fan speed can be changed.

This project helps in understanding power electronics, AC phase control, schematic design, footprint assignment, and PCB layout.

## 🎯 Objectives

* Design an AC fan regulator circuit.
* Understand DIAC and TRIAC operation.
* Control fan speed using phase-angle control.
* Learn potentiometer-based adjustment.
* Create the schematic using KiCad.
* Assign footprints to electronic components.
* Design and route the PCB.
* Perform Electrical Rules Check (ERC) and Design Rules Check (DRC).
* View the completed PCB using KiCad's 3D Viewer.

## ⚙️ Working Principle

The fan regulator operates using the **TRIAC phase-control method**.

1. The AC supply voltage is applied to the regulator circuit.
2. A resistor-capacitor timing network charges during each AC half-cycle.
3. The potentiometer adjusts the charging time of the capacitor.
4. When the capacitor voltage reaches the DIAC's breakover voltage, the DIAC conducts.
5. The DIAC delivers a triggering pulse to the TRIAC gate.
6. The TRIAC conducts for the remainder of that AC half-cycle, supplying power to the fan.
7. Adjusting the potentiometer changes the TRIAC firing angle and therefore changes the power delivered to the fan.

**Note:** The exact speed-control range depends on the circuit design and the type of fan. Some modern electronic fans are not compatible with TRIAC phase control.

## 🧩 Components Used

| Reference | Component            | Function                         |
| --------- | -------------------- | -------------------------------- |
| D1        | DIAC (e.g., DB3)     | Triggers the TRIAC               |
| Q1        | TRIAC (e.g., BT136)  | Controls AC power                |
| RV1       | Potentiometer        | Adjusts the triggering point     |
| R1, R2    | Resistors            | Limit current and control timing |
| C1        | Capacitor            | Timing network                   |
| J1        | AC input connector   | Connects the AC supply           |
| J2        | Fan output connector | Connects the fan                 |

*The component values and ratings must match the actual schematic and the intended fan load.*

## 🔌 Block Diagram

```text
       AC Supply
           |
           v
     Timing Network
    (R + C + RV1)
           |
           v
          DIAC
           |
           v
      TRIAC Gate
           |
           v
   AC Fan Power Control
           |
           v
       AC Fan
```

## 🖥️ PCB Design Using KiCad

The PCB design process includes:

1. Creating the circuit schematic.
2. Adding the DIAC, TRIAC, potentiometer, resistors, and capacitor.
3. Connecting the components according to the circuit diagram.
4. Assigning suitable footprints based on the physical components.
5. Updating the PCB from the schematic.
6. Arranging the components on the PCB.
7. Routing the copper tracks.
8. Running ERC in the schematic editor.
9. Running DRC in the PCB editor.
10. Inspecting the final PCB using the 3D Viewer.



## 🔍 PCB Design Considerations

* Select footprints that match the actual DIAC, TRIAC, and potentiometer.
* Verify the TRIAC pinout using its datasheet.
* Choose resistors and capacitors with suitable voltage and power ratings.
* Use a capacitor specifically rated for its intended AC circuit position.
* Ensure adequate PCB creepage and clearance for mains voltage.
* Use suitable track widths and connectors for the fan current.
* Keep low-voltage control or accessible parts appropriately isolated from hazardous mains circuits where required.

## ✅ Advantages

* Provides adjustable fan speed.
* Uses a relatively simple electronic control circuit.
* Demonstrates practical DIAC and TRIAC applications.
* Helps develop PCB design and power-electronics skills.
* Can be adapted to compatible AC loads with a properly rated design.

## ⚠️ Safety Precautions

**This circuit may operate directly from hazardous AC mains voltage.** Its components and PCB tracks must be treated as live unless suitable isolation is provided.

* Do not touch the PCB while it is powered.
* Disconnect the supply before making adjustments or measurements.
* Do not connect a grounded oscilloscope directly to a live mains circuit.
* Use appropriate fusing, insulation, enclosure, creepage, and clearance.
* Have the design reviewed by a qualified person before connecting it to mains voltage.
* Confirm that the regulator is suitable for the specific fan type and current rating.

For initial learning, study the circuit using simulation or an appropriately isolated, low-voltage setup.

## 🚀 Future Improvements

* Add an insulated rotary control knob.
* Improve PCB layout and thermal management.
* Add appropriate input protection.
* Optimize the timing network for a compatible fan.
* Add a properly designed enclosure.
* Simulate the circuit before manufacturing the PCB.

## 📚 Learning Outcomes

Through this project, I learned:

* DIAC and TRIAC working principles.
* AC phase-angle control.
* Potentiometer-based adjustment.
* Timing networks using resistors and capacitors.
* Schematic design in KiCad.
* Footprint assignment.
* PCB component placement and routing.
* ERC and DRC verification.
* PCB design considerations for power electronics.

## 🛠️ Software Used

* **KiCad 9.0**

## 📄 License

This project is intended for educational purposes. The circuit should be reviewed and validated for electrical safety before practical use.
