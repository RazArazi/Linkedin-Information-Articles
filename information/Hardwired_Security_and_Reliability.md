# Hardwired Security and Reliability

**Status:** Architectural control model; no external security certification or production-scale reliability result is asserted.

## Separate controls
Three boundaries must remain distinct:
- **Registration** connects an implemented operation to a Hardwired statement.
- **Publication** selects which registered operations an external caller or AI may see and request.
- **Authorization and approval** determine whether an operation may execute for a particular user, context, or request.

A registered internal statement is not automatically public. Internal statements may implement an exposed operation without becoming directly selectable by an AI.

## Workflow validation
Before execution, the complete requested workflow should be checked against the exposed capability surface, parameters, constraints, and approval requirements. If a required capability is unavailable, the workflow is rejected before any step begins. This does not prevent later runtime failures caused by application or external conditions.

## Software responsibility
Native application code retains responsibility for security enforcement, validation, state, transactions, rollback or compensation where applicable, retries, resource management, and failure recovery. Hardwired returns status and trace information; it does not replace these controls.

Consequential or regulated actions require confirmation under the application's approval policy. AI interpretation is not authorization.

## Evidence limits
The architecture describes intended boundaries. It is not a claim of independent security audit, regulatory compliance, fault tolerance at scale, or measured reliability. Those require separate implementation inspection and evidence.

## Related subjects
[Hardwired Internals and Implementation](Hardwired%20Internals%20and%20Implementation.markdown) · [Hardwired Software Architecture](Hardwired%20Software%20Architecture.markdown) · [Hardwired Software–AI Bridge](Hardwired%20Software%E2%80%93AI%20Bridge.markdown) · [Hardwired Technical Challenges and Open Questions](Hardwired%20Technical%20Challenges%20and%20Open%20Questions.markdown)

## Sources
Foundation: Hardwired Security and Reliability. Canonical: 02_HARDWIRED_ARCHITECTURE.md, 05_EVIDENCE_SURFACE.md, and 13_Hardwired_Software_AI_Bridge_Source_of_Truth.md.
