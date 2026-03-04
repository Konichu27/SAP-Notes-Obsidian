## The Financial Hand-off (SD to FI)
Once the invoice is sent, the Sales & Distribution (SD) department's job is technically done. The "Incoming Payment" is an **Accounting (FI)** function.
### The Accounting Entry
When a payment is received, the system updates the General Ledger (G/L) as follows:
- **Debit:** Cash/Bank Account (Increases your liquid assets).
- **Credit:** Customer Receivables Account (Decreases the amount the customer owes you).

> **Key Concept:** This process **clears the "Open Item"** created during the billing step. If the billing step created the debt, the payment step "extinguishes" it.

> [!ABSTRACT] Demo
> [Processing Incoming Receivables](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_79E4D16570635793:demo#2)


---
## Automation: Electronic Bank Statements (EBS)

In modern SAP environments, manual entry is the exception, not the rule.
- **Electronic Import:** Companies import bank statement files directly into SAP.
- **Multi-Format Support:** SAP supports numerous global bank formats (e.g., MT940, BAI2, CAMT).
- **Auto-Matching:** The system attempts to automatically match the payment to the open invoice using "Search Alias" or reference numbers (like the Invoice Number).
- **Post-Processing:** If the system cannot find a match (e.g., the customer forgot to include the invoice number), the item is flagged for **manual post-processing**.

---
## The "Extended" Lead-to-Cash Ecosystem

|**Module**|**Purpose in the Payment Process**|
|---|---|
|**SAP Credit Management**|Once a payment is posted, the customer's **Credit Limit** is replenished, allowing them to place new orders.|
|**SAP Collections Management**|Helps the FI team prioritize which customers to contact for overdue payments based on "Collection Rules."|
|**SAP Dispute Management**|Used if a customer pays _less_ than the invoice amount (e.g., they claim goods were damaged). It tracks the investigation of the "Short Pay."|

---
### TL;DR for FI
1. **Sales Order** increases the _Credit Exposure_.
2. **Billing** creates the _Receivable (Open Item)_.
3. **Payment** clears the _Receivable_ and reduces the _Credit Exposure_.