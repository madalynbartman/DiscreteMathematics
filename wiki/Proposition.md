# Truth Value and Proposition
## Proposition
An equation or a statement that holds a truth value that can be derived with objective standards (normally represented as p, q, r, etc)
## Truth Value
The attribute assigned to a proposition in respect of its truth(**T**) or falsehood(**F**)

### Examples
1. The capital of the United States is Washington, D.C

   **This is a proposition and it is true.**

2. x + 1 = 2

   **This is not a proposition as the equation can be true/false depending on the x value**

3. 1 + 1 = 3 

   **This is a proposition and it is false**

4. There is more than one integer n such that 2^n = n^2

   **This is a proposition and it is true (n = 2, 4)**

5. For all real numbers a, there is only one solution to a^2 = 1
 
   **This is a proposition and it is false (a = 1, -1)**

6. x = y

   **This is not a proposition since the truth value cannot be determined as the ranges of values for x and y are not suggested**

# Logical Operation and Compound Proposition
## Negation(NOT): ~p or ¬p
negation of a proposition reverses the truth value of that proposition.

|  p  | ¬p |
|-----|------|
|  T  |  F |
|  F  |  T |

### Examples
Negate the propositions and find the resulting truth value

1. p: 4 is a positive integer

   **¬p: 4 is not a positive integer, F**

2. q: 3 + 5 = 4

   **¬q: 3 + 5 ≠ 4, T**

3. r: New York is in the United States

   **¬r: New York is not in the United States, F**

## Conjunction(AND): p ∧ q
When statements p and q are propositions, **p ∧ q is only true when both p and q are true**

| p | q | p ∧ q |
|-----|------|---|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

### Examples
Use conjunction to combine given propositions and find the resulting truth value

1. p: 4 is a positive integer, q: 2+6 = 0

   **p ∧ q = F since 2 + 6 = 8**

2. r: New York is in the United States, s: Vancouver is in Canada

   **r ∧ s = T since both propositions are true**

## Disjunction(OR): p ∨ q
When statements p and q are propositions, **only one needs to be true for p ∨ q to be true**

| p | q | p ∨ q |
|-----|------|---|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

### Examples
Use disjunction to combine given propositions and find the resulting truth value

1. p: 4 is a positive integer, q: 2+6 = 0

   **p ∨ q = T since p is true**

2. r: New York is in the United States, s: Vancouver is in Canada

   **r ∨ s = T since both propositions are true**

## Exclusive OR(XOR): p ⊕ q
When statements p and q are propositions, **p ⊕ q is only true when exactly only one proposition is true**

| p | q | p ⊕ q |
|-----|------|---|
| T | T | F |
| T | F | T |
| F | T | T |
| F | F | F |

XOR can be also expressed using AND, OR, and NOT

 p ⊕ q ≡ (¬p ∧ q) V (p ∧ ¬q)

| p | q |p ⊕ q | ¬p | ¬q | ¬p ∧ q | p ∧ ¬q |(¬p ∧ q) V (p ∧ ¬q)|
|---|---|-------|----|----|--------|--------|--------------------|
| T | T |   **F**   | F | F | F | F | **F** |
| T | F |   **T**   | F | T | F | T | **T** | 
| F | T |   **T**   | T | F | T | F | **T** |
| F | F |   **F**   | T | T | F | F | **F** | 

