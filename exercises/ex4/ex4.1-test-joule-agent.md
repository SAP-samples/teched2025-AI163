## Ex. 4.1: Test an Agent in Private Environment

<br> Once the Agent is created, you can test it in a Private Environment. 


* Now click on the Agent once again - to test the Agent, follow the below steps:
  
> [!NOTE]
> If this step fails for any reason, refresh the entire page, Open the Agent and try again.

<br>1. Click on the Test button on the right top corner of the Agent Builder.
<br>2. In the pop-up screen, provide the details:

| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Environment**        | `Choose your <_UserID> related Private environment`                  |
| **AICore** | `included-ai-core` |
| **PostToGTT** | `gttwriteservice` |
| **GetFromGTT** | `gttGetService` |

<img width="1790" height="858" alt="image" src="https://github.com/user-attachments/assets/ef0350ed-7d3c-4fe3-bcd9-9ab55a6c54f4" />

* Click on Test
  

<br><br>3. In the Joule Assistant, provide the below prompts to test:

<br>  3.1.  :point_right: **Prompt**: 
<br>```Could you please assist me in creating a Shipment ?```
<br> :full_moon: **Result**: Joule Requests shipment details: Shipment ID, Source Location, Destination Location, Pick up Date. 

<img width="1785" height="811" alt="image" src="https://github.com/user-attachments/assets/84ee5c3b-1328-44c0-b17b-36182cec6a33" />


<br>  3.2:  Provide the requested inputs 
<br>:point_right: **Prompt**:
> [!NOTE]
> Replace < UserID > with your UserID

```
Shipment ID: 61000<UserID>
Source Location: SFO
Destination Location: NYC
Pick-up Date and Time: 2025-10-28T10:00:00Z
```


<br>:full_moon: **Result**: Joule responds with the success message you created earlier along with the shipment number and link to the GTT system 

> [!WARNING]
> You will not be able to directly access the GTT system due to restricted Authorization. Ask your trainer to show you the created shipment in the GTT system. 

<img width="1791" height="813" alt="image" src="https://github.com/user-attachments/assets/c842a81c-a3be-4837-9fee-8045d3090b1b" />


<br><br>
<br>  4: :point_right: **Prompt**: 
<br>```Suggest the best carriers from SFO to NYC```
<br>:full_moon: **Result**: Joule propose the carriers based on the carrier rates document uploaded in AI Core.


<img width="458" height="276" alt="image" src="https://github.com/user-attachments/assets/dd4bb5d9-58a0-4c10-ae10-0eaa77b66dcd" />



<br>  5: :point_right: **Prompt**:
<br> ```I would like to find all the delayed shipments```

<br>:full_moon: **Result**: Joule responds with Display a list of shipments with Delayed status in the GTT system
<img width="580" height="350" alt="image" src="https://github.com/user-attachments/assets/1ecae1c1-2d46-48ef-8a45-b2cc799a8367" />

<br>  6: :point_right: **Prompt**:
> [!NOTE]
> Replace < UserID > with your User Id

```I want to track the shipment 61000<UserID>```



<br>:full_moon: **Result**: Joule responds with tracking info of the shipment in the GTT system

<img width="601" height="481" alt="image" src="https://github.com/user-attachments/assets/2e244478-c62f-4074-97c4-3ccd3af7cb42" />

<br>

## Summary — Ex. 4.1: Test a Joule Agent in a Private Environment

This page explains how to **test the Joule Agent** you created in a **private environment** before deploying it more broadly.  
The testing process ensures the agent correctly interacts with the configured tools, destinations, and document grounding.

---

### 1. Set Up the Test Environment


### 2. Test Scenarios and Prompts


* 🟢 **Scenario 1: Create a Shipment**
* 🟠 **Scenario 2: Suggest Best Carriers**
* 🔵 **Scenario 3: Show Delayed Shipments**
* 🟣 **Scenario 4: Track a Shipment**

### ✅ Outcome

By the end of this exercise, the **Agent for Logistics**:
- Successfully handles shipment creation and updates  
- Suggests carriers intelligently based on AI Core documents  
- Retrieves delayed shipment lists  
- Tracks shipments accurately in GTT  


<br>

➡️ [Next Exercise - > Ex. 5 - Additional Section - Exercise to Release, Deploy and Test the Agent in Shared Environment](../ex5/ex5-release-deploy-test-agent.md)

<br> <br>  - [Back To Landing Page](../../README.md)
