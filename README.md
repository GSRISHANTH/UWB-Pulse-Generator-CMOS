# 📡 Circuit Implementation of a UWB Pulse Generator Using the Dual-Pulse Frequency Notching Approach

![Cadence](https://img.shields.io/badge/Cadence-Virtuoso-red)
![Technology](https://img.shields.io/badge/Technology-45nm%20CMOS-blue)
![Domain](https://img.shields.io/badge/Domain-VLSI-green)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

# Overview

This project presents the CMOS implementation of an **Impulse Radio Ultra-Wideband (IR-UWB) Pulse Generator** using the **Dual-Pulse Frequency Notching (DPFN)** technique. The design aims to reduce electromagnetic interference between Ultra-Wideband communication systems and IEEE 802.11a WLAN networks by introducing frequency notches into the transmitted spectrum.

The complete circuit was designed, simulated, optimized, and analyzed using **Cadence Virtuoso** in **45 nm CMOS technology**.

The project includes:

- CMOS schematic implementation
- Circuit simulation
- Transistor sizing optimization
- Layout design
- Transient analysis
- DC analysis
- Power analysis
- Delay analysis
- Power Delay Product (PDP)
- Process, Voltage and Temperature (PVT) analysis

---

# Problem Statement

Ultra-Wideband (UWB) communication operates over a very large frequency spectrum ranging approximately from **3.1 GHz to 10.6 GHz**.

However, IEEE 802.11a Wireless LAN systems operate around **5.15–5.85 GHz**, creating spectral overlap between both communication systems.

This overlap leads to:

- Electromagnetic interference
- Reduced communication reliability
- Spectrum compatibility issues
- Performance degradation

Traditional frequency-notching methods generally require complicated waveform equations that are difficult to implement in CMOS integrated circuits.

This project addresses the problem using a simpler Dual-Pulse Frequency Notching architecture.

---

# Objective

The primary objective of this project is to design a CMOS-compatible UWB pulse generator capable of suppressing WLAN interference without using complicated waveform generation techniques.

Specific objectives include:

- Design an IR-UWB pulse generator
- Generate frequency notches inside the UWB spectrum
- Implement the complete circuit using Cadence Virtuoso
- Optimize transistor dimensions
- Perform schematic simulation
- Design CMOS layout
- Verify the design through PVT analysis
- Evaluate power consumption and propagation delay

---

# Theory

Impulse Radio Ultra-Wideband communication transmits information using extremely short-duration pulses.

Instead of transmitting a continuous sinusoidal carrier, UWB systems generate narrow pulses that naturally occupy a wide frequency spectrum.

The proposed Dual-Pulse Frequency Notching (DPFN) technique generates:

- One original pulse
- One delayed pulse

Both pulses have identical amplitudes.

A carefully controlled delay is introduced between them.

When both pulses are combined,

- desired frequency components reinforce each other
- unwanted frequencies cancel due to destructive interference

As a result, frequency notches appear in the output spectrum exactly where WLAN systems operate.

This greatly improves coexistence between UWB and WLAN devices.

---

# Working Principle

The overall operation of the system can be summarized as follows:

1. Generate a basic UWB pulse.
2. Duplicate the pulse using identical pulse generators.
3. Delay one pulse using a CMOS delay block.
4. Combine both pulses.
5. Obtain destructive interference at selected frequencies.
6. Produce a UWB output spectrum containing WLAN frequency notches.

---

# System Architecture

```
                Input Trigger
                     │
                     ▼
             Basic Pulse Generator
                  │         │
                  │         ▼
                  │    Delay Block
                  │         │
                  └────┬────┘
                       ▼
                 Pulse Combiner
                       │
                       ▼
                 Output Filter
                       │
                       ▼
                UWB Pulse Output
```

---

# Design Flow

Literature Review

↓

Circuit Design

↓

Cadence Schematic

↓

Simulation

↓

Transistor Sizing

↓

Performance Analysis

↓

Layout Design

↓

PVT Verification

↓

Final Performance Evaluation

---

# Tools Used

| Tool | Purpose |
|-------|----------|
| Cadence Virtuoso | Circuit Design |
| Spectre | Analog Simulation |
| 45 nm CMOS Technology | Process Technology |
| Analog Design Environment | Analysis |
| Layout Editor | Physical Design |

---

# Design Methodology

The project was implemented in multiple phases.

## Phase 1

Research and analysis of the IEEE paper.

---

## Phase 2

Circuit implementation in Cadence Virtuoso.

---

## Phase 3

Transient and DC simulations.

---

## Phase 4

Transistor sizing for improved circuit performance.

---

## Phase 5

Power analysis.

---

## Phase 6

Delay analysis.

---

## Phase 7

Power Delay Product calculation.

---

## Phase 8

Layout generation.

---

## Phase 9

PVT analysis.

---

# Simulation Results

The circuit successfully generated the required UWB pulse.

Simulation studies included

- Transient Analysis
- DC Analysis
- Power Calculation
- Delay Measurement
- PVT Verification

---

# Performance Analysis

| Parameter | Value |
|-----------|---------|
| CMOS Technology | 45 nm |
| Total Power (Before Sizing) | 888.2 nW |
| Total Power (After Sizing) | 1.434 µW |
| Propagation Delay | 23.5 ps |
| Power Delay Product | 33.7 × 10⁻¹⁸ |

---

# Layout Design

After successful schematic verification,

the circuit was converted into a complete CMOS layout.

The layout follows standard CMOS design rules and was verified through physical implementation.

---

# PVT Analysis

To ensure reliability, Process, Voltage and Temperature analysis was performed.

The circuit was evaluated under different operating conditions to verify stable performance.

---

# Advantages

- Simple frequency-notching implementation
- CMOS compatible architecture
- Reduced WLAN interference
- Low propagation delay
- Compact analog design
- Suitable for IR-UWB systems
- Easy to integrate into modern wireless transceivers

---

# Applications

- Ultra-Wideband Communication
- Wireless Sensor Networks
- Short Range Communication
- IoT Devices
- Biomedical Wireless Systems
- RFID Systems
- Embedded Wireless Devices

---

# Future Scope

Possible improvements include:

- Lower power optimization
- Adaptive frequency tuning
- Multi-band frequency notching
- Migration to advanced CMOS nodes
- AI-assisted analog circuit optimization
- Post-layout optimization

---

# Repository Structure

```
UWB-Pulse-Generator-CMOS
│
├── README.md
├── docs
│   └── Project_Report.pdf
│
├── images
│   ├── schematic.png
│   ├── transient.png
│   ├── dc.png
│   ├── layout.png
│   ├── pvt.png
│
└── results
    ├── power.txt
    ├── delay.txt
    └── pvt_results.txt
```

---

# References

1. Ming Shen, Jan H. Mikkelsen, Hao Jiang, Ole K. Jensen and Torben Larsen,

   **Frequency Notching Applicable to CMOS Implementation of WLAN Compatible IR-UWB Pulse Generators**

   IEEE International Conference on Ultra-Wideband (ICUWB), 2012.

---

# Acknowledgements

This project was completed as part of the **VLSI Design Laboratory** coursework at **Amrita School of Engineering, Bengaluru**. It demonstrates the implementation of a published research concept using Cadence Virtuoso and CMOS design techniques.

---

## Author

**G. Srishanth**

B.Tech – Electronics & Communication Engineering

Amrita School of Engineering, Bengaluru

---

⭐ If you found this repository useful, consider giving it a star.
