Recall:
## Production Order
- Defines which materials are to be produced in which quantity, time, and way
> Further info: [[2.2 - Production Execution]]

**Production orders** can be further defined by the steps they take. They start with a *Planned Independent Requirement (PIR)* or sales order, and end with the **Goods Receipt** and **financial settlement** of the finished product.

![[Pasted image 20260301191647.png]]

---
# Production Order Steps

## 1. **Order Creation**

> System Status: **CRTD**
### Parts of a Production Order
There are **7 parts** in a production order:
1. **Order Header:** General data
2. **Settlement Rules:** This is important for the financial step.
3. **Costs:** Wherein we go back to the *[[1.4.2 - Financial & Management Accounting#Management Accounting|cost object]]*
4. **Operation Sequences:** Define how each operation follows through
5. **Operations:** The main "meat" of the production order. Operations include *work centers*, *control keys*, *quantities*, *dates*, and standard *default values*.
6. **Material Components:** Each material component has an *item category*, *material number*, *quantity*, and *date*.
7. **Confirmations:** Involves the time associated with each operation
### Converting a Planned Order to a Production Order

A **planned order**, if you may recall, is a proposal created through an MRP system before an MRP run.

Planned orders can be converted into real production orders through **3 ways**:

1. **Collective Conversion:** Part of a batch in background processing
2. **Individual Conversion:** Inputted manually
3. **Partial Conversion:** Here, the planned order is still present so that it may be edited.

> [!NOTE] Demo
> [How to Convert a Planned Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_2373113EB2E3CF97:demo#2)
## 2. **Order Release**

> System Status: **REL**

In order for a production order to proceed, it must have the *Released* status.

> [!NOTE] Demo
> [How to Release a Production Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C56FA97EAA86DFAD:demo)
## 3. **Goods Issue (GI)**

A **goods issue (GI)** prompts the materials to be delivered for the production order.

There are **3 ways** to post a goods issue:

- **Picking List:** Pick directly from the warehouse
- **Goods Movement in Inventory Management:** Use SAP Fiori's *Goods Movement* app
- **Backflushing:** Automate materials deduction

#### Effects of Goods Issue
The following are affected after a goods issue:

- **Stock Quantity:** Issued in a *materials document*
- **Account Determination:** Determined automatically
- **G/L Accounts:** Involves the balance sheet account, stock accounts, etc.
- **Point of Consumption:** Associated with a *cost object* 
- **Goods Issue Slip:** Can be issued on request

> [!NOTE] Demo
> [How to Post Goods Issue for Production Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_A48E899A9C8CE38D:demo#2)

## 4. **Confirmation**

After the order release & goods issue, production orders must **confirm consumption elements**, including quantity and especially time.

There are **5 elements** of a confirmation:
1. **Capacity Requirements:** Open capacity requirements are reduced during confirmation.
2. **Material Documents:** The GR and GI are generated automatically.
3. **Confirmation Type:** The confirmation type can be either *automatic* or *manual*.
4. **Actual Costs:** The labor and machine costs are accounted for in both the work center and cost center.
5. **HR Data:** HCM can also be affected if personal master data is associated with the confirmation.
### Triggered Processes in a Confirmation

1. **Automatic Goods Receipt**
2. **Order**
    - *Status*
    - *Activities/Quantities*
    - *Actual Costs*
3. **HR Data Transfer**
4. **Backflush Goods Issue**
5. **Reduce Capacity Requirements**
6. **Actual Costs**

> [!NOTE] Demo
> [How to Post Confirmation of Time for Production Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_DE498AF135D537A7:demo#2)
## 5. **Goods Receipt (GR)**

The **goods receipt (GR)** is handled after production is complete. There are many different processes that are pushed following the goods receipt:
### Triggered Processes in a Goods Receipt

1. **Stock/Requirements list:** The production order is deleted in the stock/requirements list and in the product view.
2. **Stock Quantity:** The quantity in the storage location in inventory management is increased.
3. **Account Determination:** This takes place automatically using the MM account determination from the [[4 - Production Order to Fulfill#3. **Goods Issue (GI)**|Goods Issue step]].
4. **G/L Accounts:**
    - Stock Account: *Debited*
    - Plant Activity: *Credited*
5. **Order:**
    - Status
    - Quantity
    - Actual Costs: *Credited to the order*
6. **Material Document:** Material, accounting, and controlling documents are generated.
7. **EWM Inbound Delivery Order:** When you use EWM, you need to create an Inbound Delivery Order for put-away and processing the steps in the Warehouse.
8. **Goods Receipt Slip:** The Goods Receipt is posted with *Movement Type 101*. A movement type is always necessary when posting goods movements.

> [!NOTE] Demo
> [How to Post Goods Receipt for Production Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_13C034709238F8A9:demo#2)

---
# Technical Completion

> System Status: **TECO** (technical completed)

After a production order is set to TECO, **it is closed**. It cannot be edited any longer.

> [!NOTE] Demo
> [How to Set Technical Completion to a Production Order](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_D4EA4A24FE4EB7B2:demo#2)

