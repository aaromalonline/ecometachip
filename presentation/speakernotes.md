

### **Presentation Strategy**
*   **Track:** Agriculture and Food Technology / Analytical Instrumentation.
*   **Time:** 12 Minutes Presentation + 3 Minutes Q&A.
*   **Visual Style:** Big images, bold lines, massive font (18pt+), almost zero text.

---

### **Slide 1: Title Slide**

**[Visual Area]**
*(Insert High-Res Photo of the Eco-MetaChip Prototype)*

**[Text Area - Centered]**
**Eco-MetaChip Mini: Sustainable Liquid Identification via Coir-Rubber Dielectric Resonators**

*Aaromal A, Abhiram B, Devanarayanan C.R, Ivana A.K*
*(CUSAT, India)*

**(Word Count: 16 words)**

> **Speaker Notes:** Good morning. I am presenting the Eco-MetaChip Mini. This is a low-cost, biodegradable system designed to identify liquids like water, ethanol, and petrol based on their dielectric properties. It utilizes a novel material developed at CUSAT.

---

### **Slide 2: The Problem**

**[Visual Area]**
*(Split screen image: Left side showing expensive lab equipment with a red "X" over it. Right side showing a drop of dirty water/fuel with a green checkmark.)*

**[Text Area]**
**"Need for low-cost, biodegradable sensing for field analysis."**

**(Word Count: 9 words)**

> **Speaker Notes:** Current liquid analysis requires expensive spectroscopy or chromatography. We needed a solution that is portable, resource-constrained, and eco-friendly for applications like detecting water in fuel or testing environmental samples.

Benchtop Benchtop FT-IR Spectrometers (example)
This is the "heavy machinery" most industries use to identify liquids (oils, chemicals, pollutants).

The Machine: Systems like the Thermo Scientific Nicolet or PerkinElmer Spectrum 3.

Why it's "Non-Eco Friendly": These require high power consumption and often use internal components made of rare-earth elements or toxic materials (like Mercury Cadmium Telluride detectors).

The Bulk: They weigh 30–60 kg and are strictly laboratory-bound. You cannot take them to a rural field or a factory floor easily.

Problem Statement Angle: "Industrial liquid ID currently requires moving the sample to a 50kg machine; we move the sensor to the sample."

---

### **Slide 3: Materials Required**

Power Source - 3 V CR2032 cell
Sensing Element - 30 mm×30 mm×2 mm Coir-Rubber Patch
Oscillator Frequency (fo) ≈100 MHz
Toroidal Inductor (L1) - 15 Turns, 8 mm OD, 54nH
Oscillator Capacitor (C1) - 47 pF NPO Ceramic
Oscillator/Driver (Q1, Q2) - 2N3904 NPN Transistor
Rectifier Diodes (D1–D4) - 1N4148 Silicon Diodes (4 ns recovery)
Filter Capacitor - 100 µF Electrolytic
Output LED Resistors - 1 kΩ (R5, R6, R7)

### **Slide 4: The Novel Material**

**[Visual Area]**
*(Insert the SEM Micrograph of the Coir-Rubber Composite from Source showing the porous structure.)*

**[Text Area]**
**"Coir-Rubber Composite: Porous matrix allows liquid integration."**

**(Word Count: 8 words)**

> **Speaker Notes:** The core innovation is this material. It is a composite of 60% Coconut Coir, 30% Rubber, and 10% Carbon. Unlike standard PCBs, this is porous. The liquid fills these voids, drastically changing the material's electromagnetic properties.

---

### **Slide 5: System Architecture**

**[Visual Area]**
*(Block Diagram: [Oscillator] $\xrightarrow{\text{Magnetic Field}}$ [Coir Patch] $\xrightarrow{\text{Coupling}}$ [Pickup Coil] $\xrightarrow{\text{Rectifier}}$ [LEDs])*

**[Text Area]**
**"100 MHz Hartley Oscillator coupled with dielectric resonator."**

**(Word Count: 8 words)**

