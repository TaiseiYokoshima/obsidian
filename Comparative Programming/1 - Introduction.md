#### Imperative Languages
Programs are composed of  computational steps and functions are used to make the program modular. 

Features: 
- variables
- assignment
- loops
- recursion

Examples:
- C
- Pascal
- Fortran
#### Functional Languages
Based on mathematical theory of functions. The focus is on what is computed rather than how it should be computed. Functions are the primary expressions to interact and create data. 

Features:
- data immutability
- functions
- recursion

Examples:
- Haskell
- Scala
- Ocaml

#### Object-oriented Languages
Everything is represented as objects which can have hierarchies of behavior which can be grouped and computed as equals.  

Features:
- class 
- inheritance
- polymorphism 
- object

Examples 
- Java
- Python
- Ruby
#### Logic Languages
Programs are describe a program rather than defining an algorithmic implementation. The most well-known logic programming is Prolog. Constraint logic programming languages combine logic programming and constraint-solving
#### Definition of a programming language
1. Syntax
2. Semantics 
3. Implementation: a software system that can read a program and execute it in a machine, plus a set of tools (editors, debuggers, etc).
### Syntax
- Concrete Syntax: describes which chains of characters are well-formed programs
- Abstract Syntax: describes the syntax trees, to which a semantics is associated 

### Semantics 
The semantics of a language defines the meaning of programs. 
2 Types:
- Static Semantics (for example typing)
- Dynamic Semantics (meaning of the program)

### Styles of Semantics (Formal Methods)
- Denotational Semantics: A formal mathematical method that can be applied to expressions to portray the meaning of the constructs in an abstract and mathematical way. 

- Axiomatic Semantics: A formal mathematical method that can be applied to programs to reason about their correctness using axioms and inference rules. Uses axioms and deduction rules in a specific logic. Predicates or assertions are given before and after each construct, describing the constraints on program variables before and after the execution of the statement (precondition, post-condition).

- Operational Semantics: The meaning of each construct is given in terms of computation steps. The behavior of the program during execution can be described using a transition system (abstract machine)