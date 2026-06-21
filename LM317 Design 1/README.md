# [LM317 Based Current Source]
A fixed current source of 10 mA and 25 mA implemented using LM317.

---

## Key Specifications

### 10 mA Fixed Current Source

| Parameter                   | Value / Range |
| :-------------------------- | :------------ |
| **Input Voltage**           | 12 V DC       |
| **Load Current **           | 10 mA         |
| **Output Voltage Range**    | 0 - 10 V      |
| **Maximum Load Resistance** | 1 k $\Omega$  |

### 25 mA Fixed Current Source

| Parameter                   | Value / Range |
| :-------------------------- | :------------ |
| **Input Voltage**           | 12 V DC       |
| **Load Current **           | 25 mA         |
| **Output Voltage **         | 0 V -  10 V   |
| **Maximum Load Resistance** | 424 $\Omega$  |

##  Schematic


![](Attachments/Schematic.png)

---

## Simulation

![](Attachments/DCAnalysis.png)
DC Analysis

---

##  Results


![](Attachments/Test1.jpg|512)
Fixed current source of 10 mA with 4 LEDs as load

![](Attachments/Test5.jpg|510)
Fixed current source of 25 mA with 3 LEDs as load
### Final Results

| Parameter          | Expected (Calc) | Expected (Sim) | Actual (Measured) |
| :----------------- | :-------------- | :------------- | ----------------- |
| Load Current       | 10 mA           | 10.02 mA       | 10.1 mA           |
| Compliance Voltage | 7.75 V          | 10.25 V        | 10.01 V           |
| Maximum Load       | 775 $\Omega$    | 1.02 k$\Omega$ | 1 k$\Omega$       |

| Parameter          | Expected (Calc) | Expected (Sim) | Actual (Measured) |
| :----------------- | :-------------- | :------------- | ----------------- |
| Load Current       | 25 mA           | 25 mA          | 23.3 mA           |
| Compliance Voltage | 7.75 V          | 10.25 V        | 9.88 V            |
| Maximum Load       | 310 $\Omega$    | 410 $\Omega$   |  424 $\Omega$     |
**Conclusion:** - The mini project was Successful.
- **Key Inference:** The dropout voltage across LM317 was lower than expected due to low load currents, as a result the compliance voltage came out higher than expected in simulations and in actual testing.

---
