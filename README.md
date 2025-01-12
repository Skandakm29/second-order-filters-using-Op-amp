# second-order-filters-using-Op-amp

# Low-Pass Filter Analysis

## 4.1.1 Key Features of the Phase Response
- The phase starts at approximately **0°** in the low-frequency range (passband).
- As the frequency approaches the cutoff, the phase begins to shift.
- At `f_c = 15.364 Hz`, the phase shift is about **-45°**.
- Beyond the cutoff frequency, the phase asymptotically approaches **-90°** or lower for a second-order filter.

## 4.1.2 Cutoff Frequency Behavior
- The cutoff frequency aligns with the theoretical design.
- The observed **-3 dB point** validates the filter's low-pass characteristic.

## Circuit Syntax (Code or Equations)

### Cutoff Frequency Calculation:
```
f_c = 1 / (2 * pi * sqrt((R1 * C1)(R2 * C2)))
```
**Substituting Values:**
```
f_c = 1 / (2 * pi * sqrt((1200 * 33e-9)(1200 * 33e-9)))
```
```
f_c ≈ 15.364 Hz
```

### Phase Equation (for reference):
At any frequency `f`, the phase is calculated as:
```
φ(f) = -arctan(f / f_c)
```

## Simulation Results
- The magnitude response aligns with the theoretical design.
- Observations:
  - The filter attenuates frequencies higher than the cutoff.
  - The phase response matches the expected behavior for a second-order filter.

## How to Run the Simulation
1. Open the circuit file in a simulation tool such as **LTspice** or **Multisim**.
2. Run the AC frequency sweep analysis with the parameters:
   - **Start Frequency**: `1 Hz`
   - **Stop Frequency**: `1 MHz`
   - **Sweep Type**: **Decade**
3. Observe the output waveform for both **magnitude** and **phase response**.

## Repository Structure
```
.
├── README.md             # Project overview and instructions
├── CircuitDesign.asc     # Circuit file for LTspice
├── Results/
│   ├── MagnitudeResponse.png  # Magnitude response plot
│   ├── PhaseResponse.png      # Phase response plot
└── Documentation/
    ├── LowPassFilter_Analysis.docx  # Detailed documentation
```

## Contributions
Feel free to contribute to this project. Submit an issue or pull request if you find any improvements!
