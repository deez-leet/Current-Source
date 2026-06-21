# Design

Schematic

![Schematic](../Attachments/Schematic.png)

$R_{\text{sense}}$ = 250 Ω (Load Current = 20 mA)

$R_{\text{sense}}$ = 500 Ω (Load Current = 10 mA)

Voltage drop across the load resistor is taken as the output voltage, i.e., 

$V_{\text{out}}$ = $V_{\text{in}}$ - $V_{\text{load}}$

Calculated Parameters:

Compliance Voltage = 5.39 V (For load current of 10 mA and 20 mA)

Maximum Load for load current of 10 mA = 539 Ω

Maximum Load for load current of 20 mA = 269.5 Ω

This is assuming that the maximum output voltage of Op-Amp swings 1.61 V less than supply rails (maximum swing from datasheet), which might not be true as this is for a load current of 5 mA. Nevertheless, it gives a rough estimate of the compliance voltage.

# Simulation

![DC Analysis](../Attachments/DC%20Analysis.png)
DC Analysis


![DC Transfer Characteristics1](../Attachments/DC%20Transfer%20Characteristics1.png)
Load Current vs Load Resistance (for 20 mA design)


![DC Transfer Characteristics2](../Attachments/DC%20Transfer%20Characteristics2.png)
Load Current vs Load Resistance (for 10 mA design)


![DC Transfer Characteristics3](../Attachments/DC%20Transfer%20Characteristics3.png)
Output Voltage vs Load Resistance (for 20 mA design)


![DC Transfer Characteristics4](../Attachments/DC%20Transfer%20Characteristics4.png)
Output Voltage vs Load Resistance (for 10 mA design)

The calculated parameters are very close to the simulated results with very slight deviation.

# Bench Testing and Debugging

![Test1](../Attachments/Test1.jpeg)
Two fixed current sources implemented using dual op-amps (LM358)


![Test2](../Attachments/Test2.jpeg)
Load current (left multimeter) and maximum output voltage (right multimeter) for 20 mA design


![Test3](../Attachments/Test3.jpeg)
Load current of 10 mA design with minimum load resistance (No load/short)

![Test4](../Attachments/Test4.jpeg)
Maximum output voltage for the 10 mA design

# Results 

### 10 mA Design
Load Current = 10.2 mA

Compliance Voltage = 5.25 V 

Maximum Load Resistance= 515 Ω

### 20 mA Design
Load Current  = 20.4 mA

Compliance Voltage = 5.12 V 

Maximum Load Resistance = 251 Ω

The implemented designs worked as expected with slight deviation due to component tolerances and limitations. The compliance voltage turned out to be less than expected due to the LM358's output swing being more than than the expected swing. 
