# Theory of Computation

## Table of Contents
- [Chapter 01: Finite Automata & Regular Expression](#chapter-01-finite-automata--regular-expression)
  - [Finite State Machines](#finite-state-machines)
  - [Deterministic and Nondeterministic Finite Automata (DFA and NDFA)](#deterministic-and-nondeterministic-finite-automata-dfa-and-ndfa)
  - [Mealy & Moore Machines](#mealy--moore-machines)
  - [Regular Expressions](#regular-expressions)
  - [Pumping Lemma](#pumping-lemma)
- [Chapter 02: Context-Free Grammars (CFG)](#chapter-02-context-free-grammars-cfg)
  - [CFG Basics](#cfg-basics)
  - [Parsing and Ambiguity](#parsing-and-ambiguity)
- [Chapter 03: Pushdown Automaton (PDA)](#chapter-03-pushdown-automaton-pda)
  - [Nondeterministic PDA](#nondeterministic-pda)
  - [Deterministic PDA](#deterministic-pda)
- [Chapter 04: Turing Machines](#chapter-04-turing-machines)
  - [Introduction](#introduction)
  - [Universal TM & Other Modifications](#universal-tm--other-modifications)
- [Chapter 05: Tractable and Untractable Problems](#chapter-05-tractable-and-untractable-problems)
  - [Complexity Classes](#complexity-classes)

---

## Chapter 01: Finite Automata & Regular Expression

### Finite State Machines
Finite State Machines (FSM) are a computational model used to design computer programs and sequential logic circuits. An FSM is composed of:
- **States**: Different configurations of the machine.
- **Transitions**: Rules for moving from one state to another.
- **Alphabet**: A set of symbols that the machine reads.
- **Basic Machine**: Fundamental concepts of states and transitions.
- **Transition Graph**: A visual representation of states and transitions.
- **Transition Matrix**: A matrix representing state transitions.

### Deterministic and Nondeterministic Finite Automata (DFA and NDFA)
- **DFA**: Every state has exactly one transition for each symbol in the alphabet.
- **NDFA**: States can have zero, one, or multiple transitions for each symbol.
- **Equivalence of DFA and NDFA**: Both recognize the same set of regular languages.
- **Decision Properties**: Important properties like emptiness, finiteness, and membership.
- **Minimization of Finite Automata**: Techniques to reduce the number of states in DFA.
  
### Mealy & Moore Machines
- **Mealy Machines**: Output is determined by the current state and the input symbol.
- **Moore Machines**: Output is determined only by the current state.

### Regular Expressions
- **Alphabet, Words, and Operations**: Fundamental components of regular expressions.
- **Relationship and Conversion**: Converting between finite automata and regular expressions.
- **Designing Regular Expressions**: Crafting expressions to match patterns.
- **Closure Properties of Regular Sets**: Properties under operations like union, intersection, and concatenation.

### Pumping Lemma
- **Application of Pumping Lemma**: Used to prove certain languages are not regular.
- **Power of Languages**: Understanding the limitations of regular languages.

## Chapter 02: Context-Free Grammars (CFG)

### CFG Basics
- **Derivations and Languages**: Generating strings from the grammar.
- **Relationship Between Derivation and Derivation Trees**: Visualizing derivations.
- **Leftmost and Rightmost Derivation**: Different strategies for deriving strings.
- **Sentential Forms**: Intermediate forms during derivation.

### Parsing and Ambiguity
- **Simplification of CFG**: Removing useless, nullable, and unit productions.
- **Normal Forms**: Converting to Greibach Normal Form (GNF) and Chomsky Normal Form (CNF).
- **Problems Related to CNF and GNF**: Challenges and solutions.
- **Membership Problem**: Determining if a string belongs to a language.

## Chapter 03: Pushdown Automaton (PDA)

### Nondeterministic PDA
- **Definitions**: Introduction to PDAs and their components.
- **PDA and Context-Free Languages (CFL)**: PDAs recognize CFLs.
- **CFG for PDA**: Constructing PDAs for given CFGs.

### Deterministic PDA
- **Deterministic PDA and Deterministic CFL**: Understanding deterministic context-free languages.
- **The Pumping Lemma for CFLs**: Proving languages are not context-free.
- **Closure Properties and Decision Properties for CFLs**: Important properties of CFLs.

## Chapter 04: Turing Machines

### Introduction
- **Definition of Turing Machine (TM)**: Basic components and operation.
- **TM as Language Acceptors and Transducers**: TMs accept languages and compute functions.
- **Computable Languages and Functions**: Languages that can be recognized by TMs.

### Universal TM & Other Modifications
- **Multiple Tracks Turing Machine**: TMs with multiple tapes.
- **Hierarchy of Formal Languages**: Classification of languages.
- **Recursive & Recursively Enumerable Languages**: Definitions and properties.
- **Properties of RL and REL**: Important characteristics.
- **Introduction to Context-Sensitive Grammars and Languages**: More powerful than CFGs.
- **The Chomsky Hierarchy**: Four levels of languages.

## Chapter 05: Tractable and Untractable Problems

### Complexity Classes
- **P, NP, NP-complete, and NP-hard Problems**: Understanding computational complexity.
- **Undecidability**: Problems that cannot be solved by TMs.
- **Examples of Problems**: Examples like vertex cover, Hamiltonian path, and traveling salesman problem.

---

## References
- [Automata Theory (Wikipedia)](https://en.wikipedia.org/wiki/Automata_theory)
- [Introduction to the Theory of Computation by Michael Sipser](https://www.amazon.com/Introduction-Theory-Computation-Michael-Sipser/dp/113318779X)
- [Formal Languages and Automata (MIT OpenCourseWare)](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-045j-automata-computability-and-complexity-spring-2011/)
