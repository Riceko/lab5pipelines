# Section 1
| PC | Opcode | src1_addr | src1_out   |dst_addr | dst_data   |
|---:|-------:|----------:|-----------:|--------:|-----------:|
| 0  |  23    |     0     | 0x00000000 |  0      | 0x00000000 |
| 4  |  23    |     0     | 0x00000000 |  0      | 0x00000000 |
| 8  |  00    |     2     | 0x00000000 |  0      |  xxxxxxxxxx|
|12  | 0x2B   |     0     | 0x00000000 |  2      | 0x00000056 |
|16  |  00    |     3     | 0x00000000 |  2      | 0x00000056 |
|20  | 0x08   |     3     | 0x00000000 |  3      | 0x00000000 |
|24  | 00     |     5     | 0x00000000 |  3      | 0x00000084 |
|28  | 00     |     6     | 0x00000000 |  4      | 0xFFFFFFAA |
|32  | 00     |     6     | 0x00000000 |  5      | 0x0000000C |
|36  | 00     |     5     | 0x0000000C |  6      | 0x00000000 |
|40  | 04     |     5     | 0x0000000C |  7      | 0x00000056 | 
|44  | 23     |     0     |0x00000000  |  8      | 0xFFFFFFA9 |
|48  | 00     |     0     |0x00000000  |  6      | 0x00000000 |
|52  | 00     |     0     |0x00000000  | 0x1F    | 0x0000000C |
 56  | 00     |     0     |0x00000000  | 0x08    | 0x00000000 | 


 # Section 2 

 Again as explained by the report descriptions many hazards happen to create many differences between the datapath. one good example is a data hazard which occurs when the instruction after a certain instruction depends on the previous instruction. This would occur with things such as load instruction and adding which without forwarding or stalling leads to incorrect calculations. Another hazard could be control hazards which are due to jumps or branch instructions. A good example is utilizing beq which could create stalls or incorrect fetches.

 # Section 3
  or $t0, $a2, $a3  this allows time for lw before add and reduce data hazard. The would help avoid stall.