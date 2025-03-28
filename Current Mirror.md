# **Current Mirror Experiment**

Aim : Design and Analyze Current mirror circuit as active load in amplifier circuit.
Given Vdd=1.8V, P<=1 mW, Av>-10 V/V.

## Introduction
A current mirror is a circuit designed to copy (mirror) a reference current from one branch of the circuit to another, ensuring that the output current remains constant regardless of voltage variations. This is essential for maintaining stable operation in analog circuits, particularly in integrated circuits (ICs).

## Theory
The basic principle of a current mirror involves using two or more transistors where one transistor is configured to set the reference current, and the other(s) mirror this current. The transistors are typically matched to ensure accurate current replication.


## Advantages of Current Mirrors:
* **Stable Biasing**: Provides consistent and accurate bias currents
* **Improved Performance**: Enhances gain, stability, and bandwidth of amplifiers
* **Power Efficiency**: Reduces power consumption compared to resistor biasing
* **Temperature Compensation**: Ensures reliable operation over a wide temperature range
* **Scalability**: Easily scalable to multiple output branches

## Effect of Current Mirrors:
* **Gain**: Improves amplifier gain
* **Stability**: Reduces variations in bias current
* **Bandwidth**: Enhances frequency response
* **Noise Reduction**: Maintains a low noise floor
* **Load Regulation**: Ensures consistent performance under varying load conditions

Circuit Diagram:

