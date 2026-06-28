The **Hadamard gate** (written as **H**) is one of the most important and frequently used gates in quantum computing. It has no classical analog — its purpose is to create *superposition* from a definite basis state, or to collapse a superposition back into a definite state.

$$H|0⟩ = \frac{1}{\sqrt{2}}|0⟩ + \frac{1}{\sqrt{2}}|1⟩ \qquad H|1⟩ = \frac{1}{\sqrt{2}}|0⟩ - \frac{1}{\sqrt{2}}|1⟩$$

Starting from $|0⟩$, the Hadamard gate produces an *equal superposition* of $|0⟩$ and $|1⟩$ — a qubit that has exactly a 50% chance of being measured as 0 and a 50% chance of being measured as 1.

## Matrix Representation

$$H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}$$

Applying it to the basis states:

$$H|0⟩ = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix} \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \frac{|0⟩ + |1⟩}{\sqrt{2}}$$

$$H|1⟩ = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix} \begin{bmatrix} 0 \\ 1 \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \end{bmatrix} = \frac{|0⟩ - |1⟩}{\sqrt{2}}$$

The resulting states are so common they have their own names:

$$|+⟩ := \frac{|0⟩ + |1⟩}{\sqrt{2}} \qquad |-⟩ := \frac{|0⟩ - |1⟩}{\sqrt{2}}$$

## The Role of Phase

Notice that $H|0⟩$ and $H|1⟩$ both produce states with equal measurement probabilities — both give a 50/50 chance of $|0⟩$ or $|1⟩$ when measured. Yet they are *different* quantum states because of the **relative phase**: the minus sign in front of $|1⟩$ in $|-⟩$.

This phase difference is invisible when you measure, but it matters when these states are fed into further gates. This is a key idea in quantum computing: **phase carries information** that gates can act on, even though measurement alone cannot reveal it.

## The Hadamard as Its Own Inverse

A remarkable property of the Hadamard gate is that it is **self-inverse**:

$$H^2 = I$$

Applying the Hadamard gate twice returns the qubit to its original state. This means the same gate that creates superposition also *undoes* it:

$$H(H|0⟩) = H|+⟩ = |0⟩$$

## Why It Is So Important

- **Creates superposition**: The Hadamard gate is the standard way to put a qubit into equal superposition, which is the starting point for almost every quantum algorithm.
- **Enables parallelism**: Applying H to $n$ qubits simultaneously creates a superposition of all $2^n$ possible bit strings — quantum algorithms exploit this to evaluate a function on many inputs at once.
- **Connects two bases**: The Hadamard gate transforms between the *computational basis* $\{|0⟩, |1⟩\}$ and the *Hadamard basis* $\{|+⟩, |-⟩\}$, which is essential in algorithms like the Deutsch–Jozsa algorithm and quantum teleportation.
