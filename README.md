# DFlipFlop
# D-FLIPDLOP-NEGEDGE
# AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

<img width="952" height="392" alt="image" src="https://github.com/user-attachments/assets/b23fc534-eeb5-42c6-887b-904ecfb85a43" />

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

<img width="466" height="172" alt="image" src="https://github.com/user-attachments/assets/3dc477e3-e47c-4700-9c1c-e0ae8af3edde" />

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

<img width="492" height="291" alt="image" src="https://github.com/user-attachments/assets/252e86a3-a599-42b4-aaac-497afbd734aa" />
Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

Procedure

# PROGRAM
```
module DFlipFlop(
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule

```

# Developed by: BUSHPIKA C
# RegisterNumber: 25007434

# RTL LOGIC FOR FLIPFLOPS
<img width="1920" height="1080" alt="Screenshot 2025-12-15 114329" src="https://github.com/user-attachments/assets/f690c190-5703-48fa-9ba7-6dc15cf15c18" />


# TIMING DIGRAMS FOR FLIP FLOPS
<img width="1920" height="1080" alt="Screenshot 2025-12-15 154758" src="https://github.com/user-attachments/assets/84c537a7-8bab-44bf-8775-e38ec2b38297" />

# RESULTS
Thus the program has been executed successfully
