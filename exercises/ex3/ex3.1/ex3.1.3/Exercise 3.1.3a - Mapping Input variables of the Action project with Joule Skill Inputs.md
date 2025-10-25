## Exercise 3.1.3a - Mapping Input variables of the Action project with Joule Skill Inputs
<br> 1: Select the Action in the Skill Builder and click on Inputs tab to map the skill inputs to action call inputs. Scroll through and locate the fields shown in the table below and click on the fields. The skill content list will open on the left. As the skill inputs are of type, ‘String’ and some of the Action inputs are of type, Date-time, you have to click on ‘Apply a   formula’ in order to map
<img width="1796" height="810" alt="image" src="https://github.com/user-attachments/assets/3f020e15-329a-4993-a0eb-40c90a2c26e3" />


| Field Name              | Mapped Path                 | Data Type |
|--------------------------|-----------------------------|-----------|
| actualBusinessTimestamp  | Skill Inputs > datetime     | datetime  |
| altKey                   | Expression                  | Expression|
| arrivalLocationId        | Skill Inputs > destlocation | Text      |
| departureLocationId      | Skill Inputs > srclocation  | Text      |
| plannedArrivalDateTime   | Static: 2025-12-21T00:00:00+08:00 | datetime |
| plannedDepartureDateTime | Skill Inputs > datetime     | datetime  |
| serviceAgentLbnId        | Skill Inputs > carrier      | Text      |
| shipmentNo               | Skill Inputs > shipmentid   | Text      |

<br><br><img width="940" height="368" alt="image" src="https://github.com/user-attachments/assets/22cbc3bb-e60d-4d51-97d3-7262078e5482" />

<br><br>Here, type 'PlanningFrom' in the formula editor 
<br><br><img width="940" height="386" alt="image" src="https://github.com/user-attachments/assets/01426f05-ccfc-462a-8a9e-674f658b10fe" />

<br><br>Click on Apply button
<br><br><img width="940" height="541" alt="image" src="https://github.com/user-attachments/assets/015e3fcd-d755-40a8-933d-6fc89a1ab869" />

<br>Similarly map the below fields
<br>
<table>
  <tr>
    <th>Action Inputs</th>
    <th>Skill Content / Skill Input Variables</th>
   </tr>
  <tr>
    <td>planning_horizon_to</td>
    <td>PlanningTo</td>
    </tr>
  <tr>
    <td>planning_start</td>
    <td>PlanningStart</td>
   </tr>
</table>
<br><br>2: Click on the field, ‘is_simulation’ and ‘Apply a formula’.
<br>In the ‘Functions’ section, expand ‘Boolean functions’ and choose ‘ValuesAreEqual’. Then click on ‘Insert’ button.
<br><br><img width="940" height="466" alt="image" src="https://github.com/user-attachments/assets/0af0a409-99a9-4443-893e-61cd2615e6e6" />

<br><br>Add the values in the bracket as ("true", "true")
<br>Click on the Apply button
<br><br><img width="940" height="509" alt="image" src="https://github.com/user-attachments/assets/bfd812f5-6a73-4bea-b1ae-bd3e1759a5d2" />

<br><br>3: Map the variable ‘Warehouse’ with skill input ‘Warehouse’
<br><br><img width="939" height="418" alt="image" src="https://github.com/user-attachments/assets/55821163-09bd-434b-b91f-c5f35842bdc9" />

<br> <br>  - [Next Exercise - > Exercise 3.1.3b - Add a Condition and Send Message in Joule Skill](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.1/ex3.1.3/Exercise%203.1.3b:%20Add%20a%20Condition%20and%20Send%20message%20in%20Joule%20Skill.md)
<br><br>Click on the Save button to save the Joule skill.
