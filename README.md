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
#### Quantum Gates
##### In quantum computing and specifically the quantum circuit model of computation, a quantum logic gate (or simply quantum gate) is a basic quantum circuit operating on a small number of qubits. They are the building blocks of quantum circuits, like classical logic gates are for conventional digital circuits. Let us undestand some of the basic gates. *nly mentioning those I have come across or read about. I'm fairly new to the topic but I wanted to explore so I may not have included many gat
