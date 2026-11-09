# EORTC walkthrough (AitriumOS 2.3.4): screen-recording script

Internal working file (not published: `docs/` is in `.mintignore`).

**Purpose:** replaces the walkthrough embedded at the top of `aitrium-os/no-protocol-submissions.mdx` (the "Basic Data Submission guide and walkthrough" named in the EORTC training statement). Swap the embed where the `EORTC WALKTHROUGH PLACEHOLDER` comment sits once the new video exists.

**Length:** 3–5 minutes. **Format:** 1440×900 app window, light mode, captions on (the narration lines double as captions).

**Setup (verified 2026-11-09 against AitriumOS 2.3.4 and prod):**
- AitriumOS 2.3.4 on the Mac, signed in as the docs user at **Example Cancer Center** (Demo Clinical Trial Organization).
- Trial **Example Trial**, dataset type **Prior Radiotherapy**. It has **Instructions** set and names one optional supporting document, **Surgical Reports**.
- Patient **`EX-0003`**: not yet on the trial; the video adds it. Only EX-0001 and EX-0002 exist today.
- Folder **`~/AitriumTest/docs-2.3.4/data/EX-0003/`** (synthetic, 85 files, 3.3 MB):
  - `prior_rt/`: CT, RTSTRUCT, RTPLAN, RTDOSE and REG (60 Gy in 30 fx);
  - `prior_diag/`: MR plus an optional CT;
  - `surgical_report.pdf`, a one-page synthetic PDF.

  Everything Prior Radiotherapy requires is present. The DICOM names Example Cancer Center as the institution and the patient as EX^0003.
- Before recording, type `EX-000` in **Search or add ID** so the list shows only EX- patients, not the E2E- test rows.
- No real patient data, real site names or hospital paths on screen. Close other apps and notifications.
- After recording, EX-0003 stays as a Sent example patient (synthetic).

| # | Scene (approx. time) | What to do on screen | Narration / caption |
|---|---|---|---|
| 1 | Intro (0:00–0:15) | Trial page open, cursor still. | "This walkthrough shows how to submit one patient's dataset to an EORTC trial with AitriumOS 2.3." |
| 2 | Add a patient (0:15–0:40) | Type `EX-0003` in **Search or add ID** → **Add patient** → **Save**. The row appears. | "Type the Trial Patient ID exactly as the trial assigned it, then add the patient. Never use a medical record number." |
| 3 | Start the submission (0:40–1:00) | In the EX-0003 row, select **Submit Dataset** under **Prior Radiotherapy** → **Select Directory** → pick `EX-0003`. | "Choose the dataset type, then the folder that holds this patient's export." |
| 4 | Check the dataset (1:00–1:40) | Results load. Point at **Studies in this folder** (CT and MR study, Radiotherapy study), then **What Prior Radiotherapy requires**: both cards read **Complete**. | "AitriumOS compares the folder with what the dataset type requires. Studies are named by what they hold, and each requirement shows whether it's complete." |
| 5 | Supporting documents (1:40–2:05) | Scroll to **Supporting documents** ("1 document file in this folder") → **Choose a file** → `surgical_report.pdf` → select **These documents contain no patient identifiers.** | "Choose the file for each document the trial asks for. AitriumOS sends documents exactly as they are, so remove patient information first." |
| 6 | Before you continue (2:05–2:30) | Select **Standardize RT Structures** → **Before you continue** → select the burned-in pixel acknowledgment → **Continue**. | "Missing items never stop you. Confirm that you'll check images for burned-in patient information. Nothing is sent yet." |
| 7 | Standardize (2:30–2:55) | Show the suggestions; select the rows to rename → **Apply Changes**. | "Check the suggested structure names, select the ones to rename, and apply." |
| 8 | De-identify (2:55–3:10) | Let de-identification run; header shows **De-identify**. | "AitriumOS de-identifies the DICOM metadata with the trial's policy and checks the result." |
| 9 | Review and send (3:10–3:35) | **Confirm Data Transfer**: point at the one-line summary ("…requires is in this folder.") and scroll the summary → **Confirm and Transfer**. Show **Data Transfer** then **Aitrium Sync**. | "Review what will be sent, then confirm. Keep AitriumOS open until the submission is complete." |
| 10 | Submission complete (3:35–4:00) | **Submission complete**: point at **What happens next** and **Instructions from {organization}**. | "When Submission complete appears, the trial team can see the dataset. Follow any instructions from the trial team." |
| 11 | Check and send a new version (4:00–4:30) | Close the flow. Point at the **Sent** cell and **Last Sent**. Select the cell → show the dialog and **Send a new version** (don't send). | "Back on the trial page, the dataset reads Sent. To correct it later, open it and send a new version. Don't add the patient again." |
| 12 | Close (4:30–4:40) | Cursor still on the trial page. | "For help, see the Troubleshooting page or contact support@aitriumos.com." |

**Don't show:** multi-patient submission, Data Tools, anything from a protocol (RTQA) trial, or any real data.
