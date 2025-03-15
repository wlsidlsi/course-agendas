# I. Introduction to Automata Theory

## Understanding Basic Concepts

### Alphabets, Strings, and Languages
*   Definition of an alphabet as a finite, non-empty set of symbols.
    *   Example: Σ = {0, 1}
*   Definition of a string as a finite sequence of symbols from an alphabet.
    *   Example: "01011" is a string over Σ = {0, 1}
*   Definition of a language as a set of strings over an alphabet.
    *   Example: L = {“0”, “1”, “00”, “11”, “01”, “10”}

### Formal Language Operations
*   Union: L1 ∪ L2 = {x | x ∈ L1 or x ∈ L2}
*   Concatenation: L1L2 = {xy | x ∈ L1 and y ∈ L2}
*   Kleene Star: L\* = {ε} ∪ L ∪ LL ∪ LLL ∪ ...

## Introduction to Automata
*   Definition of an automaton as an abstract machine model.
*   States, transitions, and input alphabet.
*   Deterministic vs. Nondeterministic Automata.

# II. Finite Automata (FA)

## Deterministic Finite Automata (DFA)

### Definition of DFA
*   Formal definition: A DFA is a 5-tuple (Q, Σ, δ, q0, F), where:
    *   Q is a finite set of states.
    *   Σ is a finite input alphabet.
    *   δ: Q x Σ → Q is the transition function.
    *   q0 ∈ Q is the initial state.
    *   F ⊆ Q is the set of accept states.

### DFA Transition Diagrams and Tables
*   Constructing and interpreting transition diagrams.
*   Creating transition tables from diagrams and vice versa.
*   Example: DFA that accepts strings ending in '0'.

### DFA Acceptance of Strings
*   How a DFA processes an input string.
*   Definition of acceptance: a string is accepted if the DFA ends in an accept state after processing the entire string.
*   Example: Trace the execution of a DFA with input "110".

## Nondeterministic Finite Automata (NFA)

### Definition of NFA
*   Formal definition: An NFA is a 5-tuple (Q, Σ, δ, q0, F), where:
    *   Q is a finite set of states.
    *   Σ is a finite input alphabet.
    *   δ: Q x (Σ ∪ {ε}) → P(Q) is the transition function (P(Q) is the power set of Q).
    *   q0 ∈ Q is the initial state.
    *   F ⊆ Q is the set of accept states.
*   ε-transitions: Transitions without consuming an input symbol.

### NFA Transition Diagrams
*   Constructing and interpreting NFA transition diagrams.
*   Example: NFA that accepts strings containing "101".

### NFA Acceptance of Strings
*   Multiple possible paths for a given input.
*   Acceptance occurs if *any* path leads to an accept state.
*   Example: Trace the execution of an NFA with input "01011".

## DFA and NFA Equivalence

### Subset Construction Algorithm
*   Converting an NFA to an equivalent DFA using subset construction.
*   Understanding the power set construction.
*   Step-by-step example: Converting an NFA recognizing (a|b)\*abb to a DFA.

### Minimization of DFA
*   Identifying and merging equivalent states.
*   Table-filling algorithm for DFA minimization.
*   Example: Minimizing a given DFA.

# III. Regular Expressions (RE)

## Definition and Syntax of Regular Expressions
*   Basic regular expressions: ε, a (where a ∈ Σ).
*   Operators: concatenation, union (|), Kleene star (\*).
*   Precedence of operators.
*   Examples: `a*`, `(a|b)`, `a(bb)*a`.

## Regular Expression Examples

### Constructing Regular Expressions
*   Writing REs for specific languages.
*   Example: RE for strings starting with "a" and ending with "b": `a(a|b)*b`.
*   Example: RE for strings containing at least two "a"s: `(a|b)*a(a|b)*a(a|b)*`.

### Regular Expression Identities
*   Identities involving union, concatenation, and Kleene star.
*   Using identities to simplify regular expressions.
*   Examples: `L ∪ Ø = L`, `Lε = L`.

## Relationship Between Regular Expressions and Finite Automata

### Converting Regular Expressions to NFAs
*   Thompson's construction algorithm.
*   Step-by-step application of Thompson's construction.
*   Example: Convert `(a|b)*abb` to an NFA.

### Converting Finite Automata to Regular Expressions
*   Using state elimination or dynamic programming approaches.
*   Example: Converting a simple DFA to a regular expression.

# IV. Context-Free Grammars (CFG)

## Definition of Context-Free Grammars

### Components of a CFG
*   Variables (non-terminals): A finite set of symbols that can be replaced by other variables or terminals.
*   Terminals: A finite set of symbols that form the strings of the language.
*   Production rules: Rules of the form A → α, where A is a variable and α is a string of variables and terminals.
*   Start variable: A designated variable that starts the derivation.

