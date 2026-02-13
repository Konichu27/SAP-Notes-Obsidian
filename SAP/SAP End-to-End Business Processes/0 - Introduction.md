**SAP S4/HANA** - an ERP business suite designed to be deployer 
**SAP Business Suite** - also an ERP business suite. The difference is that S4/HANA uses in-memory computing while BS does not

![[Pasted image 20260209143155.png]]

![[Pasted image 20260209144659.png]]

| **Business Process** | **Description**                                                           | **Interfaces**                                                                                             | **Deliverables**                                                                                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Finance**          | Day-to-day transactions, forecasts, cash flow management                  | Customers, Sales, Procurement                                                                              | **Financial statements**: balance sheet, income statement, cash flow statement:<br>**Business data**: Accounts payable, accounts receivable, fixed assets, owned inventory<br>(see financial & management accounting) |
| **Controlling**      | Budgeting                                                                 | Production, Marketing & Sales                                                                              | Analysis reports & results<br>(complements financial planning)                                                                                                                                                        |
| **HR**               | Hiring, payroll, & employment retention                                   | All departments,<br>Financial & Management Accounting                                                      | Employee surveys, leadership & training & cultural programs, payrolls, health insurances                                                                                                                              |
| **Procurement**      | Purchase of materials & supplier relations                                | Controlling, Financial Accounting                                                                          | Materials in stock, supplier contracts, shopping catalog for employees                                                                                                                                                |
| **Production**       | Manufacturing & creation of finished products                             | Controlling/Management Accounting (they're considered as one interface), Financial Accounting, Procurement | Manufactured products                                                                                                                                                                                                 |
| **Sales**            | Selling goods & services, customer satisfaction, supply chain integration | Marketing, Finance, Services                                                                               | Quotes and sales orders,  customer relationships, sales estimates & plans                                                                                                                                             |
| **Services**         | Customer suppotr, after-sales, IoT                                        | Sales, Procurement                                                                                         | Support & service delivery, "service visits" incl. spare parts & skilled representatives, recorded service history                                                                                                    |

| <u>**SAP Process**</u> | <u>**Corresp. Departments**</u> | <u>**Complementary Applications (SAP Cloud ERP)**</u> |
| ---------------------- | ------------------------------: | ----------------------------------------------------: |
| **Record to Report**   |            Finance, Controlling |                                                       |
| **Recruit to Retire**  |                 Human Resources |                                    SAP SuccessFactors |
| **Lead[^1] to Cash**   |                 Sales, Services |                                   SAP Marketing Cloud |
| **Design to Operate**  |                      Production |                                                       |
| **Source to Pay**      |                     Procurement |                             SAP Ariba, SAP Fieldglass |
[^1] **Lead** - when a customer is interested in making an order (as opposed to the order itself). We use this distinction because it means the start of the ordering process begins at the lead, not the order itself

### Other Software
- **SAP Process Navigator** - Please see here: [[SAP Applications#Business Processes]]

![[Pasted image 20260209151113.png]]

The solution scenarios relevant for **SAP S/4HANA Cloud Public Edition** are:

- **SAP Best Practices for SAP S/4HANA Cloud Public Edition**: Master package of all preconfigured business processes available in SAP S/4HANA Cloud Public Edition.
- **SAP Best Practices for SAP S/4HANA Cloud for Public Sector**: Selection of business processes from the master package with a focus on public sector management. The solution provides core business processes in finance, sourcing and procurement, and budgeting.
- **Service Centric ERP for SAP S/4HANA Cloud Public Edition**: Selection of business processes from the master package with a focus on service centric ERP. The solution provides best practices for financial management, industry-specific capabilities for project and service-related operations, with a particular emphasis on serving small and midsize companies in service-oriented industries.

The solution scenarios relevant for **SAP S/4HANA Cloud Private Edition** are:

- **SAP Best Practices for SAP S/4HANA Cloud Private Edition**: Master package of all preconfigured business processes available in SAP S/4HANA (on premise) and SAP S/4HANA Cloud Private Edition.
- **Enterprise Management Layer for SAP S/4HANA**: Selection of business processes from the master package with a focus on providing a global template for customers operating in multiple countries. It offers preconfigured, localized business processes for up to 49 countries with a corporate financial design that allows parallel accounting according to group and local requirements based on three sets of ledgers and accounting principles (Group/Local/Tax).