<span id="qiskit-chemistry-components-variational-forms-chc" />

# qiskit.chemistry.components.variational\_forms.CHC

<span id="undefined" />

`CHC(num_qubits=None, reps=1, ladder=False, excitations=None, entanglement='full', initial_state=None)`

This trial wavefunction is the Compact Heuristic for Chemistry.

The trial wavefunction is as defined in Ollitrault Pauline J., Chemical science 11 (2020): 6842-6855. It aims at approximating the UCC Ansatz for a lower CNOT count.

<Admonition title="Note" type="note">
  It is not particle number conserving and the accuracy of the approximation decreases with the number of excitations.
</Admonition>

**Parameters**

*   **num\_qubits** (`Optional`\[`int`]) – number of qubits
*   **reps** (`int`) – number of replica of basic module
*   **ladder** (`bool`) – use ladder of CNOTs between to indices in the entangling block
*   **excitations** (`Optional`\[`List`\[`List`\[`int`]]]) – indices corresponding to the excitations to include in the circuit
*   **entanglement** (`Union`\[`str`, `List`\[`int`]]) – physical connections between the qubits
*   **initial\_state** (`Optional`\[`InitialState`]) – an initial state object

<span id="undefined" />

`__init__(num_qubits=None, reps=1, ladder=False, excitations=None, entanglement='full', initial_state=None)`

**Parameters**

*   **num\_qubits** (`Optional`\[`int`]) – number of qubits
*   **reps** (`int`) – number of replica of basic module
*   **ladder** (`bool`) – use ladder of CNOTs between to indices in the entangling block
*   **excitations** (`Optional`\[`List`\[`List`\[`int`]]]) – indices corresponding to the excitations to include in the circuit
*   **entanglement** (`Union`\[`str`, `List`\[`int`]]) – physical connections between the qubits
*   **initial\_state** (`Optional`\[`InitialState`]) – an initial state object

## Methods

|                                                                                                                                                                                                               |                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| [`__init__`](#qiskit.chemistry.components.variational_forms.CHC.__init__ "qiskit.chemistry.components.variational_forms.CHC.__init__")(\[num\_qubits, reps, ladder, …])                                       | **type num\_qubits**`Optional`\[`int`]                |
| [`construct_circuit`](#qiskit.chemistry.components.variational_forms.CHC.construct_circuit "qiskit.chemistry.components.variational_forms.CHC.construct_circuit")(parameters\[, q])                           | Construct the variational form, given its parameters. |
| [`get_entangler_map`](#qiskit.chemistry.components.variational_forms.CHC.get_entangler_map "qiskit.chemistry.components.variational_forms.CHC.get_entangler_map")(map\_type, num\_qubits\[, offset])          | returns entangler map                                 |
| [`validate_entangler_map`](#qiskit.chemistry.components.variational_forms.CHC.validate_entangler_map "qiskit.chemistry.components.variational_forms.CHC.validate_entangler_map")(entangler\_map, num\_qubits) | validate entangler map                                |

## Attributes

|                                                                                                                                                                                                       |                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [`num_parameters`](#qiskit.chemistry.components.variational_forms.CHC.num_parameters "qiskit.chemistry.components.variational_forms.CHC.num_parameters")                                              | Number of parameters of the variational form.               |
| [`num_qubits`](#qiskit.chemistry.components.variational_forms.CHC.num_qubits "qiskit.chemistry.components.variational_forms.CHC.num_qubits")                                                          | Number of qubits of the variational form.                   |
| [`parameter_bounds`](#qiskit.chemistry.components.variational_forms.CHC.parameter_bounds "qiskit.chemistry.components.variational_forms.CHC.parameter_bounds")                                        | Parameter bounds.                                           |
| [`preferred_init_points`](#qiskit.chemistry.components.variational_forms.CHC.preferred_init_points "qiskit.chemistry.components.variational_forms.CHC.preferred_init_points")                         | Return preferred init points.                               |
| [`setting`](#qiskit.chemistry.components.variational_forms.CHC.setting "qiskit.chemistry.components.variational_forms.CHC.setting")                                                                   |                                                             |
| [`support_parameterized_circuit`](#qiskit.chemistry.components.variational_forms.CHC.support_parameterized_circuit "qiskit.chemistry.components.variational_forms.CHC.support_parameterized_circuit") | Whether or not the sub-class support parameterized circuit. |

<span id="undefined" />

`construct_circuit(parameters, q=None)`

Construct the variational form, given its parameters.

**Parameters**

*   **parameters** (`Union`\[`ndarray`, `List`\[`Parameter`], `ParameterVector`]) – circuit parameters
*   **q** (`Optional`\[`QuantumRegister`]) – Quantum Register for the circuit.

**Returns**

a quantum circuit with given parameters

**Return type**

[QuantumCircuit](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")

**Raises**

*   **ValueError** – the number of parameters is incorrect.
*   **ValueError** – if num\_qubits has not been set and is still None
*   **ValueError** – only supports single and double excitations at the moment.

<span id="undefined" />

`static get_entangler_map(map_type, num_qubits, offset=0)`

returns entangler map

<span id="undefined" />

`property num_parameters`

Number of parameters of the variational form.

**Returns**

An integer indicating the number of parameters.

**Return type**

int

<span id="undefined" />

`property num_qubits`

Number of qubits of the variational form.

**Returns**

An integer indicating the number of qubits.

**Return type**

int

<span id="undefined" />

`property parameter_bounds`

Parameter bounds.

**Returns**

A list of pairs indicating the bounds, as (lower, upper). None indicates an unbounded parameter in the corresponding direction. If None is returned, problem is fully unbounded.

**Return type**

list

<span id="undefined" />

`property preferred_init_points`

Return preferred init points.

If an initial state is provided then the variational form may provide back this set of parameters which when used on the variational form should result in the overall state being that defined by the initial state

<span id="undefined" />

`property setting`

<span id="undefined" />

`property support_parameterized_circuit`

Whether or not the sub-class support parameterized circuit.

**Returns**

indicate the sub-class support parameterized circuit

**Return type**

boolean

<span id="undefined" />

`static validate_entangler_map(entangler_map, num_qubits)`

validate entangler map
