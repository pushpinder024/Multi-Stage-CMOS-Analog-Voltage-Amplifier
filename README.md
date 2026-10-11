# Multi-Stage-CMOS-Analog-Voltage-Amplifier
**📌 Project Overview**
This repository contains the design, theoretical calculations, SPICE simulation schematics, AC/DC sweep waveforms, and final report for a multi-stage CMOS analog voltage amplifier. The circuit was designed using GlobalFoundries 180nm CMOS technology and operated under a 3.3 V DC power supply to meet strict gain, power dissipation, and load requirements.   

**🛠️ Circuit Architecture & Design Stages**
To achieve a high voltage gain of over 60dB while driving a 10k ohm load, a four-stage cascade architecture was implemented, with stages isolated by 10 micro F coupling capacitors:
1. Current Mirror Reference Stage: Utilizes a diode-connected PMOS transistor in series with a 27.1k ohm resistor to establish a stable reference branch current of 80 micro A, mirroring bias currents across the amplifier stages.
2. Common Source Amplifier Stage 1: Consists of PMOS current-mirror load and NMOS driver  biased via a resistive voltage divider 330k ohm and 150 k ohm to deliver an AC voltage gain of approximately 34.71 dB.
3. Common Source Amplifier Stage 2: Employs PMOS and NMOS transistors with a high-value voltage divider 3.3M ohm and 1.5M ohm to further boost the signal gain by 32.62 dB without degrading stage-one performance.
4. NMOS Source Follower Buffer Stage: Features transistors and  configured to prevent voltage drop under load, accounting for body-effect shifts to secure an overall loaded gain of 66.75dB and low load sensitivity.

**🚀 Key Performance Metrics & Results**
1. Voltage Gain: Achieved a total loaded AC gain of 66.75dB driving a 10k ohm load with a 10pF load capacitance.
2. Output Signal Swing: Delivered a clean transient output swing ranging from 0.48V to 2.2V (1.72V peak-to-peak), exceeding the 1.5V peak-to-peak project specification.
3. Power Dissipation: Optimized total DC power dissipation to 1.09mW, balancing the strict power constraint with high-gain transconductance tradeoffs. 
