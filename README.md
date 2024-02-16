# Compiler

This is a simple compiler written for an undergraduate course in Program Translation.

## Frontend

The frontend of our compiler is composed of two parts:

1. Scanner - Converts a stream of characters into tokens
2. Parser - Converts the tokens into a parse tree

The scanner uses a driver and state transition table.

## Backend

The backend of our compiler is composed of three parts:

1. Static semantics
2. Code generation
3. and optimization

### Static Semantics

The only static semantics imposed by the compiler are proper use of variables. Before using a variable, you must first declare it using the **var** keyword.

In our language scopes are imposed by blocks denoted by **start** and **end**, conditionals denoted by **if**, and loops denoted by **iter**.

For our compiler, we implement **local scoping** in contrast to global scoping.

### Code Generation
We traverse the decorated parse tree for each node generate corresponding assembly code.

