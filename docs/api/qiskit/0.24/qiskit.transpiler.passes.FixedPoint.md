<span id="qiskit-transpiler-passes-fixedpoint" />

# qiskit.transpiler.passes.FixedPoint

<span id="undefined" />

`FixedPoint(*args, **kwargs)`

Check if a property reached a fixed point.

A dummy analysis pass that checks if a property reached a fixed point. The results is saved in `property_set['<property>_fixed_point']` as a boolean.

FixedPoint initializer.

**Parameters**

**property\_to\_check** (*str*) – The property to check if a fixed point was reached.

<span id="undefined" />

`__init__(property_to_check)`

FixedPoint initializer.

**Parameters**

**property\_to\_check** (*str*) – The property to check if a fixed point was reached.

## Methods

|                                                                                                                                 |                                 |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| [`__init__`](#qiskit.transpiler.passes.FixedPoint.__init__ "qiskit.transpiler.passes.FixedPoint.__init__")(property\_to\_check) | FixedPoint initializer.         |
| [`name`](#qiskit.transpiler.passes.FixedPoint.name "qiskit.transpiler.passes.FixedPoint.name")()                                | Return the name of the pass.    |
| [`run`](#qiskit.transpiler.passes.FixedPoint.run "qiskit.transpiler.passes.FixedPoint.run")(dag)                                | Run the FixedPoint pass on dag. |

## Attributes

|                                                                                                                                                      |                                             |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [`is_analysis_pass`](#qiskit.transpiler.passes.FixedPoint.is_analysis_pass "qiskit.transpiler.passes.FixedPoint.is_analysis_pass")                   | Check if the pass is an analysis pass.      |
| [`is_transformation_pass`](#qiskit.transpiler.passes.FixedPoint.is_transformation_pass "qiskit.transpiler.passes.FixedPoint.is_transformation_pass") | Check if the pass is a transformation pass. |

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

`run(dag)`

Run the FixedPoint pass on dag.
