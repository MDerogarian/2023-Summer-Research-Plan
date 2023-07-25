Zhang, Haobo, et al. "Grid forming converters in renewable energy sources dominated power grid: Control strategy, stability, application, and challenges." Journal of modern power systems and clean energy 9.6 (2021): 1239-1256.

<be>With the increasing penetration of converter-interfaced RESs, the conventional synchronous generator (SG) dominated power grid is being changed to a weak power grid with low inertia. Under this condition, a small perturbation will cause large fluctuation and deviation of grid frequency, resulting in low-frequency demand disconnection and even the collapse of the power grid.

<be>To improve the frequency response, enhanced GFL control methods such as current-controlled droop control and current-controlled virtual synchronous generator (VSG) control are proposed to support the power grid. However, when integrating with weak power grids, the GFL control methods will deteriorate the stability of grid-tied converters and induce wide-band frequency oscillation problems.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/eb2b05de-0df5-434c-abf1-bd8953e5d843)


<be>Due to the constant output voltage and frequency, the GFM converter can only integrate with passive power grids (without SGs or GFM converters). When integrating with active power grids (e.g., SGs and GFM converters), the power synchronization loop (PSL) is added to the VF control to share power among other voltage sources. 
<be>The fundamental idea behind this PSL-based GFM control lies in the emulation of the rotor characteristics of SGs, which enable RESs to self-synchronize with power grids without PLL, share power among different power sources, and provide grid support to improve frequency response. Thus, it can overcome the drawbacks of GFL control.

<be>The GFM converters may suffer from small-signal stability issues when subjected to grid disturbances in strong, active grids. Additionally, during AC faults, the AC fault current limiting strategies may cause transient instability issues of GFM converters [30]-[32]. The reason is once the fault cur‐ rent exceeds the pre-defined current limiter thresholds, the saturated current will force GFM converters to work in constant current source mode, which affects the power-angle curve and causes transient instability problems.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/adc49e37-595c-4b19-9b4b-8d2cd976681d)

# GFL CONTROL
<be>Since the power references P* and Q* are constant, the PQ-controlled converter has no grid regulation capacity. That may induce a large grid frequency deviation even under a small disturbance. Moreover, since the dynamic of PLL affects the converter output impedance, the PQ-controlled converter has a poor small-signal stability with integration into weak grid, e.g., RESs dominated power grid. Besides, constrained by controlled current source characteristic, the PQ-controlled converter is a negative load to power grids, which can only transmit power in the presence of a stable AC voltage.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/0b894a50-0919-4804-bfde-ee8b5b1ef6ee)

<be>Compared with PQ control, a droop loop is added to regulate the output power. Hence, the converter can respond to grid disturbances, and has grid frequency/voltage regulation capability like SGs. However, this control cannot provide inertia support for the power grid.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/94e8e7ba-22ee-44a3-a5aa-ce301d974283)


![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/90fd5333-7c15-4f39-89a6-39d60cd0c262)

Although some improvements have been implemented, the inner control of the grid-supporting GFL control methods is still unchanged. Thus, those enhanced methods still operate as the controlled current sources without stand-alone operation capability. In addition, the inherent stability issue caused by PLL in RESs dominated grid is still a potential risk.

# GFM CONTROL

## Voltage/Frequency Control
<be> VF control is designed to maintain the output voltage amplitude and frequency constant through the closed-loop control, which is often applied in passive power grids, such as islanded grids or uninterruptable power supply (UPS) sys‐ tems. However, due to the constant voltage source characteristic, VF-controlled converter has no power-sharing capability, which cannot operate in active power grids.

<be> For the single-loop control, the converter output voltage Vinv * is generated directly by the frequency reference value ω* and reference value of voltage amplitude V *. While for the dual-loop control, Vinv * is obtained from cascaded voltage and current loops. Thus, the dual-loop control also has the cur‐ rent limiting capability.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/315b8f59-8957-4227-b907-8f5eee2fae57)

## Power Synchronization Loop-Based GFM Control

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/8cb1a99b-aefc-4edd-90c9-ba737281f8e5)

