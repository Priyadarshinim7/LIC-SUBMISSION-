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
The Drain current (Id) Can be determined:

P = V * I

I = P / V

I = 50μW / 1.8V

I = 27.7μA












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

inference:AC analysis of a MOSFET helps understand its frequency response, gain, and impedance characteristics, making it essential for amplifier design. Transient analysis, on the other hand, examines the MOSFET’s time-domain response, including switching speed, rise/fall times, and circuit stability. Together, these analyses provide insights into the MOSFET’s performance in both steady-state and dynamic conditions, aiding in optimizing circuit design for applications like amplification and switching.

q2:The supplied supply voltage is 1.8V, and the dissipation of power is 50μW. Given a gate voltage (VG) of 0.9V, the target voltage is used to determine the DC operating point (ID). Moreover, an AC analysis is carried out with a sinusoidal input voltage, and then analyzed using shifted transients to determine the time domain.

circuit diagram:
![Screenshot_20250217-233354~2](https://github.com/user-attachments/assets/44fe60eb-d900-4652-80e9-f61f0760b2ab)

PMOS and NMOS:
PMOS (P-channel Metal-Oxide-Semiconductor) and NMOS (N-channel Metal-Oxide-Semiconductor) are two types of MOSFET (Metal-Oxide-Semiconductor Field-Effect Transistor) devices used in digital and analog circuits. They function as electronic switches or amplifiers in integrated circuits.

NMOS (N-Channel MOSFET)

Carrier Type: Electrons (high mobility, faster operation)

Operation: Turns ON when the gate voltage (V_GS) is positive relative to the source.

Conducting State: When V_GS > V_TH (threshold voltage), the drain-to-source channel conducts.

Common Use: Faster switching, widely used in logic circuits, microprocessors, and memory devices.

Symbol: Arrow pointing out of the source.


PMOS (P-Channel MOSFET)

Carrier Type: Holes (lower mobility, slower operation)

Operation: Turns ON when the gate voltage (V_GS) is negative relative to the source.

Conducting State: When V_GS < V_TH, the drain-to-source channel conducts.

Common Use: Often used in combination with NMOS in CMOS circuits for low power consumption.

Symbol: Arrow pointing into the source.

simulation:
![Screenshot_20250217-234009~2](https://github.com/user-attachments/assets/1b581670-0350-431f-a909-e72c27c74b71)
AC Analysis
A sinusoidal input is included in the AC analysis through a modification of gate voltage.

![413776816-6c1c2fa0-3277-4d41-89bb-8a3d2d9f0fd3](https://github.com/user-attachments/assets/b8909f2e-b0fd-4171-9d00-0d54d06f8ff9)


DC Offset: 0.9V
Amplitude: 50mV
Frequency: 1kHz
Frequency Sweep Parameters

Type: Decade
Sweeps per Decade: 20
Start Frequency: 0.1Hz
Stop Frequency: 1THz
By analyzing the AC, one can determine gain, bandwidth, phase, and other characteristics of the amplifier's frequency response.



Transient Analysis
By examining the transient response of the amplifier, it is possible to determine its behavior over time when subjected to the sinusoidal input.
![Screenshot 2025-02-15 144833](https://github.com/user-attachments/assets/ea22b132-baed-46ad-9ad7-5602dca98901)


Parameters

Stop Time: 5m (5 milliseconds)
The transient analysis provides information about the amplifier's time-domain behavior, such as distortion, settling time, and waveform reproduction.



Inference
DC Analysis:
The drain current (ID) required is approximately 27.78A, which should ensure the MOSFET operates correctly at its desired location.
The conditions of biasing offer a reliable means of amplification.

AC Analysis:
The gain response and bandwidth can be analyzed using the AC sweep.
The amplifier's performance across a broad frequency range, including its cutoff frequencies and phase behavior, will be taken into account when determining its suitability for various applications.

Transient Analysis
The input waveform is accurately reproduced by the amplifier, as demonstrated.




