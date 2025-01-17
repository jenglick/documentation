# AbelianGrouper

<span id="undefined" />

`AbelianGrouper(traverse=True)`

Bases: `qiskit.aqua.operators.converters.converter_base.ConverterBase`

The AbelianGrouper converts SummedOps into a sum of Abelian sums.

Meaning, it will traverse the Operator, and when it finds a SummedOp, it will evaluate which of the summed sub-Operators commute with one another. It will then convert each of the groups of commuting Operators into their own SummedOps, and return the sum-of-commuting-SummedOps. This is particularly useful for cases where mutually commuting groups can be handled similarly, as in the case of Pauli Expectations, where commuting Paulis have the same diagonalizing circuit rotation, or Pauli Evolutions, where commuting Paulis can be diagonalized together.

**Parameters**

**traverse** (`bool`) – Whether to convert only the Operator passed to `convert`, or traverse down that Operator.

## Methods

|                                                                                                                                                                                                            |                                                                                                                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`convert`](qiskit.aqua.operators.converters.AbelianGrouper.convert#qiskit.aqua.operators.converters.AbelianGrouper.convert "qiskit.aqua.operators.converters.AbelianGrouper.convert")                     | Check if operator is a SummedOp, in which case covert it into a sum of mutually commuting sums, or if the Operator contains sub-Operators and `traverse` is True, attempt to convert any sub-Operators. |
| [`group_subops`](qiskit.aqua.operators.converters.AbelianGrouper.group_subops#qiskit.aqua.operators.converters.AbelianGrouper.group_subops "qiskit.aqua.operators.converters.AbelianGrouper.group_subops") | Given a ListOp, attempt to group into Abelian ListOps of the same type.                                                                                                                                 |
