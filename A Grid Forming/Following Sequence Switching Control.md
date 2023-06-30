Qiu, Weijie, et al. "A Grid Forming/Following Sequence Switching Control Strategy for Supporting Frequency Stability of Isolated Power Grids." 2023 5th Asia Energy and Electrical Engineering Symposium (AEEES). IEEE, 2023.

For an isolated power grid, due to the high penetration of renewable energy, the system inertia is low, and frequency instability is prone to occur after the power grid is disturbed.
<be>At present, most of converters adopt grid following (GFL) control mode and have no inertia control loop, cannot respond to the frequency dynamic process of system and cannot provide inertia support for power grid. In recent years, grid forming (GFM) control has gradually become a main control strategy to solve system frequency problems due to the introduction of control loops that simulate the inertia response of synchronous machines, which has the inertia support capability similar to that of the synchronous machines.

<be>Under a grid following control mode, the higher the renewable energy penetration, the easier the system frequency is to be unstable.
<be>Under a grid forming control mode, the impact on system frequency stability needs to be analyzed according to the specific control strategy and the level of penetration.

<be>In order to give full play to the advantages of grid forming and grid following control modes, A grid forming/following sequence switching control strategy for supporting frequency stability of isolated power grids is proposed in this paper. By dynamically switching the control mode according to different processes of frequency dynamic, the maximum frequency deviation and stabilization time of system can be reduced. Moreover, this sequence switching control strategy only relies on the dynamic characteristics of two different control modes, so there is no need to reserve power capacity in advance.

<be>The advantage of GFL control lies in its fast response speed, which can quickly adjust the active and reactive power output according to the power reference, and the external characteristics presents as a controllable current source. However, because GFL control strategy controls the output current directly, it cannot respond to the frequency dynamic of power grids, and cannot provide inertia supporting for power systems.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/6630e0c1-b92f-45ed-a3c0-5c7e28dce6fd)

<be>GFL control strategy mainly consists of three parts: power outer loop, current inner loop and PLL. The role of PLL is to keep renewable energy synchronized with the power grid. Because of its fast follow-up characteristic, renewable energy cannot respond to the frequency change of the power grid. The power outer loop enables renewable energy to output power according to the given reference power. Most renewable energy operates under the condition of unit power factor and does not output reactive power.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/06381088-881d-4499-9815-67d4b3c138fa)

<be>the voltage outer loop controls the output voltage of converters and generates the inner loop current reference. Since GFM control does not directly control the current, a current limiting loop is required to limit the output current of converters.

<be>Power synchronization loop of GFM mainly consists of two kinds of control modes, namely droop control and virtual synchronous machine (VSG) control,

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/4ec6571d-06f1-4e46-a623-03f9b4e4352d)

<be>Droop control mimics the primary frequency regulation process of synchronous machines. VSG control mimics the inertia response process of synchronous machines, so that it can support the equivalent inertia of power systems.

<be> Through switching different control strategies during different stages, renewable energy can actively support the system frequency. In this paper, a sequence switching control strategy is proposed. When the system frequency response df/dt*Δf>0, GFM control is adopted to increase the equivalent inertia of system to reduce the maximum frequency deviation. When df/dt*Δf<0, GFL control can reduce the time for system frequency to recover to stability by reducing the equivalent inertia of isolated power grid.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/753cdeef-bde5-4ec5-b5c8-2472634f38d9)