> **Speaker Notes:** Here is the system architecture. We generate a 100 MHz magnetic field using a Hartley Oscillator. The Coir-Patch acts as a "secondary resonator." We do not touch the liquid; we pick up the signal wirelessly using a secondary coil.

---

### **Slide 6: The Physics (Dielectric Loading)**

**[Visual Area]**
*(Large Equation)*
$$ f_0 \propto \frac{1}{\sqrt{LC}} $$
*(Diagram showing water ($\epsilon_r=80$) creating high capacitance vs. Petrol ($\epsilon_r=2$) creating low capacitance.)*

**[Text Area]**
**"Liquid permittivity alters capacitance, modulating magnetic field amplitude."**

**(Word Count: 8 words)**

> **Speaker Notes:** How does it work? The resonant frequency depends on Inductance and Capacitance. Water has a permittivity of 80; Petrol is roughly 2. When water hits the patch, it increases the effective capacitance, loading the oscillator and changing the amplitude of the magnetic field we detect.

---

### **Slide 7: Circuit Implementation**

**[Visual Area]**
*(Clean Schematic of the circuit. Highlight the Bridge Rectifier section.)*

**[Text Area]**
**"Fast-recovery diodes rectify RF signals to DC voltage."**

**(Word Count: 9 words)**

> **Speaker Notes:** This is the circuit. A critical design choice was the bridge rectifier. We used 1N4148 diodes with a 4-nanosecond recovery time. Standard diodes failed here because they cannot rectify a 100 MHz signal efficiently.

---

### **Slide 8: Addressing Signal Loss**

**[Visual Area]**
*(Graph from Source showing Absorption vs. Frequency, or a simple diagram of "Reflection vs. Absorption".)*

**[Text Area]**
**"Carbon content optimized for coupling, not just absorption."**

**(Word Count: 8 words)**

> **Speaker Notes:** We faced a challenge: Carbon-rubber is usually a radio wave absorber. However, by controlling the thickness to 2mm and the carbon ratio, we turned it into a coupling element. Instead of blocking the signal, the material now "tunes" the signal based on the liquid present.

---

### **Slide 9: Experimental Results**

**[Visual Area]**
*(Bar Chart: Y-axis = DC Voltage (mV). Bars for Air (45mV), Petrol (70mV), Ethanol (190mV), Water (260mV). Bold text on bars.)*

**[Text Area]**
**"Higher permittivity liquids generate significantly higher output voltages."**

**(Word Count: 9 words)**

> **Speaker Notes:** These are our results. Air gives a baseline of 45mV. Petrol shifts it slightly to 70mV. But look at Water—it jumps to 260mV. This distinct voltage separation allows us to easily classify the liquids.

---

### **Slide 10: Visual Classification**

**[Visual Area]**
*(Photo or Table showing:
Water = **BLUE** LED
Ethanol = **GREEN** LED
Petrol = **RED** LED)*

**[Text Area]**
**"Three-level LED output based on voltage thresholds."**

**(Word Count: 8 words)**

> **Speaker Notes:** We translated those voltages into a simple visual interface. We use the forward voltage drops of LEDs. Water triggers the Blue LED (highest threshold). Ethanol triggers Green. Petrol only triggers Red. It's an instant "traffic light" system for chemical purity.

---

### **Slide 11: Conclusion & References**

**[Visual Area]**
*(Photo of the final device working with a battery.)*

**[Text Area]**
**"Eco-friendly, low-power solution for real-time liquid analysis."**

**(Word Count: 8 words)**

> **Speaker Notes:** In conclusion, the Eco-MetaChip Mini proves we can use agricultural waste to build high-tech sensors. It is low cost, runs on a coin cell, and effectively distinguishes liquids. Thank you.

---

### **Checklist for APSCON Compliance:**
1.  **Words:** No slide has more than 16 words (Rule: <20).
2.  **Fonts:** Ensure all text in the "Visual Area" (like graph axes) is **18pt or larger**.
3.  **Contrast:** Make the graph lines **bold** and contrasting (e.g., bright blue bars on white background).
4.  **Backup:** Save as PPTX with **fonts embedded**, and carry a PDF version on a USB stick.
