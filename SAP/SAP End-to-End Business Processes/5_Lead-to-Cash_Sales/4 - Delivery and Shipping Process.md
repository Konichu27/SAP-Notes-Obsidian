# Outbound Deliveries

![[Pasted image 20260302215352.png]]
Sales Order -> Outbound Delivery -> Warehouse

1. **Sales Order**
	- Shipping Point Determination
    - Route Determination
    - Scheduling
2. **Outbound Delivery:** Determined by a shipping point.
	- **Shipping Point:** Highest-level unit of shipping. Should be at the *plant level*
3. **Warehouse Execution:** EWM system is finally involved.

## Additional Info
- There can be **more than one outbound delivery**.
- There can be **more than one item** in a single delivery, however they must have these same characteristics:
	- **Shipping point**
	- **Due date**
	- **Ship-to address**
- Delivery can either be **online** or a **background job** (executed during off-peak hours)

---
# Shipping Process

![[Pasted image 20260302215559.png]]
Order Document -> Delivery Transaction -> Delivery Document -> Delivery Note 

> [!NOTE] Note
> - Shipping point cannot be changed in the outbound delivery.
> - **Backorder**: When a sales order cannot be confirmed

---

# Picking
- Associated with the **picking list**

![[Pasted image 20260302215833.png]]

**Sales/Delivery Processing**
- Sales Order -> Outbound Delivery
**Extended Warehouse Management**
- -> Outbound Delivery Order -> Post Goods Issue

### List of Warehouse Tasks
- Picking
- Putaway
- Internal Movements
- Posting Changes
- Goods Receipt Postings
- Goods Issue Postings

![[Pasted image 20260302220021.png]]

Delivery Quantity <-> Pick Quantity -> Warehouse Tasks

**Delivery Quantity** is in **Shipping Point**, **Pick Quantity** is in the **Outbound Delivery** Order under the **Warehouse Number**.

---

# Post Goods Issue

![[Pasted image 20260302220157.png]]

Stock and Requirements -> Accounting Document -> Controlling Document -> Billing Due List -> Material Ledger -> Document Flow

1. **Stock and Requirements:** Material document removes the confirmed stock from the S&R list.
2. **Accounting Document:** Balance sheet is updated, along with the P&L accordingly.
3. **Controlling Document:** Breakdown of cost of goods
4. **Billing Due List:** Invoicing is now available here
5. **Material Ledger:** Goods movement, material valuation
6. **Document Flow:** As seen in SAP Sales Cloud / S/4HANA Sales