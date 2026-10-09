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

*Figure 1. SPICE schematic and simulation of the filter circuit.*

**Design and analysis**

* **Objective:** Attenuate noise from the power source and environment while amplifying select player frequencies
* **Design approach:** Voltage divider paired with two active bandpass filters with an additional lowpass filter
* **Simulation:** Using a number of noise sources, we analyzed the signal to noise strength and found the peak-to-peak voltage of the signal was 0.4 V higher than the peak-to-peak voltage of the noise.
* **Key takeaway:** A reciever must account for source and environment noise while still amplifying the signal of interest.

### Physical Circuit Implementation

<!-- IMAGE PLACEHOLDER 2: Replace the filename below with your breadboard photo. -->

![Breadboard implementation of filter circuit](/images/ecen-340/filter-breadboard.jpg)

*Figure 2. Physical breadboard implementation of the filter circuit.*

**Hardware testing**

* **Implementation:** We used two breadboards and a MCP6002 op amp
* **Equipment:** Oscilloscope and function generator
* **Debugging:** We weren't seeing any signal come through. Our photodiode wasn't configrued properly.

## Tools and Technical Skills

* **Circuit simulation:** SPICE for modeling circuit behavior and evaluating designs.
* **PCB design:** KiCad for schematic capture and printed circuit board design.
* **Laboratory instrumentation:** Oscilloscope and function generator for applying signals, observing waveforms, and evaluating circuit performance.
* **Circuit prototyping:** Breadboarding, component selection, measurement, and debugging.

## Design Journey

This project has helped me connect circuit theory and simulation with physical implementation and laboratory measurement. One important part of the process is understanding why measured circuit behavior may differ from simulated predictions.

**What I learned:** [Describe a specific technical concept or debugging lesson.]

**What I would improve next:** [Identify a design change, additional measurement, or more rigorous analysis you would perform.]
