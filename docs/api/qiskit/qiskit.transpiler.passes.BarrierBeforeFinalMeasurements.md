---
title: BarrierBeforeFinalMeasurements
description: API reference for qiskit.transpiler.passes.BarrierBeforeFinalMeasurements
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.BarrierBeforeFinalMeasurements
---

# BarrierBeforeFinalMeasurements

<span id="qiskit.transpiler.passes.BarrierBeforeFinalMeasurements" />

`qiskit.transpiler.passes.BarrierBeforeFinalMeasurements(*args, **kwargs)`

Bases: [`TransformationPass`](qiskit.transpiler.TransformationPass "qiskit.transpiler.basepasses.TransformationPass")

Add a barrier before final measurements.

This pass adds a barrier before the set of final measurements. Measurements are considered final if they are followed by no other operations (aside from other measurements or barriers.)

## Attributes

<span id="qiskit.transpiler.passes.BarrierBeforeFinalMeasurements.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit.transpiler.passes.BarrierBeforeFinalMeasurements.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### name

<span id="qiskit.transpiler.passes.BarrierBeforeFinalMeasurements.name" />

`name()`

Return the name of the pass.

### run

<span id="qiskit.transpiler.passes.BarrierBeforeFinalMeasurements.run" />

`run(dag)`

Run the BarrierBeforeFinalMeasurements pass on dag.
