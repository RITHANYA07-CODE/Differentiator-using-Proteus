## Experiment No: 3
DIFFERENTIATOR USING OP-AMP (μA741)

## Aim
To design and simulate a Differentiator circuit using μA741 in Proteus Design Suite and verify that the output is proportional to the rate of change of input voltage.

## Apparatus Required  
•	μA741 Op-Amp  
•	Capacitor C = 0.01 µF  
•	Resistor Rf = 10 kΩ  
•	Signal Generator  
•	Dual Power Supply (±15V)  
•	CRO / Oscilloscope  
•	Connecting wires  

## Circuit Diagram  
Connection Details:  
•	Input signal → Capacitor (C) → Inverting terminal (Pin 2)  
•	Feedback resistor (Rf) → Between Output (Pin 6) and Pin 2  
•	Non-inverting terminal (Pin 3) → Ground  
•	Pin 7 → +12V  
•	Pin 4 → −12V  

<img width="1195" height="747" alt="image" src="https://github.com/user-attachments/assets/efd8421e-fbd0-46d2-b0e4-7586d72e6339" />

## Theory
A Differentiator circuit produces an output voltage proportional to the rate of change of input voltage.

## Working Principle:  
•	When input changes rapidly → output amplitude increases  
•	When input is constant → output is zero  
•	Output is inverted  

## Procedure  
1.	Open Proteus software.  
2.	Select μA741, capacitor, resistor, signal generator, and CRO.  
3.	Connect circuit in differentiator configuration.  
4.	Apply ±15V power supply.  
5.	Set input sine wave (1V, 1kHz).  
6.	Run simulation.  
7.	Observe input and output waveforms on CRO.
   
## Tabulation

| S.No | Input Signal | Frequency (Hz) | Expected Output                  | Practical Observation              |
|------|-------------|----------------|----------------------------------|-----------------------------------|
| 1    | Sine Wave   | 1 kHz         | Cosine wave (90° phase shift)    | Cosine wave observed              |
| 2    | Square Wave | 1 kHz         | Positive & Negative spikes       | Spikes observed at transitions    |
| 3    | Triangular  | 1 kHz         | Square wave                      | Square wave obtained              |
| 4    | Sine Wave   | 2 kHz         | Higher output amplitude          | Output amplitude increased        |
| 5    | Sine Wave   | 500 Hz        | Lower output amplitude           | Output amplitude decreased        |

## Waveforms  
•	Sine input → Cosine output (90° phase shift)  
•	Square input → Positive & negative spikes  
•	Triangular input → Square wave  

<img width="1380" height="881" alt="image" src="https://github.com/user-attachments/assets/d8d64281-267c-4972-be76-a7c039f2d17b" />

<img width="1600" height="950" alt="image" src="https://github.com/user-attachments/assets/f45f187e-e232-4ba7-9b6f-9505840c6490" />

<img width="1600" height="950" alt="image" src="https://github.com/user-attachments/assets/3e337301-749f-4d5e-bfe1-c8472a3fadd5" />

<img width="1600" height="950" alt="image" src="https://github.com/user-attachments/assets/f9f30f83-9f0c-4711-ba81-64b11b56a453" />


## Result  
The Differentiator circuit using μA741 Op-Amp was successfully designed and simulated in Proteus.  
The output waveform is proportional to the rate of change of input voltage.  
The circuit behaves as a differentiator.  

## Conclusion  
•	Output depends on frequency.     
•	Output leads input by 90° (for sine input).  
•	Higher frequency → Higher output amplitude.  
•	Used in wave shaping and signal processing applications.  

## Viva Questions – Differentiator

### 1. What is a Differentiator?

A Differentiator is an op-amp circuit that produces an output voltage proportional to the rate of change (derivative) of the input voltage.

$$
V_{out} \propto \frac{dV_{in}}{dt}
$$

### 2. Write the output equation of differentiator.

$$
V_{out} = - R_f C \frac{dV_{in}}{dt}
$$

Where:
- $R_f$ = Feedback resistor  
- $C$ = Input capacitor  
- $\frac{dV_{in}}{dt}$ = Rate of change of input voltage  

### 3. Why is output leading input?

The output leads the input because differentiation introduces a 90° phase shift.

For a sinusoidal input:

- Input: $V_{in} = V_m \sin(\omega t)$  
- Output: $V_{out} = V_m \cos(\omega t)$  

Cosine leads sine by 90°, so the output leads the input.

### 4. What happens at very high frequency?

Capacitive reactance is:

$$
X_C = \frac{1}{2\pi f C}
$$

At very high frequency:
- $X_C$ becomes very small
- Gain increases
- Noise is amplified
- Circuit may become unstable

### 5. What is a Practical Differentiator?

A Practical Differentiator is a modified differentiator circuit that includes:

- A resistor in series with the input capacitor
- A capacitor in parallel with the feedback resistor

These components:
- Limit high-frequency gain
- Improve stability
- Reduce noise
