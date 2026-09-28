# Phase 4: Project Planning

## Team Structure

| Member | Role | Responsibility |
|---|---|---|
| **T. Chithra Devi** | Team Lead | Create UI Policy and UI Policy Action; coordinate the overall project |
| **I. Pakialakshmi** | Member 1 | Perform mandatory enforcement, successful save, and reverse condition testing |
| **R. Palaniammal** | Member 2 | Perform list-edit blocking and form-based update testing |
| **T. Indhuja** | Member 3 | Create onChange, onSubmit, and onCellEdit Client Scripts |

## Task Breakdown & Sequencing

| Step | Task | Owner | Depends On |
|---|---|---|---|
| 1 | Create UI Policy – High Impact Control | T. Chithra Devi | — |
| 2 | Configure UI Policy Action – Urgency | T. Chithra Devi | Step 1 |
| 3 | Create onChange Client Script | T. Indhuja | Step 2 |
| 4 | Create onSubmit Client Script | T. Indhuja | Step 3 |
| 5 | Create onCellEdit Client Script | T. Indhuja | Step 4 |
| 6 | Test Mandatory Enforcement | I. Pakialakshmi | Step 5 |
| 7 | Test Successful Save | I. Pakialakshmi | Step 6 |
| 8 | Test Reverse Condition | I. Pakialakshmi | Step 7 |
| 9 | Test List Edit Blocking | R. Palaniammal | Step 8 |
| 10 | Test Form-Based Update | R. Palaniammal | Step 9 |
| 11 | Documentation & Final Review | All Members | Step 10 |

## Milestones
1. **Milestone 1:** Create UI Policy – T. Chithra Devi
2. **Milestone 2:** Configure UI Policy Action – T. Chithra Devi
3. **Milestone 3:** Create onChange Client Script – T. Indhuja
4. **Milestone 4:** Create onSubmit Client Script – T. Indhuja
5. **Milestone 5:** Create onCellEdit Client Script – T. Indhuja
6. **Milestone 6:** Testing – I. Pakialakshmi & R. Palaniammal

## Timeline

| Phase | Target |
|---|---|
| UI Policy & UI Policy Action | Day 1 |
| Client Script Implementation | Day 1 |
| Mandatory & Validation Testing | Day 2 |
| List Edit & Form Update Testing | Day 2 |
| Documentation & Final Review | Day 3 |
| Project Demonstration | Day 3 |

## Risk & Mitigation

| Risk | Mitigation |
|---|---|
| UI Policy may not trigger correctly | Verify Impact = High condition and Active status |
| Assigned To validation may fail | Test the onSubmit Client Script with High Impact and empty Assigned To |
| Urgency may not update | Verify the onChange Client Script and Impact field |
| State may still be editable from list | Test the onCellEdit Client Script directly from Incident list |
| Separate PDIs among team members | Replicate required configuration and testing in each member's PDI |
| Testing errors | Perform each test case separately and record expected and actual results |
