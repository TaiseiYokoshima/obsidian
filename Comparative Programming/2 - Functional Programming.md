### General Concepts 
- Functional programs consist entirely of functions 
- A function can be defined in terms of other functions
- The focus is in what is to be computed, not how it should be computed
- Often strongly typed (no run-time type errors) and have built-in memory management
- Advantages: shorter programs, easier to understand, easier to design and maintain than imperative programs
- Disadvantage: can be slower than imperative programs

### Properties 
1. Unicity of normal forms:
	In (pure) functional languages the value of an expression is uniquely determined by its components, and is independent of the order of reduction. Advantage: readability of programs. 
2. Non-termination:
	Not all reduction sequences lead to a value, some reduction sequences do not terminate

### Strategies 
- The normal form is unique, but the order of reductions is important. 
- The strategy of evaluation defines the reduction sequence that the language implements.
- Most popular strategies: 
1. Call-by-name (Normal order): reduce first the application using the definition of the function, and then the argument 
2. Call-by-value (Applicative order): evaluate first the argument and then the application using the definition of the function

### Strategies, continued
- Different strategies require different number of reduction steps (efficiency)
- Call-by-name always finds the value, if there is one.
- Call-by-value is in general more efficient, but may final to find a value.
- Haskell uses a strategy called lazy evaluation, which guarantees that if an expression has a normal form, the evaluator will find it. 
	lazy evaluation = call-by-name + sharing 




