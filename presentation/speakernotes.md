

### **Presentation Strategy**
*   **Track:** Agriculture and Food Technology / Analytical Instrumentation.
*   **Time:** 12 Minutes Presentation + 3 Minutes Q&A.
*   **Visual Style:** Big images, bold lines, massive font (18pt+), almost zero text.

---


#### **Slide 1: Title Slide**
*   **Visual Content:**
    *   *Image:* APSCON 2026 Background.
    *   *Text:* "Ecometachip-Mini: A Low-Cost, Eco-Friendly Chemical Identifier Utilizing a Novel Coir-Rubber Dielectric Sensor".
*   **Speaker Notes:**
    "Good morning, everyone, and welcome to our presentation. Today, we are introducing the Eco-MetaChip Mini. This is a low-cost, eco-friendly chemical identifier that utilizes a novel coir-rubber dielectric sensor. This project was developed to provide a sustainable alternative for preliminary liquid identification."

#### **Slide 2: Abstract & Authors**
*   **Visual Content:**
    *   *Text:* "Abstract: This paper presents the Eco-MetaChip Mini, a novel, low-cost, and eco-friendly system for the preliminary identification of common liquids based on changes in their relative permittivity ($\epsilon_r$) using a novel rubber coir material."
    *   *Text:* "Authors: Abhiram B, Aaromal A, Devanarayanan CR, Ivana Anto. Affiliation: School of Engineering, CUSAT (Kerala, India)".
*   **Speaker Notes:**
    "This work is a collaborative effort by our team at the School of Engineering, Cochin University of Science and Technology (CUSAT). Our system identifies common liquids by measuring changes in their relative permittivity using a biodegradable rubber-coir patch. We aim to replace expensive, complex traditional sensors with a highly resource-constrained alternative."

#### **Slide 3: The Problem**
*   **Visual Content:**
    *   *Image:* Benchtop FT-IR Spectrometer.
    *   *Text:* "Need for low-cost, biodegradable sensing for field analysis."
*   **Speaker Notes:**
    "The primary motivation for this work is the high barrier to entry in chemical sensing. Currently, identifying liquids requires bulky, expensive equipment like FT-IR or chromatographic spectrometers. There is a critical need for a low-cost, portable, and biodegradable solution that can be deployed directly in the field for applications like detecting water in fuel or industrial quality control."

#### **Slide 4: Materials Required**
*   **Visual Content:**
    *   *Image:* Table showing Component, Specification, and Quantity (Coir-Rubber substrate, Copper Coils, 2N3904 Transistors, etc.).
*   **Speaker Notes:**
    "To solve this, we designed a highly resource-constrained system. As you can see in the table, the entire setup can be built on a standard breadboard using off-the-shelf components. We use standard 2N3904 NPN transistors for the oscillator and fast-recovery Schottky diodes for RF rectification. The only specialized, novel component is our proprietary 30x30mm coir-rubber substrate."

#### **Slide 5: System Architecture**
*   **Visual Content:**
    *   *Image:* Block Diagram (DC source $\rightarrow$ Hartley oscillator $\rightarrow$ coir patch $\rightarrow$ Pickup coil $\rightarrow$ precision rectifier $\rightarrow$ amplifier $\rightarrow$ LEDS).
    *   *Text:* "100 MHz Hartley Oscillator coupled with dielectric resonator."
*   **Speaker Notes:**
    "Here is our system architecture. A 3V DC source powers a Hartley oscillator to generate a 100 MHz RF magnetic field. The coir patch sits within this field. As the patch's permittivity changes due to the liquid, it modulates the magnetic field amplitude. A secondary pickup coil captures this non-contact signal, which is then passed through a precision rectifier and amplifier to drive an LED classification array."
    
#### **Slide 6: The Novel Material**
*   **Visual Content:**
    *   *Image:* Scanning electron microscopy of CoR and CoRC.
    *   *Text:* "Coir-Rubber Composite: Porous matrix allows liquid integration."
