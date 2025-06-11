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

Vector Declaration Formatting:
type \[upper : lower] name;
- type is usually either "wire" or "register"
- can be prefaced with "input" or "output" to function as a port
- type is inferred as wire unless specified
- upper and lower specify the numbering and range of the bits
- lower can be non-zero, i.e. positive or negative integer
- upper can be greater than lower, i.e. bit numbering can be increasing rather than decreasing
- "endianness" = the numbering direction of the register
	- e.g. "little-endian" = \[3:0] and "big-endian" = \[0:3]
- endianness of a vector cannot change after declaration

Vector Part Select:
assign out = w\[4];
- connects (assigns) bit number 4 of the vector w to the wire out
- i.e. bit number 4 was "selected"

Implicit Net Types:
- Default type of a net is always a 1-bit wire
- wires can be created implicitly with: assign name = value;
	- as opposed to first declaring: wire \[upper : lower] name;
- also implicitly created: module_type name(a, b);
	- a and b are implicitly 1-bit wires
- implicit net creation can be disabled: `default_nettype none