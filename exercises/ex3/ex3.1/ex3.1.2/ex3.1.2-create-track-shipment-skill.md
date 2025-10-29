## Ex. 3.1.2 - <img width="35" height="44" alt="image" src="https://github.com/user-attachments/assets/601b4116-ece9-40ff-8be0-759943cae4ab" /> Create the second Joule Skill
We will now create our second Joule Skill in a similar way as the previous section. 
<br>
> [!Note]
  > - Close the previous open Joule Skill to go to the Overview Page.

### <img width="15" height="25" alt="image" src="https://github.com/user-attachments/assets/4492da9e-a2d9-49d9-a30e-855f7c3663a0" /> Second Joule Skill: Track Shipment 
This Joule Skill is used to track a shipment in the SAP Business Networks GTT System
<br><br>  1: Click on Create button and choose ‘Joule Skill’
<img width="3574" height="1434" alt="image" src="https://github.com/user-attachments/assets/a492019e-f68d-4754-82dd-33cbe3aa1524" />



<br><br> 2: Enter the name and Description 
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Name**        | `Track Shipment`                  |
| **Description** | `A skill to track shipments in the GTT System.` |

* Click on ‘Create’ button
  
> [!Note]
  > - The Identifier is autopopulated based on the Skill name
<img width="1794" height="847" alt="image" src="https://github.com/user-attachments/assets/1c19b82c-c9cd-4f16-94f2-5daa60592ae4" />


<br><br> 3: Once the Joule skill is created, you are taken to the skill builder
<br> 4: Click on the <img width="18" height="20" alt="image" src="https://github.com/user-attachments/assets/7a9ecb53-0c74-4fcc-a7de-3deec6113ca9" /> button on the right side of the screen to open the skill input and output parameters
<img width="1797" height="733" alt="image" src="https://github.com/user-attachments/assets/6d71c0f2-fa1c-42fc-87c4-a3629fc807a4" />


<br><br>5: Click on the ‘Parameters’ tab and expand the section ‘Skill Inputs’. Click on the ‘Configure’ button to configure the skill inputs.
<img width="3594" height="1216" alt="image" src="https://github.com/user-attachments/assets/a036c07a-277e-400b-a2ac-7a163e05a23c" />



<br><br>6: Click on the 'Add Input' button and add the following Inputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field

| **S.No** | **Name**       | **Identifier**(auto-populated) | **Description**         | **Required** |
|:--------:|----------------|----------------|--------------------------|---------------|
| 1 | trackingID     | trackingiD     | Tracking Number              | ✅ |


* Once all inputs are added, click on ‘Apply’ button.
<img width="1791" height="800" alt="image" src="https://github.com/user-attachments/assets/d37a27da-593c-41cc-aef0-96bfc1d154a8" />



<br>7: In the skill builder, click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/5b524e3c-c69c-4494-bf37-73dcfaccb0cb" />button to add the action that was tested earlier
<img width="1798" height="629" alt="image" src="https://github.com/user-attachments/assets/2b1a5fe9-d2d5-4e9e-9264-99dab9e84d4a" />


<br><br>8: Choose the option, ‘Call Action’
<img width="1798" height="783" alt="image" src="https://github.com/user-attachments/assets/53fc53d1-1fe1-4c2a-9d0c-137842180c70" />


<br><br>9: Click on the 'getReadquery" Action which we added in the previous Joule Skill option
<img width="1416" height="673" alt="image" src="https://github.com/user-attachments/assets/520fde66-b76a-494b-8786-1d3f5955a87e" />





<br><br>10: Once the action call is added, click on it so that a right panel opens for mapping Input parameters & creating the Destination variable to read data from the GTT system
<img width="1788" height="621" alt="image" src="https://github.com/user-attachments/assets/31ebab5c-47fb-47fa-b565-2488f0f553df" />



<br><br>11: Since we are again reading shipment from the GTT system, we will reuse the same Destination variable 'GetFromGTT'


<img width="1794" height="738" alt="image" src="https://github.com/user-attachments/assets/c81d074b-f3cf-4d89-874d-92fc068b65b3" />


<br><br>12: We will now add filter criteria as input to Action to fetch the delayed shipments. Click on the Action and select the Input tab on the right pane. 
* Click on the $filter input area and select the <img width="100" height="25" alt="image" src="https://github.com/user-attachments/assets/97985dd3-212e-4ea3-9a00-a61302b9107b" /> option which will take you to the Formula Editor.
<img width="1790" height="679" alt="image" src="https://github.com/user-attachments/assets/ad14784f-f1b7-4e04-9ff7-075224d5de99" />


