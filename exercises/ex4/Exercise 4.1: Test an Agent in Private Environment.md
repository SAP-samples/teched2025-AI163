## Exercise 4.1: Test an Agent in Private Environment
<br> Once the Agent is created, user can test it in a private environment. To test the Agent, follow the below steps:
<br>1: Click on the Test button on the right top corner of the Agent builder.
<br>2: In the pop-up screen, provide the details:
<br>$$\color{blue}{Environment}$$: Choose your __userid_ related environment
<br>$$\color{blue}{AICore}$$: included-ai-core
<br>WHSOPMNG_DEST: zewm-autonomous-warehouse-agent-srv-api
<br><br><img width="940" height="443" alt="image" src="https://github.com/user-attachments/assets/7c153054-35cf-40d0-b88b-d272485faa2f" />
<br>Click on Test
<br><br>3: In the Joule Assistant, provide the below prompts to test:
<br>  3.1: **Prompt**: 
<br>“Could you please assist me in verifying the critical activity areas in terms of workloads for warehouse TSEB for today using 6AM as planning start? in case critical areas exist, only simulate optimal resource allocation”
<br>**Result**: Optimization should be run and rebalanced resources should be displayed.
<br><br><img width="940" height="419" alt="image" src="https://github.com/user-attachments/assets/1665026b-b3cb-44da-8f2b-a4310ba601f1" />

<br>  3.2:  You can use only below prompt to see the critical areas without optimization as well.
<br>**Prompt**:
<br>“Could you please assist me in verifying the critical activity areas in terms of workloads for warehouse TSEB for today using 6AM as planning start?”
<br>**Result**: The result should be provided with 3 critical areas, T010, T151 and T152.
<br><br><img width="940" height="418" alt="image" src="https://github.com/user-attachments/assets/38b85b95-a3ee-4840-8aae-82b566545e91" />

<br> <br>  - [Next Exercise - > Exercise 7 - Additional Section - Exercise to Release, Deploy and Test the Agent in Shared Environment](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex7/README.md)
