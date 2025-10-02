# Class-D-Amplifier-PCB
High-efficiency Class-D audio amplifier PCB designed in KiCad using PWM control and LC filtering for clean amplified output.
# Class-D Amplifier PCB Design 🎛️

## 📘 Project Overview
This repository contains the **KiCad schematic and PCB design** for a **Class-D Audio Amplifier**, built using simple and easily available components.  
The goal is to design a **high-efficiency amplifier** that uses **pulse-width modulation (PWM)** to amplify an audio signal while minimizing power loss.

---

## ⚙️ Working Principle
A **Class-D amplifier** works by converting the input analog audio signal into a high-frequency **PWM signal**.  
Instead of linearly amplifying the input like Class A or AB amplifiers, it uses **switching elements (MOSFETs)** that operate in ON/OFF states, drastically improving efficiency.

Here’s the functional breakdown of how this circuit works:

1. 🎵 **Audio Input Stage**  
   - The input analog signal is given to a **comparator (LM311)**.  
   - The comparator compares the audio signal with a **high-frequency triangular waveform** to generate a **PWM signal**.  
   - The width of each pulse corresponds to the amplitude of the input signal.

2. ⚡ **Driver Stage**  
   - The PWM signal is fed to the **IR2153 driver IC**, which is used to drive the **MOSFETs** efficiently.  
   - It provides **high-side and low-side gate control**, ensuring proper switching timing.

3. 🔁 **Switching Stage**  
   - **IRFP4668PBF MOSFETs** are used as the main switching devices.  
   - They switch ON and OFF at high frequency according to the PWM signal, creating a high-power modulated waveform.

4. 🔊 **Output Filter Stage (LC Filter)**  
   - The high-frequency PWM output passes through a **low-pass LC filter (35µH inductor + capacitor)**.  
   - This filter removes the switching frequency, reconstructing the original amplified analog signal.  
   - The output is a **clean, amplified audio signal** suitable for driving a speaker.

5. 🔋 **Power Supply and Protection**  
   - **Zener diodes (1N47xxA series)** provide voltage regulation and protect sensitive ICs.  
   - **Decoupling capacitors (0.1µF)** reduce switching noise and improve stability.

---

## 🧠 Design Highlights
- ✅ **High Efficiency:** Uses switching operation for minimal heat dissipation.  
- ✅ **Compact Layout:** Two-layer PCB with optimized routing and short return paths.  
- ✅ **Noise Control:** Proper placement of decoupling capacitors and ground planes.  
- ✅ **Easy Assembly:** Clearly labeled components and silkscreen markings.  

---

## 🛠️ Design Environment
- **Software:** KiCad v9.0  
- **Layers:** 2 (Top & Bottom)  
- **DRC Check:** Passed successfully ✅  
- **3D View:** Verified component placement and clearances  

