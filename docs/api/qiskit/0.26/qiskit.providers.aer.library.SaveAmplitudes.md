# qiskit.providers.aer.library.SaveAmplitudes

<span id="undefined" />

`SaveAmplitudes(num_qubits, params, label='amplitudes', pershot=False, conditional=False)`

Save complex statevector amplitudes.

Instruction to save complex statevector amplitudes.

**Parameters**

*   **num\_qubits** (*int*) – the number of qubits for the snapshot type.
*   **params** (*list*) – list of entries to vale.
*   **label** (*str*) – the key for retrieving saved data from results.
*   **pershot** (*bool*) – if True save a list of amplitudes vectors for each shot of the simulation rather than the a single amplitude vector \[Default: False].
*   **conditional** (*bool*) – if True save the amplitudes vector conditional on the current classical register values \[Default: False].

**Raises**

**ExtensionError** – if params is invalid for the specified number of qubits.

<span id="undefined" />

`__init__(num_qubits, params, label='amplitudes', pershot=False, conditional=False)`

Instruction to save complex statevector amplitudes.

**Parameters**

*   **num\_qubits** (*int*) – the number of qubits for the snapshot type.
*   **params** (*list*) – list of entries to vale.
*   **label** (*str*) – the key for retrieving saved data from results.
*   **pershot** (*bool*) – if True save a list of amplitudes vectors for each shot of the simulation rather than the a single amplitude vector \[Default: False].
*   **conditional** (*bool*) – if True save the amplitudes vector conditional on the current classical register values \[Default: False].

**Raises**

**ExtensionError** – if params is invalid for the specified number of qubits.

## Methods

