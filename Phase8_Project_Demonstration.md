# Phase 8: Project Demonstration

## Demo Video Checklist

The demo video should include screen recording with voice-over and demonstrate the complete project.

### 1. Project Name
**Implementation of Client Script & UI Policy in ServiceNow**

Introduce the project as a ServiceNow micro-project based on the Incident Management module.

### 2. Purpose of the Project
Explain that the project aims to improve the Incident form using Client Scripts and UI Policies.

The project helps to:
- Dynamically control Incident form fields.
- Make fields mandatory based on conditions.
- Automatically update field values.
- Validate information before saving an Incident.
- Prevent unwanted changes through list editing.

### 3. Use / Benefits of the Project
- **Improves Data Accuracy** – Prevents incomplete or invalid Incident records.
- **Dynamic Form Behavior** – Fields respond automatically to user selections.
- **Better User Experience** – Provides immediate validation and feedback.
- **Controlled Data Entry** – Important fields can be made mandatory or read-only.
- **Prevents Unwanted Updates** – Restricts direct State changes through list editing.

### 4. Project Execution / Working Process
Show the following live on screen:
1. Open ServiceNow PDI.
2. Open **System UI → UI Policies**.
3. Show **High Impact Control**.
4. Show the condition **Impact = High**.
5. Show the Assignment Group UI Policy Action.
6. Show the Urgency UI Policy Action.
7. Open **System UI → Client Scripts**.
8. Show the onChange Client Script.
9. Set Impact to High and demonstrate automatic Urgency update.
10. Show the onSubmit Client Script.
11. Leave Assigned To empty and try to submit.
12. Show the error message.
13. Fill Assigned To and submit successfully.
14. Change Impact from High to Medium.
15. Demonstrate the Reverse if false behavior.
16. Open **Incident → All**.
17. Try to edit State directly from the list.
18. Show the alert message.
19. Open the Incident form.
20. Change State from the form and successfully save it.

### 5. Final Output
The final demonstration should show:
- **UI Policy – High Impact Control**
- **UI Policy Action – Assignment Group Mandatory**
- **UI Policy Action – Urgency Read-only**
- **onChange Client Script – Automatic Urgency Update**
- **onSubmit Client Script – Assigned To Validation**
- **onCellEdit Client Script – State List Edit Restriction**

The completed project demonstrates a dynamic, validated, and controlled Incident Management form using ServiceNow Client Scripts and UI Policies.

## Submission Checklist
- [ ] Demo video recorded with screen share + voice-over
- [ ] Project name and purpose explained
- [ ] UI Policy demonstrated
- [ ] Client Scripts demonstrated
- [ ] Testing scenarios demonstrated
- [ ] Final working output shown
- [ ] Video uploaded to Google Drive
- [ ] Google Drive access set to Anyone with the link, if required
- [ ] GitHub repository created
- [ ] All 8 phase documents uploaded
- [ ] GitHub repository link copied
- [ ] Google Drive demo link copied
- [ ] Both links submitted through SkillWallet
- [ ] Task cards moved to **To Be Reviewed**

## GitHub Repository Structure

```text
Implementation-of-Client-Script-and-UI-Policy/

├── Phase1_Brainstorming_and_Ideation.md
├── Phase2_Requirement_Analysis.md
├── Phase3_Project_Design.md
├── Phase4_Project_Planning.md
├── Phase5_Project_Development.md
├── Phase6_Project_Testing.md
├── Phase7_Project_Documentation.md
├── Phase8_Project_Demonstration.md
└── README.md
```
