# -AM-Radio-Receiver-540-1600-kHz-
### LC Resonance Design, Implementation, and Experimental Validation

---

## Overview

This project consists of the design and construction of a functional AM radio receiver capable of tuning signals in the standard broadcast band (540–1600 kHz).

The system integrates key concepts from electromagnetics and circuit design, including:
- electromagnetic wave reception  
- LC resonance filtering  
- amplitude demodulation  
- analog signal amplification  

The goal was to design a system that can selectively receive a radio station, extract the audio signal, and output it through headphones.

---

## ⚙️ System Architecture

The radio is composed of four main subsystems:

1. Antenna (Inductive Loop)  
   - Captures electromagnetic waves  
   - Converts magnetic flux variations into an induced voltage  

2. LC Band-Pass Filter  
   - Selects the desired frequency  
   - Rejects unwanted signals  

3. Diode Demodulator  
   - Extracts the audio signal from the AM waveform  

4. Amplifier (LM386)  
   - Drives low-impedance headphones  

---

## Design Calculations

### Resonance Formula

f₀ = 1 / (2π√(LC))

---

### Capacitor Configuration

- Variable capacitors: 2 × TRC-210  
- Minimum capacitance: 14 pF  
- Maximum capacitance: 200 pF  
- Equivalent maximum capacitance: C_max ≈ 210 pF  

---

### Target Frequency Range

- f_min = 540 kHz  
- f_max ≈ 1600 kHz  

---

### Inductance Design

- L ≈ 413 µH  

---

### Coil Geometry

- Wire: 26 AWG  
- Wire radius: 2.0245 × 10⁻⁴ m  
- Coil side length: 0.265 m  
- Number of turns: 18 turns  

---

### Inductance Formula Used

L = (2μ₀ b N² / π) × [ ln(b/a) − 0.774 ]

---

## Implementation

The antenna was constructed as a square loop coil with 18 turns of enameled copper wire.

The LC circuit was formed by:
- the antenna inductance  
- variable capacitors for tuning  

A germanium diode (1N34A) was used for demodulation due to its low forward voltage.

An LM386 amplifier was implemented on a breadboard to drive standard headphones.

---

## Results

- Successfully received AM radio stations within the target band  
- Tuning achieved via variable capacitors  
- Audio output clearly audible through headphones  

---

## Real vs Theoretical Behavior

Although the theoretical design predicts a frequency range of 540–1600 kHz, the real system exhibits deviations due to non-ideal effects.

### Sources of Error:
- Parasitic resistance in the coil  
- Non-ideal capacitor behavior  
- Contact resistance and wiring losses  
- Environmental electromagnetic noise  
- Imperfect coil geometry  

### Impact:
- Reduced selectivity (broader resonance peak)  
- Slight shift in resonance frequency  
- Lower signal amplitude than predicted  

---


## Future Improvements

- Add digital tuning (Arduino + varactor diode)  
- Improve selectivity using a higher Q-factor coil  
- Integrate signal visualization (oscilloscope or ADC)  
- Implement software-defined radio (SDR) features  
- Optimize antenna geometry  

---

## Key Takeaways

This project demonstrates:
- Practical application of electromagnetic theory  
- Design of a frequency-selective system  
- Real-world limitations of ideal circuit models  
- Integration of analog hardware and physics principles  

---

##  Conclusion

A fully functional AM radio receiver was successfully designed and built using fundamental principles of electromagnetics and circuit analysis. The project highlights the transition from theoretical models to real-world engineering systems, where non-ideal effects play a significant role.
