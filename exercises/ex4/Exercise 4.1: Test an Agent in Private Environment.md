## Exercise 4.1: Test an Agent in Private Environment
<br> Once the Agent is created, user can test it in a private environment. 

<br>Before we begin testing, we need to creat an Destination Environment variable for Ai Core. 
<br>Click the Settings icon in the top-right corner of the agent page, as shown in the screenshot:
<img width="1798" height="670" alt="image" src="https://github.com/user-attachments/assets/399ac844-ddcb-4fe4-9e45-9ae6628d5144" />

<br>Click on 'Environment Variables' and then the Create button

<img width="1783" height="798" alt="image" src="https://github.com/user-attachments/assets/989661f9-aea0-469f-9580-90a214749c47" />

<br>Input the following Values 
<br>-Identifier: AiCore
<br>-Description: Destination for AI Core 
<br>-Type: Destination
<img width="1781" height="799" alt="image" src="https://github.com/user-attachments/assets/5139c4b5-d540-4266-9c41-3e8b3071d400" />

<br>Now click on the Agent once again - to test the Agent, follow the below steps:
<br>1: Click on the Test button on the right top corner of the Agent builder.
<br>2: In the pop-up screen, provide the details:
<br>$$\color{blue}{Environment}$$: Choose your __userid_ related environment
<br>$$\color{blue}{AICore}$$: included-ai-core
<br>PostToGTT: gttwriteservice
<br>GetFromGTT: gttGetService
<img width="1790" height="858" alt="image" src="https://github.com/user-attachments/assets/ef0350ed-7d3c-4fe3-bcd9-9ab55a6c54f4" />

<br>Click on Test

<br><br>3: In the Joule Assistant, provide the below prompts to test:
<br>  3.1: **Prompt**: 
<br>“Could you please assist me in creating a Shipment ?"
<br>**Result**:Joule Requests shipment details: Shipment ID, Source Location, Destination Location, Pick up Date. 

<img width="1785" height="811" alt="image" src="https://github.com/user-attachments/assets/84ee5c3b-1328-44c0-b17b-36182cec6a33" />


<br>  3.2:  Provide the requested inputs 
<br>**Prompt**:
"
Shipment ID: 610005250
Source Location: SFO
Destination Location: NYC
Pick-up Date and Time: 2025-10-26T16:58:01Z
"

<br>**Result**: Joule responds with the success message you created earlier along with the shipment number and link to the GTT system 
<img width="1791" height="813" alt="image" src="https://github.com/user-attachments/assets/c842a81c-a3be-4837-9fee-8045d3090b1b" />




<br><br>4: In the Joule Assistant, provide the below prompts to test:
<br>  3.1: **Prompt**: 
<br>“Suggest the best carriers from SFO to NYC”
<br>**Result**:Joule propose the carriers based on the carrier rates document uploaded in AI Core.
. 

<img width="458" height="276" alt="image" src="https://github.com/user-attachments/assets/dd4bb5d9-58a0-4c10-ae10-0eaa77b66dcd" />



<br>  4.2:  Provide the requested inputs 
<br>**Prompt**:
"
Shipment ID: 610005250
Source Location: SFO
Destination Location: NYC
Pick-up Date and Time: 2025-10-26T16:58:01Z
"

<br>**Result**: Joule responds with the success message you created earlier along with the shipment number and link to the GTT system 
<img width="1791" height="813" alt="image" src="https://github.com/user-attachments/assets/c842a81c-a3be-4837-9fee-8045d3090b1b" />



<br> <br>  - [Next Exercise - > Exercise 7 - Additional Section - Exercise to Release, Deploy and Test the Agent in Shared Environment](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex5/Exercise%205%20-%20Exercise%20to%20Release,%20Deploy%20and%20Test%20the%20Agent%20in%20Shared%20Environment.md)
