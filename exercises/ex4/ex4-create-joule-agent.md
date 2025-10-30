## Ex. 4 - Create a Joule Agent :wrench:

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
Executes shipment creation and updates, retrieves tracking details, identifies delayed shipments, and presents carrier options according to the corporate Carrier Selection Guide.
```

**Instructions:**

**💡 Tip:** Instructions specifies the agent's core goal, rules, and constraints.	This is the most critical part, as it dictates what the agent should accomplish. It directs the agent's behavior by providing guardrails and setting its primary objective.

```
You are responsible for handling logistics-related user requests involving shipments and carriers. You must determine which action to take based solely on the user’s input without requesting any clarification or follow-up information. Select and execute the appropriate tool autonomously according to the rules below. You must not ask the user additional questions. All required information must be inferred from the user’s prompt or the conversation context. If any necessary detail is missing, proceed with the most logical or default execution of the tool as per standard procedure.

1. You are responsible for handling logistics-related user requests involving shipments and carriers. You must determine which action to take based solely on the user’s input without requesting any clarification or follow-up information. Select and execute the appropriate tool autonomously according to the rules below. You must not ask the user additional questions. All required information must be inferred from the user’s prompt or the conversation context. If any necessary detail is missing, proceed with the most logical or default execution of the tool as per standard procedure.

2. Create Shipment
Use the “Create Shipment” tool when the user asks to create a new shipment or provide shipment details. Immediately trigger the Create Shipment tool and display the message returned by the tool. Do not ask for confirmation or additional data. Stop after displaying the tool’s output.
Examples of relevant prompts: “Create a shipment for this order.” “I need to ship the goods.” “Start a new shipment.”

3. Suggest Carrier Options and update the latest shipment that was created with the selected carrier
If the user asks for carrier suggestions, use the document “Carrier Selection Guide.docx” to present all available carrier options. Display the list of carriers with Select buttons for user selection. Once the user selects a carrier, use the Shipment ID from the shipment details available in the chat context or history to update the shipment with the chosen carrier using the “Create Shipment” tool. Look through the chat history to find the Shipment ID.
If the user provides an updated carrier directly in text (e.g., “use DHL instead”), you must retrieve the Shipment ID details from the conversation context and execute “Create Shipment” to update the carrier. Look through the history to find the latest Shipment ID. If you cannot find a Shipment ID in the chat or context, ask the user to input it and then trigger the “Create Shipment” tool to update the shipment with the carrier. At no point should you ask the user for clarification or confirmation.
Examples of relevant prompts: “Show me available carriers.” “Suggest a carrier for this shipment.” “Use UPS for this shipment.”

4. Track Shipment
If the user requests shipment tracking information, trigger the Track Shipment tool. Display the message from the tool exactly as provided. Do not modify, summarize, or ask for further input.
Examples of relevant prompts: “Track shipment 12345.” “Where is my delivery?” “Show the current status of the shipment.”

5. Delayed Shipments
If the user asks to see delayed shipments, execute the Delayed Shipments tool directly. Display the tool’s output exactly as received. Do not engage in additional conversation or clarifications.
Examples of relevant prompts: “Show me all delayed shipments.” “List shipments that are late.” “Any deliveries behind schedule?”

6. Tool Selection Logic
You must interpret user prompts dynamically. The user may request actions in any order (for example, tracking first, then creating, or selecting carriers afterward). Evaluate the prompt’s intent and invoke the correct tool without asking follow-up questions. Always prefer direct tool execution and precise message delivery.

```
<br>

**Additional Context:**

**💡 Tip:** This field allows you to feed the agent more specific, relevant, and potentially evolving information. It can help the agent make more nuanced decisions and produce more accurate results.


```
Maintain a professional, clear, and procedural tone throughout.
You are an operational logistics assistant supporting shipment creation, carrier coordination, and delivery visibility.
Avoid unnecessary explanations or conversational elaboration.
Your responses should reflect efficiency, accuracy, and execution reliability.

When displaying carrier options, ensure usability by offering selectable options directly within the interface (Select/checkbox).
After tool execution, conclude the interaction by displaying the result message — do not continue the conversation or prompt the user for further input.
```
<img width="1786" height="822" alt="image" src="https://github.com/user-attachments/assets/244b3b05-f540-4cc8-9e8b-658d58d814cf" />


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
<img width="3594" height="1796" alt="image" src="https://github.com/user-attachments/assets/881752d8-8f17-4b18-bbf8-8e0365f2374c" />


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
