The **NOT gate** (also called the **X gate** or **Pauli-X gate**) is the quantum equivalent of the classical NOT gate. Just as a classical NOT flips a bit from 0 to 1 or 1 to 0, the quantum NOT gate flips the basis states of a qubit:

$$X|0⟩ = |1⟩ \qquad X|1⟩ = |0⟩$$

## Matrix Representation

The NOT gate is represented by the **Pauli-X matrix**:

$$X = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$$

Applying it to the basis states confirms the flip:

$$X|0⟩ = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 1 \end{bmatrix} = |1⟩$$

$$X|1⟩ = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \begin{bmatrix} 0 \\ 1 \end{bmatrix} = \begin{bmatrix} 1 \\ 0 \end{bmatrix} = |0⟩$$

## Effect on Superposition

What happens when the NOT gate is applied to a qubit in superposition?

$$X(\alpha|0⟩ + \beta|1⟩) = \alpha X|0⟩ + \beta X|1⟩ = \alpha|1⟩ + \beta|0⟩ = \beta|0⟩ + \alpha|1⟩$$

The gate swaps the amplitudes of $|0⟩$ and $|1⟩$. The probabilities of measurement outcomes are exchanged — if the original state had a 36% chance of measuring $|0⟩$ and 64% chance of $|1⟩$, after the NOT gate those probabilities are reversed.

## Key Properties

- **Unitary**: $X^\dagger X = I$ — applying the NOT gate twice returns to the original state: $X(X|\psi⟩) = |\psi⟩$.
- **Self-inverse**: $X^2 = I$, meaning the NOT gate is its own inverse.
- **Classical analog**: On the basis states $|0⟩$ and $|1⟩$, it behaves exactly like a classical NOT gate, making it the most intuitive quantum gate to start with.
