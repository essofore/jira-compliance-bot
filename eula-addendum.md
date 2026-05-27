
# ADDENDUM TO THE ATLASSIAN MARKETPLACE STANDARD EULA

**Product:** MedTech Compliance Tracker

**Provider:** Essofore LLC ("Provider")

**Effective date:** 2026-05-27

This Addendum modifies and supplements the Atlassian Marketplace Standard End User Agreement (["Standard EULA"](https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1)) between Provider and the Customer. In the event of any conflict between this Addendum and the Standard EULA, this Addendum will control solely with respect to the MedTech Compliance Tracker app (the "Software").

---

### 1. REGULATORY DISCLAIMER AND NO MEDICAL ADVICE

**1.1 Administrative Tool Only.** Customer acknowledges and agrees that the Software is an automated administrative and workflow tracking tool designed to assist software teams. The Software is **not** a medical device, does not perform medical device functions, and does not provide legal, clinical, quality assurance, or regulatory compliance advice.

**1.2 Customer Responsibility.** Customer retains sole and exclusive responsibility for:

* Verifying the accuracy, completeness, and appropriateness of all auto-generated sub-tasks, step-by-step instructions, safety class assignments (A/B/C), and regulatory clause mappings.
* Ensuring its software development lifecycle, Design History File (DHF), and risk management processes fully comply with all applicable regional and international standards (including but not limited to IEC 62304, ISO 14971, IEC 62366-1, ISO 13485, FDA 21 CFR Part 820, and EU MDR 2017/745).
* Final approval and validation of all compliance documentation before submitting it to any regulatory body or notified body.

**1.3 Disclaimer of Warranty.** Provider makes no warranty or representation that the Software’s automated scans will identify 100% of regulatory obligations, or that adherence to the generated sub-tasks will guarantee passing a regulatory audit or receiving market clearance/approval. The Software is provided on an as-is basis, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including, without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A PARTICULAR PURPOSE.

---

### 2. INTELLECTUAL PROPERTY AND OUTPUTS

**2.1 Ownership of Logic.** As between the parties, Provider retains all rights, title, and interest in the underlying scanning logic, proprietary regex/AI rules, clause mappings, and instructional templates embedded within the Software.
**2.2 License to Generated Tasks.** To the extent the Software generates text, sub-tasks, or workflow items inside Customer’s Jira instance ("Outputs"), Provider hereby grants Customer a perpetual, worldwide, non-exclusive, non-transferable, royalty-free license to use, modify, and reproduce those Outputs solely for Customer's internal business compliance purposes.

---

### 3. HEALTH DATA, PRIVACY, AND DATA SECURITY

**3.1 Patient Data Restrictions.** While the Software is designed to help teams track compliance infrastructure (e.g., HIPAA/GDPR framework implementation), Customer is strongly discouraged from inputting actual, unencrypted Protected Health Information (PHI) or personal data of patients into Jira issue fields scanned by the Software.
**3.2 Data Residency and HIPAA Status.** The Software is built on the Atlassian Forge framework and executes entirely within the Customer's Atlassian account.
 * **No External Transmission:** The Software scans Jira issues programmatically within the customer's Atlassian account; Provider does not transmit, persistently store, or log the text contents of Customer's Jira tickets on external servers under Provider's control.
 * **HIPAA Exclusion:** Because Provider has zero access to or visibility into Customer's data or any Protected Health Information (PHI), the parties agree that Provider does not act as a "Business Associate" as defined under HIPAA. Customer's existing data protection and HIPAA agreements with Atlassian solely govern the processing of all data within the Jira environment.

---

### 4. BULK OPERATIONS AND BACKFILL LIMITATIONS

**4.1 Operational Scope.** The Software provides a "Backfill" function allowing the bulk scanning of legacy Jira issues. Customer acknowledges that running bulk operations on exceptionally large backlogs may be subject to Atlassian API rate limits, throttling, or performance degradation within Customer's Jira instance.
**4.2 Limitation of Operational Liability.** Provider shall not be liable for any operational delays, temporary service interruptions, or Jira instance slowdowns resulting from Customer’s execution of bulk backfill operations. Customer is advised to run large backfills during non-peak business hours.

---

### 5. EXCLUSION OF CONSEQUENTIAL DAMAGES

In addition to the limitations of liability set forth in the Standard EULA, in no event will Provider be liable to Customer for any indirect, incidental, special, reliance, punitive, or consequential damages—including but not limited to loss of profits, delayed medical device product launches, market recalls, FDA warning letters, regulatory fines, or third-party product liability claims—arising out of or related to the use of or inability to use the Software, even if Provider has been advised of the possibility of such damages.

---