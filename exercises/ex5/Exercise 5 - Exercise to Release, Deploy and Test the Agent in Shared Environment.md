
## Exercise 5 – Release, Deploy, and Test the Project in a Shared Environment

### ⚙️ Context and Purpose
In the previous exercise, you successfully tested your **Warehouse Workforce Optimization Agent** in a **Private Environment**.  
Now, it’s time to **release and deploy** your project to a **Shared Environment** — enabling collaboration, integration testing, and visibility for other users in the same tenant.

This step finalizes your work, ensuring that your Joule Agent is packaged, deployed, and functioning within the broader environment context.

---

### 🌍 Why This Matters
Releasing and deploying your project to a **Shared Environment** allows:
- Validation of the agent in a **multi-user** and **multi-system** setup.  
- Connection with shared **destinations** and external APIs.  
- End-to-end simulation of **Agentic Warehouse Operations** at scale.  

> 💡 **Good to Know:**  
> When your organization has Joule available in a **shared environment**, this same deployment flow will also apply when moving the project to **Joule in Production**.  
> The deployment process — including version release, environment selection, and destination mapping — follows the **same steps** as described below.


###  :file_folder: Create A Shared Environment
<br>We will first create a Shared Environment for you to deploy your package to. 

Navigate to Control Tower from you build lobby and to the Environments section
<img width="1790" height="790" alt="image" src="https://github.com/user-attachments/assets/4fb77b80-a21f-4b7c-a608-0d098e856dd3" />
<br>Click on the 'Create' button at the top right corner and provide the following inputs, replace the UserId value with your User Id for this exercise:
<br>Environment Name: JouleAgent_UserID
<br>Identifier: *Auto Populated*
<br>Color: Any colour of your choice from the dropdown
<br>Description: 'Environment For Joule Agent- UserID'

<img width="1794" height="478" alt="image" src="https://github.com/user-attachments/assets/c26f5571-ffb0-4df9-94a5-24087602cac5" />
<br>
<img width="1795" height="688" alt="image" src="https://github.com/user-attachments/assets/6974795c-685b-43df-8f10-772e96ce1cf8" />

### 7.1 – Release and Deploy the Project

1. Open your **Project Overview** page in Joule Studio and click **Release**.  
<img width="1785" height="650" alt="image" src="https://github.com/user-attachments/assets/faccf2e2-4d91-48e1-94a6-e76771abcdd2" />


2. Once released, navigate to the **Released Version** of your project and click **Deploy**.  
<img width="1798" height="583" alt="image" src="https://github.com/user-attachments/assets/4203bcc9-071a-417c-9216-763f674d74dc" />


3. In the deployment dialog, select the **Shared Environment** created earlier in your tenant and click **Deploy**.  
<img width="1799" height="576" alt="image" src="https://github.com/user-attachments/assets/b4edd086-1d3b-495d-9548-9102548ee0a0" />



4. Choose the destinations as follows:

   | Destination | Value |
   |--------------|--------|
   | **AICore** | `included-ai-core` |
   | **GetFromGTT** | `gttGetService` |
   | **PostToGTT** | `Cottwriteservice` |

<img width="1790" height="784" alt="image" src="https://github.com/user-attachments/assets/5abf7cf8-ff54-4318-b52b-9f7868c12051" />


5. Click **Deploy**.  
   The project will begin deployment and show as **Deployed** once complete.  
<img width="1779" height="628" alt="image" src="https://github.com/user-attachments/assets/2fce907d-88b7-4819-b523-680e0a79a971" />


---

### 7.2 – Test the Deployed Project in the Shared Environment

1. Navigate to **Control Tower → Environments**.  
<img width="1790" height="790" alt="image" src="https://github.com/user-attachments/assets/4fb77b80-a21f-4b7c-a608-0d098e856dd3" />

2. Search for and open the **Shared Environment** where your project was deployed.  
<img width="1797" height="439" alt="image" src="https://github.com/user-attachments/assets/e2f25742-d7ff-4084-92fd-d627dcb34f2c" />


3. Click on the **Joule** tab.  
4. Click **Launch** to open the **Joule Assistant**.  
5. Enter the same prompts used during testing in the **Private Environment** (see [Exercise 6 – Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex6/README.md)) to validate the behavior in the shared setup.

---

### ✅ Result
You have now:
- Released and deployed your **Warehouse Workforce Optimization Agent** to a shared environment.  
- Verified end-to-end agent behavior with shared API destinations.  
- Confirmed that the same process applies for **Joule Production Deployments**, ensuring consistency across environments.  
- Completed your **Agentic Warehouse Operations** setup, ready for collaborative and scalable use.



---
You’ve now mastered the **complete Joule Agent Lifecycle** — from private design and validation to enterprise-grade deployment

👏 Fantastic work — you’ve officially reached the finish line of this TechEd exercise series

➡️ **Next Step:** [Return to the Exercise Overview](https://github.com/SAP-samples/teched2025-AD169.git)
<br> <br>  - [Back To Landing Page](https://github.com/SAP-samples/teched2025-AI163/blob/main/README.md)
