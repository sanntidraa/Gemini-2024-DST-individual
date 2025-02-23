# Gemini Project Analysis of 5 selected use cases
---
# Class Diagram
![Class Diagram]()
---
# 1. Create a science plan 
## Use Case Diagram
![Create a science plan  Use Case Diagram]()

## Use Case Description

#### 
| **Use Case Name** | Create a science plan  |
|---|---|
| **ID** | 1 |
| **Importance Level** | High |
| **Primary Actor** | Astronomer  |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** | Needs to create an effective science plan |
| **Science Observer** | Uses the plan to conduct observations and collect data |

### Brief Description
The astronomer creates a science plan by specifying parameters such as the target object, observation time, telescope settings, etc. The plan can be previewed, annotated, versioned, and optionally submitted for validation.

### Trigger
| Type | User-Initiated |
|---|---|
| **Trigger** | The astronomer wants to create a new science plan |

### Relationships
| Type | Entities |
|---|---|
| **Association** |  Astronomer, Science Observer |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 | The astronomer selects "Create Science Plan" from the menu.  |
| 2 | The system displays a form for entering details (e.g., target object, observation time, telescope settings) |
| 3 | Before saving, the astronomer can preview or simulate the plan using a virtual telescope to test how it would function under different conditions (e.g., weather, instrument availability).  |
| 4 | The astronomer fills in the details and optionally attaches comments, notes, or reference materials for the Science Observer. |
| 5 | The astronomer clicks "Save", and the system validates the entered data.  |
| 6 | The system saves the plan to the database and confirms successful creation. |
| 7 | The system tracks the version of the plan for accountability and allows rollbacks if modified later. |
| 8 | The astronomer has the option to submit the science plan for validation immediately after creation. |

### Subflows
| Step | Condition |
|---|---|
| **5a** | The system verifies that all required fields are filled and correct. |
| **5a** | If data is incomplete, the system prompts the astronomer to correct the errors. |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **3a** | The system notifies the user that the simulation service is temporarily unavailable. |
| **3a** | The astronomer can proceed without simulation.  |
| **5b** | The system notifies the user of an error and suggests retrying later.  |

## Activity Diagram
![Create a science plan  Activity Diagram]()

## Sequence Diagram
![Create a science plan  Sequence Diagram]()


---
# 2. Test a science plan
## Use Case Diagram
![Test a science plan Use Case Diagram]()

## Use Case Description

#### 
| **Use Case Name** | Test a science plan |
|---|---|
| **ID** | 2 |
| **Importance Level** | High |
| **Primary Actor** | Astronomer |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** | Needs to verify that the science plan is valid before real observations. |
| **Science Observer** | Needs validated plans for scheduling actual observations. |

### Brief Description
 The astronomer tests the created science plan using a simulation system to ensure correctness and functionality before actual execution. This step helps identify issues like target visibility, instrument compatibility, and environmental constraints.

### Trigger
| Type | User-Initiated |
|---|---|
| **Trigger** | The astronomer wants to test a science plan before submission. |

### Relationships
| Type | Entities |
|---|---|
| **Association** | Astronomer, Science Observer |
| **Include** | Operate the interactive observing (virtual telescope) |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 | The astronomer selects "Test Science Plan" from the menu. |
| 2 | The system retrieves the selected science plan from the database. |
| 3 | The system loads the simulation environment. |
| 4 | The system executes the test by simulating the telescope operation using the provided science plan. |
| 5 | The system displays the results of the simulation. |
| 6 | The astronomer reviews the test results and may adjust the science plan if needed. |
| 7 | The system submits the science plan to the Science Observer for validation. |
| 8 | The Science Observer reviews and validates the plan. |
| 9 | If the plan is approved, it is transformed into an Observing Program. |
| 10 | The system logs the final decision and notifies the astronomer. |

### Subflows
| Step | Condition |
|---|---|
| **4a** | The astronomer can fine-tune test conditions by modifying telescope settings, target selection, or scheduling constraints before re-running the test |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **3a** | The system notifies the astronomer that the simulation service is temporarily unavailable. |
| **3a** | The astronomer can retry later or use offline analysis tools if available. |

