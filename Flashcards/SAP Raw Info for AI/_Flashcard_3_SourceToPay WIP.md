# Identifying the Procurement Process

Objective

After completing this lesson, you will be able to identify the procurement process in SAP Ariba and SAP S/4HANA

## Introduction

**Scenario:** Imagine that the SAP implementation project of the bike company we use as example is currently in the _Realization_ phase. In this phase the project team tests the end-to-end processes. The SAP consultant already assigned the selected scope items for each area to the business processes of the bike company. This enables the project team to understand which summarized scope items are used to represent a core process within their company.

Based on best practice scope items, they created an overview of the **source-to-pay process with focus on procurement** as illustrated below. The summarized SAP Best Practice scope items form the basis for the project team’s end-to-end process tests.

Note

For the sake of simplicity, not all of the used SAP Best Practice scope are listed.

![](https://learning.sap.com/service/media/topic/eb0e42a7-3a3b-4b24-86be-dd6ded6919b3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-Pay%20Overview.png)

- **Master Data, Requirement, Sourcing:** Like in all areas, we must define and handle master data (data that is kept for a longer period), such as suppliers, materials, prices and rebates. The steps for managing purchase requisitions in SAP S/4 HANA as well as in SAP Ariba are included if required for finding corresponding suppliers.
- **Contract Management** includes the creation and administration of all kinds of contracts (Quantity-Value contracts) for the purchasing process. Contracts can be managed as well in SAP Ariba.
- **Operational Procurement:** This step includes all process steps related to managing and processing purchase orders.
- **Receiving:** In this step, we have a close look at the posting of goods receipt as well as the possibility of using extended warehouse management
- **Invoice Management:** This step covers all the related process steps in managing the posting of supplier invoices.
- **Reporting:** This step covers comprehensive reporting functionalities and analytics for intelligent spent management.

From an SAP solution point of view we are now here:

![This image provides an overview of SAP's procurement solution landscape, highlighting the integration of SAP Ariba and SAP S/4HANA's module Materials Management (MM) within the broader SAP ecosystem.](https://learning.sap.com/service/media/topic/eb0e42a7-3a3b-4b24-86be-dd6ded6919b3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation_3.png "This image provides an overview of SAP's procurement solution landscape, highlighting the integration of SAP Ariba and SAP S/4HANA's module Materials Management (MM) within the broader SAP ecosystem.")

As you can see in the overview, there are two possible systems that can be used in procurement:

- Originally, the entire procurement process took place in the **SAP S/4HANA module Materials Management (MM).**
- In addition to the SAP S/4HANA core to run the source-to-pay process, SAP also offers the **SAP Ariba Procurement** solution.

## SAP Ariba Overview

As the SAP S/4HANA solution to run the source-to-pay process is described in detail in the upcoming lessons, let us first have look how the process runs in the SAP Ariba Procurement solution.

The following graphic provides an overview of the various components within SAP Ariba. The procurement solution is highlighted.

![This image highlights SAP Ariba's focus on procurement within its suite of solutions, alongside financial supply chain, supply chain, strategic sourcing solutions, and supplier management.](https://learning.sap.com/service/media/topic/db737176-6437-46b1-96aa-d77def3935c7/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP%20Ariba.png "This image highlights SAP Ariba's focus on procurement within its suite of solutions, alongside financial supply chain, supply chain, strategic sourcing solutions, and supplier management.")

- **Financial Supply Chain**: With these integrated financial supply chain management solutions and services, you can achieve visibility throughout the source-to-pay process, improve supplier relationships, and realize fast ROI.
- **Procurement**
    1. SAP Ariba Buying and Invoicing is a best-in-class, easy-to-use procure-to-pay solution. It helps companies effectively manage all spend-related processes and ensure negotiated savings are reflected in their net profit.
    2. SAP Ariba Catalog defines, validates, and enriches catalog content with enterprise-grade content management tools and gives employees a simple way to get what they need.
    3. SAP Ariba invoice Management increase the accuracy of invoices to speed up both processing and payments. Let SAP Business Network does the work of pre-validating invoices, so any missing or incorrect information gets corrected, and you see fewer exceptions.
    4. SAP Ariba Buying can automate your procure-to-order process and integrate with your back-end system to let your ERP handle invoice and payment processing.
- **Supply Chain**: Share real-time information with all your direct spend suppliers, obtain their commits, and tap network-generated intelligence to achieve complete supply chain visibility.
- **Strategic Sourcing Solutions** empowers you to manage and optimize your entire sourcing, contracting, and spend analysis processes for all types of spend - direct and indirect materials as well as services.
- **Supplier Management**: Integrated with the rest of your procurement processes, SAP Ariba Supplier Management is an end-to-end solution portfolio that lets you manage supplier information, lifecycle, performance, and risk all in one place. With this category of SAP Ariba solutions, you can drive spend to preferred suppliers and reduce risk every step of the way, from supplier onboarding and qualification to segmentation and performance management.

## Buying Process Using SAP Ariba and SAP S/4HANA

As we have two solutions for procurement, the challenge is to find the best way to process your procurement requirements. As one option you could integrate the entire portfolio and use SAP ARIBA and the SAP S/4HANA ERP solution.

The graphic below outlines a possible process flow by integrating SAP ARIBA in conjunction with SAP S/4HANA ERP.

![This diagram outlines the end-to-end procurement process using SAP Ariba and Ariba Network, showing the interactions between buyers and suppliers. It begins with the requester filling a shopping cart and submitting it for approval, followed by approvals, purchase order (PO) issuance, and optional order changes or cancellations. Suppliers confirm the PO, issue shipping notices, and deliver goods, which are then received and recorded by the requester. The supplier submits an invoice, which is processed by the accounts payable (AP) team, leading to payment remittance. The roles of requesters, approvers, suppliers, and AP teams are highlighted, with integration into SAP S/4HANA or other ERP systems.](https://learning.sap.com/service/media/topic/d76c4987-e011-4d80-9e45-2a401a97bc71/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit6_AribaBuyingProcess.png "This diagram outlines the end-to-end procurement process using SAP Ariba and Ariba Network, showing the interactions between buyers and suppliers. It begins with the requester filling a shopping cart and submitting it for approval, followed by approvals, purchase order (PO) issuance, and optional order changes or cancellations. Suppliers confirm the PO, issue shipping notices, and deliver goods, which are then received and recorded by the requester. The supplier submits an invoice, which is processed by the accounts payable (AP) team, leading to payment remittance. The roles of requesters, approvers, suppliers, and AP teams are highlighted, with integration into SAP S/4HANA or other ERP systems.")

Note

Please note, that this is only an exemplary process flow.

# Explaining the Requisitioning Process

Objective

After completing this lesson, you will be able to recall the basic sourcing process steps

## Introduction

We will now focus on the first business process steps in the source-to-pay process as highlighted in the graphic below.

![The image illustrates the Source-to-Pay process, a sequential workflow with six key phases: Master Data, Requirement, Sourcing; Contract Management; Operational Procurement; Receiving; Invoice Management; and Reporting. The current focus is on the 'Master Data, Requirement, Sourcing' phase, which includes tasks such as managing purchase requisitions, RFQs, sourcing projects in Ariba, and quoting in Ariba, as highlighted in yellow boxes](https://learning.sap.com/service/media/topic/cb30a101-eaf6-4b1e-8377-98470c1f6d1d/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%201.png "The image illustrates the Source-to-Pay process, a sequential workflow with six key phases: Master Data, Requirement, Sourcing; Contract Management; Operational Procurement; Receiving; Invoice Management; and Reporting. The current focus is on the 'Master Data, Requirement, Sourcing' phase, which includes tasks such as managing purchase requisitions, RFQs, sourcing projects in Ariba, and quoting in Ariba, as highlighted in yellow boxes")

**Scenario:** As part of the integration test, you first have a look at the required master data in procurement. The first documents will be created manually to initiate the source-to-pay process. Having sorted out some issues and designing the process, you test the data from the perspective of procurement and see how they impact Finance and Management Accounting.

So, we now check the required master data and the impacts to Finance and Management Accounting from the master data. Afterwards, we check the posting from Material Management (MM) to Finance in SAP S/4HANA.

## Supplier Master Data Record

In the same way that you used an FI supplier in the record-to-report process, it is now necessary to extend that Business Partner so they can be used in the source-to-pay process.

The picture shows the supplier role and its role-related data.

![The image highlights the Business Partner Role of 'Supplier,' displaying general data such as name (Jane Smith), address (Supplier Way, 58802 Balve), and bank account details, along with purchasing data linked to two organizations: 'C 100 - Bike Company Central' and '1010 - Bike Company DE.](https://learning.sap.com/service/media/topic/cd9c44d2-8039-405a-95cb-65bc4badc9c2/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/BP%20Supplier.png "The image highlights the Business Partner Role of 'Supplier,' displaying general data such as name (Jane Smith), address (Supplier Way, 58802 Balve), and bank account details, along with purchasing data linked to two organizations: 'C 100 - Bike Company Central' and '1010 - Bike Company DE.")

Note

Please note that the general data has to be provided for each Business Partner role.

## How to Create Business Partner from the Perspective of Purchasing

To use the FI vendor in purchasing, you must extend the existing business partner with the supplier role. While entering the necessary Purchasing Organization you are able to create the relevant _purchasing data_Complete the fields as required.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_5352EF1931CAAC9E:demo)

## Product or Material Master

Before the bike company in our example can procure the materials needed to produce a new e-bike, they must first create a **product master record** (sometimes referred to as a material master record). The product master data record is the most centralized object in the ERP environment. Because it is used by all departments, each department must create the necessary data.

Because we need to buy the new material in advance for the development and the prototyping, the procurement department starts creating a new product master record.

The product master is organized by departments. Views are allocated to each department (data tabs – grouping of fields) that contain the information necessary for the department. Because the development of a new product starts in the Engineering department, they are responsible for maintaining the basic data.

The purchasing department is then the first one involved in the process of sourcing and they need to maintain data as well. As the new material will be managed in stock, besides the storage data, accounting data is necessary as the materials will be managed in valuated stock.

From this perspective the following departments need to maintain data:

- Engineering / Construction
- Purchasing
- Storage
- Finance

Because there are different types of products, it is possible to differentiate the usage (which departments can maintain a product) of the product.

The following are examples for the material type:

- FERT for a finished product
- RAW for a raw material
- SEMI for a semi-finished product

You must also specify an industry sector, which determines the fields necessary.

A product master record is created (or maintained) for every enterprise structure needed by the department. Depending on the departments (and therefore the views), the product master needs to be maintained with a reference to the client – engineering data, with reference for plant – purchasing data, with reference for plant / storage location from the storage views.

Because the bike company produces products and uses production planning, the valuation level plant has been set up. Therefore, the financial views are created at the level of the plant.

The graphic below summarizes the main steps to create and maintain a material master.

![The image illustrates the key components of Product Master Data, highlighting four steps: 1) Engineering, which includes basic data such as description, weight, and dimensions; 2) Purchasing, which involves plant-specific purchasing data like purchasing group or quality inspection; 3) Storage, which covers data relevant to storage locations such as storage bins; and 4) Accounting, which includes plant-level accounting data like valuation class or price. Steps 1 to 4 will be explained in detail below.](https://learning.sap.com/service/media/topic/ccb6b202-f977-4a41-9709-dd4cc833a42b/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Product%20Master%20Data.png "The image illustrates the key components of Product Master Data, highlighting four steps: 1) Engineering, which includes basic data such as description, weight, and dimensions; 2) Purchasing, which involves plant-specific purchasing data like purchasing group or quality inspection; 3) Storage, which covers data relevant to storage locations such as storage bins; and 4) Accounting, which includes plant-level accounting data like valuation class or price. Steps 1 to 4 will be explained in detail below.")

1. As the engineering department is the first one to know about a new product, it is their responsibility to maintain the basic data of a product. This data could even be transferred from a CAD system where the product was designed. Basic data includes, for example, the description, the weight and the dimension. This data is valid on the level of the client.
    
2. Next, the Purchasing Department creates the necessary data. This data is valid for the plant. Some of the data maintained here is the purchasing group (the person responsible for buying the product), information regarding tolerances, and whether or not the product should be posted into quality inspection stock.
    
3. Because want to store the product in stock, we need to create the storage view. The data maintained is valid for the storage location in a plant. Here you maintain, for example, the storage bin. Keep in mind that one material can be stored only in one specific storage bin. If you need several bins, you need to use warehouse management functionality.
    
4. As we store our product in stock, we need to valuate our product. Because we have chosen the valuation level, plant, the accounting data is maintained at the level of the plant. In the accounting data, we maintain, for example, the valuation class (which is necessary for postings to stock accounts to be correct), and the valuation price. Here you can choose between a standard price or a moving average price. As we maintain a raw product we will use moving average price.
    

## How to Create a Product Master Record

Create a Product Master Record, based on the information presented earlier.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_9960C28E5B4681A7:demo)

## Manage Purchase Requisition

Managing the purchase requisition is part of the business process step _requirement_.

A purchase requisition is an internal document that tells the purchasing department that they should start a procurement process. Purchase requisitions can be created manually or automatically. The document consists of a header and items. Each level has individual elements to control the usage of a purchase requisition.

The following picture summarizes the process flow of a purchase requisition.

![The image outlines the process of creating a purchase requisition, starting with two document types: 'Inhouse' and 'From vendor' (step 1). It differentiates between stock and consumption scenarios, where stock does not require an item category or account assignment category, while consumption requires an account assignment category and may or may not require an item category. The process then leads to either 'In stock' (step 2) or 'Direct consumption' (step 3). Steps 1 to 3 will be explained in detail below.](https://learning.sap.com/service/media/topic/c371e4fa-596f-441d-80e8-d6043563c72a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Sourcing.png "The image outlines the process of creating a purchase requisition, starting with two document types: 'Inhouse' and 'From vendor' (step 1). It differentiates between stock and consumption scenarios, where stock does not require an item category or account assignment category, while consumption requires an account assignment category and may or may not require an item category. The process then leads to either 'In stock' (step 2) or 'Direct consumption' (step 3). Steps 1 to 3 will be explained in detail below.")

1. **Creating the purchase requisition:** You can buy products from external vendors or order products from an internal plant. To differentiate between these, you have two different document types on the header.
    
    When buying products from an external vendor, you can differentiate the way of buying the products and the follow-on business processes.
    
2. **Follow-on step material in stock:** In most cases we order material for our plant, put it in stock and receive and pay the invoice. We need no item category and no account assignment category for this way of ordering something.
    
    Stock material is a material that is kept in stock. Such materials are placed in storage following a goods receipt. When such materials are received by or issued from stores, the stock on hand is increased or reduced by the amount of the quantity received or issued.
    
    To order a material for stock, the material must have a master record. When you order a material for stock, the system does not require an manual account assignment. For each goods movement (for example goods receipt or goods issue), the necessary postings to the corresponding stock and consumption accounts are made automatically. The value and the quantity of the stocked material are updated in the material master record.
    
3. **Follow-on step direct consumption:** If we procure a material directly for consumption, we must specify an account assignment category and additional account assignment data in the document item of the purchase requisition or purchasing document.
    
    The account assignment category determines the account assignment object category that is to be charged, and which account assignment data you must provide.
    

### Assigning Categories - Example

An example of procuring a material directly for consumption is a subcontracting process: The subcontracting process involves shipping materials to the supplier for them to perform some work. For example, if you ship materials to the supplier and the supplier assembles the shipped materials, before sending it back to you.

In this example, you need to be able to post a goods issue and then a goods receipt for the assembled product.

![The image compares two purchase requisition processes: on the left, the subcontracting process with item category 'L' for subcontracting; on the right, the process for ordering consumable material (cost center) with item category 'K' for office material. Both include fields for account assignment category and item details, followed by a 'submit' button.](https://learning.sap.com/service/media/topic/c371e4fa-596f-441d-80e8-d6043563c72a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Sourcing%202.png "The image compares two purchase requisition processes: on the left, the subcontracting process with item category 'L' for subcontracting; on the right, the process for ordering consumable material (cost center) with item category 'K' for office material. Both include fields for account assignment category and item details, followed by a 'submit' button.")

- To perform the subcontracting process, you assign **item category L**. Then you submit your document. You just started creating your first purchase requisition.
- To order consumable material, a product master record is required. Let's assume we want to order office material, for example pen's or even a laptop for your use. For these materials, you might not have a product master record. You might even order from a catalog.
    
    When ordering something as a consumable material, you use the **account assignment category.** As this buying is not for stock, you post to consumption or asset accounts. For example, we use an account assignment object **K for cost center** or **P for a WBS element**.
    

### Summary

The item category is used to define the business process used in purchasing.

The following item categories are available:

- Normal
- Consignment
- Stock Transfer
- Subcontracting
- Service

The account assignment category is used when ordering products directly for an accounting object. Possible accounting object are:

- Cost Center
- Asset
- WBS element
- Order (enterprise asset management, production order and others…)

![The image outlines the purchasing process for Stock Material and Consumable Material, differentiating between scenarios with or without a Material Master Record and with or without an Account Assignment Category. For Stock Material without an Account Assignment Category, no entries are required, and the stock account is automatically determined at goods receipt. For Consumable Material with an Account Assignment Category, manual entry is required for consumption account and account assignment objects such as cost center or asset.](https://learning.sap.com/service/media/topic/c371e4fa-596f-441d-80e8-d6043563c72a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L3_Stock_Material.png "The image outlines the purchasing process for Stock Material and Consumable Material, differentiating between scenarios with or without a Material Master Record and with or without an Account Assignment Category. For Stock Material without an Account Assignment Category, no entries are required, and the stock account is automatically determined at goods receipt. For Consumable Material with an Account Assignment Category, manual entry is required for consumption account and account assignment objects such as cost center or asset.")

## How to Create Purchase Requisition

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_84728B4C9B3AF0A5:demo)

## Follow-On Process Steps of the Purchase Requisition

Now that you have manually created a purchase requisition to procure the materials needed to produce the new e-bike, continue with the following on processes:

1. Convert the purchase requisition into a purchase order. For this, you need to know where to buy the product and you need to enter the price manually.
2. Use the purchase requisition to create several requests for quotation to be sent to several suppliers. You will receive some quotations, including the conditions for the delivery. This could be processed directly in the S/4HANA system. Based on the quotes, you have the option to create purchasing info records or a contract with a preferred supplier. You can then create a follow-on purchase order.
3. Transfer the purchase requisition to SAP Ariba and process the request for quotation (RFQ) and quote in SAP Ariba.

## How to Process Request for Quotation

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6E3702716C781DBF:demo)

## Purchasing Info Record

A purchasing info record is a master data record that is used for the sourcing process. It combines the product and the supplier and is created with a reference to a purchasing organization. Optionally, it can also be maintained at the level of the plant. In addition to the purchasing info record we can maintain conditions. Conditions are possible pricing elements that could be valid for the purchasing process. For example, the price of the product, rebates or fright costs that apply.

The conditions are stored in separate master data records.

![The image depicts the connection between a supplier, a product master, and an info record in a procurement system. The info record consolidates key details such as the supplier ID, material ID, purchase organization, planned delivery time, pricing conditions (e.g., price per unit, freight, and discount), and the last purchase order, serving as a reference for procurement processes.](https://learning.sap.com/service/media/topic/aeba80b0-21d5-45c9-8859-37ee3b18eacd/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L3_PurchasingInfoRecord.png "The image depicts the connection between a supplier, a product master, and an info record in a procurement system. The info record consolidates key details such as the supplier ID, material ID, purchase organization, planned delivery time, pricing conditions (e.g., price per unit, freight, and discount), and the last purchase order, serving as a reference for procurement processes.")

## SAP Ariba Alternative

As an alternative, you can use the SAP Ariba solution to process some procurement steps or the entire procurement process.

As already seen in the process flow in lesson 2, we can create purchase requisitions in SAP Ariba. For this, we use catalogs from the SAP Guided Buying for SAP S/4HANA buying and create shopping carts. The created request would be forwarded to an approver (if necessary) and then be used as input to create a purchase order.

Please have a look at the illustration that Penelope has prepared for you.

![The image illustrates the integration process between suppliers, SAP Ariba Procurement, and ERP systems within a trading partner community, focusing on key procurement and invoicing workflows such as catalog sharing, purchase orders, order confirmations, shipping notifications, receipts, invoices, and remittance advice. The details of the data flow and system interactions are described further in the accompanying text.](https://learning.sap.com/service/media/topic/a9a166c5-973d-47b8-b385-b57f8fae4bd9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L3_SAP_AribaAlternative.png "The image illustrates the integration process between suppliers, SAP Ariba Procurement, and ERP systems within a trading partner community, focusing on key procurement and invoicing workflows such as catalog sharing, purchase orders, order confirmations, shipping notifications, receipts, invoices, and remittance advice. The details of the data flow and system interactions are described further in the accompanying text.")

# Describing Contract Management

Objective

After completing this lesson, you will be able to explain purchasing contracts and their use

## Introduction

We are now moving on to the business process step **Contract Management** as selected in the graphic below.

![This image provides an overview of the Source-to-Pay process, highlighting that the current focus is on the Contract Management phase, specifically managing contracts and processing quotes in Ariba.](https://learning.sap.com/service/media/topic/a30e2ee9-4051-49ed-b1ba-56211ae6e435/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%202.png "This image provides an overview of the Source-to-Pay process, highlighting that the current focus is on the Contract Management phase, specifically managing contracts and processing quotes in Ariba.")

## Overview of Contract Management

As the bike company in our example aims to establish long-term relationships with their preferred suppliers, they create **Outline Purchasing Agreements.**

An Outline Purchasing Agreement is a long-term agreement with a supplier covering the supply of materials or the provision of services, subject to predetermined conditions.

These agreements do not contain data on specific delivery dates or quantities to be delivered. Depending on the type of agreement, this data is transmitted to the supplier different ways.

There are two ways data can be transmitted to the supplier:

- Contract
- Scheduling Agreement

Explore the main differences in using these kind of outline agreements in the table below.

#### Outline Agreements

||Contract|Scheduling Agreement|
|---|---|---|
|Document Volume|When using a contract, you create a new purchase order in the system each time you release goods or services against the contract.|When using a scheduling agreement, there is only one document in addition to the contract document. This document is a delivery schedule line which is extended continuously.|
|Automatic Materials Planning|When using a contract, requirements planning can be set up so that the contract item is automatically assigned to a requisition item as the source of supply. However, the requisition must subsequently be converted in a purchase order (contract release order).|When using a scheduling agreement, you can directly generate scheduling agreement delivery schedules from the planning run, so that no further processing in purchasing is required.|

Contracts and scheduling agreements can be split up even further. Explore the different structures of contract types below.

![The image compares two types of procurement contracts, Quantity Contracts and Value Contracts. Quantity Contracts focus on specified item quantities, and Value Contracts are based on a set monetary value.](https://learning.sap.com/service/media/topic/cce089cf-a836-46fd-9fd2-7c2d8dc93d9c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit6_ContractTypes.png "The image compares two types of procurement contracts, Quantity Contracts and Value Contracts. Quantity Contracts focus on specified item quantities, and Value Contracts are based on a set monetary value.")

![The image presents two types of Scheduling Agreements: one without release documentation, leading directly to schedule lines for item deliveries, and another with release documentation, providing detailed forecast delivery schedules.](https://learning.sap.com/service/media/topic/cce089cf-a836-46fd-9fd2-7c2d8dc93d9c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit6_Types%20Scheduling.png "The image presents two types of Scheduling Agreements: one without release documentation, leading directly to schedule lines for item deliveries, and another with release documentation, providing detailed forecast delivery schedules.")

## How to Create Quantity Contract

To buy the new product, we will create a quantity contract with special conditions. Because we have received a quotation from our preferred supplier, we will use that quotation to create a quantity contract for the Bike Computer.

A contract has a validity period and contains the individual items. As we have agreed on special pricing conditions, we maintain these in the contract

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_9ED1C74984EFFFA8:demo)

# Managing Purchase Orders

Objective

After completing this lesson, you will be able to explain the single process steps of purchase orders

## Introduction

The next business process step to be covered is **Operational Procurement**, highlighted in the overview below.

![The image illustrates the Source-to-Pay process, highlighting various stages from master data setup to reporting. The current focus is on Manage Purchase Order within the Operational Procurement phase.](https://learning.sap.com/service/media/topic/a70194f7-7837-43d1-b9d9-8bf9bd50c9f4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%203.png "The image illustrates the Source-to-Pay process, highlighting various stages from master data setup to reporting. The current focus is on Manage Purchase Order within the Operational Procurement phase.")

## Purchase Order Overview

Having managed individual requirements with purchase requisitions and established a long-term relation with our supplier by using a quantity contract, we now focus on the **creation of purchase orders**.

Purchase orders are part of the operational procurement business process step. To manage the creation of purchase orders effectively, you should consider several things.

- First of all you need to convert the existing purchase requisitions into purchase orders.
- Where possible assign the existing contract
- Furthermore, you should try to streamline the process of purchase order creation as much as possible.

### Sending Purchase Order to Supplier

A purchase order is a formal request to a supplier to supply goods or services with the conditions stated in the purchase order. In the purchase order, you specify whether the material is intended for stock or for direct consumption (like cost center, asset, or project).

The goods receipt and invoice verification are usually carried out on the basis of the purchase order.

A purchase order includes the following data:

- **References**: You can minimize data entry time by creating purchase order items with reference to an existing purchase order, purchase requisition, quotation, or contract.
    
- **Master Records**: If a product master record exists, the material short text, the purchase order unit of measure, and the material group are transferred automatically. If a purchasing info record already exists in the system, a price can be proposed for the purchase order.
    
- **Default Values**: You can enter a purchase order without referring to existing documents in the system. When you enter the purchase order data, the system suggests default values. These are for example the ordering address of the plant.
    
- **Supplier**: If the source of supply is a plant belonging to your company, you carry out a stock transport order. If you order from an external supplier, you create a standard purchase order.
    

### Document Structure of a Purchase Order

Like other purchasing documents in the SAP system, the purchase order consists of a document header and one or more items. This is simplified illustration of the document structure:

![The image shows the structure of a Purchase Order, divided into Header Data (general order-level details) and Item Data (line-by-line details of specific items or services), with numbered lines (10, 20, 30) representing individual items. Further details are provided in the accompanying text.](https://learning.sap.com/service/media/topic/da6da500-aee6-4fcf-b9c7-ae6b8b398c40/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit6_HeaderData.png "The image shows the structure of a Purchase Order, divided into Header Data (general order-level details) and Item Data (line-by-line details of specific items or services), with numbered lines (10, 20, 30) representing individual items. Further details are provided in the accompanying text.")

1. **Header Data**: The document header contains information that refers to the entire purchase order, such as document type, supplier, purchasing organization, purchasing group and company code, currency, the document date, and the terms of payment.
    
    With a single purchase order, you can procure materials or services for different plants. All plants in a purchase order must be assigned to the purchasing organization entered in the purchase order header.
    
2. **Item Data**: The items in a purchase order describe the materials or services ordered. Data required for an item are material/service, order quantity and unit of measure, delivery date, price, and plant for which the material/service is ordered. You can maintain additional information for each item, such as tolerance for over delivery or item-based text.
    
    You can also use the item category to determine the procurement process for each purchase order item. For example, you use the item category, to determine whether it is a special procurement process, such as vendor consignment, subcontracting, or stock transfer.
    

## How to Create a Purchase Order from a Purchase Requisition

Create a purchase order from a purchase requisition with the _Assignment List_ app.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_D83AC434A41DCE81:demo)

## Automatic Creation of Purchase Orders

It is also possible to automate the creation of purchase orders.

For example, if we don’t need any approval when ordering our production materials and we already know our preferred supplier.

Imagine that we order our production materials and don't need any approval and we know our preferred supplier already. In that case we should generate the POs automatically.

A purchase requisition item with an assigned source contains all the information (for example, supplier and price) required for the system to convert it into a purchase order.

![The image depicts the automatic Purchase Order generation process, starting from Supplier and Product Master configuration as prerequisites, followed by defining requisition items with supplier sources, and ending with system-generated purchase orders for relevant suppliers.](https://learning.sap.com/service/media/topic/ad5cc4e9-8a20-4b38-89fa-cb0f5f5f3c11/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L5_Automatic_POs.png "The image depicts the automatic Purchase Order generation process, starting from Supplier and Product Master configuration as prerequisites, followed by defining requisition items with supplier sources, and ending with system-generated purchase orders for relevant suppliers.")

To automatically convert a purchase requisition into a purchase order, the following apply:

- The Automatic Purchase Order indicator must be set in the material master record (purchasing data).
- The Automatic Purchase Order indicator must be set in the supplier master record (purchasing data).
- A valid source of supply must be assigned to the purchase requisition item.
- No additional entries (such as the tax code for automatic goods receipt settlement) are required during conversion.
# Managing Goods Movements

Objective

After completing this lesson, you will be able to recall the basic process steps involved in managing goods movements

## Introduction

We now move on to the business process step **Receiving** starting with the activity **Manage goods movement** as highlighted in the graphic.

![The image illustrates the Source-to-Pay process stages, with the current focus on Manage Goods Movement under the Receiving phase.](https://learning.sap.com/service/media/topic/dc7a81bd-9686-407b-bfec-22c0aa8b90f4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%204.png "The image illustrates the Source-to-Pay process stages, with the current focus on Manage Goods Movement under the Receiving phase.")

After having created the purchase orders, we now check how inventory management works. In general, we need to differentiate in between inventory management in MM and warehouse management in EWM.

Inventory Management in the area of logistics, covers the following tasks:

- Management of material stocks on a quantity and value basis
- Planning, entry, and documentation of material movements
- Carrying out the physical inventory

## Material Stock Management on a Quantity and Value Basis

### Managing Stocks by Quantity

Inventory management maps the physical stock in real time by recording all stock-changing transactions and the resulting stock updates. An overview of the current stock situation of a material is always available. For example, you can differentiate between the following:

- Stock quantities in unrestricted-use stock
- Stock quantities in quality inspection
- Stock quantities already ordered but not yet received
- Stock quantities that are in the warehouse, but that are already reserved by the system for production or for a customer

The storage location is the organizational level on which the material's stocks are managed by quantity. Exceptions are some special stocks that are only managed at plant level (for example, customer consignment stock). Inventory management can also manage many of its own and external special types of stock, such as consignment stocks, separately from the normal stock.

### Managing Stocks by Value

In addition to managing stocks by quantity, stock is also managed by value. With each goods movement, the system automatically updates the following data:

- Stock quantities and stock values for inventory management
- G/L accounts for financial accounting by means of automatic account determination
- Account assignments for cost accounting (provided the internal accounting is active)

The valuation area is the organizational level at which material’s stock value is managed.

Because we will also use the production part of SAP S/4HANA, our valuation level is at the plant level.

## Planning, Entry, and Documentation of Goods Movements

In inventory management, a distinction is made between the different types of goods movements:

- **Goods receipt (GR)** - A goods receipt is a goods movement that is posted with the goods received from external vendors and production. A goods receipt leads to an increase in warehouse stock.
- **Goods Issue (GI)** - A goods issue is a goods movement in which a material withdrawal, material consumption, or goods shipment is posted to a customer. A goods issue leads to a decrease in warehouse stock.
- **Stock transfer** - A stock transfer is a goods movement in which materials are removed from a particular storage location and placed into another storage location. Stock transfers can take place both within the same plant and between two plants.
- **Transfer posting** - Transfer posting is a category of goods movement that is higher than stock transfer. It changes the stock identification or qualification of a material, regardless of whether the posting is linked to a physical movement. Examples of transfer postings include the release of the stock for quality inspection, the transfer posting from material to material, and the transfer of consignment material to own stock.

Take a look at the graphic below, to learn more about goods movements:

![This diagram outlines the inventory management process in a multi-plant setup, showing how stock moves from suppliers and production into unrestricted use, quality inspection, and blocked stock categories within Plant 1, and then is transferred to specific storage locations in Plant 2 for further issuance to production or customers.](https://learning.sap.com/service/media/topic/b26d5ad2-619f-4dd2-86b3-be21b75118c9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L6_PED.png "This diagram outlines the inventory management process in a multi-plant setup, showing how stock moves from suppliers and production into unrestricted use, quality inspection, and blocked stock categories within Plant 1, and then is transferred to specific storage locations in Plant 2 for further issuance to production or customers.")

## How to Post Good Receipt and Display Stock Overview

Post good receipt for a purchase order and display the stock overview.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_752FF19D48AA7997:demo)

## Integration to Finance

While posting the goods receipt for our purchase order (PO), we create a material document and a financial document. FI documents consist of individual line items.

We receive two-line items: As we post a valuated GR for our PO, for the stock material we post a **stock account** (balance sheet account) and the **GR/IR account.**. The GR/IR account ensures that the Goods Receipt corresponds to the Invoice Receipt.

The FI posting is accordingly:

- Debit Stock Account
- Credit GR/IR Account

## How to Show Financial Impact

Show Financial impact – Show Accounting document and process flow

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6492E2A7A06CCA85:demo)

## Test Your Knowledge

Try to answer the following question before you read the reply below.

- **Question:** How to valuate products when posting the goods receipt?
- **Answer:** In the product master record, in the accounting data, you use the price control to decide how you valuate your products. You can decide between two possibilities:
    
    - Moving average price
    - Standard price
    
    Products we produce on our own should be valuated by standard price. For materials we buy, either is possible. That decision should be made with the Controlling and Finance department.

# Explaining Warehouse Processing

Objective

After completing this lesson, you will be able to explain warehouse processing

## Introduction

We will now continue with **Warehouse Processing** which is part of the business process step **Receiving** as highlighted in the graphic below.

![The image outlines the steps in the Source-to-Pay process and indicates the current focus is on 'Managing warehouse processing' within the Receiving stage.](https://learning.sap.com/service/media/topic/de79df0d-36ac-47d8-9ce6-a937d02d652a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%205.png "The image outlines the steps in the Source-to-Pay process and indicates the current focus is on 'Managing warehouse processing' within the Receiving stage.")

## Warehouse Management Overview

In the following, you learn some basics about extended warehouse management and how it differs from inventory management.

### Who Needs a Warehouse Management System?

Depending on the number, variety, and diversity of the products you purchase, sell, or produce, you may have different storage requirements.

Example:

- A mining company that digs ore and sends it directly to a refining factory does not need to store the ore. That company does not need a warehouse.
- A factory that refines ore to produce steel needs a simple warehouse to hold the steel until it is sold to a customer.
- A distributor receiving thousands of products from many manufacturers and distributing those products to hundreds of customers needs a complex warehouse. That warehouse needs to facilitate the following tasks, among others:
    - Track the product received
    - Determine the location to store the incoming product
    - Track current stock levels for each product
    - Before distributing that product, determine the location to retrieve the product from
    - Track distributed product

### What are the Functions of a Warehouse Management System?

A Warehouse Management System enables you to achieve the following:

- Track the amount of a particular good or material that is stored in a warehouse.
- Track the location of every storage bin that holds a particular good or material.
- Control and records all movements of goods and materials in the warehouse.

A Warehouse Management System can also increase warehouse efficiency. It can provide tools to monitor warehouse activities and to plan resource requirements, such as warehouse staff or equipment resources.

Large warehouses, with many storage bins and many different goods and materials, need a Warehouse Management System to be efficient and satisfy customers' needs. They use a Warehouse Management System to perform the following:

- Control the put away of goods and materials that come into the warehouse. The Warehouse Management System determines an available and suitable storage bin in which to store the goods or materials.
- Control the picking of goods and materials to leave the warehouse, for example to fulfill an order. The Warehouse Management System determines a stocked and suitable storage bin from which to pick the material.

## Complex Warehouses

In more complex warehouses, additional functionality can be provided to manage other information or services related to goods and materials, for example:

- Serial number
- Batch number
- Minimum shelf life
- Vendor-managed-inventory (VMI)
- Yard Management
- Value-added service (VAS)

Examples of warehouses with this level of complexity include distribution centers or logistics service providers. Warehouses become more complex as they become responsible for value-added services (VAS) tasks, such as packaging.

If you just need to know how much stock you have, you don’t need a Warehouse Management System. But if you need to track more information about the stock, for example, the location, than you need a Warehouse Management System.

Penelope has prepared an illustration for you, to get a better idea of the process flow in Extended Warehouse Management:

![This diagram illustrates the end-to-end warehouse process, encompassing inbound processing, storage and operations, and outbound processing. Key areas include the Goods Receipt Zone for inbound items arriving via multiple doors, processing into either an automatic high-rack storage area or bulk storage area, and movement to a Clearing Zone if needed. Cross-docking operations facilitate rapid transfers from inbound to outbound areas. The Picking Area supports methods like pick-by-voice, light, or mobile device for customer orders. Outbound processing progresses through Staging Areas for consolidation before shipment via designated doors.](https://learning.sap.com/service/media/topic/f9bbe871-7d5e-442a-94e6-601b87f666ab/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U5_L7_Complex-Warehouses.png "This diagram illustrates the end-to-end warehouse process, encompassing inbound processing, storage and operations, and outbound processing. Key areas include the Goods Receipt Zone for inbound items arriving via multiple doors, processing into either an automatic high-rack storage area or bulk storage area, and movement to a Clearing Zone if needed. Cross-docking operations facilitate rapid transfers from inbound to outbound areas. The Picking Area supports methods like pick-by-voice, light, or mobile device for customer orders. Outbound processing progresses through Staging Areas for consolidation before shipment via designated doors.")

## Extended Warehouse Management (EWM): Organizational Units

EWM helps the bike company in our example store their finished e-bikes and track the serial numbers. Using EWM should support production, sales, and service processes. It might even help track serial numbers for some of the procurement products.

The organizational units in SAP S/4HANA Materials Management, Warehouse Management and Extended Warehouse Management are illustrated in the graphic below.

![This diagram represents the integration of SAP S/4HANA with warehouse management (WM) and extended warehouse management (EWM) systems. It illustrates how a plant (Plant 1010) connects to two storage locations (101D and 101S), which are managed within the warehouse (Warehouse Number 1010). The first layer shows standard warehouse management (WM) operations, while the second layer depicts extended warehouse management (EWM) functionality for enhanced logistics and inventory control.](https://learning.sap.com/service/media/topic/eb598244-e86a-48b7-8463-942780db05fc/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit6_MM_WM_EWM.png "This diagram represents the integration of SAP S/4HANA with warehouse management (WM) and extended warehouse management (EWM) systems. It illustrates how a plant (Plant 1010) connects to two storage locations (101D and 101S), which are managed within the warehouse (Warehouse Number 1010). The first layer shows standard warehouse management (WM) operations, while the second layer depicts extended warehouse management (EWM) functionality for enhanced logistics and inventory control.")

Because EWM is embedded in the SAP S/4HANA system, there are organizational units that we must consider to be in both. Inventory management takes place in materials management and stock is stored in a plant at storage location level.

Although EWM has nothing to do with the SAP Warehouse Management application, both use a warehouse number to represent the physical warehouse in which materials are stored and managed. To activate the warehouse management in the SAP S/4HANA system, the combination of plant and corresponding storage location is linked with the respective warehouse number.

### What can you do with multiple storage locations in a plant?

- Differentiate between the various stocks of material in a plant
- Differentiate between the physical storage characteristics
- Classify the quantities of material in a plant to indicate their use (for example, available for sale) ог perhaps their logical location (for example, at a third-party logistics provider)

Because we need to differentiate between inbound processing and outbound processing, let’s briefly consider the possibility of using EWM in our environment.

While looking at inbound processing, we need to differentiate goods receipt for purchase orders or goods receipt for production orders. For both processes, we can include the integration to embedded EWM.

# Managing Invoices

Objective

After completing this lesson, you will be able to explain the integration of invoice verification with accounting

## Introduction

The next business process step in procurement is **Invoice Management**.

![This diagram outlines the Source-to-Pay (S2P) process, showing key phases like sourcing, contract management, procurement, receiving, invoice management, and reporting. The focus is currently on the 'Invoice Management' phase, specifically highlighting the task of managing invoices, as indicated in yellow.](https://learning.sap.com/service/media/topic/fe2eff33-30a0-469d-82e1-e2c07ed65f5e/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%206.png "This diagram outlines the Source-to-Pay (S2P) process, showing key phases like sourcing, contract management, procurement, receiving, invoice management, and reporting. The focus is currently on the 'Invoice Management' phase, specifically highlighting the task of managing invoices, as indicated in yellow.")

## Invoice Verification Environment

Having processed the goods received for purchase orders, we need to understand the need for invoice verification and the process to follow. As the bike company in our example receives invoices from several vendors, we will have a look at how they can process invoices from multiple suppliers in MM.

Usually, the process invoice posting takes place in Finance. Logistics **Invoice Verification** is part of **SAP S/4HANA Sourcing and Procurement**. Logistics Invoice Verification checks incoming invoices for accuracy with regards to content, price, and accounting. The check occurs at the end of the logistics chain that comprises purchasing, inventory management, and invoice verification

- The main task of Logistics Invoice Verification is to complete the procedure of materials procurement by posting the supplier invoice and passing on the invoice information to Financial Accounting (FI) and subsequent applications.
    
- Logistics Invoice Verification is not an isolated component in the SAP system. It operates in conjunction with the purchasing and inventory management components and accesses data located in these application areas.
    
- You can post an incoming invoice with reference to a PO, a GR, or a service entry. The system suggests the invoice items according to the reference entered, and the corresponding account postings are carried out automatically.
    
- For each incoming invoice, Logistics Invoice Verification creates an MM invoice document and an FI accounting document (also known as an invoice document). These accounting documents record the updates in Materials Management and Financial Accounting.
    

## Invoice Receipt

There are multiple ways to post invoices in procurement.

- Invoices can be created by accounting programs that run regularly.
- Ariba Network integration enables you to collaborate in SAP S/4HANA with your suppliers through Ariba Network.
- Invoices can be transmitted electronically through electronic data interchange (EDI) in intermediate document (IDoc) format, or through the Internet in XML format.
- When the company receives an invoice, you can enter and post them manually.

Read the talk of two procurement experts in the bike company below.

![This diagram showcases the Source-to-Pay process, highlighting stages such as sourcing, contract management, procurement, receiving, invoice management, and reporting. The current focus is on the 'Invoice Management' phase, specifically the task of managing invoices, which is emphasized in yellow.](https://learning.sap.com/service/media/topic/af36c549-7406-4287-9e9c-840a616c21ae/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Dialogue_New2.png "This diagram showcases the Source-to-Pay process, highlighting stages such as sourcing, contract management, procurement, receiving, invoice management, and reporting. The current focus is on the 'Invoice Management' phase, specifically the task of managing invoices, which is emphasized in yellow.")

- **Prashad**: Hey Tom, can you quickly have a look. I understood that, in invoice verification, I first enter all the relevant data from the supplier's invoice, such as gross amount, value-added tax, invoice date, and for reference the supplier's invoice number. Correct?
- **Tom**: Exactly! And based on what I know I suppose that if you enter an invoice with reference to a purchase order, the system proposes data from the purchase order and the goods receipts. For example invoicing party, material, quantity to be invoiced, expected amount per item, and payment terms.
- **Prashad**: Ah, I see. Furthermore, if other values are specified in the supplier's invoice, I can overwrite these proposed values.
- **Tom**: Good to know. And if there were discrepancies between the purchase order or goods receipt and the invoice?
- **Prashad**: I checked that already. If that is the case, the system warns me accordingly and, depending on the system settings, blocks the invoice so that it cannot be paid.
- **Tom**: That makes sense.

Posting an invoice has the following effects in the system:

- The amounts of the individual items are posted to the appropriate accounts.
- An MM invoice document and an FI document are created
- The PO history is updated
- If necessary, the material master is updated

As we have heard already in the goods movement postings there is an impact of the price control to the accounting postings.

## How to Post an Invoice

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_B96EBAA4FB5AB4AB:demo)

# Managing Payments

Objective

After completing this lesson, you will be able to explain the automatic payment process and the impact to accounts receivable

## Introduction

The next business process step is **invoice management** , which is part of **Finance Accounting in SAP S/4HANA**. It is highlighted in the graphic below.

![This diagram outlines the Source-to-Pay process, covering steps from sourcing and contract management to procurement, receiving, invoice management, and reporting. The focus is currently on the 'Manage Payment' task within the 'Invoice Management' phase, highlighted in yellow.](https://learning.sap.com/service/media/topic/a5a0accb-303a-4b6c-9aca-6da14981ea13/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Source-To-PayProcess%207.png "This diagram outlines the Source-to-Pay process, covering steps from sourcing and contract management to procurement, receiving, invoice management, and reporting. The focus is currently on the 'Manage Payment' task within the 'Invoice Management' phase, highlighted in yellow.")

**Scenario:** Having received and posted the invoices in Logistics Invoice Management, the suppliers need to be paid. The payment is not part of the MM department. The payments are managed by the financial department. We will sort the open items by supplier and have a look at how we can manage the payments.

## Payment Management

Watch the following videos to get an overview of the automatic payment program in SAP S/4HANA.

Hi, SAP S/4HANA provides a program to automatically select open

invoices that are due to be processed for payment. During the invoice

to pay process, this program can be scheduled periodically to

efficiently process the necessary payments, taking into consideration

the payment due dates, cash discount and other invoice related data.

Let me quickly show you how this works.

The program requires a one-time basic configuration to help determine

the best method and bank to select when processing payments.

Periodically, you would schedule this program

to select the items that are ready for payment.

This can be filtered by several different attributes

of the vendor invoices such as the vendor ID,

payment due date, company code and payment type among others.

Once the items are selected, the system will calculate

the payment amount for each payment document needed.

This process will consider any cash discounts that

can be taken based on the payment terms of each item.

After the payments have been calculated, the system

will post the documents in the Vendor account,

subledger, and the relevant general ledger accounts in the main ledger.

The postings are similar to that of the manual outgoing payment.

Finally, the system will create the needed payment medium to

physically execute the payment. The medium could be an electronic

data exchange file that the bank can use to process electronic

payments, or a file used to print physical checks, for example.

The medium output can happen either manually or automatically.

The next video shows the individual steps of the payment program run in more detail.

Listen to my colleague Stefan to learn how

payments are processed in SAP S/4HANA.

The Payment Processing Program contains several steps. Each payment

run is identified by the run date and the run identification.

After identifying the payment run, the desired parameters for

the payment run must be entered. This step contains the answers

to the questions, which open items are to be selected to be

evaluated for payment, which payment method will be used, when will

the payment be made, which company codes are to be considered,

when is the next payment run to be scheduled.

Each of these items are necessary to correctly select the

invoices requiring payment prior to the next payment run.

Once the parameters have been saved, you can optionally schedule

a payment proposal that will process the invoices with the

parameters given and allow for review prior to the payment

being processed. When the proposal is generated, you can review

the data and make changes as needed, such as not paying a

particular invoice during this run, or in some cases, paying an

invoice that has had a payment block placed on it previously.

The proposal will also report any open invoices that cannot

be paid due to document issues or payment block settings.

A proposal can be deleted and re-ran as many times is needed.

After reviewing and editing the payment

proposal, you can schedule the payment run.

This step will process the payments in the subledger and close the open

items processed and post the required documents in the main ledger.

Once the payments have been processed,

you can automatically use a print program to generate the

payment medium. The medium could be an electronic data exchange

file, a data medium exchange file, or a check print file.

## Execute a Payment Run

## How to Post an Outgoing Payment

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_A26919903CD238BE:demo#29903CD238BE:demo%232)

------- ADDITIONAL QUIZ QUESTIONS -------

NOTE: "The following are all the questions for this specific module. Below each number, there are instructions/questions and a list of answers. (X) denote correct answers. Brackets ("[]") denote additional comments for that specific question.

1.
What are examples for outline agreements?
There are two correct answers.

Quality Contract

Purchase Order

(X) Scheduling Agreement

(X) Value Contract

2.
What happens when a supplier invoice is posted in SAP S/4HANA in logistics invoice verification?
There are two correct answers.

The supplier account is cleared

The supplier account is debited

(X) The supplier account is credited

(X) The GR/IR account is cleared

3.
What are exclusive benefits of using EWM in SAP S/4HANA?
There are two correct answers.

Post goods receipt

(X) Process putaway process

Manage stock at storage location

(X) Manage stock at bin level

4.
For which enterprise structure do you need to create the supplier master data record to use in the purchasing process?
There are three correct answers.

(X) Company Code

Controlling Area

(X) Purchasing Organization

Plant

(X) Client

5.
What is the impact of posting a supplier’s invoice?
There are three correct answers.

(X) The purchase order history is updated.

(X) An open Item for the supplier is created.

The quantity of stock is adjusted.

The payment is processed.

(X) A logistics invoice document is created.

[Invoices do not affect stock quantities and payment is a follow on process.]

6.
For ordering materials via a scheduling agreement you create a purchase order with a reference to the scheduling agreement.
Choose the correct answer.

True

(X) False

[To order materials with a reference to a scheduling agreement you generate a scheduling agreement delivery schedule.]

7.
A customer wants to know which SAP solutions facilitate the source-to-pay process. What is the correct answer?
There are two correct answers.

SAP Success Factors

(X) SAP Ariba

SAP IBP

(X) SAP S4/HANA

SAP Concur

8.
What are possible purchasing processes defined via the item category?
There are three correct answers.

(X) Consignment

Consumption

(X) Subcontracting

(X) Service

Investment

9.
Which enterprise structures are allocated to the header of a purchase order?
There are two correct answers.

Plant

Purchasing Group

(X) Purchasing Organization

(X) Company Code

Storage Location

10.
Which accounts does the system update when you save a goods receipt for a stock material?
There are two correct answers.

Supplier account

Consumption account

Asset account

(X) Stock account

(X) GR/IR account

11.
What is the impact of an outgoing payment?
There are two correct answers.

(X) A financial document is created

(X) The Supplier’s account is cleared

A material document is created

The product master is updated

The price of the product is adjusted

12.
What master data records are used in a purchase order?
There are three correct answers.

(X) Purchasing Info Record

Purchasing Group

(X) Supplier

(X) Product

Shipping Conditions

13.
A customer asks you which enterprise structures are required from a procurement perspective. What is the correct answer?
There are three correct answers.

Operating Concern

Purchasing Group

(X) Purchasing Organization

(X) Plant

(X) Storage Location

14.
Where do you assign a warehouse (WM) in SAP S/4HANA to the enterprise structures?
Choose the correct answer.

Plant

Storage location

Company code

Plant-Storage location combination

15.
What are required data when entering a goods receipt?
There are two correct answers.

Delivery note

Movement type

Storage location

Storage bin

Material document number