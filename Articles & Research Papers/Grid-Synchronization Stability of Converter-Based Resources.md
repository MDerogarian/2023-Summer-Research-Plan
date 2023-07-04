Wang, Xiongfei, et al. "Grid-synchronization stability of converter-based resources—An overview." IEEE Open Journal of Industry Applications 1 (2020): 115-134.

<br> The grid synchronization methods can be classified into two categories with respect to the operating modes of converter-based resources:
- The voltage-based grid synchronization that measures or estimates (voltage sensor-less) the frequency and phase of the voltage at the point of common coupling (PCC) of grid-connected converters. The detected phase is then used with the vector current control or the direct power control for regulating the active and reactive power exchanged with the grid. Such a voltage based grid synchronization control is named as the grid following control, since they follow the phase of grid voltage
- The power-based synchronization dictates directly the phase of the PCC voltage by regulating the active power of the converters [10], where the general idea is to utilize the active power-frequency (P-ω) droop control, which is widely used with synchronous generators, to synchronize converters with the grid [11]. To track the generated phase of the PCC voltage, the voltage control is required, which, thus, differs from grid-following converters. Such voltage-controlled converters are recently known as the grid-forming converters
  
<br> The synchronization stability of converter-based resources can be categorized into two types: small-signal stability and large-signal (transient) stability, similarly to the rotor angle stability of synchronous generators in legacy power systems

<br> The nonlinear systems theory is required to evaluate if the system dynamics can converge to a stable equilibrium point when subjected to large disturbances. It has recently been found that the PLL essentially introduces a second-order nonlinear swing equation to grid-following converters, and a voltage-angle curve, instead of the conventional power-angle curve, is resulted for the transient stability analysis. In contrast, the droop-controlled grid-forming converters can be characterized as a first-order nonlinear system, which can significantly improve the transient stability. Yet, the reactive power droop control loop can adversely affect the transient stability of grid-forming converters. Differing from synchronous generators (SGs), the limited overcurrent capability of power converters necessitates the use of current limiting control, which imposes another constraint to the transient stability behavior of grid-forming converters.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/1debe5d8-7b38-40eb-9b60-da8d6adbd56a)
<be> voltage feedforward (VFF) control is usually used through a low-pass filter and added to the output of the current controller, to enhance the dynamic performance.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/760a5013-9065-468a-a3ad-690238e89bf2)
<be> Differing from grid-following converters, a grid-forming converter behaves as a voltage source, which synchronizes with the power grid through the active power control APC. Hence, the PLL is not used for the grid-synchronization of grid-forming converters during normal operations.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/26e827c8-cf85-4b2e-9858-d6629938ae71)
