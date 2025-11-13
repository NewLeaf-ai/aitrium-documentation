# Creating a Protocol-Driven Trial in Trial Accelerator

This guide outlines the step-by-step process for creating a protocol-driven trial using the Advanced Mode in Trial Accelerator. This mode supports automatic ingestion of trial protocols, digitization of study arms and regimens, and configuration of downstream data workflows for designated hospital sites.

# ---

# Overview

The Advanced Trial Creation workflow is ideal for trials with structured protocols and well-defined data requirements. It minimizes manual setup by extracting study configurations from a protocol document and automating site-level experiences, including curated regimens and data collection schedules.

# ---

## **Trial Setup Workflow**

### **Step 1 – Create a Trial** **![][image1]**

Begin by navigating to the Trial Dashboard and selecting Create New Trial. Enter the following:

* Trial Name

* Start Date

* Description (optional)  
   

Click Next to proceed. Then, select Protocol Driven Trial to begin.

![][image2]

### **Step 2 – Upload Protocol Document**

### First, select your protocol method. We recommend creating a draft from PDF. **![][image3]**

Upload the trial protocol in supported formats (PDF or DOCX). The system will extract:

* Study arms and treatment regimens

* Dose and fractionation schedules

* Inclusion/exclusion criteria (informational only)

* Submission event timelines

You will see something similar to the following example.

![][image4]

Each of the study arms and regimens can be explored, confirmed, and edited here.

### **Step 3 – Confirm Study Arms and Regimens**

Review the proposed arms and associated regimens. You can:

* Rename or remove arms

* Adjust dose, fractionation, and modality settings

* Add new arms or regimens manually  
   

When the configuration matches your protocol, click ‘Publish Version’ in the top right.

### **Step 4 – Verify Data Collection Schedule**

Next, navigate to ‘Data Collection Schedule’ to confirm and edit the system’s parsed submission events. 

![][image5]

For each:

* Review the name, anticipated event information, and due date information

  ![][image6]

* Adjust timing windows (e.g., ±3 days) or anchor dates

By selecting ‘Add Data Collection Event’ fully customizable patient/site level events can be added as well:

![][image7]

 Click Continue when ready.

### **Step 5 – Assign De-Identification Policy**

Using either the activation checklist modal or navigating to ‘Settings’, add a DICOM anonymization policy to your trial. 

You will be prompted to one of the following:

* Create new policy: define a new DICOM de-identification policy based on an Aitrium template or from scratch. More information on creating policies can be found here \[link\]

* Use existing: leverage an existing de-identification policy which you’ve used for other projects

Once you’ve selected your policy, click ‘Publish Latest’ to assign the policy to the trial.

### **Step 6 – Enroll Trial Sites**

In the top-level navigation, select ‘Sites’ to view your enrolled sites. To add a site select ‘Add Sites’ in the top right.

Adding a site will prompt you to select an existing Aitrium Network site:

![][image8]

If a site you’re looking to add does not exist, send an email to [contact@aitriumos.com](mailto:contact@aitriumos.com) with the following information to begin the onboarding process:

* Site Name  
* Site City, Country, State/province  
* Site trial POC (First \+ Last name, Email Address)

Multiple sites may be added at any time. Click ‘Add X Sites’ to add them to the trial.

### **Step 7 – Assign Designated Site Users**

Once a site has been added you will also have the ability to authorize site users’ upload permissions:

![][image9]

These users will access a guided upload interface tailored to the arm, regimen, and event schedule. At this time, all users authorized to a trial will have the ability to upload patient data.

### **Step 8 – Configure Data Transfer Integration**

Designate a pre-existing data transfer integration (typically SFTP)

For more information on configuring a data transfer integration, please check here \[link\]

 Save your selection.

# ---

## Trial Activation and Propagation

Once all setup steps are complete:

* The trial is automatically deployed to all assigned sites

* Designated users will see the trial in the AitriumOS desktop application

* Upload workflows will be pre-configured based on:

  * Assigned study arms and regimens \+ resulting data requirements

  * Data collection schedules

  * De-identification policy

  * Structure nomenclature

Finally, click ‘Publish Version’ in the upper-right hand corner to propagate your trial to all participating sites. Your trial is now live.

# ---

# **Advanced Trial Configuration**

Once a protocol‑driven trial is live, you have a suite of configuration tools to refine the setup. These features let you tailor arms/regimens, enforce dose constraints, shape the data‑collection timeline, and set up benchmark/site‑events for ongoing quality and compliance.

### **1\. Manually Create or Edit Study Arms & Regimens**

You can fine‑tune the treatment structure of your trial beyond automatic extraction:

* Use the *Arms & Regimens editor* to add new arms (e.g. “Adaptive”, “Hypofractionated”) or deactivate existing ones

* Define each regimen’s dose, fractionation, and modality (e.g. 60 Gy in 30 fx, IMRT)

* Reassign patients to updated arms when needed

* All changes are logged and version-controlled

### **2\. Add Dose Constraints to Treatment Regimens**

Each regimen can have one or more ROI‑specific dose constraints:

* Examples: *Spinal Cord Dmax \< 45 Gy*, *Heart V20Gy \< 10%*, *Lung Mean \< 12 Gy*

* Mark constraints as Hard (must-pass) or Soft (advisory)

* Constraints are used in QA review and scorecard generation

### **3\. Advanced Data Collection Schedules**

The schedule of expected data submissions can be customized:

* Add/edit events such as “Week 3 Mid-Tx” or “Follow-up Month 6”

* Specify required file types (e.g. CT, RTSTRUCT, MRI)

* Configure timing logic (e.g. every 3 months, ±5 days)

* Apply globally or to specific arms

### **4\. Configure Benchmark Cases & Site-Level Events**

To enforce standards and site onboarding:

* Upload Benchmark Cases with gold-standard datasets

* Use them to test site uploads and assess QA readiness

* Add Site-Level Events such as:

  * Investigator training windows

  * Credentialing deadlines

  * Interim QA audits  
     These events appear on the trial dashboard for each site.

# ---

# Troubleshooting & Support

* Refer to the Trial FAQ: [https://docs.aitriumos.com/faq/trials](https://docs.aitriumos.com/faq/trials)

* Contact support: support@aitriumos.com

# ---

# You’ve successfully created and configured a protocol-driven trial in Trial Accelerator.

# 

# 

[image1]: images/trial_accelerator_images[image1].png
[image2]: images/trial_accelerator_images[image2].png
[image3]: images/trial_accelerator_images[image3].png
[image4]: images/trial_accelerator_images[image4].png
[image5]: images/trial_accelerator_images[image5].png
[image6]: images/trial_accelerator_images[image6].png
[image7]: images/trial_accelerator_images[image7].png
[image8]: images/trial_accelerator_images[image8].png
[image9]: images/trial_accelerator_images[image9].png