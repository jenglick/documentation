# qiskit.opflow\.gradients.QFIBase

<span id="undefined" />

`QFIBase(qfi_method='lin_comb_full')`

Base class for Quantum Fisher Information (QFI).

Compute the Quantum Fisher Information (QFI) given a pure, parameterized quantum state.

The QFI is:

> \[QFI]kl= Re\[〈∂kψ|∂lψ〉−〈∂kψ|ψ〉〈ψ|∂lψ〉] \* 4.

**Parameters**

**qfi\_method** (`Union`\[`str`, `CircuitQFI`]) – The method used to compute the state/probability gradient. Can be either a [`CircuitQFI`](qiskit.opflow.gradients.CircuitQFI#qiskit.opflow.gradients.CircuitQFI "qiskit.opflow.gradients.CircuitQFI") instance or one of the following pre-defined strings `'lin_comb_full'`, `` 'overlap_diag'` `` or `` 'overlap_block_diag'` ``.

**Raises**

**ValueError** – if `qfi_method` is neither a `CircuitQFI` object nor one of the predefined strings.

<span id="undefined" />

`__init__(qfi_method='lin_comb_full')`

**Parameters**

**qfi\_method** (`Union`\[`str`, `CircuitQFI`]) – The method used to compute the state/probability gradient. Can be either a [`CircuitQFI`](qiskit.opflow.gradients.CircuitQFI#qiskit.opflow.gradients.CircuitQFI "qiskit.opflow.gradients.CircuitQFI") instance or one of the following pre-defined strings `'lin_comb_full'`, `` 'overlap_diag'` `` or `` 'overlap_block_diag'` ``.

**Raises**

**ValueError** – if `qfi_method` is neither a `CircuitQFI` object nor one of the predefined strings.

## Methods

|                                                                                                                                                                           |                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.opflow.gradients.QFIBase.__init__ "qiskit.opflow.gradients.QFIBase.__init__")(\[qfi\_method])                                                        | **type qfi\_method**`Union`\[`str`, `CircuitQFI`]                                                          |
| [`convert`](#qiskit.opflow.gradients.QFIBase.convert "qiskit.opflow.gradients.QFIBase.convert")(operator\[, params])                                                      | **type operator**`OperatorBase`                                                                            |
| [`gradient_wrapper`](#qiskit.opflow.gradients.QFIBase.gradient_wrapper "qiskit.opflow.gradients.QFIBase.gradient_wrapper")(operator, bind\_params\[, …])                  | Get a callable function which provides the respective gradient, Hessian or QFI for given parameter values. |
| [`parameter_expression_grad`](#qiskit.opflow.gradients.QFIBase.parameter_expression_grad "qiskit.opflow.gradients.QFIBase.parameter_expression_grad")(param\_expr, param) | Get the derivative of a parameter expression w\.r.t.                                                       |

## Attributes

|                                                                                                          |                       |
| -------------------------------------------------------------------------------------------------------- | --------------------- |
| [`qfi_method`](#qiskit.opflow.gradients.QFIBase.qfi_method "qiskit.opflow.gradients.QFIBase.qfi_method") | Returns `CircuitQFI`. |

<span id="undefined" />

`abstract convert(operator, params=None)`

**Parameters**

*   **operator** (`OperatorBase`) – The operator we are taking the gradient, Hessian or QFI of
*   **params** (`Union`\[`ParameterVector`, `ParameterExpression`, `List`\[`ParameterExpression`], `None`]) – The parameters we are taking the gradient, Hessian or QFI with respect to.

**Return type**

`OperatorBase`

**Returns**

An operator whose evaluation yields the gradient, Hessian or QFI.

**Raises**

**ValueError** – If `params` contains a parameter not present in `operator`.

<span id="undefined" />

`gradient_wrapper(operator, bind_params, grad_params=None, backend=None, expectation=None)`

Get a callable function which provides the respective gradient, Hessian or QFI for given parameter values. This callable can be used as gradient function for optimizers.

**Parameters**

*   **operator** (`OperatorBase`) – The operator for which we want to get the gradient, Hessian or QFI.
*   **bind\_params** (`Union`\[`ParameterExpression`, `ParameterVector`, `List`\[`ParameterExpression`]]) – The operator parameters to which the parameter values are assigned.
*   **grad\_params** (`Union`\[`ParameterExpression`, `ParameterVector`, `List`\[`ParameterExpression`], `Tuple`\[`ParameterExpression`, `ParameterExpression`], `List`\[`Tuple`\[`ParameterExpression`, `ParameterExpression`]], `None`]) – The parameters with respect to which we are taking the gradient, Hessian or QFI. If grad\_params = None, then grad\_params = bind\_params
*   **backend** (`Union`\[`Backend`, `BaseBackend`, `QuantumInstance`, `None`]) – The quantum backend or QuantumInstance to use to evaluate the gradient, Hessian or QFI.
*   **expectation** (`Optional`\[`ExpectationBase`]) – The expectation converter to be used. If none is set then PauliExpectation() is used.

**Return type**

`Callable`\[\[`Iterable`], `ndarray`]

**Returns**

Function to compute a gradient, Hessian or QFI. The function takes an iterable as argument which holds the parameter values.

<span id="undefined" />

`static parameter_expression_grad(param_expr, param)`

Get the derivative of a parameter expression w\.r.t. the given parameter.

**Parameters**

*   **param\_expr** (`ParameterExpression`) – The Parameter Expression for which we compute the derivative
*   **param** (`ParameterExpression`) – Parameter w\.r.t. which we want to take the derivative

**Return type**

`Union`\[`ParameterExpression`, `float`]

**Returns**

ParameterExpression representing the gradient of param\_expr w\.r.t. param

<span id="undefined" />

`property qfi_method`

Returns `CircuitQFI`.

**Return type**

`CircuitQFI`

**Returns**

`CircuitQFI`.
