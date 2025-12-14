# ENCODER

AIM:

To implement Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED: Quartus prime

Encoder 8 To 3

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

Truth Table

<img width="657" height="497" alt="Screenshot 2025-12-14 124123" src="https://github.com/user-attachments/assets/cc44da2a-37fd-482a-8caa-976b7483c2e7" />

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

program:

```
module encoder8to4 (
    input wire [7:0] in, // 8 input lines
    output reg [3:0] out // 4 output lines
);

always @(*) begin
    case (in)
        8'b00000001: out = 4'b0000;
        8'b00000010: out = 4'b0001;
        8'b00000100: out = 4'b0010;
        8'b00001000: out = 4'b0011;
        8'b00010000: out = 4'b0100;
        8'b00100000: out = 4'b0101;
        8'b01000000: out = 4'b0110;
        8'b10000000: out = 4'b0111;
        default: out = 4'bxxxx; // Invalid case
    endcase
end
endmodule

```

Logical circuit of the above expressions is given below:
[ex 05 dia.pdf](https://github.com/user-attachments/files/24148188/ex.05.dia.pdf)

waveform:
<img width="1635" height="923" alt="EX 05 wave" src="https://github.com/user-attachments/assets/df753d66-4726-4625-8130-06c8e82a6c03" />

NAME : HEMA PRIYA

REF NO: 25017270

RESULT:

Thus the program was implement Encoder 8 to 3 in Dataflow Modelling using.verilog and validating their functionality using their functional tables.
