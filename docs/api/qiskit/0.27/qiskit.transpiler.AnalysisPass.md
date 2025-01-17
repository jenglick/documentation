# qiskit.transpiler.AnalysisPass

<span id="undefined" />

`AnalysisPass(*args, **kwargs)`

An analysis pass: change property set, not DAG.

<span id="undefined" />

`__init__()`

Initialize self. See help(type(self)) for accurate signature.

## Methods

|                                                                                                    |                               |
| -------------------------------------------------------------------------------------------------- | ----------------------------- |
| [`__init__`](#qiskit.transpiler.AnalysisPass.__init__ "qiskit.transpiler.AnalysisPass.__init__")() | Initialize self.              |
| [`name`](#qiskit.transpiler.AnalysisPass.name "qiskit.transpiler.AnalysisPass.name")()             | Return the name of the pass.  |
| [`run`](#qiskit.transpiler.AnalysisPass.run "qiskit.transpiler.AnalysisPass.run")(dag)             | Run a pass on the DAGCircuit. |

## Attributes

|                                                                                                                                            |                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------- |
| [`is_analysis_pass`](#qiskit.transpiler.AnalysisPass.is_analysis_pass "qiskit.transpiler.AnalysisPass.is_analysis_pass")                   | Check if the pass is an analysis pass.      |
| [`is_transformation_pass`](#qiskit.transpiler.AnalysisPass.is_transformation_pass "qiskit.transpiler.AnalysisPass.is_transformation_pass") | Check if the pass is a transformation pass. |

<span id="undefined" />

`property is_analysis_pass`

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="undefined" />

`property is_transformation_pass`

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

<span id="undefined" />

`name()`

Return the name of the pass.

<span id="undefined" />

`abstract run(dag)`

Run a pass on the DAGCircuit. This is implemented by the pass developer.

**Parameters**

**dag** ([*DAGCircuit*](qiskit.dagcircuit.DAGCircuit#qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")) – the dag on which the pass is run.

**Raises**

**NotImplementedError** – when this is left unimplemented for a pass.
