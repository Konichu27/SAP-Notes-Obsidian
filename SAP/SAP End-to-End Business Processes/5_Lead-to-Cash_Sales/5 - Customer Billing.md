# Billing Document

The **billing document** copies data from the **sales order** and **delivery document**.

It is also **referenced by FI** for their calculations (particularly the **G/L accounts**).
- **Debit:** Customer Receivables Account (Balance Sheet).
- **Credit:** Revenue Account (Profit & Loss).

![[Pasted image 20260302221441.png]]

|**Module**|**Impact / Document Generated**|
|---|---|
|**FI (Accounting)**|Creates a **Financial Accounting Document** and an "Open Item" in Accounts Receivable.|
|**CO (Controlling)**|Generates a **Controlling Document** to track revenue against cost centers/internal orders.|
|**CO-PA**|Generates a **Profitability Analysis** document for multi-dimensional reporting.|
|**Credit Management**|Updates the customer’s **Credit Limit** (reducing the available credit as the debt is recognized).|
|**Analytics**|Updates the Sales Information System (SIS) or SAP BW/4HANA for reporting.|
## Invoice
- Actually often the **last step** in SD!
- Can involve one or more deliveries/orders.

**Criteria for a single invoice:**
1. **Payer:** Must be the same.
2. **Billing Date:** Must be the same.
3. **Destination Country:** Must be the same.

> **Note:** If any of these differ, the system will perform a **"Billing Split"** and create separate documents.

>[!ABSTRACT] Demo
>[Creating a Billing Document](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_474598E8B84BF49D:demo#2)

---
# Document Flow

![[Pasted image 20260302221839.png]]

Standard Order -> Delivery -> Billing Document -> Accounting Document