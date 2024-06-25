```ebnf
program            ::= statement*

statement          ::= function_declaration
                     | variable_declaration
                     | assignment_statement
                     | if_statement
                     | loop_statement
                     | for_statement
                     | print_statement
                     | function_call
                     | record_declaration

function_declaration ::= "part" identifier "[" parameter_list "]" ":" type "{" statement* "}"

parameter_list     ::= parameter ("," parameter)* | ε

parameter          ::= type identifier

variable_declaration ::= "let" identifier ":" type "=" expression ";"

assignment_statement ::= "let" identifier "=" expression ";"

if_statement       ::= "if" expression "{" statement* "}"
                       ( "elif" expression "{" statement* "}" )*
                       ( "else" "{" statement* "}" )?

loop_statement     ::= "loop" "[" expression "]" "{" statement* "}"

for_statement      ::= "for" identifier "in" expression "{" statement* "}"

print_statement    ::= "print" "(" expression ")" ";"

function_call      ::= "call" identifier "(" argument_list ")" ";"

record_declaration ::= "record" identifier "{" field_declaration* "}"

field_declaration ::= type identifier ";"

expression         ::= literal
                     | identifier
                     | binary_operation
                     | function_call
                     | list_literal
                     | dictionary_literal
                     | record_instantiation
                     | "(" expression ")"
                     | unary_operation

literal            ::= integer_literal
                     | string_literal
                     | boolean_literal
                     | list_literal
                     | dictionary_literal

integer_literal    ::= digit+

string_literal     ::= "\"" character* "\""

boolean_literal    ::= "true" | "false"

list_literal       ::= "[" ( expression ( "," expression )* )? "]"

dictionary_literal ::= "{" ( key_value_pair ( "," key_value_pair )* )? "}"

key_value_pair     ::= expression ":" expression

binary_operation   ::= expression "+" expression
                     | expression "-" expression
                     | expression "*" expression
                     | expression "/" expression
                     | expression "%" expression
                     | expression "==" expression
                     | expression "!=" expression
                     | expression "<" expression
                     | expression ">" expression
                     | expression "<=" expression
                     | expression ">=" expression
                     | expression "and" expression
                     | expression "or" expression

unary_operation    ::= "-" expression
                     | "not" expression

type               ::= "int" | "string" | "boolean"
                     | "list" "[" type "]"
                     | "dict" "[" type "," type "]"
                     | identifier  # Custom types (records)

identifier         ::= letter ( letter | digit )*

digit              ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"

letter             ::= "a" | "b" | ... | "z" | "A" | "B" | ... | "Z"

character          ::= any printable ASCII character

argument_list      ::= expression ("," expression)* | ε
```

### Explanation:

- **Syntax Categories**:
  - **program**: Represents a sequence of statements.
  - **statement**: Represents any valid programming statement.
  - **function_declaration**: Declares a function using the `part` keyword.
  - **parameter_list**: Represents a list of parameters in a function declaration.
  - **parameter**: Represents a parameter with a type and identifier.
  - **variable_declaration**: Declares a variable using the `let` keyword.
  - **assignment_statement**: Assigns a value to a variable.
  - **if_statement**: Implements conditional branching (`if`, `elif`, `else`).
  - **loop_statement**: Implements a fixed iteration loop (`loop`).
  - **for_statement**: Implements a for-each loop over collections (`for`).
  - **print_statement**: Prints output to the console.
  - **function_call**: Calls a defined function using the `call` keyword.
  - **record_declaration**: Declares a record type using the `record` keyword.
  - **field_declaration**: Declares a field within a record type.
  - **expression**: Represents a valid expression in the language.
  - **literal**: Represents various literal types like integers, strings, booleans, lists, and dictionaries.
  - **binary_operation**: Represents binary operations like arithmetic, comparison, and logical operations.
  - **unary_operation**: Represents unary operations like negation and logical NOT.
  - **type**: Represents data types supported by the language, including basic types (`int`, `string`, `boolean`), lists, dictionaries, and custom types (records).
  - **identifier**: Represents variable names, function names, or type names.
  - **digit, letter, character**: Basic components used to define identifiers, literals, and other constructs.

