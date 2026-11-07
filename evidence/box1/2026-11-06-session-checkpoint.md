# Mystery Box 1 — session checkpoint

Date: 2026-11-06 (America/Los_Angeles)

Requested scope: Q3.3.2, Q3.3.3, Q3.3.4.

## Completed and verified in Scopy

- Opened the existing Scopy compatibility application on the Mac; the Applications copy repeatedly timed out.
- Detected the physical ADALM2000 over USB.
- Connected successfully after an earlier application exit and restart. Scopy displayed **Calibrated Connected**, enabled instrument menus, and a **Disconnect** button.
- Recovered instrument navigation: invoke the target sidebar item's exposed **Raise** action, then press **Space**. Verified that both Signal Generator and Oscilloscope displayed their actual controls. A checkbox highlight alone did not open the panel.
- Read Signal Generator CH1 settings: sine, **1 kHz**, **2 Vpp**, **0 V offset**, **0 degree phase**; Run off.
- Set and read back the oscilloscope timebase: **200 microseconds/division**. Both channel scales displayed **1 V/division**. Scope Run off; CH1 selected, CH2 not yet enabled/verified for acquisition.

These are instrument settings and connection observations, not experimental voltage or phase measurements. The generator was not started during this session.

## Question status

| Question | Status | Still required |
|---|---|---|
| Q3.3.2 | Pending acquisition | Two real scope captures with frequency and amplitude readouts for CH1, CH2, and CH2 minus CH1; cursor delays for input versus box and input versus resistor |
| Q3.3.3 | Pending measured inputs | Voltage amplitudes and signed phase differences from Q3.3.2 |
| Q3.3.4 | Pending measured inputs | Identify R/C/L, calculate the value, back-substitute into the other magnitude/phase equation, and record Box ID |

No completed cursor captures, measured phasors, or inferred component value were produced in this session. Earlier Lab 2/Lab 3 values must not be reused as Mystery Box measurements.

## Resume requirements

Confirm physical wiring and the Mystery Box #1 ID. The intended lab circuit uses a 1 kOhm series resistor, CH2 across the input Vs, CH1 across the unknown component Vz, and the math trace CH2 minus CH1 across the resistor. Physical wiring has not yet been verified in this session.

After wiring verification, enable and acquire both channels, add the math trace, select a useful frequency within 10 Hz to 300 kHz, and collect stable waveforms. The initial 1 kHz setting is only a starting point. For the selected baseline, the worksheet requires the absolute phase between Vs and the resistor voltage to be less than 50 degrees.

For each capture record actual frequency, amplitude convention (peak or peak-to-peak), cursor identities and subtraction order, signed time delay, and screenshot filename. Use peak phasors consistently: peak amplitude = Vpp/2. With delta_t = t(signal rising crossing) - t(input rising crossing), the signal phase relative to input is -360 degrees * delta_t / T. Compute the resistor voltage by complex subtraction, not subtraction of magnitudes.

The original report and previous analytical work remain in their existing repository locations. This checkpoint does not mark the final report or any experimental answer complete.
