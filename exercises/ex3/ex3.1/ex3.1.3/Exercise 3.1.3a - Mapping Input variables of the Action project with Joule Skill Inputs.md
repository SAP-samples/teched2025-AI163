## Exercise 3.1.3a - Mapping Input variables of the Action project with Joule Skill Inputs
<br> 1: Select the Action in the Skill Builder and click on Inputs tab to map the skill inputs to action call inputs. Scroll through and locate the fields shown in the table below and click on the fields. The skill content list will open on the left. As the skill inputs are of type, ‘String’ and some of the Action inputs are of type, Date-time, you have to click on ‘Apply a   formula’ in order to map
<img width="1796" height="810" alt="image" src="https://github.com/user-attachments/assets/3f020e15-329a-4993-a0eb-40c90a2c26e3" />
> [!Note]
  > - Replace the texts in $${\color{red}Red}$$ with the skill input in the expression editor as done in previous sections

| Field Name              | Mapped Path                 | Value |
|--------------------------|-----------------------------|-----------|
| actualBusinessTimestamp  | Apply Formula    | DateTimeFromISO($${\color{red}Skill Input>datetime}$$) |
| altKey                   | Apply Formula| ConcatenateStrings(["xri://sap.com/id:LBN#10010002478:EWWCLNT220:FT1_SHIPMENT:", $${\color{red}Skill Input>shipmentid}$$], "")|
| arrivalLocationId        | Skill Inputs > destlocation | |
| departureLocationId      | Skill Inputs > srclocation  | |
| plannedArrivalDateTime   | Static  | 2025-12-28T10:00:00Z |
| plannedDepartureDateTime | Apply Formula   | DateTimeFromISO($${\color{red}Skill Input>datetime}$$) |
| serviceAgentLbnId        | Skill Inputs > carrier      | |
| shipmentNo               | Skill Inputs > shipmentid   | |
<br>

### Create A Condition Branch
<br>We will now create a condition branch in the Skill builder to check if a carrier exists for the shipment (update) or we are creating a fresh shipment without a carrier. 

<br>In the skill builder click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/dd09a02b-cd57-409e-91e5-734e03150803" /> button *after* the Action step and select 'Condition Check'
<img width="1257" height="762" alt="image" src="https://github.com/user-attachments/assets/e33654c6-648c-4f07-a158-6160fe714308" />

<br>Name the step as 'Is Carrierid Empty' and then click on the Options button and then 'Condition Editor'
<img width="1789" height="709" alt="image" src="https://github.com/user-attachments/assets/57eb1a05-9536-49cb-bbc5-b769495333c0" />
<br><br>We will now define the contion to check if the carrier id is empty.
<br><br> Click on the first input field and select the Skill Input as 'carrier'. Then select 'is empty' from the next drop down menu. Finally click Apply to save the condition.
<img width="1660" height="758" alt="image" src="https://github.com/user-attachments/assets/8fa48c2a-0b5c-4262-a472-6c1631370313" />
<br><br>
On the Condition step, click on <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/4f8e276d-28ce-413b-8c99-cc178d5e3064" />
the button to expand the condition and view the condition branches. i.e. Branch 1 and Branch 2
<img width="1531" height="651" alt="image" src="https://github.com/user-attachments/assets/f1ed4f7f-ef72-4dc1-8c2e-f1a085062163" />

<br><br>Click on the Save button to save the Joule skill.

<br> <br>  - [Next Exercise - > Exercise 3.1.3b - Add Send Message steps in Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.3/Exercise%203.1.3b:%20Add%20a%20Condition%20and%20Send%20message%20in%20Joule%20Skill.md)

<br> <br>  - [Back To Landing Page](https://github.com/SAP-samples/teched2025-AI163/blob/main/README.md)
