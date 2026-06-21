# [Howland Current Pump]
A fixed current source of 5 mA is implemented using Howland current pump with an improvement in input impedance.

---

## Key Specifications

### 5 mA Howland Current Pump

| Parameter                   | Value / Range  |
| :-------------------------- | :------------- |
| **Input Voltage Supply**    | 12 V DC        |
| **Reference Voltage**       | 5 V DC         |
| **Load Current **           | 5 mA           |
| **Output Voltage Range**    | 0 - 5.3 V      |
| **Maximum Load Resistance** | 1.03 k$\Omega$ |

##  Schematic


![Schematic1New](Schematic1New.png)
Howland Current Pump with very low input impedance


![Schematic2New](Schematic2New.png)
Howland Current Pump with very high input impedance

---

## Simulation


![DC Analysis New](Attachments/DC%20Analysis%20New.png)
DC Analysis

---

##  Results

![Test10](Test10.jpeg)
Improved Howland Current Pump driving a LED
### Final Results

| Parameter          | Expected (Calc) | Expected (Sim) | Actual (Measured) |
| :----------------- | :-------------- | :------------- | ----------------- |
| Load Current       | 5 mA            | 5.01 mA        | 5.1 mA            |
| Compliance Voltage | 5.195 V         | 5.3 V          | 5.3 V             |
| Maximum Load       | 1.039 k$\Omega$ | 1.05 k$\Omega$ | 1.039 k$\Omega$   |

**Conclusion:** - The mini project was Successful.
- **Key Inference:** The poor input impedance of the original Howland current pump can be improved by adding a buffer stage (i.e., a voltage follower) for the reference voltage and thus the input impedance increases significantly (Input Impedance will be equal to input impedance of voltage follower).

---
