## Inventory Management
- Involves the ff.
	- **Management** of material stocks
	- **Planning** of material movements
	- **Carrying** of physical inventory

### Stock Quantity Types
- **Unrestricted-use**
- **In quality inspection**
- **Ordered, but unreceived**
- **Reserved** (i.e. already in the warehouse but reserved for another purpose)

> **Organizational Level**: Storage Location (excl. plant-level stock)

### Stock Value Types

> **Valuation area** - defines the value of the material. 
> It can be set either at the *company code* or *plant* level.
> Usually though, it's set at the plant level, especially in production.
## Goods Movements

### Effects of Good Movements
The system automatically updates the ff. with every goods movement:

| **Department**             | **Updated Data**                                  |
| -------------------------- | ------------------------------------------------- |
| Inventory Management       | Stock quantities, values                          |
| Financial Accounting (FI)  | G/L accounts<br>(automatic account determination) |
| Management Accounting (CO) | Cost accounting assignments                       |
IFM - SGC
### Types of Goods Movements

![[Pasted image 20260225124237.png]]

| **Type**             | **Description**                                                                                                                                                                                                                                                                                               | **Effect**                                       | **Keyword**                 |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | --------------------------- |
| **Goods Receipt**    | Goods received from external vendors and production                                                                                                                                                                                                                                                           | **Increase** in warehouse stock                  | **Receipt** -> **Received** |
| **Goods Issue**      | Material withdrawal, consumption, or goods shipment                                                                                                                                                                                                                                                           | **Decrease** in warehouse stock                  | **Issue** -> to give away   |
| **Stock Transfer**   | Movement from one storage location to another                                                                                                                                                                                                                                                                 | Either between two plants or even the same plant | If **stock**, it's movement |
| **Transfer Posting** | Changes stock identification/qualification.<br><br>Ex.<br>- Release of stock for QA<br>- Transfer posting (i.e., transformation) from material to material (ex. re-grading or processing of materials)<br>- Transfer of consignment material to own stock (buying consigned stock to convert to UU[^1] stock) | Changes stock identification/qualification       | If **posting**, it's change |
|                      |                                                                                                                                                                                                                                                                                                               |                                                  |                             |
[^1]: Unrestricted-use

## Goods Receipt Postings
- Two documents are created:
	- Material Document
	- Financial Document
### FI Integration

The following are posted after a **Goods Receipt**:

| **Balance** | **Account Type**                                 | **Purpose**                                                                                  |
| ----------- | ------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| **Debit**   | Stock Account                                    | Records new stock in warehouse.<br>This is a *balance sheet* account as it is part of Assets |
| **Credit**  | GR/IR Account<br>(Goods Receipt/Invoice Receipt) | Part of liabilities (Accounts Payable) as they are currently unpaid                          |
GR/IR involves the following, depending on the situation:

| **Term**             | **Goods?** | **Invoice?** | **Balance for the Company** |
| -------------------- | ---------- | ------------ | --------------------------- |
| Purchases in Transit | No         | Yes          | **Debit**                   |
| Unbilled Payables    | Yes        | No           | **Credit**                  |
#### Standard FI Accounting Flow

| **Step**               | **Posting Type** | **Debit**         | **Credit**        | **GR/IR Balance**      |
| ---------------------- | ---------------- | ----------------- | ----------------- | ---------------------- |
| **1. Goods Receipt**   | **GR**           | Stock Account     | **GR/IR Account** | **Credit** (Liability) |
| **2. Invoice Receipt** | **IR**           | **GR/IR Account** | Vendor (A/P)      | **Zero** (Cleared)     |

## Miscellaneous

> [!NOTE] Demos
> [How to Post a Goods Receipt and Display Stock Overview](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_752FF19D48AA7997:demo)
> [How to Display a Financial Document for Goods Receipt](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6492E2A7A06CCA85:demo#2)