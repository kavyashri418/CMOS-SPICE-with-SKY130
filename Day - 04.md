# CMOS Noise Margin Robustness Evaluation

## 1 Static Behaviour Evaluation - CMOS Inverter Robustness Noise Margin

## 1.1 Introduction to Noise Margin 
In digital circuits, excessive noise voltage at a node can cause logic errors, leading to incorrect signal interpretation. To prevent this, a parameter known as the noise margin defines the maximum allowable noise level that can be tolerated without affecting circuit operation. If the noise amplitude remains within this limit, the disturbance is naturally suppressed as it propagates through logic gates, ensuring reliable signal transmission. In essence, the noise margin guarantees that a logic ‘1’ with minor noise interference is still interpreted as a valid ‘1’, and a logic ‘0’ with slight noise remains a valid ‘0’, preserving circuit integrity.

## 1.2 Noise Margin NM<sub>H</sub> and NM<sub>L</sub>

The following images show an ideal, a piece-wise linear 

<img width="1685" height="976" alt="Screenshot 2025-10-18 181613" src="https://github.com/user-attachments/assets/0482e56f-95a6-4fd3-8088-680bbf518375" />

Any output voltage level between 0 and V_OL will be treated as logic '0'

## 1.3 Noise Margin Voltage Parameters

I/O characteristic plotted on scale
<img width="1592" height="829" alt="Screenshot 2025-10-18 182500" src="https://github.com/user-attachments/assets/2a847eb4-23f5-4d1b-a183-8d17dd1f694b" />

Any signal in undefined region will be indefinite logic level.

**NM<sub>H</sub> = V<sub>OH</sub> − V<sub>IH</sub>**  
**NM<sub>L</sub> = V<sub>IL</sub> − V<sub>OL</sub>** 

### 1.4 Noise Margin Equation and Summary

<img width="2029" height="1299" alt="Screenshot 2025-10-18 183752" src="https://github.com/user-attachments/assets/df06158f-985c-4758-9797-3df42a38c981" />

(a) Bump height lies between Vol and Vil will be considered as logic '0'

(b) Bump height lies between Vil and Vih output logic 'undefined'

(c) Bump height lies between Vih and Voh will be considerd as logic '1'


<img width="2135" height="1594" alt="Screenshot 2025-10-18 184436" src="https://github.com/user-attachments/assets/decc56c5-1db3-41a3-ba0d-187843c01939" />

NM<sub>H</sub> = 0.42
NM<sub>L</sub> = 0.27
Vm = 1.4V

<img width="2085" height="713" alt="Screenshot 2025-10-18 184842" src="https://github.com/user-attachments/assets/070e847d-ac73-444d-9ff7-b4a75a257382" />

