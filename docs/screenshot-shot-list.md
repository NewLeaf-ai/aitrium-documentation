# AitriumOS 2.3.4 docs: screenshot shot list

Internal working file (not published: `docs/` is in `.mintignore`).

**Capture setup (applies to every shot)**
- AitriumOS **2.3.4** on the Mac app, signed in to the Demo site account. Light mode.
- App window **1440×900** (points). Export PNG at 2x (2880×1800) and crop as noted.
- **Sandbox trials only, synthetic `E2E-` patients only.** No real patient data, no real site names in folder paths. Trial names visible in shots must be sandbox names.
- Keep the mouse pointer out of the shot. No hover tooltips unless noted.
- Save each file at the exact path below (repo root = docs worktree). The MDX already references these paths.
- Two shots reuse existing images: `images/trial_submissions/submission-queue-completed.png` (still accurate; retake only if convenient, same path).

**Data to prepare before you start**
- **EORTC-style sandbox trial** (non-protocol, dataset types) with:
  - dataset type A: imaging (CT + RTSTRUCT + RTPLAN + RTDOSE), **with instructions text** set on the type, and naming one supporting document (for example "Surgical report", optional or required);
  - dataset type B: documents-only (one PDF fileset, required);
  - patients `E2E-EORTC-001` (nothing sent) and `E2E-EORTC-002` (type A already sent once).
  - Folders: `E2E-EORTC-001_typeA/` (complete export + one PDF document), `E2E-docs/` with `report.pdf` and a macro-enabled `notes.docm` (or any `.exe`).
- **Protocol (RTQA) sandbox trial** with QA checks, at least one study arm with two regimens of different schedules, and:
  - patient `E2E-RTQA-001` not yet set up (no arm/regimen);
  - patient `E2E-RTQA-002` set up, with a due event, folder whose plan **matches** its regimen, one structure set;
  - patient `E2E-RTQA-003` set up on regimen X, folder whose plan matches **another** regimen of the arm (gives "Outside the protocol" and a "Switch this patient to …" option);
  - patient `E2E-RTQA-004` folder with **two RTSTRUCTs** (for example planning CT + MR), at least one needing a name decision.

---

## Pass 1: EORTC-style sandbox trial

### 1. `images/trial_submissions/2-3/eortc-patient-list.png`
- **Page/section:** EORTC data submission → Add a patient.
- **Screen/state:** trial page, **Submit a Patient Dataset** section. Type `E2E-EORTC-00` in **Search or add ID** so both patients show. `E2E-EORTC-002` type A cell reads **Sent** (green); `E2E-EORTC-001` cells read **Submit Dataset**. Status tabs (**Not started · In progress · Complete · Withdrawn**) and the **Sort:** menu and **Add patient** button visible.
- **Crop:** the section only (toolbar, tabs, table header, two rows, Last Sent column). Drop the app sidebar.
- **Highlight:** none.

### 2. `images/trial_submissions/2-3/eortc-analyzer-results.png`
- **Page/section:** EORTC data submission → 1. Check the dataset.
- **Screen/state:** `E2E-EORTC-001` → **Submit Dataset** (type A) → **Select Directory** → `E2E-EORTC-001_typeA/`. Wait for results. **Studies** tab selected; statement reads "Everything {type A} requires is in this folder." (or "All the imaging … requires is in this folder." when documents are named); **What {type A} requires** card with rows; header chip **Ready to continue**; header steps **Analyze · Standardize · De-identify · Contribute**.
- **Crop:** full submission panel (header steps to bottom of the requirements card).
- **Highlight:** none.

