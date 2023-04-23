# CLR-Emulator

# Introduction
This is an implementation of a CLR parser in Python. A CLR parser is a bottom-up parsing method based on the LR(1) parsing method. The implementation uses a parsing table to parse the input string. The parsing table is generated from the grammar of the language to be parsed.

This implementation includes code for generating the CLR parsing table from the grammar and the input string. It also includes code for the parsing process itself.

# Dependencies
Python 3.x
Usage
To use this implementation of a CLR parser, simply run the main() function in the firstfollow module. This function prompts the user to enter the productions of the grammar, and then generates the first and follow sets for the non-terminals in the grammar.

After generating the first and follow sets, the parsing_table() function in the parsingtable module can be used to generate the CLR parsing table for the grammar. The parsing_table() function takes the first and follow sets as inputs, along with the grammar productions.

Once the parsing table has been generated, it can be used to parse an input string using the parse() function in the parser module. The parse() function takes the input string and the parsing table as inputs, and returns a parse tree if the string is valid, or raises an exception if the string is invalid.

# Modules
This implementation includes the following modules:

firstfollow
This module contains code for generating the first and follow sets for the non-terminals in the grammar. The main() function in this module prompts the user to enter the productions of the grammar, and then generates the first and follow sets.

parsingtable
This module contains code for generating the CLR parsing table for the grammar. The parsing_table() function in this module takes the first and follow sets as inputs, along with the grammar productions, and returns the parsing table.

parser
This module contains code for parsing an input string using the CLR parsing table. The parse() function in this module takes the input string and the parsing table as inputs, and returns a parse tree if the string is valid, or raises an exception if the string is invalid.

# Example
The following is an example of how to use this implementation of a CLR parser:

python

from firstfollow import main as firstfollow_main
from parsingtable import parsing_table
from parser import parse

# generate the first and follow sets
firstfollow_main()

# generate the parsing table
table = parsing_table()

# parse an input string
input_string = "id + id * id"
parse(input_string, table)

# Acknowledgements
This implementation is based on the algorithm described in the book "Compilers: Principles, Techniques, and Tools" by Aho, Sethi, and Ullman. The implementation was developed by Bhanu, Ananya and Anasua.
