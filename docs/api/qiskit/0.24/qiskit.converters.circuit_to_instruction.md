<span id="qiskit-converters-circuit-to-instruction" />

# qiskit.converters.circuit\_to\_instruction

<span id="undefined" />

`circuit_to_instruction(circuit, parameter_map=None, equivalence_library=None)`

Build an `Instruction` object from a `QuantumCircuit`.

The instruction is anonymous (not tied to a named quantum register), and so can be inserted into another circuit. The instruction will have the same string name as the circuit.

**Parameters**

*   **circuit** ([*QuantumCircuit*](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – the input circuit.
*   **parameter\_map** (*dict*) – For parameterized circuits, a mapping from parameters in the circuit to parameters to be used in the instruction. If None, existing circuit parameters will also parameterize the instruction.
*   **equivalence\_library** ([*EquivalenceLibrary*](qiskit.circuit.EquivalenceLibrary#qiskit.circuit.EquivalenceLibrary "qiskit.circuit.EquivalenceLibrary")) – Optional equivalence library where the converted instruction will be registered.

**Raises**

**QiskitError** – if parameter\_map is not compatible with circuit

**Returns**

an instruction equivalent to the action of the input circuit. Upon decomposition, this instruction will yield the components comprising the original circuit.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

## Example

```python
from qiskit import QuantumRegister, ClassicalRegister, QuantumCircuit
from qiskit.converters import circuit_to_instruction
%matplotlib inline

q = QuantumRegister(3, 'q')
c = ClassicalRegister(3, 'c')
circ = QuantumCircuit(q, c)
circ.h(q[0])
circ.cx(q[0], q[1])
circ.measure(q[0], c[0])
circ.rz(0.5, q[1]).c_if(c, 2)
circuit_to_instruction(circ)
```

```python
<qiskit.circuit.instruction.Instruction at 0x7fbab6b713d0>
```
