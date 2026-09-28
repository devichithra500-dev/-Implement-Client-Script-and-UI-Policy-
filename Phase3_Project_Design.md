# Phase 3: Project Design

## System Architecture

```text
              [ServiceNow Incident Form]
                         |
                         v
                 [Field Values]
                         |
          +--------------+--------------+
          |                             |
          v                             v
   [Client Scripts]                [UI Policies]
          |                             |
          |                  +----------+----------+
          |                  |          |          |
          |                  v          v          v
          |              Mandatory   Visible   Read-only
          |                             |
          +-----------------------------+
                         |
                         v
                 [Form Validation]
                         |
              +----------+----------+
              |                     |
              v                     v
        [Valid Record]       [Invalid Record]
              |                     |
              v                     v
        [Save/Update]          [Error Message]
```

## Client Script Design

| Client Script | Type | Purpose |
|---|---|---|
| Auto set urgency for high impact | onChange | Automatically sets Urgency to High when Impact is High |
| Prevent save if Assigned To missing | onSubmit | Prevents saving when Assigned To is empty for High Impact |
| Prevent state change via list edit | onCellEdit | Prevents direct State modification from the list |

## UI Policy Design

| UI Policy | Condition | Action |
|---|---|---|
| High Impact Control | Impact = 1 – High | Make Assignment Group mandatory |
| High Impact Control | Impact = 1 – High | Make Urgency read-only |

**Reverse if false:** Enabled, so the field behavior returns to normal when the condition is no longer satisfied.

## Form Field Design

| Field | Purpose |
|---|---|
| Impact | Determines the impact level of the Incident |
| Urgency | Indicates the urgency of the Incident |
| Assignment Group | Identifies the responsible support group |
| Assigned To | Identifies the person responsible for the Incident |
| State | Shows the current Incident status |
| Priority | Indicates the Incident priority |

## Validation Design
- **onChange** → Automatically updates Urgency.
- **onSubmit** → Validates Assigned To before saving.
- **onCellEdit** → Prevents direct State modification from list view.
- **UI Policy** → Controls mandatory and read-only field behavior.
- **Reverse if false** → Restores normal field behavior when conditions change.
