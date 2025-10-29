## Exercise 4 - Create a Joule Agent :wrench:

1: In the overview page of the project, click on the drop down Create and choose Joule Agent

<img width="1789" height="615" alt="image" src="https://github.com/user-attachments/assets/ca005dd2-d51c-425e-b97e-88ce83473878" />


* Enter the below details:
  
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Name**        | `Agent for Logistics`                  |
| **Description** | `An agent to create OR update OR track shipments in GTT` |

* Click on 'Create'
<img width="3538" height="1298" alt="image" src="https://github.com/user-attachments/assets/2aadd9a6-3717-4f81-b557-22596d213e2c" />



2: In the Agent builder, enter the details as below:<br>

**Expertise**:

**💡 Tip:** Defines the agent's professional identity and field of knowledge.	This tells the agent which general business area it is operating in, such as finance, human resources, or supply chain. Your input here will help shape the agent's overall tone, vocabulary, and scope.

```
You are responsible to create shipment, determine/suggest cheapest carrier, update carrier OR track shipments in GTT.
```

**Instructions:**

**💡 Tip:** Specifies the agent's core goal, rules, and constraints.	This is the most critical part, as it dictates what the agent should accomplish. It directs the agent's behavior by providing guardrails and setting its primary objective.

```
1. Create Shipment: Use the tool 'Create Shipment' to create a new shipment. Trigger the tool Create Shipment assigned to the agent and display the message from the tool and stop. 
2. Suggest Carrier options: If the user asks for carrier suggestion then use the document "Carrier Selection Guide.docx" to show all the carrier options to the user.  Provide the list with a "Select" button or a checkbox for the user to select one of the carrier option displayed and use that carrier value and execute the tool "Create Shipment" to update the carrier to the shipment in the conversation. 
3. If the user, updates a carrier from the list of options displayed then use the tool "Create Shipment" to update the carrier with the shipment details user provided in the chat history. If no chat history, then trigger skill "Create Shipment". 
4. Track Shipment: Use the tool "Track Shipment". Trigger the tool "Track Shipment" and display the message as available in the tool. 
5. Delayed Shipment: if the user prompts for Eg. "show me all the delayed shipments", execute the tool "Delayed Shipments". 

The prompts from the user could be in any order, evaluate the right tool to be used based on the user prompt.
<br>
```
<br>

**Additional Context:**

**💡 Tip:** This field allows you to feed the agent more specific, relevant, and potentially evolving information. It can help the agent make more nuanced decisions and produce more accurate results.


```
Please maintain a clear, professional, and supportive tone. This agent is designed to assist maintenance planners and operations teams in evaluating whether a maintenance order can proceed without delays due to missing materials.

Recommendations should be practical, action-oriented, and phrased respectfully, especially when issues are detected. The agent must avoid vague language.

If shipments are unavailable, it should state so explicitly and guide the user on next steps such as check logss, api not called, etc.

The overall voice should reflect operational reliability, transparency, and collaboration, aligning with values of efficiency, accountability, and continuous improvement.

Display all carriers list as card or a selection list for the user to clearly select the carriers and also display cost, currency associated to each carrier.
```
<img width="1800" height="808" alt="image" src="https://github.com/user-attachments/assets/b33e3dfd-cbbb-4676-b9ac-bda65c2a4132" />

* Choose the remaining options according to the table below:
  
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Model**        | `Medium`                  |
| **LLM provider** | `OpenAI` |
| **Base Model** | `GPT4o Mini` |
| **Advanced Model** | `GPT4o` |
| **Backup LLM** | `Toggle Off` |
| **Advanced Configuration** | `both checkboxes Unchecked` |

* Keep the toggle off for Backup LLM
* In the Advanced Configuration, leave the check boxes un checked.

<img width="1775" height="767" alt="image" src="https://github.com/user-attachments/assets/f1926b54-788c-4b91-91ef-a76bec7e73b5" />


<br>3: In the Tools Section, add the following joule skills as tools to the agent:
<br>Click on ‘Add Tool’ and click on ‘Joule Skill’. A pop-up window with available joule skills in the project is displayed.

<br>Choose one by one and click on ‘Add’ button.
<img width="1797" height="898" alt="image" src="https://github.com/user-attachments/assets/16feaee2-b821-4ce0-94cf-3bea0ccb489d" />

<br>4: In the ‘Tools’ Section, add ‘Documents’ as Tools:
<br><br>Click on ‘Add Tool’ -> ’Documents’
<br>Enter the below details:
<br><br>Tool name: ‘Carrier Selection Guide'
<br>Description: ‘Internal guidelines required by the agent to select cheapest carrier based on the costs provided in the document. It covers the carrier selection guide as a table with all possible carriers for the given source and destination location.’
<br>-Destination variable: AICore
<br>-Resource Group ID: MyResourceGroup
<br>-Collection ID: 05af5860-a616-4ae0-ae39-bacff6d90a61
<br><br>--Click on Apply button

<img width="1800" height="852" alt="image" src="https://github.com/user-attachments/assets/df782a69-4811-4c9a-a5ec-03df27ed48ab" />


<br>
Save the Agent



<br> <br>  - [Next Exercise - > Exercise 4.1 - Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex4/Exercise%204.1%3A%20Test%20an%20Agent%20in%20Private%20Environment.md)
<br> <br>  - [Back To Landing Page](https://github.com/SAP-samples/teched2025-AI163/blob/main/README.md)
