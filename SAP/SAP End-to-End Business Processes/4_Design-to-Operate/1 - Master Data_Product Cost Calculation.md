## Product/Material Master
- Consists of the following types:
### MRP Data

| **MRP Setting**              | **Defines...**                   |
| ---------------------------- | -------------------------------- |
| **MRP Type**                 | how to plan a material           |
| **Procurement Type**         | how to procure a material        |
| **Lot-Sizing Procedure**     | the lot-size procedure[^LSP]     |
| **Planning Strategy**        | how to handle requirements       |
| **In-House Production Time** | how long is in-house production  |
| **Planned Delivery Time**    | how long is external procurement |
| **Production Version**       | how production will occur        |
| **Advanced Planning**        | if PP/DS procedures will be used |
[^LSP]: **Lot-size procedures** - the calculation of procurement quantities as according to purchase order demand. Would be useful to recall EOQ from Operations Research 
## Components
### Product/Bills of Material (BOM)
- **BOM** - Bills of Material
- Contains the drill-down of materials needed for a specific product or products.
#### Parts of a BOM
| **Part**             | **Description**                                                                                           |
| -------------------- | --------------------------------------------------------------------------------------------------------- |
| **BOM Header**       | Contains settings that refer to the BOM's purposes                                                        |
| **Stock Item L**     | An item category. Already present in the warehouse; triggers a *reservation* in the production order      |
| **Non-Stock Item L** | An item category. Not present in the warehouse; triggers a *purchase requisition* in the production order |
| **Document Item D**  | An item category. Describes the production itself (usually as a design/construction diagram)              |
### Work Center
- Specific geographical location or functional unit in a plant where an operation or activity is performed.
- It defines "where" and "who" is doing the work.
- In D2O: used for *routings*, *networks*, and *inspection plans*.
#### Functional Integration
Work Centers are utilized across several SAP S/4HANA applications:
- **Production Planning (PP):** Routings
- **Project System (PS):** Networks
- **Quality Management (QM):** Inspection Plans
- **Enterprise Asset Management (EAM):** Maintenance Routings
#### Parts of a Work Center
| **Category**       | **Key Planning Questions & Data Points**                                                                                                                                                                                     |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Basic Data**     | **Which time elements are needed for planning?**<br><br>- **Production:** Requires Setup, Labor, and Machine time.<br>- **EAM:** Generally only requires Labor time.                                                         |
| **Default Values** | **Where should documents be printed?**<br><br>Defines the number of time confirmation slips and their destination. Also maintains the default **Control Key**.                                                               |
| **Capacities**     | **What capacities are used at this work center?**<br><br>Includes number of machines/persons and working hours.<br><br>- **Formula Driven:** Setup time is usually quantity-independent; machine time is quantity-dependent. |
| **Scheduling**     | **Which capacity category is relevant for scheduling?**<br><br>When multiple capacities exist (e.g., Machine and Labor), the system must define which one drives the schedule. **Only one can be relevant.**                 |
| **Costing**        | **Which costs arise during production?**<br><br>Links the Work Center to a **Cost Center**. Different **Activity Types** (Setup, Labor, Machine) are assigned to calculate internal processing costs.                        |

### Routing
- Describes the specific procedure and operations needed for a finished product.

