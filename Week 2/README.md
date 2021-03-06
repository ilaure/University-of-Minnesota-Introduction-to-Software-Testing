# Week 2
## Dependability Quiz
1. What is the time ordering (in terms of when a mistake is made or occurs in the running system) of the following: (1) an error, (2) a fault, and (3) a failure?  
**2,1,3**  
2. Testing helps with which kind of dependability criteria?  
**error removal**  
3. Availability is the same as reliability.  
**False**  
4. A correct system (with respect to its requirements) will be safe.  
**False**  
5. A correct system will be reliable.  
**True**  
6. Robust systems are reliable.  
**False**  
7. Safe systems are robust.  
**False**  

## Testing Principles: Where
1. Why do floating point numbers sometimes lead to erroneous code?
- [x] Arithmetic on floating point numbers is often approximate, so it can introduce errors
- [x] Floating point numbers have values that are not actually numbers, such as infinity and NaN (not a number), that can cause computations to behave strangely.
- [x] As floating point computations are approximate, equality comparisons fail after computations that would succeed when using real numbers

2. Why do relational boundaries sometimes lead to erroneous code?
- [x] Programmers often make 'off-by-one' errors
- [x] Determining strict limits on ranges is difficult in requirements engineering
- [x] Relational boundaries define points of discontinuity for programs

3. Why do casts sometimes lead to erroneous code?
- [x] When converting an integer to a smaller bit length (e.g. long to int), the value may be truncated.
- [x] When converting to a larger bit length (e.g., int to long), the value may change from positive to negative.
- [x] When converting from signed to unsigned types (e.g., int to byte), negative numbers can't be represented.
- [x] When converting from a double to int, the value is truncated to a whole number.

## Testing Principles: How
1. Why are we often able to test more rigorously at the unit level rather than the system level?
- [x] The tests tend to run faster, so we can run more of them.
- [x] We can usually see more of the internal state at the unit level so we can build stronger oracles.

2. When we say that we want redundant verification, what do we mean?
- [x] We want several different verification techniques checking the same program or subsystem.

3. Which of the following are good ways to work with developers to reduce systematic errors?
- [x] Create libraries or utility functions to encapsulate operations that developers tend to get wrong.
- [x] Create checklists for developers based on the most common errors seen in test.
- [x] Use languages / IDEs that eliminate certain classes of errors by compile-time checks.
- [x] Create tools to test/verify specific kinds of common errors.

4. We state that programs, as well as tests, can be flakey.  What does it mean for a program to be flakey?
- [x] Given the same inputs, sometimes the program fails a test and other times it does not.

5. Why is observability an important issue in testing?
- [x] If a program error is transient (it happens and is masked out by other code), you might not be able to "see" it and the test may pass.
- [x] Often programs are stateful - that is, a test may trigger an error, but it only becomes visible as an output if a long sequence of steps are executed, whereas it might be immediately visible by examining internal state.
