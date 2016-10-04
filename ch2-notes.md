# Computer Organization and Design: The Hardware/Software Interface
###### By David A. Patterson & John L. Hennessy

## Chapter 2

##### Most Significant Bit
* the lefttmost bit in a MIPS word

##### Least Significant Bit
* the rightmost bit in a MIPS word

##### Big-Endian

##### Little-Endian

##### Spilling Registers
* When a program has more variables than the processor has registers, the less commonly used ones are stored in memory

##### MIPS
* a metric used for measuring performance
* stands for _million instructions per second_
* uses words that are 32 bits long
    - can create 2^32 different numbers (from 0 to 2^32 - 1)

##### Alignment Restriction
* a rule in MIPS that requires addresses of _words_ to begin on multiples of 4

##### Two's Complement Notation
* the agreed-upon best way to represent negative numbers using binary
* the leftmost bit is used to indicate the sign of the number (called the _sign bit_)
    - trailing 0's means positive
    - trailing 1's means negative
* the highest negative number is one larger than the highest positive number
    - -2,147,483,648 vs. 2,147,483,647

##### Sign Extension
* when a load is less than the full size of the register, the rest of the leading bits are filled with the number's _sign bit_

##### Add Immediate aka `addi` 
* allows you to add using a constant (number literal) as one operand
* you can also use negative constants
* faster than loading a constant from memory




#### About the Register
* a register is 32 bits in size (unless you have a 64-bit processor)
    - equal to one _word_
* there are usually about 32 of them in a computer (30 is also common)
    - less registers means less available space, but can allow for smaller physical size
* 