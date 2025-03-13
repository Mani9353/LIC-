# EXPERIMENT 3 - DIIFRENTIAL AMPLIFIER 
AIM: Design and analyse the differential amplifier for the following specifications.
Vdd=2.2V, P<=2.2mW, VinCM=1.2 V, VoCM=1.25V, Vp=0.4V
Perform DC analysis,transient analysis, frequency analysis and extract the parameters.
# Theory:
A MOSFET differential pair amplifier amplifies the difference between two input signals using MOSFETs. It consists of two MOSFETs with their sources tied together and biased by a current source. The inputs are applied to the gates of the MOSFETs. The circuit amplifies the voltage difference between the inputs, with the output taken from the drains of the MOSFETs. Common-mode signals (same voltage on both inputs) are rejected, while differential signals (difference between inputs) are amplified. It offers high input impedance and low noise.
![mosfet](https://github.com/user-attachments/assets/753cb195-dc60-4b6e-8ae8-48e3b5e5cdd9)
## Cicuit diagram 
![Screenshot 2025-03-13 214137](https://github.com/user-attachments/assets/c020269a-2013-439f-b440-e8a0bb804914)
## Procedure 

Step 1: Open LTspice and create a new schematic.

Step 2: Place the following components:

MOSFETs (CMOSN, 180nm technology)
Resistors (R1, R2, R3)
Voltage sources (VDD, differential AC inputs)
Ground connection
Step 3: Set component values and import the MOSFET model.

Step 4: Configure simulation commands:
DC Analysis (.op)
AC Analysis (.ac dec 20 0.1 1T)
Transient Analysis (.tran 5m)

Step 5: Run the simulation and observe results.
Calculate for operating point (Qpoint),Gain,Input and output swing,DC sweep
 
Step 6: Analyze DC biasing, gain vs frequency, and transient response.

## Calculations 
- Finding Vgs:
  - VinCM = Vp + Vgs1
  - 1.2 = 0.4 + Vgs1
  - Vgs1 = 0.8V

- Determine I<sub>ss 
  - Iss=Power/Vdd
  - Iss = 2.2mW/2.2V
  - Iss = 1mA
    
- Id1 = Id2 = Iss/2 = 0.5mA

- Finding R<sub>ss :
  - Rss = Vp/Iss
  - Rss = 0.4V/1mA
  - Rss = 0.4k ohm

- Determine Rd:
  - Vo1 = Vdd - Id*Rd
  - 1.25V = 2.2 - (0.5m) Rd
  - Rd = 1.9 k ohm
# DC ANALYSIS:
![Screenshot 2025-03-13 225725](https://github.com/user-attachments/assets/01a4ee8a-bb46-46c9-ac11-a0463400349a)
MOSFET dimensions: w=6.412545ul=180nm




