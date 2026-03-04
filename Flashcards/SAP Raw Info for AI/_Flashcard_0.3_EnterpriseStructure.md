# Defining the Enterprise Structure Using the Example of a Bike Company

Objective

After completing this lesson, you will be able to define and assign the enterprise structures used in SAP S/4HANA

## The Enterprise Structure Using the Example of the Bike Company

The bike company we use as example is an international company with various legal and regional entities – it has a tailored **enterprise structure**. An enterprise structure is a comprehensive organizational framework designed to reflect and manage a company's business processes, divisions, and units.

It provides for example answers to the following questions:

- Where do they produce their products?
- Who is responsible for buying their raw materials?
- Who is calculating their sales prices?

The following graphic summarizes how the organization of the bike company could be structured. There are various production sites, legal entities, departments, distribution centers, and warehouses that need to be managed and integrated.

![](https://learning.sap.com/service/media/topic/b642f6eb-386f-4f39-ab08-cddcb976d9e7/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/enterprise%20structure.png)

From the perspective of the various business departments and processes, there are diverse requirements and challenges related to the enterprise structure that must be considered in a software solution.

- **Financial Accounting**: In our example, the bike company prepares the financial statements based on the International Financial Reporting Standards (IFRS). As there are 12 global legal entities, local accounting standards must be considered too, for example, the US General Accepted Accounting Standards (GAAP). Due to IFRS 8 regulations, they also require financial key figures for the three areas of operation: bikes, spare parts, and service.
    
- **Controlling** wants to analyze and evaluate all costs and revenue from the entire company without consolidating them from the different entities. They need an internal structure for visualizing the different areas of responsibility they want to track. To analyze the profit margin, they want to track the profitability based on several characteristics.
    
- **HR** must consider various legal requirements to differentiate the business at site level. They want to have a differentiated view on employees and individual departments and gain insights into the internal employee structure, too.
    
- **Procurement**: The company has central purchasing for some materials, which means that they order the raw materials centrally for all facilities, negotiate the prices and, if possible, establish contracts with the preferred suppliers. On the other hand, there are also purchasing employees in every site to order spare parts and office materials for example.
    
- **Production**: There are two production sites in America and two in Europe. The production team must consider that production costs can be different in individual production plants. In each of their plants, they have storage areas for the materials. As they also want to store materials at the level of storage bin, they think about incorporating a warehouse management system to increase automation of their processes. They plan eight additional distribution centers from which they will deliver bicycles to their customers and materials to their flagship stores.
    
- **Sales** has a department in every subsidiary. Their customers and resellers can use these departments to place orders via different communication channels. A lean order placement process can help them to react fast, with high customer satisfaction. Because they sell through the internet, as well as directly to the reseller, they want to use separate channels for the distribution of their bikes. The sales departments should also be able to sell bikes from any other site.
    
- **Services**: All customers of the bike company contact the service team centrally in their customer interaction center. From there, they forward the individual service requests to the nearest and most suitable person responsible. Services are usually provided by a reseller, but they also offer services and technicians in all regional sites. Their service technicians are also deployed for internal maintenance.
    

How can such an enterprise structure be represented in SAP S/4HANA? Within the SAP system, the enterprise structure must ensure that data is efficiently managed and shared across different parts of the organization, enabling streamlined operations, improved decision-making, and enhanced business performance.

## Definition of the Enterprise Structure in SAP S/4HANA

When modeling the bike company in our example in SAP S/4HANA, we define a kind of picture of the company inside SAP S/4HANA and the possible corresponding applications. We must consider:

- On the one hand, the bike company has different applications for the departments to run different parts of their business processes. This is where they do the daily work, such as order materials and sell products. This is done in the applications of SAP S/4HANA .
    
- On the other hand, the bike company must configure the business processes for each application and for each enterprise structure. This is when we talk about "Customizing in SAP S/4HANA". Defining the enterprise structures isn’t done during daily business. It takes place as part of configuration or customizing of the system.
    

Note

We describe the following enterprise structure based on an SAP S/4HANA On premise system. Most enterprise structures are identical to those in SAP S/4HANA Cloud. The use and the necessity of the enterprise structures are the same, whether it is in SAP S/4HANA On premise or in the SAP S/4HANA Cloud system.

Explore the following figure to identify the various components of the enterprise structure in SAP S/4HANA. They are described below.

![](https://learning.sap.com/service/media/topic/ac1adcc3-ec94-41e4-8b79-94050212d2bf/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Enterpr_Structure_FINAL.png)

1. The **client** is the highest hierarchical enterprise structure within an SAP system that contains master records and tables. It represents a corporate group.
    
2. **Controlling:**
    - The **operating concern** represents the enterprise structure in a company for which the sales market has a uniform structure. It is the analysis level for profitability analysis.
    - The **controlling area** is the basic enterprise structure in controlling. A controlling area is a closed entity used for cost and revenue accounting. You can allocate costs and revenue only within a controlling area.
3. **Financial Accounting:**
    - The external accounting of a company within the corporate group is mapped using the organizational unit **company code**. Based on the company code, the legal requirements (commercial and tax) for financial reporting (for example,financial statement) are fulfilled.
    - The **segment** is an object of the enterprise structure that provides financial figures for objects (for example, regions and/or areas of operation) below the company code. The segment is an optional enterprise structure. The usage depends on the legal requirement, for example, the segment reporting according to US-GAAP (General Accepted Accounting Standards ) or IFRS (International Financial Reporting Standards).
4. **Sales and Distribution:**
    - A **sales organization** subdivides an enterprise based on sales requirements. It is responsible for selling goods and services.
    - A **distribution channel** characterizes the way in which goods and services are distributed. Companies use different distribution channels to separate sales for products, services, and maintenance.
    - A **shipping point** defines the place or location from which goods are shipped.
5. **General Logistics and Material Management:**
    - A **purchasing organization** is responsible for all purchasing activities, for example, processing requests for quotations and contracts.
    - A **plant** is the central enterprise structure in logistics. It subdivides an enterprise according to production, procurement, maintenance, and materials planning aspects.
    - A **storage location** is the sub-division of a plant where the stocks are physically stored and maintained within a plant. It is required to maintain at least one storage location per plant.
    - A **division** represents a certain group of materials or services and is mainly used for sales analytics.
    - The **valuation level** is defined by specifying the level at which material stocks are valuated. You can valuate material stocks at the following levels:
        - Plant level: Valuation must be at this level if you want to use the application component _production planning_ or _costing._
        - Company code level
6. **Human Resource Management**:
    
    A **personnel area** is a subdivision of a company code and organized according to human resources. The personnel area could represent different physical sites or reporting areas.
    
7. **Logistics Execution**:
    
    A warehouse complex is represented as a warehouse number in the **warehouse management system**. It is used to identify a complex warehouse setup. The physical location is usually decisive for the definition of the warehouse number. A warehouse number groups storage types and storage sections that are organized and maintained as a complete unit.
    

The graphic above includes arrows between the various components. They illustrate which elements of the enterprise structure are assigned to each other during customizing.

## Assignment of the Enterprise Structure in SAP S/4HANA

The assignment of structural elements in SAP S/4HANA can be compared with building connections between individual elements to be able to run a process end-to-end. Watch the following video to learn how this works.

The modeling of the enterprise structures

in customizing comprises two steps.

One, defining the enterprise structure and assigning it.

In this video, we focus on the assignment task.

The client reflects the entire company in

the enterprise structure in SAP S for HANA.

Therefore, the assignment task starts one level deeper with the

operating concern. Looking from the business perspective, the operating

concern is the entity where all the data flow from applications

ends, we do not need to assign it to a level above. As the operating

concern can summarise figures from various controlling areas, we

first need to assign the controlling areas to the operating concern.

In a second step, we assign the company code to the controlling

area to have a close integration between finance and controlling.

Please consider,

one controlling area can have several company codes, but usually only

Only one company code is assigned to one controlling area. To assign

several company codes, specific prerequisites must be fulfilled.

First, all company codes must use the same chart of accounts, which

is a list of all available general ledger or general ledger accounts.

Second,

all company codes and the controlling area use the same fiscal year.

The segments are not directly assigned in enterprise structure

customizing. They are determined during the postings in

finance. A personnel area is a subdivision of a company code.

Now the plant needs to be assigned to the company code.

Please consider,

a plant can only belong to one company code, but one company

code can have several plants. As we store our materials at the

plant level and must evaluate our materials, these values need to

be visible in the balance sheet from a financial perspective.

If a plant belonged to several company codes,

we would be practising creative accounting.

As a next step, we need to assign the storage locations to

plants. A plant can have several storage locations, and a

storage location can be assigned to several plants. However,

each combination of plant and storage location is

a separate physical unit, as the combination

between plant and storage location makes it unique.

A warehouse management system is needed if you use a rather

agile warehousing in your enterprise in contrast to fixed

warehousing, for which you would use inventory management.

When requiring a warehouse management application,

you can assign a warehouse number from warehouse management to

the combination of plant and storage location. This allows you

to use several storage locations in conjunction with warehouse

management or to use a storage location from an inventory

perspective only. For SAP S/4HANA, the solution for future

development is SAP Extended Warehouse management EWM. The SAP EWM

warehouse number is only linked to the SAP WM warehouse number.

The next important assignment is in context of the sales and distribution

process. A sales organisation must be first assigned to a company

code. You can assign a company code to several sales organisations,

but a sales organisation can only be assigned to one company code.

Then you assign a distribution channel to the sales organisation.

A distribution channel can be used by several sales organisations and

a sales organisation can have several distribution channels. For

example, if they sell through the internet and through physical stores.

Next, you assign the divisions to the sales organisation.

A division can be used by several sales organisations

and a sales organisation can have several divisions.

In SAP S/4HANA, some assignments are mandatory.

This is the case when defining a sales area.

A sales area is always a combination of a sales

organization, a distribution channel, and a division.

The assignment to the possible delivery plants is done on the

combination of sales organization and distribution channel. This

combination is sometimes referred to as a distribution chain. You can

assign any plant from any company code to a distribution chain.

Besides assigning the valuation level to a company code and

a plant, you must assign the shipping points. A plant can

have several shipping points and a shipping point can serve

several plants. This only makes sense with nearby plants.

The purchasing organisation can be assigned in three different ways.

Mostly, you will find a combination of the three possibilities. First,

it can be a central purchasing organisation

not assigned to any enterprise structure.

Second,

it can be a cross-plant purchasing organisation, which means the purchasing

organisation is assigned to a company code. The purchasing organisation

is then responsible for all plants assigned to the company code.

Or third, it can be a plant-specific purchasing

organisation, which means it is assigned to a plant.

The purchasing organisation is only responsible for this plant.

I hope you have now a first idea how the

enterprise structure is built in SAP S/4HANA.

I know, the assignment of structural elements might sound quite complex

at the beginning, but moving forward the logic behind becomes more

obvious and you will experience how it helps to run the daily business.

## Consolidation

As final step in this lesson, we now map the characteristics of our bike company example at the beginning with the enterprise structure in SAP S/4HANA.

Work through the tables below to consolidate what you learned so far. You will get a picture how to model the bike company in the Customizing of the SAP S/4HANA System.

### General Mapping

|Bike Company|SAP S/4HANA|
|---|---|
|The entire bike company|One client|
|Finance|Financial Accounting|
|Controlling|Controlling|
|Human Resources|Human Resource Management|
|Procurement|Materials Management|
|Sales and Services|Sales and Distribution|
|Production|Production|

### Detailed Mapping

|Bike Company|SAP S/4HANA|
|---|---|
|One view on costs and revenues|One controlling area (= bike company)|
|Profit margin based on different criteria|One operating concern (= bike company|
|12 independent legal entities|12 company codes|
|3 areas of operation (bikes, spare parts, services)|3 segments|
|Divers employee structure per site and department|12 personell areas|
|4 production sites with different costs|- 4 (production) plants<br>- Valuation level for each plant|
|8 additional distribution centers|8 distribution centers|
|Purchasing central or local|- One central purchasing organization<br>- One purchasing organization per plant<br>- Storage locations for each plant|
|Several warehouses|Warehouse management|
|1 sales department per subsidiary|One sales organization for each legal entity|
|3 sales channels (direct sales, internet, reseller)|3 distribution channels|
|1 central customer interaction center|Shipping points for each plant|
|1 service department per site|Equals the sales organization|

# Relating Enterprise Structures, Master Data, Transaction Data, and Documents

Objective

After completing this lesson, you will be able to relate enterprise structures, master data, transaction data, and documents to each other

## Introduction

The various entities or structures within an SAP system that are used to represent and organize business data are called "objects". They are essentially the fundamental building blocks of the system. The enterprise structure in SAP S/4HANA is one example - defining the organizational units and their relationships, for example client, company code, or plant.

In this lesson you get introduced to further key objects such as master data, transactional data, and documents and how they are related to the enterprise structure.

**Master data** is the core, foundational data that remains relatively unchanged over time. It's the data that an organization needs to conduct its business. Think of master data as the "nouns" of your business - the people, places, and things that are involved, for example:

- Customer data (like names, addresses, contact info)
- Product data (like product names, descriptions, prices)
- Employee data (like names, job titles, contact info)
- Supplier data (like company names, contact info)

**Transactional data** is the data that changes frequently and is generated by the day-to-day operations and transactions of an organization. Transactional data is the "verbs"of your business - the actions that happen, for example:

- Sales orders
- Invoices
- Payments
- Shipments
- Hires and terminations

In the context of master data and transactional data, **documents** refer to structured records or files that capture and store information pertinent to business operations.

- Master data documents are for example customer records, product information or vendor files.
- Transactional data documents are for example

## Master Data and the Enterprise Structure in SAP S/4HANA

Imagine you order a product from a retailer on the internet for the first time and are given the choice to create a customer account during the ordering process. In addition to your name and address, you store alternative delivery addresses, payment information such as credit card or bank data, and register for a product newsletter.

As soon as we log on with our customer account to make another purchase, the information we provided previously is populated automatically - so we do not have to enter it again.

This is the purpose of master data:

- The system holds all the essential information needed to map processes in a system and remain unchanged over a longer period.
    
- A complete maintenance of master data considerably reduces the processing time required for transactions, because the system can automatically propose the master data in the corresponding fields of the business transactions.
    

What is the relationship between the enterprise structure and the master data in an SAP system?

Let us look again at the example of our Bike Company. The same bikes will be manufactured in each of the four production plants. This raises the question whether certain product master data cannot be maintained centrally for all plants. On the other hand, we want to maintain different data for different plants, for example different goods receipt processing time. This enables us to have differentiated data by enterprise structures.

Play the video to learn how the enterprise structure organizes and supports master data maintenance using the example of the product master record.

Hi, in this video I want to tell you more about the relation

between the enterprise structure and the master data

in SAPS for HANA using the example of product master data.

The product master data holds all key information that a company

needs to manage a material within its organisation. This

information is separated according to the departments in the company.

The product master data defines, among other things, how a product is

sold, manufactured, purchased, inventoried, accounted and calculated.

These sections in the master record are managed

in relation to the enterprise structure.

The client level contains data applicable to the entire enterprise.

They are only maintained once and are automatically

available in the corresponding enterprise structures.

Typical master data objects at this level in the product

master record are product number and short text, volume,

weight or basic unit of measure For example, pieces.

The plant level contains data relevant to a specific

plant. A lot of data specific to purchasing, inventory

management and material valuation is stored at this level.

Examples of this data are the purchasing

group or the goods receipt processing time.

As a purchasing group defines different responsibilities,

you can for example separate responsibilities

of a US plant from a German plant.

All data that is valid for a particular storage location is stored at

this level, for example the storage bin processing or the picking area.

Further organisational levels can be relevant for other departments,

for example the sales data is entered depending on the sales

organisation and the distribution channel and you must specify a

warehouse number and a storage type for the warehouse management data.

I hope you can now explain how product master data and the

enterprise structure in SAP ES for HANA are related to each other.

## Display Product Master Data

This hands-on simulation demonstrates how to display a product master in the system.

Exercise[Start Exercise](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?library=library.txt&show=project!PR_2115FE51848B67A2:uebung)

## Transactional Data and Documents in SAP S/4HANA

Transactional data records single process steps in the SAP system. Compared to master data, they are of a rather short-lived nature. Typical examples for creating transactional data are entering a sales order, an incoming and outgoing invoice, or a purchase order for a supplier.

The data for a process step like creating a sales order is stored as a result by a document. The stored documents are also used for evaluations. This means that the sales totals with a customer are made up of its sales-relevant documents.

While creating a document, the document is always assigned to one or more enterprise structures.

Play the video to see an example how transactional data, master data and the enterprise structure are interacting.

Hi, in this video I explain how the enterprise

structure data and the master data in SAP,

as for HANA, are related to documents such as a sales order.

When creating a sales document, much mandatory information needs

to be entered. For example, a sales order must always be assigned

to a sales area consisting of following structural elements –

the sales organisation, the distribution channel and the division.

Based on the assignment of the sales area to the company code,

the company code is determined and populated in the sales order.

Whenever possible, master data is copied during the sales

order creation, thus avoiding re-entry of data. For example,

the user must enter the customer master number. The customer master

data is copied into all customer relevant fields of the document.

Once the product master numbers are

entered for the items being ordered,

the relevant product master data will

be copied to the sales order as well.

Finally, when the sales order is saved the sales

document receives a unique document number.

You should now be able to explain how the enterprise

structure data and the master data in SAP as for

HANA are related to documents such as a sales order.

## Create a Sales Order

#### This hands-on simulation demonstrates Create a Sales Order in the system.

Exercise[Start Exercise](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?library=library.txt&show=project!PR_9C95A956278DBFAA:uebung)

## Summary

### Master Data

- Have all the essential information required to map processes in a system
- Remain unchanged over a long period
- Are maintained with a reference to the enterprise structure
- Examples:
    - Product master data (material master)
    - Customer or vendor master data
    - G/L accounts
    - Cost center
    - Employee master data

### Transactional Data / Documents

- Records single process steps in the SAP system
- Short-lived nature
- Documents always assigned to one or more enterprise structures
- Examples:
    - Create sales order
        
    - Post vendor invoice
        
    - Create production order

# Describing the Effects of the Central Objects on Different SAP Applications

Objective

After completing this lesson, you will be able to explain the necessity of master data synchronization to different SAP applications

## Master Data Synchronization

SAP integrates various solutions to empower enterprises running their business processes end-to-end. SAP SuccessFactors is for example included to run the _recruit to retire_ process or SAP Ariba to run the _procure to pay_ process. The central objects in SAP S/4HANA to organize and process business data such as the enterprise structure, master data, transactional data, and documents are therefore relevant for other solutions, too. The data must be properly integrated and synchronized across the different solutions.

Play the video to learn more about master data integration and master data governance cross SAP solutions.

In this video, you learn why master data integration and master

data governance is important to run end-to-end business processes.

Let us begin with SAP as for HANA.

In SAP as for HANA, we have, for example,

plant and company code as enterprise structures

and product and vendor as master data records.

Now, let us have a look on the procurement solution from SAP Ariba. As

this solution has been developed by a different team, they have different

data structures. Regardless, they also need enterprise structures,

master data and transactional data.

When using SAPI as Fahana in conjunction with SAP Ariba,

we have the enterprise structures and master data structures

doubled. To avoid maintaining the master data twice,

we connect the two systems and exchange the

data. This is called a point-to-point connection.

The SAP Success Factor solution is used for human resource management.

Here the same concept applies. We need a company

code and a person master data record. However,

in order to run some applications, we also need

an employee master record in SAP, as for HANA.

To maintain the master data only once, we connect the

systems and implement a data exchange between them.

There could be additional SAP solutions that require enterprise

structures and master data as well, such as SAP Customer

Cloud or SAP Integrated Business Planning, IBP. All these

systems should now be connected for exchanging the data, enterprise

structures, master data records, and transactional data.

The more systems we have, the more connections we need.

All of this needs to be maintained and kept up to date.

We can use master data integration, MDI, to reduce the number of

connections and have a central instance to maintain the exchange

between the systems. Master Data Integration refers to the synchronization

of master data across all applications in its current state.

SAP Master Data Integration uses SAP One data model for out-of

-the-box SAP integration and openness to non-SAP environments.

Ease of integration is created because you only need to learn a

single language to integrate across your application landscape.

Master Data Integration is complemented by SAP Master Data

Governance to ensure trust in master data with key capabilities

including central governance, consolidation and data quality

management. The combination of the two disciplines allows for new

agile approaches for managing master data across an enterprise.

I hope I could give you some insights why master data

governance, master data integration and master data

synchronization is so important in context of SAP solutions.

### Summary

Master data records are necessary in each used SAP solution. Master data integration (MDI) and master data governance (MDG) are crucial for running end-to-end business processes because they ensure data consistency, accuracy, and accountability across different departments and systems.

MDI consolidates data from various sources to provide a single, trusted view, while MDG oversees data quality, security, and compliance. Together, they facilitate seamless operations, improve decision-making, and enhance efficiency by reducing data silos, errors, and redundancies, ultimately leading to better business outcomes.


------- ADDITIONAL QUIZ QUESTIONS -------

NOTE: "The following are all the questions for this specific module. Below each number, there are instructions/questions and a list of answers. (X) denote correct answers. Brackets ("[]") denote additional comments for that specific question.

1.
A product master record can only be assigned to one plant.
Choose the correct answer.

True

(X) False

[A product master record can have several plant views. This allows you to define different values for each plant. For example, the planned goods receipt processing time differs between the plant in the United States and Germany.]

2.
Which of the following objects are used to structure the business processes in SAP S/4HANA?
There are three correct answers.

(X) Plant

Document

Cost Center

(X) Client

(X) Distribution Channel

[Plant, Client and Distribution Channel are objects of the enterprise structure. They are used to organize the business processes in SAP S/4HANA.]

3.
Documents are only created for Financial Accounting related business transactions in SAP S/4HANA.
Choose the correct answer.

True

(X) False

[The document principle in SAP is not restricted to Financial Accounting. It is used system wide.]

4.
Which of the following enterprise structures belongs to Financial Accounting?
There are two correct answers.

Operating Concern

Division

(X) Company Code

Valuation Level

(X) Segment

5.
The delivery plant is assigned to the sales area.
Choose the correct answer.

True

(X) False

[A delivery plant is assigned to the distribution chain, which is a combination of sales organization and distribution channel.]

6.
Which of the following are valid direct assignments of enterprise structures?
There are two correct answers.

Segment to Company Code

Distribution Channel to Plant

(X) Sales Organization to Company Code

Purchasing Organization to Controlling Area

(X) Shipping Point to Plant

7.
With a point to point interface solution for master data integration, if you have 4 systems that all need to communicate, how many integration channels are needed?
Choose the correct answer.

Three

Four

Five

(X) Six

[Since each system needs a direct interface to each other, you would end up with 6 separate connections. Adding a 5th system, would require 10 connections!]