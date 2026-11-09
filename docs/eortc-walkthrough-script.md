# EORTC walkthrough (AitriumOS 2.3.4): screen-recording script

Internal working file (not published: `docs/` is in `.mintignore`).

**Purpose:** replaces the walkthrough embedded at the top of `aitrium-os/no-protocol-submissions.mdx` (the "Basic Data Submission guide and walkthrough" named in the EORTC training statement). Swap the embed where the `EORTC WALKTHROUGH PLACEHOLDER` comment sits once the new video exists.

**Length:** 3–5 minutes. **Format:** 1440×900 app window, light mode, captions on (the narration lines double as captions).

**Setup (same data as the screenshot shot list, Pass 1):**
- AitriumOS 2.3.4 on the Mac app, Demo site account, **EORTC-style sandbox trial**.
- Synthetic patient `E2E-EORTC-010` (not yet added). Folder `E2E-EORTC-010_typeA/` with CT + RTSTRUCT + RTPLAN + RTDOSE and one de-identified PDF (`surgical-report.pdf`) for a dataset type that names a supporting document. The type has instructions text set.
- No real patient data, real site names, or hospital paths on screen. Close other apps and notifications.

| # | Scene (approx. time) | What to do on screen | Narration / caption |
|---|---|---|---|
| 1 | Intro (0:00–0:15) | Trial page open, cursor still. | "This walkthrough shows how to submit one patient's dataset to an EORTC trial with AitriumOS 2.3." |
| 2 | Add a patient (0:15–0:40) | Type `E2E-EORTC-010` in **Search or add ID** → **Add patient** → **Save**. The row appears. | "Type the Trial Patient ID exactly as the trial assigned it, then add the patient. Never use a medical record number." |
| 3 | Start the submission (0:40–1:00) | In the new row, select **Submit Dataset** under the dataset type → **Select Directory** → pick the folder. Let **Getting ready** show. | "Choose the dataset type, then the folder that holds this patient's export. AitriumOS first checks disk space and the connection." |
| 4 | Check the dataset (1:00–1:40) | Results load on **Studies**. Hover the statement "Everything … requires is in this folder." Point at the study names and **What … requires**. | "AitriumOS compares the folder with what the dataset type requires and sums it up in one sentence. Studies are named by what they hold." |
| 5 | Supporting documents (1:40–2:05) | Scroll to **Supporting documents** → **Choose a file** → pick the PDF → tick **These documents contain no patient identifiers.** | "Choose the file for each document the trial asks for. AitriumOS sends documents exactly as they are, so remove patient information first." |
| 6 | Before you continue (2:05–2:30) | Select **Standardize RT Structures** → **Before you continue** → tick the burned-in pixel acknowledgment → **Continue**. | "Missing items never stop you. Confirm that you'll check images for burned-in patient information. Nothing is sent yet." |
| 7 | Standardize (2:30–2:55) | Show the suggestions; select the rows to rename → **Apply Changes**. | "Check the suggested structure names, select the ones to rename, and apply." |
| 8 | De-identify (2:55–3:10) | Let de-identification run; header shows **De-identify**. | "AitriumOS de-identifies the DICOM metadata with the trial's policy and checks the result." |
| 9 | Review and send (3:10–3:35) | **Confirm Data Transfer** → scroll the summary → **Confirm and Transfer**. Show **Data Transfer** then **Aitrium Sync**. | "Review what will be sent, then confirm. Keep AitriumOS open until the submission is complete." |
| 10 | Submission complete (3:35–4:00) | **Submission complete**: point at **What happens next** and **Instructions from {organization}**. | "When Submission complete appears, the trial team can see the dataset. Follow any instructions from the trial team." |
| 11 | Check and send a new version (4:00–4:30) | Close the flow. Point at the **Sent** cell and **Last Sent**. Select the cell → show the dialog and **Send a new version** (don't send). | "Back on the trial page, the dataset reads Sent. To correct it later, open it and send a new version. Don't add the patient again." |
| 12 | Close (4:30–4:40) | Cursor still on the trial page. | "For help, see the Troubleshooting page or contact support@aitriumos.com." |

**Don't show:** multi-patient submission, Data Tools, anything from a protocol (RTQA) trial, or any real data.
