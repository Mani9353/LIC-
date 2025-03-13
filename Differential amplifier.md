# EXPERIMENT 3 - DIIFRENTIAL AMPLIFIER 
AIM: To analyze and design the DC,AC,Transient analysis of Common Source NMOS Amplifier
# Introduction:
A MOSFET differential pair amplifier amplifies the difference between two input signals using MOSFETs. It consists of two MOSFETs with their sources tied together and biased by a current source. The inputs are applied to the gates of the MOSFETs. The circuit amplifies the voltage difference between the inputs, with the output taken from the drains of the MOSFETs. Common-mode signals (same voltage on both inputs) are rejected, while differential signals (difference between inputs) are amplified. It offers high input impedance and low noise.
![mosfet](https://github.com/user-attachments/assets/753cb195-dc60-4b6e-8ae8-48e3b5e5cdd9)
## Design Question:
Design and analyse the differential amplifier for the following specifications.
Vdd=2.2V, P<=2.2mW, VinCM=1.2 V, VoCM=1.25V, Vp=0.4V
Perform DC analysis,transient analysis, frequency analysis and extract the parameters.
- Finding Vgs:
  - VinCM = Vp + Vgs1
  - 1.2 = 0.4 + Vgs1
  - Vgs1 = 0.8V

- Determine I<sub>ss 
  - Iss=Power/Vdd
  - Iss = 2.2mW/2.2V
  - Iss = 1mA
    
- Id1 = Id2 = Iss/2 = 0.5mA

- **Finding R<sub>ss :**
  - Rss = Vp/Iss
  - Rss = 0.4V/1mA
  - Rss = 0.4k ohm

 
- Vo1 = Vdd - Id*Rd
  - 1.25V = 2.2 - (0.5m) Rd
  - Rd = 1.9 k ohm