* Input `ConcatenateStrings(["trackingId eq ", [Tracking ID], ""], "'")` in the Formula Editor. Replace [Tracking ID] with the trackingID Input from the left pane by double clicking on it and click on 'Apply'
<img width="1791" height="835" alt="image" src="https://github.com/user-attachments/assets/3bb0b34c-9e2c-4625-8199-32184c776661" />
<br>

![Formula](https://github.com/user-attachments/assets/dcf60744-c3ff-4c87-8e76-658cdaea960e)




<br><br>13: Finally, we will now create  output parameters for the Joule Skill and map the Action output to them. 
<br>Click anywhere in the Skill Builder's grey area and click on the <img width="25" height="25" alt="image" src="https://github.com/user-attachments/assets/ee9b22ee-e035-4324-8cda-e9a8c43a4e84" /> button on the right to show the Skill meta data
<img width="1791" height="680" alt="image" src="https://github.com/user-attachments/assets/6f0cc684-7825-45d2-8a25-79da1caf5e6c" />


* Click on the Parameters tab to show the Input & Output parameters.
* Click on the Configure button next to the Skill Outputs
  
<img width="1798" height="643" alt="image" src="https://github.com/user-attachments/assets/77841505-85e8-4b58-be6b-c2f9ff2bc5fe" />

* Click on the 'Add Ouput' button and add the following Ouputs with Description. 
> [!Note]
  > - All the Identifiers are entered automatically and will be same as ‘Name’ field

| **S.No** | **Name**          | **Identifier**     | **Description**     | **Type** | **Required** | **List** |
|:--------:|-------------------|--------------------|---------------------|-----------|---------------|-----------|
| 1 | gttstatus        | gttstatus        | Status              | String | ⬜ Unchecked| ⬜ Unchecked|
| 2 | destinationcity  | destinationcity  | Destination City    | String | ⬜ Unchecked| ⬜ Unchecked|
| 3 | json             | json             | JSON                | Any    | ⬜ Unchecked| ⬜ Unchecked|

<img width="1798" height="813" alt="image" src="https://github.com/user-attachments/assets/2e5aa012-d52c-4e1f-9606-eb6128aa5039" />


<br><br>Click on the <img width="100" height="32" alt="image" src="https://github.com/user-attachments/assets/de17ddc5-2555-4a2f-b197-ca7e7f09380b" /> node of the Skill and select the Action Project output according to the table below from the left pane by expanding the tree.
 **Field Name**     | **Mapped Value** | **Path** |
|--------------------|------------------|------------------------|
| destinationcity    | arrivalLocationId | getReadquery > result > d > list - results > arrivalLocationId |
| gttstatus      | eventStatus_code     | getReadquery > result > d > results > plannedEvents > list - results > eventStatus_code |
| json           | result           | getReadquery > result |
<img width="3586" height="1720" alt="image" src="https://github.com/user-attachments/assets/17d4aeb3-8389-48ad-a7dd-0f04092fc7d3" />



<br><br>12: Save your Joule Skill. :white_check_mark:


# Summary — Ex. 3.1.2: Create the Second Joule Skill

This page explains how to create the **second Joule Skill** in the SAP **Joule Skill Package**, named **“Track Shipment.”**  
The purpose of this skill is to **track a specific shipment** in the **SAP Business Network Global Track and Trace (GTT)** system using its tracking ID.

The exercise follows a similar approach to the previous skill and includes these main steps:

- Creating a new **Joule Skill** called `Track Shipment` with a suitable description.  
- Defining an **input parameter** named `trackingID` to capture the shipment tracking number.  
- Adding an **action call** to the previously used `getReadquery` Action from the GTT system.  
- Reusing the existing **destination variable** (`GetFromGTT`) for system connectivity.  
- Configuring a **filter formula** in the Formula Editor to retrieve shipment details based on the tracking ID:
  ```plaintext
  ConcatenateStrings(["trackingId eq ", [Tracking ID], ""], "'")
- Defining multiple output parameters to return shipment details
- Mapping the action outputs to these parameters, including the appropriate data paths for each field.

<br> Once created, this skill allows users to track any specific shipment in the GTT system by providing a tracking ID.

➡️ [Ex. 3.1.3 - Create the final Joule Skill](../ex3.1.3/ex3.1.3-create-create-shipment-skill-1.md)
<br> <br>  - [Back To Landing Page](../../../README.md)
