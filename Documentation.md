# Language Documentation: Original Language

## Introduction

Welcome to the documentation for Original Language, a modern programming language designed for clarity, efficiency, and expressiveness. This document serves as a comprehensive guide for both implementing the language and programming in Original Language.

### Language Design Goals

- **Simplicity**: Inspired by assembly but evolved to include higher-level constructs.
- **Expressiveness**: Support for modern features like conditionals, loops, data structures, and custom types.
- **Performance**: Efficient execution suitable for a variety of applications.
- **Versatility**: Designed to handle both system-level programming and application development.

## Language Overview

### Syntax and Structure

Original Language offers a structured and intuitive syntax that supports a wide range of programming tasks. Key features include:

- **Functions**: Define reusable code blocks with parameters and return types using the `part` keyword.
- **Variables**: Declare variables using `let`, supporting integers, strings, and custom types.
- **Control Flow**: Includes `if-elif-else` conditionals and `loop` statements for iteration.
- **Data Structures**: Support for lists, dictionaries, sets, and custom record types.
- **Comments**: Use `#` for single-line comments and `/* */` for multi-line comments.
- **Standard Library**: Basic functions for input/output (`print`).

### Example Program

```plaintext
# Define a function to sum two numbers
part sum[int, int](a, b):int {
    return a + b;
}

# Main program
main {
    let x = 5;
    let y = 3;
    let result = call sum(x, y);
    print("The sum is: " + result);

    let ages = {"Alice": 30, "Bob": 25};
    let age = call get_value(ages, "Alice");
    print("Alice's age is: " + age);

    let numbers = [1, 2, 3, 4, 5];
    let total = call sum_list(numbers);
    print("Total of numbers is: " + total);

    loop[5] {
        print("Hello, World!");
    }
}
```

### Features

#### Functions

- Functions are defined using the `part` keyword, specifying input and output types.
- Functions can be called using the `call` keyword.

#### Variables

- Variables are declared using the `let` keyword.
- Support for integers (`int`), strings (`string`), and custom types.

#### Control Flow

- **Conditionals**: Use `if`, `elif`, and `else` for decision-making based on conditions.
- **Loops**: Repeat blocks of code with `loop[count] { ... }`.

#### Data Structures

- **Lists**: Dynamic arrays that can hold elements of different types.
- **Dictionaries**: Key-value pairs for efficient data storage and retrieval.
- **Sets**: Collections of unique elements.
- **Records**: Custom data structures with named fields.

#### Comments

- **Single-line**: Use `#` to comment out a single line.
- **Multi-line**: Enclose multi-line comments in `/* */`.

#### Standard Library

- Basic functions for console output (`print`) and input.

## Implementation Guide

### Compiler/Interpreter Components

1. **Lexer**: Tokenizes source code into tokens (keywords, identifiers, literals).
2. **Parser**: Builds an Abstract Syntax Tree (AST) from tokens based on grammar rules.
3. **Semantic Analyzer**: Checks AST for semantic errors (type checking, variable scoping).
4. **Code Generator**: Converts AST into executable code (bytecode, intermediate code).
5. **Runtime**: Executes generated code, manages memory, and handles I/O operations.

### Example Workflow

1. **Define Grammar**: Formulate grammar rules using EBNF to describe valid syntax.
2. **Implement Lexer**: Create a lexer to tokenize source code.
3. **Implement Parser**: Build a parser to generate AST from tokens.
4. **Semantic Analysis**: Check types and scopes, resolve identifiers.
5. **Code Generation**: Translate AST into executable code or intermediate representation.
6. **Runtime Development**: Implement standard library functions and runtime environment.

### Tools and Resources

- **Lexer/Parser Generators**: Flex/Bison, ANTLR for generating lexer and parser.
- **Intermediate Representation**: LLVM for efficient code generation.
- **Documentation**: Maintain clear and updated documentation for language users and developers.

## Getting Started with Original Language

### Setting Up Development Environment

- Install Original Language(Interpreter/Compiler) on your system.
- Set up IDE or text editor with syntax highlighting for Original Language.

### Writing Your First Program

1. **Hello, World!**:
   ```plaintext
   main {
       print("Hello, World!");
   }
   ```

2. **Sum of Numbers**:
   ```plaintext
   part sum[int, int](a, b):int {
       return a + b;
   }

   main {
       let x = 5;
       let y = 3;
       let result = call sum(x, y);
       print("The sum is: " + result);
   }
   ```

3. **Using Conditionals**:
   ```plaintext
   main {
       let age = 25;
       if age >= 18 {
           print("You are an adult.");
       } elif age >= 13 {
           print("You are a teenager.");
       } else {
           print("You are a child.");
       }
   }
   ```

4. **Working with Lists and Loops**:
   ```plaintext
   part sum_list[list[int]](lst):int {
       let total = 0;
       for element in lst {
           total = total + element;
       }
       return total;
   }

   main {
       let numbers = [1, 2, 3, 4, 5];
       let total = call sum_list(numbers);
       print("Total of numbers is: " + total);

       loop[5] {
           print("Hello, World!");
       }
   }
   ```

## Conclusion

Original Language combines elements of assembly with modern programming paradigms, offering a powerful yet accessible environment for developers. Explore the language's features, experiment with different constructs, and contribute to its growing ecosystem.

For more information and updates, visit Original Language website or community forums. **!Not exists!**
