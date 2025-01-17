# qiskit.pulse.Acquire

<span id="undefined" />

`Acquire(duration, channel, mem_slot=None, reg_slot=None, kernel=None, discriminator=None, name=None)`

The Acquire instruction is used to trigger the ADC associated with a particular qubit; e.g. instantiated with AcquireChannel(0), the Acquire command will trigger data collection for the channel associated with qubit 0 readout. This instruction also provides acquisition metadata:

> *   the number of cycles during which to acquire (in terms of dt),
> *   the register slot to store classified, intermediary readout results,
> *   the memory slot to return classified results,
> *   the kernel to integrate raw data for each shot, and
> *   the discriminator to classify kerneled IQ points.

Create a new Acquire instruction.

**Parameters**

*   **duration** (`Union`\[`int`, `ParameterExpression`]) – Length of time to acquire data in terms of dt.
*   **channel** ([`AcquireChannel`](qiskit.pulse.channels#qiskit.pulse.channels.AcquireChannel "qiskit.pulse.channels.AcquireChannel")) – The channel that will acquire data.
*   **mem\_slot** (`Optional`\[[`MemorySlot`](qiskit.pulse.channels#qiskit.pulse.channels.MemorySlot "qiskit.pulse.channels.MemorySlot")]) – The classical memory slot in which to store the classified readout result.
*   **reg\_slot** (`Optional`\[[`RegisterSlot`](qiskit.pulse.channels#qiskit.pulse.channels.RegisterSlot "qiskit.pulse.channels.RegisterSlot")]) – The fast-access register slot in which to store the classified readout result for fast feedback.
*   **kernel** (`Optional`\[`Kernel`]) – A `Kernel` for integrating raw data.
*   **discriminator** (`Optional`\[`Discriminator`]) – A `Discriminator` for discriminating kerneled IQ data into 0/1 results.
*   **name** (`Optional`\[`str`]) – Name of the instruction for display purposes.

**Raises**

[**PulseError**](qiskit.pulse.PulseError#qiskit.pulse.PulseError "qiskit.pulse.PulseError") – If channels are supplied, and the number of register and/or memory slots does not equal the number of channels.

<span id="undefined" />

`__init__(duration, channel, mem_slot=None, reg_slot=None, kernel=None, discriminator=None, name=None)`

Create a new Acquire instruction.

**Parameters**

*   **duration** (`Union`\[`int`, `ParameterExpression`]) – Length of time to acquire data in terms of dt.
*   **channel** ([`AcquireChannel`](qiskit.pulse.channels#qiskit.pulse.channels.AcquireChannel "qiskit.pulse.channels.AcquireChannel")) – The channel that will acquire data.
*   **mem\_slot** (`Optional`\[[`MemorySlot`](qiskit.pulse.channels#qiskit.pulse.channels.MemorySlot "qiskit.pulse.channels.MemorySlot")]) – The classical memory slot in which to store the classified readout result.
*   **reg\_slot** (`Optional`\[[`RegisterSlot`](qiskit.pulse.channels#qiskit.pulse.channels.RegisterSlot "qiskit.pulse.channels.RegisterSlot")]) – The fast-access register slot in which to store the classified readout result for fast feedback.
*   **kernel** (`Optional`\[`Kernel`]) – A `Kernel` for integrating raw data.
*   **discriminator** (`Optional`\[`Discriminator`]) – A `Discriminator` for discriminating kerneled IQ data into 0/1 results.
*   **name** (`Optional`\[`str`]) – Name of the instruction for display purposes.

**Raises**

[**PulseError**](qiskit.pulse.PulseError#qiskit.pulse.PulseError "qiskit.pulse.PulseError") – If channels are supplied, and the number of register and/or memory slots does not equal the number of channels.

## Methods

|                                                                                                                      |                                                                                                                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.pulse.Acquire.__init__ "qiskit.pulse.Acquire.__init__")(duration, channel\[, mem\_slot, …])     | Create a new Acquire instruction.                                                                                                                                                                   |
| [`append`](#qiskit.pulse.Acquire.append "qiskit.pulse.Acquire.append")(schedule\[, name])                            | Return a new [`Schedule`](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted at the maximum time over all channels shared between `self` and `schedule`. |
| [`assign_parameters`](#qiskit.pulse.Acquire.assign_parameters "qiskit.pulse.Acquire.assign_parameters")(value\_dict) | Modify and return self with parameters assigned according to the input.                                                                                                                             |
| [`ch_duration`](#qiskit.pulse.Acquire.ch_duration "qiskit.pulse.Acquire.ch_duration")(\*channels)                    | Return duration of the supplied channels in this Instruction.                                                                                                                                       |
| [`ch_start_time`](#qiskit.pulse.Acquire.ch_start_time "qiskit.pulse.Acquire.ch_start_time")(\*channels)              | Return minimum start time for supplied channels.                                                                                                                                                    |
| [`ch_stop_time`](#qiskit.pulse.Acquire.ch_stop_time "qiskit.pulse.Acquire.ch_stop_time")(\*channels)                 | Return maximum start time for supplied channels.                                                                                                                                                    |
| [`draw`](#qiskit.pulse.Acquire.draw "qiskit.pulse.Acquire.draw")(\[dt, style, filename, interp\_method, …])          | Plot the instruction.                                                                                                                                                                               |
| [`flatten`](#qiskit.pulse.Acquire.flatten "qiskit.pulse.Acquire.flatten")()                                          | Return itself as already single instruction.                                                                                                                                                        |
| [`insert`](#qiskit.pulse.Acquire.insert "qiskit.pulse.Acquire.insert")(start\_time, schedule\[, name])               | Return a new [`Schedule`](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted within `self` at `start_time`.                                              |
| [`is_parameterized`](#qiskit.pulse.Acquire.is_parameterized "qiskit.pulse.Acquire.is_parameterized")()               | Return True iff the instruction is parameterized.                                                                                                                                                   |
| [`shift`](#qiskit.pulse.Acquire.shift "qiskit.pulse.Acquire.shift")(time\[, name])                                   | Return a new schedule shifted forward by time.                                                                                                                                                      |

## Attributes

|                                                                                             |                                                                                                                                                    |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`acquire`](#qiskit.pulse.Acquire.acquire "qiskit.pulse.Acquire.acquire")                   | Acquire channel to acquire data.                                                                                                                   |
| [`channel`](#qiskit.pulse.Acquire.channel "qiskit.pulse.Acquire.channel")                   | Return the [`Channel`](qiskit.pulse.channels#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel") that this instruction is scheduled on. |
| [`channels`](#qiskit.pulse.Acquire.channels "qiskit.pulse.Acquire.channels")                | Returns the channels that this schedule uses.                                                                                                      |
| [`discriminator`](#qiskit.pulse.Acquire.discriminator "qiskit.pulse.Acquire.discriminator") | Return discrimination settings.                                                                                                                    |
| [`duration`](#qiskit.pulse.Acquire.duration "qiskit.pulse.Acquire.duration")                | Duration of this instruction.                                                                                                                      |
| [`id`](#qiskit.pulse.Acquire.id "qiskit.pulse.Acquire.id")                                  | Unique identifier for this instruction.                                                                                                            |
| [`instructions`](#qiskit.pulse.Acquire.instructions "qiskit.pulse.Acquire.instructions")    | Iterable for getting instructions from Schedule tree.                                                                                              |
| [`kernel`](#qiskit.pulse.Acquire.kernel "qiskit.pulse.Acquire.kernel")                      | Return kernel settings.                                                                                                                            |
| [`mem_slot`](#qiskit.pulse.Acquire.mem_slot "qiskit.pulse.Acquire.mem_slot")                | The classical memory slot which will store the classified readout result.                                                                          |
| [`name`](#qiskit.pulse.Acquire.name "qiskit.pulse.Acquire.name")                            | Name of this instruction.                                                                                                                          |
| [`operands`](#qiskit.pulse.Acquire.operands "qiskit.pulse.Acquire.operands")                | Return instruction operands.                                                                                                                       |
| [`parameters`](#qiskit.pulse.Acquire.parameters "qiskit.pulse.Acquire.parameters")          | Parameters which determine the instruction behavior.                                                                                               |
| [`reg_slot`](#qiskit.pulse.Acquire.reg_slot "qiskit.pulse.Acquire.reg_slot")                | The fast-access register slot which will store the classified readout result for fast-feedback computation.                                        |
| [`start_time`](#qiskit.pulse.Acquire.start_time "qiskit.pulse.Acquire.start_time")          | Relative begin time of this instruction.                                                                                                           |
| [`stop_time`](#qiskit.pulse.Acquire.stop_time "qiskit.pulse.Acquire.stop_time")             | Relative end time of this instruction.                                                                                                             |

<span id="undefined" />

`property acquire`

Acquire channel to acquire data. The `AcquireChannel` index maps trivially to qubit index.

**Return type**

[`AcquireChannel`](qiskit.pulse.channels#qiskit.pulse.channels.AcquireChannel "qiskit.pulse.channels.AcquireChannel")

<span id="undefined" />

`append(schedule, name=None)`

Return a new [`Schedule`](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted at the maximum time over all channels shared between `self` and `schedule`.

**Parameters**

*   **schedule** (*Union\['Schedule', 'Instruction']*) – Schedule or instruction to be appended
*   **name** (`Optional`\[`str`]) – Name of the new schedule. Defaults to name of self

**Returns**

A new schedule with `schedule` a this instruction at t=0.

**Return type**

[Schedule](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule")

<span id="undefined" />

`assign_parameters(value_dict)`

Modify and return self with parameters assigned according to the input.

**Parameters**

**value\_dict** (`Dict`\[`ParameterExpression`, `Union`\[`ParameterExpression`, `float`]]) – A mapping from Parameters to either numeric values or another Parameter expression.

**Return type**

`Instruction`

**Returns**

Self with updated parameters.

<span id="undefined" />

`ch_duration(*channels)`

Return duration of the supplied channels in this Instruction.

**Parameters**

**\*channels** – Supplied channels

**Return type**

`int`

<span id="undefined" />

`ch_start_time(*channels)`

Return minimum start time for supplied channels.

**Parameters**

**\*channels** – Supplied channels

**Return type**

`int`

<span id="undefined" />

`ch_stop_time(*channels)`

Return maximum start time for supplied channels.

**Parameters**

**\*channels** – Supplied channels

**Return type**

`int`

<span id="undefined" />

`property channel`

Return the [`Channel`](qiskit.pulse.channels#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel") that this instruction is scheduled on.

**Return type**

[`AcquireChannel`](qiskit.pulse.channels#qiskit.pulse.channels.AcquireChannel "qiskit.pulse.channels.AcquireChannel")

<span id="undefined" />

`property channels`

Returns the channels that this schedule uses.

**Return type**

`Tuple`\[`Union`\[[`AcquireChannel`](qiskit.pulse.channels#qiskit.pulse.channels.AcquireChannel "qiskit.pulse.channels.AcquireChannel"), [`MemorySlot`](qiskit.pulse.channels#qiskit.pulse.channels.MemorySlot "qiskit.pulse.channels.MemorySlot"), [`RegisterSlot`](qiskit.pulse.channels#qiskit.pulse.channels.RegisterSlot "qiskit.pulse.channels.RegisterSlot")]]

<span id="undefined" />

`property discriminator`

Return discrimination settings.

**Return type**

`Discriminator`

<span id="undefined" />

`draw(dt=1, style=None, filename=None, interp_method=None, scale=1, plot_all=False, plot_range=None, interactive=False, table=True, label=False, framechange=True, channels=None)`

Plot the instruction.

**Parameters**

*   **dt** (`float`) – Time interval of samples
*   **style** (*Optional\[SchedStyle]*) – A style sheet to configure plot appearance
*   **filename** (`Optional`\[`str`]) – Name required to save pulse image
*   **interp\_method** (`Optional`\[`Callable`]) – A function for interpolation
*   **scale** (`float`) – Relative visual scaling of waveform amplitudes
*   **plot\_all** (`bool`) – Plot empty channels
*   **plot\_range** (`Optional`\[`Tuple`\[`float`]]) – A tuple of time range to plot
*   **interactive** (`bool`) – When set true show the circuit in a new window (this depends on the matplotlib backend being used supporting this)
*   **table** (`bool`) – Draw event table for supported instructions
*   **label** (`bool`) – Label individual instructions
*   **framechange** (`bool`) – Add framechange indicators
*   **channels** (`Optional`\[`List`\[[`Channel`](qiskit.pulse.channels#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel")]]) – A list of channel names to plot

**Returns**

A matplotlib figure object of the pulse schedule

**Return type**

matplotlib.figure

<span id="undefined" />

`property duration`

Duration of this instruction.

**Return type**

`Union`\[`int`, `ParameterExpression`]

<span id="undefined" />

`flatten()`

Return itself as already single instruction.

**Return type**

`Instruction`

<span id="undefined" />

`property id`

Unique identifier for this instruction.

**Return type**

`int`

<span id="undefined" />

`insert(start_time, schedule, name=None)`

Return a new [`Schedule`](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted within `self` at `start_time`.

**Parameters**

*   **start\_time** (`int`) – Time to insert the schedule schedule
*   **schedule** (*Union\['Schedule', 'Instruction']*) – Schedule or instruction to insert
*   **name** (`Optional`\[`str`]) – Name of the new schedule. Defaults to name of self

**Returns**

A new schedule with `schedule` inserted with this instruction at t=0.

**Return type**

[Schedule](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule")

<span id="undefined" />

`property instructions`

Iterable for getting instructions from Schedule tree.

**Return type**

`Tuple`\[`Tuple`\[`int`, `Instruction`]]

<span id="undefined" />

`is_parameterized()`

Return True iff the instruction is parameterized.

**Return type**

`bool`

<span id="undefined" />

`property kernel`

Return kernel settings.

**Return type**

`Kernel`

<span id="undefined" />

`property mem_slot`

The classical memory slot which will store the classified readout result.

**Return type**

[`MemorySlot`](qiskit.pulse.channels#qiskit.pulse.channels.MemorySlot "qiskit.pulse.channels.MemorySlot")

<span id="undefined" />

`property name`

Name of this instruction.

**Return type**

`str`

<span id="undefined" />

`property operands`

Return instruction operands.

**Return type**

`Tuple`

<span id="undefined" />

`property parameters`

Parameters which determine the instruction behavior.

**Return type**

`Set`

<span id="undefined" />

`property reg_slot`

The fast-access register slot which will store the classified readout result for fast-feedback computation.

**Return type**

[`RegisterSlot`](qiskit.pulse.channels#qiskit.pulse.channels.RegisterSlot "qiskit.pulse.channels.RegisterSlot")

<span id="undefined" />

`shift(time, name=None)`

Return a new schedule shifted forward by time.

**Parameters**

*   **time** (`int`) – Time to shift by
*   **name** (`Optional`\[`str`]) – Name of the new schedule. Defaults to name of self

**Returns**

The shifted schedule.

**Return type**

[Schedule](qiskit.pulse.Schedule#qiskit.pulse.Schedule "qiskit.pulse.Schedule")

<span id="undefined" />

`property start_time`

Relative begin time of this instruction.

**Return type**

`int`

<span id="undefined" />

`property stop_time`

Relative end time of this instruction.

**Return type**

`int`
