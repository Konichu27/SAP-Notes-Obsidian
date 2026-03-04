# Understanding the Basics of the Service Process

Objective

After completing this lesson, you will be able to describe the integrated SAP solution to run the service process including the used systems and the concept of organizational data

## Introduction

This lesson introduces the SAP solution to run the service process. It is assigned to the Lead-to-Cash process. You will learn how the bike company in our example benefits from using the integrated service solution.

**Scenario:** The bike company implementation project is currently in the _Realization_ phase, in which the end-to-end processes are tested by the project team. The selected scope items for all areas were assigned to the business processes of the bike company. This enables the project team to understand which summarized scope items are used to represent a core process within their company.

Based on best practice scope items, you find below a summary of the bike company’s service process.

![This image illustrates the Lead-to-Cash Process Overview for Service, showcasing the key phases of managing service operations, including Master Data, Service Contract and Invoice Management, Recurring Services, and Service Analytics.](https://learning.sap.com/service/media/topic/c41aec64-1964-4a65-bdd8-e595d8b523c3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Overview2.png "This image illustrates the Lead-to-Cash Process Overview for Service, showcasing the key phases of managing service operations, including Master Data, Service Contract and Invoice Management, Recurring Services, and Service Analytics.")

- As with all areas, you need to define and handle **master data** that is kept for a longer period of time. Customers, products, conditions, technical objects to name only a few need to be defined as master data.
    
- **Service contract management** includes the creation and administration of all kinds of contracts for the service process. Service Contract Billing is part of the Invoice Management which covers all related process steps in managing the posting of customer invoices.
    
- **Recurring service** comprises the process steps for the planning and execution of recurring inspections and service activities. At first, you need to define service order templates and maintenance plans. Maintenance plans need to be scheduled to obtain automatically generated service orders.
    
- **Service monitoring and analytics** can be used to track key figures from a technical and a controlling perspective.

In the SAP Solution Landscape we are currently here:

![This image provides an overview of the SAP Solution Landscape for Service, highlighting the integration of SAP Intelligent Asset Management (IAM) within the broader SAP Business Technology Platform and SAP S/4HANA framework. It emphasizes key service-related modules, including Customer Service (CS) and Enterprise Asset Management (EAM).](https://learning.sap.com/service/media/topic/c41aec64-1964-4a65-bdd8-e595d8b523c3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation_5.png "This image provides an overview of the SAP Solution Landscape for Service, highlighting the integration of SAP Intelligent Asset Management (IAM) within the broader SAP Business Technology Platform and SAP S/4HANA framework. It emphasizes key service-related modules, including Customer Service (CS) and Enterprise Asset Management (EAM).")

## Overview of the SAP S/4HANA Service Solution

Watch the [official video](https://www.sap.com/products/crm/enterprise-service-management.html?video=8e9bc463-e37e-0010-bca6-c68f7e60039b) to get an idea what service management with SAP includes.

The following video provides a simple overview of the main components.

Hi! To show you which components are included in SAP S/4HANA Service,

I'd like to share a video with you

that provides a brief overview. Enjoy!

A closer look at available areas will give

an overall view of SAP S/4HANA Service.

The focus of SAP S/4HANA Service on

-premise can be described as follows.

Plan service. Complex service. The focus of the SAP Service Cloud can

be described as follows. Self -service Execution of simple service

tasks The focus of SAP Field Service Management can be described as

follows. Customer self-service Planning and dispatching Mobile field

service Smart forms Analytics There are some additional capabilities.

SAP S/4HANA Service is integrated into the following areas.

Asset management Predictive maintenance Asset

network Asset performance Analytics Augmented Analytics

Digital Boardroom Self -service data exploration

Note

Service processes could formerly only be mapped via SAP Customer Service (CS) which is still available in SAP S/4HANA via the compatibility mode. The Bike Company has decided to use the enhanced features of SAP S/4HANA Service instead.

The design of SAP S/4HANA Service eliminates functional redundancies and data replication:

- Best of both worlds: Identify functional redundancies, and select the most suitable object/engine/process.
    
- Unify CRM and S/4HANA objects: Unified objects share the same database representation, thus require no middleware.
    

S/4HANA service comprises service management; sales and order management. As the following graphic illustrates, business objects of SAP S/4HANA service originate in SAP ERP as well as in CRM.

![The picture shows that all business objects of SAP S/4 HANA Service such as Service Quote, Service Contract, Service Request, Service Order, Service Confirmation and Interaction Center origin in both, SAP ERP and SAP CRM. This is also true for other objects such as Organization Model or Solution Contract.](https://learning.sap.com/service/media/topic/e57cf4b7-217d-499e-8df0-0b4669ff8116/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Service_BusObj.png "The picture shows that all business objects of SAP S/4 HANA Service such as Service Quote, Service Contract, Service Request, Service Order, Service Confirmation and Interaction Center origin in both, SAP ERP and SAP CRM. This is also true for other objects such as Organization Model or Solution Contract.")

## Organizational Structure

The organizational structure of SAP S/4HANA Service is fully integrated in the enterprise structure of SAP S/4HANA, depending on the relationship of organizational elements within the system.

Sales and distribution (SD) organizational structure elements are integrated with the organizational structure specific for SAP S/4HANA Service.

Explore the graphic below to learn more about SD and SAP S/4HANA Service.

![This image illustrates the integration between the SD Organization Structure and the SAP S/4HANA Service Organization Structure, highlighting components like Sales Organization, Distribution Channel, and Service-specific elements like Service Back Office and Technicians.](https://learning.sap.com/service/media/topic/a3b96ef6-4dfa-44ae-a15e-a48984a392c4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_SDOStructure.png "This image illustrates the integration between the SD Organization Structure and the SAP S/4HANA Service Organization Structure, highlighting components like Sales Organization, Distribution Channel, and Service-specific elements like Service Back Office and Technicians.")

**SAP S/4HANA Service Organizational Structure:** Organizational Management in SAP S/4HANA Service allows you to map your service and sales structure. You can characterize your organizational units by organizational and general attributes. Additionally, you can define rules to determine the responsible organizational unit.

### Organizational Model: Overview

Organizational Management in SAP S/4HANA Service offers you a flexible tool for handling your company’s task-related, functional organizational structure as a current organizational model.

You can maintain the company structure, including the positions and employees, and assign specific data (attributes) to the organizational units. In the system, you can open the Organization Model via _Home_→_Service Operations_→_Organization Model_:

![System screenshot of the organizational model. Sales & service 1010 is at the top of the organizational hierarchy. Below it, we see is sales organization DE, interaction center DE, marketing organization DE, and service organization DE. Under the node of the service organization, there is service back office DE, and service technicians DE. The top node sales & service 1010 is selected and on the bottom of the screenshot we see various details about the organization unit such as descriptions, validity dated, and address.](https://learning.sap.com/service/media/topic/a3b96ef6-4dfa-44ae-a15e-a48984a392c4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L2_Organizational_Model.png "System screenshot of the organizational model. Sales & service 1010 is at the top of the organizational hierarchy. Below it, we see is sales organization DE, interaction center DE, marketing organization DE, and service organization DE. Under the node of the service organization, there is service back office DE, and service technicians DE. The top node sales & service 1010 is selected and on the bottom of the screenshot we see various details about the organization unit such as descriptions, validity dated, and address.")

The organizational model will be used for organizational data determination within the SAP S/4HANA Service scenario for Sales and Service.

## How to Display an Organizational Structure for Service

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_9F2347CA22319F97:demo)

# Exploring Master Data in Service

Objective

After completing this lesson, you will be able to explain the concept of master data in service

## Introduction

This lesson covers the following process steps:

![This graphic provides an overview of the Lead-to-Cash process for services, highlighting the current stage, 'Master Data,' where elements such as Business Partner, Product, Conditions, and Technical Objects are managed before progressing to Service Contract and Invoice Management.](https://learning.sap.com/service/media/topic/c0e1ad67-85e9-4748-83fe-d49033efb12a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Service1.png "This graphic provides an overview of the Lead-to-Cash process for services, highlighting the current stage, 'Master Data,' where elements such as Business Partner, Product, Conditions, and Technical Objects are managed before progressing to Service Contract and Invoice Management.")

## Business Partner

Business partners are relevant for all service processes of a company. In the SAP system, business partners can be mapped via the relevant business partner roles. The following graphic shows an overview how business partner roles can be distinguished.

![This diagram distinguishes between external business partners, such as accounts/customers, vendors, and contacts, and internal business partners, including service agents, service technicians, and back-office employees. It notes that business partners already defined in areas like presales and sales can also be utilized.](https://learning.sap.com/service/media/topic/feb523f9-9f1d-4bcd-9214-74f2f3b34481/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_BusinessPartners.png "This diagram distinguishes between external business partners, such as accounts/customers, vendors, and contacts, and internal business partners, including service agents, service technicians, and back-office employees. It notes that business partners already defined in areas like presales and sales can also be utilized.")

The central business partners are account, contact, and employee.

- An **account** is a company, individual, or group with which you have a business relationship. An account can be, for example, a customer, prospect, vendor, or competitor.
- A **contact** is a person with whom you have a business relationship. A contact is usually assigned to a corporate account.
- An **employee** is a member of your company and is involved in the interactions between your company and customers, prospects, vendors, and other parties.

Hint

You can learn more about these topic in the following lessons:

- _Managing Accounts Receivable_, as part of the record-to-report process
- _Using Master Data in Sales_, as part of the lead-to-cash process with focus on sales

## External Business Partners

Let's take a look at external business partners such as customers and sold-to-parties. Depending on the business partner role, the data that you maintain is generic or limited to a certain area. For example, when maintaining the business partner role _Sold-To-Party_, you need to maintain sales-specific data.

The following figure shows the example of a bike company and its customer _Northsea Energy._

![This visualization represents the relationship among a company code (Bike Company Subsidiary), the customer or sold-to-party (Northsea Energy), and the contact person (Michael Fischer), emphasizing the connection within a business structure.](https://learning.sap.com/service/media/topic/b07098f2-e306-42c9-9c89-e28bb8ea1292/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/ExtBP.png "This visualization represents the relationship among a company code (Bike Company Subsidiary), the customer or sold-to-party (Northsea Energy), and the contact person (Michael Fischer), emphasizing the connection within a business structure.")

- The subsidiary of the bike company, with its own financial statement and balance sheet, is defined as **company code**.
- Northsea Energy is a **customer** of the bike company and mapped as a business partner in the system. Northsea Energy offers subsidized bikes and E-bikes to it's employees.
- Michael Fischer has bought a subsidized bike of the bike company and is defined as **contact** which is assigned to the business partner _Northsea Energy_.

## How to Display an External Business Partner

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_3F92AEC9FE6A6192:demo)

## Internal Business Partners

When creating documents, the business partner _employee_ is automatically assigned if the personnel numbers are linked to the organizational structure. The personnel master is linked to the business partner role _employee_ as well as to the _SAP user_. This means, for example, when creating a service order template, the default value for the employee responsible is linked to the SAP user.

### Example:

Tom Schmitt works as technician in the service department of the bike company. If you look for him in the SAP system, you find him as follows:

![This diagram outlines the relationship between a company code (Bike Company Subsidiary), an organizational unit (Service Department), and a personnel master (Technician S4700_00, represented as Tom Schmitt). It also connects the personnel master to roles such as Business Partner: Employee and SAP User.](https://learning.sap.com/service/media/topic/b5dcbd98-f8e2-4e6f-b2c6-baeda9384d3d/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IntBP.png "This diagram outlines the relationship between a company code (Bike Company Subsidiary), an organizational unit (Service Department), and a personnel master (Technician S4700_00, represented as Tom Schmitt). It also connects the personnel master to roles such as Business Partner: Employee and SAP User.")

1. You first look for the respective subsidiary of the bike company, with its own financial statement and balance sheet. It is defined as company code.
    
2. Then you look at the plant and will find several org units / positions defined there. Tom Schmitt is working in the service department.
    
3. There you find Tom Schmitt with his personell number as _Technician S4700-00_ from the service department. The personnel master is linked to the business partner role _employee_ as well as to the _SAP User_. When creating a service order template, the default value for Tom Schmitt as _Employee Responsible_ is linked to the SAP User.
    

## How to Display an Internal Business Partner

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_1254CF0B2EA1549B:demo)

## Product

Products are services and goods that are the object of a company's business activities. The product or material master is divided into different areas or departments such as _Basic Data_, _Sales_, _Purchasing_, _Accounting_ and so on.

In the following, you will find out about the relevance of products/material master records for the service department of the bike company we use as example.

Hint

For further information, check the

- Lesson _Explaining the impact of enterprise structures to master data and documents_.
- Lesson: _Using master data in sales_.

Products can be differentiated as follows:

![This diagram highlights elements of the Product Master: describing the service material or service product (Service), component planning (Spare Part), and structuring of technical objects (Series Number, etc.).](https://learning.sap.com/service/media/topic/dfb4ad21-a519-4e75-b3a0-ebbed225e289/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Product.png "This diagram highlights elements of the Product Master: describing the service material or service product (Service), component planning (Spare Part), and structuring of technical objects (Series Number, etc.).")

- **Service Material / Service Product**: Description of a service, for example, in-house service of a service technician.
    
- **Component Planning**: Spare parts or components that can be assigned to documents, such as a service order, for example, brake set that needs to be replaced.
    
- **Structuring of Technical Objects**: Tangible products can be divided as follows.
    
    - Material as bill of material item, for example, tires assigned to a BOM
    - Material as construction type, for example, a material representing the series of a bike
    - Material serial number, for example, a bike that you want to track as an individual piece of equipment

### Service Products

You need to maintain sales area specific data for service products. The assignment of an item category to a service product triggers the usage in service documents, for example, service orders.

![System screenshot of the product master data on the sales organization 2 page. The item category group field with the value service product](https://learning.sap.com/service/media/topic/dfb4ad21-a519-4e75-b3a0-ebbed225e289/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L3_Products.png "System screenshot of the product master data on the sales organization 2 page. The item category group field with the value service product")

## How to Display a Service Product

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_41786B7B76EF2889:demo)

## Component Planning and Spare Parts

You need to maintain sales area specific data for spare parts.

The assignment of the Item Category to a Spare Part triggers the usage in Service documents, for example, Service Orders.

![System screenshot of the product master data on the sales organization 2 page. The item category group field with the value NORM (standard item) is highlighted.](https://learning.sap.com/service/media/topic/af38a260-98ee-4e26-9c5c-93508efcc4d4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L4_Component_Planning.png "System screenshot of the product master data on the sales organization 2 page. The item category group field with the value NORM (standard item) is highlighted.")

## How to Display a Spare Part

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_AFE24FC225A9DE92:demo)

## Conditions in SAP S/4HANA Service

Prices, surcharges and discounts, freight, and taxes are all part of the conditions master data. Here you can see the condition master overview:

![Graphic with 4 boxes. First box: prices with material price and customer-specific price as example. Second box: surcharges and discounts, with, customer, material, and customer & materials as examples, third box: freight, with freight incoterms as an example. Last box: taxes, values added tax as example.](https://learning.sap.com/service/media/topic/e196950e-61d1-4ffa-9352-9f1971fa4029/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L3_Conditions.png "Graphic with 4 boxes. First box: prices with material price and customer-specific price as example. Second box: surcharges and discounts, with, customer, material, and customer & materials as examples, third box: freight, with freight incoterms as an example. Last box: taxes, values added tax as example.")

The service department of the bike company in our example needs to define the **conditions for services and spare parts**.

Depending on the business process, condition master records are differentiated according to condition types, for example, PPRO when using service orders or PSI1 when working with service contracts. This is illustrated in the following figure.

![System screenshot with condition types highlighted on the product condition records](https://learning.sap.com/service/media/topic/e196950e-61d1-4ffa-9352-9f1971fa4029/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L4_Conditions_in_Service.png "System screenshot with condition types highlighted on the product condition records")

## How to Display Conditions

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_3F2800315E9305A4:demo)

## Technical Objects

The bike company in our example uses technical objects to structure the produced bikes from a service perspective. SAP S/4HANA Service offers the possibility to structure simple as well as highly complex technical asset structures.

There are four categories of technical objects:

- **Functional locations** are elements of a technical structure and represent the system areas in which objects can be installed. Technical structure can be subdivided according to functional, process-oriented, or spatial criteria.
    
- **Equipment** represents individual objects that are to be treated as autonomous units.
    
- **Serial numbers** are assigned to materials to differentiate them from other items. They enable materials to be treated as individual items. Inventory management can be carried out for serial numbers.
    
- **Assemblies** are used to finely structure functional locations and equipment. These are treated as Bill of Material items and not as individual items.
    

Note

- The bike company in our example has decided not to use **functional locations** due to the comparatively simple requirements regarding the mapping of technical assets.
- Functional locations, equipment, and serial numbers can be assigned to documents in service processes, for example, service order templates, service orders.

## How to Display Technical Objects

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_9F4E4C4BD1240D83:demo)

# Describing Service Contract and Invoice Management

Objective

After completing this lesson, you will be able to describe the concept of service contracts and service contract billing

## Introduction

This lesson covers the following process steps:

![This graphic provides an overview of the Lead-to-Cash process for services. It highlights the current stage, focused on Service Contract and Invoice Management, which includes 'Service Contract' and 'Service Contract Billing.' Other stages in the process include Master Data, Recurring Service, and Service Analytics, covering aspects such as business partners, product details, maintenance plans, and service monitoring.](https://learning.sap.com/service/media/topic/f47c0263-e578-4925-8fc5-95d10848fb27/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Service2.png "This graphic provides an overview of the Lead-to-Cash process for services. It highlights the current stage, focused on Service Contract and Invoice Management, which includes 'Service Contract' and 'Service Contract Billing.' Other stages in the process include Master Data, Recurring Service, and Service Analytics, covering aspects such as business partners, product details, maintenance plans, and service monitoring.")

## Service Contract

Instead of waiting for service requests to come in, the bike company in our example offers its customers regular bike services based on service contracts for periods and conditions. Service contracts include certain services and spare parts.

The following image illustrates what a service contract includes.

![This diagram represents the key components of a Service Contract. It includes the customer, time period, conditions, services, and spare parts, all connected to the central concept of the service contract, which governs these elements.](https://learning.sap.com/service/media/topic/dc95ef11-0b5c-48a4-801d-b19e8508244c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_ServiceContract.png "This diagram represents the key components of a Service Contract. It includes the customer, time period, conditions, services, and spare parts, all connected to the central concept of the service contract, which governs these elements.")

From the content of a service contract, you can derive the main features.

1. Represent an **outline agreement** with customers that defines content and scope of services under specific conditions for a particular period.
2. Specify the **service levels** to which a customer is entitled.
3. List the **parts that are covered** by contracted services (for example, brake set, speed cassette, bike computer).
4. Include a **product list** containing services and service parts in contract entitlement.
5. Contain **price agreements** for services and parts.
6. Limit contracted services or service parts in terms of **value and/or quantity**.

Service contracts contain details and items. Details refer to the whole contract including all items. Items contain item-specific information. The following figure shows the structure of a service contract.

![Diagram showcasing the components of a Service Contract, divided into Details (Sold-to-Party, Dates, Status, Responsibilities) and Items (Products, Conditions, Service Profile, Response Profile, Status, Technical Object).](https://learning.sap.com/service/media/topic/dc95ef11-0b5c-48a4-801d-b19e8508244c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_SCStructure.png "Diagram showcasing the components of a Service Contract, divided into Details (Sold-to-Party, Dates, Status, Responsibilities) and Items (Products, Conditions, Service Profile, Response Profile, Status, Technical Object).")

## How to Display a Service Contract

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C128F8CB5098BA88:demo)

## Service Contract Billing

**Scenario:** Imagine your customer _Northsea Energy_ has a service contract with your bike company. They pay a monthly fee of 35€. With the service contract, they receive certain services and spare parts according to the predefined price agreements. What do you need to consider when creating the billing document?

Here you can see how to create a billing document and which content it has:

![Figure with 2 sections, top section: arrow pointing from box with billing document request to billing document. Bottom section with the following details from a billing document: sales document number (90000XXX), sales document category (billing document), sold to party (northsea energy), net value (35 euro).](https://learning.sap.com/service/media/topic/bf17fbeb-52f3-486f-9309-6f9194bb7cf1/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L4_Service_Contract_Billing.png "Figure with 2 sections, top section: arrow pointing from box with billing document request to billing document. Bottom section with the following details from a billing document: sales document number (90000XXX), sales document category (billing document), sold to party (northsea energy), net value (35 euro).")

At first, you create a billing document request. Afterward, you create a billing document, for example, an invoice to charge the customer. In the billing plan of the service contract item, you can check whether the billing process has been carried out correctly.

## How to Bill a Service Contract

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_79CD1ECB07B634AB:demo)

# Managing Recurring Service

Objective

After completing this lesson, you will be able to use service order templates and maintenance plans

## Introduction

This lesson covers the following process steps:

![This graphic illustrates the Lead-to-Cash process for services, highlighting the current stage as 'Recurring Service.' This stage includes 'Service Order Template,' 'Maintenance Plan,' and 'Maintenance Plan Scheduling.' Other stages in the process are Master Data, Service Contract and Invoice Management, and Service Analytics, covering components such as business partners, products, service contracts, and service monitoring.](https://learning.sap.com/service/media/topic/c99bd56c-3103-43c0-b9fa-fda322a978b9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Service3.png "This graphic illustrates the Lead-to-Cash process for services, highlighting the current stage as 'Recurring Service.' This stage includes 'Service Order Template,' 'Maintenance Plan,' and 'Maintenance Plan Scheduling.' Other stages in the process are Master Data, Service Contract and Invoice Management, and Service Analytics, covering components such as business partners, products, service contracts, and service monitoring.")

## Service Order Creation

The bike company in our example offer its customers recurring services. The following service categories are possible:

- In **time-based recurring services**, service tasks are triggered after a specific time period has elapsed (for example, every six months).
    
- In **performance-based recurring services**, service tasks are triggered when a specific target value (counter reading) is reached (for example, after every 10,000 km).
    
- In **condition-based preventive maintenance**, maintenance tasks are triggered when a condition is outside a specified value range (for example temperature lower than -20°C).
    
- With **predictive maintenance**, they can control machines cloud-based in real time and can predict machine failures based on collected data (IoT application - Internet of Things).
    

**Example:** Customer C700-C00 gets a 2-year recurring maintenance service. This is a time-based service. The customer pays a monthly fee of €35 and in return receives certain services. Which steps are necessary to create the corresponding service orders in the system?

The following table lists the individual steps of a service order creation. It outlines who is responsible and which app integration is used for each.

#### Service Order Creation Steps

|Step|Role|Integration|
|---|---|---|
|(1) Create service order template|Service planner|S/4 Service / MM|
|(2) Create maintenance plan|Service planner|S/4 Service / SD / MM / HCM|
|(3) Schedule maintenance plan|Service planner|S/4 Service / MM / HCM|
|(4) Process service order|Service technician|S/4 Service / FI / CO|
|(5) Complete service order|Service planner / technician|S/4 Service / FI / CO|

- The **service order template** defines services to be performed including the relevant spare parts.
- The **maintenance plan** is created for the specified technical object(s), service contract item(s) and service order template(s).
- **Scheduling** of the maintenance plan is required for the regular call-up of service orders and the recalculation of planned dates.
- The **service order** is automatically generated by scheduling the Maintenance Plan.
- The **completion** date in the maintenance plan can be used for calculating the next planned date.

## Service Order Template

Service order templates can be used to standardize recurring activities, for example, a regular bike service. The templates describe a series of individual service activities.

If you have a service order template, you can create service orders and maintenance plans with minimal effort by referencing the items and processes that were created in the service order template. You can link reference objects such as pieces of equipment, functional locations, serial numbers, and products to service order templates.

Service order templates also specify the spare parts that are required for routine service tasks and the time needed to perform the work. For example, if you create a service order for routine work for which all the individual items are already described in a service order template, you only need to specify the service order template and the required dates in the service order. You do not need to enter the individual items, because they are copied from the service order template.

The following figure shows the structure of a service order template.

![The diagram represents the structure of a service order template, highlighting key components such as details, items, and reference objects, with additional explanatory information provided in the accompanying text.](https://learning.sap.com/service/media/topic/c0f4dbb1-2b15-4ab8-8394-d17a6d8a2236/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_SOTemplate.png "The diagram represents the structure of a service order template, highlighting key components such as details, items, and reference objects, with additional explanatory information provided in the accompanying text.")

The following assignments are made via the service order **details**:

- General data: Description, Employee Responsible, Service Employee Group
- Processing data: Search Term, Status
- Dates
- Notes

The following assignments are possible for **items**:

- Products: Services, spare parts
- Item Category: Service items, service parts items, sales items
- Service type, e.g. weekend
- Valuation type, e.g. senior
- Status
- Reference objects, e.g. pieces of equipment
- Notes

## How to Display a Service Order Template

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_33C77E8BB84031B1:demo)

## Maintenance Plan

The bike company in our example uses currently only single cycle plans to map their recurring service processes. In the future, the Bike Company might also use different forms of maintenance plans, for example, strategy plans.

Single cycle plans are used to manage the service of technical objects, that is, machines and operational systems, which are always inspected or maintained in the same way at fixed intervals.

In this plan, the same bike service is executed every two years based on manufacturer recommendations: 2025 - 2027 - 2029 - 2031 and so on.

The bike company needs to define maintenance plans so that service orders are generated every two years. The service orders contain details regarding the service tasks to be accomplished.

The maintenance plan is composed of **planning data** and **maintenance items**. It is used for generating **maintenance call objects** automatically. In SAP S/4HANA Service the maintenance call object service order is currently available.

The following graphic shows the structure of maintenance plan.

![Tree hierarchy with 3 level. Top level, maintenance plan. Middle level maintenance item(s) and planning data. Under maintenance items(s), technical objects, service contract/service order type, and service order template. Under planning data, Interval (cycle).](https://learning.sap.com/service/media/topic/d0700c06-5ad3-4dbb-a1e0-505d0bdda94f/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U8_L5_Maint_Plan_Struct.png "Tree hierarchy with 3 level. Top level, maintenance plan. Middle level maintenance item(s) and planning data. Under maintenance items(s), technical objects, service contract/service order type, and service order template. Under planning data, Interval (cycle).")

A **maintenance item** contains the following information:

- Reference object
- Service contract and service contract item
- Service order template
- Service order type
- Object list

The **scheduling data** contains the following information:

- Cycle or service interval
- Scheduling parameters for fine-tuning scheduling
- List of planned dates and call dates

## How to Display a Maintenance Plan

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_50C196087893CBB3:demo)

## Maintenance Plan Scheduling

You need to schedule all maintenance plans regularly to generate recurring service orders and to update planned dates for future service tasks.

The following graphic shows the main functions of the maintenance plan scheduling.

![The image illustrates four service process initiation options: start, new start, schedule, and manual call, emphasizing different methods for triggering service-related actions.](https://learning.sap.com/service/media/topic/dc46a7ba-3dbb-4c68-94ce-e0bc40fc3745/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Maintenance%20Plan%20Scheduling.png "The image illustrates four service process initiation options: start, new start, schedule, and manual call, emphasizing different methods for triggering service-related actions.")

- **Start**: This function is normally used to start a maintenance plan for an object that has just been put into operation, or for which preventive service or maintenance work is required.
    
- **New Start**: This function is normally used for a repeated start, for example, if scheduling has been carried out with wrong parameters.
    
- **Schedule**: This function is used to call up the next service order after the last service order has been completed.
    
- **Manual Call**: If you want to schedule a maintenance task for a particular date, you can schedule this date manually.
    

**Scenario:** Imagine you planned a single cycle plan with a two-year cycle and a cycle start on 01.03.2026.

Let's take a look at how this is done.

![The diagram depicts the process of scheduling a maintenance plan, including steps to check planning data, schedule the plan, and verify scheduled dates, with a detailed timeline for cycle start and planned service orders.](https://learning.sap.com/service/media/topic/dc46a7ba-3dbb-4c68-94ce-e0bc40fc3745/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit9_SingleCyclePlan.png "The diagram depicts the process of scheduling a maintenance plan, including steps to check planning data, schedule the plan, and verify scheduled dates, with a detailed timeline for cycle start and planned service orders.")

1. The **cycle start** defines the date from which the calculation of the planned dates should begin.
2. The **planned date** defines when the service orders are to be carried out.
    - Depending on the planned date you can define a separate call date to define the date when the order is to be created.
    - The call date is usually much earlier than the planned date to obtain a preprocessing phase, for example, for material procurement.

## How to Schedule a Maintenance Plan

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_70911426EDD5DB2:demo)

# Service Analytics

Objective

After completing this lesson, you will be able to explain the concept of service monitoring and analytics

## Introduction

This lesson covers the following process step:

![The image provides an overview of the Lead-to-Cash process for services, outlining key stages like master data, service contract management, recurring service, and service analytics, with a focus on understanding the current stage in the process.](https://learning.sap.com/service/media/topic/b1fb4e8e-18d4-4638-9a71-e5014481cc06/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Lead2Cash_Service4.png "The image provides an overview of the Lead-to-Cash process for services, outlining key stages like master data, service contract management, recurring service, and service analytics, with a focus on understanding the current stage in the process.")

## Service Monitoring and Analytics

Service monitoring and analytics are used to analyze key figures from a technical and a controlling perspective. They also provide a sound basis to improve and to optimize current service processes.

There are various SAP Fiori Apps available to gain an insight on the following service relevant topics:

- General overview on service issues
- Master Data
- Service Contract and Invoice Management
- Recurring Service

In the screen shot below you can see how the topics are listed in SAP Fiori. The application_Service Management Overview_ is highlighted.

![](https://learning.sap.com/service/media/topic/c82c13be-0370-4b90-b44a-33d4a4d1d2b9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/ServiceAnalytics.png)

When selecting the highlighted app, you will get the following information:

![](https://learning.sap.com/service/media/topic/c82c13be-0370-4b90-b44a-33d4a4d1d2b9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/ServiceAnalytics2.png)

1. Expiring Service Contracts
2. Average Repair Times
3. Service Contracts
4. Release Status for Billing
5. Service Orders
6. Incomplete Service Orders
7. Overdue Service Orders
8. Service Confirmations

The **Service Management Overview** is a single screen for a service manager to focus on their role-specific tasks. It enables the service manager to filter and react to information stemming from a range of applications.

As the graphic shows, you can obtain a graphical overview of key service process data and gain insights into the current service situation. Displaying the detailed information helps you examine and analyze data across various dimensions.

## How to Use Service Analytics

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_ABDBF0A738168AB5:demo)

## Summary: Advantages of SAP S/4HANA Service

SAP S/4HANA Service does not only simplify the service processes but is a win for the entire company as especially the customers benefit from the improved service processes.

Think about the following four points: How would you describe the advantages towards your customer?

- Organization and Master Data
- Service Contract and Invoice Management
- Recurring Service
- Service Analytics

Proposal how to describe the benefits:

- **Organization and Master Data:** The organizational structure of SAP S/4HANA Service is fully integrated in the enterprise structure of SAP S/4HANA. Additionally, the ongoing maintenance of Master Data reduces the processing times for transactions significantly.
    
- **Service Contract and Invoice Management:** Service Contracts represent long-term agreements with business partners specifying which services are offered on which conditions. Service Contracts are seamlessly integrated with Invoice Management, but can also be combined with various documents, for example Service Orders, Maintenance Plans.
    
- **Recurring Service:** Recurring Service simplifies the mapping of repetitive service tasks. Service Orders which need to be carried out on a regular basis can be generated automatically by scheduling Maintenance Plans.
    
- **Service Analytics:** With Service Analytics you can check key figures from a technical and a controlling perspective. Next to analyzing the current situation you can use historical data to optimize your service processes.