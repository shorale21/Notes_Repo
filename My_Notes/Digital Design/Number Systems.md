## Stoneage Unary
This is simply counting. 
>[!example] Definition: Stonage Unary
>Stonage Unary is a "base 1" number system in which the number is represnted by counts, usually shown as tick marks.
>For example, the base 10 number "4" would be written in stonage unary as $||||$

## Quick Definitions
>[!example] Definition: Number System
>A language system consisting of an ordered set of symbols with rules defined for various mathematical operations

>[!example] Definition: Digit
>A symbol in a number system, a digit contains numerical value within that system

>[!example] Definition: Radix
>The number of digits in the ordered set of symbols in a number system
>This is also often called the base of a system.
>
>For example, the decimal system is base 10, and has a radix of 10

>[!example] Definition: Number
>A collection of digits that has numerical value with integral and fractional parts
>
>Number: (Integral Part) . (Fractional Part)
>The dot is the Radix Point

>[!example] Definition: Radix Point
>A symbol that delineates the fractional and integral portions of a number

Let's discuss how weightings work in numbers.
A number is made up of digits, each one from the base set of symbols defined in the number system.
Let's take the base 4 system, (Radix=4). The set of symbols is as so:
$$\{0,1,2,3\}$$
The number of the left of the radix point has a weight of zero. Starting from there, you can move left, counting up, or move right, counting down. 
So, for the number $103.2$ in the base 4 system, the number $1$ is associated with a weight of 2. What this means is that its numerical value is multiplied by the base to the power of the weight (to convert to decimal).
Thus $103.2$ becomes
$$103.2_{(4)}=(1\cdot4^{2})+(0\cdot4^{1})+(3\cdot4^{0})+(2\cdot4^{-1})=19.5_{(10)}$$
>[!example] Definition: The Decimal System
>This is the most common number system. It has base 10, and the symbol set
>$$\{0,1,2,3,4,5,6,7,8,9\}$$

>[!example] Definition: The Binary System
>This is the most common system for digital hardware, it is simple and easy to use. It has base 2 and the symbol set
>$$\{0,1\}$$
>The digits here are called "bits"
>A group of four bits is called a "nibble"
>A group of eight bits is called a "byte"

>[!example] Definition: The Hexadecimal (Hex) system
>This is a less common system, it compresses long binary statements for better comprehension. It has base 16 and symbol set
>$$\{0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F\}$$
>With $F_{(16)}=15_{(10)}$

In binary, the number of unique combination os bits is $2^{\text{ number of bits}}$
So for example, there can be 16 different decimal numbers represented using 4 bits.

On the flipside, the number of bits required to represent a decimal number $n$ is
$$\text{ceil }(\log_{2}n)$$
With the ceiling function.

## Conversions 
The first method of converting a decimal number $n$ to any other radix $r$ is the division algorithm.
1. Do $n\div r$. You should get a remainder of any one of $\{0,\dots,r\}$
2. This remainder is your digit, so place it in the number starting at the least significant
3. Repeat with the new numbers until your division results in a zero.
>[!definition] Example: Division Algorithm
>Let's convert $487$ in base 10, to base 10, by the division algorithm
>1. $487\div10=48$ with a remainder of $7$. This is our least significant digit.
>2. $48\div10=4$ with a remainder of $8$. This is the next digit.
>3. $4\div10=0$ with a remainder of $4$. Since we resulted in a zero, this is our most significant digit and we are finished.
>
>The number we have is then $487$, the obviously correct result.

The conversion algorithm for the fractional part is the same except you multiply instead of dividing, and your digit is the non fractional part of the result. 
Example, let's convert 0.243 (which is in decimal) to decimal:
1. $0.243\times10=2.43$ Remove the 2 which is now our most significant digit
2. $0.43\times10=4.3$ Remove the 4 which is our next digit
3. $0.3\times10=3.0$ Remove the 3 which is our least significant digit because we are left with a zero.

Thus we have resulted in the obvious answer, $0.243$

## Signed Binary Representations
We now want to represent negative binary numbers. One of the main applications of this is to subtract rather than just add. Since subtracting is just adding a negative number, we need a formalism to represent signed binary numbers.

>[!example] Sign Magnitude Notation
>In SM notation, there is a single bit, the MSB, that represents the sign of the number, and the rest of the bits represent the magnitude of the number.
>"1" means negative and "0" means positive
>
>For example, -5 would be represented as 1101, as 101 translates to 5 and the MSB 1 means the number is negative
>
>Operations: 
>1. Multiply by -1 $\longrightarrow$ invert MSB
>2. Convert positive to Decimal $\longrightarrow$ apply conversion on magnitude bits
>3. Convert negative to Decimal $\longrightarrow$ apply conversion to magnitude bits and add minus sign

>[!example] Diminshed Radix Complement
>In this idea, to make a number negative, one simply performs a 1's complement on the bits. 
>A 1's complement simply inverts all bits. The MSB will indicate the sign.
>
>For example, -5 would be represented as 1010, as 5 is 0101.

>[!example] Radix Complement
>The operation required to use the radix complement is called two's complement.
>Two's complement is simply 1 more than one's complement, so to do this operation you simply invert all bits and then add 1.
> 
>Let's convert 10 to negative 10. 
>10 In binary RC is 01010. Remember the MSB indicates the sign.
>
>One simple algorithm is to start at the right and move left until you find a 1. After the first 1, begin inverting all the bits after that (do not invert the 1).
>
>Thus our 0 bit is "0", and the 1 bit is "1", thus all bits after the 1 get inverted
>
>This gives our answer of 10110 for -10. 
>Here is the cool part. Let's add this binary number back to 10.
>01010 + 10110 = 00000, with a carry out of 1.
>
>Note that the carry out here does not matter since it indicates the sign. However, the answer is zero so the sign doesn't matter in the first place. However, we've added 10 + -10 successfully to be zero. 
