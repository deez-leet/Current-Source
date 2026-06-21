Schematic

![Schematic Old](Schematic%20Old.png)
Old Schematic

![Schematic New](Schematic%20New.png)
New Schematic

R$_{sense}$ = 100 Ω (NPN transistor as pass transistor)
R$_{sense}$ = 100 Ω (MOSFET as pass transistor)
Load Current: 0 - 50 mA
V$_{ref}$: 0 - 5 V
V$_{ref}$ linearly controls the load current
Voltage drop across the load resistor is taken as the output voltage, i.e., 
V$_{out}$ = V$_{in}$ - V$_{load}$

Calculated Parameters:
Compliance Voltage = 7 V (for both the designs)
Maximum Load Resistance (at maximum load current) = 140 Ω (for both the designs)
Assuming 0 V drop across the pass transistor at maximum load current. So, the actual compliance voltage will be lower than expected.

# Simulation

![DC Analysis](Attachments/DC%20Analysis.png)
DC Analysis with 2N2222 as one of the pass transistors

![DC Analysis2](Attachments/DC%20Analysis2.png)
DC Analysis with 2N2222 replaced by BC547 as pass transistor

![DC Transfer Characteristics1](Attachments/DC%20Transfer%20Characteristics1.png)
Load Current vs Reference Voltage with 2N2222 as pass transistor

![DC Transfer Characteristics2](Attachments/DC%20Transfer%20Characteristics2.png)
Load Current vs Reference Voltage with IRLZ44N as pass transistor

![DC Transfer Characteristics1(2)](Attachments/DC%20Transfer%20Characteristics1(2).png)
Load Current vs Reference Voltage with BC547 as pass transistor

![DC Transfer Characteristics3](Attachments/DC%20Transfer%20Characteristics3.png)
Load Current vs Load Resistance with 2N2222 as pass transistor (at maximum load current of 50 mA)

![DC Transfer Characteristics5](Attachments/DC%20Transfer%20Characteristics5.png)
Load Current vs Load Resistance with IRLZ44N as pass transistor (at maximum load current of 50 mA)

![DC Transfer Characteristics 3(2)](Attachments/DC%20Transfer%20Characteristics%203(2).png)
Load Current vs Load Resistance with BC547 as pass transistor (at maximum load current of 50 mA)

![DC Transfer Characteristics4](Attachments/DC%20Transfer%20Characteristics4.png)
Output Voltage vs Load Resistance with 2N2222 as pass transistor (at maximum load current of 50 mA)

![DC Transfer Characteristics6](Attachments/DC%20Transfer%20Characteristics6.png)
Output Voltage vs Load Resistance with IRLZ44N as pass transistor (at maximum load current of 50 mA)

![DC Transfer Characteristics4(2)](Attachments/DC%20Transfer%20Characteristics4(2).png)
Output Voltage vs Load Resistance with BC547 as pass transistor (at maximum load current of 50 mA)

The simulations provided satisfactory results. The compliance voltage came out slightly lower than calculated due to a small voltage drop across the pass transistor.

# Bench Testing and Debugging

![Test1](Test1.jpeg)
Load Current (left multimeter) at maximum reference voltage (right multimeter) with 2N2222 as pass transistor

![Test2](Test2.jpeg)
![Test3](Test3.jpeg)
![Test4](Test4.jpeg)
Latched Load Currents at different reference voltages

The load current doesn't follow the reference voltage below a certain value. The load current would latch when the reference voltage would drop below a certain value and it would remain latched until the reference voltage was increased beyond the threshold. Furthermore, the latched current was also not fixed, in one case it was around 18 mA and in another it was around 27 mA. This made the current source inconsistent at lower reference voltages. This issue occurred only with 2N2222 as a pass transistor. Reason for this behavior couldn't be explained. Thus, the design with 2N2222 as a pass transistor was discontinued and it was replaced with BC547. 

![Test7](Test7.jpeg)
Load Current (left multimeter) at maximum reference voltage (right multimeter) with BC547 as pass transistor

![Test6](Test6.jpeg)
Load Current (left multimeter) at minimum reference voltage (right multimeter) with BC547 as pass transistor

![Test8](Test8.jpeg)
Maximum load current (left multimeter) with minimum load (no load/short) with BC547 as pass transistor

![Test9](Test9.jpeg)
Maximum load current (left multimeter) with maximum load resistance with BC547 as pass transistor

Here, BC547 had no issues and the design worked as expected.

![Test13](Test13.jpeg)
Load Current (left multimeter) at minimum reference voltage (right multimeter) with IRLZ44N as pass transistor

![Test14](Test14.jpeg)
Load Current (left multimeter) at maximum reference voltage (right multimeter) with IRLZ44N as pass transistor

![Test10](Test10.jpeg)
Maximum load current (left multimeter) with maximum load resistance with IRLZ44N as pass transistor

![Test12](Test12.jpeg)
Maximum load current (left multimeter) with minimum load (no load/short) with IRLZ44N as pass transistor

![Test11](Test11.jpeg)
Load Current with load resistance crossing the limit with IRLZ44N as pass transistor

# Results

### 2N2222 as Pass Transistor
Maximum Load Current = 49.8 mA (at reference voltage = 5 V)
Minimum Load Current  is inconsistent
Design discontinued
### BC547 as Pass Transistor
Maximum Load Current = 51.2 mA (at reference voltage = 5 V)
Minimum Load Current  = 0 mA (at reference voltage  = 0 V)
The load current was linearly controlled by the reference voltage from 0 - 5 V
Compliance Voltage = 6.38 V (at maximum load current of 50 mA)
Maximum Load Resistance = 125 Ω (at maximum load current of 50 mA)

### IRLZ44N as Pass Transistor
Maximum Load Current = 51.4 mA (at reference voltage = 5 V)
Minimum Load Current  = 0 mA (at reference voltage  = 0 V)
The load current was linearly controlled by the reference voltage from 0 - 5 V
Compliance Voltage = 6.92 V (at maximum load current of 50 mA)
Maximum Load Resistance = 135 Ω (at maximum load current of 50 mA)

Despite issues with 2N2222 as a pass transistor, the remaining designs worked as expected. The linear control of the load current worked very well. The maximum load current was slightly higher than expected (1 mA deviation), nonetheless the results were satisfactory.





