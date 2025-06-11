assign statement:
assign x = a;
- assign establishes physical connection between wires
- order of assign statements does not matter
- connections are continuous (permanent)
- a drives x, i.e. signal goes from a to x

concatenation operator {}:
wire \[3:0] a = 4'b1010;
wire \[3:0] b = 4'b1100;
wire \[7:0] result;
assign result = {a, b};  // result = 8'b10101100
- assigns the bits of the inputs in order to the most significant bits of the result
- e.g. a\[3] -> result\[7]

NOT Operators:
single bit NOT: ~
logical NOT: !

AND Operators:
single bit AND: &
logical AND: &&

OR Operators:
single bit OR: |
logical OR: ||

XOR Operator:
single bit: ^

Vector Declaration:
wire \[7:0] w;
- declares an 8-bit vector (bits numbered 7 down to 0)
- functionally equivalent to having 8 separate wires
- dimensions, i.e. width, always comes before the name in a declaration
- vectors are sometimes referred to as a "bus" when used as a wire (because they contain multiple lines)

Vector Part Select:
assign out = w\[4];
- connects (assigns) bit number 4 of the vector w to the wire out
- i.e. bit number 4 was "selected"