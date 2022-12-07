# ECU KWP UDS Debugger
This is just an experiment (For now)

## Why?
With mainstream ECUs found in almost all modern vehicles, there exists diagnostic specifications (UDS, and KWP for older vehicles).

Both specifications are designed to allow for querying an ECU once it has been released, and only really supports basic data querying compared to what is avaliable on the processor for more in-depth execution debugging.

Therefore, this is a purely experimental idea. Build a data query PID for both KWP and UDS which allows for remote debugging of an ECU, querying classes and memory in realtime, and setting values in memory manually, almost like a debugger.

## Why not just use a JTAG debugger?
JTAG debugging is good for bench testing ECUs, however once an ECU is put into a moving vehicle, there is no way to query it using JTAG, not to mention as JTAG halts the CPU execution, the ECU would be frozen, which would result in undefined behaviour once the CPU resumes execution.

Therefore, this specification is designed to allow for an ECU to be queryed and debugged in the background.
