# 🔄 Regex to DFA Converter

![Language](https://img.shields.io/badge/Language-[Your_Language_Here]-blue.svg)
![Topic](https://img.shields.io/badge/Topic-Automata%20Theory-brightgreen.svg)
![Topic](https://img.shields.io/badge/Topic-Compiler%20Design-orange.svg)

A robust computational tool designed to parse Regular Expressions (Regex) and systematically construct their equivalent Deterministic Finite Automata (DFA). 

This project demonstrates the practical application of Automata Theory, translating abstract mathematical models into working code. It is an excellent resource for understanding the foundational steps behind how modern lexical analyzers and pattern-matching engines work under the hood.

## 🧠 The Conversion Pipeline

This engine processes a regular expression through several distinct algorithmic phases to achieve the final DFA:

1. **Regex Parsing & Preprocessing:** * Formats the input string, inserting explicit concatenation operators where necessary.
   * Converts the Infix regular expression into Postfix notation (often using the Shunting-Yard algorithm) to respect operator precedence (`*`, `|`, `()`, etc.).
2. **NFA Construction (Thompson's Algorithm):** * Constructs a Nondeterministic Finite Automaton (NFA) with $\epsilon$-transitions from the Postfix expression.
3. **DFA Conversion (Subset Construction):** * Applies the Powerset (Subset) Construction algorithm to convert the NFA into a Deterministic Finite Automaton (DFA), calculating $\epsilon$-closures and state transitions.
4. **[Optional] DFA Minimization:**
   * Optimizes the resulting DFA by merging equivalent states to create the most efficient state machine possible.

## ✨ Key Features
* **Standard Operator Support:** Handles core regex operators including Union (`|`), Concatenation (`.`), and Kleene Star (`*`).
* **State Mapping:** Clearly tracks and outputs the transition table, mapping the generated states to their respective inputs.
* **Algorithmic Transparency:** Built to clearly demonstrate the intermediate steps (Regex -> NFA -> DFA) rather than just functioning as a black box.

## 🛠️ Technologies & Core Concepts
* **Language:** `[Insert Language, e.g., Python 3.x / Java / C++]`
* **Concepts:** Finite State Machines, Graph Theory, Recursive Descent Parsing, Set Theory.

## 🚀 Getting Started

### Prerequisites
Make sure you have `[Insert requirement, e.g., Python 3.8+ or Java JDK 11+]` installed on your machine.

### Installation
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/AnasAbdelraouf128/RegexToDFAConverter.git](https://github.com/AnasAbdelraouf128/RegexToDFAConverter.git)

   💻 Usage Example
Upon running the program, you will be prompted to enter a Regular Expression.

Input:

Plaintext
(a|b)*abb

Output:
[Insert a sample of what your program outputs here. For example:
- The Postfix string
- The NFA states and transitions
- The final DFA Transition Table showing States, Inputs, and Next States]


=========================================
      REGEX TO DFA CONVERTER ENGINE      
=========================================

Enter Regular Expression: (a|b)*abb

[1] Parsing Regex...
    -> Infix:  (a|b)*abb
    -> Postfix: ab|*a.b.b.

[2] Constructing NFA (Thompson's Algorithm)...
    -> NFA States Generated: 10
    -> Epsilon Transitions Handled.

[3] Converting to DFA (Subset Construction)...
    -> Computing Epsilon Closures...
    -> DFA States Generated: 4

=========================================
          DFA TRANSITION TABLE           
=========================================
Alphabet (Σ): {'a', 'b'}
Start State : q0
Accept State: {q3}

+-------------+-----------+-----------+
| State       | Input 'a' | Input 'b' |
+-------------+-----------+-----------+
| -> q0       |    q1     |    q0     |
|    q1       |    q1     |    q2     |
|    q2       |    q1     |    q3     |
| * q3       |    q1     |    q0     |
+-------------+-----------+-----------+

Legend: 
(->) Start State
(*)  Accepting State











If this project helped you understand Automata Theory or Compiler Design a little better, please consider giving it a ⭐!

# Collaborators

[Eslam Ahmed](https://github.com/illusorist)

[Marwan Osama](https://github.com/maro7420)

[Ahmed Yousri](https://github.com/v0id666)

[Anas Abdelraoof](https://github.com/AnasAbdelraouf128)

[Ahmed Mahmoud](https://github.com/AhmedMahmoud195)
