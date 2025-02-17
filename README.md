ANALYSIS OF CS AMPLIFIER 

Aim: to evaluate the CS amplifier’s gain, frequency response, and overall performance using LTspice.

Analysis: Transient analysis,AC analysis and DC analysis.

Data specified: Vdd = 1.8V ,180nm technology MOSFET,tsmc library,Power of FET = 50uW,input voltage of MOSFET varies from 0 to Vdd volts


Overview:A Common-Source (CS) Amplifier in LTspice amplifies voltage using an NMOS transistor. It consists of RD, signal voltage,DC power supply,Rs(if provided) .

We should Run DC analysis to check biasing, AC analysis for gain and bandwidth, and transient analysis for waveform behavior. The amplifier provides high gain with a 180° phase shift. 


https://photos.app.goo.gl/9kYK2Z21oLCXFukg8
