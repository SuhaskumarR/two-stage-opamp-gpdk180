# Design Flow — Two-Stage CMOS Operational Amplifier

## 1. Objective

The objective is to construct and study a two-stage CMOS operational amplifier using the GPDK180 180 nm CMOS technology.

The experiment covers schematic design, analog simulation, transistor geometry study, physical layout, verification, parasitic extraction, and post-layout simulation.

## 2. Schematic Design

The two-stage operational amplifier is constructed using PMOS and NMOS devices from the GPDK180 library.

The specified device geometries are:

| Device | Width | Length |
|---|---:|---:|
| PMOS | 15 µm | 180 nm |
| PMOS | 50 µm | 180 nm |
| NMOS | 3 µm | 180 nm |
| NMOS | 4.5 µm | 180 nm |
| NMOS | 7 µm | 180 nm |

## 3. Simulation Testbench

The operational amplifier test schematic uses DC supplies, sinusoidal input, and bias current sources.

### Supply and Input Conditions

- VDD = +2.5 V
- VSS = -2.5 V
- AC magnitude = 1 V
- Input amplitude = 5 µV
- Input frequency = 1 kHz
- Bias current = 30 µA

## 4. Pre-Layout Analysis

The design is analyzed using Cadence Spectre.

The specified analyses are:

- Transient response
- DC response
- AC response
- AC magnitude and phase response

The main parameters studied are:

- Unity-Gain Bandwidth (UGB)
- 3-dB bandwidth
- Gain margin
- Phase margin
- Gain
- Power requirement

## 5. Transistor Geometry Study

Stage-wise transistor geometries are varied to study their effect on:

- UGB
- 3-dB bandwidth
- Gain
- Power requirement

The observations are used to select appropriate transistor geometries for the physical layout.

## 6. Functional Configurations

The operational amplifier is studied in:

- Inverting configuration
- Non-inverting configuration

The functionality of both configurations is verified through simulation.

## 7. Physical Layout

After selecting suitable transistor geometries, the two-stage operational amplifier layout is created in Cadence Virtuoso.

Appropriate layout techniques are used to implement the physical design.

## 8. DRC and LVS

The completed layout is subjected to physical verification.

The experiment specifies:

- DRC verification
- LVS verification

These checks verify the physical layout against the required design rules and the intended schematic.

## 9. Parasitic Extraction

After layout verification, parasitic elements are extracted from the physical layout.

The extracted design is then used for post-layout simulation.

## 10. Post-Layout Analysis

Post-layout simulations are performed using the extracted design.

The analyses include:

- Transient response
- DC response
- AC response
- AC magnitude and phase response

## 11. Pre-Layout vs Post-Layout Comparison

The experiment requires comparison between schematic-level and layout-level results.

The comparison focuses on:

- Gain
- UGB
- Bandwidth
- Frequency response
- Phase response

Numerical values are not included because the original Cadence simulation result files are unavailable.

## 12. Overall Flow

```text
GPDK180 Devices
      ↓
Two-Stage Op-Amp Schematic
      ↓
Testbench Setup
      ↓
Spectre Pre-Layout Simulation
      ↓
Transistor Geometry Study
      ↓
Select Suitable Geometry
      ↓
Physical Layout
      ↓
DRC / LVS
      ↓
Parasitic Extraction
      ↓
Spectre Post-Layout Simulation
      ↓
Pre-Layout vs Post-Layout Comparison
