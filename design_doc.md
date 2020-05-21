# tul::Precedence Design Document

## Overview
Precedence is a stack-based dynamically-typed imperative interpreted programming language. The primary goal is to permit the exploration of code constrained by artificial limitations, such as lack of non-integral real numbers and minimization of source code byte count, yet enhanced by built-in functions that are intended to simplify design and non-mainstream control flow.

## Features (and lack thereof)
 - Arbitrary-precision integer arithmetic
 - No native support for non-integral reals (to preempt numerical errors)
 - Type-based overloads for many operators/functions
 - Implicit well-defined intuitive type-casting
 - Execution with selective security policies
 - Implicit input/output
 - `comefrom` as the long lost twin of `goto`
 - No randomization support (can be simulated with `comefrom`)
 - Few possible errors in interpreting phase (instead it is on the programmer to avoid unexpected behavior)
 - Slight optimizations for code golf
 - No user-defined functions (`comefrom` replaces this functionality)

## Programming Model
Every program is composed of code points, with each code point being a sequence of bytes that is automatically terminated. A code point can be categorized as either a control or a literal.

Controls provide instructions for the interpreter to execute. A control is either an operator, which takes no arguments, a jump instruction, or a function call to a built-in, which may take arguments from multiple places.

Literals are integers, strings, or arrays, that get pushed onto the stack implicitly when the execution reaches that code point. These literals can then be transformed into other values and data types via controls.

## Execution Model
Every program starts at an instruction pointer (IP) value of 0 with a direction of "right," by default. As the interpreter executes each code point, it will attempt to advance to the next IP by incrementing/decrementing the IP value based on the current IP value and direction. There are many ways that the control flow may be redirected or interrupted via action at a distance. This differs from mainstream languages in that spaghetti code is much easier to write and maintainance of code requires careful consideration of the whole program. The direction of execution may also seemingly change unexpectedly if one is not careful! Thus, it is imperative that Precedence users fully understand the execution model of the interpreter, which will later be expanded upon in this section.

## Internals
There are four separate parts of the Precedence engine: the lexer, the parser, the interpreter, and the runtime. The lexer tokenizes the program into lexical tokens. The parser parses these tokens into a sequence of code points. The interpreter interprets these code points with the support of the runtime. The runtime manages the instruction pointer, the execution stack(s), built-in function calls, the loaded security profile(s), etc. These four parts must work together in a very intertwined way, but are separated like this to help reduce bugs in the engine.

## Documentation
Documentation is currently non-existent save for this design document. We have no timeline for documentation at the moment. Documentation should be released in three formats: pdf (latex), html/css, and markdown.
