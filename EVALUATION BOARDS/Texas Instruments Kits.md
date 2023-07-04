# TMDSSOLARUINVKIT, Solar Micro Inverter Development Kit

![image](https://github.com/MDerogarian/2023-Summer-Research-Plan/assets/74963406/e480a330-549e-4487-b366-369a358b863b)

https://www.ti.com/tool/TMDSSOLARUINVKIT

## Features (Price 850$) (Single Phase!)
### Hardware Features

- A complete solar-micro-inverter development platform with Isolated DC-DC and DC-AC power stage. Supports panel voltages of 28 to 45V at input. Hence an active clamp flyback DC/DC converter with secondary voltage multiplier is implemented on the board to enable greater efficiency. 100kHz switching is used.
- Universal power output at up to 280W for 220VAC and up to 140W for 110VAC, making it suitable for the diverse requirements of worldwide solar markets. Inverter switches at 50kHz.
<bt> 93 percent peak efficiency and less than four percent total harmonic distortion (THD) provide more power output per solar panel, reducing detrimental heat dissipation and increasing system longevity.
- The C2000 Piccolo F28035 MCU serves as a high-performance controller for the complete micro inverter system, executing high-frequency control loops for both the DC/DC and DC/AC power stages.
- Single MCU system implementation offers design simplicity and reduced system cost.
- Hardware Files are in controlSUITE at development_kits\TMDSSOLARUINVKIT_v100

### Software Features

- Complete software source code, hardware design files and detailed documentation allow designers to see and understand exactly how the design was implemented, creating the foundation to begin their own unique solar power implementations.
- Firmware for closed current loop for DC-DC and DC-AC with DC bus voltage regulation loop, along with MPPT from panel is provided.
- Solar and digital power software libraries provide code-optimized building blocks to implement a variety of power topologies and algorithms such as MPPT and Software Phase Locked Loops (PLL), perfect for designing customized solar inverter solutions.
