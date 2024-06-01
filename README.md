# NAND2TETRIS Course Project

## Boolean Functions

f(x, y, z) = (x AND y) OR (NOT(x) AND z)

### Commutative Laws

(x AND y) = (y AND x)
(x OR y) = (y OR x)

### Associative Laws

(x AND (y AND z)) = ((x AND y) AND z)
(x OR (y OR z)) = ((x OR y) OR z)

### Distributive Laws

(x AND (y OR z)) = (x AND y) OR (x AND z)
(x OR (y AND z)) = (x OR y) AND (x OR z)

### De Morgan Laws

NOT(x AND y) = NOT(x) OR NOT(y)
NOT(x OR y) = NOT(x) AND NOT(y)

## Boolean Functions Synthesis

This basically means Truth Table to Boolean Function (expression).

### Steps

1. We go row by row in the Truth Table and we focus only on the rows where the function has the value of 1.

2. We create a boolean function for each of the selected rows above. This function will return 1 for the row it represents and 0 for the all the others. We do this mostly by using NOT and AND.

3. Then we combine them one by one by adding OR between first function and the next (as 1 OR 0 = 1) and so on.

4. Optimize it using the laws above.

### Theorem

Any Boolean function can be represented using an expression containing AND, OR and NOT operations.

Any Boolean function can be represented using an expression containing AND and NOT operations.

### NAND

NAND(x, y) = NOT(x AND y)

This means that any boolean function can be represented using an expression containing only NAND operations.

## Logic Gates

A technique for implementing Boolean functions using logic gates.

Logic gates:

- Elementary (Nand, And, Or, Not)

- Composite (Mux, Adder, ...)

Gate Interface = Gate Abstraction - it's unique

Gate Implementation = The actual implementation of the Gate Interface - this is not unique. There can be many implementations of one abstraction.

Circuit Implementation = Hardwired circuits of the Gate Implementation

## Hardware Descripton Language (HDL)

Steps:

1. Create the logic function by syntesis the truth table -> the easiest way to achieve this is by pseudocode the conditions when the function returns 1. For xOR that would be: The function returns 1 if a AND NOT b OR NOT a AND b

2. Create the diagram (gate interface) based on the logic function

3. Implement the diagram in HDL 

Verilog is an HDL.
