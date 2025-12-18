Flag 4 – Non-Linear Control Transfer Abuse



Invariant

Execution flow must follow expected call/return semantics for security-critical logic.



Telemetry

User-space execution tracing and source inspection of setjmp/longjmp usage.



Observation

Not Observed. Non-linear control transfers occur without any runtime telemetry indicating skipped execution paths.



Security Impact

Abusing non-linear jumps can bypass authorization logic invisibly while keeping the service operational.



Limitations

User-space tools cannot reconstruct skipped stack frames or detect longjmp-induced path changes.

