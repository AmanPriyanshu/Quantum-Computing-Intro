# Quantum_Computing_Intro
Understanding and exploring Quantum-Computing conecpts as well as developing some simple code for it.

## Table of Contents:

<!-- MarkdownTOC depth=8 -->
- [INTRODUCTION](#introduction)
    - [Quantum Mechanics](#quantum-mechanics)
        - [Double Slit Experiment](#double-slit-experiment)
        - [Quantization](#quantization)
        - [Light as Particles](#light-as-particles)
        - [Matter as Waves](#matter-as-waves)
    - [Quantum Computing](#quantum-computing)
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
#### Qubits
##### Qubits or Quantum Bits are interesting as they break normal norms of bits containing onyl 0's and 1's. Even though they may contain a 0 or a 1 quantum state, but they can still be in superpostion. However, when qubits are measured the result is always either a 0 or a 1; the probabilities of the two outcomes depends on the quantum state they were in. It is the basic quantum information, the quantum version of the classical binary bit physically realized with a two-state device. A qubit is a two-state (or two-level) quantum-mechanical system, one of the simplest quantum systems displaying the peculiarity of quantum mechanics.
##### Two-state quantum mechanical system: in quantum mechanics, a two-state system (or two-level) is a quantum system that can exist in any quantum superposition of two independent (physically distinguishable) quantum states. The Hilbert space describing such a system is two-dimensional. Therefore, a complete basis spanning the space will consist of two independent states.
##### Hilbert Space: A mathematical concept which extends the methods of vector algebra and calculus from the two-dimensional Euclidean plane and three-dimensional space to spaces with any finite or infinite number of dimensions. The Hilbert space must be:
* A Linear Vector Space.
* Have a natural inner product, or dot product, providing a distance function.
* Under this distance function it becomes a complete metric system.
* Inner product is conjugate symmetric
* Linear w.r.t second vector in Inner product
* Anti-Linear w.r.t first vector in Inner product
* Positive Definiteness: Inner product of a vector with itself must not be negative (i.e >= 0) and =0 only if the vector itself is zero
* Closeness of two vectors is given by distance formula
* Hilbert spaces are Seperable. So they contain a countable, dense, subset. Now what makes a set/space countable. For example Integers are countable, even though we have to count till infinty they are still
