- The SAP system responsible for guaranteeing material availability...

> [!NOTE] **The Three Key Elements of MRP**
> 1. **In the right quantity**
> 2. **From the right source**
> 3. **At the right time**

---
## Automated Procurement Proposals

MRP doesn't just involve calculations. When it detects a shortage for a material, it doesn't just buy or build things immediately; instead, it creates **procurement proposals**. These are internal planning elements that can be adjusted or deleted if plans change.

Assume a shortage of Material A. Depending on how Material A is sourced, the system follows two main paths:

![[Pasted image 20260228210406.png]]

#### 1. In-House Production (5) 🏭
For items your company makes itself, the process starts with a **planned order (6)** to determine the necessary production quantity. Once the planning phase is finalized, this internal document is usually **converted into a production order (7)** to start the actual manufacturing.
#### 2. External Procurement (1)📦
For items bought from vendors, the system creates a **purchase requisition (2)**. Just like the in-house path, once planning is complete, this requisition is **converted into a purchase order (2)**.

Alternatively, if a **scheduling agreement (3)** exists for a material and is relevant for MRP in the source list, it can be created instead.

---
## MRP Steps

There are six different MRP steps:

### 1. **Define MRP Type, Planning Method**
- **MRP Type:** Also known as **planning method**, it is the kind of plan that your MRP will form its processes around.

There are two MRP types, **Deterministic Planning** and **Consumption-Based Planning**:

| **Feature**           | **Deterministic Planning 🎯**<br>(independent of requirements)                                                  | **Consumption-Based Planning 📈**<br>(dependent of requirements)                       |
| --------------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Primary Basis**     | Calculations are driven by future demand, such as specific customer orders or planned independent requirements. | Calculations are based on historical usage patterns or a simple drop in stock levels.  |
| **Calculation Scope** | **Multilevel:** It plans for the entire Bill of Material (BOM) structure (e.g., the bike and all its parts).    | **Single level:** It focuses on replenishing individual materials when stock gets low. |
| **Example MRP Types** | Often relies on requirement strategies for high-level control.                                                  | Includes **VB** (Reorder point), **VV** (Forecast-based), and **R1** (Time-based).     |
| **Typical Use Case**  | Best suited for high-value **"A" parts** where precise inventory control is critical.                           | Ideal for less critical or low-value **"B" and "C" parts** with steady demand.         |
Additionally, we also have **Reorder Point Planning**.
#### Reorder Point Planning
- A point defined by the MRP system in which it orders new stock (procurement proposal).
- It replenishes at exactly the right time, taking into consideration delivery/manufacturing time
- A **consumption-based planning** method

![[Pasted image 20260228214759.png]]

It is most useful when a material has the following characteristics:
- **Steady Demand:** The usage doesn't fluctuate wildly.
- **Reliable Supply:** You can count on getting more stock when you ask for it.
- **Known Lead Time:** You know exactly how long it takes for the supply to arrive.

### 2. **Calculate Net Requirements**
The system carries out a **net requirements calculation**, wherein it compares the available stock and incoming elements to the safety stock and the requirements.

### 3. **Calculate Quantity**
The system carries out a **quantity calculation**, where it also performs a lot sizing procedure (economic order quantity).

### 4. **Check Procurement Type**
The system checks the procurement type. The following codes are available:
- **E** - In-House Production
- **F** - External Production
- **X** - Both Procurement Types

### 5. **Scheduling**
The MRP system prepares to schedule its processes. It often performs this using **Backwards Scheduling**.
#### Backwards Scheduling
- A type of scheduling wherein processes are arranged by their end delivery date, not their starting date.
	- This optimizes resource allocation and storage time.
- The schedule is calculated during the **BOM explosion**. Each component's "start date" defines the "end dates" of the other subcomponents.

![[Pasted image 20260228221822.png]]

### 6. **Creating Purchase Requisitions**
The MRP system finally generates the **purchase requisitions** needed to start the production process.

If using **internal procurement/in-house production**, the following are considered for the order's start date:
- **Goods Receipt Processing Time**
- **In-House Production Time**
- **Opening Period** 

If using **external procurement**, the following are considered for the order's start date:
- **Processing Time for Purchasing**
- **Planned Delivery Time**


---
## Planning Run (S/4HANA)
- A **planning run** simulates the whole MRP process/steps for a product or products.
- This is usually done by **S/4HANA**, after the Planned Independent Requirements (PIR) are pre-planned by SAP IBP.

There are two levels within a planning run:
### A. Total Planning (Plant Level)
> This is the "Big Picture" run.
- **What it does:** It plans **every single material** assigned to a specific plant.
- **When to use:** Usually done as a **Background Job** overnight so that when planners arrive in the morning, all procurement suggestions are ready.
### B. Single-Item Planning (Material Level)
> This is the "Deep Dive" run.
There are two types of planning run structures here, in reference to the BOM levels:
- **Single-Level:** Only looks at the finished e-bike. It won't check if you have enough spokes for the wheels.
- **Multi-Level:** This is the most common for finished goods. It "explodes" the Bill of Materials (BOM). If you run it for the e-bike, it automatically calculates requirements for the battery, the frame, and the wheels too.

## MRP Live (S/4HANA)
- A type of real-time, optimized planning developed for S/4HANA.

| **Feature**   | **Classic MRP**                           | **MRP Live (S/4HANA)**                                                |
| ------------- | ----------------------------------------- | --------------------------------------------------------------------- |
| **Speed**     | Slower (reads data in batches).           | **Blazing Fast** (runs directly on the HANA database).                |
| **Data**      | Might use slightly older "snapshot" data. | **Real-Time.** It plans using the exact inventory levels _right now_. |
| **Frequency** | Usually once a day (nightly).             | Can be run **multiple times a day** because it's so fast.             |
