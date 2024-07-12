# GitHub Bracket Samples

These are quantum tutorials via Amazon Braket, for quantum circuits and Analogue Hamiltonian Simulation. Canonical routines are covered, such as Quantum Fourier Transform (QFT), plus hybrid quantum algorithms, like Variational Quantum Eigensolver (VQE).

The structure of these samples are as follows:

- [Beginner Quantum](#simple)
- [Advanced circuits and algorithms](#advanced)
- [Hybrid quantum algos](#hybrid)
- [Quantum ML and optimisation via PennyLane](#pennylane)
- [Braket features](#braket)
- [Bracket Hybrid Jobs](#jobs)
- [Pulse Control](#pulse)
- [Analogue Hamiltonian Simulation](#ahs)
- [Qiskit with Braket](#qiskit)

--

## <a name="simple">Quantum Computing for Beginners!</a>

- [**Start here**](examples/getting_started/0_Getting_started/0_Getting_starated.ipynb)
  Build a simple circuit and run it on a local simulator.

- [**Simulators with quantum circuits**](examples/getting_started/1_Running_quantum_circuits_on_simulators/1_Running_quantum_circuits_on_simultors.ipynb)

  This tutorial prepares a paradigmatic example involving a multi-qubit entangled state - the GHZ state (after the physicists Greenberger, Horne and Zeilinger). This is the exact opposite of classical computing - it's very sensitive to decoherence. It thus makes a great benchmark for modern quantum hardware. Also, in many quantum information protocols the GHZ state is a resource for quantum error correction, quantum metrology and quantum communication.

- [**Running quantum circuits on QPU hardware**](examples/getting_started/2_Running_quantum_circuits_on_QPU_devices/2_Running_quantum_circuits_on_QPU_devices.ipynb)

  You will prepare a maximally-entangled Bell state between two qubits, for both classical simulators and QPUs.
  On classical environments, the circuit can be run on a local simulator/cloud-based on-demand simulator.
  On quantum environments, we can run the circuit on Rigetti's superconducting machine, and the ion-trap machine from IonQ. Devices can be swapped seamlessly without circuit definition changes - just redefine the device object. You can also learn to recover results using unique ARN associated with each quantum task. This is helpful in the case of potential delays which can happen if your quantum task is in queue waiting to be executed.

- [**Get right into Quantum circuits anatomy**](examples/getting_started?3_Deep_dive_into_the_anatomy_of_quantum_circuits/3_Deep_dive_into_the_anatomy_of_quantum_circuits.ipynb)

  You'll learn the anatomy of quantum circuits in the Braket SDK. You'll also learn how to build (parameterized) circuits and visually display them, and how to add circuits to each other. Associated circuit depth and size are discussed. We also learn how to execute the circuit on a device of our choice (defining a quantum task), as well as how to track/log/recover/cancel a quantum task efficiently.

8 [**Superdense coding**](examples/getting_started/4_Superdense_coding/4_Superdense_coding.ipynb)

We learn how to implement the _superdense coding_ protocol via the Braket SDK. This is a way to transmit a couple of classical bits via the transmission of just one qubit. Beginning with a pair of entangled qubits, the sender (Alice) applies a certain quantum gate to their qubit and transmits the result to Bob, the receiver, who can then decode the full two-bit payload.

---

## <a name="advanced">Advanced circuits and algorithms</a>

* [**Grover**](examples/advanced_circuits_algorithms/Grover/Grover.ipynb)
  This tutorial explains Grover's quantum algorithm. Build the corresponding quantum circuit with simple building blocks via the Braket SDK. Learn to build custom gates that are not part of the basic gate set that comes with teh SDK. This custom gate can be used as a core quantum gate - just register it as a subroutine

* [**Quantum Amplitude Amplification**](examples/advanced_circuits_algorithms/Quantum_Amplitude_Amplification/Quantum_Amplitude_Amplification.ipynb)
  Discuss in detail and implement the QAA (Quantum Amplitude Amplification) algorithm via Braket SDK. QAA is a quantum computing routine that generalises the idea behind Grover's search algorithm, with applications across many quantum algorithms. QAA employs an iterative approach to systematically increase probability of finding 1/multiple target states in a given search space. QAA can also be used to achieve a quadratic speedup over classical algorithms in a quantum computer.

 * [**Quantum Fourier Transform**](examples/advanced_circuits_algorithms/Quantum_Fourier_Transform/Quantum_Fourier_Transform.ipynb)
  We see here a detailed implementation of Quantum Fourier Transform (QFT) and inverse QFT. There are two versions - with and without recursion. This is an important subroutine used in many quantum algorithms, such as Shor's algorithm for factoring, and the QPE (quantum phase estimation) algorithm for predicting eigenvalues of a unitary operator. QPEs run efficiently on quantum machines, using O(n<sup>2</sup>) single-qubit Hadamard gates along with two-qubit controlled phase shift gates (where 𝑛 is the number of qubits). Let's check out the basics of quantum Fourier transform and how it relates with classical/discrete Fourier transform. This notebook also displays the `circuit.subroutine` functionality, that allows one to define custom methods and tack them onto the Circuit class.

* [**Quantum Phase Estimation**](examples/advanced_circuits_algorithms/Quantum_Phase_Estimation/Quantum_Phase_Estimation.ipynb)
  View a detailed implementation of the QPE (Quantum Phase Estimation) algorithm via the SDK. This is designed to estimate the eigenvalues of unitary operator 𝑈, and is an important quantum algorithm subroutines, such as Shor's algorithm for factoring, plus the HHL algorithm (named after physicists Harrow, Hassidim and Lloyd) for solving linear systems of equations on quantum machines. Also, eigenvalue problems are evident across multiple application areas and disciplines, including, for example, PCA (principal component analysis) which is used in machine learning, or in solving differential equations in fields such as maths, physics, chemistry and engineering. Here we will checkout the QPE algorithm's basics, then implement QPE via the SDK, followed by illustration with simple examples. We also see the SDK `circuit.subroutine` functionality - we can use custom-built gates as if they were a generic built-in gate. We can run the tutorial on the local or the on-demand simulator. To toggle between both, we need to only tweak one line of code - see cell below.

* [**Randomness Generation**](examples/advanced_circuits_algorithms/Randomness/Randomness_Generation.ipynb)
  Here we implement a Quantum Random Number Generator - QRNG - we learn how to use 2 discrete quantum QPUs from different suppliers in Braket to supply two streams of weakly random bits. We then learn how to come up with physically secure randomness from the two weak sources via classical post-processing via randomness extractors.