# DESIGN-DIFFERENTIAL-AMP.
_
👇👇👇👇👇

EXPERIMENT NO.3
_
_


Q=➡️Design the amplifier for the following specification:-

VDD=3.2V, P<or=2.8mW, Vicm=1.6V, Vocm=1.7V, Vp=0.6V.

Perform DC analysis, Transient analysis, Frequancy response and extract required parameters?


COMPONENTS ARE REQUIRED TO DESIGN THE CIRCUIT:-
1:- NMOS(3). 
2:- Three RESISTORS: Two 3.43k resistors, and One 685ohm resistor are required.
3:- Four Voltages sources: Two are 1.6V, and One 3.2V.
4:- Dc power supply (3.2V and 1.6V).
5:- Current source (1 mA).
6:- And this is the most imortant component without it you can't do anythig anbout this circuit for analysing digitaly, that is LTSpice software.🤣 


🔴 ➡️➡️➡️➡️➡️ CIRCUIT 1:-

![image1](https://github.com/user-attachments/assets/c65ca9e1-3724-4f04-a247-ebac5b4037a8)


  In above the diagram i have puted two NMOS (N channel mosfet). Each mosfet has given 1.6V input as you can see V2 and V3 Voltages.
The input volatge is 3.2V which is V1. I've used Three resistors, the two resistors are RD1 and RD2 (Drain resistors) and the last resistor is at load resistor its one side is grounded.  


CALUCLATION:-

   P=2.8mW

   Iss=P/Vpp =2.8mW/3.2V =0.875m

   ID1=ID2=Iss/2 =0.875/2

  ID1=0.4375mA

=>  RD=VDD-Vocm/ID1
   
RD=3.2V-1.7V/0.4375mA

   RD=3.43kohms .

=>  Rss=Vp/Iss

=0.6/0.875mA

Rss=685ohms

=> Vicm=VDD/2

=3.2V/2

Vicm=1.6V .




➡️➡️➡️Procedure for Circuit Simulation

1. ➡️

Open your circuit simulation software (e.g., LTSpice, Cadence Virtuoso, or Ngspice).

Ensure that the required CMOS model library (tsmc018.lib) is available and properly linked.



2. ➡️

Place two NMOS transistors (M1, M2) and label them accordingly.

Add resistors (R1, R2, R3) with the specified values (3.43kΩ for R1, R2, and 685Ω for R3).

Include three voltage sources (V1 = 3.2V, V2 = 1.6V, V3 = 1.6V).

![image1](https://github.com/user-attachments/assets/8042ffe5-6311-4736-a178-8e7b43eeff50)



3. ➡️

Connect the drains of M1 and M2 to resistors R1 and R2, respectively.

Connect the sources of both MOSFETs together and attach them to R3, which is grounded.

Apply the voltage sources:

V1 (3.2V) to the top of R1 and R2.

V2 (1.6V) and V3 (1.6V) to the gates of M1 and M2.




4. ➡️

Include .ac dec 20 1 1T for AC analysis.

Add .tran 5m for transient analysis.

Perform an operating point analysis using .op.




5. ➡️

Load the TSMC 180nm model file (tsmc018.lib) into the simulator.

Run the simulation and observe the voltage and current characteristics.



6. ➡️
   Analyze the Results

Plot V_cm (common-mode voltage) and compare the differential behavior.

Check drain currents of M1 and M2 for balanced operation.

Verify gain and frequency response using AC analysis.


➡️DESIGN:-


Given:VDD=3.2; P<=2.8mW;

Vicm=1.6V; Vocm=1.7V;

Vp=0.6

Iss=p/vdd=2.8/3.2=0.875mA

ID1=ID2=Iss/2=0.875/2=0.4375mA

RD=VDD-Vocm/ID1=3.2-1.7/0.4375mA=3.42K

Rss=VP/Iss=0.6/0.875mA=685 ohms

W=2.52uM

L=180nM


➡️DC ANALYSIS:-


Id1=0.4375mA

Id2=0.4375mA

Vocm1=1.7v

Vocm2=1.7v

Iss=0.875mA


![Image2](https://github.com/user-attachments/assets/361e0827-454d-43a5-9b40-4734a0cdb42e)

This is the DC Operating Point report👆👆.



AC analysis :
![Image4](https://github.com/user-attachments/assets/5fa8a2a7-6d9c-46ac-a038-55014b6a29b6)


Magnitude Shows how the differential amplifier amplifies low-frequency signals and attenuates high-frequency signals. Phase Indicates minimal phase shift at low frequencies, with significant phase delay as frequency increases, typical for differential amplifiers.

TRANSIENT ANALYSIS:-
 COMBINED WAVEFORMS
 ![Image5](https://github.com/user-attachments/assets/d1dd78aa-8505-49b8-a8d2-f55e7d4d8346)

 

INPUT waveform.

![Image3](https://github.com/user-attachments/assets/e058e0f6-09d4-4630-81d2-c70082229b2f)

The output waveform its opposite.
![image](https://github.com/user-attachments/assets/4b262bff-e6fd-45b8-85b3-c6afbaf7aed6)


Gain calculation:-


Gain=1.86-1.53/1.65-1.55

=3.3 V.

Gain in dB=20*log(3.3)

=10.52 dB.
.
.
.
.





 🔴 ➡️➡️➡️➡️➡️➡️ CIRCIUT 2:-




Design
Given:VDD=3.2; P<=2.8mW;

Vicm=1.6V; Vocm=1.7V;

Vp=0.6

P=2.8 mV

Iss=p/vdd=2.8/3.2=0.875mA

ID1=ID2=Iss/2=0.875/2=0.4375mA

RD=VDD-Vocm/ID1=3.2-1.7/0.4375mA=3.42K

Rss=VP/Iss=0.6/0.875mA=685 ohms

W=2.52uM

L=180nM.

Circuit diagram here...

![Image6](https://github.com/user-attachments/assets/28d1de5e-9c58-4bee-bc9d-6c2561623dc0)


➡️➡️ DC ANALYSIS:-

![image](https://github.com/user-attachments/assets/b80410cc-8ae6-422f-8582-15a6b1d7b98d)


TRANSIENT ANALYSIS:-

Gain=1.86-1.53/1.65-1.55

=3.3 V.

Gain in dB=20*log(3.3)

=10.52 dB


Vin=1.65-1.55.

![image](https://github.com/user-attachments/assets/a71d6741-0306-4901-93d5-3323c78565fd)

Above the input wavwforms and down there output waveforms....

Vout=1.86-1.53

![image](https://github.com/user-attachments/assets/8f05517f-f3dc-40bf-b264-aff8cffc7ca0)

Combined waveforms:- I/O waveforms..

![image](https://github.com/user-attachments/assets/d72cbdfa-6d65-465e-b3f3-d3f9f9a935e4)


AC analysis:-

![image](https://github.com/user-attachments/assets/23e4465a-97b5-4f8a-9774-f82b0b4fe0b7)
.
.
.
.






 🔴 ➡️➡️➡️➡️➡️  CIRCUIT 3:-


Given:VDD=3.2; P<=2.8mW;

Vicm=1.6V; Vocm=1.7V;

Vp=0.6

P=2.8 mV

Iss=p/vdd=2.8/3.2=0.875mA

ID1=ID2=Iss/2=0.875/2=0.4375mA

RD=VDD-Vocm/ID1=3.2-1.7/0.4375mA=3.42K

Rss=VP/Iss=0.6/0.875mA=685 ohms

W=2.52uM

L=180nM

CMOS M3 :- W=6.22u , L=180nm with 0.966v gate voltage.


![image](https://github.com/user-attachments/assets/5060bde5-9a1f-4e99-9673-264fd1f18635)


AC analysis:- 
Magnitude Shows how the differential amplifier amplifies low-frequency signals and attenuates high-frequency signals. Phase Indicates minimal phase shift at low frequencies, with significant phase delay as frequency increases, typical for differential amplifiers.

![image](https://github.com/user-attachments/assets/72a11114-865e-4939-ac96-22c8645234ab)

TRANSIENT WAVEFORMS:-  

Gain calculation
Gain=1.86-1.53/1.65-1.55

=3.3 V.

Gain in dB=20*log(3.3)

=10.52 dB.


INPUT.. 

Vin=1.65-1.55
![image](https://github.com/user-attachments/assets/c2c259da-1d2f-4e58-b1b3-fb69bf0e1fc7)

OUTPUT..

Vout=1.86-1.53
![image](https://github.com/user-attachments/assets/c919d110-94b9-43ac-ad96-30586d6d72da)


DC analysis:-

![image](https://github.com/user-attachments/assets/26210530-aaad-48bf-ac8a-4c6076fd9e10)

COMBINED WAVES:-

![image](https://github.com/user-attachments/assets/a1d2954f-e8ab-4c15-91a7-2b2c32b0bd8e)



LAST THING...

Inference :
Differential Gain: It's like a magnifying glass for differences. It makes the tiny differences between two signals much easier to see.

Common-Mode Rejection: Think of noise-canceling headphones. They block out background noise and let you hear the important sounds clearly.

Biasing and Stability: Imagine balancing a seesaw perfectly so it stays level. Proper biasing keeps everything balanced, and stability ensures it stays that way over time.

Practical Limitations: In real life, nothing is perfect. Small variations in components can lead to minor differences in performance, just like using slightly different ingredients in a recipe can change the final dish a bit

  END

THANK YOU FOR READING THIS🙏...














