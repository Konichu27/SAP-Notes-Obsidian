**Period Closing** takes place at the **Controlling (CO)** module in SAP.

Examples of costs calculated during period closing include:

- **Scrap Variance:** Happens when there are issues during production. Ex. 
- **WIP Calculation:** Used for spending for a product still in progress, but still needs to be reported in the balance sheet
- **Variance Calculation**
- **Settlement**

![[Pasted image 20260301204351.png]]

In this note, we will be focusing on **variance calculation** and **settlement**.

---
# Variance Calculation

**Variance calculation** is the calculation of the actual costs vs the target costs. Here, scrap variance and WIP variance are dealt with.

Variance calculation involves different types of **variance categories**. There are two different types of categories: **input** and **output**.
#### Input Categories
These occur because of the **resources** (materials, labor, overhead) put **into the order**.

| **Input Category**           | **Definition**                                                      | **Real-World Example**                                                                                  |
| ---------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Input Price Variance**     | The price of a resource changed between planning and consumption.   | You planned for Raw Material A at $10/kg, but the current moving average price is $11/kg.               |
| **Input Quantity Variance**  | You used more or less of a resource than the BOM/Routing specified. | A machine was supposed to run for 15 mins but ran for 17 mins.                                          |
| **Resource Usage Variance**  | You substituted one resource for another.                           | You ran out of Raw Material 1 and used Raw Material 2 instead. The entire cost of both is flagged here. |
| **Remaining Input Variance** | Differences in overhead or costs that don't fit the above.          | Material overhead costs increased because the base price of the material rose.                          |

#### Output Categories
These occur because of how the **finished product** is received into inventory.

| **Output Category**       | **Definition**                                                                                      | **Real-World Example**                                                                                          |
| ------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Mixed Price Variance**  | Occurs when a product is made via multiple "procurement alternatives" (e.g., two different plants). | The standard price is a weighted average of two plants, but this specific batch came from only one.             |
| **Lot Size Variance**     | Fixed costs (like setup time) are spread over a different number of units than planned.             | You planned to make 100 units (spreading $100 setup cost to $1/unit), but you only made 50 (making it $2/unit). |
| **Output Price Variance** | The price at which the product is delivered to stock differs from the standard price.               | Usually happens if the material is managed at Moving Average Price (MAP) rather than Standard Price ($S$).      |
| **Remaining Variance**    | A "catch-all" for differences the system cannot specifically categorize.                            | Often caused by rounding differences or when target costs cannot be calculated.                                 |

> [!ABSTRACT] Demo
> [How to Perform Variance Calculation](https://learnsap.enable-now.cloud.sap/pub/mmcp/index.html?show=project!PR_FB0773F2CB111091:demo#2)
# Settlement
This is the last step of the period end closing.

You need to settle the variances in price (variance calculations) and all the other things needed to determine a final, definitive price.

Mainly, you need to settle 3 things:
- **Work in Progress**
- **Price Difference**
- **Variance Categories**


---

# Miscellaneous

- **FUL:** Full settlement

| **Order Status** | **What it means**                   | **The Action taken**                                                           |
| ---------------- | ----------------------------------- | ------------------------------------------------------------------------------ |
| **Open / REL**   | Still working on it! 🛠️            | **WIP is calculated.** (The money stays "in progress").                        |
| **DLV / TECO**   | Delivered or Technically Complete ✅ | **Variances are calculated.** (WIP is canceled, and differences are recorded). |
