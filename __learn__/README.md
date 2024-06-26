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

  