### 3. `images/trial_submissions/2-3/supporting-documents.png`
- **Page/section:** Documents submissions → Supporting documents in an imaging submission.
- **Screen/state:** same analyzer, scroll to **Supporting documents**. One document row with the PDF chosen (file chip visible), tier **Required**/**Optional** under its name, checkbox **These documents contain no patient identifiers.** ticked.
- **Crop:** the Supporting documents section only, with ~16 px margin.

### 4. (no file) Continue through the flow
- Select **Standardize RT Structures** → **Before you continue**: tick both acknowledgments → continue. In standardization select **Apply Changes** (or **Continue with Standard Labels**). Let de-identification run.

### 5. `images/trial_submissions/2-3/upload-in-progress.png`
- **Page/section:** EORTC guide → 5. Upload to trial; RTQA guide → 5. Data transfer (shared).
- **Screen/state:** after **Confirm and Transfer**, during **Data Transfer** (progress 40–80%). Header steps must read **Analyze · Standardize · De-identify · Contribute** (the word "De-identify" must be visible). Transfer card shows **Data Transfer** active and **Aitrium Sync** pending.
- **Crop:** header steps + transfer card; cut the logs below the card.
- **Tip:** use a larger folder or a slow destination so you have time to capture.

### 6. `images/trial_submissions/2-3/submission-complete.png`
- **Page/section:** both guides → Upload / Data transfer (shared).
- **Screen/state:** **Submission complete** with **Delivery**, **What happens next** ("The trial's team sees {type A} for E2E-EORTC-001 in their portal.") and **Instructions from {organization}** showing the type's instruction text.
- **Crop:** the completion card; include the header steps.

### 7. `images/trial_submissions/2-3/eortc-what-was-sent.png`
- **Page/section:** EORTC data submission → Send a new version.
- **Screen/state:** close the flow, back on the trial page select `E2E-EORTC-001`'s **Sent** cell (type A). Dialog with "What was sent for this patient, checked against this dataset type." and the **Send a new version** button.
- **Crop:** the dialog only.

### 8. `images/trial_submissions/2-3/documents-add-files.png`
- **Page/section:** Documents submissions → Add files.
- **Screen/state:** `E2E-EORTC-002` → **Submit Dataset** under type B (documents-only). **Add files** → add `report.pdf` and `notes.docm`. The amber notice ("Aitrium does not remove patient information from documents…") at top; card with accepted format badge and **Required**; `report.pdf` shows **Ready**; `notes.docm` shows "Macro-enabled Office files can't be submitted…"; footer shows "Remove the files that can't be sent."
- **Crop:** the documents panel (step title "Add documents" to the Continue button).
- **Then:** cancel the submission (do not send).

---

## Pass 2: protocol (RTQA) sandbox trial

### 9. `images/trial_submissions/2-3/configure-patient.png`
- **Page/section:** RTQA data submission → Set up a patient.
- **Screen/state:** `E2E-RTQA-001` → **Setup Patient**. Set Randomization Date and Study Arm (don't save yet), pick a regimen and set its start date so the pending list shows **Save 1 Regimen**. Badge reads "N of M required setup items complete".
- **Crop:** the dialog only.
- **Then:** save, so the patient is ready.

### 10. `images/trial_submissions/2-3/rtqa-analyzer-results.png`
- **Page/section:** RTQA data submission → 1. Check the dataset.
- **Screen/state:** `E2E-RTQA-002` → **Submit** on its due event → **Select Directory**. Wait until the button no longer reads **Checking plan and dose…**. Plan row reads **Matches the protocol**; study named "Radiotherapy study"; header chip **Ready to continue**; header steps **Analyze · Standardize · De-identify · RapidQA · Contribute**.
- **Crop:** full submission panel.
- **Optional extra (not referenced):** capture the **Checking plan and dose…** state for the walkthrough team.

### 11. `images/trial_submissions/2-3/map-protocol-structures.png`
- **Page/section:** RTQA data submission → 2. Map structures.
- **Screen/state:** continue from shot 10 to **Map Protocol Structures** after suggestions load. Show mapped targets and OARs, at least one row "already has this name".
- **Crop:** the mapper; include its title and description ("Map your dataset structures to the trial's structure names.").

### 12. `images/trial_submissions/2-3/qa-check.png`
- **Page/section:** RTQA data submission → 4. QA check.
- **Screen/state:** continue through de-identification to **QA check** once the preview is graded: title "{regimen} · N protocol checks", **Structures** panel, filters (**Search checks**, **All tiers**, **All results**, **All domains**), at least two result categories visible.
- **Crop:** the QA check card.
- **Then:** cancel or finish the send (finishing is fine on the sandbox).

### 13. `images/trial_submissions/2-3/rtqa-plan-outside-protocol.png`
- **Page/section:** RTQA data submission → Plan and dose checks.
- **Screen/state:** `E2E-RTQA-003` → **Submit** → folder. Plan card **Outside the protocol** with the three options: **Submit this plan as planned** ("Submit as planned"), **Switch this patient to {regimen}** ("Switch"), **Choose a different folder** ("Select folder"), and the footer "If you submit this plan, everything uploads and QA runs. The QA report states the difference." Header chip **1 choice**.
- **Crop:** the plan card with its question.
- **Then:** cancel the submission (don't switch the regimen).

### 14. `images/trial_submissions/2-3/structure-set-step.png`
- **Page/section:** Multiple structure sets.
- **Screen/state:** `E2E-RTQA-004` → **Submit** → folder with two RTSTRUCTs → continue to standardization. Step header "Structure set 1 of 2: CT · N images" with the **Graded** chip and its usage line ("used by plan …").
- **Crop:** step header + first rows of the table.
- **Then:** cancel the submission.

### 15. (optional) `images/trial_submissions/submission-queue-completed.png`
- **Page/section:** RTQA data submission → Find what's due.
- **Screen/state:** **Trial Data Submission Schedule** with **Refresh**, filter chips, rows with **Completed** + **Re-submit** and an **Overdue** row. Only retake if the existing image's trial name or data shouldn't be shown; keep the same path.

---

**Count:** 13 new images (shots 1–3 and 5–14) + 1 optional retake.

**Images no longer referenced by any page (safe to delete after the new shots land):**
`images/trial_submissions/dataset_analyzer_results.png`, `map_target_structures.png`, `map_oar_structures.png`, `qa_metrics_review.png`, `patient_schedules.png`, `upload-in-progress.png`, `upload-complete-confirmation.png`, `dataset-table-submitted.png`.
