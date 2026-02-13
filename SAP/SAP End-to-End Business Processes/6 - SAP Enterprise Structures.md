# Enterprise Structure
- a framework designed to describe a business's structure
Ex.
![[Pasted image 20260213163849.png]]
# Hierarchy of an SAP System
![[Pasted image 20260213164407.png]]
- TODO: Put this in the master notes
- **Client** - highest hierarchical enterprise in SAP
	- Contains master data
- **Controlling** - manages financial spending
	- **Operating concern** - for profitability analysis (*CO-PA* in SAP terms)
		- Sales uniform structure? Uniform analysis level of spending? (idk what this means)
	- **Controlling entry** - for management accounting
		- Where all costs and revenue are allocated
		- Basic financial structure for controlling 
		- Closed entity. (idk what this means)
- **Financial accounting** - manages financial reporting
	- **Company code** - the creme de la creme of company references in SAP. Legal & financial requirements are usually already assigned to a specific company code, based on the master data.
	- **Segment** - a division based on the company code. Usually used for independent reporting of company regions, divisions, or areas of operation (ex. EMEA, Asia-Pacific, Singapore, etc.)
		- Ex. say you have the same company code operating in US and then in Europe. You'll need two segments for each region:
			- US-GAAP (General Accepted Accounting Standards)
			- IFRS (International Financial Reporting Standards)
		- Or if you have a company like Sony, you could divide it like this:
			- **Company Code:** Sony Group (The legal entity)
			- **Segment A:** Electronics (PlayStation, TVs)    
			- **Segment B:** Pictures (Movie studio)    
			- **Segment C:** Music
			- etc.
- **Sales distribution** - manages distribution channels of products
	- **Sales area**
		- **Sales organization** - business unit that sells (ex. a German bike company has two different sales orgs, Berlin & Frankfurt)
		- **Distribution channel** - Methods of distribution (ex. Frankfurt has retail trade & online sales. Berlin only has retail)
		- *NOTE:* Plants are assigned to specific sales areas. In this case, the combo of sales organizations & distribution channels are called *distribution chains*
	- **Shipping point** - place or location where goods are shipped. Usually assigned to GLMM
	- More info: [[3.1 - Introduction#The Sales Area]]
- **General logistics and material management** - manages production, procurement, and supply chain
	- **Purchasing organization** - responsible for all purchases
	- **Plant** - Central enterprise of logistics
	- **Storage location** - where stocks are stored
	- **Division** - types of products are put into one division.
		- Part of the greater **sales area** as defined in SD. Sales orgs have a many-to-many relationship w/ divisions 
	- **Valuation level**
		- Plant level
		- Company code level
- **Human resource management** - manages employees and payrolls
	- **Personnel area** - also a subdivision of a company code, like a segment. However, this mostly refers to specific offices/reporting areas
- **Logistics execution** - manages the delivery part of the supply chain
	- **Warehouse number** - represents a single warehouse
	- **Warehouse management system** - usually used for "agile warehousing" where there isn't a specific warehousing spot at a given time.

> [!NOTE] In S/4 HANA...
> Two types of configurations: applications & business processes
> Business processes are configured during system setup/customization, not daily activities

>[!NOTE] We also have **3** different types of purchasing organization configurations...
>1. Central purchasing organization
>2. Cross-plant - **P-Org** is assigned to a **company code**, and is thus responsible for **all plants within**
>3. Plant-specific - assigned to **one plant**

> [!NOTE] Types of Links
> - Many **Storage Locations** → One **Plant**.
> - Many **Plants** → One **Company Code**.
> - Many **Company Codes** → One **Controlling Area**.

| **Bike Company**        | **SAP S/4HANA**           |
| ----------------------- | ------------------------- |
| The entire bike company | One client                |
| Finance                 | Financial Accounting      |
| Controlling             | Controlling               |
| Human Resources         | Human Resource Management |
| Procurement             | Materials Management      |
| Sales and Services      | Sales and Distribution    |
| Production              | Production                |

| **Bike Company**                                    | **SAP S/4HANA**                                                                                                        |
| --------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| One view on costs and revenues                      | One controlling area (= bike company)                                                                                  |
| Profit margin based on different criteria           | One operating concern (= bike company                                                                                  |
| 12 independent legal entities                       | 12 company codes                                                                                                       |
| 3 areas of operation (bikes, spare parts, services) | 3 segments                                                                                                             |
| Divers employee structure per site and department   | 12 personell areas                                                                                                     |
| 4 production sites with different costs             | - 4 (production) plants<br>- Valuation level for each plant                                                            |
| 8 additional distribution centers                   | 8 distribution centers                                                                                                 |
| Purchasing central or local                         | - One central purchasing organization<br>- One purchasing organization per plant<br>- Storage locations for each plant |
| Several warehouses                                  | Warehouse management                                                                                                   |
| 1 sales department per subsidiary                   | One sales organization for each legal entity                                                                           |
| 3 sales channels (direct sales, internet, reseller) | 3 distribution channels                                                                                                |
| 1 central customer interaction center               | Shipping points for each plant                                                                                         |
| 1 service department per site                       | Equals the sales organization                                                                                          |