## Exercise 3.0 - :new: Create a new Joule Skill Package
<br> 1: Open the SAP Build Lobby.
<br> 2: Click on the **Create** Button 
<img width="1794" height="740" alt="image" src="https://github.com/user-attachments/assets/baa3d4e4-458b-4e39-bae4-8647926c952c" />

<br><br> 3: On the next screen Select the **Joule Skill** tile, then choose Next.
<img width="1967" height="1238" alt="image" src="https://github.com/user-attachments/assets/ba884ee2-8ee2-406f-ba6f-613b01abf43d" />


<br><br> 4: Enter the name and Description of the Package
<br> - Name: Logistics Agent UserId
<br> - Description: Create shipments in GTT from Joule
> :exclamation:Replace UserId with you username to easily identify your package in the SAP Build Studio Lobby

<br> 5: Click on Review to review your inputs followed by the ‘Create’ button

![2025-10-24_07-50-43 (3)](https://github.com/user-attachments/assets/06387725-d200-48f6-8100-001f2931215d)

#### :fire: Your Package will now open in a new tab
<img width="1790" height="835" alt="image" src="https://github.com/user-attachments/assets/53298342-4a0b-455f-9774-1ae527353515" />



<br><br> 3: Once the Joule skill is created, click on the Joule skill to open the skill builder
<br> 4: Click on the ‘<<’ button on the right side of the screen to open the skill input and output parameters
<br><br> <img width="940" height="291" alt="image" src="https://github.com/user-attachments/assets/c63337c3-a533-4700-b1d0-a8db7c061a1e" />
<br><br>5: Click on the ‘Parameters’ tab and expand the section, ‘Skill Inputs’. Click on ‘Configure’ button to configure the skill inputs.
<br> <img width="940" height="388" alt="image" src="https://github.com/user-attachments/assets/8f6aa26c-46a3-4cd9-a87d-31dcb0ae9766" />
<br><br>6: Add the following Inputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field
<br><br>
<table>
  <tr>
    <th>Serial Number</th>
    <th>Name</th>
    <th>Description</th>
    <th>Required</th>
  </tr>
  <tr>
    <td>1</td>
    <td>IsSimulation</td>
    <td>Flag to check the simulation</td>
    <td>Checked</td>
  </tr>
  <tr>
    <td>2</td>
    <td>PlanningStart</td>
    <td>Planning start date and time convert to UTC</td>
    <td>Checked</td>
  </tr>
  <tr>
    <td>3</td>
    <td>PlanningFrom</td>
    <td>Planning from date and time convert to UTC</td>
    <td>Checked</td>
  </tr>
  <tr>
    <td>4</td>
    <td>PlanningTo</td>
    <td>Planning to date and time convert to UTC</td>
    <td>Checked</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Warehouse</td>
    <td>Warehouse</td>
    <td>Checked</td>
  </tr>
</table>
<br><br> Once added the inputs, click on ‘Save’ button.
<br>7: In the skill builder, click on the ‘+’ button to add the action that was tested in Exercise 1
<br><br><img width="940" height="248" alt="image" src="https://github.com/user-attachments/assets/b56990ed-b7d8-4430-a140-29555acc73ad" />
<br><br>8: Choose the option, ‘Call Action’
<br><br><img width="940" height="376" alt="image" src="https://github.com/user-attachments/assets/ee7f5db5-0687-4c98-84a2-1d486c875d1b" />
<br><br>9: From the list of actions displayed, choose the action ‘Invokes action optimizeWorkload’
<br><br><img width="940" height="604" alt="image" src="https://github.com/user-attachments/assets/d636dbf1-a4e3-4513-91e8-8ed9ef3207ee" />
<br><br>10: Once the action call is added, click on it so that a right panel opens for adding Input and Output parameters
<br><br><img width="940" height="387" alt="image" src="https://github.com/user-attachments/assets/9bc994c2-9057-48f7-bcd1-5c7f00fad8f6" />
<br><br>11: Add a ‘Destination Variable’, which is already pre-created in the project.
Destination variable name : WHSOPMNG_DEST
<br><br><img width="940" height="364" alt="image" src="https://github.com/user-attachments/assets/40be0237-f80a-45e7-be6a-d2924e982e19" />

  
<br> <br>  - [Next Exercise - > Exercise 4.2 - Mapping Input variables of the Action project with Joule Skill Inputs](https://github.com/SAP-samples/teched2025-AD169/tree/6d4d185a4dc5c192ce2f65d6a286b84d98ff7772/exercises/ex4/README.md/ex4.2/README.md)
