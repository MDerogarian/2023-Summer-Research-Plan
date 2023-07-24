Zhang, Haobo, et al. "Grid forming converters in renewable energy sources dominated power grid: Control strategy, stability, application, and challenges." Journal of modern power systems and clean energy 9.6 (2021): 1239-1256.

<be>With the increasing penetration of converter-interfaced RESs, the conventional synchronous generator (SG) dominated power grid is being changed to a weak power grid with low inertia. Under this condition, a small perturbation will cause large fluctuation and deviation of grid frequency, resulting in low-frequency demand disconnection and even the collapse of the power grid.

<be>To improve the frequency response, enhanced GFL control methods such as current-controlled droop control and current-controlled virtual synchronous generator (VSG) control are proposed to support the power grid. However, when integrating with weak power grids, the GFL control methods will deteriorate the stability of grid-tied converters and induce wide-band frequency oscillation problems.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/eb2b05de-0df5-434c-abf1-bd8953e5d843)


<be>Due to the constant output voltage and frequency, the GFM converter can only integrate with passive power grids (without SGs or GFM converters). When integrating with active power grids (e.g., SGs and GFM convert‐ ers), the power synchronization loop (PSL) is added to the VF control to share power among other voltage sources. 
<be>The fundamental idea behind this PSL-based GFM con‐ trol lies in the emulation of the rotor characteristics of SGs, which enable RESs to self-synchronize with power grids without PLL, share power among different power sources, and provide grid support to improve frequency response. Thus, it can overcome the drawbacks of GFL control.

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

## VF Control
<be> VF control is designed to maintain the output voltage amplitude and frequency constant through the closed-loop control, which is often applied in passive power grids, such as islanded grids or uninterruptable power supply (UPS) sys‐ tems. However, due to the constant voltage source characteristic, VF-controlled converter has no power-sharing capability, which cannot operate in active power grids.

<be> For the single-loop control, the converter output voltage Vinv * is generated directly by the frequency reference value ω* and reference value of voltage amplitude V *. While for the dual-loop control, Vinv * is obtained from cascaded voltage and current loops. Thus, the dual-loop control also has the cur‐ rent limiting capability.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/315b8f59-8957-4227-b907-8f5eee2fae57)

## PSL-based GFM control

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/8cb1a99b-aefc-4edd-90c9-ba737281f8e5)

- a) The droop control lacks inertia support capability.
- b) PSC is similar to the droop control. The difference is that the power deviation is used to adjust the frequency in droop control. Due to the lack of inertial emulation, the difference between them will not cause different results
- c) It can be found that due to the existence of LPFs, the inertia term introduces an inertia simulation to the converter dynamic. Thus, the LPF droop control can provide inertia support to suppress the frequency fluctuation of the power grid.
- d) Similar to the principle of current-controlled VSG control, the active power control of VSG control also refers to the swing equation. Hence, VSG converters can simulate the moment of inertia and the damping characteristics of the rotor.
- e) Based on the VSG, the excitation characteristics of SGs have been further considered in the design of synchronverter. Therefore, the synchronverter mimics the operation characteristics of SGs more comprehensively.
- f) By designing the power control as a second-order overdamped system, the SPC can overcome the inherent power oscillation issue of SGs under grid disturbances. Thus, the closed-loop active power control can be further designed as an overdamped system to attenuate the inherent power oscillations of SGs.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/b9580e0e-43ed-4945-97a2-3700f8eff2b8)
