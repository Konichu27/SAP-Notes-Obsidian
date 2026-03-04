# Understanding the Basics of the Production Process

Objective

After completing this lesson, you will be able to describe the production process and the systems used in production

## Introduction

**Scenario:** The implementation project of the bike company in our example is currently in the _Realization_ phase and the end-to-end processes are tested by the project team.

Based on the best practice scope items, the team created a summary of the business process for the production. The following graphic provides a high-level overview of the included business process steps.

![This diagram illustrates the Design-to-Operate process, highlighting key stages: master data and product cost calculation (including product/BOM, workcenter/routing, and cost calculation), demand planning (forecasting, sales and operations planning, and demand management), procure-to-receipt (material requirements planning), production order to fulfill (order processing and period-end closing), and reporting.](https://learning.sap.com/service/media/topic/faefd808-6189-4289-ae6d-6028a1997246/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate_Overview.png "This diagram illustrates the Design-to-Operate process, highlighting key stages: master data and product cost calculation (including product/BOM, workcenter/routing, and cost calculation), demand planning (forecasting, sales and operations planning, and demand management), procure-to-receipt (material requirements planning), production order to fulfill (order processing and period-end closing), and reporting.")

- **Master Data / Product Cost Calculation:** As with all areas, you need to define and handle master data - data that is kept for a longer period. As master data you treat work centers, materials, routings, bill of materials and more.
    
- **Demand Planning:** Based on the sales figures from the past, you will create a demand plan for the future. Planning can be done on a long-term basis in Sales and Operations Planning, or in a midterm basis in Demand Management. Planning can be undertaken in SAP IBP or SAP S/4HANA.
    
- **Procure to Receipt:** Based on the materials requirements planning, you will initiate the processing of the internal and external procurement. For both of the procurement types, you need to post a goods receipt.
    
- **Production Order to Fulfill:** After you generated planned orders for the internal procurement, you need to analyze the individual steps to be processes in the production department. These steps are needed to produce your semi-finished and finished products.
    
- **Reporting:** Using the entirety of production processing, you will have a look at the analytics possibilities.
    

Having a look on the SAP solution, we are now here:

![This diagram outlines the SAP solution landscape for production, emphasizing the role of SAP IBP (Integrated Business Planning) and the Production Planning (PP) module within SAP S/4HANA. It situates these components within the broader SAP ecosystem, which includes solutions like SAP Analytics Cloud, SAP SuccessFactors, SAP Ariba, SAP Intelligent Asset Management, and SAP CX, all connected through the SAP Business Technology Platform. The PP module is highlighted as part of SAP S/4HANA's suite, alongside other modules such as FI (Finance), CO (Controlling), HCM (Human Capital Management), MM (Materials Management), EWM (Extended Warehouse Management), SD (Sales and Distribution), CS (Customer Service), and EAM (Enterprise Asset Management).](https://learning.sap.com/service/media/topic/faefd808-6189-4289-ae6d-6028a1997246/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation_4.png "This diagram outlines the SAP solution landscape for production, emphasizing the role of SAP IBP (Integrated Business Planning) and the Production Planning (PP) module within SAP S/4HANA. It situates these components within the broader SAP ecosystem, which includes solutions like SAP Analytics Cloud, SAP SuccessFactors, SAP Ariba, SAP Intelligent Asset Management, and SAP CX, all connected through the SAP Business Technology Platform. The PP module is highlighted as part of SAP S/4HANA's suite, alongside other modules such as FI (Finance), CO (Controlling), HCM (Human Capital Management), MM (Materials Management), EWM (Extended Warehouse Management), SD (Sales and Distribution), CS (Customer Service), and EAM (Enterprise Asset Management).")

In addition to the **Product Planning (PP)** in SAP S/4HANA you can use production planning functionalities in**SAP Integrated Business Planning (IBP)**.

## Overview of SAP Integrated Business Planning (IBP)

Originally the entire production process took place in the SAP S/4HANA module PP (Production Planning). Now there is functionality from the planning aspect that can be covered in SAP IBP.

SAP IBP enables an organization to bring all its Sales and Operations Planning processes together under one roof using the same data set: Reporting, Planning, and Executing.

SAP IBP is a completely scalable solution with a unified data model. It offers simplified data integration to and from SAP IBP with an easy implemented concept via Microsoft Excel and the web-based user interfaces. It offers easy collaboration within and between internal groups such as those created by demand and supply planners, finance team members, and sales relevant employees. It provides what-if scenario capabilities and real-time analytics to show the status of the key performance indicators of a supply chain at any given time.

The SAP IBP landscape includes the components illustrated in the graphic below.

![This diagram highlights the key components of SAP Integrated Business Planning (IBP), including SAP Supply Chain Control Tower for exception handling and collaboration, Sales and Operations Planning for strategic and tactical decisions, Demand for forecasting and planning, Inventory for multi-stage optimization, Response and Supply for supply planning and order scheduling, and Demand-driven replenishment for material requirements planning (DDMRP).](https://learning.sap.com/service/media/topic/eb8afcd6-f6c7-4f7e-8650-256721bd3236/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP%20IBP.png "This diagram highlights the key components of SAP Integrated Business Planning (IBP), including SAP Supply Chain Control Tower for exception handling and collaboration, Sales and Operations Planning for strategic and tactical decisions, Demand for forecasting and planning, Inventory for multi-stage optimization, Response and Supply for supply planning and order scheduling, and Demand-driven replenishment for material requirements planning (DDMRP).")

- **SAP Supply Chain Control Tower:** Several components of SAP Supply Chain Control Tower cover the tasks for end-to-end visibility, exception handling, and performance management:
    
    - Analyze Key Performance Indicators (KPIs)
    - Check Alerts
    - Manage Cases and Tasks
- **Sales and Operations Planning** includes strategic and tactical decision processes.
    
- **Demand** covers statistical forecasting, consensus planning, and demand sensing.
    
- **Inventory**: Multi-stage Inventory Optimization SAP IBP for inventory includes the following process steps:
    
    - Validate Data Inputs
    - Run and Review Inventory Plan
    - What-if Analysis Approve and Update Inventory Plan
- **Response and Supply:** The SAP IBP for response and supply process includes the following steps:
    
    - Capture Inputs
    - Sequence Demand by Priority
    - Constrained Planning Run
    - Scenario Planning
    - Finalize Supply/Response Plan
- Demand-driven replenishment: Material Requirements Planning (DDMRP) is a fundamental part of the SAP IBP modules as well, constructing the entire SAP IBP landscape.
    
    The SAP IBP for demand-driven replenishment application has the following capabilities: SAP IBP for demand-driven replenishment supports a methodology known as Demand-Driven MRP or simply DDMRP that re-defines the way we think and behave in Supply Chain Planning
    

## SAP S/4HANA

When we look to the planning steps from Controlling, we see that there are two possible steps that could be processed in SAP S/4HANA from the perspective of Planning for Production: Sales and Operations Planning (SOP) and Demand Management.

![This diagram illustrates the integration between Sales, Production, and Controlling processes in SAP. Sales includes Sales Planning and Profit Planning, which connect to Production processes like Sales and Operations Planning, Demand Management (via SAP IBP), and Production Planning (via SAP S/4HANA). Controlling involves Cost Center and Activity Type management, which links to Material Cost Estimates and integrates with both Sales and Production for cost and profit analysis.](https://learning.sap.com/service/media/topic/cae6c6ba-31f5-48d9-92e9-4c99de82051b/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Planning%20Cycle_Production.png "This diagram illustrates the integration between Sales, Production, and Controlling processes in SAP. Sales includes Sales Planning and Profit Planning, which connect to Production processes like Sales and Operations Planning, Demand Management (via SAP IBP), and Production Planning (via SAP S/4HANA). Controlling involves Cost Center and Activity Type management, which links to Material Cost Estimates and integrates with both Sales and Production for cost and profit analysis.")

We will process these steps in IBP and hand over the planning result to SAP S/4HANA.

**SAP IBP for Sales & Operations Planning (SAP IBP S&OP)** is the post-recession business planning process. It extends the principles of S&OP to the entire supply chain, product and customer portfolio, customer demand and strategic planning to deliver a seamless management process.

**SAP IBP for Demand Management** provides the functionality to introduce new products. With this functionality, the sales history for one or more products with similar demand can be simulated and then a dynamic forecast for the new product is created.

# Managing Master Data and Product Cost Calculation

Objective

After completing this lesson, you will be able to describe the necessary steps for Product Cost Calculation

## Introduction

The scope items within in the design-to-operate process that are covered in this lesson are highlighted in the graphic below.

![The image provides an overview of the Design-to-Operate business process, visually highlighting its five key phases: Master Data and Product Cost Calculation, Demand Planning, Procure to Receipt, Production Order to Fulfill, and Reporting. The focus is currently on the first phase, Master Data and Product Cost Calculation, which includes defining Product/BOM (bill of materials), Workcenter/Routing (manufacturing processes), and performing Product Cost Calculation.](https://learning.sap.com/service/media/topic/a46dc9ac-996a-4150-9ca9-a1b7abba7150/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate_1.png "The image provides an overview of the Design-to-Operate business process, visually highlighting its five key phases: Master Data and Product Cost Calculation, Demand Planning, Procure to Receipt, Production Order to Fulfill, and Reporting. The focus is currently on the first phase, Master Data and Product Cost Calculation, which includes defining Product/BOM (bill of materials), Workcenter/Routing (manufacturing processes), and performing Product Cost Calculation.")

Supply chain planning deals with materials, which are defined in the form of material masters. For the plants used for production, you must also create work centers, BOMs (Bill of Material) and routings in addition to the materials to support planning tasks.

Plants, distribution centers (DCs), vendors, and customers are basic logistics objects for supply chain planning.

## Product Master Record (Material Master Record)

The **product or material master** is divided into different areas or departments.

A newly finished product is created with the material type "finished product" and includes data from production. Material Requirements Planning (MRP) data and work scheduling data are relevant for production for pre-planning.

- **MRP Data**: The settings for supply chain planning are mainly found in the Material Requirements Planning (MRP) and Advanced Planning views as, for example, you find as one of the following:
    
    - MRP type: Defines how to plan a material: Material requirements planning versus consumption-based planning, external planning, or no planning.
    - Procurement type: Defines how to procure a material: In-house, externally, or no procurement.
    - Lot-sizing procedure: Defines in which lot size procedure to bundle the receipts: Static, periodical, optimizing.
    - Planning strategy: Defines how to handle independent requirements and their interactions.
    - In-house production time: Defines how long in-house production is assumed to last.
    - Planned delivery time: Defines how long external procurement is assumed to last.
    - Production version: Defines how production is going to take place.
    - Advanced Planning: Defines that this material will be planned with PP/DS procedures.
- **Work Scheduling Data:** In the work scheduling data, you maintain a production supervisor (responsible person for production) and lot-size dependent inhouse production data scheduled via the routing.
    

## How to Display a Finished Product

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_49D4D19F6FF9F29E:demo)

## Master Data - BOM

The Bills of Material (BOMs) contain the assemblies or components that are involved in the production of a material. They are one necessary component for the Product Master Record.

The following graphic shows the elements integrated in a BOM.

![The diagram illustrates the relationship between the Product Master for a finished product and its associated Bill of Materials (BOM) structure. It demonstrates how the BOM header connects to individual items, categorized into four primary types: Stock Items (e.g., L), Non-Stock Items (e.g., N), and Document Items (e.g., D). Detailed explanations for categories 1 through 4 are provided in the text below.](https://learning.sap.com/service/media/topic/ead14854-1a87-4a65-84bd-e0e541ae53a2/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_BOM.png "The diagram illustrates the relationship between the Product Master for a finished product and its associated Bill of Materials (BOM) structure. It demonstrates how the BOM header connects to individual items, categorized into four primary types: Stock Items (e.g., L), Non-Stock Items (e.g., N), and Document Items (e.g., D). Detailed explanations for categories 1 through 4 are provided in the text below.")

1. **BOM:** The BOM header contains the settings that apply for the whole BOM. BOM usage determines the business applications for which a BOM can be used. The status of the BOM controls whether the BOM is active for particular applications (for example, Material Requirements Planning (MRP)). Multiple BOMs, which consist of multiple alternative BOMs, can also exist in addition to simple BOMs. The different alternative BOMs can then be valid for each of the different lot-size areas, for example.
    
2. **Stock Item L:** The components required to produce the finished product are entered as items in the BOM. The item category specifies the kind of item you are dealing with: Stock items are executed in the warehouse and are used in production. For stock items the system generates in the production order a reservation.
    
3. **Non-Stock Item L:** The components required to produce the finished product are entered as items in the BOM. The item category specifies the kind of item you are dealing with: Non-stock items are directly assigned to a manufacturing order (and not via the warehouse). For Non-stock items, the system generates in the production order a purchase requisition to initiate the procurement process.
    
4. **Document Item D:** The components required to produce the finished product are entered as items in the BOM. The item category specifies the kind of item you are dealing with: Document items contain a supplementary document that describes production (a kind of design and construction diagram).
    
    The individual items can also contain many other settings that only refer to that particular item.
    

## How to Change a Bill Of Material

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_BDEA911219904FA3:demo)

## Master Data - Work Center

Let’s move on to Work Centers, another component for the Product Master Record.

Work Centers are used in the following applications:

- Routings (Production Planning)
- Networks (Project System)
- Inspection plans (Quality Management)
- Maintenance routings (Enterprise Asset Management)

A work center is generally a specific geographical location in the plant. For example, a specific machine or department in a plant.

As we also need to define "who" is doing the work, we need to create work centers. A work center in SAP S/4HANA could be a person, a group of persons, a machine, a group of machines or the combination of both.

A work center is where an operation or an activity is carried out in a plant. It therefore specifies where production ultimately takes place.

![The image outlines key considerations for the configuration and planning of production processes, broken down into five sections: Basic Data, Default Values, Capacities, Scheduling, and Costing. Each section explains foundational aspects such as the time elements required in production (Basic Data), where and how to print documents (Default Values), the capacity requirements at work centers (Capacities), relevant capacity categories for scheduling (Scheduling), and the allocation and calculation of costs during production (Costing).](https://learning.sap.com/service/media/topic/daba52df-dd8b-4080-9c0d-2ff7052dec2f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L3_Master_Data_Work_Center.png "The image outlines key considerations for the configuration and planning of production processes, broken down into five sections: Basic Data, Default Values, Capacities, Scheduling, and Costing. Each section explains foundational aspects such as the time elements required in production (Basic Data), where and how to print documents (Default Values), the capacity requirements at work centers (Capacities), relevant capacity categories for scheduling (Scheduling), and the allocation and calculation of costs during production (Costing).")

### Work Center Capacities

The available capacity of the work center and the data needed to calculate the costing of work completed is stored in the work center. The default values define data that has to be transferred into the operation of the routing or are used as a reference.

The capacities that are available to a work center are explicitly specified in the work center. In this case, you may certainly use more than one capacity for each work center. For example, you can assign both machine capacity and labor capacity to a work center.

Work Centers contain the available working time. Moreover, formulas specify how long the capacities will be loaded by a certain operation.

### Work Center Costing

Since the work center provides working time, it also generates internal costs for labor. To calculate the costs, the work center is assigned to a cost center. As we have heard in the Controlling section, a cost center provides different output. This output is named activity type. To differentiate labor processing time, machine time, and setup time related to different costing rates, we assign the different activity types to the work center in the costing tab.

## How to Display a Work Center

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_D384FD16E705F9BA:demo)

## Master Data - Routing

As the BOM, Routing is another component of the Product Master Record. See the elements in the graphic below.

![The diagram represents the integration between the Bill of Materials (BOM) and Routing for a finished product in production planning. It shows the BOM structure with items categorized as Stock Items (e.g., L), Non-Stock Items (e.g., N), and Document Items (e.g., D), alongside the Routing that defines the sequence of operations. The control key differentiates between internal and external operations. Details for elements 1 (Routing Header), 2 (Internal), and 3 (External) are provided in the accompanying text below.](https://learning.sap.com/service/media/topic/d490d5fe-ede8-4d53-bb31-b689577f4acd/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_MasterDataRouting.png "The diagram represents the integration between the Bill of Materials (BOM) and Routing for a finished product in production planning. It shows the BOM structure with items categorized as Stock Items (e.g., L), Non-Stock Items (e.g., N), and Document Items (e.g., D), alongside the Routing that defines the sequence of operations. The control key differentiates between internal and external operations. Details for elements 1 (Routing Header), 2 (Internal), and 3 (External) are provided in the accompanying text below.")

1. **Routing:** The routing header is for the finished product. In routing, the following information is included:
    
    - Relevant operations
    - Sequence in which the operations occur
    - Work centers at which the operations are to be executed
2. **Internal:** Operations describing the individual steps to be carried out during production can be processed internally or externally. This is controlled by the control key in the operation: While defining an internal processed operation, the work center will perform that task. As a following on step later in the production order you should confirm the time worked for the operation. That is called a _confirmation of time_.
    
3. **External:** Operations describing the individual steps to be carried out during production can be processed internally or externally. This is controlled by the control key in the operation: When we need an external company to provide a particular work - for example, a quality check provided from an external auditing company - we use a control key for external processing. In this case, the system will generate it in the production order as a follow-on step a purchase requisition to initiate the procurement process.
    

## How to Change a Routing​

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_22E39F90C92EDC8E:demo)

## Product Cost Planning Overview

Let us now have a closer look at how to calculate our costs of goods manufactured (COGM).

This will lead us again to Controlling because the calculation of product costs is part of **Product Cost Calculation.**

Product cost planning assists employees in operational decision making for manufactured products by providing the following detailed information:

- Cost of goods manufactured, and the cost of goods sold
- Calculation of the break-even price for the product
- Comparison of production cost in large versus small lot sizes
- Production cost breakdown and comparison, for example, material costs and wages
- Optimization of the production process
- Production cost by organizational unit
- Manufacturing cost by plant
- Effect of primary costs on production costs

In the SAP S/4HANA application, materials can be valuated with a standard price, which can be set by a standard cost estimate.

Identify the product cost calculation along the product lifecycle in the graphic below.

![The diagram outlines the cost lifecycle associated with a product, aligned with its different stages in the Product Lifecycle Cockpit. It highlights key costing phases, including Preliminary Cost Estimate, Standard Cost Estimate, Inventory Cost Estimate, Modified Cost Estimate, and Current Cost Estimate, all of which relate to the material costing process. The timeline portrays the evolution of a product from the Idea stage to the Decline stage, with key milestones like First Prototype, Market Readiness, Saturation, and Technical or Ad Hoc changes.](https://learning.sap.com/service/media/topic/b04fcb86-9d83-4747-9691-911fd0e9500f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L3_PCPlanning_Overview.png "The diagram outlines the cost lifecycle associated with a product, aligned with its different stages in the Product Lifecycle Cockpit. It highlights key costing phases, including Preliminary Cost Estimate, Standard Cost Estimate, Inventory Cost Estimate, Modified Cost Estimate, and Current Cost Estimate, all of which relate to the material costing process. The timeline portrays the evolution of a product from the Idea stage to the Decline stage, with key milestones like First Prototype, Market Readiness, Saturation, and Technical or Ad Hoc changes.")

The different stages of the **product lifecycle** are as follows:

- **Product idea or simulation:** At the start of the product lifecycle, Product Cost Planning is used to provide initial cost projections. The projections, which are usually based on existing similar products or structures, must be delivered quickly. These projections must be flexible and variable to accommodate the simulated cost projections.
    
- **Product design and specification:** At the product design and specification stage, costs can increase as refinements are made to original specifications.
    
- **Prototype of new product** After transition to the prototype stage, the first constructive data can be entered in the form of a bill of material (BOM). During this phase, the need for integration and direct access to data in logistics increases. The person responsible for Product Cost Planning creates the data missing from logistics.
    
- **Market maturity of product:** After products attain market maturity, the integration of master data for tangible goods has a significant impact. At this stage the cost of the product or product range is monitored periodically at regular intervals and cost shifts are analyzed.
    
- **Continuous improvement:** Improvements in the production process of important products must be reflected by and analyzed in Product Cost Planning.
    

When the complete master data (BOM and routing) is available in the system, you can create a material cost estimate with a quantity structure, which automatically calculates the cost of goods manufactured and the cost of goods sold from existing data in logistics, such as BOM and routing.

Now that you have all the required master data for a material cost estimate with a quantity structure, you might want to see the impact of this calculation:

1. First, you will calculate our COGM (Costs Of Goods Manufactured)
2. Second, you will update our standard price in the product master

## Material Cost Estimate with Quantity Structure

Explore the graphic below to learn how the material cost estimate with quantity structure is mapped in SAP S/4HANA.

![The diagram illustrates the workflow of the Product Cost Estimate process, integrating the Bill of Material (BOM) and Routing to calculate costing results. The BOM provides the quantity structure and materials required, while Routing defines operational steps and associated costs. The costing results are organized into Header Data, including Master Data, Valuation, Quantity Structure, History, and Costs, which are further summarized in a report. The process links production planning data to cost analysis.](https://learning.sap.com/service/media/topic/b8eaa279-c43c-49fa-900b-3bf72906fc10/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L3_Material_Cost_Estimate.png "The diagram illustrates the workflow of the Product Cost Estimate process, integrating the Bill of Material (BOM) and Routing to calculate costing results. The BOM provides the quantity structure and materials required, while Routing defines operational steps and associated costs. The costing results are organized into Header Data, including Master Data, Valuation, Quantity Structure, History, and Costs, which are further summarized in a report. The process links production planning data to cost analysis.")

The results of a cost estimate created with quantity structure are identical to the results of a cost estimate created without quantity structure. The only difference is the origin of the information. The usual valuation principles also apply here. The term quantity structure refers to the use of production master data, such as BOM and routing.

It is only the method by which you obtain the costing results that differs. Material costing with quantity structure can determine the product structure and production plans as entered in logistics and convert them to structures of the itemization and the cost component split.

The costing result, itemization, cost component report, and costed BOM are visible from a single screen. You can execute detailed reports directly from the cost estimate screen. Overall log contains the complete list of messages for all the materials costed. It contains display variants (which you can customize) that enable you to perform summarized analysis of the errors. Double-clicking on the material in the header of a cost estimate or in the status display displays the messages specific to the particular material.

## How to Create a Material Cost Estimate

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_1181CA2E8F7A47A6:demo)

## Master Data - Prices

**Scenario:** The prototype of your new product has been successful, and production is to commence shortly. You need to calculate and set an accurate initial standard price. You must make all the settings required for valuation and use the correct quantity structure. For this reason, you require the following knowledge:

- An understanding of prices in material master
- An understanding of the procedure to update the standard price

Read the dialogue between two controlling colleagues below to learn more about creating and updating prices in the material master.

![The image illustrates the Design-to-Operate process in SAP S/4HANA, focusing on how to set prices in the material master, with Product Cost Calculation highlighted as a key step in the Master Data phase.](https://learning.sap.com/service/media/topic/bfbb531d-e27e-4e08-a289-1b8355ec0c49/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Dialogue_3.png "The image illustrates the Design-to-Operate process in SAP S/4HANA, focusing on how to set prices in the material master, with Product Cost Calculation highlighted as a key step in the Master Data phase.")

- **Liu:** John, now that we have done a calculation of our new product, what do you think the impact to our existing product master record will be?
- **John:** Based on what I know, we will need to set the standard price in the _Product Master Record_ based on our calculation.
- **Liu:** Ok. I do not exactly remember the elements for the prices in material master, can we please recapitulate that before?
- **John:** Sure.

John explains that the prices in the material master include the following elements:

- **Planned prices 1,2, and 3:** These elements are used for raw materials and purchased parts and to evaluate the materials in the cost estimate.
- **Tax-based and commercial prices:** They must be entered for purchased parts in inventory costing to determine values such as lowest value. An inventory cost estimate can use these prices for valuation, and then update the costing results for finished and semi-finished products in the material master.
- **Price control:** This is an indicator that controls which price is used to evaluate the inventory of a material. The available options are standard price and moving average price. These prices are used to valuate goods movements within the SAP S/4HANA application and to valuate inventories.
- **Standard price:** A standard cost estimate is used to update the standard price. You can branch from the accounting and costing views to the results of standard cost estimates. These results update the standard price.

Liu is now ready to update the standard price in the product master.

- **Liu:** Thanks a lot, John. Let us update the price, now.
- **John:** You need 2 steps to do so. First, you mark the standard cost estimate for update. The new valuation price is written in the product master as future price.
- **Liu:** Ok. I assume there is no impact to Finance or Controlling in this step, correct?
- **John:** Correct... Second, you release the new valuation price. Now the future price is written in the actual price and the standard price in the accounting data is updated.
- **Liu:** Ok. If there is stock available, a revaluation of the stock would take place and there would be an impact to Finance and Controlling, right?
- **John:** Correct. But as we currently have no stock available, there will be no impact to FI and CO.
- **Liu:** Ok. Thanks for your help!

## How to Release a Standard Cost Estimate

Demo[  
](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_86FDFF625C7258C:demo)

# Analyzing Demand Planning

Objective

After completing this lesson, you will be able to explain the use of demand planning and planning in SAP IBP

## Introduction

In this lesson, we focus on the business process **Demand Planning** in SAP S/4 HANA and discuss possibilities for integrating SAP IBP to perform the demand planning in SAP IBP as well. The process steps are highlighted in the overview below.

![The image illustrates the Design-to-Operate process in SAP S/4HANA and highlights the Demand Planning phase, specifically focusing on Forecast, Sales & Operations Planning, and Demand Management as key steps.](https://learning.sap.com/service/media/topic/e8ef7633-6c02-4a50-b1ce-72039da28cfa/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate_3.png "The image illustrates the Design-to-Operate process in SAP S/4HANA and highlights the Demand Planning phase, specifically focusing on Forecast, Sales & Operations Planning, and Demand Management as key steps.")

Let us start with planning possibilities in IBP and how this can be used for planning in poduction.

## Demand Planning in SAP Integrated Business Planning (IBP)

**Scenario:** You have covered the necessary master data and start now with the planning of your future production. The result of the IBP Planning will be used for the further processing in PP.

The possibilities provided for the initial planning steps in SAP IBP are summarized below. The following picture highlights the SAP IBP functions for Sales and Operations.

![The image focuses on SAP IBP for Sales and Operations, highlighting the key processes involved: Product Review, Demand Review, Supply Review, Demand-Supply Balancing, and Executive Decision, within the context of strategic and tactical decision-making.](https://learning.sap.com/service/media/topic/c29d0195-783f-491d-9483-8a7aff539fe4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP%20IBP_SandO.png "The image focuses on SAP IBP for Sales and Operations, highlighting the key processes involved: Product Review, Demand Review, Supply Review, Demand-Supply Balancing, and Executive Decision, within the context of strategic and tactical decision-making.")

1. **Product Review**
    - Plan for product life-cycle (new product ramp-ups, old product phase-downs)
    - Plan for code-changes, product and component replacements, and so on
2. **Demand Review**
    - Finalize the consensus demand plan to be used as the starting point for the Sales and Operations Planning processes (unconstrained demand)
    - Generate demand scenarios relevant for the Sales and Operations Planning processes (for example, expected, high, low or event-based scenarios)
3. **Supply Review**
    - Review critical resources against demand
    - Assess capacity scaling options
4. **Demand-Supply Balancing**
    - Develop initial feasible supply plan
    - Develop what-if scenarios for breaching supply-demand gaps
    - Analyze scenarios and financial impacts
    - Prepare recommendations for executive meeting
5. **Executive Decision**
    - Run a structured Sales and Operations Planning meeting with cross-functional representatives
    - Decide on the plan to follow
    - Hand over the decisions to execution

The SAP IBP functionalities for Demand are highlighted in the picture below.

![The image highlights SAP IBP for Demand, focusing on key processes such as Data Preparation, Data Cleaning, Statistical Forecast, Demand Sensing, Market Input, and Publish Forecast, within the context of statistical forecasting, consensus planning, and demand sensing.](https://learning.sap.com/service/media/topic/c29d0195-783f-491d-9483-8a7aff539fe4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP%20IBP_Demand.png "The image highlights SAP IBP for Demand, focusing on key processes such as Data Preparation, Data Cleaning, Statistical Forecast, Demand Sensing, Market Input, and Publish Forecast, within the context of statistical forecasting, consensus planning, and demand sensing.")

1. **Data Preparation:** Ensure all required master and transactional data is maintained and available.
    
2. **Data Cleaning:** Remove the outliers from the history data that are likely to derail or skew the Statistical Forecasting algorithm resulting in a weaker forecast (for example, special events not expected to repeat, stock-out situations, and so on.
    
3. **Statistical Forecast:** Generate a base line demand forecast by applying statistical algorithms to historical demand time series.
    
4. **Demand Sensing:** Apply more advanced pattern recognition methods and forecasting based on multiple inputs (for example, sales history and planned promotions) to improve accuracy of the short-term forecast.
    
5. **Market Input:** Adjust the statistically generated forecasts based on the latest market intelligence and knowledge of the future. This input is usually collected from sales and marketing.
    
6. **Publish Forecast :** Finalize and make the demand forecast available for the organization and other processes.
    

## Integration to SAP S/4HANA

**Scenario:** When the planning has been done in SAP IBP, the planning data is transferred to SAP S/4 HANA in the planning. Here you define planned independent requirements as a requirement for stock. This demand will be analyzed by the short-term planning the Material Requirements Planning (MRP) and will generate during the planning run the necessary input for production.

Alternatively, you could do the entire planning for SOP and DM as well as SAP S/4 HANA. Explore the graphic below to get a short overview about the possibilities.

![The image depicts the integration between SAP Integrated Business Planning (IBP) and SAP S/4HANA to streamline processes from demand forecasting to production planning. It shows how IBP (using modules like IBP for S&OP and IBP for Demand) helps forecast sales, demand, and supply plans based on factors like sales organization, sold-to-party, material, and plant data. This forecast is integrated into SAP S/4HANA as Planned Independent Requirements (PIRs), which feed into demand management. SAP S/4HANA then uses this data in Material Requirements Planning (MRP) to create planned orders, purchase requisitions, perform BOM (Bill of Materials) explosion, and calculate capacity requirements for work centers.](https://learning.sap.com/service/media/topic/caf86fe0-02cf-48b2-9855-893c36c472c1/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L4_Integration_to_S4HANA.png "The image depicts the integration between SAP Integrated Business Planning (IBP) and SAP S/4HANA to streamline processes from demand forecasting to production planning. It shows how IBP (using modules like IBP for S&OP and IBP for Demand) helps forecast sales, demand, and supply plans based on factors like sales organization, sold-to-party, material, and plant data. This forecast is integrated into SAP S/4HANA as Planned Independent Requirements (PIRs), which feed into demand management. SAP S/4HANA then uses this data in Material Requirements Planning (MRP) to create planned orders, purchase requisitions, perform BOM (Bill of Materials) explosion, and calculate capacity requirements for work centers.")

- **Forecasting** can be performed in different tools. For example, forecasting can be performed in SAP Integrated Business Planning (IBP). The result of the forecasting can be transferred to S/4HANA as a planned independent requirement.
- **Demand Management** is the management of independent requirements. The behavior of independent requirements in MRP (for example, whether they are effective or consume other requirements) is determined by the type of requirements or the planning strategy in the product master record.

# Analyzing Material Requirements Planning (MRP)

Objective

After completing this lesson, you will be able to describe the basic Material Requirements Planning Process Steps

## Introduction

For the following lessons, we will focus on **Materials Requirements Planning** in SAP S/4HANA as highlighted in the graphic below. The steps take place in the Production (PP) Module of SAP S/4HANA.

![The image shows an overview of the Design-to-Operate process, highlighting key phases such as Master Data, Demand Planning, Material Requirements Planning (currently emphasized as the active step within Procure to Receipt), Production Order to Fulfill, and Reporting.](https://learning.sap.com/service/media/topic/be6fbc6f-a21b-4097-90c4-41c44604ba0e/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate_4.png "The image shows an overview of the Design-to-Operate process, highlighting key phases such as Master Data, Demand Planning, Material Requirements Planning (currently emphasized as the active step within Procure to Receipt), Production Order to Fulfill, and Reporting.")

## Material Requirements Planning Outline

**Scenario:** You have done the pre-planning for your finished product. No you want to assure that the necessary materials will be available at the right time and quantity. This is done in Materials Requirements Planning (MRP).

MRP is to guarantee material availability. It is used to procure or produce the required quantities on time both for internal purposes and for sales and distribution:

- In the right quantity
- From the right source of supply
- At the right time

MRP takes current and future sales as its reference point. The planned requirement quantities trigger the MRP calculation. The requirements elements include sales orders, planned independent requirements, material reservations, the dependent requirements created by exploding the BOM, and so on.

If the MRP run determines a shortage of quantities, the system creates procurement proposals. Explore them in the graphic below.

![The image illustrates the Material Requirements Planning (MRP) process for Material A, showing two pathways: external procurement (steps 1–3) and in-house production (steps 4–7). The process begins with MRP calculations and proceeds through steps such as purchase requisitions, planned orders, and production orders, connecting external vendors and internal production systems. Each step is numbered and will be explained in detail in the accompanying text.](https://learning.sap.com/service/media/topic/f78d0d99-e5e2-4375-a7ba-560f68172f94/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_MRP.png "The image illustrates the Material Requirements Planning (MRP) process for Material A, showing two pathways: external procurement (steps 1–3) and in-house production (steps 4–7). The process begins with MRP calculations and proceeds through steps such as purchase requisitions, planned orders, and production orders, connecting external vendors and internal production systems. Each step is numbered and will be explained in detail in the accompanying text.")

1. **External Procurement:** With external procurement, the system creates a purchase requisition to plan the external procurement quantity.
    
2. **Purchase Order:** When planning is complete, the purchase requisition can be subsequently converted to a purchase order.
    
3. **Schedule Line:** If a scheduling agreement exists for a material and is relevant for MRP in the source list, you create schedule lines directly using MRP.
    
4. **MRP Material A:** If the MRP run determines a shortage of quantities, the system creates procurement proposals.
    
5. **In-house Production:** With in-house production, the system creates planned orders for planning the production quantities.
    
6. **Planned Order:** Purchase requisitions and planned orders are internal planning elements that can be changed, rescheduled, or deleted at almost any time.
    
7. **Convert:** When planning is complete, planned orders are normally converted into production orders. In special cases, they are converted into purchase requisitions.
    

## Six MRP Steps

Let us go through the different MRP steps:

1. Ensure planning-relevant MRP type
2. Calculate net requirements
3. Calculate quantity
4. Check procurement type
5. Scheduling
6. Create purchase requisitions

### 1. Ensure planning-relevant MRP Type / Planning Method

First, you need to decide how you want to plan your products. This is done by the **MRP type or the planning method**. The planning method is defined by the MRP type in the material master.

A material can be planned using either a deterministic or a consumption-based concept. You can identify the differences in the table below.

#### MRP Type

|Deterministic planning|Consumption-based planning|
|---|---|
|Based on independent requirements, allows for additional control using requirements strategies|Based on past consumption / historical consumption values|
|MRP based on current and future sales is executed for the entire bill of material (BOM) structure (multilevel)|- VB – Reorder point planning<br>- VV – Forecast-based planning<br>- R1 – Time-based planning|
|The quantity and date of the customer orders and the independent requirement's quantities and dates are the starting point for the requirements calculation.|Uses either forecasting or statistical procedures to determine future requirements, or just triggers replenishment if the stock situation of the material is getting low. Procurement proposals are created during MRP.|
|Mainly high-value A parts are considered|Used for less critical or low-value B parts and C parts|

One of the consumption-based planning procedures is the **reorder point planning** illustrated in the graphic below.

![The image illustrates an inventory management process, showing stock levels over time with key elements like reorder point, safety stock, and replenishment activities. It highlights the relationship between reorder points and replenishment lead time, with lot sizes and deliveries ensuring stock is maintained above safety stock levels.](https://learning.sap.com/service/media/topic/dd7accfd-df27-40fa-bacb-d844e028d17c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/MRP_Reorder.png "The image illustrates an inventory management process, showing stock levels over time with key elements like reorder point, safety stock, and replenishment activities. It highlights the relationship between reorder points and replenishment lead time, with lot sizes and deliveries ensuring stock is maintained above safety stock levels.")

This kind of planning is controlled by a (manually) entered reorder point or can be recalculated by _Demand Driven Replenishment_. If the system recognizes a stock lower than this reorder point, the system triggers a receipt element, taking into account the settings for lot sizing.

Reorder point planning is useful for materials with the following properties:

- Constant demands over several periods
- Replenishment of the requested inventory is ensured
- Replenishment lead time for procurement is known and constant

### 2. Calculate Net Requirements

As the second step, the system carries out a **net requirements calculation**. The system compares the available stock and incoming elements to the safety stock and the requirements.

### 3. Calculate Quantity

When the result of the comparison is a shortage, the system executes as a third step the **quantity calculation** of the needed receipt element, considering the lot procedure from material master (Lot Sizing Procedure).

This graphic below visualizes the second and third step.

![The image demonstrates the rescheduling horizon in inventory planning, highlighting the relationship between requirements (such as sales orders, reservations, and planned requirements) and procurement proposals. It includes components like lot sizes, safety stock, fixed receipts (e.g., purchase orders), and firmed planned orders, ensuring stock fulfillment.](https://learning.sap.com/service/media/topic/dd7accfd-df27-40fa-bacb-d844e028d17c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_QuantityCal.png "The image demonstrates the rescheduling horizon in inventory planning, highlighting the relationship between requirements (such as sales orders, reservations, and planned requirements) and procurement proposals. It includes components like lot sizes, safety stock, fixed receipts (e.g., purchase orders), and firmed planned orders, ensuring stock fulfillment.")

### 4. Check Procurement Type

The system checks whether the product is procured internally or externally. This is defined using the **Procurement Type**.

#### Procurement Type

|Procurement Type|Special Procurement|
|---|---|
|- E – In-house production<br>- F – External production<br>- X – Both procurement types|- In-house production, example:<br>    - Production in own plant<br>    - Production in another plant: 80<br>- External production, example:<br>    - Stock transfer from another plant: 40<br>    - Subcontracting: 30|

The procurement type can be in-house production (E) or external production (F). If the procurement type is both (X), material requirements planning starts with in-house production.

Based on the procurement type, the master data settings, MRP parameters, and the are scheduled.

At this point, the system knows the needed quantity to create a well-balanced stock situation and how to create receipt elements (planned orders/purchase requisitions), if needed.

### 5. Scheduling

The fifth step in MRP is **Scheduling**. Normally, MRP tries to cover demands using backward scheduling:

![The image depicts a production scheduling workflow where dependent tasks, including a purchase requisition for Component 1 and planned orders for Assembly 2 and Finished Production, are sequenced to meet the final production requirements date. It shows that Component 1 (purchase requisition) is required for Assembly 1 (purchase requisition) and Assembly 2 (planned order), both of which contribute to the Finished Production stage (planned order). The timeline emphasizes the interdependencies between these steps and their alignment with the final deadline.](https://learning.sap.com/service/media/topic/dd7accfd-df27-40fa-bacb-d844e028d17c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L5_Scheduling.png "The image depicts a production scheduling workflow where dependent tasks, including a purchase requisition for Component 1 and planned orders for Assembly 2 and Finished Production, are sequenced to meet the final production requirements date. It shows that Component 1 (purchase requisition) is required for Assembly 1 (purchase requisition) and Assembly 2 (planned order), both of which contribute to the Finished Production stage (planned order). The timeline emphasizes the interdependencies between these steps and their alignment with the final deadline.")

Backward scheduling is based on the following principles:

- The starting point is the requirement date of the finished product (for example, received as the material availability date of a sales order). Based on this material availability date of this element, the system carries out a backward scheduling over the whole BOM structure.
- Proposals are created to cover the net demand on each level of the BOM. The system calculates start and finish dates of the dependent requirements for the components and subcomponents during the BOM explosion. The start date of a component defines the end date of the related subcomponents.

### 6. Creating Purchase Requisitions

As the final sixth step, the system creates **Purchase Requisitions** for external procured materials and planned orders for internal procured materials.

The following graphic illustrates the elements in backward scheduling in case of in-house production:

![The image illustrates the timeline of a planned order process, detailing key stages including the opening period, in-house production time, and goods receipt processing time. It shows the sequence from the opening date to the start date, progressing through production to the finish date and finally reaching the availability date. The graphic highlights how these phases ensure the timely completion and readiness of planned orders.](https://learning.sap.com/service/media/topic/dd7accfd-df27-40fa-bacb-d844e028d17c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L5_PR_PO1.png "The image illustrates the timeline of a planned order process, detailing key stages including the opening period, in-house production time, and goods receipt processing time. It shows the sequence from the opening date to the start date, progressing through production to the finish date and finally reaching the availability date. The graphic highlights how these phases ensure the timely completion and readiness of planned orders.")

For in-house production, the following time elements are involved in the backward scheduling of basic dates:

- Goods receipt processing time: With backward scheduling, the system calculates the order’s start date by considering the goods receipt processing time for the planned order.
    
- In-house production time: The system calculates the order's start date by considering the in-house production time from the order finish date.
    
- Opening period: The opening period reflects the processing time the MRP controller requires to convert planned orders into production orders. It is then subtracted from the order start date. This leads to the opening date.
    

The elements in backward scheduling in case of external procurement are illustrated below:

![The image represents the external procurement process, highlighting two key phases: processing time for purchasing and planned delivery time. It shows the sequence starting from the order release date to the delivery date, indicating the planned duration needed for purchasing and delivery.](https://learning.sap.com/service/media/topic/dd7accfd-df27-40fa-bacb-d844e028d17c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U6_L5_External_Procurement.png "The image represents the external procurement process, highlighting two key phases: processing time for purchasing and planned delivery time. It shows the sequence starting from the order release date to the delivery date, indicating the planned duration needed for purchasing and delivery.")

Scheduling for externally-procured materials works in the same way as the basic date scheduling for materials produced in-house.

## Test Your Understanding

**Question:** What do you think: Which of the following is one of the most critical user mistakes in Materials Requirements Planning (MRP)?

- A) Inaccurate lead times
- B) Incorrect bill of materials (BOM) accuracy
- C) Insufficient consideration of safety stock levels
- D) Failure to account for seasonal demand changes

**Answer:** Incorrect bill of materials (BOM) accuracy is a critical user mistake in MRP as it can cause incorrect inventory levels and delays in production. Ensuring that the BOM is accurate and up-to-date is essential for the effective functioning of the MRP system.

## How to Extend the Raw Material

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C8CA0EC9D31D74A1:demo)

## Planning Run in SAP S/4HANA

**Scenario:** You are finished with your pre-planning run (planning of Planned Independent Requirements) with SAP IBP and handed the planning over to SAP S/4 HANA. Now, you want to schedule an MRP run for our new e-bike. Normally, a multi-level MRP run will be performed for all products and scheduled as a periodic job running in the background. However, for now, you will only perform one run for your finished product.

The SAP system empowers you to do that. The following graphic illustrates the various options to scope and schedule your planning.

![The image highlights various planning scope and scheduling options in material requirements planning (MRP). It presents choices like planning for a whole plant, several plants, or an individual material, as well as planning for all MRP-relevant materials, different BOM levels (multi or single level), and interactive versus background scheduling. These options provide flexibility for tailored production planning processes.](https://learning.sap.com/service/media/topic/db4d0d7f-5124-4293-8d32-a50b1d04a3a2/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/PlanningScope.png "The image highlights various planning scope and scheduling options in material requirements planning (MRP). It presents choices like planning for a whole plant, several plants, or an individual material, as well as planning for all MRP-relevant materials, different BOM levels (multi or single level), and interactive versus background scheduling. These options provide flexibility for tailored production planning processes.")

- You can execute the planning run at two levels - as total planning for a plant or for an individual material.
    
- You can also execute a total planning run for several plants and MRP areas (planning scope).
    
- It is possible to execute a single-item planning run for one BOM level only (single-level) or for all BOM levels (multi-level).
    
- Interactive planning of a material is also possible. Total planning for a plant encompasses all MRP-relevant materials for this plant and includes the BOM explosion for materials with BOMs.
    
- You can execute total planning online or as a background job. To execute the total planning run as a background job, select a report variant to restrict it to the relevant plant, and schedule the job. This makes it possible to combine several plants (or MRP areas) in a planning sequence as part of a planning run and to plan across plants in an overall planning run. Mutual dependencies, such as those caused by stock transfers, are automatically taken into account by the system.
    

With SAP S/4HANA, the MRP Live eliminates the danger of planning with obsolete data. MRP is a supply chain planning process used with other planning processes, such as Demand Planning, Supply Planning, Sales & Operations Planning, Production Planning, and Transportation Planning, all of which are used to manage the supply chain activity of the enterprise.

MRP is the process of matching enterprise-wide supply with actual and forecasted customer demand to identify potential material shortage situations and to recommend potential solutions.

Examples of supply include material in inventory, planned stock transfers, purchase orders, and good receipts from manufacturing. Examples of demand include customer sales orders and forecasts of future customer demand.

Supply and demand requirements are location-specific and MRP matching is performed to ensure that the materials are in the right location at the right time to fulfill customer demand.

## How to Analyze Planned Independent Requirements

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_1E93546663890186:demo)

## How to Execute a Material Requirements Planning Run

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_ED02045FCFD7378F:demo)

## How to Analyze the Result of the MRP Run

Demo[  
](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_2E78F944FD65C6A5:demo)


# Processing Production Orders

Objective

After completing this lesson, you will be able to describe the basic production order execution process steps

## Introduction

This lesson focuses on production execution – shop floor processing in SAP S/4HANA as highlighted in the graphic below. The steps for production execution take place in the production module (PP) of SAP S/4HANA.

![The image provides an overview of the Design-to-Operate process, highlighting its phases: master data and product cost calculation, demand planning, procure to receipt, production order to fulfill, and reporting. The focus is on the Production Order Processing step under the production order to fulfill phase, indicating the current stage in the process workflow.](https://learning.sap.com/service/media/topic/ec31f68d-d9f9-4b27-aabb-0abd579c5a97/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate5.png "The image provides an overview of the Design-to-Operate process, highlighting its phases: master data and product cost calculation, demand planning, procure to receipt, production order to fulfill, and reporting. The focus is on the Production Order Processing step under the production order to fulfill phase, indicating the current stage in the process workflow.")

## Production Order Characteristics

**Scenario:** As a result of the materials requirements planning, you received as input planned orders for production execution. The created purchase requisitions will be processed by the purchasing department. Here you will focus on the in-house Production.

**Production orders** control the whole process of in-house production of products. They are a central part of a complex process chain starting with a _Planned Independent Requirement (PIR)_ or sales order and ending with the goods receipt of the finished product.

Key features:

- Important steps in production order processing are order creation, scheduling, release, material withdrawal, confirmation, goods receipt, and settlement.
- Production orders are integrated into the functions of capacity requirements planning, costing, inventory management, and into many other applications.

The following graphic provides an overview of the integration of production orders and other applications.

![This diagram illustrates the integration of production orders within a manufacturing process, highlighting how demand, material requirements planning (MRP), and production phases connect to key functions like sales, capacity planning, inventory management, quality management, and process control.](https://learning.sap.com/service/media/topic/f8dd6058-abf4-432e-938b-1055cfc9259b/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_Overview.png "This diagram illustrates the integration of production orders within a manufacturing process, highlighting how demand, material requirements planning (MRP), and production phases connect to key functions like sales, capacity planning, inventory management, quality management, and process control.")

Production orders include the following information:

#### Production Orders

|Required Information|Production Order Data|
|---|---|
|What do you produce?|- Products<br>- Activities|
|For which dates?|- Scheduled dates<br>- Confirmed dates|
|In which quantities?|- Planned quantity<br>- Delivered quantity|
|For whom (cost object)?|- Material<br>- Cost Center<br>- Order<br>- Project|
|With which resources and methods?|- Work Centers<br>- Operations/activities<br>- Material components<br>- Production resources/tools|
|At which costs?|- Planned costs<br>- Actual costs|

### Processing a Production Order

There are five main process steps in production:

1. **Order Creation**
2. **Order Release**
3. **Goods Issue**
4. **Confirmations**
5. **Goods Receipt**

## 1. Creating a Production Order

### Structure of a Production Order

Learn more about the structure of a production order by exploring the graphic below.

![This diagram outlines the key components of a production order structure, including order header, settlement rules, costs, operation sequences, operations, material components, and confirmations. Each element (1-7) is connected to specific details that will be explained further in the accompanying text.](https://learning.sap.com/service/media/topic/c870eb9e-0064-4167-b689-99755e51eb38/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_ProductionOrder.png "This diagram outlines the key components of a production order structure, including order header, settlement rules, costs, operation sequences, operations, material components, and confirmations. Each element (1-7) is connected to specific details that will be explained further in the accompanying text.")

1. **Order Header:** General data
2. **Settlement Rules:** Used to settle the cost to corresponding receivers. In the production for stock, we settle to the material.
3. **Costs:** If you use order-related cost object controlling, a cost object is managed for every single process object. The cost object enables different cost items for the production order. The graphic below to learn more about the planned costs of a production order.
4. **Operation Sequences:** Operations allocated to the standard sequence are processed one after another.
5. **Operations:** Here we define the work that needs to be processed.
6. **Material Components:** The necessary materials are listed for producing the product.
7. **Confirmations:** The confirmation of Time processed for an operation

Note

The following graphic provides an overview of the planned costs of a production order.

![This diagram provides an overview of the planned costs associated with a production order, dividing costs into material costs, costs of internal activities (in-house production), and total overhead process costs. It highlights key inputs such as material components, operations, work centers, cost centers, tariffs, and costing variants, with calculations using planned quantities, prices, and tariffs.](https://learning.sap.com/service/media/topic/c870eb9e-0064-4167-b689-99755e51eb38/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_Overviewcosts.png "This diagram provides an overview of the planned costs associated with a production order, dividing costs into material costs, costs of internal activities (in-house production), and total overhead process costs. It highlights key inputs such as material components, operations, work centers, cost centers, tariffs, and costing variants, with calculations using planned quantities, prices, and tariffs.")

### Converting a Planned Order to a Production Order

You can convert a planned order into a production order on three different ways:

- **Collective conversion** can be performed in background processing. After converting a planned order into a production order the planned order is deleted.
- **Individual conversion:** After converting a planned order into a production order, the planned order is deleted.
- **Partial conversion:** In partial conversion, the planned order still exists and is fixed.

## How to Convert a Planned Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_2373113EB2E3CF97:demo)

## 2. Release of Production Orders

The order release is the basis for the further processing of the production order. Production orders have a status management that controls the possible processing sequence of the individual business processes. When an order is released, a status is set accordingly.

The production order must have a _Released_ status so that the business processes for production order execution can be performed.

An availability check can be executed automatically.

## How to Release a Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C56FA97EAA86DFAD:demo)

## 3. Posting Goods Issue to Production Order

The goods issue posting is executed for consumption of a material component for a production order.

Options to post goods issue:

- **Picking List** You can use a picking function to prepare and post material withdrawals. You can use this function to create and print a picking list and post the material withdrawals.
    
- **Goods Movement in Inventory Management:** You can use the Goods Movement app / transaction in inventory management to post the goods issues.
    
- **Backflushing:** A material component withdrawal can be posted automatically (backflushing), synchronously or asynchronously when an operation or the order is confirmed. Always use backflushing when you do not want to stage materials for a specific order. It is assumed that the material is staged and available at the work center.
    
    Typical application areas are flow and assembly lines and the staging of less valuable materials.
    
    You can control backflushing in the material master, in the work center or for each BOM component assignment to an operation.
    

### Effects of Goods Issue Posting

The following graphic illustrate the effects of goods issue posting.

![The process flow diagram depicts the Goods Issue process in inventory management. It shows various inputs such as stock quantity, account determination, reservation, consumption statistics, and G/L accounts flowing into the Goods Issue step. Outputs include material documents, accounting documents, a goods issue slip, and details related to the point of consumption (e.g., order, cost center). The relationships among these elements are interconnected via arrows, emphasizing how inputs are processed into outputs. The details of points 1 through 5 noted in the diagram will be further elaborated upon below.](https://learning.sap.com/service/media/topic/c85602e3-6610-4387-be96-b85861b7dacc/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_GoodsIssue.png "The process flow diagram depicts the Goods Issue process in inventory management. It shows various inputs such as stock quantity, account determination, reservation, consumption statistics, and G/L accounts flowing into the Goods Issue step. Outputs include material documents, accounting documents, a goods issue slip, and details related to the point of consumption (e.g., order, cost center). The relationships among these elements are interconnected via arrows, emphasizing how inputs are processed into outputs. The details of points 1 through 5 noted in the diagram will be further elaborated upon below.")

1. **Stock Quantity:** To document the quantity changes for the materials, we generate a materials document. Here we would see the movement types as well.
    
2. **Account Determination:** The accounts posted are determined automatically in the background using a functionality called: MM account determination.
    
3. **G/L Accounts:** As we change the inventory while consuming products, we post to G/L Accounts. This could be balance sheet account as consumption accounts. This is documented by the accounting document.
    
4. **Point of Consumption:** The goods issue (Gl) is posted to a costing object. For our example the Gl is posted to Production Order. The costs for consuming the products are posted as actual costs to the production order.
    
5. **Goods Issue Slip:** If required, you can print a Goods Issue Slip.
    

## How to Post Goods Issue for Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_A48E899A9C8CE38D:demo)

## 4. Confirmation of Time

Time confirmations are an important element of production orders.

1. Confirmations are the premise for progress control and basis for entering internal activities.
2. They should be as prompt and efficient as possible.
3. Confirmations from process control systems are possible using various interfaces.

Explore the chart below to learn more about the different functions that can work with the data from time confirmations.

![The process flow diagram illustrates the Saving the Confirmations step in production management. Key inputs include capacity requirements, material documents, activities (standard values and quantities), HR data, and actual costs. These inputs are linked to a production order (with operations such as 0010, 0020, and 9999) and processed through the confirmation step, resulting in updated production data. The details of points 1 to 5 referenced in the diagram are further described in the text below.](https://learning.sap.com/service/media/topic/e481fdcd-fb41-4fde-bc32-52662ea516ae/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_Confirmationtime.png "The process flow diagram illustrates the Saving the Confirmations step in production management. Key inputs include capacity requirements, material documents, activities (standard values and quantities), HR data, and actual costs. These inputs are linked to a production order (with operations such as 0010, 0020, and 9999) and processed through the confirmation step, resulting in updated production data. The details of points 1 to 5 referenced in the diagram are further described in the text below.")

1. **Capacity Requirements:** Open Capacity requirements are reduced during confirmation.
2. **Material Documents:** Automatic Goods Movement postings (GR and GI) can occur during time confirmation. This would result in Material Documents being posted during confirmation of time.
3. **Confirm:** Time confirmations can be automatic or manual.
    - Automatic: Process control
    - Manual:Online apps/transactions; Mass processing
4. **Actual Costs:** For the time processed, the system posts actual labor and/or machine costs to the production order at the tariff of the cost center and activity type assigned to the work center.
5. **HR Data:** If assigned to a personal master data record, relevant data could be handed over to HCM for payroll, for example.

During the confirmation of time, the work center records the time that has been used for the production steps. As the work center is assigned to a cost center providing different activity types, actual costs are posted to the production order by the confirmation of time.

The graphic below shows what processes are triggered next.

![A process flow diagram illustrating the steps triggered by time confirmation in a production system. Key processes include updating order information (status, activities/quantities, and actual costs), automatic goods receipt, backflush goods issue, HR data transfer, and reduction in capacity requirements. Actual costs are also posted to the production order.](https://learning.sap.com/service/media/topic/e481fdcd-fb41-4fde-bc32-52662ea516ae/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_TimeConfirmation.png "A process flow diagram illustrating the steps triggered by time confirmation in a production system. Key processes include updating order information (status, activities/quantities, and actual costs), automatic goods receipt, backflush goods issue, HR data transfer, and reduction in capacity requirements. Actual costs are also posted to the production order.")

The following processes are triggered:

1. Automatic Goods Receipt
2. Order
    - Status
    - Activities/Quantities
    - Actual Costs
3. HR Data Transfer
4. Backflush Goods Issue
5. Reduce capacity requirements
6. Actual Costs

## How to Post Confirmation of Time for Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_DE498AF135D537A7:demo)

## 5. Goods Receipt Posting

**Scenario:** In the bike company in our example the planned number of eBikes is successfully produced. You post a goods receipt. Goods receipts are handled in Inventory Management.

What processes are triggered now? The following graphic provides an overview.

![This diagram outlines the processes triggered during a Goods Receipt posting, including updates to the stock/requirements list, stock quantity, account determination, G/L accounts, order status, document creation, and additional steps like generating an EWM inbound delivery order and a goods receipt slip. Steps 1 to 8 are described in detail below.](https://learning.sap.com/service/media/topic/ca5b5736-8c76-47be-bd0e-cb125f470c7f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_GoodsImpact.png "This diagram outlines the processes triggered during a Goods Receipt posting, including updates to the stock/requirements list, stock quantity, account determination, G/L accounts, order status, document creation, and additional steps like generating an EWM inbound delivery order and a goods receipt slip. Steps 1 to 8 are described in detail below.")

1. **Stock/Requirements list:** The production order is deleted in the stock/requirements list and in the product view.
2. **Stock Quantity:** The quantity in the storage location in inventory management is increased.
3. **Account Determination:** The account determination takes place automatically using the MM account determination from Customizing.
4. **G/L Accounts:**
    - Stock Account
    - Plant ActivityDuring the GR posting the Stock Account is debited and the plant activity account is credited.
5. **Order:**
    - Status
    - Quantity
    - Actual CostsThe order status and the delivery quantity are updated. Actual costs are determined (evaluated) and credited to the order.
6. **Material Document:** Material, accounting, and controlling documents are generated.
7. **EWM Inbound Delivery Order:** When you use EWM, you need to create an Inbound Delivery Order for putaway and processing the steps in the Warehouse.
8. **Goods Receipt Slip:** The Goods Receipt is posted with movement type 101. A movement type is always necessary when posting goods movements.

## How to Post Goods Receipt for Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_13C034709238F8A9:demo)

## Final Step: Technical Completion

As the process flow of a production order is controlled by the system status (for example CRTD for _created_ or REL for _released_) the order should be technically completed once the order is finished from a production point of view. The status is then TECO: _technical completed_

When setting an order to TECO, the order is closed and cannot be changed any more. As subsequent activities, the period end closing procedures will take place.

## How to Set Technical Completion to a Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_D4EA4A24FE4EB7B2:demo)


# Understanding the Period End Closing

Objective

After completing this lesson, you will be able to explain the period end closing activities

## Introduction

This lesson covers **Period Closing** Activities in SAP S/4HANA. The steps for production execution take place in the Controlling (CO) module of SAP S/4HANA and are highlighted in the process flow below.

![](https://learning.sap.com/service/media/topic/fc510328-5381-45e5-a484-7104de08a7aa/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Design2Operate_6.png)

As soon as you have posted actuals to your production orders, there are period end closing activities to be processed for the production orders. These period end closing activities are processed by the Controlling Department.

The activities we focus on in this lesson are the **variance calculation** and the **settlement.**

## Surveying Period End Closing Activities

The following graphic provides an overview of the key activities in period end closing.

The variance calculation determines the target costs of the cost object. The target costs enable you to run a target/actual comparison report. The scrap variance is always calculated based on the target costs compared to actual costs.

There are also some background activities in Period End Closing. WIP calculation, variance calculation, and settlement are periodic activities of Cost Object Controlling (COC) and are processed in the background.

Do you have an idea how costs are connected to production orders? Let us have a look on a production order.

![](https://learning.sap.com/service/media/topic/f787fc3d-fa3e-4701-a826-d96210136092/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Period%20End%20Closing.png)

The settlement rule has the settlement type FUL, which means full settlement. For period end closing, the status of the cost object chooses whether WIP or variances are calculated.

Have a look on the following graphic to find out which status need to be considered in the Product Cost by Order component.

If the order has neither the status DLV, nor TECO, WIP is calculated based on actual costs. The difference between all debits and credits of the order is the value of the WIP.

If the order has the status DLV or TECO, any existing WIP will be canceled, and the system interprets the entire remaining order balance as variances. Various variance causes are evaluated and summarized into appropriate variance categories.

### Variance Calculation

To verify cost variances, the different variance categories must be calculated and settled to FI and CO-PA. Checking the variance categories like scrap, allows you to take conclusion about the effectiveness of the production.

There are different variance categories: input and output categories.

The following graphic provides an overview of input categories.

**Examples** for the marked categories:

1. **Input Price :** Raw material 1 was valuated at a price of 10 in the standard cost estimate. When the material is withdrawn from inventory, the goods movement is valuated at 11. Price control specifies that valuation is carried out at the moving average price. This results in a price variance of 1.
    
2. **Input Category:** A machine time of 15 minutes was planned but 17 minutes were confirmed. The activity price for the machine time is 5 per minute. This results in a quantity variance of 10.
    
3. **Resource x Usage:** Raw material 2 is used instead of raw material 1. The costs for both raw materials are reported as resource-usage variances.
    
4. **Remaining Input Variance** The material overhead is higher than planned as the price for material 1 is changed. The difference between the planned and actual material overhead expense is reported as a remaining input variance.
    

The following graphic provides an overview of output categories.

**Examples** for the marked categories:

1. **Mixed Price:** If the standard price of a material was calculated using multiple procurement alternatives (mixed cost estimate), subsequent production without variances will still have a difference to the standard price. This is the mixed-price variance.
    
2. **Lot Size:** If another quantity was used for production than previously generated in the product costing, the fixed costs are adjusted proportionally with another quantity, that is, the fixed costs per piece change. This is the lot-size variance.
    
3. **Output Prices:** The material is transferred to the inventory at a price other than the standard price (such as a moving average price). The difference is determined as an output price variance.
    
4. **Remaining Output Variance**If the system cannot determine the target costs, it will determine only remaining variances. This might cause anomalies by rounding up or down the costs.
    

## How to Perform Variance Calculation

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_FB0773F2CB111091:demo)

## Settlement

The last step for Period End Closing is **Settlement**.

**Scenario:** After calculated the variances, the orders also need to be settled. This step is done by the Controlling department. However, Financial Accounting should be informed about price differences in total and variance categories as well.

To do this, you must settle 3 values to Financial Accounting and Margin Analysis.

- Work in Process
- Price Difference
- Variance Categories

The following graphic shows a settlement example. On the right side you see the settlement values.

### Business Completion

When the production order costs have been settled and the balance on the production order is Zero, the production order will be closed finally. This final closure is called _Close_. This system status tells that the production order is finished from the perspective of all included departments.

## How to Perform Settlement and Close the Production Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C2589437E67ECE95:demo)