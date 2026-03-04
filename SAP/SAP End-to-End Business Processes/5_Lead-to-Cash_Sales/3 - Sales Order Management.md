# Sales Order

A sales order has the following characteristics:

- **Sales Area:** The sales order must have an associated sales area.
- **Customer & Material Data:** The sales order must have at least one customer & material number
- **Date Driven:** There is always a required *delivery date*
- **Available To Promise:** Materials are checked through a **Material Availability Check**. Products are confirmed or delivery is delayed, depending on the outcome
- **Meticulously Priced:** Sales orders have specific calculations, and only sales clerks can edit these
- **Referred From:** Data can be copied from previous sales orders.

Once saved, an **order confirmation** (receipt) can be sent to the customer.

--- 

# Sales Transaction

**Sales Transactions** are the core of the SAP system. They involve **documents** (which are the GR, GI, etc.)

Note that transactions and documents are the core of everything that happens in SAP.

![[Pasted image 20260302213322.png]]

---

# Sales Order Processing

The following are determined during **Sales Order Processing**:

- **Output:** The customer layout is defined.
- **Pricing:** Surcharges, discounts, freight, and taxes are also defined.
- **Partner Determination:** The following are mandatory *partner functions*:
	- **Sold-To-Party** -> *Places* -> **Order**.
    - **Ship-To-Party** -> *Receives* -> **Goods/Services**.
    - **Bill-To-party** -> *Receives* -> **Goods/Service Invoice**.
    - **Payer** -> *Pays* -> **Invoice**.
- **Availability Check:** Is it available for stock?
	- *Backorder Processing:* What happens when not available
- **Incompletion Log:** This covers incomplete data in the sales order.
- **Material Substitution:** This allows for changing of materials in the order.
- **Free Goods:** Bonus freebies for the order
- **Material Exclusion:** Excludes certain items from the customer.

# Sales Order Scheduled Lines

A sales order is grouped into **3 sections**:

- **Header**
- **Items**
- **Schedule Lines:** Delivery quantities, delivery dates of *each item*. Each item can have multiple schedule lines.

![[Pasted image 20260302214039.png]]

> [!ABSTRACT] Demo
> [Creating a Sales Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_90E7A1D527764290:demo#2)