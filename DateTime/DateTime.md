# Date Time in Assembly
This is a simple program written in assembly that takes a hexadecimal value and uses bit manipulation to extract the day, month, and year.

# Usage
To use this code, you will need to be running an environment with support for assembly language. You can then run the program and pass in a hexadecimal value as an argument. The program will extract the day, month, and year from the value and print them to the screen.

# Code Details
The code is written in x86 assembly language and uses the following registers:

    EDX: This register is used to store the hexadecimal value passed in as an argument. It is also used to store intermediate results during the calculation of the day, month, and year.
    
    DX: This register is used to store the result of the bit manipulation operations performed on the value stored in EDX.

# Procedure
The program first clears the EDX and DX registers using the xor instruction. It then moves the hexadecimal value into the EDX register using the mov instruction.

To extract the year from the value, the program first shifts the value in EDX to the right by 9 bits using the shr instruction. It then adds the result to the year variable using the add instruction.

To extract the day from the value, the program first shifts the value in EDX to the left by 11 bits using the shl instruction. It then shifts the result to the right by 11 bits, effectively clearing the bits used to store the year. The program then adds the result to the day variable using the add instruction.

To extract the month from the value, the program first shifts the value in EDX to the left by 7 bits using the shl instruction. It then shifts the result to the right by 12 bits, effectively clearing the bits used to store the year and day. The program then adds the result to the month variable using the add instruction.

Finally, the program returns with the ret instruction.