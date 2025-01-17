<span id="qiskit-chemistry-algorithms-minimumeigensolverfactory" />

# qiskit.chemistry.algorithms.MinimumEigensolverFactory

<span id="undefined" />

`MinimumEigensolverFactory`

A factory to construct a minimum eigensolver based on a qubit operator transformation.

<span id="undefined" />

`__init__()`

Initialize self. See help(type(self)) for accurate signature.

## Methods

|                                                                                                                                                                                            |                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.chemistry.algorithms.MinimumEigensolverFactory.__init__ "qiskit.chemistry.algorithms.MinimumEigensolverFactory.__init__")()                                           | Initialize self.                                                                        |
| [`get_solver`](#qiskit.chemistry.algorithms.MinimumEigensolverFactory.get_solver "qiskit.chemistry.algorithms.MinimumEigensolverFactory.get_solver")(transformation)                       | Returns a minimum eigensolver, based on the qubit operator transformation.              |
| [`supports_aux_operators`](#qiskit.chemistry.algorithms.MinimumEigensolverFactory.supports_aux_operators "qiskit.chemistry.algorithms.MinimumEigensolverFactory.supports_aux_operators")() | Returns whether the eigensolver generated by this factory supports auxiliary operators. |

<span id="undefined" />

`abstract get_solver(transformation)`

Returns a minimum eigensolver, based on the qubit operator transformation.

**Parameters**

**transformation** (`Transformation`) – The qubit operator transformation.

**Return type**

`MinimumEigensolver`

**Returns**

A minimum eigensolver suitable to compute the ground state of the molecule transformed by `transformation`.

<span id="undefined" />

`abstract supports_aux_operators()`

Returns whether the eigensolver generated by this factory supports auxiliary operators.

**Return type**

`bool`
