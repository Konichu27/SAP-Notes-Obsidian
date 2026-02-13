![[Pasted image 20260202231257.png]]

| **Level**   | **Stability** | **Risk Level** | **Description**                                                                       | **Recommendation**                                           |
| ----------- | ------------- | -------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **Level A** | **Highest**   | **Zero/Low**   | Uses only officially released, stable **ABAP Cloud** interfaces.                      | **Best Practice.** Always try this first.                    |
| **Level B** | **High**      | **Low**        | Uses unreleased APIs (like BAPIs) that SAP deems **stable and upgrade-safe**.         | **Preferred.** Safe to use if Level A isn't possible.        |
| **Level C** | **Medium**    | **Moderate**   | Uses unreleased APIs for **legacy needs**. SAP provides a changelog for tracking.     | **Conditional.** Use only if necessary; requires monitoring. |
| **Level D** | **Low**       | **High**       | Uses non-recommended objects. Creates **technical debt** and breaks the "clean core." | **Avoid.** High risk of breaking during upgrades.            |

### 3-Tier Development Model
![[Pasted image 20260202230943.png]]

- **Tier 1** - Cloud-ready ABAP
- **Tier 2** - Cloud APIs that connect to non-SAP objects, usually used for private edition/on-premise
- **Tier 3** - Legacy code, should be retired