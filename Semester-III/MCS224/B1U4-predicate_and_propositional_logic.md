# Predicate and Propositional Logic

## Propositional Logic

### Propositions
- A proposition (statement or assertion) is a sentence which is either always true or always false.
- **Example(Proposition)**
  - Earth revolves around the sun.
  - Water freezes at 100° Celsius.
  - 1 + 2 = 4
  - 2 is the only even prime number.
- **Example(Not a proposition)**
  - What is your name?
  - a + 5 = b
  - Let’s play football in the evening.
  - ∠X is an acute angle greater than 27° 

### Properties of propositional logic
- Propositional statements can be either true or false, they can’t be both simultaneously.
- Propositional logic is also referred to as binary logic as it works only on the two values 1 (True) and 0 (False)
- **Tautology**: Any proposition or statement which is always valid (true) is known as a tautology.
- **Contradiction**:Any proposition or statement which is always invalid (false) is known as a contradiction.
- **Truth Table**:A table listing all the possible truth values of a proposition is known as a truth table.

## Syntax of Propositional Logic

### Atomic Propositions
- These are simplest propositions containing a single proposition symbol and are either true or false.
- **Example**
  - Venus is the closest planet to the Sun in the solar system (F)
  - 7 – 3 = 4 (T)

### Compound Propositions
- They are formed by a collection of atomic propositions joined with logical connectives or logical operators.
- **Example**
  - The Sun is very bright today *and* its very hot outside.
  - Diana studies in class 8th *and* her school is in Karol Bagh

## Logical Connectives

Logical connectives are operators used to join two or more atomic propositions (operands). The logic and truth value of the obtained compound proposition depend on the input atomic propositions and the connective used.

### Conjunction
- **Definition**: A proposition “A ∧ B” with connective ∧ is known as the conjunction of A and B.
- **Truth Condition**: True only when both constituent propositions are true. If one of the input propositions is false, the output is also false.
- **Example**:
  - A = Ram is a playful boy.
  - B = Ram loves to play football.
  - A ∧ B = Ram is a playful boy and he loves to play football.

  - **Truth Table**
    | A     | B     | A ∧ B |
    |-------|-------|-------|
    | True  | True  | True  |
    | True  | False | False |
    | False | True  | False |
    | False | False | False |

### Disjunction
- **Definition**: A proposition “A ∨ B” with connective ∨ is known as the disjunction of A and B.
- **Truth Condition**: True when at least one of the constituent propositions is true. The output is false only when both input propositions are false.
- **Example**:
  - A = I will go to her house.
  - B = She will come to my house.
  - A ∨ B = I will go to her house or she will come to my house.

  -  **Truth Table**
    | A     | B     | A ∨ B |
    |-------|-------|-------|
    | True  | True  | True  |
    | True  | False | True  |
    | False | True  | True  |
    | False | False | False |

### Negation
- **Definition**: The proposition ¬A (or ~A) with connective ¬ (or ~) is known as the negation of A.
- **Truth Condition**: Negates the logic of the given proposition. If A is true, ¬A is false, and if A is false, ¬A is true.
- **Example**:
  - A = University is closed.
  - ¬A = University is not closed.

  -  **Truth Table**
    | A     | ¬A    |
    |-------|-------|
    | True  | False |
    | False | True  |

### Implication
- **Definition**: The proposition A → B with connective → is known as "A implies B". It is also called an if-then proposition.
- **Truth Condition**: True unless A is true and B is false.
- **Example**:
  - A = You score above 90%.
  - B = You will get a mobile phone.
  - A → B = If you score above 90%, you will get a mobile phone.

  -  **Truth Table**
    | A     | B     | A → B |
    |-------|-------|-------|
    | True  | True  | True  |
    | True  | False | False |
    | False | True  | True  |
    | False | False | True  |

### Bi-conditional
- **Definition**: A proposition A ⟷ B with connective ⟷ is known as a biconditional or if-and-only-if proposition.
- **Truth Condition**: True when both atomic propositions are either true or false.
- **Example**:
  - A = You will succeed in life.
  - B = You work hard.
  - A ⟷ B = You will succeed in life if and only if you work hard.

  -  **Truth Table**
    | A     | B     | A ⟷ B |
    |-------|-------|-------|
    | True  | True  | True  |
    | True  | False | False |
    | False | True  | False |
    | False | False | True  |

### Exclusive Disjunction (XOR)
- **Definition**: A proposition “A ⊕ B” with connective ⊕ is known as the exclusive disjunction (XOR) of A and B.
- **Truth Condition**: True only when exactly one of the constituent propositions is true.
- **Example**:
  - A = It's raining.
  - B = It's sunny.
  - A ⊕ B = It's either raining or sunny, but not both.

  -  **Truth Table**
    | A     | B     | A ⊕ B |
    |-------|-------|-------|
    | True  | True  | False |
    | True  | False | True  |
    | False | True  | True  |
    | False | False | False |

## Rule of Precedence for Logical Connectives

In propositional logic, the order of preference in which connectives are applied in a formula without brackets is as follows:

1. **Negation (~)**
   - Highest precedence. Applied first in the absence of brackets.

2. **Conjunction ( ∧ )**
   - Second in precedence. Applied after negation.

3. **Disjunction ( ∨ ) and Exclusive Disjunction ( ⊕ )**
   - Third in precedence. If both appear in a statement, apply the leftmost one first.

4. **Implication ( → ) and Biconditional ( ↔ )**
   - Fourth in precedence. Applied after conjunction, disjunction, and exclusive disjunction.

***Note:***
- "Inclusive or" (∨) and "exclusive or" (⊕) are both third in precedence. However, if both these appear in a statement, we first apply the left most one.
- "Implication" (→) and "biconditional" (↔) are both fourth in precedence. However, if both these appear in a statement, we first apply the left most one.

***Example usage:*** In the expression p ∨ q ⊕ ~p, apply ∨ first due to its leftmost position in the expression.

