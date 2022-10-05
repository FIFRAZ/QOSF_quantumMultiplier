# QOSF_quantumMultiplier
Quantum circuit implementation of multiplication of two positive integers
--------------------------------------------------------------------

The codebase for quantum multiplier, consists of two code files: QuantumUtil, and QuantumMultiplier
QuantumUtil contains utility functions and this module(file) would be imported into QuantumMultiplier.

QuantumMultiplier contains the main functions named
q_multiplier_with_user_input() and q_multiplier(decimal_num1, decimal_num2).
-------------------------------------------------------------------
These two functions perform multiplication, and implementation of these two functions consist of invoking one or more functions from QuantumUtil.


This is my first ever quantum code.

Open Questions(that I am yet to research):
---------------------------------------------
-> Is creating quantum circuit multiple times for implementing the multiplication algorithm using repeatitive addition, expensive? Would QFT eliminate this problem and be more efficient?

--> With the current implementation of adder, for adding 2 numbers of n bits, I am using 4n+1 qubits(including the classical register), and n*4 logic gates.

--> Could the same be done using any other logic gates? I used X, CX, CCX. Is each quantum gate equally expensive?

--> There must be other shorter ways of performing addition, multiplication, as implemented by Qiskit libraries. What are those functions? How are those implemented internally?

--> I checked the simulator configuration and according to it, number of qubits in simulator could be 29 max.
My code uses 4n+1 qubits, if n is the number of bits in each of the input number, so I was expecting an error when I ran the addition code with both input numbers 10 bits long. There was no error, the code produced correct output, the sum of the two numbers. During multiplication, kernel hangs for input numbers greater than 3 bits long.
