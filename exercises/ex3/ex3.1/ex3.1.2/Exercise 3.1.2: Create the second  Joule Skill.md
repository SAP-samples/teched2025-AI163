## Exercise 3.1.2 - <img width="35" height="44" alt="image" src="https://github.com/user-attachments/assets/601b4116-ece9-40ff-8be0-759943cae4ab" /> Create the second Joule Skill
We will now create our second Joule Skill in a similar way as the previous section. 
<br>
> [!Note]
  > - Close the previous open Joule Skill to go to the Overview Page.

### <img width="15" height="25" alt="image" src="https://github.com/user-attachments/assets/4492da9e-a2d9-49d9-a30e-855f7c3663a0" /> Second Joule Skill: Track Shipment 
This Joule Skill is used to create a shipment in the SAP Business Networks GTT System
<br><br>  1: Click on Create button and choose ‘Joule Skill’
<img width="1787" height="717" alt="image" src="https://github.com/user-attachments/assets/70cf8d0d-43c7-4cc8-acb3-5a973d365521" />


<br><br> 2: Enter the name and Description 
<br> - Name: Track Shipment
<br> - Description: A skill to track shipments in the GTT System.
<br> Click on ‘Create’ button
> [!Note]
  > - The Identifier is autopoulated based on the Skill name
<img width="1794" height="847" alt="image" src="https://github.com/user-attachments/assets/1c19b82c-c9cd-4f16-94f2-5daa60592ae4" />


<br><br> 3: Once the Joule skill is created, you are taken to the skill builder
<br> 4: Click on the <img width="18" height="20" alt="image" src="https://github.com/user-attachments/assets/7a9ecb53-0c74-4fcc-a7de-3deec6113ca9" /> button on the right side of the screen to open the skill input and output parameters
<img width="1797" height="733" alt="image" src="https://github.com/user-attachments/assets/6d71c0f2-fa1c-42fc-87c4-a3629fc807a4" />


<br><br>5: Click on the ‘Parameters’ tab and expand the section ‘Skill Inputs’. Click on the ‘Configure’ button to configure the skill inputs.
<img width="1797" height="608" alt="image" src="https://github.com/user-attachments/assets/82ff9a2c-ef7d-4a15-9f1e-b826de24ee88" />


<br><br>6: Click on the 'Add Input' button and add the following Inputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field

| **S.No** | **Name**       | **Identifier**(auto-populated) | **Description**         | **Required** |
|:--------:|----------------|----------------|--------------------------|---------------|
| 1 | trackingID     | trackingiD     | Tracking Number              | ✅ |


<br>Once all inputs are added, click on ‘Apply’ button.
<img width="1791" height="800" alt="image" src="https://github.com/user-attachments/assets/d37a27da-593c-41cc-aef0-96bfc1d154a8" />



<br>7: In the skill builder, click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/5b524e3c-c69c-4494-bf37-73dcfaccb0cb" />button to add the action that was tested earlier
<img width="1798" height="629" alt="image" src="https://github.com/user-attachments/assets/2b1a5fe9-d2d5-4e9e-9264-99dab9e84d4a" />


<br><br>8: Choose the option, ‘Call Action’
<img width="1798" height="783" alt="image" src="https://github.com/user-attachments/assets/53fc53d1-1fe1-4c2a-9d0c-137842180c70" />


<br><br>9: Click on the 'getReadquery" Action which we added in the previous Joule Skill option
<img width="1416" height="673" alt="image" src="https://github.com/user-attachments/assets/520fde66-b76a-494b-8786-1d3f5955a87e" />





<br><br>10: Once the action call is added, click on it so that a right panel opens for adding Input and Output parameters & the Destination variable
<img width="1794" height="757" alt="image" src="https://github.com/user-attachments/assets/aaf37d72-a657-409d-b5c7-dc3bb757b73f" />

<br><br>12: Create a ‘Destination Variable’
<br>Destination variable name : PostToGTT
<br>Description: Destination to create shipment in the GTT System
> [!Note]
  > - Once created, remember to select the destination name from the dropdown and Save your project.

<br>![2025-10-24_11-27-50 (1)](https://github.com/user-attachments/assets/2574b83d-12d3-4dbd-be2d-3f50162b3d98)
