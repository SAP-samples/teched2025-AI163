## Ex. 3.1.3b - Add Send Message steps in Joule Skill
<br> A 'Send Message' step enables you to send a personalized & pre-defined message to the end user in addition to the standard Joule response. 
<br> We will be creating 2 "Send Message" steps, one for each of the Condition branches created in the previous exercise. 

1. In Branch 1, click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/dd09a02b-cd57-409e-91e5-734e03150803" /> button & select 'Send Response' followed by 'Send Message'. Repeat the step for Branch 2, as well.

![2025-10-27_18-00-19 (1)](https://github.com/user-attachments/assets/a0659e7d-6fbe-4fc6-ac0c-81f6486d4c2a)

<br>

* Click on the Send Message step on Branch 1 and name it as ```Create Shipment Message```.

<img width="3572" height="1398" alt="image" src="https://github.com/user-attachments/assets/256a69d4-430c-4586-b1b0-d509435f97e9" />

<br>

* Repeat this for Branch 2 and name it as ```Shipment Update Message```.
<img width="1796" height="658" alt="image" src="https://github.com/user-attachments/assets/7344e2bd-daa6-419a-9183-d9d4b18679a7" />

* Click on the 'Create Shipment Message' in Branch 1 and click the 'Open Message Editor" button.
<img width="1787" height="683" alt="image" src="https://github.com/user-attachments/assets/efd72d08-292f-4e59-993e-47f130cc4fe1" />

* In the **Message Configuration** section, fill in the details from the table below. 

| Field Name              | Value                |
|--------------------------|-----------------------------|
| Message Type | Illustrated Message    |
| Title                   | `Success`|
| Text        | `Shipment Id ${context.startEvent.shipmentid} created successfully in GTT`  |
| Illustration      | Success High Five  |

<img width="1549" height="844" alt="image" src="https://github.com/user-attachments/assets/609ba0dc-3449-4617-9d26-aa85afef4e2b" />

* In the **Action Button** section, click **Add Button** and enter the values from the table below:
  
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Title                   | `View Shipment`|
| url        | `https://coenagtt.gtt-flp-lbnplatform.cfapps.eu10.hana.ondemand.com/cp.portal/site?sap-language=en#Shipment-track?sap-ui-app-id-hint=com.sap.gtt.app.sts`  |

> [!WARNING]
> You will not be able to directly access the GTT system due to restricted Authorization. Ask your trainer to show you the created shipment in the GTT system. 

<br>

* Your Send Message step should look like the image below. You will also notice a preview of what you have designed on the left side. 
<img width="1550" height="665" alt="image" src="https://github.com/user-attachments/assets/2b9295c1-c0f0-4e0e-b2b1-e61b20d4a00c" />
<br>
2. We will now replicate these steps for the 'Shipment Update Message' in Branch 2 with a change in a few fields as per the table below:
  
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Message Type | Illustrated Message    |
| Title                   | `Carrier Updated`|
| Text        | `Shipment Id ${context.startEvent.shipmentid} created successfully in GTT`  |
| Illustration      | Success Check Mark  |

* In the **Action Button** section, click **Add Button** and enter the values from the table below:
  
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Title                   | `View Shipment`|
| url        | `https://coenagtt.gtt-flp-lbnplatform.cfapps.eu10.hana.ondemand.com/cp.portal/site?sap-language=en#Shipment-track?sap-ui-app-id-hint=com.sap.gtt.app.sts`  |


> [!WARNING]
> You will not be able to directly access the GTT system due to restricted Authorization. Ask your trainer to show you the created shipment in the GTT system. 

<img width="1563" height="856" alt="image" src="https://github.com/user-attachments/assets/b85f17a6-3a1c-4c63-b17e-149ab3adb13e" />

* Save your Skill.

## Summary — Ex. 3.1.3b: Add Send Message Steps in Joule Skill

This page explains how to add **“Send Message”** steps in the Joule Skill to provide personalized and pre-defined feedback messages to users.  
These messages are displayed in addition to the standard Joule response when a shipment is **created** or **updated** in the SAP Business Network GTT system.

The exercise builds on the condition branches from the previous step and includes:

### 1. Creating Send Message Steps
Two **Send Message** steps are created—one for each condition branch:
- **Branch 1:** For a new shipment, a `Create Shipment Message` is configured.
- **Branch 2:** For an existing shipment, a `Shipment Update Message` is configured.

### 2. Configuring the "Create Shipment Message"
This step configures an illustrated message with the title "Success" and text confirming the shipment was created, along with a button to view the shipment.

### 3. Configuring the "Shipment Update Message"
This step configures a similar illustrated message with the title "Carrier Updated" to confirm the update was successful.

<br>

➡️ [Next Exercise: Ex. 4 - Create a Joule Agent!](../../../ex4/ex4-create-joule-agent.md)
  
<br> <br>  - [Back To Landing Page](../../README.md)