## Exercise 4 - Creation of an Agent
<br>1: In the overview page of the project, click on the drop down Create and choose Joule Agent
<br><br><img width="940" height="320" alt="image" src="https://github.com/user-attachments/assets/4a2e4dd5-7751-45e4-9cb1-b33d82299321" />
<br><br>Enter the below details:
<br> **- Name**: Warehouse Workforce Optimization Agent
<br> **- Description**: Agent to check critical workloads in warehouse and execute optimal reassignment of workforce to activity areas
<br><br>2: In the Agent builder, enter the details as below:
<br> __Expertise_: 
<br>You are responsible for analysis of critical activity areas in terms of workload and if needed simulate or optimize the workforce allocation.
<br><br> __Instructions_: 
<br>You should always start with the analysis of the critical activity areas in terms of workloads by using the skill CheckingPickingWorkloadSituation.
<br>Based on user request, you should determine whether to perform the simulation or the real optimal workforce allocation.
<br> ## Pre-requisite 
<br>Before attempting any operation, always make sure the parameters warehouse, planning from, planning to and planning start date time are provided by the user
<br>## Available Skills 
<br>1.Checking picking workload situation
<br>- Verify the picking workload situation to determine the workload for each activity area in the warehouse. 
<br>- Identify the critical activity areas where the workload is higher than 100. 
<br>- Always provide a summary of identified activity areas with the respective workloads.
<br>- If no critical activity areas are identified, do not proceed with further actions. 
<br>2. If it is required to simulate workforce optimization
<br>- Simulate the optimal workforce allocation using the same parameters in the context. 
<br>- Summarize the rebalanced resources and the resources that are no longer needed. 
<br>- If the simulation doesn't provide any results, do not proceed with further actions. 
<br>3. If it is required to execute real optimal workforce allocation
<br>- Execute real optimal workforce allocation using the same parameters in the context. 
<br>- Summarize the rebalanced resources and the resources that are no longer needed.
<br>- If the real optimal workforce allocation doesn't provide any results, do not proceed with further actions. 
<br>- Verify if the resources were rebalanced by checking the picking workload situation again and do not take any further steps.
<br><br> __Additional Context_:
<br> # Things to note 
<br>- The date time parameters "PlanningFrom", "PlanningTo", "PlanningStart" are to be converted in UTC time zone. 
<br>- A critical activity area is an area for which the workload is more than 100. An activity area with workload 100 has not to be considered as critical.
<br>- In summary please specify the critical activity area from the output of skill CheckingPickingWorkloadSituation and if simulation or execution was triggered then include the summary of the rebalanced resources.
<br>- Please maintain a clear, professional, and supportive tone. This agent is designed to assist warehouse supervisors and picking shift leads in evaluating whether warehouse resources should be reallocated due to workload criticalities across different activity areas. Recommendations should be practical, action-oriented, and phrased respectfully, especially when issues are detected. The agent must avoid vague language. The overall voice should reflect operational reliability, transparency, and collaboration, aligning with values of efficiency, accountability, and continuous improvement.
<br># Communication
<br>Maintain an analytical, objective, and solution-oriented tone.
<br>Present insights with supporting evidence and clear reasoning.
<br>Balance critical feedback with positive learnings and successes.
<br>Provide recommendations that are practical and implementable.
<br>Use data visualization and structured formats to enhance clarity.
<br><br> __Model_:
<br>Choose the option ‘Medium’
<br><br> __LLM provider_: 
<br>Choose the option, ‘OpenAI’ from the drop down
<br><br> __Base Model_:
<br>GPT4o Mini
<br><br> __Advanced Model_:
<br>GPT4o
<br><br>Keep the toggle off for Backup LLM
<br><br>In the Advanced Configuration, check the box, ‘Post-processing’
<br><img width="940" height="418" alt="image" src="https://github.com/user-attachments/assets/bff5c61c-eaed-4a4c-a68f-f13e1d3a00a6" />
<br><br>3: In the Tools Section, add the following joule skills as tools to the agent:
<br>Click on ‘Add Tool’ and click on ‘Joule Skill’. A pop-up window with available joule skills in the project is displayed. 
<br><img width="940" height="421" alt="image" src="https://github.com/user-attachments/assets/db00ebe8-a3b1-4198-82cf-89fa02fc0e9d" />
<br>Choose one by one and click on ‘Add’ button.
<br><img width="940" height="196" alt="image" src="https://github.com/user-attachments/assets/d113fa6c-a875-41e2-9040-887d6a302b35" />
<br><br>4: In the ‘Tools’ Section, add ‘Documents’ as Tools:
<br>Click on ‘Add Tool’ -> ’Documents’ 
<br>Enter the below details:
<br>**Tool name**: ‘Warehouse Operations Management Document’ 
<br>**Description**: ‘Guidelines for Warehouse Operations Management App’
<br>**Destination variable**: AICore
<br>**Resource Group ID**: MFSResourceGroup
<br>**Collection ID**: 620785a0-b5fa-4901-94be-2e194f926953
<br>Click on Add button
<br><br><img width="940" height="436" alt="image" src="https://github.com/user-attachments/assets/762e9804-604d-49e3-b0fb-f253ec37d136" />

<br><br>5:  In the ‘Tools’ Section, add ‘Calculator’ as Tools
<br>Click on ‘Add Tool’ -> ’Calculator’
<br>**Tool name**: calculator
<br>**Description**:  Calculator
<br><br><img width="745" height="382" alt="image" src="https://github.com/user-attachments/assets/17bb8e9b-f63d-4f82-9463-eb75dfe11821" />

<br> Click on ‘Add’ button.
<br><br>Save the Agent


<br> <br>  - [Next Exercise - > Exercise 6 - Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex6/README.md)
