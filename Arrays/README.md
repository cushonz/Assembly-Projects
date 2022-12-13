Readme
This code is written in x86-64 Assembly.

It contains three segments: .data, .text, and .bss.

The .data segment stores the initial values for the arrays a and b and the signed integer c. It also defines the memory location for the result of the calculations.

The .text segment contains the main program, which performs the following actions:

    1.Clears the values in registers rax, rbx, and rcx.
    2.Moves the first value in array a into rax and the value stored in const into rbx.
    3.Adds the values in rax and rbx and stores the result in rcx.
    4.Moves the first value in array b into rax and the value of c into rbx.
    5.Adds the values in rax and rbx and stores the result in rax.
    6.Subtracts the value in rax from the value in rcx and stores the result in rcx.
    7.Adds the value in rcx to the result stored in memory.
    8.Repeats steps 2-7 for the remaining values in arrays a and b.
    9.Returns.
The .bss segment is used for uninitialized data. It is not used in this code.
