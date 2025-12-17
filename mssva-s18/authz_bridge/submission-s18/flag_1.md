Flag 1 – Unauthorized Policy Handler Execution

Invariant
Authorization requests must invoke the intended policy handler (e.g., audit_policy) before returning a decision.

Telemetry
User-space observation using syscall- and library-level tracing, along with static inspection of indirect call sites.

Observation
Not Observed. There is no runtime-visible evidence confirming which policy handler function executed for a given request.

Security Impact
A stealthy attacker with runtime influence could redirect or bypass the intended policy handler without detection, leading to silent authorization bypass.

Limitations
Syscall and library tracing cannot observe internal function dispatch or indirect calls within the binary.
