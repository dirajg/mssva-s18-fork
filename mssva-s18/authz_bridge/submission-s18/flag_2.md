Flag 2 – Return Address Integrity Violation

Invariant
Authorization decisions must return through an intact and verifiable control-flow path to the caller.

Telemetry
User-space observation via syscall/library tracing and review of call/return boundaries in the source.

Observation
Not Observed. There is no runtime evidence that the authorization return value or return path was not altered after function return.

Security Impact
Manipulating return values or return paths can force authorization outcomes while preserving correct output and service stability.

Limitations
User-space tools cannot validate register state, stack integrity, or return-path correctness.