## Activity Diagram
![Test a science plan Activity Diagram]()

## Sequence Diagram
![Test a science plan Sequence Diagram]()


---
# 3. Submit a science plan
## Use Case Diagram
![Submit a science plan Use Case Diagram]()

## Use Case Description

#### 
| **Use Case Name** | Submit a Science Plan |
|---|---|
| **ID** | 3 |
| **Importance Level** | High |
| **Primary Actor** | Astronomer |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** | Wants to submit the science plan for review and execution. |
| **Science Observer** | Needs to validate and transform the submitted plan into an observing program. |
| **Operation Staff** | Ensures the plan is executable within the telescope system. |

### Brief Description
This use case describes the process where an Astronomer submits a completed science plan for validation and execution by the Science Observer and Operation Staff.

### Trigger
| Type | User-Initiated |
|---|---|
| **Trigger** | The Astronomer completes the science plan and initiates the submission process. |

### Relationships
| Type | Entities |
|---|---|
| **Association** | Astronomer, Science Observer, Operation Staff |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 | The Astronomer finalizes the science plan. |
| 2 | The Astronomer selects the "Submit Science Plan" option in the system. |
| 3 | The system verifies the completeness of the plan. |
| 4 | The system records the submission and notifies the **Science Observer**. |
| 5 | The **Science Observer** reviews the plan for validation. |
| 6 | If valid, the plan is transformed into an **Observing Program**. |

### Subflows
| Step | Condition |
|---|---|
| **3a** | If mandatory fields are missing, the system prompts the **Astronomer** to complete them. |
| **5a** | If the **Science Observer** requires modifications, they return the plan for revision. |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **4a** | If submission fails due to a system error, the **Astronomer** is notified and advised to retry later. |
| **6a** | If the plan is **not approved**, the **Astronomer** is notified with feedback for revisions. |

## Activity Diagram
![Submit a science plan Activity Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Activity%20diagrams/3_SubmitSciencePlan.png)

## Sequence Diagram
![Submit a science plan Sequence Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Sequence%20diagrams/3_SubmitSciencePlan.png)


---
# 4. Access collected astronmical data
## Use Case Diagram
![Access collected astronmical data Use Case Diagram]()

## Use Case Description

#### 
| **Use Case Name** | Access collected astronmical data  |
|---|---|
| **ID** | 4 |
| **Importance Level** | High |
| **Primary Actor** |  |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** |  |
| **Science Observer** |  |
| **Operation Staff** |  |

### Brief Description


### Trigger
| Type | User-Initiated |
|---|---|
| **Trigger** |  |

### Relationships
| Type | Entities |
|---|---|
| **Association** | - |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 |  |
| 2 |  |
| 3 |  |
| 4 |  |
| 5 |  |
| 6 |  |

### Subflows
| Step | Condition |
|---|---|
| **3a** |  |
| **5a** |  |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **4a** |  |
| **6a** |  |

## Activity Diagram
![Access collected astronmical data  Activity Diagram]()

## Sequence Diagram
![Access collected astronmical data  Sequence Diagram]()
---


# 5. Access live view of telescope
## Use Case Diagram
![Access live view of telescope Use Case Diagram]()

## Use Case Description

#### 
| **Use Case Name** | Access live view of telescope  |
|---|---|
| **ID** | 5 |
| **Importance Level** | High |
| **Primary Actor** |  |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** |  |
| **Science Observer** |  |
| **Operation Staff** |  |

### Brief Description


### Trigger
| Type | User-Initiated |
|---|---|
| **Trigger** |  |

### Relationships
| Type | Entities |
|---|---|
| **Association** | - |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 |  |
| 2 |  |
| 3 |  |
| 4 |  |
| 5 |  |
| 6 |  |

### Subflows
| Step | Condition |
|---|---|
| **3a** |  |
| **5a** |  |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **4a** |  |
| **6a** |  |

## Activity Diagram
![Access live view of telescope Activity Diagram]()

## Sequence Diagram
![Access live view of telescope Sequence Diagram]()
---
