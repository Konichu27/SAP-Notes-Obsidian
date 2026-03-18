## Purchase Orders
- The core of operational procurement
- Done after the material requirements (master record) & contract are defined
- Converted from purchase requisitions made in the first step

### Elements of a Purchase Order
- **References** - POs can reference the ff. to save data entry:
	- *Existing PO*
	- *Purchase requisition*
	- *Quotation*
	- *Contract*
- **Master Records** - automatically fill existing info
	- *Product Master Record* - if exists, material short text, purchase order unit, and material group are filled
	- *Purchasing Info Record* - if exists, price is automatically proposed
	- *Default Values*
	- *Supplier*
		- *Standard Purchase Order - for external suppliers
		- *Stock Transport Order* - for internal suppliers (company-owned plants)

### Document Structure of a Purchase Order
- Contains **header data** (general data like document type, supplier, currency, terms of payment, plant/s etc.) and **item data** (material/service, order, quantity)
- **Item categories** can also be used to define an item's procurement process (subcontracting, stock transfer, vendor consignment, etc.)

> Reference for item categories: [[1 - Master Record, Requisition#Category Assignment]]
## Automatic PO Generation
- Purchase requisitions can be *automated* to be converted to purchase orders, as long as four conditions are met:
	- **"Automatic PO"** - must be <u>checked</u> for *<u>Material Master</u> and <u>Supplier Master</u>
	- **Source of Supply** - A valid source (like a contract or info record) must be assigned to the requisition.
	- **No manual intervention** - The system doesn't need extra info (like a missing tax code) to finish the job.

![[Pasted image 20260225115447.png]]



## Miscellaneous

> [!NOTE] Demos
> [How to Create a Purchase Order from a Purchase Requisition](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_D83AC434A41DCE81:demo#2)