![Screenshot 2025-03-24 020933](https://github.com/user-attachments/assets/1e4f8e49-63a2-4835-a5de-baf66b9a8a22)

CALCULATION:

Drain current equation is given by:

I<sub>D</sub> = (1/2)μnC<sub>ox</sub>(W/L)(VGS - Vth)^2\
I<sub>Total</sub> = P / V<sub>DD</sub>\
I<sub>Total</sub> = I<sub>ref</sub> + I<sub>x</sub>\
For 1:1 ratio I<sub>ref</sub> = I<sub>x</sub>\
I<sub>ref</sub>(2) = I<sub>Total</sub>\
I<sub>ref</sub> = I<sub>Total</sub>/2\
I<sub>Total</sub> = 1 mW/1.8 V\
I<sub>Total</sub> = 0.555 mA\
I<sub>ref</sub> = 0.555 m/2\
Therefore, I<sub>ref</sub> = 0.2778 mA.

# Design question:
Given Vdd=1.8V, P<=1 mW, Av>-10 V/V.

# Case 1 : 1:1 Current mirror circuit L = 180n

# DC Analysis:

![Screenshot 2025-03-24 020933](https://github.com/user-attachments/assets/1e4f8e49-63a2-4835-a5de-baf66b9a8a22)

OUTPUT:

![Screenshot 2025-03-24 021657](https://github.com/user-attachments/assets/667285d0-133c-4002-8501-a907a4d7a991)

OBSEVATIONS:
- w is adjusted to 6.689um to get uniform Id current in the mosfets.
- w/l ratio is maintained same .

# Transient Analysis:

- Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.865 V.
- Select run and choose transient anlaysis. Choose 10 ms for stop time.

  
![Screenshot 2025-03-24 022623](https://github.com/user-attachments/assets/420af5c5-fe68-4dbb-a3c7-4f33287727b5)

OUTPUT:

Heres the obtained result:

![Screenshot 2025-03-24 023024](https://github.com/user-attachments/assets/78f90046-7271-41a9-b5d0-fb0a15e145ab)

# AC Analysis:

- Change the Vin to AC and set AC amplitude to 1.
- Select type of sweep to decade ,set start and stop frequencies to 0.1 and 1T Hz respectively.

OUTPUT:

Heres the obtained result:

![Screenshot 2025-03-24 022623](https://github.com/user-attachments/assets/5ddfd064-8941-4514-a198-3f06ce6d361c)


# Case 2 : 1:1 Current mirror circuit L = 500n

# DC Analysis:

![Screenshot 2025-03-24 020933](https://github.com/user-attachments/assets/1e4f8e49-63a2-4835-a5de-baf66b9a8a22)

OUTPUT:

![Screenshot 2025-03-24 021515](https://github.com/user-attachments/assets/7dea319c-a945-4762-a5b4-60aea2c5155c)


OBSEVATIONS:
- w is adjusted to 18.869um to get uniform Id current in the mosfets.
- w/l ratio is maintained same .

# Transient Analysis:

- Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.865 V.
- Select run and choose transient anlaysis. Choose 10 ms for stop time.

  
![Screenshot 2025-03-24 022623](https://github.com/user-attachments/assets/420af5c5-fe68-4dbb-a3c7-4f33287727b5)

OUTPUT:

Heres the obtained result:

  ![Screenshot 2025-03-24 025124](https://github.com/user-attachments/assets/44e1b4cf-58e7-4848-b16b-c6446a8327ec)

 the expected Av value is 10v/v and obtained value is 12.6
 

# AC Analysis:

- Change the Vin to AC and set AC amplitude to 1.
- Select type of sweep to decade ,set start and stop frequencies to 0.1 and 1T Hz respectively.

OUTPUT:

Heres the obtained result:

![Screenshot 2025-03-24 161710](https://github.com/user-attachments/assets/b18e4da0-b898-40c3-b5d5-9881319f8bb2)

# Case 3 : 1:1 Current mirror circuit L = 1u

# DC Analysis:

![Screenshot 2025-03-24 020933](https://github.com/user-attachments/assets/1e4f8e49-63a2-4835-a5de-baf66b9a8a22)

OUTPUT:

![Screenshot 2025-03-24 021657](https://github.com/user-attachments/assets/2b89c87a-ff50-478c-ac86-8ca1be8d49c4)




OBSEVATIONS:
- w is adjusted to 37.869um to get uniform Id current in the mosfets.
- w/l ratio is maintained same .

# Transient Analysis:

- Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.865 V.
- Select run and choose transient anlaysis. Choose 10 ms for stop time.

  
![Screenshot 2025-03-24 022623](https://github.com/user-attachments/assets/420af5c5-fe68-4dbb-a3c7-4f33287727b5)

OUTPUT:

Heres the obtained result:

 ![Screenshot 2025-03-24 160652](https://github.com/user-attachments/assets/a1d79966-4dda-4f23-ab5e-62cbacffabf0)


 # AC Analysis:

- Change the Vin to AC and set AC amplitude to 1.
- Select type of sweep to decade ,set start and stop frequencies to 0.1 and 1T Hz respectively.

OUTPUT:

Heres the obtained result:

![Screenshot 2025-03-24 160945](https://github.com/user-attachments/assets/6105e630-7c4a-4623-a94a-6b6de25a3cee)


# Results:


| Case             | L (Length) | W (Width)  | W/L Ratio |
|----------------- |------------|----------- |-----------|
| Case 1           | 180 nm     | 6.689  µm  | 1:1       |
| Case 2           | 500 nm     | 18.869 µm  | 1:1       |
| Case 3           | 1 µm       | 37.869 µm  | 1:1       |
| Special case     | 180 nm     | 13.378 µm  | 1:2       |

# INFERENCE:

1) W/L Ratio Consistency:

 - Keeping the W/L ratio consistent for the MOSFETs is crucial to ensure the current mirror operates predictably.

2) Adjusting W and L:

 - As the length (L) of the MOSFETs increases, the width (W) must also increase to maintain the same W/L ratio.

3) Special Case of W/L Ratio 1:2:

 - A W/L ratio of 1:2 helps adjust the current mirror to achieve different mirroring ratios.

4) Total Current Calculation:

- The total current (I_total = 0.55 mA) is determined based on the power supply and constraints.
- The reference current (I_ref) and output current (I_p) are each set to 0.2778 mA.

5) Total Current Calculation:

- The total current (I_total = 0.55 mA) is determined based on the power supply and constraints.
- The reference current (I_ref) and output current (I_p) are each set to 0.27 mA.



# PART B:

Aim : Design the differential amplifier using the same design specification as Experiment-3. Perform DC analysis,trasient and AC analysis.

# DC Analysis:

![Screenshot 2025-03-24 161239](https://github.com/user-attachments/assets/0a93bf82-c8dd-4f5a-8241-5d154cf6b740)



OUTPUT:

![Screenshot 2025-03-24 155041](https://github.com/user-attachments/assets/2713df6a-f1e3-4bb5-bfb5-6da6826c4621)


# Transient Analysis:


- Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.865 V.
- Select run and choose transient anlaysis. Choose 10 ms for stop time.

![Screenshot 2025-03-24 161317](https://github.com/user-attachments/assets/a5b86228-ed2e-4aab-81d8-c746ba31f67d)

OUTPUT:

![Screenshot 2025-03-24 161553](https://github.com/user-attachments/assets/b2ab4ed9-8093-4857-922b-2b48286f7623)

 # AC Analysis:

- Change the Vin to AC and set AC amplitude to 1.
- Select type of sweep to decade ,set start and stop frequencies to 0.1 and 1T Hz respectively.

OUTPUT:

Heres the obtained result:


![Screenshot 2025-03-24 162251](https://github.com/user-attachments/assets/0703e993-49c7-4ea0-b983-b647419c40cd)

# INFERENCE:

# Differential Amplifier Circuit Description

This circuit functions as a differential amplifier using a current mirror, with the output voltage (\(V_{out}\)) determined by the difference between \(V_1\) and \(V_2\). The PMOS current mirror (M5-M6) ensures stable current replication, providing reliable current control. This configuration is effective for signal amplification in analog designs, as the NMOS differential pair (M2-M3) is responsible for the amplification process.

​