*   **Speaker Notes:**
    "The core of our innovation is this coir-rubber composite, developed by Dr. Anju Pradeep at CUSAT. It is made of 60% coir fiber, 30% nitrile rubber, and 10% carbon/copper filler. The SEM images on the slide show its highly porous matrix. When a liquid droplet is placed on the patch, it replaces the air inside these pores, causing a massive, measurable shift in the material's effective dielectric constant."

#### **Slide 7: Methodology/Physics (Dielectric Loading)**
*   **Visual Content:**
    *   *Image:* Equation $f_o \propto 1/\sqrt{LC}$.
    *   *Text:* "Liquid permittivity alters capacitance, modulating magnetic field amplitude."
*   **Speaker Notes:**
    "The physics behind this modulation relies on dielectric loading. The resonant frequency of our oscillator is inversely proportional to the square root of inductance and capacitance. When a high-permittivity liquid like water (with an $\epsilon_r$ of roughly 80) enters the patch, it significantly increases the effective capacitance of the system. This alters the resonance and modulates the amplitude of the magnetic field captured by our secondary coil."

#### **Slide 8: Addressing Signal Loss**
*   **Visual Content:**
    *   *Image:* Waveguide Method Graphs showing Reflection, Transmission, and Absorption.
    *   *Text:* "Carbon content optimized for coupling, not just absorption."
*   **Speaker Notes:**
    "During development, we had to carefully engineer the material to prevent total signal loss. Normally, rubber composites mixed with carbon are highly efficient radio wave absorbers, as seen in the severe drop in transmission in these graphs. By optimizing the patch to a 2mm thickness and controlling the carbon ratio, we ensured the material couples the near-field rather than dissipating it entirely as heat."

#### **Slide 9: Circuit Implementation**
*   **Visual Content:**
    *   *Image:* LTSpice Schematic showing the oscillator, inductive coupling (`k_val`), and precision rectifier.
*   **Speaker Notes:**
    "This is our circuit implementation. On the left is the Hartley oscillator. The gap shown represents the 2-millimeter non-contact air gap, where the rubber-coir substrate acts as the coupling medium. We step the coupling parameter `k_val` in our simulations to mimic different liquids. Fast-recovery diodes with a 4-nanosecond recovery time are absolutely critical here to efficiently rectify the 100 MHz RF signal into a usable DC voltage."

#### **Slide 10: Simulation Results**
*   **Visual Content:**
    *   *Image:* LTSpice waveform plots (Pre-Amplification and Post-Amplification output).
*   **Speaker Notes:**
    "Our LTSpice simulations verified the theory. In the top plot, you can see the pre-amplification DC output from the precision rectifier. As we step the coupling coefficient to mimic liquids of increasing permittivity, the output voltage splits into distinct, measurable levels. The bottom plot shows these levels after amplification, confirming we have enough separation to drive our visual LED logic."

#### **Slide 11: Experimental Observations**
*   **Visual Content:**
    *   *Image:* Table comparing Water, Ethanol, Coconut Oil, and Petrol with Mean $V_{dc}$.
    *   *Text:* "Higher permittivity liquids generate significantly higher output voltages."
*   **Speaker Notes:**
    "Our experimental results perfectly mirror the simulations. We tested 50-microliter droplets of liquids with vastly different dielectric constants. Petrol, with a very low permittivity of 1.9, yielded a mean output of 72 millivolts. Coconut oil gave 86 millivolts. Ethanol jumped to 184 millivolts, and Water, with a permittivity of 80, generated the highest output at 262 millivolts."

#### **Slide 12: Repeatability**
*   **Visual Content:**
    *   *Image:* Plots showing "Output Consistency across Variable Humidity" and "Thermal Stability Analysis".
*   **Speaker Notes:**
    "For a field sensor, environmental robustness is key. We tested the Eco-Metachip across varying humidity levels from 32% to 86% and found an incredibly low drift of just 0.04 millivolts per percentage of relative humidity. Similarly, thermal stability tests between 25 and 29 degrees Celsius showed a minimal drift of 0.50 millivolts per degree. The output remains highly consistent."

