# AM Radio Transmitter & Receiver (DSBWC) 📻

Developed as a faculty project at Helwan University under the supervision of Prof. Ahmed Salah[cite: 1].

## 📝 Overview
This repository contains the design, Proteus simulation, and hardware implementation of a fully functional Amplitude Modulation (AM) Double Sideband with Carrier (DSBWC) broadcasting system[cite: 1]. The system operates on a 100 kHz carrier frequency, modulated by an input audio signal[cite: 1]. 

The transmitted signal follows the fundamental AM equation[cite: 1]:
$s_{DSB-WC}(t)=A_{c}cos(2\pi f_{c}t)[1+k_{a}m(t)]$

This project successfully demonstrates the principles of AM modulation, from signal generation to transmission and reception, validating the performance on a breadboard before finalizing a noise-resistant PCB layout[cite: 1].

## ⚙️ System Architecture

### 1️⃣ Transmitter (TX)[cite: 1]
*   **Audio Input Stage:** Captures an audio signal and amplifies it using LM386 op-amps, providing built-in gain control (20-200x)[cite: 1].
*   **Carrier Generation:** A custom Colpitts oscillator generates a stable 100 kHz carrier[cite: 1]. It utilizes a BC547 transistor and an LC tank circuit ($L \approx 47 \mu H$, $C_{eq} = 50 nF$)[cite: 1].
*   **Modulation:** An LM741 acts as a summing amplifier, combining the signals before a diode-based modulator performs the amplitude modulation[cite: 1].
*   **Transmission Chain:** An LM741 bandpass filter removes unwanted harmonics, and a 2N2222 transistor acts as the final power amplifier to drive the antenna[cite: 1].

### 2️⃣ Receiver (RX)[cite: 1]
*   **RF Amplifier:** A tuned LM741 amplifier selects the 100 kHz AM signal and rejects out-of-band interference[cite: 1].
*   **Demodulation:** A standard envelope detector (diode + RC network) extracts the audio envelope[cite: 1].
*   **Audio Output:** An LM741 low-pass filter removes residual RF components, and an LM386 audio amplifier boosts the signal for clear speaker playback[cite: 1].

### 3️⃣ Antenna
*   The system utilizes a compact helical antenna, optimized for omnidirectional, short-range testing in the medium-wave band[cite: 1].

## 🔮 Future Improvements[cite: 1]
*   Integration of Automatic Gain Control (AGC) to stabilize varying signal strengths[cite: 1].
*   Adding improved frequency selectivity in the receiver stage[cite: 1].
*   Enhancing the power efficiency of the transmitter's final amplifier[cite: 1].
*   Exploring stereo or digital modulation techniques[cite: 1].

## 🤝 Project Team[cite: 1]
*   **Aly Hamdy** (Section 4)
*   **Diaa Salah El-Din** (Section 3) 
*   **Abdelrahman Mohammed** (Section 3) 
*   **Mohamed Mahmoud Atef** (Section 5) 
*   **Mohamed Mahmoud Elaaser** (Section 5)
*   **Amr Waheed** (Section 4)
*   **Ahmed Raed** (Section 1) 
*   **Mohamed Ebrahim** (Section 5) 

---
*For a complete mathematical breakdown and detailed component values, please refer to the full [Project Report](docs/Project_Report.pdf) located in the `docs/` folder.*
