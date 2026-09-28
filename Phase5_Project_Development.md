# Phase 5: Project Development

This phase covers the actual implementation of Client Scripts and UI Policies on the ServiceNow Incident table.

## Step 1: Create the UI Policy
- Navigated to **System UI → UI Policies**.
- Clicked **New**.
- **Name:** `High Impact Control`
- **Table:** `Incident`
- **Active:** `true`
- Condition: **Impact is 1 – High**
- Configured **Assignment Group** as mandatory.
- Enabled **Reverse if false**.
- Clicked **Submit**.

## Step 2: Configure UI Policy Action – Urgency
- Opened **High Impact Control**.
- Navigated to **UI Policy Actions**.
- Clicked **New**.
- **Field Name:** Urgency
- **Read-only:** true
- **Visible:** unchanged
- Clicked **Submit**.
- Verified that Urgency becomes read-only when Impact is High.

## Step 3: Create onChange Client Script
**Name:** `Auto set urgency for high impact`  
**Table:** Incident  
**Type:** onChange  
**Field:** Impact  
**Active:** true

```javascript
function onChange(control, oldValue, newValue, isLoading) {
    if (isLoading || newValue == '') {
        return;
    }

    if (newValue == '1') {
        g_form.setValue('urgency', '1');
        g_form.addInfoMessage('Urgency set to High for High impact incident.');
    }
}
```

When Impact is changed to High, the script automatically sets Urgency to High.

## Step 4: Create onSubmit Client Script
**Name:** `Prevent save if Assigned To missing`  
**Table:** Incident  
**Type:** onSubmit  
**Active:** true

```javascript
function onSubmit() {
    if (g_form.getValue('impact') == '1' &&
        g_form.getValue('assigned_to') == '') {

        g_form.showErrorBox(
            'assigned_to',
            'Assigned To is mandatory for High impact incidents.'
        );
        return false;
    }
    return true;
}
```

The script prevents saving when Impact is High and Assigned To is empty.

## Step 5: Create onCellEdit Client Script
**Name:** `Prevent state change via list edit`  
**Table:** Incident  
**Type:** onCellEdit  
**Field:** State  
**Active:** true

```javascript
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {

    alert('State cannot be updated using list editing. Please open the Incident.');

    callback(false);
}
```

This prevents users from changing State directly through list editing.

## Step 6: Test Mandatory Enforcement
- Opened **Incident → Create New**.
- Set Impact to **High**.
- Left Assigned To empty.
- Clicked Submit.
- Record was not saved.
- Error message was displayed.

## Step 7: Test Successful Save
- Selected a user in Assigned To.
- Clicked Submit.
- Incident was saved successfully.
- Verified the configured Client Script and UI Policy behavior.

## Step 8: Test Reverse Condition
- Opened an Incident with Impact = High.
- Changed Impact from High to Medium.
- Verified that Assigned To was no longer mandatory.
- Verified that Urgency became editable.
- Saved the record successfully.

## Step 9: Test List Edit Blocking
- Opened **Incident → All**.
- Tried to edit State directly from the list.
- Alert message appeared.
- State value remained unchanged.

## Step 10: Test Form-Based Update
- Opened the Incident form.
- Changed State.
- Clicked Update.
- State was successfully saved through the form.
