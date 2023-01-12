This note is a compendium of the various logic gates used in digital logic.

>[!example] AND gate
>This gate is only toggled on if both inputs are 1.
>[[Truth_Table_Storage#^4192cd|truth table]]
>This gate is denoted with the "$\cdot$" operator in boolean algebra

^ee8e59

>[!example] OR gate
>This gate is only toggled off if both inputs are zero. It is 1 otherwise.
>[[Truth_Table_Storage#^5df80f|truth table]]
>This gate is denoted with the "$+$" operator in boolean algebra

^fca52d

>[!example] NOT gate
>This is essnetially a negation gate, or an inverter. A 1 becomes 0, and a 0 becomes a 1. This only takes in one input.
>This gate is denoted with the "$\overline{}$" operator in boolean algebra

>[!example] NAND gate
>The negated [[Logic Gates#^ee8e59|AND]] gate. Essentially the opposite truth table to the AND gate. This gate is only toggled off if both inputs are true.
>This gate is denoted with the "$\overline{\cdot}$" operator in boolean algebra
>
>If one input is permanently connected to "1", then it acts as an inverter for the second input.

>[!example] NOR gate
>The negated [[Logic Gates#^fca52d|OR]] gate. Essentially the opposte truth table to OR. This gate is only toggled on if both inputs are false.
>This gate is denoted with the "$\overline{+}$" operator in boolean algebra
>
>If one input is permanently connected to "0", then it acts as an inverter for the second input.

>[!example] XOR gate
>This is the exclusive OR gate. This input is only toggled on if both inputs are different. For example, if the A=1 and B=1, this gate is 0, but if A=1 and B=0, this gate is 1. 
>[[Truth_Table_Storage#^32a743|truth table]]
>This gate is denoted with the "$\oplus$" operator in boolean algebra
>
>The XOR can be expressed in terms of AND and OR as such:
>$$A\oplus B=\overline{A}B+A\overline{B}$$
>If one input is permanently connected to "1", then it acts as an inverter for the second input.

^c71224

>[!example] XNOR gate
>This is the exclusive NOR gate. This input is only toggled on if both inputs are the same.
>[[Truth_Table_Storage#^54a210|truth table]]
>This gate is denoted with the "$\overline{\oplus}$" operator in boolean algebra

>[!example] Definition: Switch
>A Switch is a circuit we can turn on and off based on an input.
>If you connect one input of an [[Logic Gates#^ee8e59|AND]] gate to "1", then the second input acts as a switch.
>When you set the second input to "1", the gate will output "1", and when you set the second input to "0", the gate will turn off.

>[!example] Definition: Buffer
>A buffer is a function that outputs the input. Here are some common ways to make a buffer:
>1. Connect an [[Logic Gates#^ee8e59|AND]] gate to "1" permanently
>2. Connect an [[Logic Gates#^fca52d|OR]] gate to "0" permanently
>3. Connect an [[Logic Gates#^c71224|XOR]] gate to "0" permanently