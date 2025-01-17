<span id="qiskit-pulse-builder-build" />

# qiskit.pulse.builder.build

<span id="undefined" />

`build(backend=None, schedule=None, name=None, default_alignment='left', default_transpiler_settings=None, default_circuit_scheduler_settings=None)`

Create a context manager for launching the imperative pulse builder DSL.

To enter a building context and starting building a pulse program:

```python
from qiskit import execute, pulse
from qiskit.test.mock import FakeOpenPulse2Q

backend = FakeOpenPulse2Q()

d0 = pulse.DriveChannel(0)

with pulse.build() as pulse_prog:
    pulse.play(pulse.Constant(100, 0.5), d0)
```

While the output program `pulse_prog` cannot be executed as we are using a mock backend. If a real backend is being used, executing the program is done with:

```python
qiskit.execute(pulse_prog, backend)
```

**Parameters**

*   **backend** (*Union\[*[*Backend*](qiskit.providers.Backend#qiskit.providers.Backend "qiskit.providers.Backend")*,* [*BaseBackend*](qiskit.providers.BaseBackend#qiskit.providers.BaseBackend "qiskit.providers.BaseBackend")*]*) – A Qiskit backend. If not supplied certain builder functionality will be unavailable.
*   **schedule** (`Optional`\[`Schedule`]) – a *mutable* pulse Schedule in which your pulse program will be built.
*   **name** (`Optional`\[`str`]) – Name of pulse program to be built. Only used if schedule is not `None`.
*   **default\_alignment** (`str`) – Default scheduling alignment for builder. One of `left`, `right`, `sequential` or an alignment contextmanager.
*   **default\_transpiler\_settings** (`Optional`\[`Dict`\[`str`, `Any`]]) – Default settings for the transpiler.
*   **default\_circuit\_scheduler\_settings** (`Optional`\[`Dict`\[`str`, `Any`]]) – Default settings for the circuit to pulse scheduler.

**Return type**

`AbstractContextManager`\[`Schedule`]

**Returns**

A new builder context which has the active builder inititalized.