#### **Slide 13: Sensitivity**
*   **Visual Content:**
    *   *Image:* Scatter Plot "Eco-Metachip Sensitivity Analysis ($V_{dc}$ vs. $\epsilon_r$)".
*   **Speaker Notes:**
    "Plotting the pre-amplification DC voltage output against the known dielectric constants of the samples reveals a strong linear sensitivity. We achieved a sensitivity fit of 2.31 millivolts per unit of relative permittivity, with an $R^2$ score of 0.906. This level of linearity and distinct separation is exceptional for a low-cost, analog diagnostic tool."

    (R^2 value is a mathematical score (usually around $0.99$) that shows how close your red dots are to the dashed line.This proves your sensor is Predictable. If the $R^2$ is high, it means you don't need complex AI to identify the liquid; a simple linear equation ($y = mx + c$) is enough.)
    (The small red lines extending above and below your data points represent the Uncertainty or "noise" in your readings across different test sessions.)
    (The dashed line shows the mathematical relationship between your input (e.g., Dielectric Constant $\epsilon_r$) and your output (Voltage $V_{dc}$). It "smooths out" the minor variations caused by noise or experimental error to show the general trend of the sensor. The linear curve fn can be used to predict permitivity change of read Vdcs in classification.)

#### **Slide 14: Exp-Setup & Visual Classification**
*   **Visual Content:**
    *   *Image:* Equation $V_{DC} \propto \Delta\epsilon_r \propto$ Number of Illuminated LEDs, alongside physical prototype photos with multimeter.
    *   *Text:* "Three-level LED output based on voltage thresholds."
*   **Speaker Notes:**
    "Here is the physical prototype showing the 2mm non-contact air gap. We mapped the linear DC output directly to a simple visual interface using the natural forward voltage drops of LEDs. Petrol only produces enough voltage to dimly light the Red LED. Ethanol lights Red and Green. Water generates enough voltage to trigger the highest threshold, lighting Red, Green, and Blue simultaneously."

#### **Slide 15: Conclusion & References**
*   **Visual Content:**
    *   *Text:* "Eco-friendly, low-power solution for real-time liquid analysis."
    *   *Image:* List of references (Pradeep, Lide, Young).
*   **Speaker Notes:**
    "In conclusion, the Eco-MetaChip Mini proves that we can utilize biodegradable agricultural waste to build highly effective, non-contact liquid sensors. It runs on very low power (a single 3V coin cell) and provides real-time, visual chemical classification. Thank you for your time, and we would like to acknowledge Prof. Dr. Anju Pradeep for her foundational work. I am now open to questions."

### **Slide 15 : Future Work - MCU integration and ML models for digital classification mapping permittivity to voltage variations**

* **Speaker Notes (How to verbalize it during the presentation):**
"Currently, our system outputs an analog DC voltage between 0 and 300 millivolts to drive a visual LED interface. However, as outlined in our paper's future scope, we plan to transition to a quantitative digital output stage. 

To achieve this, we will implement a hardware MCU bridge. We will use an operational amplifier to boost our millivolt output to a standard 3.3V logic level, incorporating a DC clamper to ensure a strictly positive signal for the microcontroller's ADC. Once digitized, we will utilize machine learning—specifically, models developed via Scikit-Learn (sklearn)—deployed on the MCU. 

By training this ML model on the extensive dataset of **relative permittivity** ($\epsilon_r$) versus $V_{DC}$ variations we have already collected, the device will move from simple thresholding to highly accurate, digital chemical classification. 

### **Checklist for APSCON Compliance:**
1.  **Words:** No slide has more than 16 words (Rule: <20).
2.  **Fonts:** Ensure all text in the "Visual Area" (like graph axes) is **18pt or larger**.
3.  **Contrast:** Make the graph lines **bold** and contrasting (e.g., bright blue bars on white background).
4.  **Backup:** Save as PPTX with **fonts embedded**, and carry a PDF version on a USB stick.
