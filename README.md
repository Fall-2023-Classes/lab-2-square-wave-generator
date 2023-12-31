# Lab2_Square_Wave_Generator

[Lab 2 Files](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/tree/main/Lab2Files)

## TOP MODULE
![image](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/assets/47878471/79b2eb9c-759e-43ed-8e19-badd923aa0d9)

Design for a square wave generator with variable *ON* and *OFF* durations depending on 4-bit inputs *m* and *n* respectively. Durations are in intervals of 100ns for both *ON* and *OFF*. The top module includes a [2x1 multiplexer](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/mux_2x1.sv) to select between inputs *m* and *n* inputs using the output *signal*. The output of the MUX is then multiplied by **'d10** before being fed into the [modulus counter](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/modulus_counter.sv) as an input. The Modulus Counter then counts up to the input value and outputs a **Max_Tick** pulse signal to the input of the [T-Flip Flop](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/t_ff.sv). The resulting output of the T-Flip Flop is our generated square wave with custom durations for *ON* and *OFF* times.
  - [TOP Module File](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/t_ff.sv)
    - [TOP Module Test Bench Simulation File](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/SimulationFiles/top_TB.sv)
  - [2x1 MUX file](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/mux_2x1.sv)
  - [Modulus 8-bit Counter File](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/modulus_counter.sv)
  - [T-Flip Flop](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/t_ff.sv)

    
## 2x1 MUX Module
Basic parameterized 2 to 1 multiplexer (in this case: two 4-bit inputs, one 4-bit output).
  - [2x1 MUX file](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/mux_2x1.sv)

## Modulus Counter Module
Modulus counter that increments by 1 every positive edge of the clock with a max count of any 8-bit input.
  - [Modulus 8-bit Counter](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/modulus_counter.sv)
    
## T-Flip Flop Module
Basic T-Flip Flop to toggle the square wave signal based on our counter output (Max_Tick).
  - [T-Flip Flop](https://github.com/Fall-2023-Classes/lab-2-square-wave-generator/blob/main/Lab2Files/DesignFiles/t_ff.sv)