- a) The droop control lacks inertia support capability.
- b) PSC is similar to the droop control. The difference is that the power deviation is used to adjust the frequency in droop control. Due to the lack of inertial emulation, the difference between them will not cause different results
- c) It can be found that due to the existence of LPFs, the inertia term introduces an inertia simulation to the converter dynamic. Thus, the LPF droop control can provide inertia support to suppress the frequency fluctuation of the power grid.
- d) Similar to the principle of current-controlled VSG control, the active power control of VSG control also refers to the swing equation. Hence, VSG converters can simulate the moment of inertia and the damping characteristics of the rotor.
- e) Based on the VSG, the excitation characteristics of SGs have been further considered in the design of synchronverter. Therefore, the synchronverter mimics the operation characteristics of SGs more comprehensively.
- f) By designing the power control as a second-order overdamped system, the SPC can overcome the inherent power oscillation issue of SGs under grid disturbances. Thus, the closed-loop active power control can be further designed as an overdamped system to attenuate the inherent power oscillations of SGs.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/b9580e0e-43ed-4945-97a2-3700f8eff2b8)

## Virtual Oscillator Controller  Control

<be>The VOC does not require multi-loop hierarchical control, nor does it require the voltage amplitude and frequency measurements, which makes VOC much faster in terms of synchronization speed and power-sharing. The commonly used VOC is based on the Van der Pol oscillator.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/1b732600-a7b0-4c14-a8ee-3aeedef7519d)

# CURRENT LIMITING STRATEGIES OF GFM CONVERTER

<be>Due to the voltage source characteristic, the GFM converter may encounter overcurrent problems under large grid disturbances, such as AC faults. To ensure the safety of power semiconductors, the current limiting strategies for AC fault are necessary for GFM converter. There are two classic fault current limiting strategies, i. e., the instantaneous saturation limiter and the latched limiter. They are both realized by adding the current limiter block between voltage and current control.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/3d0f1046-7e1b-49d6-9e02-3fc29126f172)

<be>However, for the limiters in SYRF and STRF, all current reference coordinates will be switched to pre-defined values once the magnitude exceeds the threshold, which will cause the same injected current in three phases. As a result, there will be a large converter current injected into healthy phase under asymmetric faults, which may cause overvoltage in healthy phases.

<be> When the fault current exceeds the limiter threshold, the current reference is saturated, which will change the operation mode of GFM converters from voltage source mode to current source mode. Under this circumstance, a large input error of the PSL during faults may cause a large output frequency deviation. Meanwhile, the power angle of converters will increase continuously, leading to the loss of synchronization.

# APPLICATIONS OF GFM CONTROL

## Application in AC Microgrids

<be>Under grid disturbances, the frequency fluctuation caused by low-inertia is the major stability issue in microgrids. To im‐ prove the stability of the microgrids, GFM control is promising for grid-tied converters. By implementing the GFM control in converters of charging stations, the EVs can behave like an energy storage device to provide grid support similar to RESs. 

<be>Owing to different distances from converters to PCC, the line impedance may not meet, which will cause reactive power sharing error. The large power error may result in a large circulating current between converters and even damage the converters. While for active power sharing, since the frequency cannot be affected by the line impedance, active power can be shared according to the converter capacity without error. To eliminate the reactive power sharing error, the virtual impedance control is regarded as a promising solution. By introducing large matched virtual impedances in parallel converters, the mismatched line impedance issues can be overcome.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/5938b629-3d0e-4f0c-b737-56728b6101bd)

<be>For the power decoupling error, it arouses from the resistive lines, especially in the low-voltage microgrids. The decoupling design of P-f and Q-V droop control in GFM converters is commonly based on pure inductive lines. Thus, the resistive lines will increase the coupling between active and reactive power, which will deteriorate the power control accuracy. To overcome the power decoupling error, the virtual im‐ pedance control technology is still effective. By introducing a large virtual inductance, the effect of resistive lines can be ignored. However, the virtual inductance should be selected appropriately. A large virtual inductance will cause a large output voltage sag, which requires compensation.

## Application in Offshore Wind Farm (OWF) HVDC Systems

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/5fc33545-65c4-4df1-be1e-18d52158e66e)

<be>Since the grid-side converter (GSC) of wind turbine (WT) adopts GFL control, the offshore AC grid is equivalent to a passive grid. Thus, the VF control is commonly applied in offshore HVDC converters to provide a stable AC voltage.

<be>With the increasing integration of RESs via HVDC systems, the onshore AC grid has potential instability problems, such as low inertia and low short-circuit ratio (SCR). To overcome these issues, the GFM control can be applied in onshore HVDC converters. Due to the requirement of DC voltage control, the self-synchronization strategies of the onshore converter are commonly based on DC capacitor voltage (i. e., matching control). The matching control methods utilize the physical DC-link capacitor as energy storage, which is like the rotor energy storage of SGs.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/402f3af2-a032-4cdc-8248-0f28199b5120)

