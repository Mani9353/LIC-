# LIC-
LINEAR Integrated CIRCUIT

# Expeiment-1
Question : Given that POWER, P=100µ W; Perform DC Analysis, Transient Analysis and AC Analysis for the Given Circuit Designs and also check what happens when the width is increased or decreased of each mosfet
# Design-1 :
![Screenshot 2025-02-17 010622](https://github.com/user-attachments/assets/46233abf-9521-43fc-be66-c3df23eec67a)

Aim: TO find DC operating point,find gain using transient analysis and AC analysis.

Components : MOSFET,resistors,DC power supply

Procedure:
  1. Make the circuit connection as show above.

  2. Connect the RD resistor to the drain terminal and DC power supply to the gate terminal as 
     well as to the resistor.

  3. Connect the source terminal to the ground.

  4.Set the input voltage to 0.9 V and VDD to 1.8 V.

Using the formula for power,

P = V*I

We will get the values of Id as,

Id = 5.56*10^-5A

we have to get the output current,Id for the given circuits by adjusting the values of L & W(Lenght and widthh of the channel of the MOSFET)
Length and Width of the channel used to obtain the given current is shown in the figure below;

![Screenshot 2025-02-17 005840](https://github.com/user-attachments/assets/2568fc83-e279-4020-b3f4-33ec4cee553d)

1.DC ANALYSIS :

 Procedure for performing DC analysis : we have to selesct the DC output print (DC op pnt)in the edit simulation command and run the simulation 
 
 ![Screenshot 2025-02-17 005944](https://github.com/user-attachments/assets/aa989a50-c642-49b9-bcc2-e0a51a2d1249)
 
The Figure below shows the Values obtained from the DC Analysis :
![Screenshot 2025-02-17 010010](https://github.com/user-attachments/assets/96047fdd-12f7-4c17-9181-f3157ca4d88c)

 2.TRANSIENT ANALYSIS:

Procedure for Performing Transient Analysis: We have to select the Transient Analysis in the edit simulation command,Give the stop time as 1ms and Run the simulation

![Screenshot 2025-02-17 010729](https://github.com/user-attachments/assets/f507a205-427f-49be-b500-5a180aab776b)

The Graph below shows the Transient Response of the Given Design ;
![Screenshot 2025-02-17 010109](https://github.com/user-attachments/assets/89a034ca-a29b-4594-9c8e-1eb11d213f09)

 3. AC ANALYSIS:

Procedure for Performing AC Analysis : We have to select the AC Analysis in the edit simulation command,Give the values asa shown in the figure beloww and run the simulation.

![Screenshot 2025-02-17 010801](https://github.com/user-attachments/assets/9b184879-1312-4900-84c1-7fdbf1028697)

The Graph below shows the AC Analysis of the Given Design;

![Screenshot 2025-02-17 010222](https://github.com/user-attachments/assets/c81901e9-d8af-4134-99b0-63b6fb4d4340)
# RESULT(Design - 1):
1 . DC Analysis

   1.The C alculated drain current (Id) aligns with the expected value based on power and 
      voltage,Id = 5.56*10^-5 A.
      
   2.By adjusting the MOSFET's channel dimensions to L = 175 nm and W=178 nm,the required was 
      successfully achieved.
      
   3.The circuit performs as expected under DC conditions .
    
2 .TRANSIENT ANALYSIS :

   1. The transient response graph illustarates the circuits behaviour over time.
      
   2.The response is smooth, without any delays or distortions.
   
   3.The circuit reacts well to changes confirming its stability.


3 . AC Analysis :

   1. The AC response graoh confirms that the ciruit remains stable at different frequencies.
     
   2. The gain(-9.94 dB) and phase shift(which is nearly 180 deg)align with theoretical 
      expectations.
      
   3. The circuit maintains its performance across the tested frequency range.

# INFERENCE(Design - 1):

   1.The experiment confirms that by properly selecting the MOSFET dimensions, we can control the drain current effectively.
   
   2.Impact of Width Adjustments:
         1.M1 has a influence on Id, meaning its width affects the output current. Increase in 
           Width increases Id and Vice-versa.
           
   3.The circuit performs well in all three analyses—DC, transient, and AC—demonstrating its 
     reliability.
     
  4.Overall, the design works as intended, following theoretical predictions and proving its 
    practical feasibility.


# DESIGN - 2 
![Screenshot 2025-02-17 010844](https://github.com/user-attachments/assets/89df9849-00e4-4c90-9381-d835087cc479)

Aim : To find DC operating point, find gain using transient analysis and AC analysis.

Components: MOSFET's (M1 & M2),DC power supply.

Procedure :

 1. Make the circuit connection as show above.

  2.Connect DC power supply to the gate terminal.

  3.Connect the source terminal to the ground.

  4.Set the input voltage by obtaining VTC curve and VDD to 1.8 V.

Using the formula for power,

P = V*I/n

We will get the values of Id as,

Id = 5.56*10^-5 A

we have to hget the output current,Id for the given ciruits by adjusting the values of L & W of both the MOSFET'S M1 & M2(Width and Length of the channel of the MOSFET)

DC Sweep Analysis : This analysis is done for obtaining the value of Vin in saturation range;

we have to select the DC Sweep in the edit simulation command , Gve the values as shown in the figure below and run the simulation
![Screenshot 2025-02-16 232909](https://github.com/user-attachments/assets/09af4f47-077f-46d5-9873-9727e977b32b)

The Graph beow represents the VTC Curve and the value of the vin is selected as 0.8V as it is present in the saturation region of the VTC Curve
![Screenshot 2025-02-16 232735](https://github.com/user-attachments/assets/1ceb05a2-46ba-43af-9857-623692a0ca3a) 

The input vltage parameters are given as;
![Screenshot 2025-02-17 004134](https://github.com/user-attachments/assets/79614f61-ca04-41fe-af59-094887c1c7c0)

Length and Width of the Channel of the two MOSFETS used to obtain the given Current is shown in
the figure below;
![Screenshot 2025-02-16 232841](https://github.com/user-attachments/assets/872fca49-9bab-4964-9cea-984593b22091)
![Screenshot 2025-02-16 232852](https://github.com/user-attachments/assets/d1530afa-ca86-4d75-90a7-d1547117f46e)

Now let us perform DC,Transient & AC analysis;

1. DC ANALYSIS :

 Procedure for Performing DC Analysis: We have to select the DC output print(DC op pnt)in the edit simulation command and run the simulation
![Screenshot 2025-02-17 005944](https://github.com/user-attachments/assets/f8bc17df-fb60-41b5-a506-070400679fc8)

The Figure below shows the Values obtained from the DC Analysis :
![Screenshot 2025-02-16 233805](https://github.com/user-attachments/assets/48d964c9-8fc1-4009-a912-b1b57978ef41)

2. Transient Analysis:

    Procedure for Performing DC Analysis: We have to select the DC output print(DC op pnt)in 
    the edit simulation command and run the simulation
   
![Screenshot 2025-02-17 010729](https://github.com/user-attachments/assets/4045cd57-3797-4495-92a3-92f465718305)

The Graph below shows the Transient Response of the Given Design :
![Screenshot 2025-02-16 231510](https://github.com/user-attachments/assets/ba515163-6c9b-48c3-ac56-4bba2ba3cd97)

3. AC Analysis :
   
    Procedure for Performing DC Analysis: We have to select the DC output print(DC op pnt)in 
    the edit simulation command and run the simulation
   
![Screenshot 2025-02-17 010801](https://github.com/user-attachments/assets/b4d6277d-53d7-45ec-bdd1-4e0afe22a977)

The Graph below shows the Transient Response of the Given Design :

![Screenshot 2025-02-16 233952](https://github.com/user-attachments/assets/e7ba22f3-4154-4023-aff0-f94e641302e3)

# RESULT(DESIGN - 2)

1. DC Analysis :

   1. The calculated drain current (Id) matches the expected value based on power and voltage, 
      Id = 5.56*10^-5 A.
      
   2.By adjusting the MOSFET’s channel dimensions (L & W) of both MOSFET's(M1 & M2), the 
     desired current was acheived,
           1.M1 : L=500nm,W=950nm.
           2.M2 : L=300nm,W=1020nm.
   
    3.The circuit behaves as expected under DC conditions.


3. Transient Analysis :

     1.The response is smooth, with no unexpected delays or distortions.
   
     2.The circuit reacts well to changes, confirming its stability.

5. AC Analysis :

    1.The AC response graph confirms that the circuit maintains stability over the tested 
      frequency range.
   
    2.The gain(3.8 dB) and phase shift (which is nearly 180deg) align with theoretical 
      expectations.
   
    3.The circuit functions as expected under AC conditions.


#Inference(Design - 2):

  1.The experiment validates that by appropriately selecting the MOSFET dimensions (L & W), 
    the drain current can be precisely controlled.

  2.The voltage transfer characteristics (VTC) helped in selecting the correct operating 
    voltage (0.8V) for saturation.

  3.Impact of Width Adjustments:

    1.M2 has a stronger influence on Id, meaning its width significantly affects the output 
      current. Increase in width increases Id drastically and vice-versa.
    2.M1 has a smaller influence, meaning changes in its width result in only minor variations 
      in Id. Increase in qidth increases Id by small amounts and vice-versa.
      
  4.The design meets the expected performance criteria and follows theoretical predictions, 
    demonstrating its feasibility in practical applications.

   
