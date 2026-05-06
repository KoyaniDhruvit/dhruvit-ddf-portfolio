# 🌐 My Design Logbook – Digital Design & Fabrication Portfolio

## 👤 About the Student
- **Name:** Dhruvit Koyani  
- **Email:** dhruvit.koyani@uni-oldenburg.de
- **University:** Carl von Ossietzky University of Oldenburg
- **Program:** M.Sc. Engineering of Socio-Technical Systems  
- **Matrikelnummer:** 6649717

---

## 📘 Course Information
- **Course:** Digital Design & Fabrication (inf175) 
- **Semester:** Summer Semester 2026    

---

## 📂 Portfolio Overview
This repository documents my learning journey in the **Digital Design & Fabrication** course.

It follows a blog-style structure where each exercise represents a step in the process of transforming digital ideas into physical outcomes.

Each exercise includes:
- Concept exploration  
- Design and workflow steps  
- Fabrication process  
- Reflections and learnings  

This portfolio focuses not only on final results but also on the thinking and iteration behind them.

---

## 🛠 Exercises

### 🧪 Exercise 1:  Electrical Circuits

## 1. Introduction
In this lab, I built and tested five different electrical circuits to explore LED control and transistor switching. This portfolio documents the measurements, observations, and visual results of these experiments.

---

## 2. Task 1: LED Control Circuit

### 2.1 Simple LED Circuit (Task 1.1)
I tested the behavior of a green LED by swapping different resistors ($R1$) to observe changes in current and brightness.

| R1 [Ω] | Measured $V_1$ [V] | Measured $V_{LED}$ [V] |
| :--- | :--- | :--- |
| 220 | 2.28 | 2.86 |
| 1000 | 2.77 | 2.51 |
| 4700 | 2.97 | 2.31 |

**Observations:** 
*As the resistance of $R1$ increased, the brightness of the LED noticeably decreased. and the voltage drop on $R1$ increased as the resistance increased. And also changing $R1$ directly affects the LED's operating voltage and brightness.

**Task 1.1: Simple LED Circuit**
![Simple LED Circuit Setup](./Task_1.1.jpeg)

---

### 2.2 Switchable LED Circuit (Task 1.2) 
I introduced a 2-position switch and a 1kΩ potentiometer to control the state and intensity of the light.

The switch acts as a physical break in the circuit. When the switch is in the "closed" position, the circuit is complete and the LED lights up. When it is "open," the current flow stops and the LED turns off.

When i connect the switch in opposite direction the LED still works exactly the same way because a switch doesn't have a positive or negative side. It doesn't matter which way you plug it in; its only job is to connect or disconnect the two points in the circuit.

**Task 1.2: Switchable LED Circuit**
![Switchable LED Setup](./Task_1.2.jpeg)

### 2.3 Dimmable LED Circuit (Task 1.3) 
**Potentiometer Measurements:**
| Position | $V_{LED}$ [V] | $V_2$ [V] |
| :--- | :--- | :--- |
| **Full Brightness** | 3.01 V | 3.05 V |
| **Dimmed** | 2.30 V | 4.45 V |
| **OFF** | 0.005 V | 4.50 V |

I observed that rotating the potentiometer provides smooth, continuous control over the LED's light intensity. My data shows an inverse relationship between the LED voltage ($V_{LED}$) and the potentiometer output voltage ($V_2$). This is an analog relationship where the potentiometer acts as a variable voltage divider.

**Task 1.3: Dimmable LED Demonstration (Analog)**
<p align="center">
  <a href="https://raw.githubusercontent.com/KoyaniDhruvit/dhruvit-ddf-portfolio/main/Task_1.3.mp4">
    <img src="./thumbnail1.jpg" width="450"/>
  </a>
</p>
---

## 3. Task 2: Transistor Switch Circuit

### 3.1 Switchable LED Strip (Task 2.1)

Using an **IRLZ44N NPN MOSFET**, I controlled a 12V LED strip using a 5V control signal.

I observed a specific behavior regarding the USB power board. When powering the 5V control side via a laptop or mobile device, the voltage was detected and the board functioned as expected. However, when using a direct power adapter, the USB module did not show the same behavior or detection.

**Principle of Operation:**
The MOSFET acts as an electronic switch. When 5V is applied to the **Gate**, it allows current to flow from the **Drain** to the **Source**, completing the 12V circuit for the LED strip.

**Task 2.1: MOSFET Switching Setup**
![MOSFET Circuit Setup](./Task_2.1.jpeg)

---

### 3.2 Dimmable LED Strip (Task 2.2)
I used a PWM generator at 90Hz to observe how the **Duty Cycle** and **Frequency** affect the perceived light.

#### Part A: Duty Cycle ($f = 90\text{Hz}$)
* **2% Duty Cycle:** The light was dim.
* **15% Duty Cycle:** The light was noticeably brighter than at 2%.
* **40% Duty Cycle:** The light reached a moderate level of brightness.
* **75% Duty Cycle:** The light was bright.
* **100% Duty Cycle:** The light was at its maximum brightness.

**Relationship:** I observed a direct linear relationship: as the **Duty Cycle increased**, the **brightness increased** proportionally. 
**Mechanism:** Even though the LED is technically switching ON and OFF rapidly, the eye perceives the average power as a change in intensity.

**Task 2.2: PWM Duty Cycle Setup**
![PWM Setup](Task_2.2.jpeg)

#### Part B: Frequency ($D = 0.5$)
| Frequency [Hz] | Visual Observation |
| :--- | :--- |
| **5 Hz** | Clear and distinct LED flicker/strobing effect. |
| **25 - 45 Hz** | Flicker is still visible but becoming much faster. |
| **60 - 65 Hz** | **Critical Point:** The light almost stops flickering; the pulses become nearly indistinguishable. |
| **100 Hz** | The flicker stops completely; the LED appears as a solid, steady glow. |

**Task 2.2 B: Frequency Observations (Persistence of Vision)**
*   **5 Hz Flicker:** f = 05 Hz.
    ![5Hz Frequency Demo](./Task_2.2_B_45_Hz.mp4)
*   **45 Hz Flicker:** f = 45 Hz.
    ![45Hz Frequency Demo](./Task_2.2_B_5_Hz.mp4)

---

## 4. Conclusion
Through this exercise, I learned the difference between analog dimming (potentiometer) and digital dimming (PWM), as well as the utility of MOSFETs in controlling high-voltage loads with low-voltage signals.
