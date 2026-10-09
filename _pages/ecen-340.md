---
layout: single
title: "ECEN 340"
permalink: /ecen-340/
author_profile: true
---

# ECEN 340: Circuit Design and Laboratory Work

This page documents selected circuit design and laboratory projects completed in ECEN 340 at Brigham Young University. My work includes circuit simulation, PCB design, hardware prototyping, and laboratory testing.

## Laser-tag Reciever

### Overview

For this project, I designed and simulated a filter circuit using SPICE, then worked with physical circuit implementation and testing. The project involves analyzing circuit behavior, evaluating design choices, and comparing theoretical expectations with practical results.

### SPICE Simulation

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

![Breadboard implementation of filter circuit](/images/ecen-340/filter-breadboard.jpg)

*Figure 2. Physical breadboard implementation of the filter circuit.*

**Hardware testing**

* **Implementation:** We used two breadboards and a MCP6002 op amp
* **Equipment:** Oscilloscope and function generator
* **Debugging:** We didn't see any signal come through until we repositioned our photodiode current-to-voltage component.

## Tools and Technical Skills

* **Circuit simulation:** SPICE for modeling circuit behavior and evaluating designs.
* **PCB design:** KiCad for schematic capture and printed circuit board design.
* **Laboratory instrumentation:** Oscilloscope and function generator for applying signals, observing waveforms, and evaluating circuit performance.
* **Circuit prototyping:** Breadboarding, component selection, measurement, and debugging.

## Design Journey

This project has helped me connect circuit theory and simulation with physical implementation and laboratory measurement. One important part of the process is understanding why measured circuit behavior may differ from simulated predictions. This took a lot of debugging.

**What I learned:** I learned that eacho component must be measured and tested before integrating it into the rest of the circuit. This is an iterative process.

**What I would improve next:** We need to simplify our breadboard construction of the reciever. We also need to add our transmitter next. We will test the transmitter with the lab equipment and oscilloscope.
