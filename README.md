# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */



### PROGRAM 
Up counter:
![ex6UCcode](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/b3459466-a600-4d19-90bd-ccfbeee6d9d7)

Down counter:
![ex6DCcode](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/46d3423c-d1f5-45ce-abad-a705fea5cc84)

/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Visalan H
RegisterNumber: 23007458 
*/
## TRUTHTABLE
Up counter:
![ex6uptt](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/af21e24b-aa9c-4830-83aa-9fa25192e3c1)

Down counter:
![ex6downtt](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/f6237089-17ad-4538-ab92-e9f9dfd04d71)

### RTL REALIZATION
Up counter:
![ex6UCrtl](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/247e5a47-6f20-46af-9ab3-6b7218fbb556)

Down counter:
![ex6DCrtl](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/4753a31b-73e1-4c0f-b859-4e7637a1d141)

### OUTPUT
Up counter:
![ex6bUCoutput](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/e8091ff5-7850-469c-9597-47511b37dd5c)

Down counter:
![ex6DCoutput](https://github.com/Visalan-H/Exp-7-Synchornous-counters-/assets/152077751/970f1869-53bd-4a05-b152-0dfaadb6bed2)


### RESULTS 
HENCE THE OUTPUTS ARE VERIFIED.
