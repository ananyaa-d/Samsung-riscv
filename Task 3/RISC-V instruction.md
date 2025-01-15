![Screenshot_from_2025-01-15_16-30-38_-_3 1](https://github.com/user-attachments/assets/b7c28a07-a6df-4b68-ac9c-82c026f164e9)


1. ### Instruction: addi  sp, sp, -16
    Opcode: 0010011 (7 bits)\
    Immediate: -16 (12 bits, represented in two's complement)\
    Source Register (rs1): sp (x2, 5 bits)\
    Destination Register (rd): sp (x2, 5 bits)\
    Function (funct3): 000 (3 bits)\
**Breakdown:**<br/>
    Immediate (-16): 111111110000 (12-bit two's complement representation of -16)\
    rs1 (sp = x2): 00010\
    rd (sp = x2): 00010\
    funct3: 000\
    Opcode: 0010011

2. ### Instruction: sd  ra, 8(sp)
    Opcode: 0100011 (7 bits)\
    Immediate: 8 (12 bits, split into two parts: imm[11:5] and imm[4:0])\
    Source Register (rs2): ra (x1, 5 bits)\
    Base Register (rs1): sp (x2, 5 bits)\
    Function (funct3): 011 (3 bits)\
**Breakdown:**<br/>
   Immediate (8): 0000000001000 (split into imm[11:5] = 0000000 and imm[4:0] = 01000)\
    rs2 (ra = x1): 00001\
    rs1 (sp = x2): 00010\
    funct3: 011\
    Opcode: 0100011

3. ### Instruction: li  a5, 200
    Opcode: 0010011 (7 bits)\
    Immediate: 200 (12 bits)\
    Source Register (rs1): x0 (constant 0, 5 bits)\
    Destination Register (rd): a5 (x15, 5 bits)\
    Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
    Immediate (200): 000011001000 (12-bit binary representation of 200)\
    rs1 (x0): 00000\
    rd (a5 = x15): 01111\
    funct3: 000\
    Opcode: 0010011

4. ### Instruction: addiw  a5, a5, -1
    Opcode: 0011011 (7 bits)\
    Immediate: -1 (12 bits, represented in two's complement)\
    Source Register (rs1): a5 (x15, 5 bits)\
    Destination Register (rd): a5 (x15, 5 bits)\
    Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
    Immediate (-1): 111111111111 (12-bit two's complement representation of -1)\
    rs1 (a5 = x15): 01111\
    rd (a5 = x15): 01111\
    funct3: 000\
    Opcode: 0011011 

5. ### Instruction: bnez a5, 10190 <main+0xc>
    Opcode: 1100011 (7 bits)\
    Immediate: offset (12 bits, split into parts: imm[12], imm[11], imm[10:5], and imm[4:1])\
    Source Register (rs1): a5 (x15, 5 bits)\
    Source Register (rs2): x0 (x0, 5 bits)\
    Function (funct3): 001 (3 bits)\
**Breakdown**:<br/>
    Immediate (offset): <calculated value> (split into imm[12], imm[10:5], imm[4:1], and imm[11])\
    rs1 (a5 = x15): 01111\
    rs2 (x0 = x0): 00000\
    funct3: 001\
    Opcode: 1100011

6. ### Instruction: lui a2, 0x5
    Opcode: 0110111 (7 bits)\
    Immediate: 0x5 (20 bits)\
    Destination Register (rd): a2 (x12, 5 bits)\
**Breakdown**:<br/>
    Immediate (0x5): 00000000000000000005 (20-bit binary representation of 0x5)\
    rd (a2 = x12): 01100\
    Opcode: 0110111

7. ### Instruction: addi a2, a2, -380
    Opcode: 0010011 (7 bits)\
    Immediate: -380 (12 bits, represented in two's complement)\
    Source Register (rs1): a2 (x12, 5 bits)\
    Destination Register (rd): a2 (x12, 5 bits)\
    Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
    Immediate (-380): 111110100100 (12-bit two's complement representation of -380)\
    rs1 (a2 = x12): 01100\
    rd (a2 = x12): 01100\
    funct3: 000\
    Opcode: 0010011

8. ### Instruction: li  a1, 200
    Opcode: 0010011 (7 bits)\
    Immediate: 200 (12 bits)\
    Source Register (rs1): x0 (constant 0, 5 bits)\
    Destination Register (rd): a1 (x11, 5 bits)\
    Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
    Immediate (200): 000011001000 (12-bit binary representation of 200)\
    rs1 (x0): 00000\
    rd (a1 = x11): 01011\
    funct3: 000\
    Opcode: 0010011

9. ### Instruction: lui a0, 0x21
    Opcode: 0110111 (7 bits)
    Immediate: 0x21 (20 bits)
    Destination Register (rd): a0 (x10, 5 bits)
**Breakdown**:<br/>
    Immediate (0x21): 0000000000021 (20-bit binary representation of 0x21)
    rd (a0 = x10): 01010
    Opcode: 0110111

10. ### Instruction: addi a0, a0, 400
      Opcode: 0010011 (7 bits)\
      Immediate: 400 (12 bits)\
      Source Register (rs1): a0 (x10, 5 bits)\
      Destination Register (rd): a0 (x10, 5 bits)\
      Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
      Immediate (400): 0000001100100000 (12-bit binary representation of 400)\
      rs1 (a0 = x10): 01010\
      rd (a0 = x10): 01010\
      funct3: 000\
      Opcode: 0010011

11. ### Instruction: jal ra, 10418
      Opcode: 1101111 (7 bits)\
      Immediate: 10418 (20 bits, split into parts for the J-type format)\
      Destination Register (rd): ra (x1, 5 bits)\
**Breakdown**:<br/>
      Immediate (10418): 0000000001010000010\
      rd (ra = x1): 00001\
      Opcode: 1101111

12. ### Instruction: li  a0, 0
      Opcode: 0010011 (7 bits)\
      Immediate: 0 (12 bits)\
      Source Register (rs1): x0 (constant 0, 5 bits)\
      Destination Register (rd): a0 (x10, 5 bits)\
      Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
      Immediate (0): 000000000000 (12-bit binary representation of 0)\
      rs1 (x0): 00000\
      rd (a0 = x10): 01010\
      funct3: 000\
      Opcode: 0010011

13. ### Instruction: ld ra, 8(sp)
      Opcode: 0000011 (7 bits)\
      Immediate: 8 (12 bits, split into two parts: imm[11:5] and imm[4:0])\
      Destination Register (rd): ra (x1, 5 bits)\
      Base Register (rs1): sp (x2, 5 bits)\
      Function (funct3): 011 (3 bits)\
**Breakdown**:<br/>
      Immediate (8): 000000001000 (12-bit binary representation of 8, split into imm[11:5] = 0000000 and imm[4:0] = 01000)\
      rd (ra = x1): 00001\
      rs1 (sp = x2): 00010\
      funct3: 011\
      Opcode: 0000011

14. ### Instruction: addi  sp, sp, 16
      Opcode: 0010011 (7 bits)\
      Immediate: 16 (12 bits)\
      Source Register (rs1): sp (x2, 5 bits)\
      Destination Register (rd): sp (x2, 5 bits)\
      Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
      Immediate (16): 000000010000 (12-bit binary representation of 16)\
      rs1 (sp = x2): 00010\
      rd (sp = x2): 00010\
      funct3: 000\
      Opcode: 0010011

15. ### Instruction: jalr x0, 0(ra)
      Opcode: 1100111 (7 bits)\
      Immediate: 0 (12 bits)\
      Source Register (rs1): ra (x1, 5 bits)\
      Destination Register (rd): x0 (constant 0, 5 bits)\
      Function (funct3): 000 (3 bits)\
**Breakdown**:<br/>
      Immediate (0): 000000000000 (12-bit binary representation of 0)\
      rs1 (ra = x1): 00001\
      rd (x0 = x0): 00000\
      funct3: 000\
      Opcode: 1100111
