# Two-Stage CMOS Operational Amplifier — GPDK180

## Overview

This project documents the design and characterization of a two-stage CMOS operational amplifier using Cadence Virtuoso and the GPDK180 180 nm CMOS technology.

The work covers schematic-level design, Spectre-based analog simulation, physical layout, DRC/LVS verification, parasitic extraction, and post-layout analysis.

## Technology and Tools

- Technology: GPDK180, 180 nm CMOS
- Design Tool: Cadence Virtuoso
- Analog Simulator: Spectre
- Verification: Assura DRC/LVS
- Design Type: Analog IC Design / Physical Design

## Design Objectives

The two-stage operational amplifier was studied for:

- Unity-Gain Bandwidth (UGB)
- 3-dB bandwidth
- Gain margin
- Phase margin
- Operation with and without coupling capacitance
- Inverting configuration
- Non-inverting configuration
- Effect of stage-wise transistor geometry on UGB, bandwidth, gain, and power
- Physical layout
- DRC/LVS verification
- Parasitic extraction
- Post-layout simulation
- Pre-layout and post-layout comparison

## Design Flow

Schematic Design
→ Pre-Layout Simulation
→ Transistor Geometry Study
→ Physical Layout
→ DRC/LVS Verification
→ Parasitic Extraction
→ Post-Layout Simulation
→ Pre-Layout vs Post-Layout Comparison

## Transistor Dimensions

| Device | Width (W) | Length (L) |
|---|---:|---:|
| PMOS | 15 µm | 180 nm |
| PMOS | 50 µm | 180 nm |
| NMOS | 3 µm | 180 nm |
| NMOS | 4.5 µm | 180 nm |
| NMOS | 7 µm | 180 nm |

## Simulation Setup

| Parameter | Value |
|---|---:|
| VDD | +2.5 V |
| VSS | -2.5 V |
| AC Magnitude | 1 V |
| Input Amplitude | 5 µV |
| Input Frequency | 1 kHz |
| Bias Current | 30 µA |
| Transient Stop Time | 5 ms |
| DC Sweep | -5 V to +5 V |
| AC Sweep | 100 Hz to 10 GHz |

## Analyses

The operational amplifier was studied using:

1. Transient analysis
2. DC analysis
3. AC analysis
4. AC magnitude and phase analysis

## Layout and Verification

The two-stage operational amplifier layout was created using the selected transistor geometries.

The design flow includes physical layout, DRC/LVS verification, parasitic extraction, and post-layout Spectre simulation.

## Results

The experiment evaluates Gain, UGB, bandwidth, gain margin, phase margin, and power.

The original Cadence simulation result files are not available, so numerical values are not fabricated in this repository.

| Implementation | Gain | UGB |
|---|---|---|
| Schematic / Pre-layout | Not available | Not available |
| Layout / Post-layout | Not available | Not available |

## Repository Contents

```text
two-stage-opamp-gpdk180/
├── README.md
├── design/
│   └── design_flow.md
└── results/
    └── results.md