### Formal Definition
*   A CFG is a 4-tuple (V, Σ, R, S), where:
    *   V is a finite set of variables.
    *   Σ is a finite set of terminals.
    *   R is a finite set of production rules.
    *   S ∈ V is the start variable.

### Derivations
*   Leftmost and rightmost derivations.
*   Derivation trees (parse trees).
*   Example: CFG for balanced parentheses:
    *   S → SS | (S) | ε

## Ambiguity in CFGs

### Definition of Ambiguity
*   A CFG is ambiguous if there exists a string in the language that has multiple distinct derivation trees (or leftmost/rightmost derivations).
*   Example: A CFG for arithmetic expressions that doesn't specify operator precedence can be ambiguous.

### Resolving Ambiguity
*   Rewriting the grammar to enforce precedence and associativity.
*   Example: Removing ambiguity from an arithmetic expression grammar.

## Normal Forms for CFGs

### Chomsky Normal Form (CNF)
*   All production rules are of the form A → BC or A → a, where A, B, and C are variables and a is a terminal.
*   Algorithm for converting a CFG to CNF.
*   Steps: Eliminate ε-productions, unit productions, and useless symbols; then, adjust remaining productions.

### Greibach Normal Form (GNF)
*   All production rules are of the form A → aα, where A is a variable, a is a terminal, and α is a string of variables.
*   Less commonly used, but useful for certain parsing algorithms.

# V. Pushdown Automata (PDA)

## Definition of Pushdown Automata

### Components of a PDA
*   States, input alphabet, stack alphabet, transition function, initial state, initial stack symbol, accept states.
*   Formal definition: A PDA is a 7-tuple (Q, Σ, Γ, δ, q0, Z0, F), where:
    *   Q is a finite set of states.
    *   Σ is a finite input alphabet.
    *   Γ is a finite stack alphabet.
    *   δ: Q x (Σ ∪ {ε}) x (Γ ∪ {ε}) → P(Q x Γ\*) is the transition function.
    *   q0 ∈ Q is the initial state.
    *   Z0 ∈ Γ is the initial stack symbol.
    *   F ⊆ Q is the set of accept states.

### PDA Transition Diagrams
*   Visual representation of PDA transitions.
*   Labeling edges with input symbol, stack symbol to be popped, and stack symbol(s) to be pushed.

### PDA Acceptance of Strings
*   Acceptance by final state: The PDA enters an accept state after processing the entire string.
*   Acceptance by empty stack: The PDA empties its stack after processing the entire string.
*   Example: PDA for language {w c wR | w ∈ {a, b}*}, accepting by empty stack.

## Equivalence of CFGs and PDAs

### Converting CFGs to PDAs
*   Algorithm for constructing a PDA from a given CFG.
*   Example: Converting the balanced parentheses grammar to a PDA.

### Converting PDAs to CFGs
*   More complex than the CFG-to-PDA conversion.
*   Involves creating variables to represent all possible transitions between states with specific stack symbols.

# VI. Turing Machines (TM)

## Definition of Turing Machines

### Components of a TM
*   States, input alphabet, tape alphabet, transition function, initial state, blank symbol, accept state, reject state.
*   Formal definition: A TM is a 7-tuple (Q, Σ, Γ, δ, q0, qaccept, qreject), where:
    *   Q is a finite set of states.
    *   Σ is a finite input alphabet (does not contain the blank symbol).
    *   Γ is a finite tape alphabet (Σ ⊆ Γ, Γ contains the blank symbol '⊔').
    *   δ: Q x Γ → Q x Γ x {L, R} is the transition function.
    *   q0 ∈ Q is the initial state.
    *   qaccept ∈ Q is the accept state.
    *   qreject ∈ Q is the reject state.

### TM Transition Diagrams
*   Representing TM transitions graphically.
*   Edges labeled with input symbol, symbol to write, and direction to move.

### TM Acceptance of Strings
*   A TM accepts a string if it enters the qaccept state.
*   A TM rejects a string if it enters the qreject state.
*   A TM can also loop infinitely.

## TM Examples
### TM for recognizing {0^n 1^n | n >= 0}
*   Design a TM that accepts strings with an equal number of 0s and 1s, in that order.

### TM for incrementing a binary number
*   Design a TM that takes a binary number as input and outputs the number incremented by one.

## Variants of Turing Machines

### Multitape Turing Machines
*   Turing machines with multiple tapes and read/write heads.
*   Any multitape TM can be simulated by a single-tape TM.

### Nondeterministic Turing Machines
*   Turing machines with nondeterministic transition functions.
*   Any nondeterministic TM can be simulated by a deterministic TM.

## Undecidability

### The Halting Problem
*   The problem of determining whether a given Turing machine will halt (accept or reject) on a given input.
*   The Halting Problem is undecidable: There is no Turing machine that can solve the Halting Problem for all possible inputs.

### Reducibility
*   Using reducibility to prove that other problems are undecidable.
*   If problem A can be reduced to problem B, and problem A is undecidable, then problem B is also undecidable.
