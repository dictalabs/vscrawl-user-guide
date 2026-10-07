## Overview

**Delegate Recipient** lets a document owner (or a recipient themselves) hand off a pending signing or approval task to a different person. The original recipient loses access to the document and the new person is invited to complete the fields in their place — only the **name and email** change; any fields already assigned to that recipient carry over automatically.

This is useful when the person a document was originally sent to is unavailable and someone else needs to review, fill, or sign on their behalf.

Delegation is available only on documents that have been sent (Multi Sign and Power Survey), and only for recipients with the **Signer** or **Approver** role who have not acted yet. The document owner can delegate any such recipient; a recipient can delegate only their own task.

!!! note ""
    To hand over your turns automatically while you are away, use [Auto Delegation](settings.md#auto-delegation) in Settings.

## Delegating a Recipient

1. Open the **Documents** list.
2. Find the document with the pending recipient you want to delegate.
3. Click the **⋮** (three-dot) menu on that document's row.
4. Select **Delegate Signing**.
5. If you are the document owner, the **Delegate Signing** dialog lists the **Pending recipients** — click **Delegate** next to the recipient you want to replace. If you are delegating your own task, the **Delegate Recipient** dialog opens directly.

![delegate-signing-menu-action.png](images/delegate-signing-menu-action.png)

!!! note ""
    The same **Delegate** action is also available from the recipient list inside a document's viewer/sidebar, for owners managing multiple recipients on a Multi Sign document.

## The Delegate Recipient Dialog

The dialog shows who the task is currently assigned to and lets you choose the replacement in one of two ways:

- **Choose from team** – search and pick an existing team member from a dropdown.
- **Enter details manually** – type the new recipient's full name and email directly.

![delegate-recipient-dialog.png](images/delegate-recipient-dialog.png)

### Choosing a Team Member

Click **Choose from team** to expand the picker, then search by name or email. Select a match from the list to auto-fill the new recipient's name and email.

![delegate-recipient-choose-team.png](images/delegate-recipient-choose-team.png)

### Entering Details Manually

If the new recipient isn't part of your team, skip the dropdown and fill in:

- **New Recipient Name** – full name of the person taking over (3–50 characters, letters only, with single spaces between words).
- **New Recipient Email** – their email address.

!!! note ""
    You cannot delegate to the recipient's own email — the new email must be different from the one currently assigned. You also cannot delegate to the document owner's email or to the email of another recipient already on the document.

### Confirming the Delegation

Once a new recipient is selected or entered, click **Delegate**.

- The current recipient immediately **loses access** to the document.
- The new recipient receives an invitation to complete the assigned fields, with the same fields the original recipient had.

Click **Cancel** at any point to close the dialog without making changes.
