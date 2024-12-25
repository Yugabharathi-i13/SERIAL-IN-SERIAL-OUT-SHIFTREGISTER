# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Type the program in Quartus software. 

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram. 

5.For different input combinations generate the timing diagram.

**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming.
~~~
module exp10(clk,sin,q); 
input clk;
input sin;
output [3:0] q; 
reg [3:0] q; 
always @(posedge clk) 
begin  
q[0] <= sin; 
q[1] <= q[0]; 
q[2] <= q[1]; 
q[3] <= q[2]; 
end  
endmodule
~~~

Developed by:Yugabharathi.T RegisterNumber:24900006


**RTL LOGIC FOR SISO Shift Register**

![392214203-12dec3fb-9932-47df-91a4-08b4b0d32cfe](https://github.com/user-attachments/assets/1fc32c6b-6f2f-438e-9295-170152696240)

**TIMING DIGRAMS FOR SISO Shift Register**

![392215485-3f4fc3f2-b8da-4e27-8e50-9ebd1cc484bd](https://github.com/user-attachments/assets/34d9e0b6-75f7-46ab-bdb9-b2dd17b45e44)


**RESULT:**

Thus the SISO shift register is implemented and its functionality is validated in Quartus using Verilog Programming.
