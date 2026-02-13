- We start with a single Purchase Order

### Purchase Order
- Formal request to a supplier to supply specific materials
- Quantity of material, agreed price, received person, etc.
- Goods receipt is received after delivery and purchase is in inventory, and the supplier invoice is registered in SAP S4/HANA
### SAP S4/HANA Role
- **Manage Purchase Orders** app
	- Automatically creates documents that can be sent or printed out for the supplier
- There are many ways to create a purchase order:
	- Creating from scratch (ex. ordering from a new supplier for the first time)
	- Referencing other documents, ex. earlier purchase orders
- There are always the following default values:

| Default Value                                           | From...                       |
| ------------------------------------------------------- | ----------------------------- |
| Ordering address, terms of payment, freight (incoterms) | Supplier's business partner   |
| Material short text, unit of measure, material group    | Material master record        |
| Negotiated price                                        | Purchasing information record |
### Parts of a Purchase Order
- Document Header - contains info for the entire purchase order
- Item - corresponds to the material ordered for the supplier

![[Pasted image 20260128231050.png]]

