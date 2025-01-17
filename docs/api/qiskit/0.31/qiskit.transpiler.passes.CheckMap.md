# CheckMap

<span id="undefined" />

`CheckMap(*args, **kwargs)`

Bases: `qiskit.transpiler.basepasses.AnalysisPass`

Check if a DAG circuit is already mapped to a coupling map.

Check if a DAGCircuit is mapped to coupling\_map by checking that all 2-qubit interactions are laid out to be physically close, setting the property `is_swap_mapped` to `True` or `False` accordingly.

CheckMap initializer.

**Parameters**

**coupling\_map** ([*CouplingMap*](qiskit.transpiler.CouplingMap#qiskit.transpiler.CouplingMap "qiskit.transpiler.CouplingMap")) – Directed graph representing a coupling map.

## Methods

|                                                                                                                                  |                               |
| -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| [`name`](qiskit.transpiler.passes.CheckMap.name#qiskit.transpiler.passes.CheckMap.name "qiskit.transpiler.passes.CheckMap.name") | Return the name of the pass.  |
| [`run`](qiskit.transpiler.passes.CheckMap.run#qiskit.transpiler.passes.CheckMap.run "qiskit.transpiler.passes.CheckMap.run")     | Run the CheckMap pass on dag. |

## Attributes

<span id="undefined" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="undefined" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).
