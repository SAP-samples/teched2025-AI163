## Ex. 4 - Create a Joule Agent :wrench:

### Prerequisite: Create AI Core Destination Variable
Before we build the agent, we must create a Destination Environment variable for AI Core. This allows the Joule Agent to connect with the AI Core environment for document-based reasoning.
<br>
1. Click the **Settings** icon in the top-right corner of the Joule Skill Package, as shown in the screenshot:
<img width="1798" height="670" alt="image" src="https://github.com/user-attachments/assets/399ac844-ddcb-4fe4-9e45-9ae6628d5144" />

* Click on **Environment Variables** and then the **Create** button.
<img width="1783" height="798" alt="image" src="https://github.com/user-attachments/assets/989661f9-aea0-469f-9580-90a214749c47" />

<br>Input the following values and click **Create**: 

| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Identifier**        | `AiCore`                  |
| **Description** | `Destination for AI Core` |
| **Type** | `Destination` |

<img width="1781" height="799" alt="image" src="https://github.com/user-attachments/assets/5139c4b5-d540-4266-9c41-3e8b3071d400" />

<br>

---
### 💡 Understanding Joule Agents

**Joule Agents** represent the next evolution of enterprise automation — intelligent, autonomous systems that **plan, reason, and act** across multiple tools and systems to achieve complex goals.  
While **Joule Skills** execute predefined, deterministic operations, Joule Agents handle **multi-step, adaptive workflows**, deciding *what to do, when, and how* based on business context and user intent.

Functioning as orchestration layers, Joule Agents combine analytical reasoning with real-time decision-making. They use **Large Language Models (LLMs)** to interpret user requests, dynamically select relevant tools (including Joule Skills), and generate contextual responses — enabling **goal-oriented, conversational automation**.

Each Joule Agent is built around four key cognitive abilities:

1. **Planning** – The agent determines the best sequence of actions to achieve a business goal, orchestrating multiple tools or Joule Skills as needed.  
2. **Reflection** – The agent evaluates its own steps, identifies errors or missing data, and self-corrects to reach the desired outcome.  
3. **Tool Usage** – The agent dynamically invokes SAP Build Actions, Joule Skills, or other APIs to perform operations, retrieve data, or trigger systems.  
4. **Collaboration** – Agents can cooperate with other agents or human users, engaging in dialogue, confirmation, or validation when business logic requires oversight.

![Joule Skills vs Agents](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex5/Joule%20Skills%20vs%20Agents.jpg)

---

### ⚙️ Why This Matters

While **Joule Skills** define *what* actions can be performed (e.g., analyze workloads or simulate optimizations), the **Joule Agent** defines *how* these skills are orchestrated in a conversational, goal-driven workflow.  

This agent:
- Combines multiple Joule Skills into an intelligent flow.  
- Makes autonomous decisions based on data and context.  
- Communicates naturally with warehouse supervisors.  

In short, this is where your **Logistics Agent** scenario becomes fully functional.

---

### Part 1: Create and Define the Agent

1. In the overview page of your project, click on the dropdown **Create** and choose **Joule Agent**.
<img width="1789" height="615" alt="image" src="https://github.com/user-attachments/assets/ca005dd2-d51c-425e-b97e-88ce83473878" />

* Enter the below details and click **Create**:
  
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Name**        | `Agent for Logistics`                  |
| **Description** | `An agent to create OR update OR track shipments in GTT` |

<img width="3538" height="1298" alt="image" src="https://github.com/user-attachments/assets/2aadd9a6-3717-4f81-b557-22596d213e2c" />

<br>
<br>

2. In the Agent builder, enter the details as below:<br>

**Expertise**:

**💡 Tip:** Expertise defines the agent's professional identity and field of knowledge.	This tells the agent which general business area it is operating in, such as finance, human resources, or supply chain. Your input here will help shape the agent's overall tone, vocabulary, and scope.

```
You are responsible to create shipment, determine/suggest cheapest carrier, update carrier OR track shipments in GTT.
```

