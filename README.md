QAOA Probability Visualization – Ambassador Seating Problem

Overview:
This project demonstrates the Quantum Approximate Optimization Algorithm (QAOA) applied to a combinatorial seating problem inspired by an Olympiad-style question. The problem asks:
"Given a number of ambassadors, each with at most a certain number of enemies, can they be seated around a round table so that no one sits next to an enemy?"
While traditionally solved using linear graph theory and combinatorial arguments, this project explores a quantum-inspired approach to the problem, providing a fresh perspective and visualization of how probabilities evolve towards optimal seating arrangements.

Background – The Problem:
In the classical approach, the problem can be handled using the Invariance Principle, which ensures that there always exists a way to swap positions to reduce hostile neighbor pairs. Linear graph theory shows that a Hamiltonian circuit exists, guaranteeing a solution.
This project takes inspiration from that logical solution but demonstrates it using QAOA, highlighting how quantum algorithms can handle combinatorial optimization in a visual, intuitive manner.

Quantum Approximate Optimization Algorithm (QAOA):
QAOA is a quantum algorithm designed to find optimal solutions for combinatorial problems. The basic idea:
Start with all possible arrangements equally probable.
Apply a cost layer to penalize “bad” arrangements (where enemies sit next to each other).
Apply a mixer layer to redistribute probabilities across arrangements.
Repeat for several layers → the probabilities gradually favor optimal arrangements.
The final measurement shows which seating arrangements are most likely to succeed, and the process can be visualized as evolving probabilities.

Implementation:
The project is implemented in Python and can be run in Jupyter Notebook.
Each possible seating is represented as a point on a circle.
Marker size and color indicate the probability of a seating arrangement being selected (red = high cost, green = optimal).
As QAOA layers are applied, bad arrangements fade, and good arrangements dominate, visually demonstrating the algorithm in action.
This animation provides a clear and intuitive view of QAOA in practice and offers a novel approach to exploring classical combinatorial problems with quantum techniques.

How to Run:
Open the Jupyter Notebook (qaoa_visualization.ipynb) in VS Code or Jupyter.
Run all cells to see the animated probability evolution.
Experiment by changing the number of ambassadors or enemy pairs to explore different scenarios.

Inspiration:
This project came from exploring an Olympiad problem in a math/IMO book. While the classical linear approach guarantees a solution, using QAOA gives a new perspective, helping visualize how quantum-inspired algorithms can solve combinatorial optimization problems.

Visualization:
Red dots: arrangements with enemies seated together (bad).
Green dots: optimal arrangements.
Size indicates the likelihood of a seating being chosen.
Animation shows how probabilities shift toward optimal solutions with each layer of QAOA.
