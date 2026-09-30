# Two-Stage CMOS Operational Amplifier — GPDK180

## Overview

This project documents the design and analysis flow of a **two-stage CMOS operational amplifier** using **Cadence Virtuoso** and the **GPDK180 180 nm CMOS technology**.

The project covers:

- Two-stage CMOS op-amp schematic design
- Transistor sizing and geometry selection
- DC analysis
- AC analysis
- Transient analysis
- Gain and bandwidth analysis
- Unity-gain bandwidth (UGB)
- 3-dB bandwidth
- Gain margin
- Phase margin
- Inverting and non-inverting configurations
- CMOS layout
- DRC verification
- LVS verification
- Parasitic extraction
- Post-layout simulation
- Pre-layout vs post-layout comparison

---

## Technology and Tools

| Item | Details |
|---|---|
| Technology | GPDK180 |
| Technology Node | 180 nm |
| Design Tool | Cadence Virtuoso |
| Simulator | Spectre |
| Verification | DRC / LVS |
| Layout | Cadence Virtuoso Layout |
| Analysis | DC, AC and Transient |

---

## Design Objectives

The main objectives of the experiment are:

1. Construct the schematic of a two-stage CMOS operational amplifier.
2. Measure the unity-gain bandwidth (UGB).
3. Determine the 3-dB bandwidth.
4. Measure gain margin and phase margin.
5. Study the effect of coupling capacitance.
6. Evaluate the op-amp in inverting and non-inverting configurations.
7. Study the effect of transistor geometry on amplifier performance.
8. Design the physical layout.
9. Perform DRC and LVS verification.
10. Extract parasitic components.
11. Perform post-layout simulation.
12. Compare pre-layout and post-layout performance.

---

## Transistor Dimensions

The GPDK180 device dimensions used as specified in the laboratory experiment include:

| Device | Width (W) | Length (L) |
|---|---:|---:|
| PMOS | 15 µm | 180 nm |
| PMOS | 50 µm | 180 nm |
| NMOS | 3 µm | 180 nm |
| NMOS | 4.5 µm | 180 nm |
| NMOS | 7 µm | 180 nm |

These device dimensions are used as the basis for transistor geometry studies in the two-stage operational amplifier experiment.

---

## Simulation Setup

The laboratory setup specifies the following representative simulation conditions:

| Parameter | Value |
|---|---:|
| Positive Supply (VDD) | +2.5 V |
| Negative Supply (VSS) | −2.5 V |
| Input AC Magnitude | 1 V |
| Input DC | 0 V |
| Input Offset | 0 V |
| Input Amplitude | 5 µV |
| Input Frequency | 1 kHz |
| Bias Current | 30 µA |
| Transient Stop Time | 5 ms |
| DC Sweep | −5 V to +5 V |
| AC Sweep | 100 Hz to 10 GHz |

---

## Analyses Performed

### DC Analysis

DC sweep analysis is used to study the DC transfer characteristics of the operational amplifier.

### AC Analysis

AC analysis is used to obtain:

- Voltage gain
- Frequency response
- Unity-gain bandwidth
- 3-dB bandwidth
- Gain margin
- Phase margin
- Magnitude response
- Phase response

### Transient Analysis

Transient simulation is used to observe the time-domain response of the operational amplifier.

---

# Representative Results

The following values are **representative/illustrative values** selected to resemble typical simulation results for a two-stage CMOS operational amplifier.

> **Important:** These are not claimed as measured Cadence Virtuoso results. They are included for project documentation and presentation purposes. Actual Cadence simulation results should replace these values when available.

| Parameter | Pre-Layout | Post-Layout |
|---|---:|---:|
| DC Gain | 68.4 dB | 65.9 dB |
| Unity-Gain Bandwidth (UGB) | 9.8 MHz | 8.7 MHz |
| 3-dB Bandwidth | 14.6 kHz | 13.2 kHz |
| Phase Margin | 61.5° | 56.8° |
| Gain Margin | 12.7 dB | 11.1 dB |
| Supply Voltage | ±2.5 V | ±2.5 V |
| Bias Current | 30 µA | 30 µA |

### Pre-Layout vs Post-Layout

The representative results show a moderate reduction in performance after layout.

| Parameter | Pre-Layout | Post-Layout | Change |
|---|---:|---:|---:|
| DC Gain | 68.4 dB | 65.9 dB | ↓ 2.5 dB |
| UGB | 9.8 MHz | 8.7 MHz | ↓ 1.1 MHz |
| 3-dB Bandwidth | 14.6 kHz | 13.2 kHz | ↓ 1.4 kHz |
| Phase Margin | 61.5° | 56.8° | ↓ 4.7° |
| Gain Margin | 12.7 dB | 11.1 dB | ↓ 1.6 dB |

The post-layout degradation is representative of the effect of parasitic resistance and capacitance introduced by the physical layout.

---

## Layout and Verification

The physical design flow consists of:

```text
Schematic
    ↓
Pre-Layout Simulation
    ↓
Layout
    ↓
DRC Verification
    ↓
LVS Verification
    ↓
Parasitic Extraction
    ↓
Post-Layout Simulation
    ↓
Performance Comparison
