### Goods Receipt
- References the corresponding purchase order
- Once the goods receipt is recorded, the system suggests all open items from the PO
- The following can be checked:
	- If the right material has been delivered
	- If the right quantity has been delivered (over/under-delivery?)
	- If perishable goods are within their minimum shelf life
- Multiple goods receipts can be issued for one purchase order in case there is a problem (ex. shortage)

### SAP S4/HANA Role
- **Post Goods Receipt for Purchasing Document** app
1. Enter the **number** of the purchase order
	1. (OPTIONAL) **Name of the supplier/plant ordered from**
2. System proposes a **list** with all purchasing documents fitting the entry
3. After selecting, all open items of the document are shown in the **item list**
4. Proposed quantity & storage location can be **changed**
5. Finally, goods receipt is **posted**
### Generated Documents
- The following documents/info are generated every posting:
	- Info about the delivered material
	- Info about the delivered quantity
	- Material plant & material storage location

![[Pasted image 20260128234114.png]]

![[Pasted image 20260128234741.png]]