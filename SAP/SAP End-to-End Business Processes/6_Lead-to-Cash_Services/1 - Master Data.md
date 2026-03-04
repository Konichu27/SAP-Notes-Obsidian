# Business Partner

The **Business Partner** is the core of all service processes in the company. They can either be **external** (outside the company) or **internal** (services under the payroll).

![[Pasted image 20260303155549.png]]

---

# Types of Service Business Partners
- **Account** - This is someone with a business relationship. It could be a customer, vendor, or even competitor
- **Contact** - assigned to a corporate account
- **Employee** - member of *your* company

| **Feature**               | **External BP (Customer)**            | **Internal BP (Employee)**              |
| ------------------------- | ------------------------------------- | --------------------------------------- |
| **Key Identifier**        | Customer Number / BP Number           | Personnel Number (PERNR)                |
| **Primary Link**          | Sales Organization / Company Code     | Org Unit / Position / SAP User ID       |
| **Data Focus**            | Sales terms, credit limits, shipping  | Skills, cost centers, login permissions |
| **Usage in Lead-to-Cash** | Who is paying and receiving the bike? | Who is repairing or selling the bike?   |
## External Business Partner Structure

![[Pasted image 20260303160727.png]]

- **Company Code**
- **Customer**
- **Contact**

> [!ABSTRACT] Demo
> [How to Display an External Business Partner](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_3F92AEC9FE6A6192:demo#2)

## Internal Business Partner Structure
- **Company Code**
- **Organizational Unit**
- **Personnel Number**

> [!ABSTRACT] Demo
> [How to Display an External Business Partner](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_3F92AEC9FE6A6192:demo#2)

---
# Product

Products refer to goods or services central to a company's business activities.
## Types of Products

- **Service Material / Service Product** - the *service itself*
- **Component Planning** - spare parts
- **Structuring of Technical Objects** - have the following characteristics:
	- *BOM*
	- *Construction type*
	- *Serial number*

> [!ABSTRACT] Demo
> [How to Display a Service Product](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_41786B7B76EF2889:demo#2)
> [How to Display a Spare Part](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_AFE24FC225A9DE92:demo#2)

## Technical Objects

**Technical objects** are the physical assets that require maintenance, repair, or tracking.

- **Functional Locations:** These represent a place or a system area. They can be subdivided to *functional*, *process-oriented*, and *spatial* types
- **Equipment:** Equipment represents an autonomous, physical object that is maintained as a single unit.
- **Serial Numbers:** Serial numbers are used to tell two identical items apart, particularly materials. In SAP S/4HANA, Equipment and Serial Numbers are often linked. When you sell a serialized bike, the system can automatically create an Equipment record for it.
- **Assemblies:** Assemblies are not tracked as individual "units" with their own history. Instead, they are items from a **Bill of Material (BOM)** used to break down a piece of Equipment into smaller pieces. (ex. Electric Motor, Braking System)

| **Feature**             | **Equipment**      | **Assembly**                   |
| ----------------------- | ------------------ | ------------------------------ |
| **Individual History?** | Yes                | No                             |
| **Serial Number?**      | Yes                | No                             |
| **Inventory Tracked?**  | No (it's an asset) | Yes (it's a material/BOM item) |
| **Example**             | The Bike           | The Chain                      |
## Others

The following are also involved:
- **Conditions** (prices, surcharges/discounts, freight, taxes)

> [!ABSTRACT] Demo
> [How to Display Conditions](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_3F2800315E9305A4:demo#2)