**Instructions:**

**💡 Tip:** Instructions specifies the agent's core goal, rules, and constraints.	This is the most critical part, as it dictates what the agent should accomplish. It directs the agent's behavior by providing guardrails and setting its primary objective.

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

<br><br>

---

### Part 2: Model and Tool Configuration

1. Choose the **Model Configuration** options according to the table below:
  
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Model**        | `Medium`                  |
| **LLM provider** | `OpenAI` |
| **Base Model** | `GPT4o` |
| **Advanced Model** | `GPT4o` |
| **Backup LLM** | `Toggle OFF` |
| **Advanced Configuration** | `Both checkboxes Unchecked` |

<img width="1775" height="767" alt="image" src="https://github.com/user-attachments/assets/f1926b54-788c-4b91-91ef-a76bec7e73b5" />
<br><br>

2. In the **Tools Section**, add the Joule Skills you created as tools for the agent:
* Click on **‘Add Tool’** and then click on **‘Joule Skill’**. A pop-up window with available skills in the project will be displayed.
* Choose each skill one-by-one and click the **‘Add’** button.
<img width="1797" height="898" alt="image" src="https://github.com/user-attachments/assets/16feaee2-b821-4ce0-94cf-3bea0ccb489d" />

<br><br>

3. Add **Document Grounding** as a tool:
* In the ‘Tools’ Section, click on **‘Add Tool’** -> **’Documents’**.
<img width="1789" height="785" alt="image" src="https://github.com/user-attachments/assets/42a5cd61-65fe-468c-956c-f59f415a70a9" />

<br>Enter the below details:

| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Tool name**        | `Carrier Selection Guide`                  |
| **Description** | `Internal guidelines required by the agent to select cheapest carrier based on the costs provided in the document. It covers the carrier selection guide as a table with all possible carriers for the given source and destination location.` |
| **Destination variable**        | `AICore`                  |
| **Resource Group ID**        | `MyResourceGroup`                  |
| **Collection ID**        | `05af5860-a616-4ae0-ae39-bacff6d90a61`                  |

**💡 Tip:** Document grounding in SAP Build Joule Agent is a capability that uses a Retrieval-Augmented Generation (RAG) technique to provide users with accurate, specific answers based on an organization's internal business documents. Instead of relying only on a large language model's (LLM) general training data, Joule can reference a customer's private data, such as HR policies, manuals and FAQs. 
This process enhances the reliability and relevance of Joule's responses by reducing inaccuracies and hallucinations that can occur when an LLM operates without specific context. 

<br>

* Click the **Apply** button.
<img width="1800" height="852" alt="image" src="https://github.com/user-attachments/assets/df782a69-4811-4c9a-a5ec-03df27ed48ab" />


<br>

* **Save** the Agent.

## Summary — Ex. 4: Create a Joule Agent 🔧

This page explains how to create a **Joule Agent** in SAP Joule and configure it with the previously created **Joule Skills** and relevant document grounding.  
The agent acts as an intelligent assistant that can **create, update, or track shipments** in the **SAP Business Network Global Track and Trace (GTT)** system.

---

### Part 1: Create and Configure the Agent
This section covers creating the agent and defining its core behavior:
- **Expertise** - Defines the agent’s professional focus and domain.
- **Instructions** - Specifies the agent’s primary goals and logic for choosing tools.
- **Additional Context** - Provides tone and behavioral guidance for the agent.

### Part 2: Model and Tool Configuration
- **Model Configuration** ensures a balanced, performant setup for the agent’s reasoning.
- **Joule Skills** are added as tools, enabling the agent to perform specific logistics tasks.
- **Document Grounding** is added as a tool, allowing the agent to reference real carrier data.

<br>

➡️ [Next Exercise - > Ex. 4.1 - Test an Agent in a Private Environment](ex4.1-test-joule-agent.md)
<br> <br>  - [Back To Landing Page](../../README.md)
