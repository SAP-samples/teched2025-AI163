## Ex. 3.1.1 - <img width="35" height="44" alt="image" src="https://github.com/user-attachments/assets/601b4116-ece9-40ff-8be0-759943cae4ab" /> Create a new Joule Skill
We will now create our Joule Skills within the Joule Skill Package.
<br><br>For this hands-on, we will be creating a total of: 
  <br> - 3 Joule Skills.
  <br>&nbsp;&nbsp; :heavy_minus_sign: One to fetch all delayed shipments from the GTT system.
  <br>&nbsp;&nbsp; :heavy_minus_sign: One to track a particular shipment the GTT system using its shipment id. 
  <br>&nbsp;&nbsp; :heavy_minus_sign: One to create a shipment in the GTT system
  <br> - 1 Joule Agent which uses these skills as **tools** along with Document Grounding. 

### <img width="15" height="25" alt="image" src="https://github.com/user-attachments/assets/4492da9e-a2d9-49d9-a30e-855f7c3663a0" /> First Joule Skill: Delayed Shipment
This Joule Skill is used to fetch delayed shipments from the SAP Business Networks GTT System
<br><br>  1. Click on the Create button and choose ‘Joule Skill’.
<img width="3570" height="1598" alt="image" src="https://github.com/user-attachments/assets/bccec6e3-a803-44c6-a4f5-2aed4d8a7e3e" />


<br><br> 2. Enter the name and Description.
| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Name**        | `Get Delayed Shipments`                  |
| **Description** | ` A skill to get all delayed shipments from the GTT system` |

<br> Click on the ‘Create’ button.
> [!Note]
  > The Identifier is autopopulated based on the Skill name.
<img width="1789" height="831" alt="image" src="https://github.com/user-attachments/assets/d810d3d8-e561-4b0e-8392-c8082bfff11a" />


<br><br> 3. Once the Joule skill is created, you are taken to the skill builder.

<br>4. In the skill builder, click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/ebaa8b75-7024-4b4e-bedd-56ee58638b6e" /> button to add the action that was tested earlier.
<img width="1791" height="666" alt="image" src="https://github.com/user-attachments/assets/35cb80fa-077a-4931-9c2e-da86eaab7dea" />


<br><br>5. Choose the option, ‘Call Action’.
<img width="1799" height="837" alt="image" src="https://github.com/user-attachments/assets/503f93b3-c586-4bd5-a5f4-d22d30572545" />


<br><br>6. Click on the 'Browse All Actions" option.
<img width="1799" height="852" alt="image" src="https://github.com/user-attachments/assets/da42efb2-69d2-48a9-9b94-b93d40a5546c" />


<br><br>7. In the search bar, enter ```GTTReadService``` and press Enter to search for the Action and click on the Add button.
<img width="1797" height="851" alt="image" src="https://github.com/user-attachments/assets/370ac218-fa2b-451a-8e9c-6f291d90de17" />


<br><br>8. Once the action call is added, click on it so that a right panel opens for mapping Input parameters & creating the Destination variable to read data from the GTT system.
<img width="1794" height="677" alt="image" src="https://github.com/user-attachments/assets/54b89c1e-a5dd-4009-a1be-5dfd8b7c3139" />


<br><br>9. Create a ‘Destination Variable’.
* On the General Tab, click in the 'Destination Variable' input field.
* Click on the 'Create Environment Variable' option from the drop-down.
<br>

| Field         | Value                                     |
|---------------|-------------------------------------------|
| **Identifier**        | `GetFromGTT`                  |
| **Description** | `Destination to fetch data from the GTT System` |


> [!Note]
  > Once created, remember to select the destination name from the dropdown and Save your project.

