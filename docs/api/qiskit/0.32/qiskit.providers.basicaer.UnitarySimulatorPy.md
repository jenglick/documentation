# UnitarySimulatorPy

<span id="undefined" />

`UnitarySimulatorPy(configuration=None, provider=None, **fields)`

Bases: `qiskit.providers.backend.BackendV1`

Python implementation of a unitary simulator.

Initialize a backend class

**Parameters**

*   **configuration** ([*BackendConfiguration*](qiskit.providers.models.BackendConfiguration#qiskit.providers.models.BackendConfiguration "qiskit.providers.models.BackendConfiguration")) – A backend configuration object for the backend object.
*   **provider** ([*qiskit.providers.Provider*](qiskit.providers.Provider#qiskit.providers.Provider "qiskit.providers.Provider")) – Optionally, the provider object that this Backend comes from.
*   **fields** – kwargs for the values to use to override the default options.

**Raises**

**AttributeError** – if input field not a valid options

In addition to the public abstract methods, subclasses should also implement the following private methods:

<span id="undefined" />

`classmethod _default_options()`

Return the default options

This method will return a [`qiskit.providers.Options`](qiskit.providers.Options#qiskit.providers.Options "qiskit.providers.Options") subclass object that will be used for the default options. These should be the default parameters to use for the options of the backend.

**Returns**

**A options object with**

default values set

**Return type**

[qiskit.providers.Options](qiskit.providers.Options#qiskit.providers.Options "qiskit.providers.Options")

## Methods

|                                                                                                                                                                                                           |                                                                    |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [`configuration`](qiskit.providers.basicaer.UnitarySimulatorPy.configuration#qiskit.providers.basicaer.UnitarySimulatorPy.configuration "qiskit.providers.basicaer.UnitarySimulatorPy.configuration")     | Return the backend configuration.                                  |
| [`name`](qiskit.providers.basicaer.UnitarySimulatorPy.name#qiskit.providers.basicaer.UnitarySimulatorPy.name "qiskit.providers.basicaer.UnitarySimulatorPy.name")                                         | Return the backend name.                                           |
| [`properties`](qiskit.providers.basicaer.UnitarySimulatorPy.properties#qiskit.providers.basicaer.UnitarySimulatorPy.properties "qiskit.providers.basicaer.UnitarySimulatorPy.properties")                 | Return the backend properties.                                     |
| [`provider`](qiskit.providers.basicaer.UnitarySimulatorPy.provider#qiskit.providers.basicaer.UnitarySimulatorPy.provider "qiskit.providers.basicaer.UnitarySimulatorPy.provider")                         | Return the backend Provider.                                       |
| [`run`](qiskit.providers.basicaer.UnitarySimulatorPy.run#qiskit.providers.basicaer.UnitarySimulatorPy.run "qiskit.providers.basicaer.UnitarySimulatorPy.run")                                             | Run qobj asynchronously.                                           |
| [`run_experiment`](qiskit.providers.basicaer.UnitarySimulatorPy.run_experiment#qiskit.providers.basicaer.UnitarySimulatorPy.run_experiment "qiskit.providers.basicaer.UnitarySimulatorPy.run_experiment") | Run an experiment (circuit) and return a single experiment result. |
| [`set_options`](qiskit.providers.basicaer.UnitarySimulatorPy.set_options#qiskit.providers.basicaer.UnitarySimulatorPy.set_options "qiskit.providers.basicaer.UnitarySimulatorPy.set_options")             | Set the options fields for the backend                             |
| [`status`](qiskit.providers.basicaer.UnitarySimulatorPy.status#qiskit.providers.basicaer.UnitarySimulatorPy.status "qiskit.providers.basicaer.UnitarySimulatorPy.status")                                 | Return the backend status.                                         |

## Attributes

<span id="undefined" />

### DEFAULT\_CONFIGURATION = \{'backend\_name'

`= {'backend_name':`

`= {'backend_name': 'unitary_simulator', 'backend_version': '1.1.0', 'basis_gates': ['u1', 'u2', 'u3', 'rz', 'sx', 'x', 'cx', 'id', 'unitary'], 'conditional': False, 'coupling_map': None, 'description': 'A python simulator for unitary matrix corresponding to a circuit', 'gates': [{'name': 'u1', 'parameters': ['lambda'], 'qasm_def': 'gate u1(lambda) q { U(0,0,lambda) q; }'}, {'name': 'u2', 'parameters': ['phi', 'lambda'], 'qasm_def': 'gate u2(phi,lambda) q { U(pi/2,phi,lambda) q; }'}, {'name': 'u3', 'parameters': ['theta', 'phi', 'lambda'], 'qasm_def': 'gate u3(theta,phi,lambda) q { U(theta,phi,lambda) q; }'}, {'name': 'rz', 'parameters': ['phi'], 'qasm_def': 'gate rz(phi) q { U(0,0,phi) q; }'}, {'name': 'sx', 'parameters': [], 'qasm_def': 'gate sx(phi) q { U(pi/2,7*pi/2,pi/2) q; }'}, {'name': 'x', 'parameters': [], 'qasm_def': 'gate x q { U(pi,7*pi/2,pi/2) q; }'}, {'name': 'cx', 'parameters': [], 'qasm_def': 'gate cx c,t { CX c,t; }'}, {'name': 'id', 'parameters': [], 'qasm_def': 'gate id a { U(0,0,0) a; }'}, {'name': 'unitary', 'parameters': ['matrix'], 'qasm_def': 'unitary(matrix) q1, q2,...'}], 'local': True, 'max_shots': 65536, 'memory': False, 'n_qubits': 16, 'open_pulse': False, 'simulator': True, 'url': 'https://github.com/Qiskit/qiskit-terra'}`

<span id="undefined" />

### DEFAULT\_OPTIONS = \{'chop\_threshold'

`= {'chop_threshold':`

`= {'chop_threshold': 1e-15, 'initial_unitary': None}`

<span id="undefined" />

### MAX\_QUBITS\_MEMORY

`= 16`

<span id="undefined" />

### options

Return the options for the backend

The options of a backend are the dynamic parameters defining how the backend is used. These are used to control the [`run()`](qiskit.providers.basicaer.UnitarySimulatorPy.run#qiskit.providers.basicaer.UnitarySimulatorPy.run "qiskit.providers.basicaer.UnitarySimulatorPy.run") method.

<span id="undefined" />

### version

`= 1`
