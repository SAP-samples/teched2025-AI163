
## Ex. 5 – Release, Deploy, and Test the Project in a Shared Environment

### ⚙️ Context and Purpose
In the previous exercise, you successfully tested your **Logistics Agent** in a **Private Environment**. Now, it’s time to **release and deploy** your project to a **Shared Environment** — enabling collaboration, integration testing, and visibility for other users in the same tenant.

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


### Part 1: Create a Shared Environment
We will first create a Shared Environment for you to deploy your package to. 

1. Navigate to **Control Tower** from your SAP Build lobby and go to the **Environments** section.
<img width="1790" height="790" alt="image" src="https://github.com/user-attachments/assets/4fb77b80-a21f-4b7c-a608-0d098e856dd3" />

2. Click on the **Create** button at the top right corner and provide the following inputs, replacing `<UserID>` with your assigned ID:

| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Environment Name** | `JouleAgent_<UserID>` |
| **Identifier**        | Auto Populated                |
| **Color** | Any colour of your choice from the dropdown|
| **Description** | `Environment For Joule Agent - <UserID>`|

<img width="1794" height="478" alt="image" src="https://github.com/user-attachments/assets/c26f5571-ffb0-4df9-94a5-24087602cac5" />
<br>
<img width="1795" height="688" alt="image" src="https://github.com/user-attachments/assets/6974795c-685b-43df-8f10-772e96ce1cf8" />

---

### Part 2: Release and Deploy the Project

1. Open your **Project Overview** page in Joule Studio and click **Release**.  
<img width="1785" height="650" alt="image" src="https://github.com/user-attachments/assets/faccf2e2-4d91-48e1-94a6-e76771abcdd2" />

2. Once released, navigate to the **Released Version** of your project and click **Deploy**.  
<img width="1798" height="583" alt="image" src="https://github.com/user-attachments/assets/4203bcc9-071a-417c-9216-763f674d74dc" />

3. In the deployment dialog, select the **Shared Environment** you just created and click **Deploy**.  
<img width="1799" height="576" alt="image" src="https://github.com/user-attachments/assets/b4edd086-1d3b-495d-9548-9102548ee0a0" />

4. In the next step, map the destinations as follows:

   | Destination | Value |
   |--------------|--------|
   | **AICore** | `included-ai-core` |
   | **GetFromGTT** | `gttGetService` |
   | **PostToGTT** | `gttwriteservice` |

<img width="1790" height="784" alt="image" src="https://github.com/user-attachments/assets/5abf7cf8-ff54-4318-b52b-9f7868c12051" />

5. Click **Deploy**.
  
> [!NOTE]
> If this step fails for any reason, refresh the entire page and try again.

   The project will begin deployment and show as **Deployed** once complete.  
<img width="1779" height="628" alt="image" src="https://github.com/user-attachments/assets/2fce907d-88b7-4819-b523-680e0a79a971" />


---

### Part 3: Test in the Shared Environment

1. Navigate to **Control Tower → Environments**.  
<img width="1790" height="790" alt="image" src="https://github.com/user-attachments/assets/4fb77b80-a21f-4b7c-a608-0d098e856dd3" />

2. Search for and open the **Shared Environment** where your project was deployed.  
<img width="1797" height="439" alt="image" src="https://github.com/user-attachments/assets/e2f25742-d7ff-4084-92fd-d627dcb34f2c" />

3. Click on the **Joule** tab, then click **Launch** to open the **Joule Assistant**.
> [!NOTE]
> If you do not see the Joule tab, it may be hidden due to yur screen resolution. Click the menu button to the right (3 vertical dots) to find the **Joule tab**.

4. Enter the same prompts used during private testing (see [Ex. 4.1](../ex4/ex4.1-test-joule-agent.md)) to validate the behavior.

<img width="1795" height="502" alt="image" src="https://github.com/user-attachments/assets/00e848fa-a6d5-4f19-8351-4dcdba54de0c" />

---

### ✅ Result
You have now:
- Released and deployed your **Logistics Agent** to a shared environment.  
- Verified end-to-end agent behavior with shared API destinations.  
- Confirmed that the same process applies for **Joule Production Deployments**, ensuring consistency across environments.  
- Completed your **Logistics Agent** setup, ready for collaborative and scalable use.



---
You’ve now mastered the **complete Joule Agent Lifecycle** — from private design and validation to enterprise-grade deployment.

👏 **Fantastic work — you’ve officially reached the finish line of this TechEd exercise series!**

<br> <br>  - [Back To Landing Page](../../README.md)