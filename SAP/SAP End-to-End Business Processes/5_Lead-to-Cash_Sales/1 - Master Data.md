# Customer Master Data
Master data for an *FI Customer* (a type of Business Partner) consists of the following:
## 1. **FI Customer Role**
- This is **relevant for Accounting**.
- It is **valid for the company code**.
## 2. **Customer Role**
- It is **valid for the sales area**. (recall that the sales area consists of a sales org, distribution channel, division)

> [!ABSTRACT] Demo
> [Extend BP Role - Customer](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_731417FACCFBDD98:demo#2)

---
# Product Master Record

The product master record consists of the following:
- **Material Master Record**
- **Plants** (Plant A, Plant B, etc.)
- **Sales Organizations** (A, B, etc.)
- **Localized Data** can also be recorded for each plant or sales org.

![[Pasted image 20260302202627.png]]
# Condition Master Record
- A unique type of master data that decides the cost of a product
- Can be **dependent on other data**
- Consists of the following:

> [!ABSTRACT] Demo
> [Creating Pricing Conditions](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_DF7BF0E94E935EB2:demo#2)
## Parts of a Condition Master Record
- **Prices**
- **Surcharges & Discounts**
- **Freight**
- **Taxes**

# Output Data Master

The output data master **determines the information sent to the customer**. What is available for the user? Is it sent through mail, EDI, and/or fax? etc.
## Data Flow of Output Master Data
1. **Output Master Data:** First, data from each business partner must be confirmed. Ex. transport agreements, delivery, payment conditions, etc.
2. **Sales Order:** "Applicable organizational elements must be assigned" (idk what this means)
3. **Order Confirmation:** The document is generated

![[Pasted image 20260302203324.png]]
