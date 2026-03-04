# Identifying the Basics of Financial and Management Accounting

Objective

After completing this lesson, you will be able to describe Financial Accounting and Management Accounting

## Financial Accounting

Accounting is divided into two major areas: Financial Accounting (FI) and Management Accounting (CO).

Identify the FI areas in the following graphic: The General Ledger (G/L) with the various sub-ledgers.

![General Ledger Accounting diagram. At the center are Balance Sheet Accounts with Profit and Loss Accounts below (Expense and Revenue). Three subledgers feed into the Balance Sheet Accounts: Accounts Receivable (Customer) from the left, Accounts Payable (Vendor) from the right, and Asset Accounting (Asset) from the lower left. Green T‑account marks appear under each category label.](https://learning.sap.com/service/media/topic/d200d209-635b-406b-bd9c-13bf84c62738/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_Balance%20Sheet.png "General Ledger Accounting diagram. At the center are Balance Sheet Accounts with Profit and Loss Accounts below (Expense and Revenue). Three subledgers feed into the Balance Sheet Accounts: Accounts Receivable (Customer) from the left, Accounts Payable (Vendor) from the right, and Asset Accounting (Asset) from the lower left. Green T‑account marks appear under each category label.")

- The main purpose of **General Ledger Accounting** is to fully represent external accounting and the accounts involved in it. Recording all business transactions and SAP S/4HANA that is fully integrated with all other operational areas of your company, ensures that the accounting data is always complete and accurate. Example: A billing document in the sales process results in an automatic increase in receivables in the balance sheet and our revenue posting.
    
- **Accounts Payable** records accounting data such as incoming invoices or outgoing payments for each individual supplier. Accounts Payable focuses on the management of accounting transactions for individual suppliers. Posting on a supplier account updates the general ledger at the same time. For example, posting a supplier invoice increases the liabilities G/L account and the Balance Sheet of the Bike Company.
    
- **Accounts Receivable** monitors and clears,a company's customer receivables. Similar to Accounts Payable, this subledger focuses on the management of accounting transactions for individual customers. Each customer account is linked to General Ledger Accounting. For example, if we receive an incoming payment from a customer, the receivables on their customer account and the total receivables in the General Ledger and the balance sheet are reduced.
    
- **Asset Accounting** is used to map the complete financial life cycle of fixed assets, such as buildings, computers, and industrial machines. Asset accounting records detailed information for transactions involving fixed assets. Typical transactions and asset accounting are asset acquisitions, transfers, and asset retirement postings. As with customer and supplier accounts, these transactions are posted to the individual asset as well as the General Ledger Account at the same time through the single transaction.
    

## Management Accounting

Management Accounting or Controlling (CO) contains all the functions necessary for controlling cost and revenue effectively. It covers all aspects of management controlling including tools for compiling information to manage a company.

Controlling processes data, which comes from other SAP solutions. The following graphic introduces the different areas of Controlling and its basic value flow with Financial Accounting.

![Integration of G/L with subledgers and Controlling. Asset, Customer (AR) and Vendor (AP) subledgers feed Balance Sheet Accounts in General Ledger. Profit and Loss Accounts include Expense and Revenue, which map to Cost Element Accounting as Primary Cost Element, Secondary Cost Element, and Revenue Element. Primary costs flow to Overhead Cost Controlling (cost centers) and then to Product Cost Controlling (product cost planning and cost object controlling). Results, together with revenue elements, roll into Margin Analysis.](https://learning.sap.com/service/media/topic/c7b863a6-4d5a-45ba-9d76-401054825b75/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_General_ledger.png "Integration of G/L with subledgers and Controlling. Asset, Customer (AR) and Vendor (AP) subledgers feed Balance Sheet Accounts in General Ledger. Profit and Loss Accounts include Expense and Revenue, which map to Cost Element Accounting as Primary Cost Element, Secondary Cost Element, and Revenue Element. Primary costs flow to Overhead Cost Controlling (cost centers) and then to Product Cost Controlling (product cost planning and cost object controlling). Results, together with revenue elements, roll into Margin Analysis.")

- In **cost element accounting** costs and revenues are separated according to objective criteria. Material cost, personnel costs, depreciation costs, and so on.
    
    - **Primary costs and revenues:** Financial accounting is a primary source of data for management accounting. Most expense or revenue postings in the general ledger result in a cost or revenue posting. In management accounting. These costs or revenues are considered primary costs or revenues.
    - **Secondary costs:** There are also cost flows that originate directly from controlling e.g. facility management provides a service for production or administration. These type of internal costs are considered secondary costs and use special GL accounts called secondary cost accounts.
- **Product cost controlling:** Various types of objects can be cost objects in SAP, for example a sales order to produce ten bicycles, or a production order for the make-to-stock production of certain bike parts can be cost objects. Costs resulting from these activities can be assigned directly to these account assignment objects. Cost object controlling in product cost controlling records and monitors all costs, allowing you to compare it with planned costs. So you can identify where variants arise and to implement corrective measures.
    
- Planned costs, or the outcome of **product cost planning**: This area in product cost controlling calculates the estimated production costs and thus provides a minimum selling price for breaking even.
    
- **Overhead cost controlling** gathers all costs that can be assigned directly to a cost object, for example the marketing cost for an advertising campaign. Using a variety of allocations methods. These overhead costs are transferred to product cost controlling, giving a more complete view of the actual costs of a product.
    
- **Margin analysis:** It is important to know what the bike company in our example earns by selling its products. Margin analysis collects all costs and revenues incurred at analyzes the operating results of the company focusing on a market segment view margin analysis. It provides for example the answer to the following question: What operating profit did we generate with reseller A in the region _North America_ with our bike parts last quarter?
    

### Test Your Knowledge 

**Question:** Which of the following enterprise structures do you think are necessary for Financial Accounting in a bike company and why? First, think about the enterprise structures in SAP S/4HANA listed below! Then, read the text afterward to get the correct answer.

- Operating Concern
- Valuation Level
- Controlling Area
- Sales Organization

**Answer**: The **controlling area** and the **operating concern** are required for Management Accounting.

- The controlling area is the basic enterprise structure in Management Accounting. It is a self-contained entity used for cost and revenue accounting.
- The operating concern represents an organizational unit for which the sales market has an uniform structure. This is the valuation level for Margin Analysis.
# Managing General Ledger Accounting: Basic Functions

Objective

After completing this lesson, you will be able to manage basic functions of general ledger accounting including master data, posting, reporting, and general journal entries

## Introduction

The first business process step within the **Record-to-Report** process is: **Manage G/L Accounting** . The following graphic provides a simplified view which SAP solution is used.

SAP Solution Overview: Financial Accounting

![SAP Solution Overview for Financial Accounting. The diagram positions FI as a core SAP S/4HANA module integrated with peer modules (CO, HCM, MM, PP, EWM, SD, CS, EAM) and connected through SAP Business Technology Platform to surrounding SAP cloud solutions including SAP Analytics Cloud, SuccessFactors, Ariba, IBP, Intelligent Asset Management, and CX. The intent is to orient the learner to where FI sits within the overall SAP solution landscape.](https://learning.sap.com/service/media/topic/eda7db80-749e-47c1-8191-bea71e6b98ba/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation.png "SAP Solution Overview for Financial Accounting. The diagram positions FI as a core SAP S/4HANA module integrated with peer modules (CO, HCM, MM, PP, EWM, SD, CS, EAM) and connected through SAP Business Technology Platform to surrounding SAP cloud solutions including SAP Analytics Cloud, SuccessFactors, Ariba, IBP, Intelligent Asset Management, and CX. The intent is to orient the learner to where FI sits within the overall SAP solution landscape.")

Managing a general ledger account involves defining the account's master data, including account type, currency, and associated profit center. This is followed by posting relevant financial transactions to the account and monitoring its balance through periodic reporting and reconciliation.

The next graphic illustrates where the process step **Manage G/L Accounting**  is located in the **Record-to-Report** process flow.

![Record-to-Report process overview. A timeline presents stages from creditworthiness through master data and financial transactions to money and reporting. The highlighted focus is Manage G/L accounting within the Master Data and Financial Transactions phase. Related areas shown include accounts payable, accounts receivable, and asset accounting, with subsequent activities such as financial close, payments, and disputes leading to the final reporting step. Further details are provided in the accompanying text.](https://learning.sap.com/service/media/topic/eda7db80-749e-47c1-8191-bea71e6b98ba/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process.png "Record-to-Report process overview. A timeline presents stages from creditworthiness through master data and financial transactions to money and reporting. The highlighted focus is Manage G/L accounting within the Master Data and Financial Transactions phase. Related areas shown include accounts payable, accounts receivable, and asset accounting, with subsequent activities such as financial close, payments, and disputes leading to the final reporting step. Further details are provided in the accompanying text.")

As part of the first integration test during the SAP implementation project, you have a look at the most important master data in Financial Accounting. The first manual postings are then made in General Ledger Accounting. You also test the first reporting options in the General Ledger.

In this lesson, you will learn more about the following functions of G/L accounting:

- **Chart of Accounts**: It serves as a framework to ensure the G/L accounts are created uniformly in Financial Accounting.
    
- **Financial Statement**: The structure of a balance sheet and profit and loss (P&L) statement is determined in SAP by the financial statement version.
    
- **General Journal Entry**: A general journal entry is a recording of a financial transaction that affects at least two accounts in a company's general ledger. While most accounting-relevant transactions are posted automatically to the general ledger, there are also operational general ledger postings that are entered manually in general ledger accounting. 
    

## Chart of Accounts and G/L Accounts

The General Ledger (G/L) is the core of Financial Accounting. All accounting-relevant business transactions are posted to G/L accounts. G/L accounts are managed using a **chart of accounts**.

The chart of accounts serves as a framework to ensure the G/L accounts are created uniformly in Financial Accounting.

**Example:** Imagine our bike company has decided to use the standard chart of accounts YCOA delivered with SAP S/4HANA in each company code for their operational postings.

This decision has the following advantages:

- Uniform structure of individual general ledger accounting
- Prerequisite for cross-company code controlling

The following graphic illustrates that the YCOA chart of accounts is assigned to each company code in configuration and is referred to as its operating chart of accounts.

![Chart of Accounts feeding multiple company codes. A single operating COA branches to Bike Company DE (company code 1010), Bike Company US (company code 1710), and additional companies, with each company ledger labeled FI and GL to show use in Financial Accounting and General Ledger.](https://learning.sap.com/service/media/topic/e9d91c29-3a35-4c43-b036-018bda9a19c7/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_Operating%20Chart%20.png "Chart of Accounts feeding multiple company codes. A single operating COA branches to Bike Company DE (company code 1010), Bike Company US (company code 1710), and additional companies, with each company ledger labeled FI and GL to show use in Financial Accounting and General Ledger.")

The **G/L accounts** in the YCOA chart of accounts are grouped according to business aspects using their eight-digit G/L account number as follows.

![This graphic explains how a standard chart of accounts groups general ledger (G/L) numbers into Balance Sheet and Profit and Loss categories so users can quickly infer financial statement impact from the account range.](https://learning.sap.com/service/media/topic/e9d91c29-3a35-4c43-b036-018bda9a19c7/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/GeneralLedger.png "This graphic explains how a standard chart of accounts groups general ledger (G/L) numbers into Balance Sheet and Profit and Loss categories so users can quickly infer financial statement impact from the account range.")

The **account number** enables the accounting department to select, post, and analyze documents quickly and reliably. 

In addition to the account number and description, a G/L account master record also contains information about how business transactions are posted to G/L accounts and how the posting data is processed.  

**Example:** A specific profit and loss account always needs to be posted in relation to sales tax, or a G/L Account can only be posted using certain currency (for example, a foreign currency account that is managed in USD (US Dollars) at the bank). 

Hint

If you run several systems in parallel, you can look for possibilities to help keep master data consistent for all systems. Master data in different systems can be managed in parallel by using SAP Master Data Integration and SAP Master Data Governance, which run on SAP Business Technology Platform (SAP BTP).

## Financial Statement Version

General Ledger Accounting provides the information needed to create a **balance sheet** and a **profit and loss (P&L) statement**. These reports must meet country-specific requirements.

The following graphic illustrates the financial statements based on the country-specific standards.

![Diagram showing Bike Company SE preparing parallel financial statements under three frameworks: IFRS for group reporting, German HGB, and US‑GAAP for the USA. Each framework presents the same high‑level sections—Assets, Equity and Liabilities, and Profit & Loss—with items and sub‑items, indicating that the company maps its accounts to different reporting structures to satisfy group and local GAAP requirements. The details of the item groupings and mappings are described in the text that follows.](https://learning.sap.com/service/media/topic/f1b0a6e5-61fc-4a97-9c6f-aa6bfcc25667/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_Country_Specific.png "Diagram showing Bike Company SE preparing parallel financial statements under three frameworks: IFRS for group reporting, German HGB, and US‑GAAP for the USA. Each framework presents the same high‑level sections—Assets, Equity and Liabilities, and Profit & Loss—with items and sub‑items, indicating that the company maps its accounts to different reporting structures to satisfy group and local GAAP requirements. The details of the item groupings and mappings are described in the text that follows.")

### Summary

- The structure of a balance sheet and P&L statement is determined in SAP by the **Financial Statement Version**.
    
- The required G/L accounts are assigned to the individual balance sheet and income statement sub-items.
    
- The aggregated values of the assigned G/L accounts are then displayed at the level of the corresponding balance sheet or P&L items and sub-items.
    

## How to Display the Chart of Accounts

In the following demo, you see the **Operating Chart of Accounts** used by the bike company in our example. We will analyze the structure of G/L accounts that you will use for G/L account test postings. Finally, we will check whether selected accounts have been assigned in the financial statement version.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_F9E679293D9546B9:demo)

## How to Display the Financial Statement Version

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_C916D203E4293099:demo)

## General Journal Entry

A general journal entry is a recording in a company's financial records that documents the specifics of a financial transaction.

If a general journey entry in SAP is posted, the G/L account document consists of the following two areas:

- **Document Header**: The document header contains general information about the document that is valid for all document items.
    
- **Document Items**: The information of a document item includes the amount, account number, assignment of debit or credit, as well as other information about the specific business transaction.
    

The screen shot below shows a G/L account posting in connection with a balance sheet and a P&L account. Identify the basic structure of the G/L account document and the initial reporting options in Financial Accounting.

![Annotated screenshot of the SAP Fiori Post General Journal Entries application. Seven numbered callouts mark the essential components for posting a journal entry: dates and period, journal entry type, company and currency context, the line‑item area, debit fields, credit fields, and the overall balance indicator. The purpose is to show how the app captures header data and line items while offering a real‑time check that debits equal credits. The numbered items are explained below.](https://learning.sap.com/service/media/topic/af813c63-5769-4c0f-a333-d5b8b9402545/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Journal%20Entries.png "Annotated screenshot of the SAP Fiori Post General Journal Entries application. Seven numbered callouts mark the essential components for posting a journal entry: dates and period, journal entry type, company and currency context, the line‑item area, debit fields, credit fields, and the overall balance indicator. The purpose is to show how the app captures header data and line items while offering a real‑time check that debits equal credits. The numbered items are explained below.")

1. The **Journal Entry Date** is the date the original document was issued. The **Posting Date** is the date the document was entered in the system.
    
2. The**Journal Entry Type** is a business transaction classification used to filter and refine the documents displayed. Further examples are Vendor Invoice (KR), Payment Posting (ZP), or Asset Posting (AA).
    
3. **Company Code:** Journal entries are entered at Company Code level.
    
4. **General Ledger Account:** Only the G/L Accounts that are part of the operating chart of accounts assigned to the current Company Code are displayed.
    
5. **Debit:** When a value is entered here, the value on the debit side of the account is updated.
    
6. **Credit:** When a value is entered here, the value on the credit side of the account is updated.
    
7. **Total Balance:** The total debit and credit posting must be equal. Key Concept: Double-entry bookkeeping
    

In SAP S/4HANA, most accounting-relevant transactions are posted **automatically** to the general ledger. **Example:** A goods issue in sales automatically leads to a G/L account posting in the general ledger.

However, there are also operational general ledger postings that are entered **manually** in General Ledger Accounting.  **Example:**. At our bike company you sometimes make cash payments. A donation of EUR 500 was made in cash and must now be entered as a G/L account posting in General Ledger Accounting. This business scenario of manual postings is a good way to test the settings and the configuration of the General Ledger Accounting.

The following demo shows how to post this accounting document in the general ledger.

## How to Post a General Journal Entry

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_7EEC9D31AF39A09B:demo)

## Reporting: Analyzing General Journal Entries

A general journal entry is crucial for **reporting** in Financial Accounting because it serves as the initial record of financial transactions, documenting the specific accounts affected and the amounts involved. This systematic recording ensures accuracy and completeness in tracking financial activities, providing a basis for generating financial statements.

As the following graphic illustrates, the general journal entries can be accessed and analyzed in several ways in the system. You can review the entries in detail from the total values in the balance sheet and profit and loss statement, through an item display to the document level. Or you call up specific documents using an account or document display to change or reverse them if necessary.

The original document (for example, an invoice or credit memo) can also be attached to the journal entry document.

![Process diagram illustrating multiple navigation paths to access and analyze general journal entries. Journal Entry serves as the hub connecting balances and source documents: from Balance Sheet or Profit and Loss totals, users drill to a Line Item Display and then to a Document Display; from an account’s Balance Display they can open line items; and from a Journal Entry they can open the originating document directly to review, change, or reverse it if needed. The goal is to show traceability from aggregated figures to individual documents for reconciliation and audit. The details shown in the process flow are described in the text that follows.](https://learning.sap.com/service/media/topic/ec3845f8-eff8-415e-aa80-bc3670f27136/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Analyzing_Journal_Entry.png "Process diagram illustrating multiple navigation paths to access and analyze general journal entries. Journal Entry serves as the hub connecting balances and source documents: from Balance Sheet or Profit and Loss totals, users drill to a Line Item Display and then to a Document Display; from an account’s Balance Display they can open line items; and from a Journal Entry they can open the originating document directly to review, change, or reverse it if needed. The goal is to show traceability from aggregated figures to individual documents for reconciliation and audit. The details shown in the process flow are described in the text that follows.")

**Scenario:** Imagine the situation that the accounting department of our bike company wants to check the cash desk posting in the balance sheet and the P&L statement. Work through the following demonstration to learn how they do that in the SAP system.

## How to Create a Balance Sheet and P&L Statement

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_ED022C6721A343BE:demo)

# Managing General Ledger Accounting: Integration Aspects

Objective

After completing this lesson, you will be able to explain the main integration aspects of Financial and Management Accounting and the function of the G/L account type

## Integration Aspects of Financial Accounting and Management Accounting

In accounting with SAP S/4HANA, the data from Financial Accounting (FI) and Management Accounting (CO) is processed in a uniform data environment. This applies to both transaction data and accounting master data.

While Financial Accounting considers inventory values, expense, and income, only costs and revenues are processed in Controlling.

Not all expenses or income in FI are equal to costs or revenues in CO. For example, transactions that are posted as expenses in FI will probably not be considered in CO when they are not directly related to the goods and services of the bike company.

In the following graphic, identify which business transaction is relevant for FI and / or CO.

![Accounting integration diagram conveying how a vendor invoice triggers coordinated postings across Financial Accounting (G/L and AP subledger) and Controlling. An invoice for office supplies of 1,000 € posts a credit to the vendor in the AP subledger; the same amount updates the G/L via the payables reconciliation account to keep subledger and general ledger in sync. In parallel, the G/L debits the Office Supplies expense account, and the amount is carried as a primary cost to the relevant cost center for management reporting. The intention is to show that one AP invoice creates balanced entries, automatic reconciliation, and cost assignment for analysis. The details shown in the diagram are described in the accompanying text.](https://learning.sap.com/service/media/topic/eca0f60f-38bb-4604-aa8f-48b9f8b2dcd0/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_DeterminingFI_CO.png "Accounting integration diagram conveying how a vendor invoice triggers coordinated postings across Financial Accounting (G/L and AP subledger) and Controlling. An invoice for office supplies of 1,000 € posts a credit to the vendor in the AP subledger; the same amount updates the G/L via the payables reconciliation account to keep subledger and general ledger in sync. In parallel, the G/L debits the Office Supplies expense account, and the amount is carried as a primary cost to the relevant cost center for management reporting. The intention is to show that one AP invoice creates balanced entries, automatic reconciliation, and cost assignment for analysis. The details shown in the diagram are described in the accompanying text.")

## Account Type

The distinction of whether a transaction is relevant for Financial Accounting (FI) and/or Management Accounting (CO) is made by the **G/L Account Type** in the G/L Account Master Record.

Explore the graphic below to learn more about the function of the account type.

![Conceptual mapping of FI G/L account groups to CO cost element accounting. Profit and Loss accounts split into two meanings: “Primary Costs or Revenue,” which are CO-relevant and become cost or revenue elements, and “Non-operating Expense or Income,” which are not CO-relevant. A separate group of “Secondary Costs” is also CO-relevant and represents internal allocations within CO. Balance sheet–oriented accounts (including cash) are shown as FI-only and do not create CO elements. A legend distinguishes economic terms, G/L account types, CO relevance, and cost/revenue elements.](https://learning.sap.com/service/media/topic/d388cd0e-054e-4b36-81d9-dd81993307a3/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_AccountType.png "Conceptual mapping of FI G/L account groups to CO cost element accounting. Profit and Loss accounts split into two meanings: “Primary Costs or Revenue,” which are CO-relevant and become cost or revenue elements, and “Non-operating Expense or Income,” which are not CO-relevant. A separate group of “Secondary Costs” is also CO-relevant and represents internal allocations within CO. Balance sheet–oriented accounts (including cash) are shown as FI-only and do not create CO elements. A legend distinguishes economic terms, G/L account types, CO relevance, and cost/revenue elements.")

In the following table you find a list of the various account types and their definition.

#### Account Types

|Account Type|Function|
|---|---|
|Balance Sheet Account|The balances of the corresponding accounts are reported in the balance sheet only. The transaction figures are not relevant in Controlling.|
|Cash Account / Bank Reconciliation Account|This G/L account type is only relevant for the balance sheet reporting in FI. It offers the option to manage bank accounts using a single reconciliation account in FI|
|Non-Operating Expense or Income|This is an income statement account that records costs and revenues from activities that are not part of the main purpose of the company, for example a donation. Cost or revenue elements are not created when a corresponding G/L account is entered in the system.|
|Primary Costs or Revenue|This is an income statement account that functions as a cost element for primary costs or revenue. Primary costs reflect operating expenses such as payroll, selling expenses, or a goods issue posting. When using such an account type, the system automatically creates the corresponding cost or revenue element.|
|Secondary Costs|Secondary costs result from value flows within the organization, such as internal activity cost allocations, overhead allocations, and settlement transactions. Secondary costs will be defined as a G/L account but can only be posted within CO.|

## How to Display the G/L Account Type

Let’s check two G/L accounts master data to see whether the correct G/L account type is assigned and to review additional controlling information.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_6E4CB10FE988CEAE:demo)

## General Journal Entries integrated with Controlling

As soon as cost or revenue element exists in Management Accounting, CO also needs to know the information who incurred these costs or revenues. This is done by CO-related account assignment objects at line-item level of the general journal entry.

The following demo shows an integration test performed in connection with the Office Supplies primary cost account 65100000. We use the CO object cost center from Overhead Cost Controlling as the CO account assignment object.

## How to Post and Analyze Journal Entries Integrated with Controlling

Check out how to  upload and analyze general journal entries with a cost center entered:

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_6972349EC0C6C6A7)

## Further Reading

- [Chart of Accounts](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/651d8af3ea974ad1a4d74449122c620e/9f53c2531bb9b44ce10000000a174cb4.html?version=2021.000)
- [G/L Account Master Data](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/651d8af3ea974ad1a4d74449122c620e/381146531c9eac48e10000000a423f68.html?version=2021.000)
- [General Journal Entries](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/651d8af3ea974ad1a4d74449122c620e/b050d7531a4d424de10000000a174cb4.html?version=2021.000)

# Managing Accounts Payable

Objective

After completing this lesson, you will be able to use relevant data and functions in accounts payable for example to process payments to a vendor

## Introduction

The next step within record-to-report process is **Manage Accounts Payable**.

The graphic shows where we are in the overall process flow:

![This image illustrates a overview of the Record-to-Report process, highlighting the current focus within the workflow. The process is depicted as a horizontal timeline with five key stages: Creditworthiness, Master Data, Financial Transactions, Money, and Reporting. The highlighted section, Financial Transactions, is emphasized with a yellow box, indicating the current stage of focus. Within this stage, the task Manage accounts payable is specifically outlined, suggesting it is the primary activity being addressed.](https://learning.sap.com/service/media/topic/aa9faf7d-27bb-467e-b8e4-67c7f5e54a38/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process%202.png "This image illustrates a overview of the Record-to-Report process, highlighting the current focus within the workflow. The process is depicted as a horizontal timeline with five key stages: Creditworthiness, Master Data, Financial Transactions, Money, and Reporting. The highlighted section, Financial Transactions, is emphasized with a yellow box, indicating the current stage of focus. Within this stage, the task Manage accounts payable is specifically outlined, suggesting it is the primary activity being addressed.")

Accounts Payable records and administers accounting data for each individual vendor. As soon as we have accounting-relevant transactions, such as incoming invoices or outgoing payments in relation to a vendor, an account (master data) is needed in Accounts Payable.

In this lesson, you will learn more about the following:

- The concept of the **business partner** as central master data in Accounts Payable: You will see how the business partner master data is structured and how to define it as a vendor for the accounts payable department of the bike company we use as example.
    
- In addition to creating a business partner, you learn how to **post incoming invoices** in Financial Accounting. Reporting is also used to track the integration with Financial Accounting and Management Accounting.
    

**Scenario:** Imagine the situation that our bike company has suppliers that deliver goods and services for multiple company codes. The accounting department asks whether vendor master data must be defined separately for each company code. What do you think? Continue to find the correct answer.

## Business Partner: FI Vendor

The master data of vendors (this is the term used in Accounts Payable) is administered by the **business partner** in SAP S/4HANA. The business partner allows you to centrally maintain master data for different SAP solutions in one place.

The business partner data that is relevant for Accounts Payable is, therefore, subdivided into the following two areas:

- **General data** is valid for a single client. General data includes data such as the vendor’s address, control data, bank details, and contact persons.
    
- **Financial Accounting data** is maintained at the company code level. Company code data includes data such as the link to the General Ledger Accounting, information for correspondence, and the payment methods for payment transactions.
    

Because the general data is maintained at client level, it is automatically available to all company codes (and other SAP solutions). Therefore, there is no need to define them separately for each company code.

In the company code views, each company code can then maintain its specific Financial Accounting data, such as VAT information or payment methods (for example, a bank transfer or check).

### Business Partner Role

When you define a new business partner, you must assign a predefined **business partner role**. The business partner role provides the master data fields to provide input for the corresponding task in the SAP system.

Examples:

- Customer
- Supplier
- FI Customer
- FI Vendor

The **FI Vendor** role is required to maintain data that is specific to Financial Accounting for Accounts Payable at **company code level**.

If this vendor is also used as a supplier in purchasing, you will extend an existing business partner in connection with the business partner role provided for this (business partner role: Supplier). This business partner role is relevant for the Source-to-Pay process.

Check the role-related data of the FI vendor role below. Please note, that the general data has to be provided for each business partner role.

![This image represents the Business Partner Role of an FI Vendor, providing key details about the vendor's general and accounting data. The general data includes the vendor's name, Antonio Rodriguez, their address at Vendor Path 7, 10123 Berlin, and their bank account information (partially redacted). The accounting data specifies two company codes: 1010 for Bike Company Germany and 1710 for Bike Company US.](https://learning.sap.com/service/media/topic/b51ce54e-09d9-49ad-8c10-85cf1929dcb9/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/BP%20FI%20Vendor.png "This image represents the Business Partner Role of an FI Vendor, providing key details about the vendor's general and accounting data. The general data includes the vendor's name, Antonio Rodriguez, their address at Vendor Path 7, 10123 Berlin, and their bank account information (partially redacted). The accounting data specifies two company codes: 1010 for Bike Company Germany and 1710 for Bike Company US.")

### Test your Knowledge

**Question:** How would you proceed if an existing supplier would now also become a customer of the bike company? Think about your answer before you read the answer below.

**Answer:** For this existing business partner record, simply maintain the customer role(s) for Sales (business partner role: **Customer**) and for Financial Accounting (business partner role: **Supplier**).

## How to Create a Supplier Business Partner

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_FA6B8CBD1A38F2B6)

## Vendor Invoice

In most cases, when making any purchase, the bike company in our example has a strict procurement policy that requires the procurement department to manage, or at least be made aware of, all purchases. 

In predefined, exceptional cases it is allowed to order office supplies without involving the procurement department. This is for example the case, when the office printer requires toner unexpectedly and we must purchase new cartridges from the office supply shop next to our office.  

The following graphic shows the financial accounting flow for a vendor invoice process, connecting General Ledger (FI) and Controlling (CO) modules.

![This image illustrates the financial accounting flow for a vendor invoice process, connecting General Ledger (FI) and Controlling (CO) modules. The process begins with an invoice for €1,000 for office supplies (e.g., printer cartridges) issued to Bike Company DE. The Accounts Payable Subledger records the transaction under Vendor T-BP00, with the amount posted to the reconciliation account (21000000* Payables Domestic) in the General Ledger. The expense is categorized under the Profit and Loss account (65100000 Office Supplies) and is further allocated to the Overhead Cost Controlling module, specifically to Cost Center 10101801, as primary costs](https://learning.sap.com/service/media/topic/b0513cba-ab58-4e8a-aca6-d8b3c00b5f4a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_Post%20Vendor.png "This image illustrates the financial accounting flow for a vendor invoice process, connecting General Ledger (FI) and Controlling (CO) modules. The process begins with an invoice for €1,000 for office supplies (e.g., printer cartridges) issued to Bike Company DE. The Accounts Payable Subledger records the transaction under Vendor T-BP00, with the amount posted to the reconciliation account (21000000* Payables Domestic) in the General Ledger. The expense is categorized under the Profit and Loss account (65100000 Office Supplies) and is further allocated to the Overhead Cost Controlling module, specifically to Cost Center 10101801, as primary costs")

The process begins with an invoice for €1,000 for office supplies (e.g., printer cartridges) issued to bike company DE. The Accounts Payable subledger records the transaction under Vendor T-BP00, with the amount posted to the reconciliation account (21000000* Payables Domestic) in the General Ledger. The expense is categorized under the Profit and Loss account (65100000 Office Supplies) and is further allocated to the Overhead Cost Controlling module, specifically to Cost Center 10101801, as primary costs.

Play the video to learn about the initial value flow when posting a vendor invoice directly in the Accounts Payable.

Hi, let me quickly explain how to post a

vendor invoice directly in the accounts payable.

Imagine the bike company has purchased office supplies

without involving the purchasing department. An incoming invoice

from a supplier needs to be posted in accounts payable.

For the sake of simplicity, we will ignore value-added tax.

The corresponding business partner with an FI vendor

business partner role has already been created in accounts

payable. When posting an incoming invoice, a credit amount

will be posted to the supplier account in the subledger.

Accounts in the accounts payable

subledger are always open item managed.

That means that each transaction is assigned a status.

The status for the supplier invoice is open

because it still must be paid when it is due.

In the open item management of the supplier

account, this is indicated by a red traffic light.

The balance sheet must show the total amount of supplier liabilities

in general ledger accounting. To keep the financial statement

balanced, the account's payable reconciliation account assigned to the

supplier is updated at the same time. In company code 1010, the

reconciliation account 21000000 is used for domestic payables. As with any

financial posting, an equivalent debit amount must also be posted.

The general ledger account used as offsetting account for

the supplier line item depends on the business transaction.

The debit amount in our example will be posted to

the expense account 651000000, office supplies.

In another case, when purchasing tangible assets, for example,

such as a photocopier, the asset with its corresponding

balance sheet account would be used as the offsetting account.

Since the office supplies general ledger account is defined

as a primary cost account by the general ledger account type,

the amount is posted to a cost center in overhead cost controlling.

## How to Post and Analyze a Vendor Invoice

You are now well prepared to see this business scenario in the system.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_EDC8E455C72824A3)

## Manual Outgoing Payments

Our bike company usually performs outgoing payments automatically by using the payment program on a weekly basis. Imagine that a vendor invoice is already paid by cash from the pretty cash. You need to clear now the open item created from the invoice posting by manually entering the cash payment made at the shop in the system.

The following graphic illustrates how to clear a vendor invoice and posting outgoing payments manually.

![This image illustrates the financial accounting process for recording and clearing a vendor invoice. It highlights the interaction between the General Ledger and the Accounts Payable Subledger, showing how accounts such as petty cash, payables domestic (reconciliation account), and the vendor's account are impacted during a cash payment transaction. The details of this process are described in the text that follows.](https://learning.sap.com/service/media/topic/abda6f70-4183-4b91-b0fb-cac571025ff0/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_Post%20Vendor2.png "This image illustrates the financial accounting process for recording and clearing a vendor invoice. It highlights the interaction between the General Ledger and the Accounts Payable Subledger, showing how accounts such as petty cash, payables domestic (reconciliation account), and the vendor's account are impacted during a cash payment transaction. The details of this process are described in the text that follows.")

**Scenario:** The invoice has already been paid. So the next step is to post this outgoing payment to Accounts Payable. In this test scenario, you post the payment manually to the system. When posting the payment, you choose the relevant invoice that is to be paid.

The payment amount will be posted on the debit side of the supplier account and Accounts Payable. The outgoing payment references the supplier invoice. Both line items will be marked as cleared. At the same time, the assigned payables reconciliation account in the General Ledger is also reduced. As with any financial accounting posting, an equivalent credit amount must also be posted.

In this cash payments scenario, we use the balance sheet account 10010000 Petty Cash.

## How to Post a Manual Outgoing Payment

The following system demonstration shows the manual clearing of a vendor invoice in Accounts Payable in connection with the value flow into the General Ledger.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_8F251574286CC68C:demo)

## Further Reading

- [Creating Supplier/Vendor Master Records: Overview | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/3cb1182b4a184bdd93f8d62e3f1f0741/7649d153c9684608e10000000a174cb4.html?version=2021.000)
    
- [Invoices and Credit Memos | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/3cb1182b4a184bdd93f8d62e3f1f0741/8bcfba538c95b54ce10000000a174cb4.html?version=2021.000)
    
- [Incoming and Outgoing Payments | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/3cb1182b4a184bdd93f8d62e3f1f0741/2c57d7531a4d424de10000000a174cb4.html?version=2021.000)

# Managing Accounts Receivable

Objective

After completing this lesson, you will be able to describe the tasks and structure of Accounts Receivable

## Introduction

In this lesson you learn more about the structure and basic tasks of **Accounts Receivable** accounting.

Note

The basic structures of Accounts Receivable are similar to those of Accounts Payable, so we recommend to work through the lesson about Accounts Payable before.

The Accounts Receivable is integrated with Sales. You will get more details when learning more about the Lead-to-Cash process.

The current process step is highlighted in the following overview.

![The image represents the Record-to-Report process in financial management, focusing specifically on the Master Data and Financial Transactions stages. The task Manage Accounts Receivable is highlighted, emphasizing its role in tracking customer payments and ensuring financial accuracy. Other stages in the process, such as Creditworthiness, Money, and Reporting, are shown but grayed out, indicating they are not the current focus.](https://learning.sap.com/service/media/topic/b4108a4d-ac7d-4865-9ad5-cc2bbd962813/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process3.png "The image represents the Record-to-Report process in financial management, focusing specifically on the Master Data and Financial Transactions stages. The task Manage Accounts Receivable is highlighted, emphasizing its role in tracking customer payments and ensuring financial accuracy. Other stages in the process, such as Creditworthiness, Money, and Reporting, are shown but grayed out, indicating they are not the current focus.")

Accounts Receivable in Financial Accounting (FI) records and manages the accounting data of each customer.

Because it is highly integrated with SAP S/4HANA Sales, customer invoices and credit notes from SAP S/4HANA Sales are automatically posted in Accounts Receivable. This is illustrated in the graphic below.

![This image demonstrates the relationship between Accounts Receivable and General Ledger Accounting. It shows how customer-specific accounts (e.g., Customer A and Customer B) in Accounts Receivable are linked to the General Ledger through balance sheet accounts and profit and loss accounts, such as expense and revenue.](https://learning.sap.com/service/media/topic/b4108a4d-ac7d-4865-9ad5-cc2bbd962813/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_AccountsRecieve.png "This image demonstrates the relationship between Accounts Receivable and General Ledger Accounting. It shows how customer-specific accounts (e.g., Customer A and Customer B) in Accounts Receivable are linked to the General Ledger through balance sheet accounts and profit and loss accounts, such as expense and revenue.")

Because many postings in Accounts Receivable Accounting are made automatically, the integration tests take place as part of the Lead-to-Cash processes. Regardless of this, it is interesting, to know how master data and open item management works.

## Business Partner: FI Customer

The master data of customers in accounts payable is also administered by the business partner in SAP S/4HANA. Its structure can easily be transferred from accounts payable.

If you want to create a business partner for accounts receivable, you must assign the business bartner role _FI Customer_ for this purpose. You can then create general master data and financial accounting data at company code level.

Because the general data is maintained at client level, it is automatically available to all company codes (and other SAP solutions). Therefore, there is no need to define that data separately in each company code.

Financial account data for accounts receivable that is specific to each company code is maintain in the company code views. This includes the following data:

- Reconciliation account
- Payment terms
- Dunning terms

If a business partner already exists in the SAP system, you can assign the business partner role _FI Customer_ and maintain the master data that is required.

The following graphic shows the role-related data of a business partner that is created as both a vendor and a customer in FI. Please note that the general data has to be provided for each business partner role.

![This image represents the Business Partner Role of an FI Customer, showcasing general data such as name, address, and bank account details, along with accounting data linked to specific company codes (e.g., Bike Company Germany and Bike Company US).](https://learning.sap.com/service/media/topic/b4f5b88f-217c-400a-a984-7fa63d065b93/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/BP%20FI%20Customer.png "This image represents the Business Partner Role of an FI Customer, showcasing general data such as name, address, and bank account details, along with accounting data linked to specific company codes (e.g., Bike Company Germany and Bike Company US).")

## How to Create a Customer Business Partner Master Record

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_9FCF1D9686CF1880)

## Accounts Receivable Value Flows

The following graphic illustrates an accounts receivable value flow. Read about the various step below.

- **Step 1: Create a business partner**
    
    You create a business partner for Accounts Receivable by choosing the business partner role FI customer. In the company code data a reconciliation account must be assigned for the integration with the General Ledger Accounting.
    
- **Step 2: Post an invoice**
    
    Customer invoices from SAP S/4HANA Sales will be automatically posted in Accounts Receivable. An open item is created on the corresponding business partner account. The assigned reconciliation account is automatically updated, too. As the general ledger must be balanced, the revenues are posted on a profit and loss account.
    
- **Step 3: Post a payment**
    
    You receive the invoice amount by bank transfer on your bank account from the customer. The payment is automatically posted on the corresponding customer account in Accounts Receivable. The reconciliation account in general ledger is automatically updated. Finally, the customer invoice and the payment are marked as _cleared_.
    

## Further Reading

- [Customer Master Data | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/a8aaa72cb39a48528b39b61623c15baa/5ae2bf5362ebb44ce10000000a174cb4.html?version=2021.002)
- [Accounts Receivable Accounting | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/3cb1182b4a184bdd93f8d62e3f1f0741/48170ad70c6c43bf87e8ce3351cb36c5.html?version=2021.002)

# Managing Asset Accounting

Objective

After completing this lesson, you will be able to manage asset accounting across the life cycle of a fixed asset

## Introduction

An asset is something your company owns that has value, like a building, a vehicle, or a machine. Managing asset accounting in SAP is, in simple terms, about keeping track of what your company owns and what those things are worth.

Examples:

- Recording new assets
- Calculating and recording depreciation (loss in value)
- Selling or retiring assets
- Generating reports on assets, their value, depreciation and more

The graphic shows where we are in the process.

![A process flow diagram illustrating the Record-to-Report process. The highlighted sections focus on the Master Data and Financial Transactions phases. In the Master Data phase, the task Manage asset accounting is emphasized, while the Financial Transactions phase includes tasks such as managing general ledger (G/L) accounting, accounts payable, and accounts receivable.](https://learning.sap.com/service/media/topic/ee9a56a9-db43-4aa3-8e30-ed3d8d5df6a1/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process4.png "A process flow diagram illustrating the Record-to-Report process. The highlighted sections focus on the Master Data and Financial Transactions phases. In the Master Data phase, the task Manage asset accounting is emphasized, while the Financial Transactions phase includes tasks such as managing general ledger (G/L) accounting, accounts payable, and accounts receivable.")

Asset accounting is crucial for the design-to-operate process, too. As it tracks the financial aspects of assets from acquisition to disposal, it is integral to the asset lifecycle management including planning, designing, building, operating, maintaining, or replacing assets.

In this lesson, we therefore discuss asset accounting in context of asset lifecycle management - partly jumping into to the production execution, more specifically into the shop floor processing in SAP S/4HANA .

## Asset Accounting

Asset Accounting (FI-AA) is used to manage and supervise fixed assets in the SAP System.

The central task of asset accounting is to provide the correct acquisition costs for each fixed asset (for example, a purchased laptop for the controlling department) or the cost of goods manufactured (for example, in the case of a self-produced machine) and to document and post the value changes through the life cycle of the asset.

Due to the integration of asset accounting with general ledger accounting, the individual asset values are displayed in aggregated form in the balance sheet and profit and loss statement of the enterprise.

Assets as a whole is made up of a variety of different types of assets. The balance sheet represents this variety using the following balance sheet items:

- Intangible assets
- Fixed assets
- Financial assets

The following graphic shows a sample breakdown of assets in the balance sheet and how they are categorized.

![The image highlights the classification of non-current assets within a company balance sheet and their categorization across three types: Intangible Assets, Fixed Assets, and Financial Assets. The chart on the right provides examples of how different asset types—such as property, machines, investments, securities, patents, and software—are categorized. For instance, Patents and Software fall under Intangible Assets, while Property and Machines are classified as Fixed Assets, and Investments and Securities are part of Financial Assets. Depreciation expenses related to these assets are recorded in the Profit and Loss Statement.](https://learning.sap.com/service/media/topic/d1eb52d8-c358-41e7-9735-000cd2224e0d/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Asset_Types.png "The image highlights the classification of non-current assets within a company balance sheet and their categorization across three types: Intangible Assets, Fixed Assets, and Financial Assets. The chart on the right provides examples of how different asset types—such as property, machines, investments, securities, patents, and software—are categorized. For instance, Patents and Software fall under Intangible Assets, while Property and Machines are classified as Fixed Assets, and Investments and Securities are part of Financial Assets. Depreciation expenses related to these assets are recorded in the Profit and Loss Statement.")

Note

Balance sheet items may differ according to accounting principles (for example, US GAAP and IFRS).

In SAP, Financial Assets (for example stocks or bonds) are managed using SAP Treasury and Risk Management.

[Financial Risk & Treasury Software | SAP Treasury and Risk Management](https://www.sap.com/products/financial-management/treasury-risk-management.html)

Typically, non-current asset items are usually subdivided into individual balance sheet items. The following is a sample breakdown of balance sheet item **fixed assets**:

1. Real estate
2. Plants and engines
3. Office equipment and other furniture
4. Down payments made on fixed assets

This detailed information is also used in the asset history sheet, as part of the annual financial reporting. The asset history sheet provides a more accurate insight of the changes in the value of fixed assets by displaying acquisitions, retirements, transfers, depreciation, and other transactions within the reporting period.

Note

The asset history sheet is also referred to as the notes to the financial statements.

## Basic Life Cycle of a Fixed Asset

The following graphic shows the basic life cycle of a fixed asset in Asset Accounting:

![The image depicts the basic fixed asset life cycle process, starting with the creation of an asset master record. This is followed by key stages of asset management, including asset acquisition (represented with an inflow of EUR), asset accounting (which includes depreciation tracking), and asset retirement (represented with an outflow of EUR). The asset life cycle reflects a continuous accounting process where fixed assets are tracked, depreciated, and eventually retired, ensuring proper financial management.](https://learning.sap.com/service/media/topic/bb4cc243-7153-42e9-b218-9d7600f14894/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_LifeCycle.png "The image depicts the basic fixed asset life cycle process, starting with the creation of an asset master record. This is followed by key stages of asset management, including asset acquisition (represented with an inflow of EUR), asset accounting (which includes depreciation tracking), and asset retirement (represented with an outflow of EUR). The asset life cycle reflects a continuous accounting process where fixed assets are tracked, depreciated, and eventually retired, ensuring proper financial management.")

1. **Create Asset Master Record:** To be able to manage values in the Asset Accounting for a fixed asset, an asset master record is needed. The asset master record consists of the following data areas:
    
    - **General Master Data:** This part of the master record contains concrete information about the fixed asset.
        
        Examples:
        
        - Description
        - Account assignment information, such as Cost Center
        - Posting information, such as activation date
        - Physical inventory data, such as last inventory date
        - Information on the origin of the asset, such as vendor and manufacturer
    - **Asset Value Data:** This part of the master record contains concrete information about the fixed asset.
        
        - Depreciation keys for controlling the valuation of the asset
        - Useful life
        - Expired useful life
        - Starting date of depreciation
        - Scrap value
2. **Asset Acquisitions:** The following are the methods of posting external acquisitions (acquisition of an asset from a business partner):
    
    - **In Asset Accounting:**
        - Without Accounts Payable integration: The assets are posted either before the invoice is received or after the invoice is posted by the Accounts Payable department in a separate step.
        - With Accounts Payable integration: The assets and the incoming invoices are posted in one step.
    - **In Procurement (with reference to a purchase order):** The assets are posted and activated in Asset Accounting during the Goods Receipt – Invoice Receipt process.
3. #### Depreciation:
    
    - **Ordinary depreciation** represents the planned depreciation of an asset when the asset is normally used. Ordinary depreciation reflects the deduction for wear and tear during the normal use of the asset.
    - **Unplanned depreciation** covers unusual influences that lead to a permanent decrease in the value of an asset. For example, damage of a production machine.
    - **Special depreciation** is a depreciation for wear and tear that is based solely on tax law. This type of depreciation allows you to depreciate a percentage of the asset value. The percentage rate can be scaled within a tax concession period, without taking into account the actual wear and tear of the asset.
        
4. **Asset Retirement:** As soon as an asset that is managed in Asset Accounting leaves the company, an asset retirement is posted in Asset Accounting. Depending on the business transaction, it can be posted in different ways:
    
    - **Retirement by Sale**
        
        - Without Accounts Receivable integration, against a clearing account
        - With Accounts Receivable integration
        
        Note
        
        In addition to adjusting the asset balance sheet values, the system automatically calculates and posts a gain or loss from the asset retirement. This applies for retirement by sale with or without Accounts Receivable integration.
        
    - **Retirement by Scrapping**: A retirement without revenue is the removal of an asset from the asset portfolio without any revenue, for example, by scrapping.
        

Note

When you use this posting option, the system does not create revenue and gain/loss postings. Instead, it creates a _Loss made on asset retirement without revenue_ posting in the amount of the net book value being retired.

## Fixed Asset Master Record

Imagine the following business scenario: The bike company in our example has decided to manufacture some components of a new e-bike model in-house. In this context, new machines have already been ordered for the production plant in Germany. For the new machines, fixed asset master data must be recorded.

Information in the asset master data has a significant impact on the correct recording of its values. For this reason, the creation of an asset master record must be tested in detail.

As highlighted in the following graphic, two objects in the fixed asset master record are of central importance when defining an asset account:

- Asset class
- Depreciation areas

![This image illustrates the Fixed Asset Master Record process tied to Company Code 1010. It starts with an asset classification, here represented as Asset Class: 3100 – Machines. The process flows into account determination to assign financial accounts associated with the asset. Following this, depreciation areas are defined, which include multiple regulatory requirements, such as Book Depreciation (Area 01), Local Tax (Area 15), and IFRS (Area 32). These depreciation postings are then reflected in the General Ledger Accounting system. The results of these entries impact both the Balance Sheet and Profit and Loss Statement, ensuring accurate financial reporting.](https://learning.sap.com/service/media/topic/af557795-bf18-47ae-b07a-36caf9702f1a/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_FixedAsset.png "This image illustrates the Fixed Asset Master Record process tied to Company Code 1010. It starts with an asset classification, here represented as Asset Class: 3100 – Machines. The process flows into account determination to assign financial accounts associated with the asset. Following this, depreciation areas are defined, which include multiple regulatory requirements, such as Book Depreciation (Area 01), Local Tax (Area 15), and IFRS (Area 32). These depreciation postings are then reflected in the General Ledger Accounting system. The results of these entries impact both the Balance Sheet and Profit and Loss Statement, ensuring accurate financial reporting.")

### Asset Class

The **Asset Class** is the main criterion when defining the asset. Each asset must be assigned to one asset class. There are two main purposes of an asset class:

- **Account determination:** The asset class is used to assign an account determination key to the asset master record. This account determination key provides all G/L accounts that a fixed asset requires for various posting transactions. This includes, for example, posting and displaying the acquisition cost or manufacture costs of an asset in the correct balance sheet item (for example, machines under balance sheet item II. Fixed Assets - 2. Plants and Engines) or expense accounts as part of the monthly depreciation postings.
    
- **Control parameters and default values:** The individual assets differ in terms of planned useful life and depreciation terms (for example, straight-line or declining-balance depreciation methods). The asset class provides control parameters and default values for the depreciation calculation in the asset master record. If necessary, these default values can be adjusted.

In addition to these two main purposes, the asset class is responsible for assigning the asset number and controlling the master data layout.

### Depreciation Areas

Assets need to be valuated differently depending on the purpose of the valuation (for example, commercial, tax, or group valuation). This can result in different acquisition values or depreciation values for the identical asset, for example, according to local GAAP and international GAAP.

These different valuation approaches are displayed using **depreciation areas** (and ledgers) in the asset master record. For this reason, the control parameters and default values (see Asset Class) for the depreciation calculation are always displayed at the level of the depreciation area of an asset.

Note

These different fixed assets valuation approaches are represented by valuation views in the settings of Asset Accounting. A valuation view is assigned to a depreciation area within a company code.

## How to Create an Asset Master Record

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_660C8047C3CE5DA5:demo)

## Integrated Asset Acquisition

Imagine the following situation: As part of the initial implementation, the bike company in our example wants to use the non-integrated asset acquisition and the integrated asset acquisition with accounts payable accounting. The non-integrated asset acquisition has already been tested successfully. The test of an integrated asset acquisition is still pending.

The graphic below shows the incoming invoice of the supplier and the various components of the integrated asset acquisition with accounts payable accounting.

![This image illustrates the process of integrated asset acquisition in SAP, starting with an invoice and its subsequent accounting entries. The invoice, issued by Bike Company DE to a business partner in Munich, details the purchase of a laser etching machine for €10,000, including VAT. The process flow diagram on the right shows two key steps: (1) Asset Accounting, where the laser etching machine is recorded as an asset worth €10,000, and (2) Reconciliation Account, which links the asset to general ledger accounting under Machinery/Equipment for €10,000. The accounts payable section records the payment obligation to the business partner for €10,000. Steps 1 and 2 will be explained in detail in the text that follows.](https://learning.sap.com/service/media/topic/f62fe913-a359-488e-b59d-b0c3029201fe/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IntAssAcqu.png "This image illustrates the process of integrated asset acquisition in SAP, starting with an invoice and its subsequent accounting entries. The invoice, issued by Bike Company DE to a business partner in Munich, details the purchase of a laser etching machine for €10,000, including VAT. The process flow diagram on the right shows two key steps: (1) Asset Accounting, where the laser etching machine is recorded as an asset worth €10,000, and (2) Reconciliation Account, which links the asset to general ledger accounting under Machinery/Equipment for €10,000. The accounts payable section records the payment obligation to the business partner for €10,000. Steps 1 and 2 will be explained in detail in the text that follows.")

As part of the integrated asset acquisition, the gross amount of the incoming invoice is posted as an open item in the terms of payment. The reconciliation account assigned in the vendor master record is also automatically updated in the general ledger. Once the invoice is due, Accounts Payable pays the amount to the vendor. This clears the open item.

1. **Asset capitalization:** The asset is capitalized in Asset Accounting with the net invoice amount. Effects:
    
    - The capitalization **date** is noted in the master record. It is used in conjunction with the depreciation key to determine the depreciation start of the asset.
    - The **vendor** is stored in the asset master record.
    - Planned **monthly depreciation amounts** are calculated and displayed.
2. The **account determination** in the asset master record is used to update the assigned **reconciliation account** in General Ledger Accounting. This ensures that the correct values are displayed on the asset side of the balance sheet.
    
    As part of the monthly closing operations, the planned depreciation is posted in Asset Accounting. A value adjustment account for the corresponding reconciliation account is used to adjust the balance sheet values by the depreciation amounts.
    
    The offsetting account of the depreciation postings is an expense account. Both accounts are also maintained in the account determination key of the asset master record.
    

Note

The posting logic and the structure of the journal entries is slightly more complex and extensive in SAP S/4HANA than in the interaction above. This is because it involves mapping multiple valuation approaches.

This course focuses on the interaction between Asset Accounting, General Ledger Accounting, and other sub-ledgers in general accounting. It does not cover the exact posting logic and the structure of the journal entries in SAP S/4HANA.

Further Reading:

- [External Asset Acquisitions | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/3e5fcf2c768746049b5627bd5a42f720/3cf74e52ecbacc71e10000000a44176d.html)
- [Example: Acquisition, Non-Integrated Posting | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/3e5fcf2c768746049b5627bd5a42f720/70de4c7e9e22452dba388a05e024505f.html)

## How to Post and Analyze an Asset Acquisition

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_57EAF298B8D208B4)

## SAP Intelligent Robotic Process Automation (SAP Intelligent RPA)

The bike company in our example handles a large number of asset acquisitions. They urgently need a way to automatically upload those asset acquisitions to be more efficient.

SAP offers the **SAP Intelligent Robotic Process Automation (SAP Intelligent RPA)** as part of the SAP Business Technology Platform to reduce the manual effort and time spent entering that data in SAP S/4HANA. SAP Intelligent RPA accelerates the digital transformation of business processes by automatically replicating repetitive tasks.

The purpose is all about making tasks more efficient: For example, during activity peaks, SAP Intelligent RPA can reduce the errors made by personnel who are under pressure to enter significant amounts of information in a short time frame.

Play the video to get introduced to the SAP Best Practice pre-built business content to automate asset acquisition postings.

This video focuses on Intelligent Robot Process Automation, IRPA.

While SAP Business AI is designed to provide advanced analytics

and predictive capabilities, leveraging artificial intelligence to

derive insights from data and make informed business decisions,

SAP IRPA is used to automate repetitive, rule-based tasks typically

carried out by humans. It aims to improve efficiency, reduce

errors and free up employees to focus on more strategic activities.

Listen to my colleague, Stefan, to learn more.

Large enterprises tend to acquire assets in enormous quantities

and subsequently need to post the acquisitions in asset

accounting. The larger the number of acquired assets, the more

tedious and time-consuming it becomes to post these acquisitions.

SAP provides the standard bot to get information on the

assets to be posted from a prepared Microsoft Excel file and

posts them automatically into the system. In this video, a

user has added several assets to be posted into the Excel

sheet. By mistake, two assets include incorrect information.

As a result, this acquisition posting runs into errors.

Using the Desktop Agent, the user first starts

the execution of the bot in simulation mode.

After the Excel table is selected, the bot automatically opens the SAP

Fiori app post-acquisition, not integrated, with automatic offset

account. each individual asset acquisition is simulated step by step at the

end of the process the bot reports the execution of the simulation with

two errors the user can easily review the results after the bot has

finished processing after correcting the two asset acquisitions with

errors in the Excel sheet the user starts the execution in an update run

SAP Intelligent RPA posts acquisitions by collecting asset information and transactional data from an Microsoft Excel file and processes them automatically via SAP Fiori. It collects and classifies success and error cases that occur during the process and updates the Microsoft Excel file with the results.

## Further Reading

- [Manage Fixed Assets | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/3e5fcf2c768746049b5627bd5a42f720/aec7ecb2ee11437bbbc2041572be9612.html)
- [Depreciation | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/3e5fcf2c768746049b5627bd5a42f720/df6cbd53e3acb64ce10000000a174cb4.html)
- [Retirement | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/3e5fcf2c768746049b5627bd5a42f720/a7886752458a712de10000000a44176d.html)

# Introducing Ledgers for Parallel Accounting

Objective

After completing this lesson, you will be able to explain the basic logic of the ledger solution within SAP S/4HANA

## Introduction

The bike company that we use as example creates its consolidated balance sheet in accordance with International Financial Accounting Standards (IFRS). In addition, each legal entity creates their individual financial statements based on the respective local accounting principle.

As a result, a business transaction (for example provisions posting or foreign currency valuations) may be valuated differently by two legal entities, depending on the applicable accounting principles.

This prompts the question: how can different valuation approaches be mapped within one general ledger?

This lesson explains the basic concept of the ledger solution within SAP S/4HANA. The graphic below highlights where this process step is located within the record-to-report process flow:

![The diagram provides an overview of the Record-to-Report process and highlights its main stages: Creditworthiness, Master Data, Financial Transactions, Money, and Reporting. The current focus is on the Financial Transactions stage, specifically the task Manage Financial Close, which is framed in yellow. This task ensures accurate and timely closure of financial records, a critical step before proceeding to the Reporting phase. The diagram also visually emphasizes the question, Where are we in the process? to help contextualize the workflow's progression.](https://learning.sap.com/service/media/topic/e11cec4b-61f5-4e30-a779-2a782186ef87/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process5.png "The diagram provides an overview of the Record-to-Report process and highlights its main stages: Creditworthiness, Master Data, Financial Transactions, Money, and Reporting. The current focus is on the Financial Transactions stage, specifically the task Manage Financial Close, which is framed in yellow. This task ensures accurate and timely closure of financial records, a critical step before proceeding to the Reporting phase. The diagram also visually emphasizes the question, Where are we in the process? to help contextualize the workflow's progression.")

In our example, the bike company Germany calculates, and post pension provisions based on IFRS and local accounting principles, as part of the closing operations at fiscal year end. The provision amounts for each accounting principle are different.

The ledger solution in SAP S/4HANA helps them to map these parallel accounting requirements.

## Ledger Solution

The ledger solution in SAP S/4HANA enables you to manage several general ledgers (in General Ledger Accounting) in parallel and create separate financial statements for each general ledger. Ledgers for parallel accounting are always managed as standard ledgers that contain a full set of configuration settings and full posting information.

Depending on the type of posting, you can post data to one ledger at a time or all to the available ledgers at once.

The following example shows the basic principle of a manual provision allocation/acquisition posting with different amounts in different ledgers:

![The image shows two cylindrical ledgers representing dual accounting systems: the 0L-Ledger for Local GAAP and the 2L-Ledger for IFRS. The 0L-Ledger records a provision of 3,000 in the balance sheet and an expense provision of 3,000 in the P&L account. The 2L-Ledger records a provision of 5,000 in the balance sheet and an expense provision of 5,000 in the P&L account. The differences between the two ledgers reflect adjustments for IFRS compliance.](https://learning.sap.com/service/media/topic/b2183cf5-a4a7-423f-97f2-878b31339eb2/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_0L2L_Ledger.png "The image shows two cylindrical ledgers representing dual accounting systems: the 0L-Ledger for Local GAAP and the 2L-Ledger for IFRS. The 0L-Ledger records a provision of 3,000 in the balance sheet and an expense provision of 3,000 in the P&L account. The 2L-Ledger records a provision of 5,000 in the balance sheet and an expense provision of 5,000 in the P&L account. The differences between the two ledgers reflect adjustments for IFRS compliance.")

- In this example, pension provisions are calculated according to local GAAP (resulting in EUR 3,000) and according to international financial reporting standards (resulting in EUR 5,000).
    
- The postings of these two valuation approaches must be made in separate G/L journal entries. While the G/L accounts used are identical, two separate journal entries are needed as the ledger is a document header level element (Field= Ledger-Group).
    

This enables you to create separate evaluations for each ledger (for example, a balance sheet, income statement, or trial balance).

Note

SAP S/4HANA Cloud provides you with different accounting principles and ledgers to use for parallel accounting. For more information, see: [Accounting Principles | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6b39bd1d0e5e4099a5b65d835c29c696/50f1192d60274ed29eb0985bf46086df.html)

## How to Create a Ledger-Specific Posting

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_446A57F8B174D6AF:demo)

## Further Reading

[Parallel Accounting | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6b39bd1d0e5e4099a5b65d835c29c696/fce0d25320cd4608e10000000a174cb4.html)


# Processing Plan and Actual Data in Overhead Cost Controlling

Objective

After completing this lesson, you will be able to manage cost centers, secondary cost accounts and work breakdown structure elements (WBS elements)

## Introduction: Primary Cost Posting

Welcome to the area of controlling. In this lesson we define the scope of **Overhead Cost Controlling.** The following graphic provides a simplified view which SAP solution is covered in this lesson.

![This image provides an overview of the SAP solution landscape, focusing on the context of Management Accounting (CO). The diagram highlights the position of Management Accounting within the SAP S/4HANA system, which is part of the broader SAP ecosystem. SAP S/4HANA is shown as a core component, with modules such as FI (Financial Accounting), MM (Materials Management), PP (Production Planning), and others. Management Accounting (CO) is specifically emphasized within the SAP S/4HANA framework. Above SAP S/4HANA, the diagram includes other SAP solutions like SAP Analytics Cloud, SAP SuccessFactors, SAP Ariba, and others, all connected through the SAP Business Technology Platform.](https://learning.sap.com/service/media/topic/da1e6b9a-b40d-423c-902e-10ac9af00223/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/SAP_Sol_Orientation_2.png "This image provides an overview of the SAP solution landscape, focusing on the context of Management Accounting (CO). The diagram highlights the position of Management Accounting within the SAP S/4HANA system, which is part of the broader SAP ecosystem. SAP S/4HANA is shown as a core component, with modules such as FI (Financial Accounting), MM (Materials Management), PP (Production Planning), and others. Management Accounting (CO) is specifically emphasized within the SAP S/4HANA framework. Above SAP S/4HANA, the diagram includes other SAP solutions like SAP Analytics Cloud, SAP SuccessFactors, SAP Ariba, and others, all connected through the SAP Business Technology Platform.")

In this lesson, you get introduced to the cost assignment objects that are used to collect overhead costs (cost center and WBS element) and learn how they are maintained in the system. Furthermore, you explore selected planning options in overhead cost controlling. Finally, you look at how actual values are posted on cost centers and WBS elements.

The next graphic illustrates where the process steps we discuss are located in the overall **Record-to-Report** process flow.

![This image provides an overview of the Record-to-Report process, highlighting the current focus on the Manage primary cost posting step within the Financial Transactions phase. The process is depicted as a timeline, starting with Product Cost Calculation, progressing through Master Data and Financial Transactions, and concluding with Reporting. The highlighted step, Manage primary cost posting, is part of the Financial Transactions phase, which involves recording and managing financial data. This step is critical for ensuring accurate cost allocation and financial reporting.](https://learning.sap.com/service/media/topic/da1e6b9a-b40d-423c-902e-10ac9af00223/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process6_CO.png "This image provides an overview of the Record-to-Report process, highlighting the current focus on the Manage primary cost posting step within the Financial Transactions phase. The process is depicted as a timeline, starting with Product Cost Calculation, progressing through Master Data and Financial Transactions, and concluding with Reporting. The highlighted step, Manage primary cost posting, is part of the Financial Transactions phase, which involves recording and managing financial data. This step is critical for ensuring accurate cost allocation and financial reporting.")

### Overhead Cost Controlling: Examples

Imagine the following situation:

In the bike company, you have costs that arise as a direct consequence of producing a single bike, for purchasing bike components and labor costs in the production line. However, in addition to these direct product costs, there are costs that arise from the normal operation of our business: Labor costs for business departments (for example, finance and marketing departments), energy and telecommunication costs, and costs associated with running the employee canteen.

Overhead Cost Controlling in SAP S/4HANA provides structures, master records, and processes that help to plan, track, assign, allocate, and analyze these costs.

Play the video to get some examples of processes performed in Overhead Cost Controlling.

In overhead,

cost controlling costs are allocated

to the areas which generate the costs.

First, primary costs which come from other modules

are assigned to different assignment objects.

A cost centre is typically used to collect overhead

costs such as canteen costs, energy and IT costs.

A work breakdown structure is another option. It is

an assignment object related to a project. It collects

all costs that arise during a certain project.

You're planning a trade fair for the event.

You need marketing brochures.

All costs for designing and printing the

brochures are assigned to the WBS element.

Every month, costs are allocated to

the cost drivers who cause the costs.

For this purpose,

different types of allocations can be used.

First example, assessment. Employees from finance

and sales consulting use the canteen regularly.

The arising canteen costs are collected

monthly by a canteen cost centre.

At the end of the period, the costs are assessed

from the canteen cost centre to the causing cost

centres, which are finance and sales consulting.

Second example, activity allocation.

Our consultant supports our marketing project.

In total, he worked five hours to support the project.

The labour costs have to be charged. Activity allocation

sends the costs from his cost centre to the project, or more

precisely, to a WBS element which collects the project costs.

The bike company in our example uses product cost controlling.

Overhead costs are allocated to the products you

make in order to calculate the production costs.

As a result, all overhead cost assignment objects

should be fully credited at the end of each period,

bringing their balance to zero settlement of variances.

When overhead cost assignment objects can be credited fully to

products, any remaining balances are settled to margin analysis.

### Test Your Knowledge

Think about the question below and try to find an answer before you continue.

**Question:** Which master record settings are required so that the values on an expense account used in Financial Accounting are also posted in Controlling? Select the card to flip it and see if you were right.

**Answer:** The expense account must be defined as Primary Cost or Revenue account in General Ledger Accounting.

## Cost Center Master Data

It is extremely important for the bike company to be able to display the costs for each area of responsibility in a transparent manner. For this reason, they test the structure of the **cost center master data** as part of the integration tests.

In SAP S/4HANA, cost centers define areas of responsibility within the company that collect overhead costs. Typical cost centers of this category are the Finance, Sales, Procurement, and Marketing departments.

Cost centers are often hierarchical structures, especially in larger companies. For example, the Finance department might be split into Accounting, Controlling, Treasury, and Receivables. This hierarchical relation is depicted in the system in a tree structured hierarchy, the Cost Center Hierarchy.

In addition to cost centers that depict departments, you can create cost centers for special purposes that aren't mapped to a specific department. These are used to gather costs that will later be allocated to other cost centers, for example a cost center for the canteen or for energy.

These cost centers must also be assigned to the cost center hierarchy.

![This image depicts a standard organizational hierarchy structure (A001) in SAP, showing the relationship between company codes, cost centers, and sub-cost centers. At the top level is the standard hierarchy (A001), which branches into two company codes: H1010 (Company Code 1010) and H1710 (Company Code 1710). Under H1010, there are multiple cost centers, including Services (H10111), Fleet of Cars (H10110), Training (H10109), Admin & Finance (H10101), and Marketing & Sales (H10102). The Services cost center (H10111) is further divided into sub-cost centers: IT Services (1011101) and Canteen (1011102). This hierarchy illustrates how cost centers and sub-cost centers are organized within a company code.](https://learning.sap.com/service/media/topic/cc3e985b-71c7-4d8c-af47-e118b0a1e477/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_CostCHierarchy.png "This image depicts a standard organizational hierarchy structure (A001) in SAP, showing the relationship between company codes, cost centers, and sub-cost centers. At the top level is the standard hierarchy (A001), which branches into two company codes: H1010 (Company Code 1010) and H1710 (Company Code 1710). Under H1010, there are multiple cost centers, including Services (H10111), Fleet of Cars (H10110), Training (H10109), Admin & Finance (H10101), and Marketing & Sales (H10102). The Services cost center (H10111) is further divided into sub-cost centers: IT Services (1011101) and Canteen (1011102). This hierarchy illustrates how cost centers and sub-cost centers are organized within a company code.")

Before you can create cost centers, you must define a Cost Center Hierarchy. This hierarchy is a tree structure that consists of different cost center groups (hierarchy nodes). Every cost center created is assigned to a specific hierarchy node. Postings cannot be made to the hierarchy nodes themselves. They are used as a summary level in reporting or to select a group of cost centers for planning or special reporting purposes.

## How to Display Cost Center Master Data

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_418640EC1907A2A7:demo)

## Secondary Cost Accounts

Secondary cost accounts are relevant when defining G/L accounts in Financial Accounting. We now take a closer look on the tasks associated with these accounts.

![This image explains the integration between Financial Accounting (FI) and Controlling (CO) in SAP, focusing on the categorization of General Ledger (G/L) accounts and their relevance to cost and revenue management. The G/L accounts are grouped into three main categories: Secondary Costs, Profit and Loss Accounts, and Balance Sheet Accounts. Secondary Costs (specific to CO) are used for internal cost allocations and are managed through Cost Element Accounting. Profit and Loss Accounts include Primary Costs or Revenue and Non-Operating Expense or Income, with Primary Costs and Revenue being CO-relevant. Balance Sheet Accounts, including Cash Accounts, are not CO-relevant. The diagram highlights how FI data flows into CO for cost and revenue tracking.](https://learning.sap.com/service/media/topic/d723196a-329e-4960-955e-5dfc24b7fcf1/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U3_L6_Cost_El_Accts.png "This image explains the integration between Financial Accounting (FI) and Controlling (CO) in SAP, focusing on the categorization of General Ledger (G/L) accounts and their relevance to cost and revenue management. The G/L accounts are grouped into three main categories: Secondary Costs, Profit and Loss Accounts, and Balance Sheet Accounts. Secondary Costs (specific to CO) are used for internal cost allocations and are managed through Cost Element Accounting. Profit and Loss Accounts include Primary Costs or Revenue and Non-Operating Expense or Income, with Primary Costs and Revenue being CO-relevant. Balance Sheet Accounts, including Cash Accounts, are not CO-relevant. The diagram highlights how FI data flows into CO for cost and revenue tracking.")

Secondary cost elements are only posted in Management Accounting (CO). They are used for certain internal allocations, such as assessments or settlements.

For secondary cost elements, G/L accounts are managed in FI with the _Secondary Costs_ G/L account type.

## Check Controlling Settings of Cost G/L Accounts

## Activity Types

When a cost center provides activities for other cost centers or Work Breakdown Structure elements (WBS elements), the resources of that cost center are used. The cost of this must be allocated to the receivers of the activity. Activity types are used as tracing factors for this cost allocation.

**The activity type classifies activities that are performed within a company by one or several cost centers.**

Typical Activity Types are:

- Machine Hours
- Personnel Hours
- Repair Hours
- Service Hours
- Internal Consulting Hours

To enable internal activity allocation, for each activity type, you must specify the cost center providing the activity and the price of the activity. You do this in the SAP S/4HANA system by planning the activity output/prices for a cost center.

![This image outlines the two-step process for managing activity types and their pricing in SAP Controlling (CO). Step 1 involves creating an activity type, such as Repair Hours, and defining its default values. These include the Price Indicator, which determines whether the system calculates the price for a cost center or if it is set manually, and the Allocation Cost Element, a secondary cost element used for CO allocation postings. Step 2 focuses on planning the price for the activity type, linking it to a specific cost center. Prices can be defined as fixed or variable. Steps 1 and 2 will be further explained in the accompanying text.](https://learning.sap.com/service/media/topic/d0a8a93e-d3f4-40c9-873a-f075ac3d789c/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/U3_L7_AT.png "This image outlines the two-step process for managing activity types and their pricing in SAP Controlling (CO). Step 1 involves creating an activity type, such as Repair Hours, and defining its default values. These include the Price Indicator, which determines whether the system calculates the price for a cost center or if it is set manually, and the Allocation Cost Element, a secondary cost element used for CO allocation postings. Step 2 focuses on planning the price for the activity type, linking it to a specific cost center. Prices can be defined as fixed or variable. Steps 1 and 2 will be further explained in the accompanying text.")

## How to Display an Activity Type

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_70AE2642426B9AA9:demo)

## Introduction: Cost Planning

With cost planning, we now jump to another step in the record-to-report process. The process step is highlighted in the graphic below.

![This image provides an overview of the Record-to-Report process, highlighting the current focus on the Planning overhead costs step within the Master Data phase. The process is depicted as a timeline, starting with Product Cost Calculation, progressing through Master Data and Financial Transactions, and concluding with Reporting. The highlighted step, Planning overhead costs, involves defining and allocating overhead costs to ensure accurate cost management and reporting. This step is a critical part of the Master Data phase, laying the foundation for subsequent financial transactions.](https://learning.sap.com/service/media/topic/d1ce10ab-b274-4388-81ca-cfc9addb6f46/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process7_CO.png "This image provides an overview of the Record-to-Report process, highlighting the current focus on the Planning overhead costs step within the Master Data phase. The process is depicted as a timeline, starting with Product Cost Calculation, progressing through Master Data and Financial Transactions, and concluding with Reporting. The highlighted step, Planning overhead costs, involves defining and allocating overhead costs to ensure accurate cost management and reporting. This step is a critical part of the Master Data phase, laying the foundation for subsequent financial transactions.")

Why does the bike company in our example need to plan their overhead costs?

To continuously monitor their company's financial objectives, the bike company must plan their costs and revenues accurately. This planning provides a baseline measurement against which they can compare actual operating results. This makes it easier to analyze and control business operations to achieve the desired results.

### Planning Cycle

The extent and method of planning can vary greatly from one enterprise to another. The following graphic provides a basic **planning cycle** of a company.

![This image illustrates the integration of planning processes across Sales, Production, and Controlling in SAP. It shows how sales planning feeds into sales and operations planning in production, which then leads to production planning to align manufacturing activities with sales forecasts. In the controlling process, cost center and activity type data are used to calculate material cost estimates, providing cost insights for production and sales. The process concludes with profit planning, ensuring alignment between costs, production, and profitability.](https://learning.sap.com/service/media/topic/d1ce10ab-b274-4388-81ca-cfc9addb6f46/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Planning%20Cycel.png "This image illustrates the integration of planning processes across Sales, Production, and Controlling in SAP. It shows how sales planning feeds into sales and operations planning in production, which then leads to production planning to align manufacturing activities with sales forecasts. In the controlling process, cost center and activity type data are used to calculate material cost estimates, providing cost insights for production and sales. The process concludes with profit planning, ensuring alignment between costs, production, and profitability.")

- **Sales Planning:** The integrated planning cycle begins with sales planning. It establishes the quantities of products or product groups to be sold. Sales plans are created by the Sales Department.
    
    Example of the result of sales planning: In the following year, the bike company wants to sell 10,000 units of the I-F3000 bike in the e-bikes product group in the EMEA region.
    
    The consolidated sales plan is transferred to Sales & Operations Planning (SOP).
    
- **Sales and Operations Planning:** Sales & Operations Planning determines the planned, future production demands to be covered by subsequent production planning.
    
    Example: There are already 2,000 units of the e-bike I-F3000 in stock. The remaining quantity of 8,000 units will be forwarded to Production Planning (PP) as planned, future production demands.
    
- **Production Planning:** Production planning creates plan orders for production to cover the future production demands from Sales & Operations Planning.
    
    Example: For the remaining quantity, a plan order in production of 8,000 units is now generated. The required machine and labor capacities (Activity Input Quantities) are also calculated in production planning. For example, to produce the remaining 8,000 e-bikes, the following is required:
    
    - 2,700 Personnel Hours - Production
    - 1,300 Machine Hours – Production
- **Cost Center and Activity Type:** Some costs are not planned directly in Cost Center Accounting. Instead, they are transferred from other areas, such as personnel planning from SAP Human Experience Management or planned depreciations from Asset Accounting.
    
    The planned costs and activity quantities are then used to calculate the activity prices. Prices are used to valuate internal activities during the period, before actual costs are known.
    
    Example of a price planning for activity types (simplified):
    
    - Total costs of personnel in the Production cost center: EUR 1,000,000 / period
    - Total activity of the Production cost center in hours: 20,000 H / period
    - Price for the Personnel Hours Activity Type € 50/Hour
- **Material Cost Estimate:** Material Cost Estimate calculates the costs of products. The most important cost items are the activity costs (for example, personnel hours or machine hours) and material costs. The material cost estimate includes the non order-related cost of goods manufactured and cost of goods sold for each unit.
    
    What is the difference between the cost of goods manufactured and cost of goods sold?
    
    - Material Costs + Production Costs = **Cost of Goods Manufactured**
    - Material Costs + Production Costs + Sales Costs and Administrative Overhead Costs = **Cost of Goods Sold**
    
    This cost of goods manufactured or costs of goods sold will be transferred to profit planning.
    
- **Profit Planning:** You calculate the revenues, sales deductions, and costs based on the planned sales quantities. Profit planning enables you to plan sales, revenue, and profitability data for any profitability segments. This means that the complete planning process for an enterprise can be mapped in accordance with its business requirements.
    
    If the target margin, for example, is not met after profit planning, the planning cycle can be restarted to make appropriate adjustments.
    

## Planning in Overhead Cost Controlling

Cost managers must have an efficient way to compare planned and actual costs (including costs incurred by cost centers outside Management Accounting) and track all cost and activity allocations that take place in the period-end closing process.

You can plan the cost flows of a cost center so that all overhead costs are covered through cost or activity type allocations.

When you have finished planning activity types, you can plan the primary costs associated with those activities. Activity-dependent primary costs are divided into fixed costs and variable costs. Variable costs are relative to the quantity of the planned activity.

The following video shows a simplified example of how the Bike Company plans activity-dependent primary costs for a production cost center:

![A diagram illustrating the cost structure of a production cost center. It includes two activity types: Machine Hours (1000 hours) and Personnel Hours (1200 hours). The cost breakdown is shown in a table with primary cost elements, fixed costs, and variable costs. Direct labor costs (61103000) are entirely variable at €30,000, while auxiliary labor costs (61104000) are entirely fixed at €24,000. Labor hours are calculated as €20/hour for fixed costs and €25/hour for variable costs.](https://learning.sap.com/service/media/topic/ca677cd1-db1c-4e6f-bef6-3e2d5c9c5554/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_PlanningActivity.png "A diagram illustrating the cost structure of a production cost center. It includes two activity types: Machine Hours (1000 hours) and Personnel Hours (1200 hours). The cost breakdown is shown in a table with primary cost elements, fixed costs, and variable costs. Direct labor costs (61103000) are entirely variable at €30,000, while auxiliary labor costs (61104000) are entirely fixed at €24,000. Labor hours are calculated as €20/hour for fixed costs and €25/hour for variable costs.")

## Planning Secondary Costs

In addition to the primary costs, a cost center often incurs secondary costs because it must use services (activity input) from other cost centers.

To calculate the planned secondary costs, the SAP system multiplies the price of the activity type (from the sender cost center) with the activity quantity that is consumed by the receiver cost center.

![: A diagram showing the cost allocation for the Maintenance cost center, focusing on repair hours. The activity type Repair hours has a planned quantity of 100 hours, which matches the scheduled quantity of 100 hours. The fixed price per hour is €30, and the variable price per hour is €50. The total planned cost is calculated as €80 per hour (fixed + variable) multiplied by 100 hours, resulting in €8,000. The Sender Cost Center is Maintenance, with the sender activity type being repair hours, input quantity of 100 hours, and planned costs of €8,000.](https://learning.sap.com/service/media/topic/d526d234-3e0b-4d89-8167-71bf74866a9b/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_SecondaryCosts.png ": A diagram showing the cost allocation for the Maintenance cost center, focusing on repair hours. The activity type Repair hours has a planned quantity of 100 hours, which matches the scheduled quantity of 100 hours. The fixed price per hour is €30, and the variable price per hour is €50. The total planned cost is calculated as €80 per hour (fixed + variable) multiplied by 100 hours, resulting in €8,000. The Sender Cost Center is Maintenance, with the sender activity type being repair hours, input quantity of 100 hours, and planned costs of €8,000.")

## Cost Center Planning with SAP Analytics Cloud

**SAP Analytics Cloud** is an analytics and planning solution that can be integrated with SAP S/4HANA or deployed as a single, cloud-based solution. SAP Analytics Cloud includes planning, reporting, and analytics capabilities in one product.

It can connect data from internal and external sources and create visualizations of that data in the SAP Analytics Cloud.

The bike company in our example uses SAP Analytics Cloud to perform overhead cost planning.

![A conceptual diagram showcasing the key functionalities of SAP Analytics Cloud, divided into four main areas: Business Intelligence, Planning, Predictive, and Analytics Designer. Business Intelligence focuses on data preparation, enterprise reporting, data visualization, and storytelling. Planning emphasizes sharing and simulation capabilities. Predictive highlights forecasting and automated insights, while Analytics Designer enables the creation of custom apps and SDK extensions. These components collectively illustrate the comprehensive capabilities of SAP Analytics Cloud.](https://learning.sap.com/service/media/topic/db7e44b1-5de9-4b46-b86d-880d6ac62919/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_APPRO.png "A conceptual diagram showcasing the key functionalities of SAP Analytics Cloud, divided into four main areas: Business Intelligence, Planning, Predictive, and Analytics Designer. Business Intelligence focuses on data preparation, enterprise reporting, data visualization, and storytelling. Planning emphasizes sharing and simulation capabilities. Predictive highlights forecasting and automated insights, while Analytics Designer enables the creation of custom apps and SDK extensions. These components collectively illustrate the comprehensive capabilities of SAP Analytics Cloud.")

The following video introduces the concept of cost center planning using the SAP Analytics Cloud (detached from the Bike Company business scenario).

In the following video, you learn how to manage

cost center planning with SAP Analytics Cloud.

Financial planning in SAP Analytics Cloud helps you plan

your company's future activities in specific periods.

You can use the plan and actual comparison to

monitor efficiency at the end of each period.

Comparing the actual operating results to the

plan data helps you identify deviations and take

corrective measures in your business operations.

SAP provides predefined integrated financial planning processes for

SAP Analytics Cloud such as sales and profitability planning product

cost planning and cost center planning in this video let's have

a look at the cost center planning process once I've decided to

produce a cake for example I have to think about the costs and also

where it is that I need to allocate those costs I I have certain

production costs like utilities, personnel, and communication, and

depending on the size of my venture, I'm going to have different teams

or areas that are part of the production process. So let's simplify

our example and just break that down to team one and team two.

I'll need to allocate the cost to these two teams based on

the role they're playing in the production process, and

to do that, I need to consider exactly what the costs are.

Now, to allocate this expense, I could use a distribution factor, like

U square meterage or the number of employees per team. This is just

one example of allocating overall costs based on a statistical key

figure, but of course we could do this for all of our incurred costs.

I can also further structure my costs according to whether they're

fixed or whether they're variable, like my communications costs.

This makes my overall costing more transparent. And from

here, I can determine my activity cost rates as long

as I also know the respective activity quantities, such

as the total number of hours I need to run my equipment.

The activity cost rate is simply the

cost divided by the activity quantity.

And so, at this point, I've essentially drawn up a cost center plan.

This plan includes the cost planning as well as the allocation based

on my two teams and their respective contributions to the production

process and their costs incurred during that process. My costs are

differentiated by whether they're fixed or variable and by the activity

type. So now, with our activities costed out and knowing the quantity

of each activity, we can calculate our cost rates. this diagram

provides an overview of the cost and activity planning process if I

want to look more closely at the details here I can see for example

additional options for determining activity quantities I can also see

how my plan fits with other plans like how we can use planned resource

requirements from the product cost plan as an additional source of

activity quantities or how our determined cost rates can be used in

product cost planning or how to allocate or distribute non-product

related costs that need to be taken up in the financial statement planning

and this is just a simple example of how this cost center planning

process works but you can imagine the other ways in which this

process can help you plan more efficiently and thus help you run simple

## Introduction: Actual Posting

After looking at the basic features of planning in Overhead Cost Controlling, let's go over a couple actual posting processes in controlling:

- Direct Activity Allocation
- Postings using WBS Elements

The relevant business process steps are highlighted in the graphic below.

![A process overview diagram for the Record-to-Report workflow, highlighting the current stage in the process. The timeline includes key phases: Product Cost Calculation, Master Data, Financial Transactions, and Reporting. The focus is on the Master Data and Financial Transactions stages, with specific tasks such as Direct activity allocation and Post actuals emphasized in yellow. The diagram provides a visual representation of progress within the overall process, helping to identify the current step.](https://learning.sap.com/service/media/topic/bab0f320-80f0-40f9-8371-908179eb0fc4/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/Record%20to%20Report%20Process8_CO.png "A process overview diagram for the Record-to-Report workflow, highlighting the current stage in the process. The timeline includes key phases: Product Cost Calculation, Master Data, Financial Transactions, and Reporting. The focus is on the Master Data and Financial Transactions stages, with specific tasks such as Direct activity allocation and Post actuals emphasized in yellow. The diagram provides a visual representation of progress within the overall process, helping to identify the current step.")

## Direct Activity Allocation

During the normal business activity, costs are charged to various cost centers. These costs are usually indicated in an invoice that a supplier sends for a product or service provided. The invoice for common expenses such as utility bills, is posted in FI directly.

Account assignment to cost centers is also possible in FI. In this lesson, we focus on cost flows within Controlling.

In direct activity allocation, you enter the cost center that provides the activity (sender cost center), the object that receives the activity (receiver cost object), the type of activity provided (activity type), and the activity quantity.

The sender cost center is credited, and the receiver cost object is debited using a secondary G/L account.

The value of the activity allocation is calculated by multiplying the activity quantity provided by the planned price of the period.

![A diagram illustrating the process of activity allocation between a sender cost center and receiver cost objects. The sender cost center, labeled Cost Center for Internal Services, allocates activities to three receiver cost objects: Cost Center for Production (10 hours), Cost Center for Customer Service (3 hours), and Projects (5 hours). The flow of activities is represented by arrows, showing the distribution of hours from the sender to the respective receivers. This visual demonstrates how internal services are allocated to different cost objects.](https://learning.sap.com/service/media/topic/a8cb7bb6-63d8-4586-8ff5-9281991212b6/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_ActivityAllocation.png "A diagram illustrating the process of activity allocation between a sender cost center and receiver cost objects. The sender cost center, labeled Cost Center for Internal Services, allocates activities to three receiver cost objects: Cost Center for Production (10 hours), Cost Center for Customer Service (3 hours), and Projects (5 hours). The flow of activities is represented by arrows, showing the distribution of hours from the sender to the respective receivers. This visual demonstrates how internal services are allocated to different cost objects.")

## How to Enter and Analyze a Direct Activity Allocation

The Internal Services cost center performs activities for other cost centers as part of repair measures. The cost of this internal activity depends on the number of units of the executed activity quantity.

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_E38DB936BA7A73A0)

## Project and WBS Elements

In addition to analyzing costs at a departmental level using cost centers, it is often useful to be able to track the costs for projects. Projects are business undertakings that have a specific goal and finite time line.

In SAP S/4HANA, you manage projects using Work Breakdown Structure (WBS) Elements. WBS Elements are an integral part of the complete project system functionality with a lot of possibilities and complexity. However, their simplest form, the WBS Element can act as a "bucket" that you fill with costs and revenues. This is done by assigning the WBS element in the journal entries when posting purchasing, sales, and financial documents.

![This image depicts a Work Breakdown Structure (WBS) for a project titled M-1000 Trade Fair. It organizes the project into five main phases: Rough Planning, Fine Planning, Final Preparation, Execution, and Debriefing. Each phase is further divided into sub-tasks, such as Choose Location and Set Up Project Team under Rough Planning, and Set Up Agenda and Gap Analysis under Fine Planning. The diagram visually represents the hierarchical structure of tasks, with placeholders for additional details in the Execution and Debriefing phases.](https://learning.sap.com/service/media/topic/de36f380-a3bb-44d0-917d-73396d37d057/IEE2E_2508_en-US_media/IEE2E_2508_en-US_images/IEE2E_Unit4_WBS.png "This image depicts a Work Breakdown Structure (WBS) for a project titled M-1000 Trade Fair. It organizes the project into five main phases: Rough Planning, Fine Planning, Final Preparation, Execution, and Debriefing. Each phase is further divided into sub-tasks, such as Choose Location and Set Up Project Team under Rough Planning, and Set Up Agenda and Gap Analysis under Fine Planning. The diagram visually represents the hierarchical structure of tasks, with placeholders for additional details in the Execution and Debriefing phases.")

In the figure Project and WBS Elements, a trade fair project is displayed as a work breakdown structure. A WBS shows the required project activities in a hierarchical form. All activities are maintained as WBS elements, which can be subdivided.

The _Rough Planning_ activity can for example include _Choose Location_, _Set Up Structure_, and_Set Up Project Team_. Each of these WBS elements can carry a different type of data, such as costs, revenues or a budget (depending on their settings).

**Business Example:** The bike company in Germany in our example participates in several trade fairs in Germany. To get a precise overview of the costs of each individual trade fair, the respective costs are entered in a WBS element for each trade fair. For test purposes, a Project with a single WBS element has already been defined in the system to post actual costs on this cost object. At the end of a trade fair, 50% each of the costs will be borne by the Sales and Marketing cost center.

Watch the following demo how this is managed by WBS elements.

## How to Manage WBS Elements

Demo[Start Demo](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=slide!SL_D82D9D9753C86DB2)

## Further Reading

- [Cost Center Accounting](https://help.sap.com/docs/SAP_ERP_SPV/9afb6f90c86748ef9f2b17c7d857f9b3/d795cf52fafdc066e10000000a441470.html?version=6.00.31)
- [Master Data in Cost Center Accounting](https://help.sap.com/docs/SAP_ERP_SPV/9afb6f90c86748ef9f2b17c7d857f9b3/6b41f45155a4315ee10000000a423f68.html?version=6.00.31)
- [Manual Actual Postings](https://help.sap.com/docs/SAP_ERP_SPV/9afb6f90c86748ef9f2b17c7d857f9b3/647ad153da7e4308e10000000a174cb4.html?version=6.00.31)
- [What is a Work Breakdown Structure?](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/4dd8cb7b1c484b4b93af84d00f60fdb8/26d4b65334e6b54ce10000000a174cb4.html?version=2021.001)
- [Period-End Closing](https://help.sap.com/docs/SAP_ERP_SPV/9afb6f90c86748ef9f2b17c7d857f9b3/ed0cd553088f4308e10000000a174cb4.html?version=6.00.31)

------- ADDITIONAL QUIZ QUESTIONS -------

NOTE: "The following are all the questions for this specific module. Below each number, there are instructions/questions and a list of answers. (X) denote correct answers. Brackets ("[]") denote additional comments for that specific question.

1.
In SAP S/4HANA, how many general ledgers can you manage in parallel?
Choose the correct answer.

One

Two

(X) Several

None

2.
Which of the following enterprise structures do you think are necessary for Financial Accounting in a bike company and why?
There are two correct answers.

Operating Concern

(X) Company Code

Valuation Level

(X) Segment

[The company code and the segment are required for Financial Accounting. The company code is the central enterprise structure of the Financial Accounting by which the General Ledger and its sub-ledgers is managed. The segment is used for required segment reporting according to US-GAAP and IFRS, for example.]

3.
Which object in SAP S/4HANA defines the structure of a balance sheet and P&L statement?
Choose the correct answer.

Chart of accounts

Fiscal year period

Financial statement version

Valuation method

[The financial statement version structures the accounts into balance sheet and p&l statements.]

4.
Which G/L account types are relevant for Management Accounting?
There are two correct answers.

Non-operating expense or income

(X) Primary cost or revenue

(X) Secondary cost

Balance sheet accounts

5. Before you create an asset master record, you must specify an asset class. What does the asset class provide for the asset?
There are two correct answers.

(X) Account determination (key)

(X) Control parameters

Default cost assignment objects

Allowed posting transactions

6.
For a new business partner, which roles would you need to maintain to be able to post a vendor invoice directly through financial accounting?
There are two correct answers.

(X) FI Vendor

Supplier

(X) General Data

FI Customer

7.
Imagine you received an incoming payment from a customer by bank transfer. Unfortunately, the customer forgot to include the invoice number in the payment. Accounts Receivable can post the incoming payment to the customer account but is not able to assign it to a customer invoice. Which of the following transactions will take place for this incoming payment posting?
There are two correct answers.

The open item on the customer account is cleared.

(X) The reconciliation account in the General Ledger Accounting is posted (Credit).

The bank account in General Ledger Accounting is posted (Debit).

(X) The customer account is posted (Credit).

[As the incoming payment is posted to the customer account, the reconciliation account in the General Ledger Accounting is automatically posted on the credit side. The offsetting entry is made on the debit side of the bank account in General Ledger Accounting. However, it is not possible to clear an open item on the customer account because there is no exact payment information available from the customer. The Accounts Receivable department informs the customer about the incoming payment and requests more information about which invoice was paid.]

8.
Activity types are allocated using a secondary cost element, which is stored in the activity type master record.
Choose the correct answer.

(X) True

False