# EMG and Strain-Gauge Signal Conditioning

**Sanaz Mazrae**  
Sensing and Measurement · Department of Electrical Engineering, Sharif University of Technology

Design and simulation of a two-channel analog signal-conditioning system for surface electromyography (sEMG) of the triceps and a strain-gauge voltage associated with gripping and lowering a load. The circuits use filtering, buffering, and instrumentation amplification to process low-amplitude differential signals.

## Circuit Design

| | EMG channel | Strain-gauge channel |
|---|---|---|
| Nominal input scale | 100 µV | 1 mV |
| Main filtering | ~20 Hz high-pass, ~200 Hz low-pass, 50 Hz notch | ~35 Hz low-pass, DC blocking |
| Instrumentation-amplifier gain | 164 V/V | 20 V/V |
| Additional amplifier gain | 41 V/V | 11 V/V |
| Nominal combined gain | 6724 V/V | 220 V/V |

The values above describe the Proteus design calculations. The LTspice circuit uses separate component configurations and includes an exploratory ADC and isolation stage.

## Project Files

- [Technical report](Report.pdf) — circuit architecture, design equations, simulation conditions, waveforms, and discussion of the results.
- [`proteus/sensing_project.pdsprj`](proteus/sensing_project.pdsprj) — complete Proteus schematic project.
- [`ltspice/Project.asc`](ltspice/Project.asc) — LTspice analog signal-conditioning and ADC-stage schematic.

## Simulation

Open the `.pdsprj` file in **Proteus** to inspect the analog signal-conditioning design and simulation graphs. Open the `.asc` file in **LTspice** to inspect and run its configured transient analysis; the relevant Analog Devices component models must be available in the installed LTspice library.

The project evaluates simulated sensor-level signals. No physical EMG recordings or calibrated force measurements are included.
