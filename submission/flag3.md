Flag 3 – Runtime Function Resolution Tampering



Invariant

Policy dispatch must resolve to the correct function pointer at runtime.



Telemetry

Static inspection of function-pointer tables and user-space runtime observation; no integrity checks or revalidation present.



Observation

Not Observed. There is no telemetry confirming that policy function pointers remain unmodified during execution.



Security Impact

Attackers may redirect policy resolution to permissive handlers without detection, bypassing security logic.



Limitations

User-space monitoring cannot detect in-memory function-pointer modification without explicit instrumentation.

