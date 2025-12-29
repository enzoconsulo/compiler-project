## Compiler Project

This repository contains a compiler developed in C and Python as part of Compiler classes at PUC Campinas.
The main goal of this project is to study and implement the core phases of a compiler for a simple programming language inspired by Portugol syntax, applying academic and practical concepts of compilation.

---
### Overview

A compiler is a program that translates source code written in a high-level programming language into a lower-level representation that can be executed by a computer. The compilation process is composed of several well-defined phases, including lexical analysis, syntactic analysis, semantic analysis, and code generation.

This project follows a classic compiler pipeline and was developed with an educational focus, emphasizing clarity, correctness, and understanding of each compilation stage rather than performance optimizations.

---
### Project Structure
```
├── include/
│   └── Header files (.h) containing token definitions, data structures, and interfaces
├── src/
│   ├── lexical/
│   │   └── Lexical analyzer responsible for tokenizing the source code
│   ├── syntactic/
│   │   └── Parser and grammar rules for syntactic validation
│   ├── semantic/
│   │   └── Semantic analysis (symbol table, scope, and type validation)
│   ├── code_generator/
│   │   └── Code generation and instruction handling
│   └── error_UI/
│       └── Error handling and user-friendly compiler messages
├── tests/
│   └── Test source files for validating compiler behavior
├── Makefile
│   └── Build automation
├── compilador_ui.py
│   └── Optional Python-based interface for compiler execution
└── README.md
```

---
### Implemented Features

1. Lexical Analysis
   - Scans the source code and converts it into a sequence of tokens
   - Identifies keywords, identifiers, literals, operators, and delimiters
   - Provides detailed error messages for invalid lexemes

2. Syntactic Analysis
   - Parses the token stream according to a predefined grammar
   - Builds and validates an Abstract Syntax Tree (AST)
   - Detects and reports syntax errors with line and column information

3. Semantic Analysis
   - Validates variable declarations and usage
   - Ensures correct scoping rules
   - Performs type checking and semantic consistency validation

4. Code Generation
   - Traverses the AST to generate intermediate or executable instructions
   - Structures instructions in a modular and extensible format
   - Provides a foundation for future optimizations or target backends

---
### Build and Execution

Compilation:
```sh
gcc -Wall -Wextra -g src/syntactic/parser.c src/lexical/lexer.c src/semantic/semantic.c src/code_generator/generator.c src/code_generator/instructions.c ./src/error_UI/error.c -o parser
```

Execution:
```sh
./parser

> Than execute your program (this strange language on tests)
tests/syntactic/sint1.txt
```

---
### Testing

The tests directory contains multiple source code examples designed to validate:
- Correct tokenization
- Grammar rule enforcement
- Semantic correctness
- Error detection and reporting

These tests were used throughout development to ensure correctness at each compilation stage.

---
### Technologies

- C — core compiler implementation
- Python — auxiliary interface and tooling
- Makefile — build automation

---
### Academic Context

This project was developed for academic purposes as part of Compiler Theory coursework at PUC Campinas.
It demonstrates practical applications of formal languages, automata theory, grammar parsing, and compiler architecture.

---
### Acknowledgements

Original academic inspiration and initial project concept provided by course material and instructor guidance.
This repository represents an independent implementation and extension for learning and portfolio purposes.
