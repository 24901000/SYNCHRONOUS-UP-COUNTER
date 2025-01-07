NAME : BARKAVI.B

REFRENCE NUMBER : 24901000

**EXPERIMENT NUMBER : 11 IMPLEMENTATION OF  SYNCHRONOUS UP COUNTER**



**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
A synchronous up counter is a type of digital counter in which all the flip-flops are triggered simultaneously (in sync) by a common clock signal. It is designed to count upward in a binary sequence, incrementing the count with each clock pulse.

Key Features of a Synchronous Up Counter:
Synchronous Operation:

All flip-flops are triggered at the same time by the same clock signal.
This eliminates the propagation delay associated with asynchronous counters, making synchronous counters faster and more reliable.
Binary Counting:

The counter follows a binary sequence, counting from 000...0 to 111...1 and then rolling over to 000...0 again.
Flip-Flops Used:

Typically constructed using edge-triggered flip-flops, such as JK or D flip-flops.
Control Logic:

Each flip-flop's toggle input is controlled by combinational logic that ensures the correct binary sequence is followed.


A synchronous up counter is a type of digital counter in which all the flip-flops are triggered simultaneously (in sync) by a common clock signal. It is designed to count upward in a binary sequence, incrementing the count with each clock pulse.

Key Features of a Synchronous Up Counter:
Synchronous Operation:

All flip-flops are triggered at the same time by the same clock signal.
This eliminates the propagation delay associated with asynchronous counters, making synchronous counters faster and more reliable.
Binary Counting:

The counter follows a binary sequence, counting from 000...0 to 111...1 and then rolling over to 000...0 again.
Flip-Flops Used:

Typically constructed using edge-triggered flip-flops, such as JK or D flip-flops.
Control Logic:

Each flip-flop's toggle input is controlled by combinational logic that ensures the correct binary sequence is followed.
Working Principle:
Clock Signal: All flip-flops receive the same clock pulse.
Toggle Conditions:
The least significant bit (LSB) toggles on every clock pulse.
Each higher-order flip-flop toggles only when all the lower-order flip-flops are in the 1 state.
Logic Implementation:
For an n-bit counter:
The first flip-flop toggles with every clock pulse.
The second flip-flop toggles when the first flip-flop outputs a 1.
The third flip-flop toggles when both the first and second flip-flops output 1.
This pattern continues for higher-order bits.


**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

write all the steps invloved 

1.Initialize the shift register to a known state (e.g., all zeros).
2.Input a bit serially into the shift register. 
3.Shift the contents of the register oneposition to the right (or left). 
4.Output the shifted bit from the last stage of the register.
5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**


Program for flipflops and verify its truth table in quartus using Verilog programming. 


![Screenshot (129)](https://github.com/user-attachments/assets/79caef0f-ff79-4738-98d3-a3caec009936)

**RTL LOGIC UP COUNTER**


![Screenshot (127)](https://github.com/user-attachments/assets/473e5e9e-d755-4531-9f8d-df5d8274642d)

**TIMING DIAGRAM FOR IP COUNTER**
![Screenshot (128)](https://github.com/user-attachments/assets/acf65e46-d343-4fbe-adc6-1721aa8beb79)

**TRUTH TABLE**
![Screenshot (130)](https://github.com/user-attachments/assets/9a4eada0-64d7-47a1-b2c1-81a133ad5f26)

**RESULTS**

Hence a 4 bit synchronous up counter is implemented correctly.
