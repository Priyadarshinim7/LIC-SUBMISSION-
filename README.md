ANALYSIS OF CS AMPLIFIER 

Aim: to evaluate the CS amplifier’s gain, frequency response, and overall performance using LTspice.

Analysis: Transient analysis,AC analysis and DC analysis.

Data specified: Vdd = 1.8V ,180nm technology MOSFET,tsmc library,Power of FET = 50uW,input voltage of MOSFET varies from 0 to Vdd volts


Overview:A Common-Source (CS) Amplifier in LTspice amplifies voltage using an NMOS transistor. It consists of RD, signal voltage,DC power supply,Rs(if provided) .

We should Run DC analysis to check biasing, AC analysis for gain and bandwidth, and transient analysis for waveform behavior. The amplifier provides high gain with a 180° phase shift. 

![Screenshot 2025-02-16 215141](https://github.com/user-attachments/assets/00397026-78ba-46cd-932f-43321e0070ae)

For the given power of MOSFET ,and Voltage range is 0 volts to Vdd ,
From power formula drain current Id is 27.77mA
To find the value of length and width of the MOSFET












Simulation:
![Screenshot 2025-02-15 114543](https://github.com/user-attachments/assets/a35529cc-34da-42d0-b884-b8be182ac719)

DC operation:
![Screenshot 2025-02-15 114427](https://github.com/user-attachments/assets/b30c2510-8a03-4be9-bd79-c59570ff2672)

The drain current obtained in the simulation is matching with our calculations,hence width and length of the MOSFET we have calculated is correct is then verified 

AC analysis: 
AC analysis of a MOSFET involves studying its response to small AC signals while ignoring DC components. First, the DC operating point (Q-point) is determined to establish biasing conditions. Then, the MOSFET is replaced with its small-signal equivalent model, which includes parameters like transconductance () and output resistance (). The circuit is analyzed to determine voltage gain, input impedance, and output impedance. This analysis helps in designing amplifiers and understanding frequency response characteristics.

![Screenshot 2025-02-16 140654](https://github.com/user-attachments/assets/83550495-72e2-4a2b-927b-02e821e3dc79)

Transient analysis:
Transient analysis of a MOSFET studies its time-domain response to input signals, analyzing voltage and current changes over time. It helps evaluate switching behavior, rise/fall times, and circuit stability.
input voltage characteristics is as follows 
![Screenshot 2025-02-15 161021](https://github.com/user-attachments/assets/7382de93-945d-4b7a-b843-5e9cc3ba9a13)


output characteristics is as follows 
![Screenshot 2025-02-15 163432](https://github.com/user-attachments/assets/44005265-3c2c-40b2-b070-d193155dc365)

from input and output characteristics we can observe the 180° phase shift 

aslo input voltage and output current is having 180° phase difference 
![Screenshot 2025-02-15 161245](https://github.com/user-attachments/assets/840efbb3-359a-4712-ab21-95a4843bbc2f)

also one thing that we can observe is when we give input lenth and width of mosfet as same value the drain current is same in that case
for example;
![Screenshot 2025-02-16 215203~2](https://github.com/user-attachments/assets/d7f1b1a9-3fbf-4789-be8c-a156787399c8)
![Screenshot 2025-02-16 215302~2](https://github.com/user-attachments/assets/6eb4e6f7-7bd6-420f-bd90-bc5f4a0fc22a)

for both the cases drain current output is same
![Screenshot 2025-02-16 215323](https://github.com/user-attachments/assets/a7fb5ccc-70c5-4def-b6f5-dd582491784e)




