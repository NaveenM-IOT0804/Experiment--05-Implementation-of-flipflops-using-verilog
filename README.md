# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
SR flip flop

SR flip-flop is a gated set-reset flip-flop. The S and R inputs control the state of the flip-flop when the clock pulse goes from LOW to HIGH . The flip-flop will not change until the clock pulse is on a rising edge. When both S and R are simultaneously HIGH, it is uncertain whether the outputs will be HIGH or LOW.

JK flip flop

When both of the inputs of JK flip flop are set to 1 and clock input is also pulse "High" then from the SET state to a RESET state, the circuit will be toggled. The JK flip flop work as a T-type toggle flip flop when both of its inputs are set to 1. The JK flip flop is an improved clocked SR flip flop

Delay flip flop

The Delay flip-flop is designed using a gated SR flip-flop with an inverter connected between the inputs allowing for a single input D(Data). This single data input, which is labeled as "D" used in place of the "Set" input and for the complementary "Reset" input, the inverter is used.

Toggle flip flop

The toggle, or T, flip-flop is a two-input flip-flop . The inputs are the toggle (T) input and a clock (CLK) input. If the toggle input is HIGH, the T flip-flop changes state (toggles) when the clock signal is applied. If the toggle input is LOW, the T flip-flop holds the previous state. T flip-flop symbol.

### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Naveen M
RegisterNumber: 22000748
*/
SR flip flop:

module exp5i(s,r,clk,q, qbar);
input s,r,clk;
output q,qbar;
wire x,y;
nand (x,s,clk);
nand (y,r,clk);
nand (q,x,qbar);
nand (qbar,y,q);
endmodule

JK flip flop:

module jk(j,k,clk,q,qbar);
input j,k,clk;
output q,qbar;
wire x,y;
nand (x, j,clk,qbar);
nand (y,k,clk,q);
nand (q,x,qbar);
nand (qbar,y,q);
endmodule

Toggle flip flop:

module tft(t,clk,q,qbar);
input t,clk;
output q,qbar;
wire s,r;
nand(s,t,clk,qbar);
nand(r,t,clk,q);
nand(q,s,qbar);
nand(qbar,r,q);
endmodule

Delay flip flop:

module delayi(d,clk,q,qbar);
input d,clk;
output q,qbar;
assign dbar=!d;
wire x,y;
nand(x,d,clk);
nand(y,dbar,clk);
nand(q,x,qbar);
nand(qbar,y,q);
endmodule


### RTL LOGIC FOR FLIPFLOPS 

SR flip flop:
![sr](https://user-images.githubusercontent.com/117974950/212672705-129c5af1-b915-40ca-aa85-0b18fbf9901e.png)

JK flip flop:

![jk](https://user-images.githubusercontent.com/117974950/212672933-40c50b8c-dbc1-4a66-8331-466e42910b3e.png)


Toggle flip flop:

![tflipflop](https://user-images.githubusercontent.com/117974950/212673011-20a1f0af-acb0-4fd7-89e1-0bc8138b4e89.png)


Delay flip flop:

![delay](https://user-images.githubusercontent.com/117974950/212673100-8371b622-3b4c-4dba-b06a-c36fdff1dcd8.png)


### TIMING DIGRAMS FOR FLIP FLOPS 

SR flip flop:

![srwaveform](https://user-images.githubusercontent.com/117974950/212673255-a07e133b-444d-4757-8766-09e99785ba31.png)


JK flip flop:

![jkwaveform](https://user-images.githubusercontent.com/117974950/212714175-843de913-28e7-4f70-a92a-5f81cc67a103.png)


Toggle flip flop:

![tfwaveform](https://user-images.githubusercontent.com/117974950/212714206-bb3b58be-a9d1-4b70-9251-8a73c6a1139f.png)

Delay flip flop:

![delaywaveform](https://user-images.githubusercontent.com/117974950/212714289-3c73eeb5-3c46-48ea-ad7d-6fab9f945557.png)


### RESULTS 
Thus the above program is successfully runned
