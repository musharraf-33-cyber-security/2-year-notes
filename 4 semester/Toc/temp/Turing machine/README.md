
# Turing Machine in TOC


Turing Machine was invented by Alan Turing in 1936 and it is used to accept Recursive Enumerable Languages (generated by Type-0 Grammar).

Turing machines are a fundamental concept in the theory of computation and play an important role in the field of computer science. They were first described by the mathematician and computer scientist Alan Turing in 1936 and provide a mathematical model of a simple abstract computer.

In the context of automata theory and the theory of computation, Turing machines are used to study the properties of algorithms and to determine what problems can and cannot be solved by computers. They provide a way to model the behavior of algorithms and to analyze their computational complexity, which is the amount of time and memory they require to solve a problem.

A Turing machine is a finite automaton that can read, write, and erase symbols on an infinitely long tape. The tape is divided into squares, and each square contains a symbol. The Turing machine can only read one symbol at a time, and it uses a set of rules (the transition function) to determine its next action based on the current state and the symbol it is reading.

The Turing machine’s behavior is determined by a finite state machine, which consists of a finite set of states, a transition function that defines the actions to be taken based on the current state and the symbol being read, and a set of start and accept states. The Turing machine begins in the start state and performs the actions specified by the transition function until it reaches an accept or reject state. If it reaches an accept state, the computation is considered successful; if it reaches a reject state, the computation is considered unsuccessful.

Turing machines are an important tool for studying the limits of computation and for understanding the foundations of computer science. They provide a simple yet powerful model of computation that has been widely used in research and has had a profound impact on our understanding of algorithms and computation.

A Turing machine consists of a tape of infinite length on which read and writes operation can be performed. The tape consists of infinite cells on which each cell either contains an input symbol or a special symbol called blank. It also consists of a head pointer which points to the cell currently being read and it can move in both directions.






<img src="![image](https://github.com/user-attachments/assets/fb68225a-ef12-47f3-9c85-55bc59b8e71a)" width="700" height="500">



## Figure: Turing Machine

A TM is expressed as a 7-tuple (Q, T, B, Σ, δ, q0, F) where:
- Q is a finite set of states
- T is the tape alphabet (symbols which can be written on Tape)
- B is the blank symbol (every cell is filled with B except input alphabet initially)
- Σ is the input alphabet (symbols which are part of input alphabet)
- δ is a transition function which maps Q × T → Q × T × {L,R}. Depending on its present state and present tape alphabet (pointed by head pointer), it will move to a new state, change the tape symbol (may or may not) and move the head pointer to either left or right.
- q0 is the initial state
- F is the set of final states. If any state of F is reached, the input string is accepted.

## Example: Constructing a Turing Machine for L={0^n1^n | n>=1}
- Q = {q0, q1, q2, q3} where q0 is the initial state.
- T = {0, 1, X, Y, B} where B represents blank.
- Σ = {0, 1}
- F = {q3}
- Transition function δ is given in Table 1 as :

![image](https://github.com/user-attachments/assets/1963e4d6-8bc8-4dce-92d9-57de0ce12e52)

  

##                                            Illustration
Let us see how this Turing machine works for `0011`. Initially, the head points to 0 which is underlined and the state is q0 as:

 ![image](https://github.com/user-attachments/assets/278a633e-c7a1-42b2-a4a8-5fe4c8963edc)


The move will be δ(q0, 0) = (q1, X, R). It means it will go to state q1, replace 0 by X and the head will move to the right as:


![image](https://github.com/user-attachments/assets/b3cf36b5-0b01-47f8-8334-fdbfeab0770e)

 

The move will be δ(q1, 0) = (q1, 0, R) which means it will remain in the same state and without changing any symbol, it will move to the right as:

 ![image](https://github.com/user-attachments/assets/2108f5f9-996a-4aa6-8c18-06cd8acf687e)


The move will be δ(q1, 1) = (q2, Y, L) which means it will move to q2 state and change 1 to Y, it will move to the left as:

 ![image](https://github.com/user-attachments/assets/3152344e-c670-47a3-b5c0-fe05c8dcf51f)


Working on it in the same way, the machine will reach state q3 and the head will point to B as shown:

 ![image](https://github.com/user-attachments/assets/52b136a7-38d5-4e6d-b316-14975bf768c6)


Using move ?(q3, B) = halt, it will stop and accept.

## Notes
- In a non-deterministic Turing machine, there can be more than one possible move for a given state and tape symbol, but non-deterministic TM does not add any power.
- Every non-deterministic TM can be converted into a deterministic TM.
- In a multi-tape Turing machine, there can be more than one tape and corresponding head pointers, but it does not add any power to the Turing machine.
- Every multi-tape TM can be converted into a single tape TM.

## Question
A single tape Turing Machine M has two states q0 and q1, of which q0 is the starting state. The tape alphabet of M is {0, 1, B} and its input alphabet is {0, 1}. The symbol B is the blank symbol used to indicate the end of an input string. The transition function of M is described in the following table:

 ![image](https://github.com/user-attachments/assets/5bc03090-c105-424a-bc17-e546a3a3cd29)


The table is interpreted as illustrated below. The entry (q1, 1, R) in row q0 and column 1 signifies that if M is in state q0 and reads 1 on the current tape square, then it writes 1 on the same tape square, moves its tape head one position to the right, and transitions to state q1. Which of the following statements is true about M?

1. M does not halt on any string in (0 + 1)+
2. M does not halt on any string in (00 + 1)*
3. M halts on all strings ending in a 0
4. M halts on all strings ending in a 1

### Solution
Let us see whether the machine halts on the string `1`. Initially, the state will be q0, and the head will point to 1 as:

![image](https://github.com/user-attachments/assets/97304b9c-576e-410a-aebb-2b2a185b54f2)


Using δ(q0, 1) = (q1, 1, R), it will move to state q1 and the head will move to the right as:

![image](https://github.com/user-attachments/assets/733038ff-e32d-4092-a3bd-fa985ae036e3)


Using δ(q1, B) = (q0, B, L), it will move to state q0 and the head will move to the left as:

![image](https://github.com/user-attachments/assets/6ef31a6d-f05e-4438-b80f-158fad94ec24)


It will run in the same way again and again and not halt.

Option D says M halts on all strings ending with 1, but it is not halting for 1. So, option D is incorrect.

Let us see whether the machine halts on the string `0`. Initially, the state will be q0, and the head will point to 1 as:


![image](https://github.com/user-attachments/assets/b9b4f7b0-25c9-412b-8739-0e5625594c5d)


Using δ(q0, 0) = (q1, 0, R), it will move to state q1 and the head will move to the right as:


![image](https://github.com/user-attachments/assets/570bef89-d443-4f8f-ab17-e0a439e3cd7b)


Using δ(q1, B) = (q0, B, L), it will move to state q0 and the head will move to the left as:


![image](https://github.com/user-attachments/assets/b327a63e-c404-4faf-82e0-f69a740386c3)


It will run in the same way again and again and not halt.

Option C says M halts on all strings ending with 0, but it is not halting for 0. So, option C is incorrect.

Option B says that TM does not halt for any string (00 + 1)*. But NULL string is a part of (00 + 1)* and TM will halt for NULL string. For NULL string, the tape will be:
 
 
 ![image](https://github.com/user-attachments/assets/72e9f69c-ea95-4399-93b4-1a00b4dfccd4)

 


 
Using δ(q0, B) = halt, TM will halt. As TM is halting for NULL, this option is also incorrect.

So, option (A) is correct.
 
