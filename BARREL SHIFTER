`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 23.12.2024 16:52:54
// Design Name: 
// Module Name: BARREL_SHIFTER
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module BARREL_SHIFTER(
    input [0:3] W,
    input S0,
    input S1,
    output [0:3] Y
    );
    
    //mux=1
    assign a0= W[3]&~S0&~S1;
    assign a1= W[0]&S0&~S1;
    assign a2= W[1]&~S0&S1;
    assign a3= W[2]&S0&S1;
    assign Y[0]= a0|a1|a2|a3;
    
    //mux=2
    assign b0= W[2]&~S0&~S1;
    assign b1= W[3]&S0&~S1;
    assign b2= W[0]&~S0&S1;
    assign b3= W[1]&S0&S1;
    assign Y[1]= b0|b1|b2|b3;
    
    
    //mux=3
    assign c0= W[1]&~S0&~S1;
    assign c1= W[2]&S0&~S1;
    assign c2= W[3]&~S0&S1;
    assign c3= W[0]&S0&S1;
    assign Y[2]=c0|c1|c2|c3;
    
    //mux=4
     assign d0= W[0]&~S0&~S1;
    assign d1= W[1]&S0&~S1;
    assign d2= W[2]&~S0&S1;
    assign d3= W[3]&S0&S1;
    assign Y[4]= d0|d1|d2|d3;
    
    
endmodule
