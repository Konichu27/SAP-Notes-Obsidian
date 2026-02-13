| **Feature**                  | **Software as a Service (SaaS)**     | **Managed Cloud Services**                 |
| ---------------------------- | ------------------------------------ | ------------------------------------------ |
| **SAP's Cloud ERP Offering** | SAP S/4HANA Cloud **Public Edition** | SAP S/4HANA Cloud **Private Edition**      |
| **Services**                 | Governed by SLA[^1]                  | Governed by SLA + Roles & Responsibilities |
| **Infrastructure**           | Multi-tenant[^2]                     | Single-tenant[^2]                          |
[^1]: **SLA (Service Level Agreement):** A formal contract between a service provider and a customer that outlines the expected level of service, such as system uptime (e.g., 99.9%), performance metrics, and responsibilities.

[^2]: **Tenant:** In cloud computing, a "tenant" refers to a single user or organization. * **Multi-tenant** means multiple customers share the same physical server and software instance (like an apartment building). * **Single-tenant** means the customer has a dedicated instance of the software and infrastructure, providing more control and isolation (like a private house).

### Terminologies
- **Managed cloud service** - service provider fully controls infrastructure
	- Typically single-tenant
	- In SAP, this is SAP S/4HANA Cloud **Private Edition**; particularly, through **Enterprise Cloud Services (ECS)**
		- **Hyperscalers** - third-party cloud service providers that ECS go through, apart from in-house SAP servers
- **Greenfield**, **brownfield**, **selective data transition (SDT)** - see [[2 - Implementation Types]] and image below
![[Pasted image 20260210142526.png]]

### Two-Tier ERP
- **Two-tier ERP** - when a company uses different ERP systems at different levels for the organization
- Refresher: [[Levels of Clean Core#3-Tier Development Model]]
- **Tier-1** serves as the global backbone for administrative and general functions (ex. finance workflows), while **Tier-2** is for localized business needs
- Allows for a mix of high-level standardization and low-level flexibility

![[Pasted image 20260210143539.png]]

#### Scenarios for Two-Tier ERP

| **Headquarter & Subsidiary** | **HQ** runs specialized *private cloud*[^3], while **subsidiaries** run *standardized public clouds*                  |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Central Service**          | Only **certain parts of the company** run on a standardized public cloud, the rest run on a specialized private cloud |
| **Supply Chain Ecosystem**   | Only **supply chain partners** (subcontructors, dealers, bendors) run on standardized public cloud                    |
[^3]: Assuming private includes both private & on-premise

![[Pasted image 20260210145856.png]]

We also do the following to assess a two-tier ERP strategy:
- **Reporting strategy** - how are reports transmitted throughout the company?
- **Master data management**
- **Change enablement** - end-user training and changes in current business processes