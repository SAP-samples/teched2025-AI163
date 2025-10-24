## Exercise 3.1 - <img width="35" height="44" alt="image" src="https://github.com/user-attachments/assets/601b4116-ece9-40ff-8be0-759943cae4ab" /> Create a new Joule Skill
We will now create our Joule Skills within the Joule Skill Package.
<br><br>For this hands-on, we will be creating a total of: 
  <br> - 3 Joule Skills.
  <br> - 1 Joule Agent which uses these skills as **tools** along with Document Grounding. 

### <img width="15" height="25" alt="image" src="https://github.com/user-attachments/assets/4492da9e-a2d9-49d9-a30e-855f7c3663a0" /> First Joule Skill: Create Shipment 
This Joule Skill is used to create a shipment in the SAP Business Networks GTT System
<br><br>  1: Click on Create button and choose ‘Joule Skill’
<img width="1785" height="799" alt="image" src="https://github.com/user-attachments/assets/25e74b71-36b3-4310-8afd-dd0af40f102a" />

<br><br> 2: Enter the name and Description 
<br> - Name: Create Shipment
<br> - Description: A skill to create shipment or update shipment with ONLY carrier name.During update only carrier is required.
<br> Click on ‘Create’ button
> [!Note]
  > - The Identifier is autopoulated based on the Skill name
<img width="1794" height="670" alt="image" src="https://github.com/user-attachments/assets/f973ea8e-fbf4-4cb6-a84a-5adbbf5fc0b8" />

<br><br> 3: Once the Joule skill is created, you are taken to the skill builder
<br> 4: Click on the <img width="18" height="20" alt="image" src="https://github.com/user-attachments/assets/7a9ecb53-0c74-4fcc-a7de-3deec6113ca9" /> button on the right side of the screen to open the skill input and output parameters
<img width="1790" height="643" alt="image" src="https://github.com/user-attachments/assets/85646164-311a-47d7-b509-897c005d2db7" />

<br><br>5: Click on the ‘Parameters’ tab and expand the section, ‘Skill Inputs’. Click on ‘Configure’ button to configure the skill inputs.
<img width="1787" height="643" alt="image" src="https://github.com/user-attachments/assets/65d0c9ab-11cd-4e34-81ce-b568501c2313" />

<br><br>6: Click on the 'Add Input' button and add the following Inputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field

| **S.No** | **Name**       | **Identifier** | **Description**         | **Required** |
|:--------:|----------------|----------------|--------------------------|---------------|
| 1 | shipmentid     | shipmentid     | Shipment ID              | ✅ |
| 2 | srclocation    | srclocation    | Source Location          | ✅ |
| 3 | destlocation   | destlocation   | Destination Location     | ✅ |
| 4 | datetime       | datetime       | Pick up Date             | ✅ |
| 5 | carrier        | carrier        | carrierid                | ⬜ (not required) |

<br><br> Once all inputs are added, click on ‘Apply’ button.
<img width="1783" height="788" alt="image" src="https://github.com/user-attachments/assets/59a23305-7c8a-4072-8df0-f8f1260d9f83" />

<br>7: In the skill builder, click on the ‘+’ button to add the action that was tested earlier
<img width="1790" height="673" alt="image" src="https://github.com/user-attachments/assets/3c6105a3-e43c-4229-b900-d4c6f1299c41" />

<br><br>8: Choose the option, ‘Call Action’
<img width="1789" height="810" alt="image" src="https://github.com/user-attachments/assets/ef020b5b-54b3-499b-b9b0-6fab00db9f53" />

<br><br>9: Click on the 'Browse All Actions" option
<img width="1775" height="779" alt="image" src="https://github.com/user-attachments/assets/18426b2b-9ab1-4729-bb96-912c67fb9be1" />

<br><br>10: In the search bar, enter 'createshipment' and press Enter to search for the Action to create a shipment and click on the Add button
<img width="1793" height="915" alt="image" src="https://github.com/user-attachments/assets/9f72cb4b-4b50-457b-960a-b20dabb00093" />

<br><br>11: Once the action call is added, click on it so that a right panel opens for adding Input and Output parameters & the Destination variable
<img width="1794" height="757" alt="image" src="https://github.com/user-attachments/assets/aaf37d72-a657-409d-b5c7-dc3bb757b73f" />

<br><br>12: Create a ‘Destination Variable’
<br>Destination variable name : PostToGTT
<br>Description: Destination to create shipment in the GTT System
> [!Note]
  > - Once created, remember to select the destination name from the dropdown and Save your project.

<br>![2025-10-24_11-27-50 (1)](https://github.com/user-attachments/assets/2574b83d-12d3-4dbd-be2d-3f50162b3d98)


  
<br> <br>  - [Next Exercise - > Exercise 3.2 - Mapping Input variables of the Action project with Joule Skill Inputs](https://github.com/SAP-samples/teched2025-AI163/blob/main/exercises/ex3/ex3.2/Exercise%203.2%20-%20Mapping%20Input%20variables%20of%20the%20Action%20project%20with%20Joule%20Skill%20Inputs.md)
