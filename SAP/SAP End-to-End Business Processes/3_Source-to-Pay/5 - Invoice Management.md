## SAP S4/HANA Sourcing and Procurement
- The SAP solution responsible for **invoice verification**

## Invoice Verification Environment
- Invoicing posting starts at **FI** (Finance)
- The invoice verification checks for accuracy during the *end of the logistics chain*
	- Information from this verification is then passed to FI and other systems.
- Additionally, invoices can **reference an existing PO[^PO], GR[^GR], or service entry** for its data.

[^PO]: Purchase Order
[^GR]: Goods Receipt
## Invoice Receipt
Can be received through the following methods:
- **Automated** by account programs
- **Ariba Network** (SAP's supplier network)
- **Electronically** through EDI[^EDI]; either through *IDoc*[^IDOC] or *XML*
- **Manually**
## Invoice Receipt Effects
- **Individual FI accounts** are updated (depending on items)
- **Two documents** are generated: one for **MM** and one for **FI** (accounting)
- **PO history** is updated
- Optionally, **Material Master** is updated

[^EDI]: Electronic data interchange
[^IDOC]: [Intermediate Document](https://en.wikipedia.org/wiki/IDoc) - the **file format** used by SAP for business transaction data transfers

> [!NOTE] Demos
> [How to Post an Invoice in Logistics Invoice Verification and Display FI Document](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_B96EBAA4FB5AB4AB:demo#2)