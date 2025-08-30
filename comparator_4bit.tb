// Code your testbench here
// or browse Examples
`timescale 1ns/1ps

module tb_comparator_4bit;

reg [3:0] A;
reg [3:0] B;
wire A_gt_B;
wire A_lt_B;
wire A_eq_B;

comparator_4bit uut (
    .A(A),
    .B(B),
    .A_gt_B(A_gt_B),
    .A_lt_B(A_lt_B),
    .A_eq_B(A_eq_B)
);

initial begin
    $dumpfile("dump.vcd");
    $dumpvars(0, tb_comparator_4bit);
    $monitor("Time=%0t A=%d B=%d | A>B=%b A<B=%b A=B=%b",
              $time, A, B, A_gt_B, A_lt_B, A_eq_B);

    A = 4'b0000; B = 4'b0000; #10;
    A = 4'b1010; B = 4'b0110; #10;
    A = 4'b0101; B = 4'b1110; #10;
    A = 4'b1111; B = 4'b1111; #10;
    A = 4'b0011; B = 4'b0100; #10;

    $finish;
end
endmodule
