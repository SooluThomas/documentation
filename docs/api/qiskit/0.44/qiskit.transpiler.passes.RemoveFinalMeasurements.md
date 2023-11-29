---
title: RemoveFinalMeasurements
description: API reference for qiskit.transpiler.passes.RemoveFinalMeasurements
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.RemoveFinalMeasurements
---

# RemoveFinalMeasurements

<span id="qiskit.transpiler.passes.RemoveFinalMeasurements" />

`qiskit.transpiler.passes.RemoveFinalMeasurements(*args, **kwargs)`

Bases: [`TransformationPass`](qiskit.transpiler.TransformationPass "qiskit.transpiler.basepasses.TransformationPass")

Remove final measurements and barriers at the end of a circuit.

This pass removes final barriers and final measurements, as well as all unused classical registers and bits they are connected to. Measurements and barriers are considered final if they are followed by no other operations (aside from other measurements or barriers.)

Classical registers are removed iff they reference at least one bit that has become unused by the circuit as a result of the operation, and all of their other bits are also unused. Seperately, classical bits are removed iff they have become unused by the circuit as a result of the operation, or they appear in a removed classical register, but do not appear in a classical register that will remain.

## Attributes

<span id="qiskit.transpiler.passes.RemoveFinalMeasurements.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit.transpiler.passes.RemoveFinalMeasurements.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### name

<span id="qiskit.transpiler.passes.RemoveFinalMeasurements.name" />

`name()`

Return the name of the pass.

### run

<span id="qiskit.transpiler.passes.RemoveFinalMeasurements.run" />

`run(dag)`

Run the RemoveFinalMeasurements pass on dag.

**Parameters**

**dag** ([*DAGCircuit*](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")) – the DAG to be optimized.

**Returns**

the optimized DAG.

**Return type**

[DAGCircuit](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")