|                                                                                                                                                                           |                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [`__init__`](#qiskit.providers.aer.library.SaveAmplitudes.__init__ "qiskit.providers.aer.library.SaveAmplitudes.__init__")(num\_qubits, params\[, label, …])              | Instruction to save complex statevector amplitudes.                      |
| [`add_decomposition`](#qiskit.providers.aer.library.SaveAmplitudes.add_decomposition "qiskit.providers.aer.library.SaveAmplitudes.add_decomposition")(decomposition)      | Add a decomposition of the instruction to the SessionEquivalenceLibrary. |
| [`assemble`](#qiskit.providers.aer.library.SaveAmplitudes.assemble "qiskit.providers.aer.library.SaveAmplitudes.assemble")()                                              | Return the QasmQobjInstruction for the intructions.                      |
| [`broadcast_arguments`](#qiskit.providers.aer.library.SaveAmplitudes.broadcast_arguments "qiskit.providers.aer.library.SaveAmplitudes.broadcast_arguments")(qargs, cargs) | Validation of the arguments.                                             |
| [`c_if`](#qiskit.providers.aer.library.SaveAmplitudes.c_if "qiskit.providers.aer.library.SaveAmplitudes.c_if")(classical, val)                                            | Add classical condition on register classical and value val.             |
| [`copy`](#qiskit.providers.aer.library.SaveAmplitudes.copy "qiskit.providers.aer.library.SaveAmplitudes.copy")(\[name])                                                   | Copy of the instruction.                                                 |
| [`inverse`](#qiskit.providers.aer.library.SaveAmplitudes.inverse "qiskit.providers.aer.library.SaveAmplitudes.inverse")()                                                 | Special case.                                                            |
| [`is_parameterized`](#qiskit.providers.aer.library.SaveAmplitudes.is_parameterized "qiskit.providers.aer.library.SaveAmplitudes.is_parameterized")()                      | Return True .IFF.                                                        |
| [`mirror`](#qiskit.providers.aer.library.SaveAmplitudes.mirror "qiskit.providers.aer.library.SaveAmplitudes.mirror")()                                                    | DEPRECATED: use instruction.reverse\_ops().                              |
| [`qasm`](#qiskit.providers.aer.library.SaveAmplitudes.qasm "qiskit.providers.aer.library.SaveAmplitudes.qasm")()                                                          | Return a default OpenQASM string for the instruction.                    |
| [`repeat`](#qiskit.providers.aer.library.SaveAmplitudes.repeat "qiskit.providers.aer.library.SaveAmplitudes.repeat")(n)                                                   | Creates an instruction with gate repeated n amount of times.             |
| [`reverse_ops`](#qiskit.providers.aer.library.SaveAmplitudes.reverse_ops "qiskit.providers.aer.library.SaveAmplitudes.reverse_ops")()                                     | For a composite instruction, reverse the order of sub-instructions.      |
| [`soft_compare`](#qiskit.providers.aer.library.SaveAmplitudes.soft_compare "qiskit.providers.aer.library.SaveAmplitudes.soft_compare")(other)                             | Soft comparison between gates.                                           |
| [`validate_parameter`](#qiskit.providers.aer.library.SaveAmplitudes.validate_parameter "qiskit.providers.aer.library.SaveAmplitudes.validate_parameter")(parameter)       | Instruction parameters has no validation or normalization.               |

## Attributes

|                                                                                                                                              |                                                                               |
| -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`decompositions`](#qiskit.providers.aer.library.SaveAmplitudes.decompositions "qiskit.providers.aer.library.SaveAmplitudes.decompositions") | Get the decompositions of the instruction from the SessionEquivalenceLibrary. |
| [`definition`](#qiskit.providers.aer.library.SaveAmplitudes.definition "qiskit.providers.aer.library.SaveAmplitudes.definition")             | Return definition in terms of other basic gates.                              |
| [`duration`](#qiskit.providers.aer.library.SaveAmplitudes.duration "qiskit.providers.aer.library.SaveAmplitudes.duration")                   | Get the duration.                                                             |
| [`params`](#qiskit.providers.aer.library.SaveAmplitudes.params "qiskit.providers.aer.library.SaveAmplitudes.params")                         | return instruction params.                                                    |
| [`unit`](#qiskit.providers.aer.library.SaveAmplitudes.unit "qiskit.providers.aer.library.SaveAmplitudes.unit")                               | Get the time unit of duration.                                                |

<span id="undefined" />

`add_decomposition(decomposition)`

Add a decomposition of the instruction to the SessionEquivalenceLibrary.

<span id="undefined" />

`assemble()`

Return the QasmQobjInstruction for the intructions.

<span id="undefined" />

`broadcast_arguments(qargs, cargs)`

Validation of the arguments.

**Parameters**

*   **qargs** (*List*) – List of quantum bit arguments.
*   **cargs** (*List*) – List of classical bit arguments.

**Yields**

*Tuple(List, List)* – A tuple with single arguments.

**Raises**

**CircuitError** – If the input is not valid. For example, the number of arguments does not match the gate expectation.

<span id="undefined" />

`c_if(classical, val)`

Add classical condition on register classical and value val.

<span id="undefined" />

`copy(name=None)`

Copy of the instruction.

**Parameters**

**name** (*str*) – name to be given to the copied circuit, if None then the name stays the same.

**Returns**

**a copy of the current instruction, with the name**

updated if it was provided

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property decompositions`

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="undefined" />

`property definition`

Return definition in terms of other basic gates.

<span id="undefined" />

`property duration`

Get the duration.

<span id="undefined" />

`inverse()`

Special case. Return self.

<span id="undefined" />

`is_parameterized()`

Return True .IFF. instruction is parameterized else False

<span id="undefined" />

`mirror()`

DEPRECATED: use instruction.reverse\_ops().

**Returns**

**a new instruction with sub-instructions**

reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property params`

return instruction params.

<span id="undefined" />

`qasm()`

Return a default OpenQASM string for the instruction.

Derived instructions may override this to print in a different format (e.g. measure q\[0] -> c\[0];).

<span id="undefined" />

`repeat(n)`

Creates an instruction with gate repeated n amount of times.

**Parameters**

**n** (*int*) – Number of times to repeat the instruction

**Returns**

Containing the definition.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

**Raises**

**CircuitError** – If n \< 1.

<span id="undefined" />

`reverse_ops()`

For a composite instruction, reverse the order of sub-instructions.

This is done by recursively reversing all sub-instructions. It does not invert any gate.

**Returns**

**a new instruction with**

sub-instructions reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`soft_compare(other)`

Soft comparison between gates. Their names, number of qubits, and classical bit numbers must match. The number of parameters must match. Each parameter is compared. If one is a ParameterExpression then it is not taken into account.

**Parameters**

**other** (*instruction*) – other instruction.

**Returns**

are self and other equal up to parameter expressions.

**Return type**

bool

<span id="undefined" />

`property unit`

Get the time unit of duration.

<span id="undefined" />

`validate_parameter(parameter)`

Instruction parameters has no validation or normalization.
