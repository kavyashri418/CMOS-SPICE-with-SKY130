# CMOS Switching Threshold and Dynamic Simulations

## 1 Voltage transfer characteristics - SPICE Simulation 
## 2 Static Behaviour Robustness:
1) Switching Threshold, VM
  - The switching threshold, $V_M$, is defined as the point where $V_{in} = V_{out}$.
  - Graphically it can be found from the intersection of the VTC with the $V_{in} = V_{out}$ line.
  - In the region around $V_M$, both PMOS and NMOS are in saturation, since $V_{DS} = V_{GS}$.
  - An analytical expression for $V_M$ can be obtained by equating the currents through the PMOS and NMOS transistors, $I_{DSn}=I_{DSp}$.
  - Depending on the supply voltage, $V_{DD}$ and the Channel length, $L$, of the devices, there can be two cases:
    1) Devices are Velocity Saturated
    2) Velocity Saturation does not occur

_**Note:**_ For the following derivations, we ignore the effects of Channel Length Modulation for simplicity.  


**<ins>Case 1:</ins> Devices are Velocity-Saturated - $V_{DSAT}<(V_M-V_{TH})$**  
  - This case is applicable to short-channel devices or when the supply voltage is high so that the devices are in velocity saturation.

$I_{DSn} = -I_{DSp}$  
$i.e.,$  
$~~~~ I_{DSn} + I_{DSp} = 0$  

$k_n \left[ (V_M - V_{THn})V_{DSATn} - \dfrac{V_{DSATn}^2}{2} \right] + k_p \left[ (V_M - V_{DD} - V_{THp})V_{DSATp} - \dfrac{V_{DSATp}^2}{2} \right] = 0$

$k_n V_{DSATn} \left[ V_M - V_{THn} - \dfrac{V_{DSATn}}{2} \right] + k_p V_{DSATp} \left[ V_M - V_{DD} - V_{THp} - \dfrac{V_{DSATp}}{2} \right] = 0$

<br>

$Solving for V_M:$  

$\boxed{V_M = \dfrac{\left( V_{THn}+\dfrac{V_{DSATn}}{2} \right) + r \left( V_{DD}+V_{THp}+\dfrac{V_{DSATp}}{2} \right)}{1+r}},$  
  
$where, ~ \boxed{r=\dfrac{k_p V_{DSATp}}{k_n V_{DSATn}} = \dfrac{\upsilon_{satp} W_p}{\upsilon_{satn} W_n}}$ _(assuming for identical oxide thickness for PMOS and NMOS transistors)_  

  - Now, for large values of $V_{DD}$ compared to the threshold voltages $(V_{THp}, V_{THn})$ and saturation voltages $(V_{DSATp}, V_{DSATn})$, the above equation can be approximated to:

$~~~~~~~~~~~~~~~~ \boxed{V_M \approx \dfrac{rV_{DD}}{1+r}}$  

  - The switching threshold is determined by the ratio, $r$ - which is a measure of the relative drive strengths of the PMOS and NMOS transistors.
  - For comparable values for low and high noise margins, $V_M$ is desired to be located around the centre of the available voltage swing (or at $V_{DD}/2$ as CMOS logic has rail-to-rail swing). This implies:  
$~~~~~~~~ r \approx 1$  
$~~~~~~~~ i.e., k_p V_{DSATp} = k_n V_{DSATn}$  
$\boxed{(W/L)\_p = (W/L)\_n * \dfrac{{k_n}^\prime V_{DSATn}}{{k_p}^\prime V_{DSATp}}}$  

  - To move the $V_M$ upwards, a larger value of $r$ is needed, which in other words is to make the PMOS wider.
  - On the other hand, to move the $V_M$ downwards, the NMOS must be made wider.
  - If a target design value for $V_M$ is desired, we can derive the required ratio of PMOS vs. NMOS transistor sizes in a similar manner:

$~~~~~~~~ \boxed{\dfrac{(W/L)\_p}{(W/L)\_n} = \dfrac{k_n^\prime V_{DSATn} \left[ V_M - V_{THn} - \dfrac{V_{DSATn}}{2} \right]}{k_p^\prime V_{DSATp} \left[ V_{DD} - V_M + V_{THp} + \dfrac{V_{DSATp}}{2}\right]}}$  
$~~~~~~~~ Note:$ _Make sure that the assumption that both devices are velocity-saturated still holds for the chosen operation point._


**<ins>Case 2:</ins> Velocity Saturation does not occur - $V_{DSAT}>(V_M-V_{TH})$**  
  - This case is applicable for long-channel devices or when the supply voltages are low, that the devices are not velocity saturated.
  - Using a similar analysis done in Case 1 above, we derive the switching threshold, $V_M$ to be:

$~~~~~~~~ \boxed{V_M = \dfrac{V_{THn} + r(V_{DD} + V_{THp})}{1+r}}, ~~~~ where ~ r = \sqrt{\dfrac{-k_p}{k_n}}$  

  - The switching threshold, $V_M$ **is relatively insensitive to variations in the device ratio**.
    - Small variations of the ratio (e.g., 3 or 2.5) do not disturb the transfer characteristic that much.



