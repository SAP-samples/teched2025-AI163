## Exercise 4 - Create a Joule Agent :wrench:

1: In the overview page of the project, click on the drop down Create and choose Joule Agent

<img width="1789" height="615" alt="image" src="https://github.com/user-attachments/assets/ca005dd2-d51c-425e-b97e-88ce83473878" />


Enter the below details:
- Name: Agent for Logistics
- Description: An agent to create OR update OR track shipments in GTT
<br>And click on 'Create'
<img width="1769" height="649" alt="image" src="https://github.com/user-attachments/assets/a955d4f2-273a-4640-8b2a-92b89b749710" />


2: In the Agent builder, enter the details as below:<br>

**Expertise**:
<br>You are responsible to create shipment, determine/suggest cheapest carrier, update carrier OR track shipments in GTT.
<br>
<br>**Instructions:**
<br>1. Create Shipment: Use the tool 'Create Shipment' to create a new shipment. Trigger the tool Create Shipment assigned to the agent and display the message from the tool and stop. 
<br>2. Suggest Carrier options: If the user asks for carrier suggestion then use the document "Carrier Selection Guide.docx" to show all the carrier options to the user.  Provide the list with a "Select" button or a checkbox for the user to select one of the carrier option displayed and use that carrier value and execute the tool "Create Shipment" to update the carrier to the shipment in the conversation. 
<br>3. If the user, updates a carrier from the list of options displayed then use the tool "Create Shipment" to update the carrier with the shipment details user provided in the chat history. If no chat history, then trigger skill "Create Shipment". 
<br>4. Track Shipment: Use the tool "Track Shipment". Trigger the tool "Track Shipment" and display the message as available in the tool. 
<br>5. Delayed Shipment: if the user prompts for Eg. "show me all the delayed shipments", execute the tool "Delayed Shipments". 

The prompts from the user could be in any order, evaluate the right tool to be used based on the user prompt.
<br>
<br>**Additional Context:**
<br>Please maintain a clear, professional, and supportive tone. This agent is designed to assist maintenance planners and operations teams in evaluating whether a maintenance order can proceed without delays due to missing materials.
<br>Recommendations should be practical, action-oriented, and phrased respectfully, especially when issues are detected. The agent must avoid vague language. If shipments are unavailable, it should state so explicitly and guide the user on next steps such as check logss, api not called, etc. 
<br>The overall voice should reflect operational reliability, transparency, and collaboration, aligning with values of efficiency, accountability, and continuous improvement. 
<br>Display all carriers list as card or a selection list for the user to clearly select the carriers and also display cost, currency associated to each carrier.

<img width="1800" height="808" alt="image" src="https://github.com/user-attachments/assets/b33e3dfd-cbbb-4676-b9ac-bda65c2a4132" />


<br>**Model:**
<br>Choose the option ‘Medium’

<br>**LLM provider:**
<br>Choose the option, ‘OpenAI’ from the drop down
<br>
**Base Model:**
<br>GPT4o Mini
<br>
<br>**Advanced Model:**
<br>GPT4o

<br>Keep the toggle off for Backup LLM
<br>In the Advanced Configuration, leave the check boxes un checked.

<img width="1775" height="767" alt="image" src="https://github.com/user-attachments/assets/f1926b54-788c-4b91-91ef-a76bec7e73b5" />


<br>3: In the Tools Section, add the following joule skills as tools to the agent:
<br>Click on ‘Add Tool’ and click on ‘Joule Skill’. A pop-up window with available joule skills in the project is displayed.

<br>Choose one by one and click on ‘Add’ button.
<img width="1797" height="898" alt="image" src="https://github.com/user-attachments/assets/16feaee2-b821-4ce0-94cf-3bea0ccb489d" />

<br>4: In the ‘Tools’ Section, add ‘Documents’ as Tools:
<br><br>Click on ‘Add Tool’ -> ’Documents’
<br>Enter the below details:
<br>Tool name: ‘Carrier Selection Guide'
<br>Description: ‘Internal guidelines required by the agent to select cheapest carrier based on the costs provided in the document. It covers the carrier selection guide as a table with all possible carriers for the given source and destination location.’
<br>Destination variable: AICore
<br>Resource Group ID: LGAResourceGroup
<br>Collection ID: 620785a0-b5fa-4901-94be-2e194f926953
<br>Click on Add button

<img width="1789" height="811" alt="image" src="https://github.com/user-attachments/assets/d720f40e-502b-4af9-afc8-57e1c9cb298f" />



Save the Agent



<br> <br>  - [Next Exercise - > Exercise 4.1 - Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex4/Exercise%204.1%3A%20Test%20an%20Agent%20in%20Private%20Environment.md)
