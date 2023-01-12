This design approach is called IMD or "iterative modular design".

Brute force design has limitations associated with boolean logic that can be overcome at the gate level.

## Half Adders
This is a 1-bit adder. This circuit takes as input two 1-bit values and outputs their sum and a carry out.
Let's take a look at the truth table for this circuit:

| A   | B   | S   | $C_{out}$ |
| --- | --- | --- |:---------:|
| 0   | 0   | 0   |     0     |
| 0   | 1   | 1   |     0     |
| 1   | 0   | 1   |     0     |
| 1   | 1   | 0   |     1     |

"S" is the sum output and $C_{out}$ is the carry out. Notice that the carry out is only 1 when both A and B are 1, hinting at an AND gate.
"S" is slightly more complicated so we introduce the XOR gate
>[!example] Exclusive OR gate
>This is a form of the [[Boolean Algebra#^daf0c1|OR gate]], in which it is exclusive.
>This means that when both inputs are $1$ the output is actually $0$.

Our final design for the half adder is to run $A$ and $B$ through an XOR gate which produces $S$ as an output, and then also run $A$ and $B$ through an AND gate which produces $C_{out}$ as an output.

## Full Adder
The full adder is an upgrade to the half adder in which a carry in is placed into the design which affects the output. This way we can string together multiple full adders to add multi-bit numbers.

The logic goes as follows:
1. Implement the half adder as shown, but relabel the sum "S" as "Q" and the carry out as "D"
2. Add the carry in to the result of the binary addition "Q"
3. Use the two inputs as before to determine a carry out for the first addition
4. Use the carry in and the result "Q" to determine a carry out for the second addition
5. If either of the carry outs are one, then the entire carry out is one.

>[!example] Full Adder Design
>This is a circuit to add together two 1 bit numbers with a carry in.
>We have inputs $\text{A,B,C}_{\text{in}}$ and outputs $\text{S,C}_{\text{out}}$
>1. XOR $\text{A,B}$ and define the output as $\text{Q}_{1}$
>2. AND $\text{A,B}$ and define the output as $\text{C}_1$
>3. XOR $\text{Q}_1,\text{C}_{\text{in}}$ and assign the output to $\text{S}$
>4. AND $\text{Q}_1,\text{C}_{\text{in}}$ and define the output $\text{C}_2$
>5. OR $\text{C}_1,\text{C}_2$ and assign the output to $\text{C}_{\text{out}}$
>
>Here are boolean equations defining the outputs:
>$$S=(\overline{A}\cdot\overline{B}\cdot C_{in})+(\overline{A}\cdot B\cdot\overline{C_{in}})+(A\cdot\overline{B}\cdot\overline{C_{in}})+(A\cdot B\cdot C_{in})$$

^e8d287

## Ripple Carry Adder
This is a type of mathematica circuit called an RCA.
>[!example] Definition: Ripple Carry Adder
>A Mathematical circuit designed to add two numbers together
>
>It takes in two $n$-bit inputs and outputs a $n$-bit "sum" and a 1-bit carry out.
>
>A great method of designing an RCA is to string together [[Ripple Carry Adders#^e8d287|full adders]]
