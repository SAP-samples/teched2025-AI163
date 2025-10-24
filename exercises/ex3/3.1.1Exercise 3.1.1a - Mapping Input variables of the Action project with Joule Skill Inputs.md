## Exercise 3.1.1a - Mapping Input variables of the Action project with Joule Skill Inputs
<br> 1: Select the Action in the Skill Builder and click on Inputs tab to map the skill inputs to action call inputs. Click on the field, ‘planning_horizon_from’. The skill content list will open on the left. As the skill inputs are of type, ‘String’ and some of the Action inputs are of type, Date-time, you have to click on ‘Apply a   formula’ in order to map
<br><br><img width="939" height="465" alt="image" src="https://github.com/user-attachments/assets/4fdea1c3-f6b7-437b-8ebe-25a31a107552" />

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

<br> <br>  - [Next Exercise - > Exercise 4.3 - Add a Send Message in Joule Skill](https://github.com/SAP-samples/teched2025-AD169/tree/6d4d185a4dc5c192ce2f65d6a286b84d98ff7772/exercises/ex4/README.md/ex4.3/README.md)
<br><br>Click on the Save button to save the Joule skill.
