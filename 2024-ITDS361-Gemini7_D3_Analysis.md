# Gemini Project Analysis of 5 selected use cases
---
# Class Diagram
![Class Diagram]()
---
# 1. Create a science plan 

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
![Submit a science plan Activity Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Sequence%20diagrams/3_SubmitSciencePlan.png)

## Sequence Diagram
![Submit a science plan Sequence Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Sequence%20diagrams/3_SubmitSciencePlan.png)


---
# 4. Access collected astronmical data

## Use Case Description

#### 
| **Use Case Name** | Access collected astronmical data  |
|---|---|
| **ID** | 4 |
| **Importance Level** | High |
| **Primary Actor** | Astronomer |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** | Requires access to collected astronomical data for research and analysis. |
| **Science Observer** | Ensures the accuracy and completeness of the collected data. |

### Brief Description
The Astronomer accesses collected astronomical data stored in the system for research purposes. The system verifies user authentication and data integrity before granting access.

### Trigger
| Type | External |
|---|---|
| **Trigger** | The Astronomer requests access to collected astronomical data. |

### Relationships
| Type | Entities |
|---|---|
| **Association** | Astronomer |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 | The Astronomer logs into the system. |
| 2 | The system verifies the Astronomer’s authentication and access permissions. |
| 3 | The system displays the available astronomical data. |
| 4 | The Astronomer selects the required astronomical data. |
| 5 | The system validates the integrity of the selected data. |
| 6 | The system grants access to the validated data. |
| 7 | The Astronomer retrieves and analyzes the data. |

### Subflows
| Step | Condition |
|---|---|
| **5a** |  If data integrity issues are detected: The system notifies the Science Observer for verification before granting access. |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **2a** | If the Astronomer lacks access permissions: The system denies access and provides instructions to request necessary permissions. |
| **6a** | If the requested data is unavailable: The system notifies the Astronomer and suggests verifying the request or checking back later. |

## Activity Diagram
![Access collected astronmical data  Activity Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Activity%20diagrams/4_AccessCollectedAstronomicalData.png)

## Sequence Diagram
![Access collected astronmical data  Sequence Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Sequence%20diagrams/4_AccessCollectedAstronomicalData.png)
---


# 5. Access live view of telescope

## Use Case Description

#### 
| **Use Case Name** | Access live view of telescope  |
|---|---|
| **ID** | 5 |
| **Importance Level** | High |
| **Primary Actor** | Astronomer |
| **Use Case Type** | Detail, Essential |

### Stakeholders and Interests
| Stakeholder | Interest |
|---|---|
| **Astronomer** | Requires live access to the telescope’s view for real-time observations and analysis. |
| **Telescope Operator** | May monitor or manage the live view to ensure proper functioning of the telescope |

### Brief Description
The Astronomer accesses a live view of the telescope through the system to observe astronomical objects in real-time. The system streams the live data from the telescope for the Astronomer to view and analyze.

### Trigger
| Type | External |
|---|---|
| **Trigger** | The Astronomer requests to access the live view from the telescope. |

### Relationships
| Type | Entities |
|---|---|
| **Association** | Astronomer |
| **Include** | - |
| **Extend** | - |
| **Generalization** | - |

### Normal Flow of Events
| Step | Description |
|---|---|
| 1 | The Astronomer sends a request to access the live view of the telescope. |
| 2 | The system authenticates the Astronomer’s credentials. |
| 3 | The system establishes a live connection to the telescope's feed. |
| 4 | The system streams the live view to the Astronomer. |
| 5 | The Astronomer observes and analyzes the live view for further study. |

### Subflows
| Step | Condition |
|---|---|
| **3a** |  If the system requires additional permissions: The system requests authorization from the Telescope Operator before granting access |

### Alternate/Exceptional Flow
| Step | Condition |
|---|---|
| **2a** |  If authentication fails: The system denies access and prompts the Astronomer to retry or contact support. |
| **3b** |  If the live view connection fails: The system notifies the Astronomer and suggests retrying later. |

## Activity Diagram
![Access live view of telescope Activity Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Activity%20diagrams/5_AccessLiveViewOfTelescope.png)

## Sequence Diagram
![Access live view of telescope Sequence Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/Sequence%20diagrams/5_AccessLiveViewOfTelescope.png)
---
