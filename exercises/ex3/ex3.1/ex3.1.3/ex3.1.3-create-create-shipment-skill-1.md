## Ex. 3.1.3 - <img width="35" height="44" alt="image" src="https://github.com/user-attachments/assets/601b4116-ece9-40ff-8be0-759943cae4ab" /> Create your last Joule Skill
We will now create our final Joule Skills 
> [!Note]
  > - Close the previous open Joule Skill to go to the Overview Page.

### <img width="15" height="25" alt="image" src="https://github.com/user-attachments/assets/4492da9e-a2d9-49d9-a30e-855f7c3663a0" /> Final Joule Skill: Create Shipment 
This Joule Skill is used to create a shipment in the SAP Business Networks GTT System
<br><br>  1: Click on Create button and choose ‘Joule Skill’
<img width="3588" height="1162" alt="image" src="https://github.com/user-attachments/assets/0a42f04e-ee81-4246-835a-ba8f1520be20" />



<br><br> 2: Enter the name and Description 
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Name**        | `Create Shipment <UserID>`                  |
| **Description** | `A skill to create shipment or update shipment with ONLY carrier name.During update only carrier is required.` |

* Click on ‘Create’ button
> [!Note]
  > - The Identifier is autopopulated based on the Skill name
<img width="1800" height="721" alt="image" src="https://github.com/user-attachments/assets/0d1108d6-c301-4591-a11d-e7fc7f4d2ad8" />


<br><br> 3: Once the Joule skill is created, you are taken to the Skill builder
<br> 4: Click on the <img width="18" height="20" alt="image" src="https://github.com/user-attachments/assets/7a9ecb53-0c74-4fcc-a7de-3deec6113ca9" /> button on the right side of the screen to open the skill input and output parameters
<img width="1790" height="643" alt="image" src="https://github.com/user-attachments/assets/85646164-311a-47d7-b509-897c005d2db7" />

<br><br>5: Click on the ‘Parameters’ tab and expand the section, ‘Skill Inputs’. Click on ‘Configure’ button to configure the skill inputs.
<img width="3574" height="1286" alt="image" src="https://github.com/user-attachments/assets/20eb33c2-b385-45e6-a331-48c6884dc533" />


<br><br>6: Click on the 'Add Input' button and add the following Inputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field

| **S.No** | **Name**       | **Identifier** | **Description**         | **Required** |
|:--------:|----------------|----------------|--------------------------|---------------|
| 1 | shipmentid     | shipmentid     | Shipment ID              | ✅ Checked|
| 2 | srclocation    | srclocation    | Source Location          | ✅ Checked|
| 3 | destlocation   | destlocation   | Destination Location     | ✅ Checked|
| 4 | datetime       | datetime       | Pick up Date             | ✅ Checked|
| 5 | carrier        | carrier        | carrierid                | ⬜ Unchecked|

* Once all inputs are added, click on ‘Apply’ button.
<img width="1783" height="788" alt="image" src="https://github.com/user-attachments/assets/59a23305-7c8a-4072-8df0-f8f1260d9f83" />

<br>7: In the skill builder, click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/dd09a02b-cd57-409e-91e5-734e03150803" />
 button to add the Action to create shipments.
<img width="1790" height="673" alt="image" src="https://github.com/user-attachments/assets/3c6105a3-e43c-4229-b900-d4c6f1299c41" />

<br><br>8: Choose the option, ‘Call Action’
<img width="1789" height="810" alt="image" src="https://github.com/user-attachments/assets/ef020b5b-54b3-499b-b9b0-6fab00db9f53" />

<br><br>9: Click on the 'Browse All Actions" option
<img width="1775" height="779" alt="image" src="https://github.com/user-attachments/assets/18426b2b-9ab1-4729-bb96-912c67fb9be1" />

<br><br>10: In the search bar, enter ```createshipment``` and press Enter to search for the Action to create a shipment and click on the Add button
<img width="1793" height="915" alt="image" src="https://github.com/user-attachments/assets/9f72cb4b-4b50-457b-960a-b20dabb00093" />

<br><br>11: Once the action call is added, click on it so that a right panel opens to adding Input parameters & the Destination variable
<img width="1794" height="757" alt="image" src="https://github.com/user-attachments/assets/aaf37d72-a657-409d-b5c7-dc3bb757b73f" />

<br><br>12: Create a ‘Destination Variable’

* Click on the Destination Variable input area and select "Create Destination Variable" and provide the inputs below:
<img width="3593" height="1514" alt="image" src="https://github.com/user-attachments/assets/337a2ea8-d516-48ea-a2da-7fedf9d5b657" />


  
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Identifier**        | `PostToGTT`                  |
| **Description** | `Destination to create shipment in the GTT System` |


> [!Note]
  > - Once created, remember to select the destination name from the dropdown and Save your project.

<br>![2025-10-24_11-27-50 (1)](https://github.com/user-attachments/assets/2574b83d-12d3-4dbd-be2d-3f50162b3d98)

* Save your Joule Skill

<br><br>

# Summary — Ex. 3.1.3: Create the Final Joule Skill

This page explains how to create the **final Joule Skill** in the SAP **Joule Skill Package**, named **“Create Shipment.”**  
The purpose of this skill is to **create or update a shipment** in the **SAP Business Network Global Track and Trace (GTT)** system.  
In an update scenario, only the carrier name is required.

The exercise continues from the previous steps and includes the following main actions:

- Creating a new **Joule Skill** called `Create Shipment <UserID>` with a description indicating its purpose for creating or updating shipment details.  
- Defining **input parameters** required to create or update shipments
- Adding a new **action** to create shipments using the **`createshipment`** action.  
- Opening the **Skill Builder** and selecting **“Call Action”** to connect this backend operation.  
- Creating a new **destination variable** named `PostToGTT`, which serves as the connection point to send shipment data to the GTT system.
- Ensuring the destination is saved and correctly selected within the project.  

Once completed, this Joule Skill enables users to **create new shipments** or **update existing ones** within the GTT system via Joule.  
The page concludes with a link to the next exercise, which focuses on mapping the **input variables** of the action project with the Joule Skill inputs.



  
➡️ [Next Exercise - > Ex. 3.1.3a - Mapping Input variables of the Action project with Joule Skill Inputs](ex3.1.3a-create-create-shipment-skill-2.md)
<br> <br>  - [Back To Landing Page](../../../README.md)
