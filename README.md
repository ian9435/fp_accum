# fp_accum

It used Xilinx examples design that compute floating point accumulator function.

# Algorithm 

adder tree to optimize design

Initial：
float windowi[NUM_ELEM/(2^i)] = {0.0}; i=1,2,3,4,5,6
float result = 0.0;
For loop：i=1,2,3,4,5,6
Li: for(ap_uint<7> x=0; x.to_uint()<NUM_ELEM/(2^i); x++)
windowi[x] = windowi-1[x] + windowi-1 [NUM_ELEM/(2^i)+x];
result = window6[0] + window6[1];

# fpga board setup
We use Xilinx ZedBoard Evaluation and Development Kit or PYNQ to evaulate this project

# Reference
https://github.com/Xilinx/HLx_Examples/tree/master/Math/fp_accum

