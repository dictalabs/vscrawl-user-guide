## Overview

The **Audit Report** is a dedicated, full-page timeline of everything that happened to a document — from creation to completion. It replaces the older summary popup with a complete activity log, including a detailed **Consent Record** for every recipient's e-signature consent.

## Opening the Audit Report

1. Go to the **Documents** list.
2. Click the **⋮** (three-dot) menu on the document you want to inspect.
3. Select **Audit Report**.

![audit-report-menu-action.png](images/audit-report-menu-action.png)

!!! note ""
    A **Power Survey** row has no **Audit Report** entry in this menu — each recipient's copy has its own audit action on the Power Survey screen instead. See [Power Survey](power_survey.md).

## Summary and Activity Log

The Audit Report opens as a full page with two sections:

- **Summary** – Subject, Owner, Signing Flow, Status, Workflow ID, Sent/Created/Completed timestamps, Time zone, the list of **Documents**, and the list of **Recipients** with their current status.
- **Activity log** – A chronological, timestamped list of every event on the document (Created, Opened, Sent invitations, Consent, Signed, Completed), each showing who performed it, their IP address, and access channel.

Timestamps are shown as date and time to the minute, converted to your own time zone; the **Time zone** row in the Summary names the zone in use.

You can download the document and its evidence report from the **Download** button in the top-right corner. It works the same way as **Download** on the [Documents](documents.md#downloading-documents) page: for a completed document with a separate evidence report you choose **Download all**, **Signed document** or **Evidence report**. Each entry in the Summary's **Documents** list also has its own download button, for saving a single file.

![audit-report-summary.png](images/audit-report-summary.png)

### Generating a Missing Evidence Report

If your organization produces evidence reports and a **completed** document does not have one yet — neither as a separate file nor merged into the signed PDF — the header shows a **Generate Evidence Report** button. Click it to create the report. When it is ready, an **Evidence report generated** message confirms it and the report can be downloaded like any other. If it fails, try again in a moment.

## Viewing Consent Details

Whenever a recipient consents to sign electronically, a **Consent** entry appears in the Activity log with a **View details** link.

![audit-report-consent-row.png](images/audit-report-consent-row.png)

Click **View details** to open the **Consent Record** dialog, showing exactly what was captured at the moment of consent:

- Recipient **name and email**
- **Consented at** timestamp and **How it was given**
- **Where it came from** — IP address, access channel, declared channel, and device (user agent)
- **Disclosure accepted** — the full consent text the recipient agreed to

![consent-record-dialog.png](images/consent-record-dialog.png)

Click **Close** to return to the Activity log.
