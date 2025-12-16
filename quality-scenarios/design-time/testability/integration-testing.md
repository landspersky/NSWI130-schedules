## Supporting Automated Integration Testing

Containers in question:

- Správce rozvrhových lístků
- Správce předmětů

**Stimulus:**
Developers want to implement automated integration tests that simulate end-to-end schedule management workflows.

**Environment:**
Continuous Integration (CI) pipeline.

**Problem:**
The system must support automated integration testing without requiring manual intervention or access to production services.

**Solution:**
- Provide mock or test implementations for external dependencies (e.g., notification service, authentication).
- Allow test configuration to redirect notifications and logs to test sinks.
- Ensure test data can be easily set up and torn down between test runs.
