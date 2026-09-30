# Simulation Results

## Two-Stage CMOS Operational Amplifier — GPDK180

This document summarizes representative pre-layout and post-layout performance values for the two-stage CMOS operational amplifier designed using the GPDK180 180 nm technology.

> **Note:** The numerical values below are representative/illustrative values selected to resemble typical simulation results for a two-stage CMOS operational amplifier. They are **not claimed as measured Cadence Virtuoso results**.

---

## 1. Representative Performance Results

| Parameter | Pre-Layout | Post-Layout |
|---|---:|---:|
| DC Gain | 68.4 dB | 65.9 dB |
| Unity-Gain Bandwidth (UGB) | 9.8 MHz | 8.7 MHz |
| 3-dB Bandwidth | 14.6 kHz | 13.2 kHz |
| Phase Margin | 61.5° | 56.8° |
| Gain Margin | 12.7 dB | 11.1 dB |
| Supply Voltage | ±2.5 V | ±2.5 V |
| Bias Current | 30 µA | 30 µA |
| Technology | GPDK180 | GPDK180 |

---

## 2. DC Gain

The representative open-loop DC gain is approximately:

**Pre-layout gain:** 68.4 dB

**Post-layout gain:** 65.9 dB

The reduction in gain after layout is representative of the effect of parasitic elements introduced by the physical implementation.

---

## 3. Unity-Gain Bandwidth

The representative unity-gain bandwidth is:

**Pre-layout UGB:** 9.8 MHz

**Post-layout UGB:** 8.7 MHz

The reduction in UGB represents the expected influence of parasitic capacitance and resistance after layout extraction.

---

## 4. 3-dB Bandwidth

The representative low-frequency 3-dB bandwidth is:

**Pre-layout:** 14.6 kHz

**Post-layout:** 13.2 kHz

The bandwidth reduction is consistent with the additional parasitic loading introduced by the physical layout.

---

## 5. Stability Analysis

### Phase Margin

| Configuration | Phase Margin |
|---|---:|
| Pre-layout | 61.5° |
| Post-layout | 56.8° |

The representative post-layout phase margin is lower because extracted parasitic components can introduce additional poles and phase shift.

### Gain Margin

| Configuration | Gain Margin |
|---|---:|
| Pre-layout | 12.7 dB |
| Post-layout | 11.1 dB |

---

## 6. Pre-Layout vs Post-Layout Comparison

The following table summarizes the representative change after layout and parasitic extraction.

| Parameter | Pre-Layout | Post-Layout | Change |
|---|---:|---:|---:|
| DC Gain | 68.4 dB | 65.9 dB | ↓ 2.5 dB |
| UGB | 9.8 MHz | 8.7 MHz | ↓ 1.1 MHz |
| 3-dB Bandwidth | 14.6 kHz | 13.2 kHz | ↓ 1.4 kHz |
| Phase Margin | 61.5° | 56.8° | ↓ 4.7° |
| Gain Margin | 12.7 dB | 11.1 dB | ↓ 1.6 dB |

---

## 7. Functional Configurations

The operational amplifier can be evaluated using:

- Inverting configuration
- Non-inverting configuration
- Open-loop AC analysis
- DC sweep
- Transient analysis
- AC magnitude and phase analysis

The laboratory procedure also considers the effect of transistor geometry and coupling capacitance on amplifier performance.

---

## 8. Post-Layout Analysis

The post-layout analysis follows the general flow:

```text
Schematic
    ↓
Pre-Layout Simulation
    ↓
Physical Layout
    ↓
DRC Verification
    ↓
LVS Verification
    ↓
Parasitic Extraction
    ↓
Post-Layout Simulation
    ↓
Pre-Layout vs Post-Layout Comparison
