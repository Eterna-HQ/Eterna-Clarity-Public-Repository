# Fictional example - Backup restore check

**What do you need to restore?** Current customer proposal folder

**Backup source or service:** ExampleCloud nightly backup

**Restore point / version / date:** 2026-09-14 nightly copy

**Safe test location:** Temporary recovery-test folder

**Tested by:** Operations lead

**Test date:** 2026-09-15

### Proof

- Did the restore complete? **Yes**
- Could you open or read the restored information? **Yes**
- Real task: Open the current proposal, confirm the attached pricing sheet is present, and prepare a copy for a customer follow-up.
- Could you complete the task using the restored copy? **No**
- What was missing? The pricing attachment linked from the proposal was not present in the restored folder.
- Next action: Confirm whether linked attachments are included in the backup scope, then repeat the same restore test.

The backup exists, but this specific recovery job is **not yet proven**.
