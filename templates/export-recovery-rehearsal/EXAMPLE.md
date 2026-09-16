# A fictional rehearsal that found a real gap in the example

This example is invented. It is not a customer story or a claim about any actual software product.

A community club is changing where it keeps its equipment notes. The test task is: **the replacement coordinator must find the packing instructions and photo, then prepare the next equipment handoff without opening the old workspace.** The selected export includes notes and tasks. The original workspace is retained.

The exported packing note opens in the new folder. That is a useful result, but the photo is only a link back to the old service. A task also points to the old note rather than the new copy. When the coordinator tests their own access, they can read the note but not the photo. The due-back filter and a recurring reminder have not yet been tested. A known archived checklist is outside the selected export.

| Check | Recorded outcome | Next action |
| --- | --- | --- |
| Packing note | Pass: the reviewer opened and read the local file. | Retain the dated evidence of this sample. |
| Attached photo | Fail: it cannot be opened without the original service. | Obtain the actual file through the authorised source, then retest. |
| Task-to-note reference | Fail: it leads back to the old workspace. | Add the correct destination reference and test it. |
| Earlier comments | Not applicable: only the current note is needed for this particular task; history is retained separately. | Do not describe history as recovered. |
| Due-back filter | Not tested. | Check the destination view with a known due item. |
| Reminder | Not tested. | Recreate and test an approved reminder using a harmless test case. |
| Receiver access | Fail: the coordinator cannot open the photo. | Correct the appropriate permission, not share a password. |
| Archived checklist | Fail: the known item is absent from the selected export. | Resolve the export scope. |
| Next action | Fail: preparing the equipment stops at the missing photo. | Repeat the task after the information and access gaps are resolved. |

The conclusion is not "the migration passed because the ZIP downloaded." It is: **the selected note is readable, while this task still depends on missing files, references and access.** The example deliberately does not give an overall score or permission to delete the old workspace.

The workbook's Example sheet records these same observations. The Checks sheet remains blank for your own work.
