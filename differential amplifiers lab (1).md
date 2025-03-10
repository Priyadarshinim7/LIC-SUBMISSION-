Design and analysis of the MOSFET differential

theory:
A **MOS differential amplifier** is a key circuit used in analog electronics, consisting of two MOS transistors with their sources connected together and input signals applied to their gates. It amplifies the **difference** between the two input signals while rejecting **common-mode signals**, which is a crucial feature for many applications. The voltage gain of the amplifier is given by \( A_v = g_m R_D \), where \( g_m \) is the transconductance of the MOS transistors and \( R_D \) is the load resistance. An important parameter, the **common-mode rejection ratio (CMRR)**, measures how well the amplifier rejects common-mode signals; higher CMRR values indicate better performance. Small-signal analysis of the amplifier typically involves using **transconductance** and **drain-source resistance** to model the behavior of the transistors. Proper **biasing** is essential to ensure the transistors operate in the saturation region, where they can amplify the input signals efficiently. To stabilize the current in the differential pair, a **current source** is often used to provide a constant tail current. The design process must consider factors such as **input impedance**, **output impedance**, and **gain** to ensure optimal performance. For improved performance, a **cascode configuration** can be used to reduce the effects of **channel-length modulation**, thereby enhancing the voltage gain and CMRR. MOS differential amplifiers are widely used in **operational amplifiers (op-amps)**, **signal conditioning**, and **analog-to-digital converters (ADCs)**, where precise amplification of small signals is critical.

