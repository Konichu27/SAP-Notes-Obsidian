# Service Contracts

A **Service Contract** represents an **outline agreement** with customers defining the scope of services under specific conditions for a particular period.
### Main Features:
- **Outline Agreement:** Defines the scope of services delivered for the customer. 
- **Service Levels:** Specifies the entitlements (SLAs[^SLA]) the customer receives.
- **Coverage:** Lists specific **parts covered** (e.g., brake sets, bike computers).
- **Product List:** Contains the specific services and service parts in the contract entitlement.
- **Price Agreements:** Includes predefined prices for services and parts.
- **Limitation:** Can limit services based on **value** and/or **quantity**.

[^SLA]: Service level agreement
### Structure of a Service Contract:
- **Header (Details):** Refers to the whole contract and all included items.
- **Items:** Contains item-specific information and individual entitlements.

![[Pasted image 20260303173306.png]]

> [!ABSTRACT] Demo
> [Displaying a Service Contract](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_90E7A1D527764290:demo#2)

---
# Service Contract Billing

**Scenario:** A customer (e.g., Northsea Energy) pays a fixed monthly fee (e.g., 35€) for predefined services and spare parts.

### The Billing Process
![[Pasted image 20260303173651.png]]
Billing Document Request -> Billing Document
1. **Billing Document Request (BDR):** Generated first to initiate the billing cycle.
2. **Billing Document:** The actual **Invoice** created to charge the customer.
3. **Billing Plan:** Located within the **service contract item**; used to verify if the billing process was carried out correctly.

| **Step**       | **Action**                      | **Purpose**                                          |
| :------------- | :------------------------------ | :--------------------------------------------------- |
| **1. Request** | Create Billing Document Request | Identifies what is ready to be billed.               |
| **2. Invoice** | Create Billing Document         | Finalizes the charge to the customer.                |
| **3. Verify**  | Check Billing Plan              | Ensures the timeline and amounts match the contract. |

---
# TL;DR for Service Management
- **Contracts** move from "reactive" service to "proactive" scheduled agreements.
- **Entitlements** define exactly what parts/services are "free" or discounted.
- **Billing** is driven by the **Billing Plan** inside the contract item, not just a one-time delivery.

> [!ABSTRACT] Demo
> [How to Bill a Service Contract](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_474598E8B84BF49D:demo#2)