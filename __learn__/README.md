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
* [**Start here**](examples/getting_started/0_Getting_started/0_Getting_starated.ipynb)
Build a simple circuit and run it on a local simulator.

* [**Simulators with quantum circuits**](examples/getting_started/1_Running_quantum_circuits_on_simulators/1_Running_quantum_circuits_on_simultors.ipynb)

  This tutorial prepares a paradigmatic example involving a multi-qubit entangled state - the GHZ state (after the physicists Greenberger, Horne and Zeilinger). This is the exact opposite of classical computing - it's very sensitive to decoherence. It thus makes a great benchmark for modern quantum hardware. Also, in many quantum information protocols the GHZ state is a resource for quantum error correction, quantum metrology and quantum communication.

* [**Running quantum circuits on QPU hardware**](examples/getting_started/2_Running_quantum_circuits_on_QPU_devices/2_Running_quantum_circuits_on_QPU_devices.ipynb)

  You will prepare a maximally-entangled Bell state between two qubits, for both classical simulators and QPUs.
  On classical environments, the circuit can be run on a local simulator/cloud-based on-demand simulator.
  On quantum environments, we can run the circuit on Rigetti's superconducting machine, and the ion-trap machine from IonQ. Devices can be swapped seamlessly without circuit definition changes - just redefine the device object. You can also learn to recover results using unique ARN associated with each quantum task. This is helpful in the case of potential delays which can happen if your quantum task is in queue waiting to be executed. 
