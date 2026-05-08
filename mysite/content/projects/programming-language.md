---
title: "Custom Shader Programming Language"
date: 2025-06-01
draft: false
description: "A fully implemented programming language designed for shader programming, built from scratch in C++ and Java with a complete compiler pipeline."
tags: ["C++", "Java", "compilers", "programming-languages"]
weight: 1
---

## Overview
Built a fully implemented programming language designed for shader programming as part of a Programming Languages course. The language is built from scratch in C++ and Java and includes a complete compiler pipeline from source code to execution — Scanner, Parser, AST, Type Checker, Code Generator, and Interpreter.

The language is designed around a `cellCode` function that returns a `vector3` color value, making it suitable for pixel shaders and cellular automaton-style graphics programs.

## Tech Stack
- **Languages:** C++, Java
- **Components:** Scanner, Parser, AST, Type Checker, Code Generator, Interpreter
- **Build Tool:** g++ with C++17, javac

## Features
- Full compiler pipeline from source text to execution
- Custom type system with `float`, `int`, `bool`, `string`, and `vector3` types
- Built-in RGB vector type with `.r`, `.g`, `.b` component access
- Control flow — `if`, `while`, `for`
- User-defined functions with typed parameters and return values
- Texture loading and sampling via `getTextureColor`
- Compile-time constants with `#def`
- Full static type checking with error messages
- Built-in math functions — `abs`, `sqrt`, `pow`
- Mouse and canvas position constants (`MOUSE_X`, `MOUSE_Y`, etc.)

## Architecture
The compiler and interpreter follow a clean pipeline:
- **Scanner** — tokenizes source text into a stream of tokens
- **Parser** — recursive descent parser that builds the AST
- **Type Checker** — walks the AST and verifies type correctness
- **Code Generator** — emits a flat token-stream IR to `input.txt`
- **Interpreter** — Java program that reads and executes the IR

## What I Learned
- How to build a full compiler pipeline from scratch
- Implementing a recursive descent parser and AST in C++
- Static type checking and code generation techniques
- Bridging a C++ compiler with a Java interpreter via an intermediate representation
- Designing a domain-specific language with a clear grammar and type system

## Links
- [GitHub Repository](https://github.com/JJ-Gillis23/Programming-Language)