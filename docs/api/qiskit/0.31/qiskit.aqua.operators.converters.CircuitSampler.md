# CircuitSampler

<span id="undefined" />

`CircuitSampler(backend, statevector=None, param_qobj=False, attach_results=False)`

Bases: `qiskit.aqua.operators.converters.converter_base.ConverterBase`

The CircuitSampler traverses an Operator and converts any CircuitStateFns into approximations of the state function by a DictStateFn or VectorStateFn using a quantum backend. Note that in order to approximate the value of the CircuitStateFn, it must 1) send state function through a depolarizing channel, which will destroy all phase information and 2) replace the sampled frequencies with **square roots** of the frequency, rather than the raw probability of sampling (which would be the equivalent of sampling the **square** of the state function, per the Born rule.

The CircuitSampler aggressively caches transpiled circuits to handle re-parameterization of the same circuit efficiently. If you are converting multiple different Operators, you are better off using a different CircuitSampler for each Operator to avoid cache thrashing.

**Parameters**

*   **backend** (`Union`\[`Backend`, `BaseBackend`, `QuantumInstance`]) – The quantum backend or QuantumInstance to use to sample the circuits.
*   **statevector** (`Optional`\[`bool`]) – If backend is a statevector backend, whether to replace the CircuitStateFns with DictStateFns (from the counts) or VectorStateFns (from the statevector). `None` will set this argument automatically based on the backend.
*   **attach\_results** (`bool`) – Whether to attach the data from the backend `Results` object for a given `` CircuitStateFn` `` to an `execution_results` field added the converted `DictStateFn` or `VectorStateFn`.
*   **param\_qobj** (`bool`) – Whether to use Aer’s parameterized Qobj capability to avoid re-assembling the circuits.

**Raises**

**ValueError** – Set statevector or param\_qobj True when not supported by backend.

## Methods

|                                                                                                                                                                                                                        |                                                                                                                                   |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| [`convert`](qiskit.aqua.operators.converters.CircuitSampler.convert#qiskit.aqua.operators.converters.CircuitSampler.convert "qiskit.aqua.operators.converters.CircuitSampler.convert")                                 | Converts the Operator to one in which the CircuitStateFns are replaced by DictStateFns or VectorStateFns.                         |
| [`sample_circuits`](qiskit.aqua.operators.converters.CircuitSampler.sample_circuits#qiskit.aqua.operators.converters.CircuitSampler.sample_circuits "qiskit.aqua.operators.converters.CircuitSampler.sample_circuits") | Samples the CircuitStateFns and returns a dict associating their `id()` values to their replacement DictStateFn or VectorStateFn. |
| [`set_backend`](qiskit.aqua.operators.converters.CircuitSampler.set_backend#qiskit.aqua.operators.converters.CircuitSampler.set_backend "qiskit.aqua.operators.converters.CircuitSampler.set_backend")                 | Sets backend with configuration.                                                                                                  |

## Attributes

<span id="undefined" />

### backend

Returns the backend.

**Return type**

`Union`\[`Backend`, `BaseBackend`]

**Returns**

The backend used by the CircuitSampler

<span id="undefined" />

### quantum\_instance

Returns the quantum instance.

**Return type**

`QuantumInstance`

**Returns**

The QuantumInstance used by the CircuitSampler
