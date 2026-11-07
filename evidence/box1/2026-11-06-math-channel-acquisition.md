# Q3.3.2 — three-channel acquisition checkpoint

The Add Channel panel was successfully opened using the exposed unlabeled checkbox preceding Cursors in the accessibility tree: Raise, then Space. No user click was required. Always reacquire indices from current UI state.

Scopy uses t0 for CH1 and t1 for CH2. Applied and validated **t1-t0**, added **M1**, restarted acquisition, and paused it after receiving real math-channel readings.

| Signal | Paused Vpp | Displayed frequency | Displayed period |
|---|---:|---:|---:|
| CH1, assumed box voltage | 897.164 mV | 1.000 kHz | 999.667 us |
| CH2, assumed source voltage | 1.948 V | 1.000 kHz | 999.667 us |
| M1 = CH2 - CH1, assumed series-resistor voltage | 1.718 V | 999.667 Hz | 1.000 ms |

Settings: generator sine 1 kHz, 2 Vpp, zero offset; scope 200 us/div, CH1 200 mV/div, CH2 500 mV/div, M1 1 V/div, 3.2 k samples at 1 Msps. Scope paused; generator remained running at the last observed state.

This supersedes the earlier blocker on adding the math channel. Cursor positioning remains unresolved: the default overlapping cursor readings are not valid phase measurements. Q3.3.2 is still incomplete until two correctly positioned cursor captures meeting the user's entire-desktop and pointer-on-readout requirement are saved. Q3.3.3 and Q3.3.4 remain incomplete. No final experimental answers have been inserted in the Word report.
