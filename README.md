# Quantum Teleportation Protocol
Implementation of the Quantum Teleportation Protocol through Qiskit using 3 qubits.
### Circuit Initialization
The teleportation circuit contains 3 qubits and 2 classical bits(crz, crx).
### Teleported qubit
The state psi is randomly initialized. This is the state that will be teleported from Alice to Bob. The inverse gates of the initialization are also
stored to later verify the circuit.
### Bell pair creation
The qubits of Alice and Bob are entangled using the Hadamard gate and a Controlled NOT gate.
### Operations by Alice
Alice first performs a Controlled NOT using psi and her qubit. Then, applies the Hadamard gate on psi. Finally, she measures both qubits and sends the 
measurements to Bob through a classical channel.
### Operations by Bob
Bob receives the classical bits and applies Pauli-X Gate and Pauli-Z Gate accordingly. Now, the arbitrary state psi has been teleported to Bob's qubit.
### Verification
The inverse gates are performed on Bob's qubit, if the teleportation had occured correctly the current state of Bob's qubit should be |0> and it is 
verified using the aer_simulator.