This is called [Logical Equivalence](https://github.com/jongwoojeff/DiscreteMathematics/wiki/Logical-Equivalence)

# How to approach a compound proposition
pro tip when you are faced with a complex ugly looking compound proposition

Follow the priorities!

1. brackets ()
2. negation ¬
3. conjunction ∧
4. disjunction V

### Example
Construct a truth table for ¬(p ∧ q) ⊕ (¬p V q)

From left to right following the priorities ->

| p | q | ¬p | p ∧ q | ¬(p ∧ q) | ¬p V q |¬(p ∧ q) ⊕ (¬p V q)
|---|---|----|----|--------|--------|--------------------|
| T | T | F | T | F | T | **T** |
| T | F | F | F | T | F | **T** | 
| F | T | T | F | T | T | **F** |
| F | F | T | F | T | T | **F** | 

# Types of compound proposition
## Tautology(T)
Always true no matter what the individual parts are.

## Contradiction(F)
Always false no matter what the individual parts are.

## Contingency
Neither true nor false; truth value changes based on the individual parts.

### Examples
Determine the type
1. ¬p

|  p  | ¬p |
|-----|------|
|  T  |  F |
|  F  |  T |

**Contingency**

2. p ∨ ¬p

| p | ¬p | p ∨ ¬p |
|-----|------|---|
| T | F | T |
| F | T | T |

**Tautology**

3. p ∧ ¬p

| p | ¬p | p ∧ ¬p |
|-----|------|---|
| T | F | F |
| F | T | F |

**Contradiction**

# Conditional Proposition / Implication: p → q

p → q can be translated as:

* if p, then q
* p implies q
* p is sufficient for q
* p only if q
* q is necessary for p

**p → q is only false when p is true and q is false**

| p | q | p → q |
|-----|------|---|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

### Example
Determine the truth table

(¬p V r) → ¬q

[follow the priorities!](https://github.com/jongwoojeff/DiscreteMathematics/wiki/Proposition#how-to-approach-a-compound-proposition)

| p | q | r | ¬p | ¬q | ¬p V r |(¬p V r) → ¬q
|---|---|----|----|--------|--------|--------------------|
| T | T | T | F | F | T | **F** |
| T | T | F | F | F | F | **T** | 
| T | F | T | F | T | T | **T** |
| T | F | F | F | T | F | **T** | 
| F | T | T | T | F | T | **F** |
| F | T | F | T | F | T | **F** | 
| F | F | T | F | T | T | **T** |
| F | F | F | T | T | T | **T** | 

## Biconditional Proposition: p ↔ q

p ↔ q can be translated as

* p is necessary and sufficient for q
* if p then q, and conversely
* p if and only if q

p ↔ q is only true when both truth values are equal 

| p | q | p ↔ q |
|-----|------|---|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | T |

**Updated priorities for approaching compound propositions**

1. brackets ()
2. negation ¬
3. conjunction ∧
4. disjunction V
5. one way implication →
6. both ways implication ↔

### Examples
Determine the truth table and its type

1. [p ∧ (p → q)] → q

| p | q | p → q | p ∧ (p → q) | [p ∧ (p → q)] → q |
|---|---|----|----|--------|
| T | T | T | T | T |
| T | F | F | F | T |
| F | T | T | F | T |
| F | F | T | F | T |

**Tautology**

2. ¬p ↔ (p V ¬p)

| p | ¬p | p V ¬p | ¬p ↔ (p V ¬p) |
|-----|------|---|---|
| T | F | T | F |
| F | T | T | T |

**Contingency**

3. (p ↔ ¬q) ∧ (p ∧ q)

| p | q | ¬q | p ↔ ¬q | p ∧ q |(p ↔ ¬q) ∧ (p ∧ q)|
|---|---|----|----|--------|--------|
| T | T | F | F | T | F |
| T | F | T | T | F | F |
| F | T | F | T | F | F |
| F | F | T | F | F | F |

**Contradiction**

# Converse, Inverse, and Contraposition
For proposition p → q
## Converse
Switch hypothesis and result

**q → p**
## Inverse
Negate the whole proposition

**¬p → ¬q**
## Contraposition
Converse then Inverse

**¬q → ¬p**

| p | q | p → q | q → p (con) | ¬p → ¬q (in) |¬q → ¬p (contra)|
|---|---|----|----|--------|--------|
| T | T | T | T | T | T |
| T | F | F | T | T | F |
| F | T | T | F | F | T |
| F | F | T | T | T | T |


### Example
Determine the converse, inverse, and contraposition of a proposition and their truth vales

**For an integer x, if x >= 50, then x <= 30. Solve for x = 70, 23, 46**


Original: if x >= 50, then x <= 30

Converse: if x <= 30, then x >= 50

Inverse: if x < 50, then x > 30

Contraposition: if x > 30, then x < 50


x = 70


**Original: False**

**Converse: True**

**Inverse: True**

**Contraposition: False**


x = 23


**Original: True**

**Converse: False**

**Inverse: False**

**Contraposition: True**


x = 46


**Original: True**

**Converse: False**

**Inverse: True**

**Contraposition: True**

