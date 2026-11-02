# Windows 11 and Intune deployment notes

**Stage: planning.** This repository contains a proposed pilot and change-record template. It does not contain a deployed Intune configuration or a completed rollout.

## The question

How would I pilot an endpoint change with clear prerequisites, a small scope, observable acceptance checks, and a recovery path?

## Documents

- [Pilot plan](docs/pilot-plan.md): identity/enrollment prerequisites, configuration intent, application checks, update behavior, and recovery limits.
- [Change record](templates/change-record.md): baseline, assignments, execution, verification, and recovery outcome.
- [Evidence index](evidence/README.md): where sanitized results will go after execution.

## Work still needed

1. Confirm an authorized test tenant, suitable licensing, and an owned/disposable test device.
2. Record the exact Windows build and chosen join/enrollment method.
3. Review current Microsoft requirements before making assignments.
4. Apply one harmless pilot change and record its actual outcome.
5. Verify ordinary sign-in and user tasks, then test the documented recovery procedure.

Removing a policy assignment does not necessarily reverse its settings. Wipe, retire, and delete are different actions; none is a generic rollback. The pilot plan requires choosing a recovery method before execution.

There are no tenant exports, device identifiers, recovery keys, licensed images, or scripts applying policies here. The value at this stage is the written plan; execution evidence is pending.

[MIT license](LICENSE) · [Security](SECURITY.md)
