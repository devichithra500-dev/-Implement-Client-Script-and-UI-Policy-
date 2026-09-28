# Phase 1: Brainstorming & Ideation

## Project Title
**Implementation of Client Script & UI Policy in ServiceNow**

## Problem Statement
In ServiceNow, users may enter incorrect or incomplete information while creating or updating Incident records. This can lead to invalid data, unnecessary errors, and inconsistent form behavior. There is a need to control form fields dynamically and validate user inputs based on specific conditions.

## Idea
Use ServiceNow's built-in **Client Scripts** and **UI Policies** to build a dynamic Incident form management system that:
- Validates user input using Client Scripts
- Dynamically makes fields mandatory, visible, or read-only using UI Policies
- Applies rules based on Incident fields such as Impact, State, and Assigned To
- Prevents users from submitting invalid or incomplete records
- Controls unwanted changes made through list editing

## Why This Approach
- Client Scripts allow client-side validation and dynamic form behavior.
- UI Policies provide an easy way to control field visibility, mandatory status, and read-only behavior.
- These features are commonly used in ServiceNow applications for maintaining data quality and form consistency.
- Combining Client Scripts and UI Policies provides both validation and dynamic user interface control.

## Expected Outcome
A working ServiceNow Incident configuration where:
1. Client Scripts validate user input according to defined conditions.
2. UI Policies dynamically control Incident form fields.
3. Required fields are enforced when necessary.
4. Invalid Incident records are prevented from being submitted.
5. Direct State changes through list editing can be controlled.

## Team Brainstorming Notes
- Discussed different ServiceNow customization options and selected Client Scripts & UI Policies.
- Decided to use Incident Management as the main form.
- Identified important fields such as Impact, State, Priority, Urgency, Assignment Group, and Assigned To.
- Planned to implement onChange, onSubmit, and onCellEdit Client Scripts.
- Planned UI Policies to control mandatory and read-only field behavior.
