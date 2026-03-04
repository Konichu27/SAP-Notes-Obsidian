# Understanding the Basics of the Sales Process

Objective

After completing this lesson, you will be able to describe the sales process, the organizational levels, and the systems used in sales

## Introduction

In this lesson you will learn more about the sales process and the organizational levels and master data relevant for sales.

**Scenario:** The implementation project of the bike company we use in our example is currently in the _Realization_ phase, in which the end-to-end processes are tested by the project team. The selected scope items for each area were assigned to the business processes. Have a look at a high-level overview of the steps below.

![This diagram outlines the Lead-to-Cash sales process, highlighting stages including Master Data, Presales Activities, Order Processing, Product Delivery, Invoicing, and Money. Each of these stages will be described in detail below.](https://learning.sap.com/service/media/topic/d4ebb5c0-faf9-495d-90bf-6fb8176f8f77/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Overview.png "This diagram outlines the Lead-to-Cash sales process, highlighting stages including Master Data, Presales Activities, Order Processing, Product Delivery, Invoicing, and Money. Each of these stages will be described in detail below.")

- **Master Data** in the sales process refers to core business information such as customer, product, condition, and output data. It enables an efficient sales process, ensures accuracy and consistency of data for better customer management, and effective sales analysis and reporting.
    
- **Presales Activities** refer to the set of tasks and processes that a sales team undertakes before closing a sale. These activities are designed to help the sales team understand the customer's needs. This helps to build relationships with potential customers and position the company's products or services in the best way possible.
    
- **Order Processing** occurs after the customer has agreed to purchase a product or service. This step includes order receipt and validation, inventory and pricing checks, and order confirmations sent to the customer. This involves a series of tasks and activities that ensure that the customer's order is processed efficiently and accurately, while also managing the business's resources and maintaining profitability.
    
- **Product Delivery** refers to the process of physically transporting, digitally transporting, or providing access to the product to the customer. Key steps to effectively manage a sales order's delivery are to create a delivery schedule, accounting for lead times, shipping times, and other factors that could affect the delivery timeframe. Running an efficient warehouse can ensure a clear focus on cost control and quality control, while also complying with required regulations and safety standards.
    
- **Invoicing** is a crucial part of the sales process as it triggers the accounts receivable process. It ensures that the company is attempted to be paid for the goods or services it provides and it helps to keep accurate financial records. This typically refers to the process of creating and sending a bill or invoice to a customer for goods or services that have been purchased
    
- **Money** processing is a crucial step that ensures that the company is paid. Incoming payments can be tracked, recorded, and reconciled. This process also works with bank accounting, disputes management, and collections processing. Once payments are recorded, they are deposited into a bank account to be reconciled to compare and match invoices from customers to ensure no discrepancies.
    

Before you learn more about the individual process steps in sales, you should familiarize yourself with the enterprise structure and master data from the perspective of Sales and Distribution.

The graphic below shows which SAP solution components are covered in this lesson.

![This diagram provides an overview of the SAP solution landscape with a focus on Sales. It highlights key components such as SAP CX (Customer Experience) and the SD (Sales and Distribution) module within SAP S/4HANA. The integration of these components into the broader SAP ecosystem, including the SAP Business Technology Platform, will be explained in detail below.](https://learning.sap.com/service/media/topic/d4ebb5c0-faf9-495d-90bf-6fb8176f8f77/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation_6.png "This diagram provides an overview of the SAP solution landscape with a focus on Sales. It highlights key components such as SAP CX (Customer Experience) and the SD (Sales and Distribution) module within SAP S/4HANA. The integration of these components into the broader SAP ecosystem, including the SAP Business Technology Platform, will be explained in detail below.")

This lesson focuses on the end-to-end sales process. There are two possible systems that can be used in Sales:

Originally, the entire order-to-cash process took place in the SAP S/4HANA module Sales and Distribution (SD). Additionally, the presales process can be started in SAP Sales Cloud, a Customer Relationship Management (CRM) system. This integration links presales documents like Lead, Opportunity, and Sales Quotes to Sales Orders. The SD module can then take the sales order and start delivery processing.

## Enterprise Structure

An enterprise structure is implemented in SAP Sales and Distribution to help organize and manage business operations within the system. It is used to define the various organizational units within a company and their relationships to one another, including sales and distribution channels, plants, storage locations, and more.

The enterprise structure in SAP Sales and Distribution allows for the segregation of data and processes according to the different organizational units, enabling businesses to manage their operations more effectively. For example, a company may want to manage their sales and distribution for different regions or countries separately, and the enterprise structure allows them to do this within the same system.  

Additionally, the enterprise structure in SAP Sales and Distribution also enables businesses to assign specific responsibilities and authorize access to different organizational units.  

Let’s revisit the enterprise structure in SAP, but from the perspective of Sales and Distribution (SD). The following graphic shows the interconnected elements of the enterprise structure.

![This diagram displays the key organizational elements in SAP Sales and Distribution (SD), including Company Code, Sales Area, Storage Location, Shipping Point, and Delivery Plant. These interconnected components form the structure necessary for managing and executing sales processes efficiently.](https://learning.sap.com/service/media/topic/aea3dca2-54ef-4b51-bca1-9119a8415fbd/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit7_Enterprisestruc.png "This diagram displays the key organizational elements in SAP Sales and Distribution (SD), including Company Code, Sales Area, Storage Location, Shipping Point, and Delivery Plant. These interconnected components form the structure necessary for managing and executing sales processes efficiently.")

- **Company Code:** Company code has already been introduced as an organizational level in Financial Accounting. It is important to link sales and distribution to accounting, one or more sales organizations can be assigned to a company code. However, the sales organization can only be assigned to one company code.
    
- **Sales Area:** A sales area is a combination of a sales organization, a distribution channel, and a division. A sales area defines the distribution channel that a sales organization uses to sell products from a certain division. When processing the Sales and Distribution documents, the system accesses master data according to the sales area. For our Bike Company, we have a Sales Organization in each subsidiary. The distribution channels are direct retail sales, internet sales, and reseller sales.
    
- **Delivery Plant:** The delivery plant is assigned to the combination of Sales Organization and Distribution Channel. Several plants can be assigned to one combination. One plant can be assigned to several combinations of Sales Organization and Distribution Channel. The Bike Company has several distribution centers that manage their shipping, along with warehouses that utilize SAP EWM (Extended Warehouse Management). In the system, a plant can be designated as a distribution center or store for retail or wholesale purposes.
    
- **Shipping Point:** A shipping point is the responsible enterprise structure for the entire shipping process. One plant can have several shipping points. One shipping point can be assigned to several plants.
    
- **Storage Location:** A storage location is an organizational level of Materials Management (MM). This is where sales stock will physically be stored until ordered and delivered to the customer. One or more storage locations can be assigned to a plant. When implementing EWM, a warehouse number is a combination of Plant and Storage Locations organizational levels.
# Using Master Data in Sales

Objective

After completing this lesson, you will be able to extend the master data relevant for sales

## Introduction

In SAP Sales and Distribution, master data refers to the fundamental data elements that are used to support business transactions and processes. This includes data such as material master data, customer master data, and pricing master data.

The respective scope items are highlighted in the graphic below

![Process diagram titled 'Lead-to-Cash' (Sales) outlining stages from Master Data to Money, with the 'Master Data' section highlighted, showing its components: Customer, Product, Condition, and Output.](https://learning.sap.com/service/media/topic/add344eb-44e0-407c-8087-a3c91cfb7ddb/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_1.png "Process diagram titled 'Lead-to-Cash' (Sales) outlining stages from Master Data to Money, with the 'Master Data' section highlighted, showing its components: Customer, Product, Condition, and Output.")

**Scenario:** The bike company in our example has procured materials and produced the new e-bike. Enough stock is stored in the warehouse to start selling them. They now need to sell the bike to their customers.  

## Customer Master Data Record

Imagine you already created the business partner _FI Customer_ and assigned it to the record-to-report process. Now, you want to extend that business partner so that it can be used in the **lead-to-cash** process. What do you do?

In the business partner concept, a master data record consists of different roles. You assign the relevant sales area information as illustrated in the figure below.

![Diagram showing the structure of a Business Partner Record, starting with the General Role and branching into two roles: 1. 'FI Customer (per Company Code)' and 2. 'Customer (per Sales Area),' which lead to specific sales areas (Sales Area A and Sales Area B). Details of roles 1 and 2 will be explained in the text below.](https://learning.sap.com/service/media/topic/a24396c2-8525-4f26-b421-13f34d40b855/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_BPRecord.png "Diagram showing the structure of a Business Partner Record, starting with the General Role and branching into two roles: 1. 'FI Customer (per Company Code)' and 2. 'Customer (per Sales Area),' which lead to specific sales areas (Sales Area A and Sales Area B). Details of roles 1 and 2 will be explained in the text below.")

1. The **Fl customer** role data is relevant for accounting. It is valid for the respective **company code**. In the role FI Customer, you enter the reconciliation account in the general ledger.
    
2. The **customer** role is extended by the **sales area**, which means that each sales area might have different shipping, billing, and sales information for the same customer. Sales areas consist of three fields from the enterprise structure: Sales Organization, Distribution Channel, and Division. When these three fields are used together, it makes a combination that SAP refers to as the sales area.
    
    - Sales Area A (Sales organization US, distribution channel wholesale, division bikes): In this sales area, partial deliveries are allowed, and shipping conditions are immediate. Wholesales business might have different terms than online or retail terms.
        
    - Sales Area B (Sales organization US, distribution channel online, division bikes): In this sales area, partial deliveries are not allowed, and shipping conditions are standard
        

### Summary

The customer role data is relevant for sales and distribution. It is valid for the respective sales area (sales organization, distribution channel, and division). It includes all data necessary for processing orders, deliveries, invoices, and customer payments. You can decide to either maintain many roles at once, or to add roles later, whenever you need them.

You are now ready to extend the business partner with customer role on your own.

## How to Extend BP Roles for Customer Master Data

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_731417FACCFBDD98:demo)

## Product Master Record

If you want to sell materials for the bike company that we use as example, you need to ensure that the product and all the sales-related details of that product are created in the system. Product master records (also called material master records) can be used to automatically populate fields with stored data whenever they are used.

**Scenario:** You created the product master record already for accounting, planning, and production. Now, it needs to be extended for sales. To do this, the e-bike master record needs to be changed in order to have specific settings for the sales organizations that will be selling the bike. These are details such as pricing, packaging, and transport within the plants that will be delivering it.

Because product master record data is stored and recorded globally, you need to extend the data locally for data maintenance. You must maintain the data for the sales organizations that sell the bike and the plants that plan and store the bike as inventory.

The concept of product master record is illustrated in the graphic below.

![The image illustrates the hierarchical structure of a Material Master Record and its association with localized data across different entities. The Material Master Record branches into two levels: Plants (e.g., Plant A and Plant B) and Sales Organizations (e.g., Sales Organization A and Sales Organization B). Each branch connects to corresponding localized data relevant to the specific plant or sales organization.](https://learning.sap.com/service/media/topic/fa6e4a0a-4d64-4775-a98e-e6d284149407/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_MMRecord.png "The image illustrates the hierarchical structure of a Material Master Record and its association with localized data across different entities. The Material Master Record branches into two levels: Plants (e.g., Plant A and Plant B) and Sales Organizations (e.g., Sales Organization A and Sales Organization B). Each branch connects to corresponding localized data relevant to the specific plant or sales organization.")

- **Material Master Record**: The material master data is stored and recorded globally, then extended to local areas for data maintenance.
- We can sell our bikes for example from multiple plants:
    - **Plant A** might transfer and load their bikes with a forklift.
    - **Plant B** might transfer and load the same bike model with a crane.
- We also have several sales organizations:
    - **Sales Organization A** is for example US Sales. They price the bike at a specific price in US dollars and use packaging material they buy locally.
    - **Sales Organization B** is for example German Sales. They price the bike in Euro and use packaging material they buy locally.
- As the graphic illustrates, the type of **localized data** can be recorded for each, even though the product is stored as just one master data record.

The product master recorded can be structured in different views according to the needs of different departments. Each department is allocated views (data tabs - grouping of fields) that contain the information necessary for that department.

As changes to the product are needed, the sales department is responsible for extending the master data to new views. This material will be managed as inventory after it is produced, so, storage data is also necessary.

The graphic below shows the different information types for the product master record.

![The image illustrates the structure of a product master record, emphasizing how it is organized into various functional views such as basic data, purchasing, MRP, accounting, and sales, among others, to support different business processes.](https://learning.sap.com/service/media/topic/fa6e4a0a-4d64-4775-a98e-e6d284149407/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_PMR.png "The image illustrates the structure of a product master record, emphasizing how it is organized into various functional views such as basic data, purchasing, MRP, accounting, and sales, among others, to support different business processes.")

Now you have a good overview of the product master record. Because the product has already been created, there is no need to determine the material type again. Those details are stored globally and will apply to all local areas that would like to sell the product.

The E-Bike is material type FERT, for Finished Product. It is produced by using raw material (RAW) and semi-finished products (SEMI).

## How To Display Material for Sale

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_E7DE597735C4DA90:demo)

## Condition Master Record

The condition master data includes prices, surcharges and discounts, freight, and taxes as illustrated in the graphic below.

![The image provides an overview of condition master data, showcasing key categories such as prices, surcharges and discounts, freight, and taxes, which are used to define pricing elements in business transactions.](https://learning.sap.com/service/media/topic/f1e8d7dc-9232-4f7d-80d2-459e7325c975/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L3_Condition_Master_Record.png "The image provides an overview of condition master data, showcasing key categories such as prices, surcharges and discounts, freight, and taxes, which are used to define pricing elements in business transactions.")

You can define condition master data (condition records) to be dependent on various data. You can, for example, maintain a material price per customer or define a discount to be dependent on the customer and the material pricing group.

Building conditions allows for the creation of pricing procedures. These procedures perform sales order pricing based on the condition records found in the system.

## How to Create a Condition Master Record

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_DF7BF0E94E935EB2:demo)

## Output Master Data

**Scenario:** As a last step, you want to send an order confirmation to the customer.

The data for this confirmation is stored in the output data master. The output is information that is sent to the customer via various media such as mail, EDI or fax. An example of an output is the printout of an order confirmation.

The following chart shows the data flow.

![The image illustrates how output master data is used in a sales order process to generate an order confirmation, detailing the output type, transmission medium, partner function, and specific order information such as items, quantities, and total value.](https://learning.sap.com/service/media/topic/d898d6df-8ae4-471d-a8ab-ab8f5efcc81c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_OutputMD.png "The image illustrates how output master data is used in a sales order process to generate an order confirmation, detailing the output type, transmission medium, partner function, and specific order information such as items, quantities, and total value.")

- **Output Master Data:** When creating an order for a customer, you must consider transport agreements, delivery, and payment conditions, and so on, with business partners. To avoid re-entering this information each time for every activity related to these business partners, relevant data for the activity from the master record of the business partner is simply copied.
- **Sales Order:** When performing each transaction, applicable organizational elements must be assigned. Assignments to the enterprise structure in the document are generated in addition to the information stored for the customer and material.
- **Order Confirmation:** All of this data can subsequently be captured in the output, which is likely to be a PDF document or electronic document.

The Order Confirmation is now ready to be sent to the customer.

# Describing Presales Activities

Objective

After completing this lesson, you will be able to explain the presales process steps in SAP Sales Cloud

## Introduction

This lesson covers the following scope items within the lead-to-cash process:

![The image depicts a Lead-to-Cash sales process overview, highlighting the current stage—Presales Activities—focused on leads, opportunities, and quotes within the broader workflow of master data, order processing, product delivery, invoicing, and payments.](https://learning.sap.com/service/media/topic/f47a8ec5-9d3f-44a4-86d7-64d26a0730bd/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_2.png "The image depicts a Lead-to-Cash sales process overview, highlighting the current stage—Presales Activities—focused on leads, opportunities, and quotes within the broader workflow of master data, order processing, product delivery, invoicing, and payments.")

The goal of these process steps is a sales document. A sales document gathers all important data and keeps a record of the business transaction. Throughout the business process, each document can be linked to the next to show the flow of the process – the big picture.

In this lesson, we focus on SAP Sales Cloud. The integration with SAP S/4HANA provides a clear 360-degree view of customer interactions for marketing, sales, and distribution activities.

## SAP Sales Cloud

**Scenario:** The bike company in our example has sales teams out in the field. They need a way to easily access their customer information, even when they are offline. They also need a way to quickly create quotes and sales orders without a laptop, as well as looking up past orders and delivery information for their customers. Meetings and interactions with their customers aren’t tracked or linked to any active sales targets. Another important need is to know what bikes are in stock so that they don’t sell what they do not have. Stock visibility is key!

With SAP Sales Cloud, sales representatives can use a mobile app as illustrated in the following graphic.

![The image highlights the capabilities of SAP Sales Cloud, showcasing how it provides mobile access to critical sales functionalities, including customer master data, sales documents, payment data, stock availability, delivery status, contacts, email, and task synchronization.](https://learning.sap.com/service/media/topic/d94b3bef-7a67-41cc-ab91-e1b6d46a4c87/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_SAP_Sales_Cloud.png "The image highlights the capabilities of SAP Sales Cloud, showcasing how it provides mobile access to critical sales functionalities, including customer master data, sales documents, payment data, stock availability, delivery status, contacts, email, and task synchronization.")

The mobile app can be used to store customer master data, enter sales documents, or look up past sales documents to check their delivery status. There is also integration with Outlook, Gmail, and Lotus Notes for calendar, email, contact, and task synchronization. Any meetings with a customer can be linked to the sales document or deal they are referencing, better track the sales cycle, and be used in analytics and reports. Stock availability checks and credit checks can be performed to ensure the sales representatives are selling in-stock products to customers with a favorable payment and credit history.

### SAP Sales Cloud as part of the SAP Customer Experience (CX) Portfolio

SAP offers the SAP Sales Cloud to capture presales related data. This way, the entire relationship and all interactions with a customer are recorded as SAP Sales Cloud is part of the SAP Customer Experience (CX) Portfolio.

![](https://learning.sap.com/service/media/topic/d94b3bef-7a67-41cc-ab91-e1b6d46a4c87/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_SC_Portfolio.png)

SAP Intelligent Sales Execution is the built-in analytics of SAP Sales Cloud. It provides embedded graphical analytics that monitor sales opportunities. Machine Learning is activated for lead and opportunity scoring, showing a numerical value for the statistical chance of the Lead or Opportunity becoming a firm sales order.

### Benefits

How can the bike company in our example benefit from SAP Sales Cloud?

Imagine that before implementing SAP Sales Cloud, the company was facing the following issues:

- Sales representatives wanted to sell bike models with parts that had been on backorder for some time, not knowing that they had other bike models in stock waiting to be sold.
- Instant information about shipping was missing.
- Order delivery was not tracked.
- Sales representatives were not able to see when their customers had been invoiced.
- Warehouse personnel and the billing department were overwhelmed with constant calls and messages from sales representatives due to poor insight into the business process.
- Sometimes sales representatives deviated from the standard pricing and processes and created their own quotes for a particular customer. This could be costly for the company and risky for the bike customers.

After implementing SAP Sales Cloud, the entire process runs much more efficiently:

- Sales representatives can do all of their day-to-day tasks and customer orders from anywhere, at any time.
- Customers get an optimal shopping experience with speedy and accurate delivery.
- Going forward, the process will be as automated as possible.
- In case of a huge order placed by a big box customer, the bike company is ready to keep them coming. Keeping their business will help their own business.

## SAP Sales Cloud Sales Cycle

The following figure illustrates the sales cycle in SAP Sales Cloud with nine steps:

![The image outlines a sales process workflow, starting with a lead qualifier identifying hot leads, followed by sales representatives managing leads, planning activities, qualifying opportunities, creating quotations, and recording customer decisions, with a sales manager overseeing win/loss analysis.](https://learning.sap.com/service/media/topic/f59addf7-6f12-42ac-ade6-f18d1529f2ad/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_Sales_Cycle.png "The image outlines a sales process workflow, starting with a lead qualifier identifying hot leads, followed by sales representatives managing leads, planning activities, qualifying opportunities, creating quotations, and recording customer decisions, with a sales manager overseeing win/loss analysis.")

- The first sales document is the **lead.**. When a lead is created, it can occur in many ways. It can come from interactions types such as marketing promotions, clicking on emails, or even trade show interests shown by a prospect or existing customer.
    
- Once the lead is qualified, the next sales document can be created: the **opportunity**. An opportunity might have many sales representatives or an entire sales team working simultaneously.
    
- Having a sales cycle is very important to assist each sales employee with their activities required to reach the **quotation** phase and an agreement for **sales order**.
    

The entire process can be monitored for analysis.

## From Lead to Opportunity

A lead is a potential sales contact. It can be for an individual (B2C) or organization (B2B). Leads are generated through a referral or through a direct response to an advertising or marketing campaign.

​​Below you see the lead functions in SAP Sales Cloud.

![The image showcases the lead management functionality within SAP, emphasizing features such as lead routing and forwarding, various ways to create leads (manual entry, system integration, or business card scanning), and helpful lead creation tools like LinkedIn Sales Navigator, product information, attachments, and other resources to assist the sales team in progressing with leads.](https://learning.sap.com/service/media/topic/c100461d-ad7c-4d81-b92b-f85d978204d6/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_Lead.png "The image showcases the lead management functionality within SAP, emphasizing features such as lead routing and forwarding, various ways to create leads (manual entry, system integration, or business card scanning), and helpful lead creation tools like LinkedIn Sales Navigator, product information, attachments, and other resources to assist the sales team in progressing with leads.")

Qualified leads can be converted to opportunities, with all the key information flowing automatically from lead to opportunity for further processing​​.

A link between the two documents is established for referencing, as well as reporting. An audit trail of changes is logged automatically for key information updates. Feeds are posted automatically for these changes, and key stakeholders and people following the leads are automatically notified of the changes.

Play the video to see the steps from Lead to Opportunity in the SAP system.

## From Opportunity to Quote

An Opportunity is a sales document that collects the customer (sales prospect), their requested products and services, the total volume of the customer project, the expected sales volume, and an estimated sales probability. ​

This information becomes more and more concrete throughout the sales process and is updated regularly.​

Here you can see an Opportunity in SAP Sales Cloud:

![The image demonstrates the opportunity management functionality within SAP, highlighting key features such as the Estimated Deal Value for sales pipeline and commission planning, a detailed view of all Products included in the sales opportunity, and Involved Parties, which shows the internal sales team, the customer, and decision-makers associated with the opportunity.](https://learning.sap.com/service/media/topic/b18dda98-28cd-4fa4-a64e-d4fcac11e2aa/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_Opportunity.png "The image demonstrates the opportunity management functionality within SAP, highlighting key features such as the Estimated Deal Value for sales pipeline and commission planning, a detailed view of all Products included in the sales opportunity, and Involved Parties, which shows the internal sales team, the customer, and decision-makers associated with the opportunity.")

​Collection of this data allows for the correct sales team to be formed in order to win the deal. Once the sales team has been formed, a sales methodology, or sales cycle, can be followed. A sales cycle is broken down into phases, each phase with specific tasks and activities that need to be performed in order to further the deal. ​

You can connect business opportunities with tools to manage activities, sales teams, competitors, surveys, and relationships.​ You can use the Buying Center to manage relationships and understand the influencers of a particular deal. But most importantly, you can enable guided selling. This enables you to walk your sales team through the steps required to create quotations and sales orders. Knowing the steps and tasks needed to complete the process is key for streamlined information gathering, fast turnarounds, to evolve the opportunity, and continue the sales cycle.​

Once you have qualified an opportunity and created a value proposition for the sales deal, you are ready to create a quote.​

​To keep a full sales cycle document flow, converting an opportunity to a sales quote captures the full history of the business interaction.

Play the video to see how an opportunity is converted into a quote in the SAP system.

## From Quote to SAP S/4HANA Sales Order

Flexible quoting capabilities enable you to deliver compelling offers to customers and prospective customers, provide consistent accurate pricing, and streamline the sales process​.

Once a sales quote is accepted, it can be converted to a sales order. Any details, products, or pricing you have in the quote will be replicated to the order in SAP S/4HANA. A document flow captures all documents in a lead-to-cash business process and their document statuses. The documents are linked together in chronological order for easy interpretation of what occurred on certain dates in the business process. ​

Here you can see a quote in SAP Sales Cloud:

![The image shows SAP quote management features: Full ERP pricing and material availability checks, approval workflows, customizable quotation output designs, and tools for easy product maintenance.](https://learning.sap.com/service/media/topic/af4fc914-4d84-4eb1-913e-addcef0335ff/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_Quote.png "The image shows SAP quote management features: Full ERP pricing and material availability checks, approval workflows, customizable quotation output designs, and tools for easy product maintenance.")

A quotation could be a follow-up document for a sales lead or opportunity. This would link the quote to those documents, as well as any activities, such as phone calls or appointments, that were made about the quotation. After the quotation is created, subsequent documents, such as sales order or other activities could be linked to maintain the process flow. ​

Once a sales order is replicated to SAP S/4HANA, the delivery documents and billing documents can appear in the document flow of the sales order. This will show a PDF overview of those documents in SAP Sales Cloud. This is a great way for a sales representative to understand the entire flow of the business scenario surrounding a certain customer. ​

​Play the video to see how to convert a quote into a sales order.

## Integration Scenarios for SAP Sales Cloud and SAP S/4HANA

SAP provides two solutions for sales: The SAP Sales Cloud and SAP S/4HANA Sales. These solutions can work together. Quotation, order, pricing, and material availability data is shared between both systems, so document creation is seamless.

This is an example of a possible process flow by integrating SAP Sales Cloud with SAP S/4HANA:

![The diagram demonstrates the integration between SAP Sales Cloud and SAP S/4HANA, showcasing the end-to-end sales process, including opportunity creation, sales quoting, and order management in the Sales Cloud, as well as delivery, sales contracting, and customer invoicing in S/4HANA, supported by real-time pricing, material availability, and credit checks](https://learning.sap.com/service/media/topic/c52d9222-139c-4f9f-aee0-4fec3d37c3cc/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L4_Integration_Scenarios.png "The diagram demonstrates the integration between SAP Sales Cloud and SAP S/4HANA, showcasing the end-to-end sales process, including opportunity creation, sales quoting, and order management in the Sales Cloud, as well as delivery, sales contracting, and customer invoicing in S/4HANA, supported by real-time pricing, material availability, and credit checks")

The graphic illustrates that sales quotes and sales orders can be created in either SAP Sales Cloud or SAP S/4HANA. Once they are created in one of these systems, they are automatically created in the other. Therefore, no matter where they are created, they will always be in both systems.

This means that the sales representatives do not have to log into both systems to view sales-related data. As a result, sales teams out in the field on their iPad can do their job making the sales and can trust that the warehouse team is receiving the delivery orders for shipping to their customers.

When this integration occurs, it's possible for supply chain and billing information to synchronize with SAP Sales Cloud. This gives a sales rep visibility over the entire business process, even when they are in the field.

This also allows for accurate and consistent pricing to be used from SAP S/4HANA, stock can be checked, and even credit can be checked.

Play the video to see how the integration is done in the system:

As part of the integration strategy in SAP Sales Cloud, documents created in SAP Sales Cloud can be replicated to SAP S/4HANA for order fulfillment, logistics execution, and finance to occur.

Sales quotes and orders can be sent to the EPR system. Any further processing in the ERP system can be sent back to SAP Sales Cloud for complete visibility of the entire process. ​

# Describing Sales Order Management

Objective

After completing this lesson, you will be able to describe the basics of sales order management

## Introduction

By capturing order information, order management enables sales representatives to deliver compelling offers and provide consistent and accurate pricing.

This lesson covers the following scope items:

![This graphic provides an overview of the Lead-to-Cash sales process, highlighting the stages from master data setup to payment, with the current focus on the Order Processing stage and the task of managing sales orders.](https://learning.sap.com/service/media/topic/f4b7a02d-1a72-48c5-a155-58592bbfce65/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_3.png "This graphic provides an overview of the Lead-to-Cash sales process, highlighting the stages from master data setup to payment, with the current focus on the Order Processing stage and the task of managing sales orders.")

## Sales Order Overview

Whether a sales order is created in SAP Sales Cloud, as described in this lesson, or created directly in SAP S/4HANA, there are automatic checks that occur to help get products to our customers.

When a sales document is created, a lot of mandatory information must be maintained.

For example, each sales document must always be assigned to a **sales area**. Furthermore, most sales documents must contain a **customer number** and at least one item with a **material number**.

A sales order is always **customer specific**, and **date driven**. There is a required delivery date in the sales order that drives deliveries and billing. The system will always use that date as a basis for checking to see if there is enough stock to promise the customer. This is called a material availability check. If the check is successful, products will be confirmed for that sales order. If the check is unsuccessful, future dates can be proposed for later delivery than requested. The result of the availability check is Scheduled Lines: line items scheduled for delivery, based on the dates the system confirmed.

Sales orders are also meticulously priced. There are pricing calculations that automatically occur when products and quantities are added to orders. Only a salesclerk with the proper authorization can change the pricing conditions once assigned to the order.

If a relevant preceding document exists, data can be copied from it when the sales document is created. For example, one or more quotations can serve as reference documents for a sales order. In this case, the system copies the relevant data to the sales order and the user does not have to maintain everything manually.

When an order is saved, an order confirmation can be sent to the customer to show receipt of their purchase order.

### Sales Transactions

Transactions are application programs that execute business processes in the SAP system, such as creating a sales order, posting a goods issue, or creating a customer’s billing document. A document is a data record that is generated when a transaction is carried out. It reproduces a business event in the system.

When performing each transaction, organizational elements must be assigned. Assignments of organizational elements to master data, like customer and material, are copied into sales documents. This process is illustrated in the overview below.

![This diagram illustrates the process of creating a sales order, starting from a customer ordering goods, detailing the order information, and resulting in an order document and confirmation.](https://learning.sap.com/service/media/topic/e95d17ed-511e-48d6-9c0b-7578a50359d0/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_SOOverview.png "This diagram illustrates the process of creating a sales order, starting from a customer ordering goods, detailing the order information, and resulting in an order document and confirmation.")

## Sales Order Processing

When an order is processed, the system can run various functions to accelerate and assist the process:

- **Output:** The information that is used to define the layout and formatting of documents sent to customers. Output can be created for various sales and distribution documents (quotes and proposals, sales order confirmations, invoices, and other ways of communications).
    
- **Pricing:** Many business documents have pricing procedures, built in formulas to intelligently and correctly price products and services. Prices, surcharges, discounts, freight, and taxes (conditions) for a business transaction can be determined automatically. You can also change these conditions manually.
    
- **Partner Determination:** The partner functions for a customer are stored in the customer master record in their sales area data. During sales order processing, they are copied as default values into the documents. For sales order processing, you need the mandatory partner functions:
    
    - The sold-to party places the order.
    - The ship-to party receives the goods or services.
    - The bill-to party receives the invoice for the goods or services.
    - The payer is responsible for paying the invoice.
- **Availability Check:** Material availability check is the process of determining whether a specific product is in stock and ready for purchase or if it is currently out of stock and not available for purchase. When you enter a sales order, materials are confirmed based on the required delivery date, if they are available. Otherwise, they will need Backorder Processing to be delivered.
    
- **Incompletion Log:** An incompletion log is a control function used to track and record incomplete or unfinished items, fields, or data in a sales order. It is commonly used in sales order processing ensure that all necessary tasks are completed before the document is ready for delivery processing.
    
- **Material Substitution:** Using material determination, you have a tool for automatically exchanging materials in the sales document. During order entry, the material ordered by the customer is replaced by the substitute defined in the master record. When you enter an order, the system searches for different material numbers for the same product, if found, the new material ID is used.
    
- **Free Goods:** Free goods can be part of the order quantity not included in the invoice. This is called an inclusive bonus quantity. The ordered goods and the free goods both involve the same material. Free goods can also take the form of extra goods that are free of charge. These are called exclusive bonus quantities.
    
- **Material Execution:** If you want to ensure that the customer does not receive certain materials, you can mark them as excluded materials. The material exclusion is also controlled when pricing occurs and will ensure a customer cannot buy certain products.
    

## Sales Order Scheduled Lines

A sales document is grouped into three levels: header, item, and scheduled line. The different levels are highlighted in the following graphic.

![This table provides an overview of a standard sales order, including header details (sold-to and ship-to parties), item information (materials and quantities), and corresponding scheduled delivery lines.](https://learning.sap.com/service/media/topic/d7ea5b16-50ce-4c24-820b-ce6bfe8d00b5/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_SalesOSLines.png "This table provides an overview of a standard sales order, including header details (sold-to and ship-to parties), item information (materials and quantities), and corresponding scheduled delivery lines.")

- **Header:** The data in the document header is valid and summarizes the entire document. This includes, for example, customer-related data.
    
- **Item 10 and 20:** Each item in the sales document contains its own data. This includes, for example, data about the material and quantities ordered. Each sales document can have several items, while individual items can be controlled differently. Examples include material item, service item, free-of-charge item, or text item.
    
- **Scheduled lines:** Scheduled lines contain delivery quantities and delivery dates. They belong uniquely to an item. Every item that has a subsequent outbound delivery in the sales and distribution process must have at least one scheduled line. The item can have several scheduled lines, for example when the quantity ordered is to be delivered in several partial deliveries at different times. The scheduled lines are confirmed quantities of product that the material availability check has verified and "promised" to the sales order delivery.
    

## How to Create a Sales Order

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_90E7A1D527764290:demo)

# Describing the Delivery and Shipping Process

Objective

After completing this lesson, you will be able to describe the delivery document creation, the goods movement processing, and the integration with the SAP Extended Warehouse Solution

## Introduction

The scope of this lesson is highlighted in the following process overview.

![This graphic provides an overview of the Lead-to-Cash sales process, highlighting the 'Product Delivery' stage, which includes managing delivery and executing warehouse tasks.](https://learning.sap.com/service/media/topic/a0bf13fb-048a-485d-80d8-fcc9d0f5554f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_4.png "This graphic provides an overview of the Lead-to-Cash sales process, highlighting the 'Product Delivery' stage, which includes managing delivery and executing warehouse tasks.")

### Outbound Deliveries

**Outbound deliveries** are the basic documents for the different activities during the shipping process (picking, packing, and posting the goods issue).

In most cases, they are created with reference to one or more sales orders that are ready to be shipped. Because of this reference, the system can copy all the relevant data from the order(s) to the outbound delivery. Referring deliveries to a sales order builds a continuous document flow of the process, linking the sales documents and influencing the document status in the process.

The process is illustrated in the graphic below.

![This diagram outlines the sales order fulfillment process, progressing from sales order creation to outbound delivery and warehouse activities like picking, packing, document processing and goods issue to the customer.](https://learning.sap.com/service/media/topic/a0bf13fb-048a-485d-80d8-fcc9d0f5554f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_Introduction.png "This diagram outlines the sales order fulfillment process, progressing from sales order creation to outbound delivery and warehouse activities like picking, packing, document processing and goods issue to the customer.")

1. **Sales Order:** Shipping-relevant functions of the sales order are
    
    - Shipping Point Determination
    - Route Determination
    - Scheduling
2. **Outbound Delivery:** Each outbound delivery is processed by one shipping point. The shipping point is the highest-level organizational unit of shipping that controls your shipping activities. This can be a loading ramp, a mail depot, or a rail depot. It can also be, for example, a group of employees responsible (only) for organizing urgent deliveries.
    
3. **Warehouse execution:** By assigning the plant and it's storage locations to a warehouse number in the Enterprise Structure, the outbound delivery is passed to the EWM system. The bikes are picked from storage by a forklift, packaged with packing slips, and shipped to the customer.
    

Note

While not all sales order items are delivery- or billing-relevant, we will cover the process as if items will be delivered and invoiced.

You can create one or more outbound deliveries with reference to a single order. Alternatively, multiple items from different sales orders can be combined in a single outbound delivery. To combine items from multiple orders, they must all have the same values for the characteristics that are key to the shipping process, for example:

- Shipping point
- Due date
- Ship-to address

The system can create deliveries either online or as a background job to be executed during off-peak hours.

## The Shipping Process

Explore the shipping process in the following graphic:

![This diagram illustrates the shipping process, starting with shipping activities, creating a delivery transaction, specifying order details, and ending with the generation of a delivery document and delivery note.](https://learning.sap.com/service/media/topic/bf45d8a7-c252-42d7-869e-fc2c86c724a5/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_ShippingProcess.png "This diagram illustrates the shipping process, starting with shipping activities, creating a delivery transaction, specifying order details, and ending with the generation of a delivery document and delivery note.")

1. You trigger shipping activities by creating deliveries.
    
2. The organizational unit responsible for creating deliveries is the shipping point. The shipping point is the highest-level organizational unit of shipping that controls your shipping activities. Each outbound delivery is processed by one shipping point. This can be a loading ramp, a mail depot, or a rail depot. It can also be, for example, a group of employees responsible (only) for organizing urgent deliveries.
    
3. You assign a shipping point at plant level. A shipping point is a physical place and should be near the delivering plant. A shipping point can provide shipping activities for one or more plants. This can also be appropriate for plants in physical proximity.
    
4. The responsible shipping point is determined for each order item. The system automatically proposes a shipping point that you can change within given limits. The shipping point cannot be changed in the outbound delivery. When an order is processed for delivery by the shipping point, the system only copies the order items that are defined for this shipping point into the outbound delivery.
    

Despite the different options for adjusting the scope of the material availability check, there will be times when you cannot confirm a sales order. In SAP S/4HANA, such sales orders are called _backorders_.

In many cases, you will not be able to do anything to resolve the situation. Nevertheless, backorder processing could be an option to fix any product shortages for orders you really need to fill.

## Picking Outbound Deliveries

Picking is the process of preparing or providing goods for delivery to the customer with special attention paid to dates, quantity, and quality. Picking often takes place using the printout of a picking list.

In the standard configuration of the system, the prerequisite for posting a goods issue is that picking-relevant items are completely picked. This means that the delivery quantity and the pick quantity in the outbound delivery must be the same.

An outbound delivery order contains all the data that is required to trigger and monitor the complete outbound delivery process. In other words, the outbound delivery order is the basis for the execution of picking activities.

When the goods issue is posted in SAP Extended Warehouse Management (SAP EWM), a final outbound delivery (in SAP EWM) is created automatically. This document triggers the goods issue posting in inventory management.

![This flowchart represents the sales and delivery process in SAP S/4HANA, starting with the creation of a sales order, followed by outbound delivery, transitioning into extended warehouse management with the creation of an outbound delivery order, and culminating with the post goods issue.](https://learning.sap.com/service/media/topic/b483e320-5b2d-4342-9e12-df24c0338946/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L6_SDandEWM.png "This flowchart represents the sales and delivery process in SAP S/4HANA, starting with the creation of a sales order, followed by outbound delivery, transitioning into extended warehouse management with the creation of an outbound delivery order, and culminating with the post goods issue.")

To execute physical goods movements in the warehouse, warehouse tasks are used. Warehouse tasks are needed for the following:

- Picking
- Putaway
- Internal Movements
- Posting Changes
- Goods Receipt Postings
- Goods Issue Postings

Updating the pick quantity in the warehouse order will also update the pick quantity in the outbound delivery.

![This diagram illustrates the delivery process flow between the shipping point and warehouse, showing item details (e.g., E-Bikes and Bike Tires), delivery and pick quantities, the creation of outbound delivery orders, and corresponding warehouse tasks like generating a picking list.](https://learning.sap.com/service/media/topic/b483e320-5b2d-4342-9e12-df24c0338946/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L6_PickingOutbound.png "This diagram illustrates the delivery process flow between the shipping point and warehouse, showing item details (e.g., E-Bikes and Bike Tires), delivery and pick quantities, the creation of outbound delivery orders, and corresponding warehouse tasks like generating a picking list.")

## Post Goods Issue

When you post a goods issue, the system automatically performs a number of tasks.

Explore the graphic to learn more.

![This diagram illustrates the process flow for outbound delivery and goods issue, highlighting the creation of a material document and its integration with stock requirements, accounting, controlling, billing, material ledger, and document flow systems.](https://learning.sap.com/service/media/topic/cc53d0aa-ff8a-4832-b06a-f303e411bbde/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_PostGoofdsIssue.png "This diagram illustrates the process flow for outbound delivery and goods issue, highlighting the creation of a material document and its integration with stock requirements, accounting, controlling, billing, material ledger, and document flow systems.")

1. The material document removes the confirmed stock from the stock requirements list. This updates the quantities in inventory management. Any loss of inventory updates the stock and requirements list. The material document removes the confirmed stock from the stock requirements list. This updates the quantities in inventory management. Any loss of inventory updates the stock and requirements list.
    
2. The accounting document decreasing inventory valuation is created. This updates the value change in the balance sheet accounts for inventory accounting. This balances with the P&L statement's cost of goods sold account.
    
3. A controlling document is generated breaking down the costs of goods sold.
    
4. The billing due list is updated. Invoicing tasks can now be performed.
    
5. A material ledger document is generated based on the goods movement and material valuation.
    
6. The document flow and status is updated in all relevant sales documents.
    

## How to Create an Outbound Delivery

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6DE694B2DE006985:demo)

# Describing Customer Billing

Objective

After completing this lesson, you will be able to describe customer billing processes and how to integrate with FI

## Introduction

In this lesson, we discuss the following business process step:

![This graphic provides an overview of the Lead-to-Cash sales process, focusing on the current stage, 'Invoicing,' specifically the 'Manage Billing' step within the sequence of activities from master data to payment handling.](https://learning.sap.com/service/media/topic/e32316d1-c943-4da7-869e-46a59b24b450/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_5.png "This graphic provides an overview of the Lead-to-Cash sales process, focusing on the current stage, 'Invoicing,' specifically the 'Manage Billing' step within the sequence of activities from master data to payment handling.")

When you create a **billing document**, data is copied from the sales order and the delivery document to the billing document. Delivery items, as well as order items (for example, services), can be references for the billing document.

![This diagram illustrates the data flow from a sales order and delivery document to the creation of a billing document, which facilitates invoice generation, payment monitoring, and automatic updates to the general ledger (G/L) account.](https://learning.sap.com/service/media/topic/e32316d1-c943-4da7-869e-46a59b24b450/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Billing_DataTransfer.png "This diagram illustrates the data flow from a sales order and delivery document to the creation of a billing document, which facilitates invoice generation, payment monitoring, and automatic updates to the general ledger (G/L) account.")

The billing document serves several important functions:

- It is the sales and distribution document that helps you to generate invoices.
- It serves as a data source for financial accounting (FI) to help you to monitor and process customer payments.
- Typically, creating a billing document automatically updates the G/L accounts.

## Creating a Billing Document

The main type of billing document is the **invoice**. The creation of invoices is often the last step in a sales and distribution process. If you have delivered physical products to the customer, you can create invoices with reference to outbound deliveries. If you have sold services, you can create invoices with reference to sales orders.

The system can combine a number of preceding documents (such as outbound deliveries) in one billing document on the condition that these documents have the same values for some relevant characteristics. Examples of these characteristics include the following:

- Payer
- Billing date
- Destination country

![This diagram outlines the billing process, starting from a delivery document, proceeding to the creation of a billing document with specific items, quantities, and bill-to-party details, and concluding with the generation of an invoice.](https://learning.sap.com/service/media/topic/b8a16868-a254-44e3-acad-6e5195e533a4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L7_BillingProcessing.png "This diagram outlines the billing process, starting from a delivery document, proceeding to the creation of a billing document with specific items, quantities, and bill-to-party details, and concluding with the generation of an invoice.")

The system can create invoices either online or as a background job to be executed during off-peak hours.

## How to Create a Billing Document

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_474598E8B84BF49D:demo)

## Results of Saving the Billing Document

When you save the billing document, the system automatically generates all the required documents for accounting. It carries out a debit posting on the customer receivables account and a credit posting on the revenue account. The postings can be reproduced using the corresponding accounting document, which can be accessed directly via the billing document or via the process flow.

The following graphic provides an overview which documents are generated.

![This diagram shows the integration of an SD billing document with various business processes, including accounting, controlling, sales reporting, profitability analysis, customer credit management, and document flow.](https://learning.sap.com/service/media/topic/d19ca9f3-74e4-4c6f-a74a-acdd92957e7c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit8_SaveBilling.png "This diagram shows the integration of an SD billing document with various business processes, including accounting, controlling, sales reporting, profitability analysis, customer credit management, and document flow.")

1. A **financial accounting document** is created - creating an open item in the customers accounts receivable account.
2. A **controlling document** is generated to record the revenue posting.
3. **Sales information system:** Embedded analytics can be executed or SAP BW/4HANA ready data for staging and reporting.
4. A controlling **profitability analysis document**(COPA) is generated for operating concern controlling.
5. If the credit limit functionality is used, the limit data in the **credit account of the customer** is updated.
6. **Document flow:** The billing document is the last step performed by the sales department. The accounting department will take over the remaining tasks.

## The Complete Document Flow

The documents within a sales and distribution process are linked to each other via the document flow. This enables you to access the history and current status of your sales and distribution processes at any time.

You can display the document flow as a list with the linked documents. Depending on the document from which you call up the list, all the relevant preceding and subsequent documents are displayed.

From this list, you can display the relevant documents or call up status overviews for the documents.

This provides a quick overview of the progress of your sales processes at any time and can be used to answer customer questions quickly and reliably.

![This diagram represents the end-to-end process flow from creating a standard order to delivery, billing, and accounting documentation, with a detailed document list showcasing key transactional steps.](https://learning.sap.com/service/media/topic/f5f01270-97c2-4e46-ba3c-a5080fc29a70/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U7_L7_DocumentFlow.png "This diagram represents the end-to-end process flow from creating a standard order to delivery, billing, and accounting documentation, with a detailed document list showcasing key transactional steps.")

Note

Had there been an ERP quote that proceeded the sales order, it would also be linked in the document flow.

# Managing Customer Payments

Objective

After completing this lesson, you will be able to manage customer payments and describe how to integrate with SAP Collections and Dispute Management

## Introduction

This lesson covers the last business process step within the sales related lead-to-cash process that links back to accounting: Posting incoming payments. The process step is highlighted in the overview below.

![This graphic provides an overview of the Lead-to-Cash sales process, highlighting the current step, 'Manage Payments,' within the final stage of the process called 'Money,' following invoicing and earlier steps like order processing and product delivery.](https://learning.sap.com/service/media/topic/f0888cc3-ecd5-44dd-ab6b-63bc7c52f269/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Sales_7.png "This graphic provides an overview of the Lead-to-Cash sales process, highlighting the current step, 'Manage Payments,' within the final stage of the process called 'Money,' following invoicing and earlier steps like order processing and product delivery.")

## Posting Incoming Payments

The posting of incoming payments is carried out in the financial accounting department.

When an incoming payment is posted, the data on the relevant G/L accounts is posted automatically. The system posts a debit on the cash account and enters a credit on the customer's receivables account.

Read the following dialogue of two SAP experts to think about this process step.

![This image highlights a discussion titled 'How to import bank statements into the SAP system,' emphasizing the topic of SAP functionality for financial processes.](https://learning.sap.com/service/media/topic/a9e584b6-1bc7-4b87-913a-cd17366b56a3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Dialogue_4.png "This image highlights a discussion titled 'How to import bank statements into the SAP system,' emphasizing the topic of SAP functionality for financial processes.")

- **Heinz:** I have the feeling that many companies use the option of obtaining bank statement data from the bank electronically. What are your thoughts on this?
    
- **Simona:** That is actually true. You can import the bank statement files into the SAP system using the electronic bank statement. Numerous bank statement formats are supported for this. For any bank statement items that could not be updated by the system directly, you can manually postprocess them in the system and then post them.
    
- **Heinz:** So it seems that it is not a perfect world, but SAP applications such as SAP Credit Management and SAP Collections and Dispute Management make it easier to manage.
    
- **Simona:** Exactly. That is also my understanding.
    

## How to Process Incoming Receivables

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_79E4D16570635793:demo)