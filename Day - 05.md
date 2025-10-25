# CMOS Power Supply and Device Variation Robustness Evaluation

## Static Behavior Evaluation -  CMOS Inverter Robustness Power Supply Variation

## 1 Smart SPICE Simulation for Power Supply Variation

Smart SPICE simulation for power supply variation involves performing detailed DC, transient, and parametric analyses to evaluate the impact of V<sub>DD</sub> fluctuations on circuit performance metrics such as propagation delay, static and dynamic power, rise/fall times, and noise margins. In advanced CMOS technologies, supply variations arise due to IR drop, Ldi/dt noise, and process-voltage-temperature (PVT) interactions, which can degrade timing and logic integrity. Using Smart SPICE, we can perform corner simulations and Monte Carlo analyses to model voltage droops and transients across operating conditions. This enables precise characterization of supply sensitivity, identification of critical timing paths, and optimization of device sizing and biasing to maintain robust operation and ensure design reliability under voltage scaling conditions.

## 2 Power Supply Scaling

Reducing the supply voltage yields a significant reduction in the energy dissipation, but it is absolutely detrimental to the performance of the gate, increasing the transition times greatly.
The DC characteristic becomes increasingly sensitive to variations in the device parameters such as the transistor threshold, once supply voltages and intrinsic voltages become comparable.
Scaling the supply voltage means reducing the signal swing. While this typically helps to reduce the internal noise in the system (such as caused by crosstalk), it makes the design more sensitive to external noise sources that do not scale.

Advantages of using 0.5V supply
- Increase in gain (close to 50% improvement)
- Significant reduction in energy (close to 90% improvement)

Disadvantages of using 0.5V supply
- Performance inputs

## Static Behavior Evaluation -  CMOS Inverter Robustness Device Variation

1 Source of variation - etching process

<img width="2753" height="1087" alt="Screenshot 2025-10-18 194109" src="https://github.com/user-attachments/assets/033a8072-c062-4342-ad4d-7be0875fc3c3" />
<img width="928" height="522" alt="CircuitDesignWorkshop_D5_CMOS_Inverter_Robustness_DeviceVariations_2" src="https://github.com/user-attachments/assets/b3f49721-92ec-42d6-9c3f-499a37aa56fe" />

2 Source of variation - oxide thickness

<img width="2845" height="1081" alt="Screenshot 2025-10-18 195559" src="https://github.com/user-attachments/assets/00dc446e-3fa7-4088-b7f6-2209d01f703e" />
<img width="928" height="527" alt="CircuitDesignWorkshop_D5_CMOS_Inverter_Robustness_DeviceVariations_4" src="https://github.com/user-attachments/assets/96d8380f-b59b-4b9d-bb90-8042d05643ae" />

LAB Device Variation - sky130 Inverter - ((Wp:7u --> 0.42u, Wn:0.36u --> 7u, L=0.15u)

In this exercise, we try to capture the CMOS Inverter's robustness in the case of a ridiculously extreme case of device width variation.

<img width="925" height="522" alt="CircuitDesignWorkshop_D5_CMOS_Inverter_Robustness_DeviceVariations_5" src="https://github.com/user-attachments/assets/dae3dbae-71f2-4e0a-85bc-083540eb1826" />


