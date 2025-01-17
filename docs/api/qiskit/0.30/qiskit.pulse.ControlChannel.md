# ControlChannel

<span id="undefined" />

`ControlChannel(index)`

Bases: `qiskit.pulse.channels.PulseChannel`

Control channels provide supplementary control over the qubit to the drive channel. These are often associated with multi-qubit gate operations. They may not map trivially to a particular qubit index.

Channel class.

**Parameters**

**index** (`int`) – Index of channel.

## Methods

|                                                                                                                                                                |                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| [`assign`](qiskit.pulse.ControlChannel.assign#qiskit.pulse.ControlChannel.assign "qiskit.pulse.ControlChannel.assign")                                         | Return a new channel with the input Parameter assigned to value. |
| [`is_parameterized`](qiskit.pulse.ControlChannel.is_parameterized#qiskit.pulse.ControlChannel.is_parameterized "qiskit.pulse.ControlChannel.is_parameterized") | Return True iff the channel is parameterized.                    |

## Attributes

<span id="undefined" />

### index

Return the index of this channel. The index is a label for a control signal line typically mapped trivially to a qubit index. For instance, `DriveChannel(0)` labels the signal line driving the qubit labeled with index 0.

**Return type**

`Union`\[`int`, `ParameterExpression`]

<span id="undefined" />

### name

Return the shorthand alias for this channel, which is based on its type and index.

**Return type**

`str`

<span id="undefined" />

### parameters

Parameters which determine the channel index.

**Return type**

`Set`

<span id="undefined" />

### prefix

`= 'u'`
