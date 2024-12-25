### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

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

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: RegisterNumber:
*/

module synchronous_up_counter (

Input clk, //Clock input

Input reset,

// Reset input (active high)

output reg [3:0] count // 4-bit output

always @(posedge cik or posedge reset) begin

if (reset)

else

end

count < 4'b0000; // Reset the counter to

count < count 1; // Increment the counter

endmodule

**RTL LOGIC UP COUNTER**

![Screenshot 2024-12-25 211546](https://github.com/user-attachments/assets/e393ca4a-8de3-4229-a30e-185c5f28f39b)


**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot 2024-12-25 211556](https://github.com/user-attachments/assets/c986ca57-50b3-49d2-befd-264ac72e0f15)

**TRUTH TABLE**

![Screenshot 2024-12-25 211732](https://github.com/user-attachments/assets/e62da20b-fd27-46d6-9a88-c1056ab2bcf9)


**RESULTS**
Thus the 4 Bit synchronous up counter using Verilog is implemented and validated  their functionality using their functional tables.
