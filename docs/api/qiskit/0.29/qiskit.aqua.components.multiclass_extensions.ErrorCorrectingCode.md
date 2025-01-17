# ErrorCorrectingCode

<span id="undefined" />

`ErrorCorrectingCode(code_size=4)`

Bases: `qiskit.aqua.components.multiclass_extensions.multiclass_extension.MulticlassExtension`

The Error Correcting Code multiclass extension.

Error Correcting Code (ECC) is an ensemble method designed for the multiclass classification problem. As for the other multiclass methods, the task is to decide one label from $k > 2$ possible choices.

|       |           |       |       |       |       |       |
| ----- | --------- | ----- | ----- | ----- | ----- | ----- |
| Class | Code Word |       |       |       |       |       |
|       | $f_0$     | $f_1$ | $f_2$ | $f_3$ | $f_4$ | $f_5$ |
| 1     | 0         | 1     | 0     | 1     | 0     | 1     |
| 2     | 1         | 0     | 0     | 1     | 0     | 0     |
| 3     | 1         | 1     | 1     | 0     | 0     | 0     |

The table above shows a 6-bit ECC for a 3-class problem. Each class is assigned a unique binary string of length 6. The string is also called a **codeword**. For example, class 2 has codeword `100100`. During training, one binary classifier is learned for each column. For example, for the first column, ECC builds a binary classifier to separate $\{2, 3\}$ from $\{1\}$. Thus, 6 binary classifiers are trained in this way. To classify a new data point $\mathbf{x}$, all 6 binary classifiers are evaluated to obtain a 6-bit string. Finally, we choose the class whose bitstring is closest to $\mathbf{x}$’s output string as the predicted label. This implementation of ECC uses the Euclidean distance.

**Parameters**

**code\_size** (`int`) – Size of error correcting code

## Methods

|                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`predict`](qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.predict#qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.predict "qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.predict")                         | Applying multiple estimators for prediction.                                                                                                                                                                                            |
| [`set_estimator`](qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.set_estimator#qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.set_estimator "qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.set_estimator") | Called internally to set `Estimator` and parameters :type estimator\_cls: `Callable`\[\[`List`], `Estimator`] :param estimator\_cls: An `Estimator` class :type params: `Optional`\[`List`] :param params: Parameters for the estimator |
| [`test`](qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.test#qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.test "qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.test")                                     | Testing multiple estimators each for distinguishing a pair of classes.                                                                                                                                                                  |
| [`train`](qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.train#qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.train "qiskit.aqua.components.multiclass_extensions.ErrorCorrectingCode.train")                                 | Training multiple estimators each for distinguishing a pair of classes.                                                                                                                                                                 |
