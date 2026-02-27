- We are in the **first** step of the procurement process.
- Master data, requirements, etc. must be provided
## Supplier Master Data Record
- Defined on a *Supplier* business partner
## Product Master Record
- Must be created for a new product
- Fields include:
	- **Material Type**
	- **Industry Sector**
	- **References** (ex. engineering data for plant, purchasing data for plant/storage location)
### Types of Materials
| **Type** | **German**       | **English**         |
| -------- | ---------------- | ------------------- |
| **FERT** | Fertiges Produkt | Finished Product    |
| **ROH**  | Rohstoff         | Raw Material        |
| **HALB** | Halbfertigwaren  | Semi-Finished Goods |
[SAP Material Types Explained: ROH, HALB, FERT, NLAG & More for Effective Inventory Control | Learn with Yasir](https://yasirbhutta.github.io/sap-education-research/docs/sap-mm/material-types.html)
### Steps on Creating a Master Record

| **Step** | **View/Department** | **Input Data**                                                                                                                                                      | **Valid For...**       |
| -------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| **1.**   | **Engineering**     | Description, weight, material type, dimension                                                                                                                       | Client                 |
| **2.**   | **Purchasing**      | Purchasing group, tolerance information, quality inspection requirements                                                                                            | Plant                  |
| **3.**   | **Storage**         | Storage bin, etc.<br><br>*NOTE:* A material can only be stored in one storage bin.<br>If you need several bins, you need to use warehouse management functionality. | Plant storage location |
| **4.**   | **Accounting**      | Valuation class, valuation price (either standard or moving average)<br><br>*NOTE:* Moving average is usually used for raw materials.                               |                        |
## Purchase Requisition
- Internal document to start the procurement process
- Part of the *requirement* step

### Steps in Creating a Purchase Requisition
![[Pasted image 20260224154242.png]]
1. Creating the purchase requisition
2. Follow-on step
	1. Material in stock
		- Placed in storage after goods receipt. Postings are made automatically for each goods receipt or issue, as well as the corresponding stock & consumption postings/adjustments, as well as value & quantity adjustments in the master record.
		- Material must have a master record
	2. Direct consumption
		- *Account assignment category* + other data

### Category Assignment

- **Item Category** - Affects the *Inventory* and the *Goods Receipt* process
- **Account Assignment** - Affects the *Finance (FI)* and *Controlling (CO)* postings

![[Pasted image 20260224160254.png]]
![[Pasted image 20260224161016.png]]

| **Feature**             | **Item Category (L, etc.)**                                      | **Account Assignment (K, P, etc.)**                      |
| ----------------------- | ---------------------------------------------------------------- | -------------------------------------------------------- |
| **Question it answers** | **How** are we getting this? (Subcontract, Service, Consignment) | **Who** is paying for this and which GL account is hit?  |
| **Inventory Impact**    | Changes _how_ stock is moved (e.g., shipping components out).    | Tells the system _not_ to track this as warehouse stock. |
| **Typical Example**     | **L**: We send raw parts; they send back a finished assembly.    | **K**: Buying 100 pens for the Accounting department.    |
#### Item Categories

| **Item Category** | **German**      | **Name**           | **Description**                                                                                            |
| ----------------- | --------------- | ------------------ | ---------------------------------------------------------------------------------------------------------- |
| **(Blank)**       | Standard        | **Normal**         | The default category for standard procurement where you buy a material and receive it into your own stock. |
| **K**             | Konsignation    | **Consignment**    | You keep the vendor's stock at your site, but you only pay for it once you actually use or "withdraw" it.  |
| **U**             | Umlagerung      | **Stock Transfer** | Used to move materials from one plant to another within the same company.                                  |
| **L**             | Lohnbearbeitung | **Subcontracting** | You provide raw components to a vendor, and they send back a finished or semi-finished product.            |
| **D**             | Dienstleistung  | **Service**        | Used for purchasing labor or tasks (like consulting or repairs) rather than physical goods.                |

#### Account Assignment Categories
| **Assignment Category** | **German**        | **Name**        | **Description**                                                                                        |
| ----------------------- | ----------------- | --------------- | ------------------------------------------------------------------------------------------------------ |
| **K**                   | Kostenstelle      | **Cost Center** | Charges the expense to a specific department's budget (e.g., HR, IT, or Marketing).                    |
| **A**                   | Anlage            | **Asset**       | Used when purchasing a Fixed Asset (like a vehicle or a building) that will be depreciated over time.  |
| **P**                   | Projekt           | **WBS Element** | Charges the cost to a specific "Work Breakdown Structure" element within a larger Project (PS module). |
| **F**                   | Fertigungsauftrag | **Order**       | Charges the cost to an Internal Order, Production Order, or Maintenance Order (EAM).                   |
## Transferring the Purchase Requisition into a Purchase Order
1. **Convert** the purchase requisition into a purchase order
2. **Use** the purchase requisition to create several quotation requests
	 - Could create purchasing info records or a supplier contract
3. **Transfer** the purchase requisition to SAP Ariba. This creates a request for quotation (RFQ)/quote in SAP Ariba

## Purchasing Info Record
- Master data record for the sourcing process
- *Conditions* - possible pricing elements that could be valid for the purchasing process

![[Pasted image 20260224175118.png]]

## Alternate Steps
![[Pasted image 20260224175945.png]]

## Miscellaneous

> [!NOTE] Demos
> [How to Create a Supplier Business Partner](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_5352EF1931CAAC9E:demo#2)
> [How to Create a Product Master](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_9960C28E5B4681A7:demo#2)
> [How to Create a Purchase Requisition](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_84728B4C9B3AF0A5:demo#2)
> [How to Process a Request for Quotation](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6E3702716C781DBF:demo#2)

