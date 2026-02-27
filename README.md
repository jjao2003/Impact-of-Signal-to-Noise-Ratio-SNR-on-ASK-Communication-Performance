# Impact of Signal-to-Noise Ratio (SNR) on ASK Communication Performance

## 🎯 Objective
To investigate how varying Signal-to-Noise Ratio (SNR) levels affect the demodulation performance of a digital communication system using Amplitude Shift Keying (ASK).

## 🛠️ System Parameters
- **Sampling Frequency ($f_s$):** 1000 Hz
- **Carrier Frequency ($f_c$):** 50 Hz
- **Modulation Scheme:** Amplitude Shift Keying (ASK)
- **Tested SNR Levels:** 10 dB, 5 dB, 0 dB, -5 dB

## 📊 Methodology
1. **Signal Generation:** A random binary message is generated to simulate digital data.
2. **Modulation:** The message is multiplied by a high-frequency sine wave carrier.
3. **Channel Simulation:** AWGN (Additive White Gaussian Noise) is added at specific power levels.
4. **Demodulation:** An envelope detection method is used to recover the original binary bits.

## 📈 Results and Observations

[Insert your exported MATLAB plot here: ![SNR Results](results/snr_comparison.png)]

| SNR Value | Observation | Performance |
| :--- | :--- | :--- |
| **10 dB** | Minimal noise interference. Signal peaks are distinct. | **Excellent** - No bit errors. |
| **5 dB** | Noticeable distortion in the carrier waveform. | **Good** - High reliability. |
| **0 dB** | Noise power equals signal power. Some "spikes" cross the threshold. | **Fair** - Occasional bit errors occur. |
| **-5 dB** | Noise dominates the signal. The carrier is barely visible. | **Poor** - Signal is heavily corrupted. |

### Conclusion
As the SNR decreases, the probability of bit error increases. For ASK modulation, a low SNR makes it difficult for the receiver to distinguish between a "1" and a "0," especially when noise peaks mimic the amplitude of the carrier.

## 🚀 How to Run
1. Open MATLAB.
2. Navigate to the `src/` folder.
3. Run `snr_analysis.m`.