> [!NOTE] Definition
> **Control Key:** a default value which defines how an operation should be processed.
> 
> More info: [Control Key - SAP Documentation](https://help.sap.com/doc/b183ce53118d4308e10000000a174cb4/700_SFIN3E%20006/en-US/90a1b8535c39b44ce10000000a174cb4.html)

#### Parts of Routing

| **Category**             | **Description**                                                                                                                                                                            |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Routing Header**       | Contains basic info such as relevant operations, their sequence, and work centers involved.                                                                                                |
| **Internal Control Key** | The work center is responsible for this section of the routing.<br><br>Creates a recording called a **Confirmation of Time**, which updates the system on progress and costs               |
| **External Control Key** | An *outside vendor* is responsible for this section of the routing.<br><br>Creates a **Purchase Requisition**, which acts as a formal request to buy the service from the external company |
### Product Cost Calculation
- Also known as the **Cost of Goods Manufactured (COGM)**
- **Controlling (CO)** is heavily involved here.
#### Product Lifecycle
Product Cost Planning isn't a one-time event; it evolves as a product moves from a simple idea to a finished good:

- **Product Idea Or Simulation:** 💡 Early on, projections are based on similar existing products to provide quick, flexible cost simulations.
- **Product Design & Specification:** At the product design and specification stage, costs can increase as refinements are made to original specifications.
- **Prototype Stage:** 🛠️ As a prototype develops, the first logistics data, like the **Bill of Material (BOM)**, is entered.
- **Market Maturity:** 🏗️ Once a product is ready for the market, integration with master data is critical. Costs are monitored at regular intervals to analyze any shifts.
- **Continuous Improvement:** 🔄 Any refinements to the production process are analyzed to see their impact on the overall cost.
### Quantity Structure

![[Pasted image 20260228202642.png]]
When all master data—specifically the **BOM** (list of parts) and **Routing** (steps for production)—is available, the system can create a **Material Cost Estimate with Quantity Structure**. This tool automatically calculates the **COGM (Cost of Goods Manufactured)** and the **Cost of Goods Sold (COGS)** using that real-world logistics data. The final result is often used to update the **Standard Price** in the product master record.
#### How the System Processes Costs
Instead of manually entering costs, the system automatically pulls from logistics and translates them into financial reports:
- **Costing Result**
- **Itemization:** A detailed list of every cost element (materials, internal activities, etc.) involved in the process.
- **Cost Component Report:** Breaks down the total cost into logical groups, such as raw materials, labor, and overhead.
- **Costed BOM:** Displays the hierarchical structure of the product with costs applied at each level.
#### Analysis and Error Handling
SAP S/4HANA provides a unified interface where you can view the costing results and detailed reports from a single screen.
- **Centralized Reporting:** You can execute detailed reports directly from the cost estimate screen to analyze cost shifts or production variances.
- **The Overall Log:** If something goes wrong (e.g., a missing price for a material), the log contains a complete list of messages for all costed materials.
- **Deep-Dive Troubleshooting:** You can double-click a specific material in the header or status display to see only the error messages related to that specific item.
### Prices
In this stage of the lifecycle, the goal is to translate your costing results into a "live" price that the system uses for inventory and accounting.
#### Price Elements in the Material Master
To set an accurate standard price, you need to understand how different prices interact within the **Product Master Record**:
- **Planned Prices (1, 2, and 3):** Used primarily for raw materials and purchased parts to provide a valuation basis for the cost estimate.
- **Tax-Based and Commercial Prices:** Required for inventory costing to determine values like "lowest value" for purchased parts.
- **Price Control Indicator:** Determines how inventory is valuated—either via **Standard Price (S)** or **Moving Average Price (V)**.
- **Standard Price:** This is the specific value updated by a **Standard Cost Estimate**. You can view these results directly from the Accounting or Costing views in the system.
#### The Two-Step Update Procedure
Updating the standard price is a controlled process to ensure financial accuracy:
##### Step 1: Marking
- **Action:** You mark the standard cost estimate for update.
- **Result:** The new price is written to the Product Master as the **Future Price**.
- **Impact:** There is **no impact** to Finance (FI) or Controlling (CO) at this stage.
##### Step 2: Releasing
- **Action:** You release the new valuation price.
- **Result:** The "Future Price" becomes the **Actual/Standard Price** in the accounting data.
- **Impact:**
    - **If stock exists:** The system performs a **revaluation of stock**, creating a financial impact in FI and CO.
    - **If no stock exists:** The price is updated, but there is no immediate financial posting.
