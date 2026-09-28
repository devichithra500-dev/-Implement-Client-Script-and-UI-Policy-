# Phase 2: Requirement Analysis

## Functional Requirements

| # | Requirement |
|---|---|
| FR1 | The system shall provide an Incident form for creating and updating Incident records. |
| FR2 | The system shall validate form fields using Client Scripts based on defined conditions. |
| FR3 | The system shall use an onChange Client Script to perform actions when field values are changed. |
| FR4 | The system shall use an onSubmit Client Script to validate the form before submission. |
| FR5 | The system shall use an onCellEdit Client Script to control direct list editing. |
| FR6 | The system shall prevent submission when required conditions are not satisfied. |
| FR7 | The system shall use UI Policies to dynamically make fields mandatory. |
| FR8 | The system shall use UI Policies to make fields read-only when required. |
| FR9 | The system shall reverse UI Policy actions when the specified condition becomes false. |
| FR10 | The system shall ensure that Client Scripts and UI Policies work correctly together. |

## Non-Functional Requirements
- **Usability:** The Incident form should be simple and easy for users to operate.
- **Data Integrity:** Invalid or incomplete Incident records should be prevented from being submitted.
- **Performance:** Client Scripts and UI Policies should execute without noticeable delay.
- **Maintainability:** Scripts and policies should be easy for a ServiceNow administrator to understand and modify.

## Tools & Platform Requirements
- ServiceNow Personal Developer Instance (PDI)
- ServiceNow Incident Management
- Client Scripts
- UI Policies
- JavaScript
- ServiceNow Application Navigator

## Data Requirements
The Incident form uses fields such as:
- Caller
- Category
- Subcategory
- State
- Impact
- Urgency
- Priority
- Assignment Group
- Assigned To
- Work Notes
- Short Description
- Description

## Stakeholders
- **End User:** Creates, updates, and submits Incident records.
- **ServiceNow Administrator / Project Team:** Creates Client Scripts, UI Policies, conditions, and validation rules.
- **Project Guide / Trainer:** Reviews the implementation and verifies functionality.
