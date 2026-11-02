# Windows 11 / Intune pilot design

Status: planned lab. Do not treat these notes as tenant configuration exports.

## Prerequisites

Record the target Windows edition/build, hardware support, identity model, tenant
licensing, enrollment rights, network requirements, recovery keys, and device owner.
Confirm current Microsoft requirements before a real deployment.

## Configuration intent

| Area | Design intent | Evidence required |
| --- | --- | --- |
| Enrollment | Use a small assigned lab pilot group | Enrollment status and management channel |
| Identity | Choose Entra join or hybrid join explicitly | Join state; no tenant IDs in public output |
| Updates | Stage a pilot before broad rollout | Policy assignment and observed update behavior |
| Encryption | Follow approved BitLocker/recovery-key process | Encryption state; never publish recovery keys |
| Applications | Deploy one harmless test app | Detection rule, install/uninstall result |
| Compliance | Define requirements separately from configuration | Policy evaluation and access implications |

## Pilot entry and exit

Entry: disposable lab device, authorized account, backup/recovery plan, baseline notes.
Exit: enrollment works; intended policies arrive; test app installs/uninstalls; normal
sign-in and required workflows still work; recovery procedure is documented and tested.

## Recovery

Record policy/application rollback options and their limitations before applying.
Removing an assignment does not necessarily reverse every setting. Wipe/retire/delete
actions have different effects: never use them as generic rollback. Protect data first.

## Imaging versus modern provisioning

Keep traditional imaging notes separate from Autopilot/MDM design. Record the chosen
method, prerequisites, version, maintenance burden, and how a failed deployment is recovered.
Do not redistribute licensed Windows images, product keys, or vendor packages here.
