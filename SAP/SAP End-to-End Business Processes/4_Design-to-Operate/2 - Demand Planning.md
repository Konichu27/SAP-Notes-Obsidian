- **Demand planning** is usually handled by **SAP IBP** (Integrated Business Planning).

--- 
## SAP IBP Functions for Demand Planning

1. **Product Review** - Focuses on the product life-cycle, as well as code-changes and product/component replacements.
2. **Demand Review** - Finalizes the demand plan for S&OP[^S&OP], as well as generating demand scenarios
3. **Supply Review:** Assesses capacity, resources, and scaling
4. **Demand-Supply Balancing:** Develops the supply plan, as well as supply-demand scenarios and recommendations
5. **Executive Decision:** Decides on the cross-functional execution of S&OP[^S&OP]

[^S&OP]: Sales and Operations Planning

## SAP IBP for Demand
1. **Data Preparation:** Requires master & transactional data.
2. **Data Cleaning:** Removes outlier history data
	- *Examples of real-world outliers:* special events, stock-out situations
3. **Statistical Forecast:** Defines a "baseline" forecast, using the history as a time-series
4. **Demand Sensing:** Refines the forecast by adding more features, such as sales history or future promotions
5. **Market Input:** Further adjusts the forecast based on market intelligence
6. **Publish Forecast**

> [!NOTE] Finally
> Our data science degree is useful

---
## S/4HANA Integration

When you finish a Demand Plan in IBP, it is just a set of numbers in a cloud database. To make products, those numbers must be "pushed" into S/4HANA to become **Planned Independent Requirements (PIRs)**.
### Planned Independent Requirements
- Essentially a "placeholder" for demand in the warehouse.
- **The Trigger:** Once IBP data arrives in S/4HANA as a PIR, it acts as a formal "requirement for stock".
- **The Next Step:** This triggers **Material Requirements Planning (MRP)**, which looks at the PIR and says, "If IBP says we need 1,000 units in June, do I have enough raw materials to make them?".
### Demand Management
- **Planning Strategies:** Represent the business execution of demand management, usually in production plans or forecast adjustment.
	- [Planning Strategies | SAP Help Portal](https://help.sap.com/docs/SAP_ERP/74c0b3a391174482a66a3a23bb28c10d/ce22bf53d25ab64ce10000000a174cb4.html)
	- Ex. If a real customer order comes in, should it _reduce_ the IBP forecast (so you don't overproduce), or should it be _added_ on top?
- **Behavior:** The "Planning Strategy" determines if the PIR is just a suggestion or a hard command to start production immediately.

| **Feature**      | **SAP IBP (Planning)**                                        | **SAP S/4HANA (Execution)**                                            |
| ---------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Primary Goal** | Creating the most accurate forecast using statistical models. | Turning the forecast into Purchase Requisitions and Production Orders. |
| **Data Point**   | **Forecasting Result**.                                       | **Planned Independent Requirement (PIR)**.                             |
| **Key Process**  | Demand Sensing / Statistical Forecasting.                     | Material Requirements Planning (MRP).                                  |
| **Output**       | Consensus Demand Plan.                                        | Production/Purchase Orders for specific Work Centers.                  |