CIRCUIT DESIGN:
A common mode differential amplifier consists of two matched transistors,a current source,and load resistors or active loads. The input signals are
applied to the bases of the transistors, while the emitters share a common connection to the current source. In differential mode, when one input increases and the other decreases, the circuit amplifies the difference between them.In common mode, when both inputs change together, the output ideally remains unchanged,
rejecting noise and interference.The amplifier's performance is characterized by its differential gain, common-mode gain, and
Common Mode Rejection Ratio (CMRR).High CMRR ensures better noise immunity, making this circuit essential in operational  amplifiers, instrumentation systems, and communication.
![image](https://github.com/user-attachments/assets/e345def0-d07d-4e51-ae0e-2b37e2647b35)

Given question:
Design and analyze the differential amplifier for the following spets. V DD=2.2V ,P <= 2.2W Vicm =1.2v V ocm =1.25 v v\_{p} = 0.4v perform:DC, transient analysis,
frequency response and Extract the parameter

From calculation we got
![IMG-20250310-WA0007](https://github.com/user-attachments/assets/5eb3349a-eb06-4bce-a3f5-d604206acda9)

Iss=1mA
Rd= 1.9kohm

Rss= 400ohm
![Screenshot 2025-03-05 084529](https://github.com/user-attachments/assets/79caac10-28b4-4bc5-8f90-02f0bba753a8)


DC operation:
![Screenshot 2025-03-05 200009](https://github.com/user-attachments/assets/d486e1d5-7f9c-4f87-8718-668c45411f54)

Transient analysis:Transient analysis of a common mode differential amplifier focuses on its
time-domain response to changing input signals. It examines how the circuit reacts to step,
pulse, or sinusoidal inputs, considering factors like rise time, fall time, and settling time.
![Screenshot 2025-03-05 194750](https://github.com/user-attachments/assets/7129fc04-71c6-4f53-b1f6-409bce36f8cd)

![Screenshot 2025-03-05 194846](https://github.com/user-attachments/assets/ba84e155-adf4-4e9d-b0c2-5e63eabfd4de)

AC Analysis:AC analysis of a common mode differential amplifier evaluates its small-signal

gain, impedance, and frequency response. Differential gain is high, while common-mode

gain is minimized for better noise rejection. Parasitic capacitances affect bandwidth, and

CMRR determines signal integrity. This analysis ensures optimal performance in

amplification and filtering applications.
![Screenshot 2025-03-05 195117](https://github.com/user-attachments/assets/6b62c287-bb35-4597-8817-21a767199646)

![Screenshot 2025-03-05 195316](https://github.com/user-attachments/assets/ca0ac5e5-9d22-43a7-9f02-5dbeef7cae17)

We can observe the bandwidth of the each MOSFET at 3dB in the above pictures of ac
analysis of M1 and M2 respectively.which is of 30-40GHz

Gain of mosfets in the circuit:
![Screenshot 2025-03-05 213210](https://github.com/user-attachments/assets/dd0f80e9-f6e1-4c2f-8fda-8202483a1aff)

![Screenshot 2025-03-05 195941](https://github.com/user-attachments/assets/2d5e9c72-ccae-4da0-8cab-c161d08a021c)

 We can observe gain of each MOSFET is same which Is obtained in dB
 MOSFETs in a common mode differential amplifier have the same gain because they are
typically matched transistors operating under identical conditions. Their transconductance (),
drain resistance, and bias currents are nearly equal, ensuring symmetrical operation.
In differential mode, when one MOSFET increases conduction, the other decreases by the
same amount, maintaining balance. This symmetry results in equal but opposite gains for
both transistors, ensuring proper differential amplification and minimizing common-mode
signal amplification.

Gain in V/V
![gain](https://github.com/user-attachments/assets/d01cece0-d8d6-41fb-a7aa-42276f4f5c36)

Other parameters from the simulation:

![Screenshot 2025-03-05 200542](https://github.com/user-attachments/assets/b8099d22-ed4a-4189-a2ea-66db2637f125)
 

Next for the circuit 2: replace Rss by current source of the value Iss
![Screenshot 2025-03-05 215920](https://github.com/user-attachments/assets/fdbaece8-02a3-4907-a269-381c91fb1e54)


DC operation:
![Screenshot 2025-03-06 002009](https://github.com/user-attachments/assets/39255ee6-876a-4778-b2a1-ce6046b2ab41)

Transient analysis: is a method used to study how a circuit's voltages and currents change
over time in response to varying inputs or initial conditions. It helps engineers analyze the
behavior of circuits before they reach a steady state. This type of analysis is essential for
understanding signal propagation, switching behavior, and dynamic performance in
electronic circuits. It is commonly applied to RC, RL, and RLC circuits, as well as oscillators,
filters, and digital logic circuits. By solving time-dependent differential equations, transient
analysis provides insight into how circuits respond to sudden changes, such as power-on
conditions or signal transitions.
![Screenshot 2025-03-06 083056](https://github.com/user-attachments/assets/e9b5bfe9-d8e9-4216-9d00-785cedb28bda)
![Screenshot 2025-03-06 083007](https://github.com/user-attachments/assets/46442318-7292-464e-9e50-52fc0371b528)

Vout peak to peak and Vin peak to peak are same from both the MOSFETs

Manual gain calculation:
![gain](https://github.com/user-attachments/assets/d4772f7f-c7e4-4a0d-b212-e97d94d054b5)

Gain in dB from the simulation of the circuit:
![Screenshot 2025-03-06 083900](https://github.com/user-attachments/assets/7afb63a3-c5b3-42c5-84ac-361eb0eecbff)


AC analysis:
AC analysis of a differential amplifier helps evaluate its frequency response, gain, and phase
shift across different frequencies. It determines how effectively the amplifier amplifies the
difference between two input signals while rejecting common-mode signals. This analysis
assumes a small AC signal is applied, and the circuit is linearized around its DC operating
point. The results typically include the differential gain, bandwidth, and phase response,
which are crucial for designing high-performance amplifiers. By plotting a Bode plot,
engineers can observe the gain in dB and phase shift over a frequency range, helping
optimize circuit performance for specific applications.

![Screenshot 2025-03-06 082838](https://github.com/user-attachments/assets/47f94d70-68b5-4944-92ee-f8143b48aa8a)

To calculate the bandwidth from the graph:
1. Identify the maximum gain (mid-band gain)
From the Bode plot, the maximum gain is around 12.6 dB.
2. Find the -3dB point
The bandwidth is the frequency at which the gain drops by 3 dB from the maximum.
Since the max gain is 12.6 dB, we look for the frequency where the gain reaches 9.6 dB.
3. Locate the -3dB frequency on the graph
From the graph, the gain starts rolling off around the GHz range.
The cursor shows 4.48 GHz with a gain of 6.789 dB, which is already lower than -3dB from
the peak.
Observing the graph, the -3dB point appears to be around 3 GHz to 3.5 GHz.
Estimated Bandwidth
Bandwidth ≈ 3.2 GHz (approximate value based on visual interpretation).

Circuit 3:  we replace the current source by the MOSFET having the input signal Vb.

![Screenshot 2025-03-06 084638](https://github.com/user-attachments/assets/78901070-85b8-4156-9a74-aca42d95baf4)
 
To get Id of M3 ,we arranged the value of w and L of MOSFET:
![Screenshot 2025-03-10 145438](https://github.com/user-attachments/assets/821add64-7164-465c-a0aa-7f0e021a488b)

Manual calculation of Vgs of M3 using data sheet:

![IMG_20250306_120703477~2](https://github.com/user-attachments/assets/6c4ee9b7-1f85-4f8b-a8bd-d93eb7bbe241)

Transient analysis:
![Screenshot 2025-03-06 084827](https://github.com/user-attachments/assets/2795521b-1224-4f64-98cd-795f65b7cacf)

![Screenshot 2025-03-06 084752](https://github.com/user-attachments/assets/c00dac5c-1263-4979-a4ee-f685e3744fa9)

"Gain of circuit 2 and Circuit 3 remains same."
![gain](https://github.com/user-attachments/assets/d09380f1-da79-47bd-a683-f9635036e5ca)
gain in dB from graph:
![Screenshot 2025-03-06 085303](https://github.com/user-attachments/assets/c78003fa-e990-4e02-afcd-f586d452e46a)


AC analysis:
![Screenshot 2025-03-06 085405](https://github.com/user-attachments/assets/971d30b7-91dc-4eee-824e-b80314bb82c7)

To calculate the bandwidth from the given AC analysis graph,

Step 1: Identify the Midband Gain
Step 2: Find the -3dB Point
Bandwidth is defined as the frequency range where the gain is within -3dB of the peak gain.
The -3dB point is:
12.6 dB - 3 dB = 9.6 dB
From the cursor at 4.48 GHz, the gain is 6.789 dB, meaning the -3dB point occurs at a lower frequency.
Observing the plot, the -3dB cutoff appears around 3-4 GHz.
Step 3: Estimate the Bandwidth
Lower cutoff frequency (fL): Since it's a differential amplifier, low-frequency cutoff is usually very low (near DC).
Upper cutoff frequency (fH): From the graph, it's approximately 4 GHz.
Final Answer:
The bandwidth of the differential amplifier is approximately 4 GHz.

Inference of Common-Mode Analysis in a Differential Amplifier:

Common-mode analysis of a differential amplifier helps determine how well the circuit rejects
noise or unwanted signals that appear equally on both inputs. Here are the key inferences:
1. Common-Mode Gain ()
Ideally, a differential amplifier should have a very low common-mode gain.
In practical circuits, due to device mismatches, a small common-mode gain exists.
2. Common-Mode Rejection Ratio (CMRR)
   CMRR = , where is the differential gain.A high CMRR indicates better rejection of noise and power supply variations.
   Typically, MOSFET-based differential amplifiers (like in your circuit) have a high CMRR dueto current source biasing.
3. Impact of Mismatch 
  Resistor mismatches and MOSFET threshold variations can increase common-mode gain,reducing CMRR.
  The addition of active loads or tail current sources improves CMRR by ensuring better symmetry.
4. Frequency Response in Common Mode
 The common-mode bandwidth is usually different from the differential mode.
 At high frequencies, common-mode rejection may degrade due to parasitic capacitances.
5. Practical Applications
   A high CMRR is essential in sensor interfaces, communication circuits, and operational amplifiers to reject power supply noise and external interference.
Final Conclusion:
A well-designed differential amplifier should exhibit low common-mode gain and high CMRR,
ensuring better signal integrity by rejecting external noise and interference effectively.

Summary Comparison
![Screenshot 2025-03-10 153251](https://github.com/user-attachments/assets/f9a86b4e-d77e-43cf-9402-d20946bc5334)
Conclusion:
Resistive load amplifiers are simple and cost-effective but have lower gain and CMRR.
Current source load amplifiers offer higher gain and better linearity, making them suitable for high-performance applications.
MOSFET load amplifiers deliver the highest gain and best CMRR, suitable for precision analog applications but require more complex design and higher cost.
The choice of load depends on the specific application, performance requirements, and design constraints.





