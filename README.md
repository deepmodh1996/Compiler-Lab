# Compiler-Lab

This repository contains work done during Spring 2017 as part of "Implementation of Programming Languages Lab" course.

Since copyrights are reserved by [Prof. Uday Khedker](https://www.cse.iitb.ac.in/~uday/), I am only maintaing brief a summary of assignments which are based on "[sclp: A Language Processor for a Subset of C](https://www.cse.iitb.ac.in/~uday/sclp-web/)" created by him. (Link can be accessed publicaly as of May 2017.)

| Assignment |  Content |
|:------:|:------|
| 1 | Declaration and Assignment |
| 2 | Arithmatic Expression |
| 3 | Control Flow, Conditional Expression and Relational Expression |
| 4 | Intermediate Code Generation and C++ Style Commenting |
| 5 | Optimization using [Live Variable Analysis](https://en.wikipedia.org/wiki/Live_variable_analysis) |
| 6 | Functions, Assembly Code Generation and Print |

In each assignment entire compiler is implemented including AST, intermediate code and assembly code for SPIM.

Functionality supported by language is augmented in later assignment.

### Assignment 1 : Declaration and Assignment

In this assignment, language consists of a (possibly empty) list of global declaration statements followed by the definition of the main procedure.

Main procedure consists of a (possibly empty) list of local declaration statements followed by a (possibly empty) list of assignment statements containing only integer data type.

### Assignment 2 : Arithmatic Expression

Apart from integers, single precision floating point types (introduced by the type specifier float) are supported.

Arithmatic Expressions are included. Expressions appearing in the right hand side of an assignment may contain the following arithmetic operators:  +, -, *, /, and unary minus. The expressions do not have any side effects.

### Assignment 3 : Control Flow, Conditional Expression and Relational Expressions

Conditional expression e1?e2:e3, while, do-while, if, and if-else statements are allowed. 

'for' statement is implemented for bonus marks.

The boolean conditions controlling the control flow consist of the six relational operators (<, <=, >, >=, ==, and !=) and three logical operators (&&, ||, and !). Type overloading is emited.
    

### Assignment 4 : Intermediate Code Generation and C++ Style Commenting

Type declaration statement now supports a comma separated list. C++ style comments beginning with // and stretching upto the end of a line are supported.

Complete intermediate code is generated in out.ic along with abstract syntax trees in out.ast file.

### Assignment 5 : Optimization using [Live variable analysis](https://en.wikipedia.org/wiki/Live_variable_analysis) 

Optimize the intermediate code using live variable analysis to to remove unnecessary assignments. Control flow graph of entire code must be created.

Quick example of Optimization : If snippet of code contains a = c + 2; b = 3; a = b; Here a = c + 2 is not required because 'a' is not used before its next assignment. It may lead to removal of assignments of 'c' if it is not used elsewhere.

### Assignment 6 : Functions, Assembly Code Generation and Print

Function calls (including recursion) are supported. 

Multiple functions which may take arguments and may return results. Function calls may appear as operands in expression.

Assembly code in SPIM must be created which is tested by running it on QtSpim. Print statements are supported which takes expression or string or function call as argument which will be printed on console.