![2025-10-24_14-44-26 (1)](https://github.com/user-attachments/assets/26c4de22-31a6-4347-ae63-0dd684465aab)

<br><br>10. We will now add filter criteria as input to Action to fetch the delayed shipments. Click on the Action and select the Input tab on the right pane. 
<img width="3562" height="1448" alt="image" src="https://github.com/user-attachments/assets/16ed9986-7fdb-43a6-b24d-04d5f5f08266" />


<br><br>11. Click on the `$filter` input area and select the <img width="100" height="25" alt="image" src="https://github.com/user-attachments/assets/97985dd3-212e-4ea3-9a00-a61302b9107b" /> option which will take you to the Formula Editor.
<img width="1790" height="850" alt="image" src="https://github.com/user-attachments/assets/79f00018-3f51-49ed-b404-042910d48a65" />

* Input the following formula in the Formula Editor and click on 'Apply'.
ConcatenateStrings(["delayStatus eq ", true, ""], "")


<img width="3590" height="1694" alt="image" src="https://github.com/user-attachments/assets/fd36e993-1b0d-445c-a76c-082dd86728e7" />

<br><br>12. **Configure the Skill Output**

Finally, we will create an output parameter for the Joule Skill to hold the results from the action.

*   Click anywhere in the Skill Builder's grey area and then click on the <img width="25" height="25" alt="image" src="https://github.com/user-attachments/assets/ee9b22ee-e035-4324-8cda-e9a8c43a4e84" /> button on the right to open the skill's property panel.
  <img width="1793" height="591" alt="image" src="https://github.com/user-attachments/assets/9d61f8eb-e8ff-448e-9d35-bb98fce63b3b" />

*   Click on the **Parameters** tab to show the Input & Output parameters.
*   Click the **Configure** button next to **Skill Outputs**. 
  <img width="3586" height="1370" alt="image" src="https://github.com/user-attachments/assets/b3606f47-e4a3-42a9-9819-9ca58ddadea2" /><br>

*   Click the **Add Output** button and add the following output parameter. 
> [!Note]
> The Identifier is autopopulated based on the ‘Name’ field.

| Name | Identifier | Description | Type | Required | List |
| :--- | :--- | :--- | :--- | :--- | :--- |
| json | json | JSON | Any | ✅ Checked| ✅ Checked|

<img width="1793" height="846" alt="image" src="https://github.com/user-attachments/assets/fdf645a0-d605-4256-b42b-3b58f0603ea1" /><br>

<br><br>13. **Map the Action Output to the Skill Output**

With the output parameter created, you can now map the result from the action call to it.

*   Click on the <img width="100" height="32" alt="image" src="https://github.com/user-attachments/assets/de17ddc5-2555-4a2f-b197-ca7e7f09380b" /> node of the skill. The output mapping panel will appear on the right.
*   In the **json** output field, map the action's result by selecting it from the left pane: `getReadquery > result`.
<img width="1792" height="855" alt="image" src="https://github.com/user-attachments/assets/7255ee94-d4bb-422e-99d3-b71cdb0e0eff" />


<br><br>14. Save your Joule Skill. :white_check_mark:

# Summary — Ex. 3.1.1: Create a New Joule Skill

This page explains how to create the first **Joule Skill** in the SAP **Joule Skill Package**, named **“Get Delayed Shipments.”**  
The purpose of this skill is to **retrieve all delayed shipments** from the **SAP Business Network Global Track and Trace (GTT)** system.

The exercise walks users through the complete process — from creating the skill and configuring its properties to connecting it with a backend action and defining input/output parameters. It involves:

- Creating a new **Joule Skill** using the **Skill Builder** interface.  
- Adding an action call to **`GTTReadService`** for data retrieval.  
- Setting up a **destination variable** (`GetFromGTT`) to connect with the GTT system.  
- Applying a **filter formula** to fetch only delayed shipments:
  ```plaintext
  ConcatenateStrings(["delayStatus eq ", true, ""], "")
- Defining an output parameter to return the results in JSON format.<br>

➡️ [Ex. 3.1.2 - Create the second Joule Skill](../ex3.1.2/ex3.1.2-create-track-shipment-skill.md)<br>

- [Back To Landing Page](../../README.md)