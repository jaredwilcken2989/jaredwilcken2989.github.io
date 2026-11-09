---
layout: single
title: "ECEN 340"
permalink: /ecen-340/
author_profile: true
---

# ECEN 340: Circuit Design and Laboratory Work

This page documents selected circuit design and laboratory projects completed in ECEN 340 at Brigham Young University. My work includes circuit simulation, PCB design, hardware prototyping, and laboratory testing.

## Laser-tag Reciever/Transmitter

### Overview

For this project, I designed and simulated a filter circuit using SPICE, then worked with physical circuit implementation and testing. The project involves analyzing circuit behavior, evaluating design choices, and comparing theoretical expectations with practical results.

### SPICE Simulation (Reciever Only)

<!-- IMAGE PLACEHOLDER 1: Replace the filename below with your SPICE screenshot. -->

![SPICE simulation of filter circuit](/images/ecen-340/filter-spice.jpg)
![SPICE simulation Graphs](/images/ecen-340/spice-simulation-graphs.jpg)

*Figure 1. SPICE schematic and simulation of the filter circuit.*

**Design and analysis**

* **Objective:** Reduce noise from the power supply and surrounding environment while amplifying frequencies associated with the desired signal.
* **Design approach:** Combined a voltage divider with two active band-pass filters and an additional low-pass filter to shape the circuit's frequency response.
* **Simulation:** Tested the circuit using multiple noise sources and analyzed the resulting signal. The simulated signal had a peak-to-peak voltage 0.4 V greater than that of the noise.
* **Key takeaway:** A reciever must account for source and environment noise while still amplifying the signal of interest.

### Physical Circuit Implementation

<!-- IMAGE PLACEHOLDER 2: Replace the filename below with your breadboard photo. -->

![Breadboard implementation of filter circuit](/images/ecen-340/reciever_transmitter_breadboard.jpg)

*Figure 2. Breadboard Implementation and Hardware Testing for both reciever and transmitter.*

**Design and Testing**

* **Objective:** Build and test the laser tag transmitter and receiver circuits on a breadboard.
* **Implementation:** Built the receiver circuit across two breadboards using MCP6002 operational amplifiers, resistors, capacitors, and a photodiode. The transmitter required surface-mount soldering an LED driver chip onto a breakout board.
* **Receiver testing:** Used an oscilloscope and FFT analysis to test signals at 1250 Hz, 2000 Hz, and 3636 Hz. At a sampling rate of 100 kHz, we measured a signal-to-noise difference of 0.333 V, passing the requirement of at least 100 mV.
* **Transmitter testing:** Measured an LED current magnitude of approximately 77.6 mA at 2000 Hz using oscilloscope data and FFT analysis.
* **Troubleshooting:** We didn’t see any signal come through until we repositioned our photodiode current-to-voltage component. Our transmitter also didn't initially produce enough current. This is because we had a faulty LED component.
* **Key takeaway:** Building the circuit showed me that a working simulation doesn't always translate directly to physical hardware. Component placement, wiring, and troubleshooting are just as important as the circuit design itself.

### KiCad Schematic

<!-- IMAGE PLACEHOLDER 3: Replace the filename below with your kicad schematic. -->

![Kicad Schematic](/images/ecen-340/pcb_schematic.jpg)

*Figure 3. KiCad Schematic Design.*

**Design and Analysis**

* **Objective:** Convert our tested laser tag transmitter and receiver circuits into a complete KiCad schematic for PCB design.
* **Design approach:** Organized the receiver's amplification and filtering stages alongside the LED transmitter circuit, selecting components and assigning appropriate symbols and footprints.
* **Design specifications:** Designed around a 3.3 V power supply, with the receiver intended to detect signals across the 1250–3636 Hz frequency range.
* **Verification:** Checked component connections, pin assignments, and power connections before transferring the schematic into the PCB layout.
* **Key takeaway:** Creating a PCB schematic required more attention to component specifications and physical connections than the original SPICE simulation.

### PCB Design

<!-- IMAGE PLACEHOLDER 4: Replace the filename below with your kicab pcb and 3D rendering. -->

![Kicad PCB Design](/images/ecen-340/pcb.jpg)
![Kicad PCB 3D Rendering](/images/ecen-340/pcb_3d.png)

*Figure 4. KiCad PCB Design and 3D Rendering.*

**PCB Design and Layout**

* **Objective:** Convert our KiCad schematic into a compact PCB layout that fits inside the laser tag housing.
* **Design approach:** Selected component footprints, arranged components on both sides of the board, and routed copper traces to connect the transmitter and receiver circuits.
* **Board specifications:** Designed a 74 × 32 mm PCB containing 33 components and 72 pads, with a minimum trace width of 0.305 mm and minimum clearance of 0.713 mm.
* **Verification:** Used KiCad's 3D viewer to inspect component placement and check the physical layout before preparing the board for fabrication.
* **Key takeaway:** PCB design taught me to consider physical constraints, component footprints, and trace routing alongside electrical functionality.

## Tools and Technical Skills

* **Circuit simulation:** SPICE for modeling circuit behavior and evaluating designs.
* **PCB design:** KiCad for schematic capture and printed circuit board design.
* **Laboratory instrumentation:** Oscilloscope and function generator for applying signals, observing waveforms, and evaluating circuit performance.
* **Circuit prototyping:** Breadboarding, component selection, measurement, and debugging.

## Design Journey

This project has helped me connect circuit theory and simulation with physical implementation and laboratory measurement. One important part of the process is understanding why measured circuit behavior may differ from simulated predictions. This took a lot of debugging.

**What I learned:** I learned that each component must be measured and tested before integrating it into the rest of the circuit. This is an iterative process.

**What I would improve next:** We need to simplify our breadboard construction of the reciever. We also need to add our transmitter next. We will test the transmitter with the lab equipment and oscilloscope.
