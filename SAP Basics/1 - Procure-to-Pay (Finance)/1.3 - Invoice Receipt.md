- Managed by **Create Supplier Invoice** (SAP Fiori)
- Invoice can be entered manually or electronically
- Contains invoice & delivery dates, invoice number, referenced logistical documents (ex. PO no. or sales order no.), list of invoice numbers, terms of payment, and bank details

1. Relevant data from invoice is entered manually.
	- **NOTE!** Logistics invoice verification does not include evaluation of payment or open liabilities (ex. when entering gross amount, VAT, etc.). These are tasks of financial accounting
	- Input the following:
		- Gross amount, invoice date, reference number
		- PO items (we use the PO no. for this one)
2. The system then proposes all relevant PO items. Suggested invoice items are compared with the supplier invoice, and values are corrected for quantity, amount, tax code if necessary.
3. The system also compares each supplier invoice item with the data it has of the related PO item. If there is a deviation outside defined tolerances, the invoice is posted but blocked until clarified
![[Pasted image 20260129115428.png]]

| Sample Invoice Receipt               |
| ------------------------------------ |
| ![[Pasted image 20260129115711.png]] |

