# Energy-Efficient Analog Integrated Circuits (EEAIC)

This repository contains advanced analog and mixed-signal integrated circuit design projects implemented in **TSMC 65 nm CMOS technology**, developed as part of the advanced Master's course Energy-Efficient Analog Integrated Circuits (EEAIC) at ETH Zürich. The assignments explore the design, optimization, and rigorous simulation (including PSS, PNOISE, and PSTB analyses) of high-performance analog systems, with a focus on power efficiency and precision.

While this repository serves as a comprehensive portfolio of coursework, the following three projects represent the primary architectural designs:

### 1. Chopper-Stabilized Precision Sensor Interface (65 nm)

* **Architecture:** Designed an inverter-based fully differential amplifier utilizing chopper stabilization to eliminate low-frequency artifacts and flicker noise by shifting the signal to a higher frequency.
* **Feedback & Impedance:** Integrated pseudo-resistors to achieve a 10 GΩ feedback resistance.
* **Impedance Boosting:** Implemented a capacitive positive feedback loop specifically designed to boost the input impedance of the chopper-stabilized amplifier.

**[🔗 View Chopper-Stabilized Amplifier PDF](./03_chopper_stabilized_amp/ASS_3_EEAIC.pdf)**.

### 2. Successive-Approximation Switched-Capacitor DC-DC Converter (65 nm)

* **Architecture:** Designed a high-resolution 4-stage step-down SAR SC converter utilizing 2:1 interleaved switched-capacitor cells to generate $2^N$ voltage levels.
* **Specifications:** Operates from a 2.4V input, providing a programmable nominal output ranging from 0.15V to 2.4V in fine-grained 150mV increments.
* **Performance:** Designed custom phase-generation buffer chains and capacitive level shifters to minimize switching losses, targeting a peak efficiency greater than 85% for a 1.8V output.

**[🔗 View SAR SC DC-DC Converter PDF](./06_SAR_DC_DC/ASS_6_EEAIC.pdf)**

### 3. Phase-Locked Loop (PLL) and Voltage-Controlled Oscillators (65 nm)

* **Architecture:** Designed a Class-B LC VCO for a Charge Pump PLL designed to multiply a 25 MHz reference frequency up to a 2 GHz output.
* **Frequency Tuning:** Engineered digitally switching capacitor banks containing an analog-controlled MOSCAP, linearly/binary weighted MOSCAPs, and binary-weighted MOMCAPs to ensure a ±5% tuning range without tuning holes.
* **Noise Optimization:** Conducted periodic steady-state and phase noise analyses to size the cross-coupled pair (XCP) and tank capacitance, achieving a Figure of Merit (FoM) of -187 dBc/Hz at a 100 kHz offset.

**[🔗 View PLL and VCO PDF](./08_classB_LC_VCO_PLL/ASS_8_EEAIC.pdf)**

---

*(Note: Additional assignments and core component designs are uploaded on an ongoing basis.)*

## Tools & Methodologies

* **EDA Tools:** Cadence Virtuoso (ADE Maestro, Layout XL)
* **Analyses:** Transient, Periodic Steady-State (PSS), Periodic Noise (PNOISE), Periodic AC (PAC), and Stability (PSTB)
* **Technology:** TSMC 65 nm CMOS
