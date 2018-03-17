This is an ARM Simulator. Which reads the instruction from instruction memory, decode
the instruction, read the register, execute the operation, and write back to the register file.
The instruction set supported is : MOV, ADD, SUB, LDR, STR, etc. 
<br/>

The execution of instruction continues till it reaches instruction “swi 0x11”. In other words as
soon as instruction reads “0xEF000011”, the simulator stops execution.<br/>
All the instructions in the given in the input MEM file are executed as per the functional
behavior of the instructions. Each instruction must go through the following phasmustes:<br/>
- Fetch<br/>
- Decode<br/>
- Execute<br/>
- Memory<br/>
- Writeback<br/><br/>
The simulator also prints messages for each stage, for example for the third instruction
above following messages are printed.<br/>
● Fetch prints:<br/>
○ “FETCH:Fetch instruction 0xE3A0200A from address 0x0”<br/>
● Decode<br/>
○ “DECODE: Operation is ADD, first operand R2, Second operand R3,
destination register R1”<br/>
○ “DECODE: Read registers R2 = 10, R3 = 2”<br/>
● Execute<br/>
○ “EXECUTE: ADD 10 and 2”<br/>
● Memory<br/>
○ “MEMORY:No memory operation”<br/>
● Write-back<br/>
○ “WRITEBACK: write 12 to R1”<br/>
