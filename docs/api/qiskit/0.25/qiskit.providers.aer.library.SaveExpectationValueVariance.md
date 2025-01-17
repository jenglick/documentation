# qiskit.providers.aer.library.SaveExpectationValueVariance

<span id="undefined" />

`SaveExpectationValueVariance(operator, label='expectation_value_variance', unnormalized=False, pershot=False, conditional=False)`

Save expectation value and variance of an operator.

Instruction to save the expectation value and variance of a Hermitian operator.

The expectation value of a Hermitian operator $H$ for a simulator in quantum state :math\`rho\`is given by $\langle H\rangle = \mbox{Tr}[H.\rho]$. The variance is given by $\sigma^2 = \langle H^2 \rangle - \langle H \rangle>^2$.

**Parameters**

*   **operator** ([*Pauli*](qiskit.quantum_info.Pauli#qiskit.quantum_info.Pauli "qiskit.quantum_info.Pauli")  *or*[*SparsePauliOp*](qiskit.quantum_info.SparsePauliOp#qiskit.quantum_info.SparsePauliOp "qiskit.quantum_info.SparsePauliOp")  *or*[*Operator*](qiskit.quantum_info.Operator#qiskit.quantum_info.Operator "qiskit.quantum_info.Operator")) – a Hermitian operator.
*   **label** (*str*) – the key for retrieving saved data from results.
*   **unnormalized** (*bool*) – If True return save the unnormalized accumulated or conditional accumulated expectation value over all shot \[Default: False].
*   **pershot** (*bool*) – if True save a list of expectation values for each shot of the simulation rather than the average over all shots \[Default: False].
*   **conditional** (*bool*) – if True save the average or pershot data conditional on the current classical register values \[Default: False].

**Raises**

**ExtensionError** – if the input operator is invalid or not Hermitian.

<Admonition title="Note" type="note">
  This instruction can be directly appended to a circuit using the [`save_expectation_value()`](qiskit.providers.aer.library.save_expectation_value#qiskit.providers.aer.library.save_expectation_value "qiskit.providers.aer.library.save_expectation_value") circuit method.
</Admonition>

<span id="undefined" />

`__init__(operator, label='expectation_value_variance', unnormalized=False, pershot=False, conditional=False)`

Instruction to save the expectation value and variance of a Hermitian operator.

The expectation value of a Hermitian operator $H$ for a simulator in quantum state :math\`rho\`is given by $\langle H\rangle = \mbox{Tr}[H.\rho]$. The variance is given by $\sigma^2 = \langle H^2 \rangle - \langle H \rangle>^2$.

**Parameters**

*   **operator** ([*Pauli*](qiskit.quantum_info.Pauli#qiskit.quantum_info.Pauli "qiskit.quantum_info.Pauli")  *or*[*SparsePauliOp*](qiskit.quantum_info.SparsePauliOp#qiskit.quantum_info.SparsePauliOp "qiskit.quantum_info.SparsePauliOp")  *or*[*Operator*](qiskit.quantum_info.Operator#qiskit.quantum_info.Operator "qiskit.quantum_info.Operator")) – a Hermitian operator.
*   **label** (*str*) – the key for retrieving saved data from results.
*   **unnormalized** (*bool*) – If True return save the unnormalized accumulated or conditional accumulated expectation value over all shot \[Default: False].
*   **pershot** (*bool*) – if True save a list of expectation values for each shot of the simulation rather than the average over all shots \[Default: False].
*   **conditional** (*bool*) – if True save the average or pershot data conditional on the current classical register values \[Default: False].

**Raises**

**ExtensionError** – if the input operator is invalid or not Hermitian.

<Admonition title="Note" type="note">
  This instruction can be directly appended to a circuit using the [`save_expectation_value()`](qiskit.providers.aer.library.save_expectation_value#qiskit.providers.aer.library.save_expectation_value "qiskit.providers.aer.library.save_expectation_value") circuit method.
</Admonition>

## Methods

|                                                                                                                                                                                                       |                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.providers.aer.library.SaveExpectationValueVariance.__init__ "qiskit.providers.aer.library.SaveExpectationValueVariance.__init__")(operator\[, label, unnormalized, …])           | Instruction to save the expectation value and variance of a Hermitian operator. |
| [`add_decomposition`](#qiskit.providers.aer.library.SaveExpectationValueVariance.add_decomposition "qiskit.providers.aer.library.SaveExpectationValueVariance.add_decomposition")(decomposition)      | Add a decomposition of the instruction to the SessionEquivalenceLibrary.        |
| [`assemble`](#qiskit.providers.aer.library.SaveExpectationValueVariance.assemble "qiskit.providers.aer.library.SaveExpectationValueVariance.assemble")()                                              | Return the QasmQobjInstruction for the intructions.                             |
| [`broadcast_arguments`](#qiskit.providers.aer.library.SaveExpectationValueVariance.broadcast_arguments "qiskit.providers.aer.library.SaveExpectationValueVariance.broadcast_arguments")(qargs, cargs) | Validation of the arguments.                                                    |
| [`c_if`](#qiskit.providers.aer.library.SaveExpectationValueVariance.c_if "qiskit.providers.aer.library.SaveExpectationValueVariance.c_if")(classical, val)                                            | Add classical condition on register classical and value val.                    |
| [`copy`](#qiskit.providers.aer.library.SaveExpectationValueVariance.copy "qiskit.providers.aer.library.SaveExpectationValueVariance.copy")(\[name])                                                   | Copy of the instruction.                                                        |
| [`inverse`](#qiskit.providers.aer.library.SaveExpectationValueVariance.inverse "qiskit.providers.aer.library.SaveExpectationValueVariance.inverse")()                                                 | Special case.                                                                   |
| [`is_parameterized`](#qiskit.providers.aer.library.SaveExpectationValueVariance.is_parameterized "qiskit.providers.aer.library.SaveExpectationValueVariance.is_parameterized")()                      | Return True .IFF.                                                               |
| [`mirror`](#qiskit.providers.aer.library.SaveExpectationValueVariance.mirror "qiskit.providers.aer.library.SaveExpectationValueVariance.mirror")()                                                    | DEPRECATED: use instruction.reverse\_ops().                                     |
| [`qasm`](#qiskit.providers.aer.library.SaveExpectationValueVariance.qasm "qiskit.providers.aer.library.SaveExpectationValueVariance.qasm")()                                                          | Return a default OpenQASM string for the instruction.                           |
| [`repeat`](#qiskit.providers.aer.library.SaveExpectationValueVariance.repeat "qiskit.providers.aer.library.SaveExpectationValueVariance.repeat")(n)                                                   | Creates an instruction with gate repeated n amount of times.                    |
| [`reverse_ops`](#qiskit.providers.aer.library.SaveExpectationValueVariance.reverse_ops "qiskit.providers.aer.library.SaveExpectationValueVariance.reverse_ops")()                                     | For a composite instruction, reverse the order of sub-instructions.             |
| [`soft_compare`](#qiskit.providers.aer.library.SaveExpectationValueVariance.soft_compare "qiskit.providers.aer.library.SaveExpectationValueVariance.soft_compare")(other)                             | Soft comparison between gates.                                                  |
| [`validate_parameter`](#qiskit.providers.aer.library.SaveExpectationValueVariance.validate_parameter "qiskit.providers.aer.library.SaveExpectationValueVariance.validate_parameter")(parameter)       | Instruction parameters has no validation or normalization.                      |

## Attributes

|                                                                                                                                                                          |                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| [`decompositions`](#qiskit.providers.aer.library.SaveExpectationValueVariance.decompositions "qiskit.providers.aer.library.SaveExpectationValueVariance.decompositions") | Get the decompositions of the instruction from the SessionEquivalenceLibrary. |
| [`definition`](#qiskit.providers.aer.library.SaveExpectationValueVariance.definition "qiskit.providers.aer.library.SaveExpectationValueVariance.definition")             | Return definition in terms of other basic gates.                              |
| [`duration`](#qiskit.providers.aer.library.SaveExpectationValueVariance.duration "qiskit.providers.aer.library.SaveExpectationValueVariance.duration")                   | Get the duration.                                                             |
| [`params`](#qiskit.providers.aer.library.SaveExpectationValueVariance.params "qiskit.providers.aer.library.SaveExpectationValueVariance.params")                         | return instruction params.                                                    |
| [`unit`](#qiskit.providers.aer.library.SaveExpectationValueVariance.unit "qiskit.providers.aer.library.SaveExpectationValueVariance.unit")                               | Get the time unit of duration.                                                |

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
