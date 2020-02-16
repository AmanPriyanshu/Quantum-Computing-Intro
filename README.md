# Quantum_Computing_Intro
Understanding and exploring Quantum-Computing conecpts as well as developing some simple code for its implementation. These are my notes for understanding and revising later if I forget something

## Table of Contents:

<!-- MarkdownTOC depth=8 -->
- [INTRODUCTION](#introduction)
    - [Quantum Mechanics](#quantum-mechanics)
        - [Double Slit Experiment](#double-slit-experiment)
        - [Quantization](#quantization)
        - [Light as Particles](#light-as-particles)
        - [Matter as Waves](#matter-as-waves)
    - [Quantum Computing](#quantum-computing)
        - [Qubits](#qubits)
        - [Quantum Logic Gates Basics](#quantum-logic-gates-basics)
        - [Quantum Memory](#quantum-memory)
        - [Quantum Entanglement](#quantum-entanglement)
- [Quantum Gates](#quantum-gates)
    - [Single Qubit](#single-qubit)
        - [Hadamard Gate](#hadamard-gate)
        - [Pauli-X Gate](#pauli-x-gate)
- [Quantum Circuits a Basic Understanding](#quantum-circuit-basics)
- [My Understanding of Quantum Computing](#my-understanding-of-quantum-computing)
- [LIBRARIES- which I have tried out](#libraries)
    - [Quiskit](#quiskit)
    <!--- - [Yao.jl](#yao-jl) --->
    <!--- - [Cirq](#cirq) --->
    <!--- - [Strawberryfields](#strawberryfields) --->
    <!--- - [PyQuil](#pyquil) --->
<!-- /MarkdownTOC -->
<!--- comment example ---> 
<a name="introduction"></a>
## INTRODUCTION

<a name="quantum-mechanics"></a>
### Quantum Mechanics

##### The ability of particles part of the atomic scale to behave as neither particles nor waves, they exhibit a unique nature which is understood and studied as Quantum Mechanics. 

<a name="double-slit-experiment"></a>
#### Double Slit Expermient
##### Let's take a look at Double Slit Experiment, now we know for sure that a Double Slit experiment for a particle-system would give us no interference pattern. Rather it would simply give us two patterns directly in front of the slits. Now performing the same experiment with a wave-system we get an interference pattern. Light on the other hand was believed to be of particle nature, but with this experiment it gave an interference pattern.

##### In modern physics, the double-slit experiment is a demonstration that light and matter can display characteristics of both classically defined waves and particles; moreover, it displays the fundamentally probabilistic nature of quantum mechanical phenomena.

<a name="quantization"></a>
#### Quantization
##### An essential ingredient in quantum mechanics, it is the idea that certain objects or properties could tune in by only a certain defined set. It is the process of constraining an input from a continuous or otherwise large set of values (such as the real numbers) to a discrete set (such as the integers).

<a name="light-as-particles"></a>
#### Light as Particles
##### The study of Photoelectric effect by scientists such as Max Planc found that certain types of metal and other materials will eject electrons when light shines on them. They expected that the number of electrons ejected from the metal would increase with the intensity of light directed towards the metal. What they found instead, was that the wavelength of the light affected the number of electrons ejected. The reason was not understood till much later, when Einstein theorized that electromagnetic energy comes in packets, or quanta which we now call photons. So light behaves as a wave and as a particle, depending on the circumstances and the effect being observed. This concept is now known as wave-particle duality.

<a name="matter-as-waves"></a>
#### Matter as waves
##### Matter does exist as waves, just that we cannot see it, as its amplitude of vibration is much smaller than the body's total size. A fairly intriguing conecpt where-in the wavelenght of body or matter in motion can be given by, λ=h/p.
##### Here h = 6.626×10−34Js and p is the moment of the moving body. As we can see from the value of h, it is far too small ≈ 10−34 scale, so it can't give any significant wavelenght for large objects.

<a name="quantum-computing"></a>
### Quantum Computing
##### Quantum Computing is the use of quantum-mechanical phenomena such as superposition and entanglement to perform computation. A quantum computer is used to perform such computation, which can be implemented theoretically or physically[1]:I-5 There are two main approaches to physically implementing a quantum computer currently, analog and digital. Analog approaches are further divided into quantum simulation, quantum annealing, and adiabatic quantum computation. Digital quantum computers use quantum logic gates to do computation. Both approaches use quantum bits or qubits. (Reference: <https://www.nap.edu/catalog/25196/quantum-computing-progress-and-prospects>)

<a name="qubits"></a>
#### Qubits
##### Qubits or Quantum Bits are interesting as they break normal norms of bits containing only 0's and 1's. Even though they may contain a 0 or a 1 quantum state, but they can still be in superpostion. However, when qubits are measured the result is always either a 0 or a 1; the probabilities of the two outcomes depends on the quantum state they were in. It is the basic quantum information, the quantum version of the classical binary bit physically realized with a two-state device. A qubit is a two-state (or two-level) quantum-mechanical system, one of the simplest quantum systems displaying the peculiarity of quantum mechanics.
##### Two-state quantum mechanical system: in quantum mechanics, a two-state system (or two-level) is a quantum system that can exist in any quantum superposition of two independent (physically distinguishable) quantum states. The Hilbert space describing such a system is two-dimensional. Therefore, a complete basis spanning the space will consist of two independent states.
##### Hilbert Space: A mathematical concept which extends the methods of vector algebra and calculus from the two-dimensional Euclidean plane and three-dimensional space to spaces with any finite or infinite number of dimensions. The Hilbert space must be:
* A Linear Vector Space.
* Have a natural inner product, or dot product, providing a distance function.
* Under this distance function it becomes a complete metric system.
* Inner product is conjugate symmetric
* Anti-Linear w.r.t first vector in Inner product
* Linear w.r.t second vector in Inner product
* Positive Definiteness: Inner product of a vector with itself must not be negative (i.e >= 0) and =0 only if the vector itself is zero
* Closeness of two vectors is given by distance formula
* Hilbert spaces are Seperable. So they contain a countable, dense, subset. Now what makes a set/space countable. For example Integers are countable, even though we have to count till infinty they are still mathematically or say theoretically countable. Just like that rational numbers which can be expressed as ratios of these Integers can be tagged as Countable. Now a subset A is said to dense if every point x in X either belongs to A or is a limit point of A; For Eg: the rational numbers are a dense subset of the real numbers because every real number either is a rational number or has a rational number arbitrarily close to it. Finally seperable: Now since the Rational Numbers are a subest of Real Numbers and since they are countable and dense then we can call Real Numbers as Seperable.
* Hilbert spaces are complete (No breaks, openings, etc.)

<a name="quantum-logic-gates-basics"></a>
#### Quantum Logic Gates Basics
##### The prevailing model of quantum computation describes the computation in terms of a network of quantum logic gates. In quantum computing and specifically the quantum circuit model of computation, a quantum logic gate (or simply quantum gate) is a basic quantum circuit operating on a small number of qubits. They are the building blocks of quantum circuits, like classical logic gates are for conventional digital circuits. Unlike many classical logic gates, quantum logic gates are reversible.
##### Quantum logic gates are represented by unitary matrices. The number of qubits in the input and output of the gate must be equal; a gate which acts on n qubits is represented by a 2^n x 2^n unitary matrix. The quantum states that the gates act upon are vectors in 2^n complex dimensions. The base vectors are the possible outcomes if measured, and a quantum state is a linear combination of these outcomes.
##### A memory consisting of n bits of information has 2^n possible states (Each bit could be a 0 or 1 independent of the others, so 2x2x2...n times). A vector representing all memory states has hence 2^n entries (one for each state). This vector should be viewed as a probability vector and represents the fact that the memory is to be found in a particular state. Now classical bits give us a 100% result, however, here it is a probability matrix (Density Matrix). Density Matrix: is a matrix that describes the statistical state of a system in quantum mechanics. The probability for any outcome of any well-defined measurement upon a system can be calculated from the density matrix for that system.
<a name="quantum-memory"></a>
#### Quantum Memory
##### This memory may be found in one of two classical states: the zero state or the one state. We may represent the state of this memory using Dirac notation:
##### |0> := (1)
##### .     (0)
##### |1> := (0)
##### .     (1)
*How do I add Images*
##### A quantum memory may then be found in any quantum superposition |Ψ> of the two classical states |0> and |1>:
##### |Ψ> := α|0> + β|1> := (α)
##### .                     (β)
##### α^2 + β^2 = 1
##### In general, the coefficients α and β are complex numbers. In this scenario, one qubit of information is said to be encoded into the quantum memory. The state |Ψ> is not itself a probability vector but can be connected with a probability vector via a measurement operation. If the quantum memory is measured to determine if the state is |0> or |1> (this is known as a computational basis measurement), the zero state would be observed with probability α^2 and the one state with probability β^2. The numbers α and β are called quantum amplitudes.

<a name="quantum-entaglement"></a>
#### Quantum Entanglement
##### An important distinguishing feature between qubits and classical bits is that multiple qubits can exhibit quantum entanglement. Quantum entanglement is a nonlocal property of two or more qubits that allows a set of qubits to express higher correlation than is possible in classical systems. The simplest system to display quantum entanglement is the system of two qubits. Consider, for example, two entangled qubits in the |Φ+> Bell state:
##### 1(|00>+|11>)/(2)^0.5
##### In this state, called an equal superposition, there are equal probabilities of measuring either product state |00>  or |11> , as (1/(2)^0.5)^2=1/2. In other words, there is no way to tell if the first qubit has value “0” or “1” and likewise for the second qubit.
##### Imagine that these two entangled qubits are separated, with one each given to Alice and Bob. Alice makes a measurement of her qubit, obtaining—with equal probabilities—either |0>  or |1> , i.e., she can now tell if her qubit has value “0” or “1”. Because of the qubits' entanglement, Bob must now get exactly the same measurement as Alice. For example, if she measures a |0> , Bob must measure the same, as |00>  is the only state where Alice's qubit is a |0> . In short, for these two entangled qubits, whatever Alice measures, so would Bob, with perfect correlation, in any basis, however far apart they may be and even though both can not tell if their qubit has value “0” or “1” — a most surprising circumstance that can not be explained by classical physics.


<a name="quantum-gates"></a>
## Quantum Gates
##### In quantum computing and specifically the quantum circuit model of computation, a quantum logic gate (or simply quantum gate) is a basic quantum circuit operating on a small number of qubits. They are the building blocks of quantum circuits, like classical logic gates are for conventional digital circuits. Let us undestand some of the basic gates. *Only mentioning those I have come across or read about. I'm fairly new to the topic but I wanted to explore so I may not have included many gates.*
<a name="single-qubit"></a>
### Single Qubit

<a name="hadamard-gate"></a>
#### Hadamard Gate
##### It maps the basis state |0>  to (|0> + |1>)/(2)^0.5 and |1>  to (|0> - |1>)/(2)^0.5, which means that a measurement will have equal probabilities to becomes either of the two classical states. For example, say we have: 
##### α|0> + β|1> --|H|-> α(|0> + |1>)/(2)^0.5 + β(|0> - |1>)/(2)^0.5 = (α + β)|0>/(2)^0.5 + (α - β)|1>/(2)^0.5
##### We can clearly see H = [1  1]
##### .                      [1 -1]/(2)^0.5
##### So the operations is conducted as H|0> or H|1> to give the above output. It is as usual a Reversible gate.
##### Application: Expand the range of states which its possible for a computer to be in. It allows us to take optimized steps which aren't possible in classical computation.

<a name="r-x-gate"></a>
#### Rx Gate
##### The Rx gate is a single-qubit rotation through angle θ (radians) around the x-axis.
##### We can clearly see Rx = [cos(θ/2)  -i sin(θ/2)]
##### .                       [-i sin(θ/2)  cos(θ/2)]

<a name="r-y-gate"></a>
#### Ry Gate
##### The Ry gate is a single-qubit rotation through angle θ (radians) around the y-axis.
##### We can clearly see Ry = [cos(θ/2)   sin(θ/2)]
##### .                       [-sin(θ/2)  cos(θ/2)]

<a name="r-z-gate"></a>
#### Rz Gate
##### The Rz gate is a single-qubit rotation through angle \thetaθ (radians) around the z-axis.
##### We can clearly see Rz = [e^(-θ/2)   0]
##### .                       [0    e^(θ/2)]

<a name="s-gate"></a>
#### S Gate
##### The S gate is also known as the phase gate or the Z90 gate, because it represents a 90 degree rotation around the z-axis.
##### We can clearly see S = [1   0]
##### .                      [0  -1]

<a name="pauli-x-gate"></a>
#### Pauli-X Gate
##### It is the quantum equivalent of the NOT gate for classical computers (with respect to the standard basis |0> , |1> , which distinguishes the Z-direction; It maps |0>  to |1>  and |1>  to |0>. Due to this nature, it is sometimes called bit-flip.
##### We can clearly see X = [0  1]
##### .                      [1  0]
##### Application: Used for bit-flipping

<a name="pauli-y-gate"></a>
#### Pauli-Y Gate
##### It equates to a rotation around the Y-axis of the Bloch sphere by π  radians. It maps |0>  to i|1> and |1>  to -i|0>. It is represented by the Pauli Y matrix:
##### We can clearly see Y = [0 -i]
##### .                      [i  0]

<a name="pauli-z-gate"></a>
#### Pauli-Z Gate
##### It equates to a rotation around the Z-axis of the Bloch sphere by π  radians. It leaves the basis state |0>  unchanged and maps |1>  to -|1>. Due to this nature, it is sometimes called phase-flip. It is represented by the Pauli Z matrix:
##### We can clearly see Z = [1  0]
##### .                      [0 -1]

<a name="square-root-not-gate"></a>
#### Square Root Not Gate
##### It maps the basis state |0>  to ( (i+1)|0> + (i-1)|1> )/2 and |1>  to ( (i-1)|0> + (i+1)|1> )/2 . It is represented by the Pauli Z matrix:
##### We can clearly see Z = [1+i  1-i]
##### .                      [1-i  1+i]
##### Squared root-gates can be constructed for all other gates by finding a unitary matrix that, multiplied by itself, yields the gate one wishes to construct the squared root gate of. All rational exponents of all gates can be found similarly.

<a name="phase-shift-gate"></a>
#### Phase Shift Gate
##### It is a gate that leave the basic state |0>  unchanged and maps |1>  to e^(iΦ)|1> . The probability of measuring a |0>  or |1>  is unchanged after applying this gate, however it modifies the phase of the quantum state. This is equivalent to tracing a horizontal circle (a line of latitude) on the Bloch sphere by Φ radians. It is represented by the phase shift matrix:
##### We can clearly see R = [1      0 ]
##### .                      [0  e^(iΦ)]
##### where Φ  is the phase shift.

<a name="double-qubit"></a>
### Double Qubit
<a name="swap-gate"></a>
#### Swap Gate
##### The swap gate swaps two qubits. Expressed in basis states, the SWAP gate swaps the state of the two qubits involved in the operation:
##### We can clearly see SWAP = [1 0 0 0]
##### .                         [0 0 1 0]
##### .                         [0 1 0 0]
##### .                         [0 0 0 1]

<a name="c-not-gate"></a>
#### Controlled not Gate: Cx,Cy
##### Controlled gates act on 2 or more qubits, where one or more qubits act as a control for some operation. For example, the controlled NOT gate (or CNOT or cX) acts on 2 qubits, and performs the NOT operation on the second qubit only when the first qubit is |1> , and otherwise leaves it unchanged. With respect to the basis |00> , |01>, |10>, |11> , it is represented by the matrix:
##### We can clearly see cX = [1 0 0 0]
##### .                       [0 1 0 0]
##### .                       [0 0 0 1]
##### .                       [0 0 1 0]
##### The CNOT (or controlled-X) gate can be described as the gate that maps |a,b> to |a, a^b>. (Here ^ is for Ex-OR gate)

<a name="ising-gate"></a>
#### Ising (ZZ) coupling gate
##### The gate is used to apply phase e^(iα) to the basis elements |00⟩ and |11⟩, and e(−iα) otherwise. 
##### We can clearly see cX = [e^(iα) 0 0 0 ]
##### .                       [0 e^(-iα) 0 0]
##### .                       [0 0 e^(-iα) 0]
##### .                       [0 0 0 e^(iα) ]

<a name="triple-qubit"></a>
### Triple Qubit
<a name="toffoli-gate"></a>
#### toffoli Gate: CCNOT
##### is a 3-bit gate, which is universal for classical computation but not for quantum computation. The quantum Toffoli gate is the same gate, defined for 3 qubits. If we limit ourselves to only accepting input qubits that are \0>  and |1> , then if the first two bits are in the state |1>  it applies a Pauli-X (or NOT) on the third bit, else it does nothing. It is an example of a controlled gate. Since it is the quantum analog of a classical gate, it is completely specified by its truth table.
##### We can clearly see CCNOT = [1  0  0  0  0  0  0  0]
##### .                          [0  1  0  0  0  0  0  0]
##### .                          [0  0  1  0  0  0  0  0]
##### .                          [0  0  0  1  0  0  0  0]
##### .                          [0  0  0  0  1  0  0  0]
##### .                          [0  0  0  0  0  1  0  0]
##### .                          [0  0  0  0  0  0  0  1]
##### .                          [0  0  0  0  0  0  1  0]

<a name="fredkin-gate"></a>
#### Fredkin (CSWAP) gate
##### It performs a controlled swap. It is universal for classical computation. It has the useful property that the numbers of 0s and 1s are conserved throughout, which in the billiard ball model means the same number of balls are output as input.
##### We can clearly see CSWAP = [1  0  0  0  0  0  0  0]
##### .                          [0  1  0  0  0  0  0  0]
##### .                          [0  0  1  0  0  0  0  0]
##### .                          [0  0  0  1  0  0  0  0]
##### .                          [0  0  0  0  1  0  0  0]
##### .                          [0  0  0  0  0  0  1  0]
##### .                          [0  0  0  0  0  1  0  0]
##### .                          [0  0  0  0  0  0  0  1]
