# ALU
$$ The Full version of Verilog code which implements the main functions in 32-Bit ALU like And, Or, Addition and Subtractions operations $$


module AndGate (input wire x, y, output reg out);
    always @(*) 
      begin
        out = x & y;
      end
endmodule

module AndGate32Bit (
    input  wire [31:0] num1,
    input  wire [31:0] num2,
    output wire [31:0] AndGate32BitResult,
    output reg         ZeroFlag
);

    // Instantiate 32 ANDGate using 1-Bit AndGate
    AndGate A0(num1[0], num2[0], AndGate32BitResult[0]);
    AndGate A1(num1[1], num2[1], AndGate32BitResult[1]);
    AndGate A2(num1[2], num2[2], AndGate32BitResult[2]);
    AndGate A3(num1[3], num2[3], AndGate32BitResult[3]);
    AndGate A4(num1[4], num2[4], AndGate32BitResult[4]);
    AndGate A5(num1[5], num2[5], AndGate32BitResult[5]);
    AndGate A6(num1[6], num2[6], AndGate32BitResult[6]);
    AndGate A7(num1[7], num2[7], AndGate32BitResult[7]);
    AndGate A8(num1[8], num2[8], AndGate32BitResult[8]);
    AndGate A9(num1[9], num2[9], AndGate32BitResult[9]);
    AndGate A10(num1[10], num2[10], AndGate32BitResult[10]);
    AndGate A11(num1[11], num2[11], AndGate32BitResult[11]);
    AndGate A12(num1[12], num2[12], AndGate32BitResult[12]);
    AndGate A13(num1[13], num2[13], AndGate32BitResult[13]);
    AndGate A14(num1[14], num2[14], AndGate32BitResult[14]);
    AndGate A15(num1[15], num2[15], AndGate32BitResult[15]);
    AndGate A16(num1[16], num2[16], AndGate32BitResult[16]);
    AndGate A17(num1[17], num2[17], AndGate32BitResult[17]);
    AndGate A18(num1[18], num2[18], AndGate32BitResult[18]);
    AndGate A19(num1[19], num2[19], AndGate32BitResult[19]);
    AndGate A20(num1[20], num2[20], AndGate32BitResult[20]);
    AndGate A21(num1[21], num2[21], AndGate32BitResult[21]);
    AndGate A22(num1[22], num2[22], AndGate32BitResult[22]);
    AndGate A23(num1[23], num2[23], AndGate32BitResult[23]);
    AndGate A24(num1[24], num2[24], AndGate32BitResult[24]);
    AndGate A25(num1[25], num2[25], AndGate32BitResult[25]);
    AndGate A26(num1[26], num2[26], AndGate32BitResult[26]);
    AndGate A27(num1[27], num2[27], AndGate32BitResult[27]);
    AndGate A28(num1[28], num2[28], AndGate32BitResult[28]);
    AndGate A29(num1[29], num2[29], AndGate32BitResult[29]);
    AndGate A30(num1[30], num2[30], AndGate32BitResult[30]);
    AndGate A31(num1[31], num2[31], AndGate32BitResult[31]);

    // Zeroflag sets to 1 if result is all zeros
    always @(*) begin
        if (AndGate32BitResult == 32'b0)
            ZeroFlag = 1;
        else
            ZeroFlag = 0;
    end

endmodule


module ORGate (input wire x, y, output reg out);
    always @(*) 
      begin
        out = x | y;
      end
endmodule

module OrGate32Bit (
    input  wire [31:0] num1,
    input  wire [31:0] num2,
    output wire [31:0] Or32BitResult,
    output reg         ZeroFlag
);

    // Instantiate 32 OR gates using 1-Bit ORGate
    ORGate O0(num1[0], num2[0], Or32BitResult[0]);
    ORGate O1(num1[1], num2[1], Or32BitResult[1]);
    ORGate O2(num1[2], num2[2], Or32BitResult[2]);
    ORGate O3(num1[3], num2[3], Or32BitResult[3]);
    ORGate O4(num1[4], num2[4], Or32BitResult[4]);
    ORGate O5(num1[5], num2[5], Or32BitResult[5]);
    ORGate O6(num1[6], num2[6], Or32BitResult[6]);
    ORGate O7(num1[7], num2[7], Or32BitResult[7]);
    ORGate O8(num1[8], num2[8], Or32BitResult[8]);
    ORGate O9(num1[9], num2[9], Or32BitResult[9]);
    ORGate O10(num1[10], num2[10], Or32BitResult[10]);
    ORGate O11(num1[11], num2[11], Or32BitResult[11]);
    ORGate O12(num1[12], num2[12], Or32BitResult[12]);
    ORGate O13(num1[13], num2[13], Or32BitResult[13]);
    ORGate O14(num1[14], num2[14], Or32BitResult[14]);
    ORGate O15(num1[15], num2[15], Or32BitResult[15]);
    ORGate O16(num1[16], num2[16], Or32BitResult[16]);
    ORGate O17(num1[17], num2[17], Or32BitResult[17]);
    ORGate O18(num1[18], num2[18], Or32BitResult[18]);
    ORGate O19(num1[19], num2[19], Or32BitResult[19]);
    ORGate O20(num1[20], num2[20], Or32BitResult[20]);
    ORGate O21(num1[21], num2[21], Or32BitResult[21]);
    ORGate O22(num1[22], num2[22], Or32BitResult[22]);
    ORGate O23(num1[23], num2[23], Or32BitResult[23]);
    ORGate O24(num1[24], num2[24], Or32BitResult[24]);
    ORGate O25(num1[25], num2[25], Or32BitResult[25]);
    ORGate O26(num1[26], num2[26], Or32BitResult[26]);
    ORGate O27(num1[27], num2[27], Or32BitResult[27]);
    ORGate O28(num1[28], num2[28], Or32BitResult[28]);
    ORGate O29(num1[29], num2[29], Or32BitResult[29]);
    ORGate O30(num1[30], num2[30], Or32BitResult[30]);
    ORGate O31(num1[31], num2[31], Or32BitResult[31]);

    // Zeroflag sets to 1 if result is all zeros
    always @(*) begin
        if (Or32BitResult == 32'b0)
            ZeroFlag = 1;
        else
            ZeroFlag = 0;
    end

endmodule

module Half_Adder(input wire x, y, output reg sum, carry);
    always @(*) 
      begin
        sum = x ^ y;
        carry = x & y;
      end
endmodule

module FullAdder1Bit (
    input wire Op1, Op2, Cin,
    output reg Sum, Cout
);

    inout wire sum_first, carry_first, carry_second;

    Half_Adder HA1(Op1, Op2, sum_first, carry_first);
    Half_Adder HA2(sum_first, Cin, Sum, carry_second);
    ORGate OR1(carry_first, carry_second, Cout);

endmodule

module FullAdder32Bit (
    input  wire [31:0] num1,
    input  wire [31:0] num2,
    input  wire       Cin,

    output reg        Cout,
    output reg        OverFlow,
    output reg        ZeroFlag
);

    inout wire [31:0] FullAdder32BitResult;
    inout wire [30:0] carry;

    // implementaion of 1-bit full adders
    FullAdder1Bit FA0(num1[0], num2[0], 1'b0,      FullAdder32BitResult [0], carry[0]);
    FullAdder1Bit FA1(num1[1], num2[1], carry[0],  FullAdder32BitResult [1], carry[1]);
    FullAdder1Bit FA2(num1[2], num2[2], carry[1],  FullAdder32BitResult [2], carry[2]);
    FullAdder1Bit FA3(num1[3], num2[3], carry[2],  FullAdder32BitResult [3], carry[3]);
    FullAdder1Bit FA4(num1[4], num2[4], carry[3],  FullAdder32BitResult [4], carry[4]);
    FullAdder1Bit FA5(num1[5], num2[5], carry[4],  FullAdder32BitResult [5], carry[5]);
    FullAdder1Bit FA6(num1[6], num2[6], carry[5],  FullAdder32BitResult [6], carry[6]);
    FullAdder1Bit FA7(num1[7], num2[7], carry[6],  FullAdder32BitResult [7], carry[7]);
    FullAdder1Bit FA8(num1[8], num2[8], carry[7],  FullAdder32BitResult [8], carry[8]);
    FullAdder1Bit FA9(num1[9], num2[9], carry[8],  FullAdder32BitResult [9], carry[9]);
    FullAdder1Bit FA10(num1[10], num2[10], carry[9],  FullAdder32BitResult [10], carry[10]);
    FullAdder1Bit FA11(num1[11], num2[11], carry[10],  FullAdder32BitResult [11], carry[11]);
    FullAdder1Bit FA12(num1[12], num2[12], carry[11],  FullAdder32BitResult [12], carry[12]);
    FullAdder1Bit FA13(num1[13], num2[13], carry[12],  FullAdder32BitResult [13], carry[13]);
    FullAdder1Bit FA14(num1[14], num2[14], carry[13],  FullAdder32BitResult [14], carry[14]);
    FullAdder1Bit FA15(num1[15], num2[15], carry[14],  FullAdder32BitResult [15], carry[15]);
    FullAdder1Bit FA16(num1[16], num2[16], carry[15],  FullAdder32BitResult [16], carry[16]);
    FullAdder1Bit FA17(num1[17], num2[17], carry[16],  FullAdder32BitResult [17], carry[17]);
    FullAdder1Bit FA18(num1[18], num2[18], carry[17],  FullAdder32BitResult [18], carry[18]);
    FullAdder1Bit FA19(num1[19], num2[19], carry[18],  FullAdder32BitResult [19], carry[19]);
    FullAdder1Bit FA20(num1[20], num2[20], carry[19],  FullAdder32BitResult [20], carry[20]);
    FullAdder1Bit FA21(num1[21], num2[21], carry[20],  FullAdder32BitResult [21], carry[21]);
    FullAdder1Bit FA22(num1[22], num2[22], carry[21],  FullAdder32BitResult [22], carry[22]);
    FullAdder1Bit FA23(num1[23], num2[23], carry[22],  FullAdder32BitResult [23], carry[23]);
    FullAdder1Bit FA24(num1[24], num2[24], carry[23],  FullAdder32BitResult [24], carry[24]);
    FullAdder1Bit FA25(num1[25], num2[25], carry[24],  FullAdder32BitResult [25], carry[25]);
    FullAdder1Bit FA26(num1[26], num2[26], carry[25],  FullAdder32BitResult [26], carry[26]);
    FullAdder1Bit FA27(num1[27], num2[27], carry[26],  FullAdder32BitResult [27], carry[27]);
    FullAdder1Bit FA28(num1[28], num2[28], carry[27],  FullAdder32BitResult [28], carry[28]);
    FullAdder1Bit FA29(num1[29], num2[29], carry[28],  FullAdder32BitResult [29], carry[29]);
    FullAdder1Bit FA30(num1[30], num2[30], carry[29],  FullAdder32BitResult [30], carry[30]);
    FullAdder1Bit FA31(num1[31], num2[31], carry[30],  FullAdder32BitResult [31], Cout);

    always @(*) begin
     

        // Overflow detection logic for signed numbers according to 2's comp
      OverFlow = carry[30] ^ Cout;

        // Zeroflag sets if the result is all zeros
        if (FullAdder32BitResult == 32'b0)
            ZeroFlag = 1;
        else
            ZeroFlag = 0;
    end

endmodule

module NotGate(input wire x, output reg out);
    always @(*) begin
        out = ~x;
    end
endmodule

module Not32Bit(
    input wire [31:0] In,
    output wire [31:0] Out
);

    NotGate N0(In[0], Out[0]);
    NotGate N1(In[1], Out[1]);
    NotGate N2(In[2], Out[2]);
    NotGate N3(In[3], Out[3]);
    NotGate N4(In[4], Out[4]);
    NotGate N5(In[5], Out[5]);
    NotGate N6(In[6], Out[6]);
    NotGate N7(In[7], Out[7]);
    NotGate N8(In[8], Out[8]);
    NotGate N9(In[9], Out[9]);
    NotGate N10(In[10], Out[10]);
    NotGate N11(In[11], Out[11]);
    NotGate N12(In[12], Out[12]);
    NotGate N13(In[13], Out[13]);
    NotGate N14(In[14], Out[14]);
    NotGate N15(In[15], Out[15]);
    NotGate N16(In[16], Out[16]);
    NotGate N17(In[17], Out[17]);
    NotGate N18(In[18], Out[18]);
    NotGate N19(In[19], Out[19]);
    NotGate N20(In[20], Out[20]);
    NotGate N21(In[21], Out[21]);
    NotGate N22(In[22], Out[22]);
    NotGate N23(In[23], Out[23]);
    NotGate N24(In[24], Out[24]);
    NotGate N25(In[25], Out[25]);
    NotGate N26(In[26], Out[26]);
    NotGate N27(In[27], Out[27]);
    NotGate N28(In[28], Out[28]);
    NotGate N29(In[29], Out[29]);
    NotGate N30(In[30], Out[30]);
    NotGate N31(In[31], Out[31]);

endmodule

module Subtractor32Bit (
    input  wire [31:0] A,
    input  wire [31:0] B,
    output wire [31:0] Subtractor32BitResult,
    output wire        Cout,
    output wire        OverFlow,
    output wire        ZeroFlag
);

    inout wire [31:0] B_inverted;

    // Invert B
  Not32Bit invert_B(.In(B), .Out(B_inverted));

    // subtraction main function => A - B = A + (~B + 1)
    FullAdder32Bit subtractor (
        .Op1(A),
        .Op2(B_inverted),
        .Cin(1'b1),
        .FullAdder32Bit(Subtractor32BitResult),
        .Cout(Cout),
        .OverFlow(OverFlow),
        .ZeroFlag(ZeroFlag)
    );

endmodule

module ALU (
    input  [31:0] Op1,
    input  [31:0] Op2,
    input  [3:0]  OpCode,
    input         Cin,
    output reg [31:0] Result,
    output reg        Cout,
    output reg        oFlag,
    output reg        zFlag
);

    always @(*) begin
        // Reset outputs
        Result = 0;
        Cout   = 0;
        oFlag  = 0;
        zFlag  = 0;
					 /*  $$ This part should be edited according to the code design with the team $$ */
      
        case (OpCode)
            4'b0000: begin // AND operation (Op1 AND Op2)
                Result = and_result;
                zFlag = and_zero;
            end
            4'b1111: begin // OR operation (Op1 OR Op2)
                Result = or_result;
                zFlag = or_zero;
            end
            4'b1001: begin // ADD operation (Op1 + Op2)
                Result = FullAdder32Bit;
                Cout = add_cout;
                oFlag = add_of;
                zFlag = add_zero;
            end
            4'b0110: begin // SUBTRACT operation (Op1 - Op2)
                Result = sub_result;
                Cout = sub_cout;
                oFlag = sub_of;
                zFlag = sub_zero;
            end
            default: begin
                // Default case, result is zero if no valid opcode
                Result = 32'b0;
                zFlag = 1; // Default zero flag set to 1
            end
        endcase
    end

endmodule
