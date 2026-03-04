# Service Order Creation

**Service orders** have a variety of templates based on what is provided. There are **4 different categories of services**:

| **Service Category**                              | **What do they do?**                      | **Example**                          |
| ------------------------------------------------- | ----------------------------------------- | ------------------------------------ |
| **Time-Based Recurring**                          | Triggered after a specific *time period*  | Every six months                     |
| **Performance-Based Recurring**                   | Triggered after a specific *target value* | After every 10,000 km                |
| **Condition-Based <u>Preventive</u> Maintenance** | Triggered after a specific *value range*  | When temperature is lower than -20°C |
| **<u>Predictive</u> Maintenance**                 | Triggered based on *real-time data*       | Machine learning, IoT                |
> [!WARNING]
> **<u>Preventive</u>** Maintenance is different from **<u>Predictive</u>** Maintenance!!!

---
# Service Order Template

![[Pasted image 20260303183512.png]]

Here, you can set up the default header and item data.

### Header Assignments
- **General Data:** Description, Employee Responsible, Service Employee Group
- **Processing Data:** Search Term, Status
- **Dates**
- **Notes**
### Item Assignments
- **Products:** Services, spare parts
- **Item Category:** Service items, service parts items, sales items
- **Service Type:** Weekend, etc.
- **Valuation Type:** Senior, etc.
- **Status**
- **Reference Objects**, e.g. pieces of equipment
- **Notes**

> [!ABSTRACT] Demo
> [How to Display a Service Order Template](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_33C77E8BB84031B1:demo#2)

---
# Service Order Creation Steps

| **Step**                             | **Role**                     | **Integration**            |
| ------------------------------------ | ---------------------------- | -------------------------- |
| **1. Create Service Order Template** | Service planner              | S/4 Service<br>MM          |
| **2. Create Maintenance Plan**       | Service planner              | S/4 Service<br>SD, MM, HCM |
| **3. Schedule Maintenance plan**     | Service planner              | S/4 Service<br>MM, HCM     |
| **4. Process Service Order**         | Service technician           | S/4 Service<br>FI, CO      |
| **5. Complete Service Order**        | Service planner / technician | S/4 Service<br>FI, CO      |
Create service order template -> Create maintenance plan -> Schedule maintenance plan -> Process service order -> Complete service order

### Elements of a Service Order
- **Service Order Template:** Defines services to be performed.
- **Maintenance Plan:** Created for the service contract.
- **Scheduling:** Calls up the service orders.
- **Service Order:** Automatically scheduled by the Maintenance Plan.
- **Completion:** Calculates the next planned date

---

# Maintenance Plan

![[Pasted image 20260303184044.png]]

- **Planning Data/Scheduling Data:** - Determines the cycle/service interval (ex. every 2 years, etc.) and call dates
- **Maintenance Items:** Consist of the main service order & contract data
- **Maintenance Call Objects** - Triggers the need for maintenance

> [!ABSTRACT]
> [How to Display a Maintenance Plan](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_50C196087893CBB3:demo#2)

## Maintenance Plan Scheduling

![[Pasted image 20260303184310.png]]

- **Start:** The basic initiation of a maintenance plan schedule.
- **New Start:** Performed if there is a mistake in the Start process.
- **Schedule:** Organizes the service orders, depending of past activity
- **Manual Call:** Manually triggers service orders if needed.

### Additional Info
- **Cycle Start:** The first date where the cycle of planned dates begins
- **Planned Date:** The date the service is scheduled to occur, based on the cycle
- **Call Date:** The date the system actually *generates* the service order.
	- Usually separate from the planned date to allow time for preprocessing (ex. material procurement, assignment of technician, etc.)

> [!ABSTRACT]
> [How to Schedule a Maintenance Plan](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_70911426EDD5DB2:demo#2)
