Lin, Yashen, et al. **Research roadmap on grid-forming inverters.** No. NREL/TP-5D00-73476. National Renewable Energy Lab.(NREL), Golden, CO (United States), 2020.
<br>A workshop has been held at the University of Washington the related [Link](https://lowinertiagrids.ece.uw.edu/) is here, the videos of the workshop are available in YouTube as well.

<br>Many of these new resources are connected to the power system through power electronic inverters rather than spinning electromechanical machines. Collectively, we refer to these generation technologies as inverter-based resources.
![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/4cb36517-198a-4f68-83e7-d48e06a9a52d)

<br>Synchronous generators regulate their terminal voltages and respond to a change in grid frequency through a change in its power output; these are traditionally referred to as generator excitation and turbine-governor controls, respectively. These types of primary, secondary, and tertiary controls and voltage control are well-known. We refer to these generation sources as grid-forming. 

<br>Today’s inverter-based generation sources generally use phase-locked loops (PLLs), which rely on externally generated voltages by synchronous machines to operate. We refer to these types of inverter-based generation as grid-following inverters. 

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/3d37b0a0-b386-4d8d-82e4-cf97ba33fefd)

<br>Today’s inverter-based sources, by design, provide lower— sometimes much lower—fault currents. Inverter-based resources, moreover, do not provide the same fault current phasors as traditional machine generators. System protection methods for hybrid power systems, therefore, will need to be re-engineered, accounting for these differing fault currents and conditions.

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/b5007b98-6547-4165-9d1f-677b3d5d77e4)

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/52ae382b-697a-48d9-bdbc-7923dece5ffe)

<br>Droop control: The most well-established grid-forming method is droop control, which was first proposed in the early 1990s (Chandorkar, Divan, and Adapa 1993). Its key feature is that it exhibits a linear trade-off between frequency and voltage versus real and reactive power, much like a typical synchronous machine does in steady state. These so-called “droop laws” are referred to as the P-omega (real power-frequency) and Q-V (reactive power-voltage) relationships, and they give rise to the following properties regardless of whether they are machines or inverters: o System-wide synchronization: All units reach the same frequency. o Power sharing: Each unit provides power in proportion to its capacity (or its programmable droop slope). These properties arise as a result of the networked interactions from the grid and locally programmed droop laws.

<br>Virtual synchronous machines: This approach is based on the emulation of a synchronous machine within the controls of an inverter (Beck and Hesse 2007; Alatrash 2012; Zhong 2016). Specifically, inverter terminal measurements are fed as inputs into a digital synchronous machine model whose emulated dynamics are mapped to the inverter output in real time. The complexity of the virtual machine can vary greatly, from detailed electromechanical models to simplified swing dynamics. Implementations that closely match machine characteristics, possibly even with virtual flux dynamics, have both Q-V and Pomega characteristics and are often called “synchronverters.” On the other end of the spectrum, virtual inertia methods are simpler and capture only the dynamics of an emulated rotor and its steady-state P-omega droop.

<br>Virtual oscillator controllers: In recent years, another inverter control method based on the emulation of nonlinear oscillators has emerged (Johnson et al. 2016a). Much like a virtual synchronous machine, real-time measurements are processed by the digitally implemented model whose output variables modulate the inverter power stage. As illustrated in Figure 4, the key difference is that the model takes the form of an oscillator circuit with a natural frequency that coincides with the nominal AC grid frequency, and its remaining parameters are tuned to adjust the nominal voltage and control bandwidth. Although the virtual oscillator might appear radically different, it has been shown to exhibit the Q-V and P-omega droop laws in steady state.

<br>For machine-based grids, system frequency is intricately tied to the Newtonian mechanics of the rotating generator masses and the speed-governor droop law at each generator. Lower system inertia leads to higher rates of change in frequency.
<br>Inverter-based resources do not contribute inertia to a power system. As traditional resources are replaced with inverter-based resources, system inertia and thus damping is reduced, making the risk of frequency swings higher. In low-inertia systems where frequency deviations could be large, spinning mechanical reserves might not be fast enough to provide primary frequency control

<br>
