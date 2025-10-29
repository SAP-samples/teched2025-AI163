## Ex. 3.1.3a - Mapping Input variables of the Action project with Joule Skill Inputs
<br>

### 1. Mapping Skill Inputs
<br>Select the Action in the Skill Builder and click on Inputs tab to map the skill inputs to action call inputs. 
* Scroll through and locate the fields shown in the table below and click on the fields.
* The skill content list will open on the left.
* As the skill inputs are of type, ‘String’ and some of the Action inputs are of type, Date-time, you have to click on ‘Apply a   formula’ in order to map
<img width="1796" height="810" alt="image" src="https://github.com/user-attachments/assets/3f020e15-329a-4993-a0eb-40c90a2c26e3" />

> [!Note]
  > - Replace the texts in between **<** **>** with the skill input in the expression editor as done in previous sections


| Field Name              | Mapped Path                 | Value |
|--------------------------|-----------------------------|-----------|
| actualBusinessTimestamp  | Apply Formula    | ```DateTimeFromISO(<Skill Input>datetime>)``` |
| altKey                   | Apply Formula| ```ConcatenateStrings(["xri://sap.com/id:LBN#10010002478:EWWCLNT220:FT1_SHIPMENT:", <Skill Input>shipmentId>], ""```)|
| arrivalLocationId        | Skill Inputs > destlocation | |
| departureLocationId      | Skill Inputs > srclocation  | |
| plannedArrivalDateTime   | Static  | ```2025-12-28T10:00:00Z``` |
| plannedDepartureDateTime | Apply Formula   | ```DateTimeFromISO(<Skill Input>datetime>)``` |
| serviceAgentLbnId        | Skill Inputs > carrier      | |
| shipmentNo               | Skill Inputs > shipmentid   | |
<br>

### 2. Create A Condition Branch
<br>We will now create a condition branch in the Skill builder to check if a carrier exists for the shipment (update) or we are creating a fresh shipment without a carrier. 

* In the skill builder click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/dd09a02b-cd57-409e-91e5-734e03150803" /> button *after* the Action step and select 'Condition Check'
<img width="1257" height="762" alt="image" src="https://github.com/user-attachments/assets/e33654c6-648c-4f07-a158-6160fe714308" />

<br>

* Name the step as ```Is Carrierid Empty``` and then click on the Options button and then 'Condition Editor'
<img width="3578" height="1418" alt="image" src="https://github.com/user-attachments/assets/0169c524-ebf6-48cd-b5da-e8837bbfcc2d" />


<br>

* We will now define the contion to check if the carrier id is empty.

* Click on the first input field and select the Skill Input as ```carrier```. Then select ```is empty``` from the next drop down menu. Finally click Apply to save the condition.
<img width="3320" height="1516" alt="image" src="https://github.com/user-attachments/assets/c49f4fa3-ac4b-4362-a82b-a97619ca890e" />

<br><br>
* On the Condition step, click on <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/4f8e276d-28ce-413b-8c99-cc178d5e3064" />
the button to expand the condition and view the condition branches. i.e. Branch 1 and Branch 2
<img width="1531" height="651" alt="image" src="https://github.com/user-attachments/assets/f1ed4f7f-ef72-4dc1-8c2e-f1a085062163" />

* Click on the Save button to save the Joule skill.

# Summary — Ex. 3.1.3a: Mapping Input Variables of the Action Project with Joule Skill Inputs

This page explains how to **map input variables** of the Action project to the corresponding **Joule Skill inputs** for the “Create Shipment” skill created in the previous exercise.  
It also covers how to set up a **conditional branch** within the skill to handle different scenarios based on whether a carrier ID is provided.

---

## 1. Mapping Skill Inputs

In this section, you map the Joule Skill input parameters to the Action’s input fields within the **Skill Builder**.

- Select the Action in the Skill Builder and open the **Inputs** tab.  
- Locate the relevant fields and map them according to the table below.  

## 2. Creating a Condition Branch

This step adds a **Condition Check** to the skill to determine whether the carrier ID field is empty.  
Depending on the result, the skill can take different paths (e.g., create a new shipment or update an existing one).

- In the Skill Builder, click the **+** button after the Action step and choose **Condition Check**.  
- Name the condition step **“Is Carrierid Empty”**.  
- Open the **Condition Editor** and define the condition

Once added, the condition will create two branches:
- **Branch 1** — Executes when the carrier ID is empty  
- **Branch 2** — Executes when the carrier ID is provided  

Finally, click **Save** to store the completed Joule Skill configuration.


<br>
<br>

➡️ [Next Exercise - > Ex. 3.1.3b - Add Send Message steps in Joule Skill](ex3.1.3b-create-create-shipment-skill-3.md)

<br> <br>  - [Back To Landing Page](../../../README.md)
