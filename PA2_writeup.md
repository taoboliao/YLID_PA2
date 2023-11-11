# PA2

Greetings,

This document serves as the writeup of your second programming assignment. Within the scope of this assignment, you are expected to implement a somehow intricate class structrue. We will talked about the strucure in detail later, but now, let's focus on things that are more basic.

## Boolean operand   

We've talked about some of the boolean algebra (acctually more than enough for this assignment) in the class, which invovles 6 opperation:   

### Conjunction (AND, ∧)   
| A | B | A and B |
|---|---|-------------|
| 0 | 0 | 0           |
| 0 | 1 | 0           |
| 1 | 0 | 0           |
| 1 | 1 | 1           |

### Disjunction (OR, ∨)   
| A | B | A or B |
|---|---|------------|
| 0 | 0 | 0          |
| 0 | 1 | 1          |
| 1 | 0 | 1          |
| 1 | 1 | 1          |

### Exclusive Disjunction (XOR, ⊕)   
| A | B | A xor B |
|---|---|--------------|
| 0 | 0 | 0            |
| 0 | 1 | 1            |
| 1 | 0 | 1            |
| 1 | 1 | 0            |

### Implication (IMPLIES, →)   
| A | B | A -> B |
|---|---|-------------------|
| 0 | 0 | 1                 |
| 0 | 1 | 1                 |
| 1 | 0 | 0                 |
| 1 | 1 | 1                 |

### Negation (NOT, ¬)   
| A | not A |
|---|--------|
| 0 | 1      |
| 1 | 0      |

### Equivalence (IFF, ↔)
| A | B | A iff B |
|---|---|-----------------------|
| 0 | 0 | 1                     |
| 0 | 1 | 0                     |
| 1 | 0 | 0                     |
| 1 | 1 | 1                     |

In this assignment, one of your task is to correctly return the values of each of them.

## Arithmetic opperand   
We'll also implement 5 of the basic arithmetic opperand, which are: +, -, *, /, and negative. Those will function as normal as our daily usage.

## Structure to be implemented:   
![微信图片_20231111150934](https://github.com/taoboliao/YLID_PA2/assets/59666193/92e5281a-7262-4984-a42c-8aacfd244969)

It looks terrible at first glance, but let's break it down:   
```This is the workflow that I suggest you to follow, but you can also implement the structure in any order you want.```   
- Complete Derived Classes for Values: You'll need concrete classes for IntegerValue and BooleanValue. These classes represent the basic values in your expressions and will be the leaves of your expression tree. They'll override the evaluate() method to return their internal value.

- Implement Arithmetic and Binary Expressions: Create classes and their constructor for each of the operations like conjunction, disjunction, sum, etc. These classes will contain references to other Expression instances representing the operands.

- Evaluation Method: Each class representing an operation will implement the evaluate() method to perform its specific computation. For binary operations, this typically involves calling evaluate() on the left and right operands and then combining the results according to the operation's logic.

- Error Handling: Consider how you will handle errors, such as type mismatches (e.g., trying to perform a boolean operation on integers) or undefined operations. Note if an error occurs here, we simply return a null and let system to handle that.


- Testing: Write unit tests for each class and operation to ensure that expressions are evaluated correctly. Testing can help you catch edge cases and errors in logic.

## Deadline
This homework is due Nov. 17 Friday at 11:59 p.m. With the late due Nov. 18 Saturday 11:59 a.m.   
# Turn in
Send your Programming_Assignment2 file/package to two instructors privately by Wechat.   
