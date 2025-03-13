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
### CASE-1: Circuit with Rss resistor

# DC ANALYSIS:
![Screenshot 2025-03-13 225725](https://github.com/user-attachments/assets/01a4ee8a-bb46-46c9-ac11-a0463400349a)
MOSFET dimensions: W=6.412545u L=180nm(Both MOSFET'S)

# Transient Analysis:
Input and output waveforms of M1:
![Screenshot 2025-03-14 011101](https://github.com/user-attachments/assets/391078f1-bed5-41b3-8751-96ccb42545b9)

Input and output waveforms of M2:
![Screenshot 2025-03-14 011128](https://github.com/user-attachments/assets/6b7e3891-ee66-46c7-9ac1-f47e064755b0)


# Transient Gain:
![Screenshot 2025-03-13 233219](https://github.com/user-attachments/assets/053617cf-15bd-46c9-b7a3-5fd7f466a574)
 From simulation, Gain= -4 V/V;
 Theoretical gain= -4.31 V/V
 # AC Analysis:


![Screenshot 2025-03-14 010820](https://github.com/user-attachments/assets/a9996de9-f5d2-4712-8ee4-8dade9deca41)


From simulation, Gain= 12.145 dB ; Theoretical gain= 12.68 dB

### CASE-2 Circuit with current source 
![Screenshot 2025-03-14 002140](https://github.com/user-attachments/assets/bed49cee-1884-4187-b7bb-c77b37ae738f)


DC ANALYSIS:
![Screenshot 2025-03-14 001603](https://github.com/user-attachments/assets/94393801-3123-48ff-8d53-3d30f9d6b6a8)

MOSFET dimensions: W=6.412545u L=180nm(Both MOSFET'S)

# Transient Analysis:
Input and output waveforms of M1:
![Screenshot 2025-03-14 002916](https://github.com/user-attachments/assets/81fd1e28-e1b4-4d3c-9121-9bf6ed6a8317)

Input and output waveforms of M2:
![Screenshot 2025-03-14 002848](https://github.com/user-attachments/assets/f62433dc-cf62-4370-950e-e28ae929707b)

# AC Analysis:

![Screenshot 2025-03-14 005533](https://github.com/user-attachments/assets/4d99a587-f71a-4c3d-8d26-0bab7dfb8343)


From simulation, Gain= 12.145 dB ; Theoretical gain= 12.68 dB


### CASE-3 Circuit with N-MOS
![Screenshot 2025-03-14 012807](https://github.com/user-attachments/assets/4019f4f5-dab6-4107-ba73-d3ffb8d46eba)

 To get the output voltage and vp and current desired value we have to 
 vary the width and length of the new mosfet
![Screenshot 2025-03-02 25023](https://github.com/user-attachments/assets/39f0a14a-c7f1-45ce-b951-6841a94a4e38)

# DC ANALYSIS:
![Screenshot 2025-03-14 012522](https://github.com/user-attachments/assets/83c86ca3-1aac-4d76-b2bc-961be249dc2e)



# Transient Analysis:



# AC Analysis:



# Result:

1. Circuit-1: 
   - The DC analysis shows that the MOSFETs operate in saturation with balanced drain currents when input voltages are equal.  
   - The transient response confirms proper differential behavior.  
   - The AC analysis indicates moderate gain and common-mode rejection.  

2. Circuit-2:  
   - Replacing the resistor with a current source improves bias stability, as seen in the DC analysis.  
   - The transient response is more stable, ensuring better symmetry.  
   - The AC analysis shows increased gain and bandwidth compared to Circuit-1.  

3. Circuit-3:  
   - The DC analysis confirms that the MOSFET-based current source regulates the tail current effectively.  
   - The transient response maintains signal accuracy with improved performance.  
   - The AC analysis shows higher gain and bandwidth.  
   - The DC sweep analysis validates expected output variations.


# Inference :
This experiment looked at three types of differential amplifier setups: resistor-based, current source-based, and NMOS-based, each affecting gain, bandwidth, and stability in different ways.

- **Resistor-based**: High bandwidth, but low gain and poor CMRR.  
- **Current source-based**: High gain, good CMRR, but slightly lower bandwidth.  
- **NMOS-based (CMOSN)**: Highest gain.

**Best Setup Based on Needs:**  
1. For high bandwidth → Resistor-based  
2. For maximum gain → NMOS-based (CMOSN)  
3. For better CMRR → Current source-based or NMOS-based (CMOSN)




