# MIT 6.042J: Mathematics for Computer Science

This repository contains comprehensive, digitized Markdown notes for the **MIT 6.042J Mathematics for Computer Science (Fall 2010)** course. These notes have been transcribed and expanded from the original video lectures and the accompanying course textbook, *Mathematics for Computer Science*.

## Table of Contents

Currently, the repository contains complete notes for the following lectures:

* **[Lecture 1: Proofs, Propositions, and Axioms](./lecture-notes/l1.md)**
  * Ascertaining truth, propositions, predicates, quantifiers, logical connectives, and the axiomatic method.
* **[Lecture 2: Indirect Proofs and Induction](./lecture-notes/l2.md)**
  * Proof by contradiction, the danger of false visual proofs, ordinary induction, and strengthening the inductive hypothesis.
* **[Lecture 3: Good Proofs, Invariants, and Strong Induction](./lecture-notes/l3.md)**
  * Anatomy of a good proof, state machines, the Invariant Principle (e.g., the 8-puzzle), and Strong Induction.
* **[Lecture 4: Number Theory I – Divisibility, State Machines, and GCD](./lecture-notes/l4.md)**
  * Divisibility, the *Die Hard* water jug problem, Greatest Common Divisors, and Euclid's Algorithm.
* **[Lecture 5: Number Theory II – Cryptography and RSA](./lecture-notes/l5.md)**
  * Turing's codes, modular arithmetic, multiplicative inverses, Euler's Totient Function, Fermat's Little Theorem, and the RSA Public Key Cryptosystem.
* **[Lecture 6: Graph Theory and Graph Colouring](./lecture-notes/l6.md)**
  * Bipartite graphs, degrees, the exam scheduling problem, the chromatic number, the basic greedy colouring algorithm, and real-world applications.
* **[Lecture 7: Graph Theory II – Matching Problems and Stable Marriage](./lecture-notes/l7.md)**
  * Perfect matchings, min-weight matchings, rogue couples, the Mating Algorithm (TMA/Gale-Shapley), and proofs of optimality and fairness.

## Compilation and Rendering

These notes are designed to be converted into a high-quality PDF eBook using **Pandoc**. Because the notes heavily utilize `mermaid.js` for graph theory visualizations, you must use a Mermaid filter during the Pandoc conversion.

### Prerequisites
1. Install [Pandoc](https://pandoc.org/installing.html).
2. Install [mermaid-filter](https://github.com/raghur/mermaid-filter) (usually via npm: `npm install -g mermaid-filter`).
3. A working LaTeX distribution (like TeX Live or MiKTeX) for rendering the math and generating the PDF.

### Build Command
To compile a single lecture into a PDF, use the following command:

```bash
pandoc ./lecture-notes/l6.md -o ./lecture-notes/l6.pdf --filter mermaid-filter
```

To compile all notes into a single eBook:
```bash
pandoc lecture_*.md -o MIT_6042J_Notes.pdf --filter mermaid-filter --toc --top-level-division=chapter
```
*(Note: Ensure that any special brackets inside Mermaid nodes are enclosed in double quotes (e.g., `["v_{n/2}"]`) to prevent parsing errors.)*

## Source Material & Acknowledgements
* **Course Video Lectures:** MIT OpenCourseWare (OCW) 6.042J, Fall 2010. Content is provided under a Creative Commons license.
* **Textbook:** *Mathematics for Computer Science* by Eric Lehman, F. Thomson Leighton, and Albert R. Meyer. 
* Support MIT OpenCourseWare at [ocw.mit.edu](https://ocw.mit.edu).
