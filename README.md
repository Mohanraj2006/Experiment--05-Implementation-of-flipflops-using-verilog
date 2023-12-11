# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![Screenshot 2023-11-26 164713](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/66a8a670-6496-49b0-bbec-e5ea56ef57e9)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![th](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/8c86c689-0344-483b-893b-d68e76629902)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-22 143002](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/5f0db11d-2d4b-4f79-af79-c93b421851ec)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![Screenshot 2023-11-22 143128](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/55bb4c24-bb18-4439-8cb2-606fc893b8b7)


 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![Screenshot 2023-11-26 204555](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/3abe1f34-e5e5-485d-949b-8919138b2c3e)
![Screenshot 2023-11-26 170739](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/0baa48e0-9b1d-492d-b668-6fa58ff5bcf9)




Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D

![Screenshot 2023-11-26 170721](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/26830adc-ee56-4552-89ab-8a6c4766b13f)
![download](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/08057072-ccbe-4015-89a9-9e1d801af433)



Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![Screenshot 2023-11-26 210428](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/a89546b9-5b7a-40f2-8b2d-352dee604fcc)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![Screenshot 2023-11-26 210447](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/13be69c3-bb57-43b8-a263-3ad35f846afb)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-26 210612](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/ae331c3d-da7f-453d-bfef-2ddbce0e9b10)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 ![download](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/f9c0edf4-6d99-4c12-8676-ad4207e8fbae)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![Screenshot 2023-11-26 204555](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/aa48549c-bf3b-498f-bdeb-67e55fd0d75a)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.


![Screenshot 2023-11-26 170739](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/47d482e3-bebe-454d-9f41-ca379921364b)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![Screenshot 2023-11-26 170721](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/d7f4deb5-fc17-497d-86b3-4de0dbaa116e)

![download](https://github.com/Mohanraj2006/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152195759/9c9d63ff-bf16-415f-ab65-d16a032e25ad)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
