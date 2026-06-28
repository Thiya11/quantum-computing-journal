A **quantum wire** is the simplest quantum gate. It takes a qubit as input and passes it through unchanged — it does nothing to the qubit's state.

$$|\psi⟩ \xrightarrow{\text{wire}} |\psi⟩$$

If the input is $\alpha|0⟩ + \beta|1⟩$, the output is exactly $\alpha|0⟩ + \beta|1⟩$.

## Why It Matters

The quantum wire is not about transformation — it is about *identity*. It represents the passage of time or the movement of a qubit from one part of a quantum circuit to another without any operation being applied. In circuit diagrams, it is drawn as a horizontal line:

$$—\!\!—\!\!—\!\!—$$

Every line you see in a quantum circuit diagram that is not a gate is a quantum wire.

## Matrix Representation

Every quantum gate is represented as a matrix that acts on the qubit's state vector. The quantum wire corresponds to the **identity matrix**:

$$I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$$

Applying $I$ to any state vector leaves it unchanged:

$$I|\psi⟩ = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} \alpha \\ \beta \end{bmatrix} = \begin{bmatrix} \alpha \\ \beta \end{bmatrix} = |\psi⟩$$

## Key Properties

- **Unitary**: $I^\dagger I = I$ — all valid quantum gates must be unitary, and the identity is trivially so.
- **Reversible**: Applying it twice (or any number of times) gives the same state back.
- **Building block**: Understanding the wire establishes the baseline — every other gate is a *deviation* from this do-nothing operation.
