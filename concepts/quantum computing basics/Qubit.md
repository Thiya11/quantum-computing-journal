If we analyze the very fundamentals of a computer, all data is stored in memory as 0s and 1s. Every operation a computer performs ultimately comes down to manipulating these 0s and 1s — this is the foundation of classical computing.

A **qubit**, however, is not just a 0 or a 1. It is a *vector representation*. The two basis states of a qubit are defined as:

$$|0⟩ := \begin{bmatrix} 1 \\ 0 \end{bmatrix} \qquad |1⟩ := \begin{bmatrix} 0 \\ 1 \end{bmatrix}$$

These are called **computational basis states** — they are the quantum analogs of the classical bit values 0 and 1. Unlike a classical bit, which must be either 0 or 1 at all times, a qubit can exist in a combination of both states simultaneously. This is the core power of quantum computing.

## Superposition

The states $|0⟩$ and $|1⟩$ are just two specific possibilities for a quantum state. In general, a qubit's state can be *any* linear combination of these basis states:

$$|\psi⟩ = \alpha|0⟩ + \beta|1⟩$$

This is called a **superposition** of $|0⟩$ and $|1⟩$. The values $\alpha$ and $\beta$ are called **probability amplitudes** — they describe how much of each basis state is present in the superposition.

For example:

$$0.6|0⟩ + 0.8|1⟩$$

represents a qubit that is in a superposition of $|0⟩$ and $|1⟩$ with amplitudes 0.6 and 0.8 respectively.

## Normalization Constraint

The amplitudes $\alpha$ and $\beta$ are not free to be any numbers — they must satisfy the **normalization constraint**:

$$|\alpha|^2 + |\beta|^2 = 1$$

This constraint comes from probability theory: when you *measure* a qubit, it collapses to either $|0⟩$ or $|1⟩$. The squared magnitude of each amplitude gives the probability of getting that outcome. Since the total probability of all outcomes must equal 1, the amplitudes must be normalized.

In the example above: $0.6^2 + 0.8^2 = 0.36 + 0.64 = 1$ ✓

So if you measured $0.6|0⟩ + 0.8|1⟩$, you would get outcome $|0⟩$ with probability 36% and outcome $|1⟩$ with probability 64%.

## Complex Amplitudes

In general, the amplitudes $\alpha$ and $\beta$ can be **complex numbers**, not just real numbers. This means the full state space of a qubit is a two-dimensional *complex* vector space. The normalization constraint then uses the squared *absolute values* of the amplitudes:

$$|\alpha|^2 + |\beta|^2 = 1$$

where $|\alpha|^2 = \alpha \cdot \bar{\alpha}$ (the amplitude multiplied by its complex conjugate).

> _The quantum state of a qubit is a vector of unit length in a two-dimensional complex vector space known as state space._

This is why linear algebra — particularly the geometry of vectors, inner products, and complex numbers — is an essential prerequisite for understanding quantum computing.
