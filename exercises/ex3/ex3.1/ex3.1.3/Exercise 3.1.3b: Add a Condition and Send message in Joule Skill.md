## Exercise 3.1.3b - Add Send Message steps in Joule Skill
<br> A 'Send Message' step enables you to send a personalized & pre-defined message to the end user in addion to the standard Joule response. 
<br> We will be creating 2 "Send Message" steps, one for each of the Condition branches mentioned in the previous section. 

<br>In Branch 1, Click on the <img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/dd09a02b-cd57-409e-91e5-734e03150803" /> button & select 'Send Response' followed by 'Send Message'. Repeat the step for Branch 2, as well.
<br>

![2025-10-27_18-00-19 (1)](https://github.com/user-attachments/assets/a0659e7d-6fbe-4fc6-ac0c-81f6486d4c2a)

Click on the Send Message step on branch 1 and name it as 'Create Shipment Message'.
<br>
<img width="1786" height="699" alt="image" src="https://github.com/user-attachments/assets/1adda104-bdfb-4fc8-8ea1-e53135dbb9b4" />
<br>
Repeat this for Branch 2 and name it as 'Shipment Update Message'.
<img width="1796" height="658" alt="image" src="https://github.com/user-attachments/assets/7344e2bd-daa6-419a-9183-d9d4b18679a7" />

<br>Click on the 'Create Shipment Message' in Branch 1 and click on the 'Open Message Editor" button.

<br>In the Message Configuration section fill up the details from the table below. 

| Field Name              | Value                |
|--------------------------|-----------------------------|
| Message Type | Illustrated Message    |
| Title                   | 'Success'|
| Text        | 'Shipment Id ${context.startEvent.shipmentid} created successfully in GTT'  |
| Illustration      | Success High Five  |

<img width="1549" height="844" alt="image" src="https://github.com/user-attachments/assets/609ba0dc-3449-4617-9d26-aa85afef4e2b" />

<br>In the Action Button section, Click on Add Button and enter the values from the table below:
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Title                   | 'View Shipment'|
| url        | https://coenagtt.gtt-flp-lbnplatform.cfapps.eu10.hana.ondemand.com/cp.portal/site?sap-language=en#Shipment-track?sap-ui-app-id-hint=com.sap.gtt.app.sts  |

<br>Your Send Message step should look like the image below. You will also notice a preview of what you have designed on the left side. 
<img width="1550" height="665" alt="image" src="https://github.com/user-attachments/assets/2b9295c1-c0f0-4e0e-b2b1-e61b20d4a00c" />
<br>
<br>We will now replicate these steps for the 'Shipment Update Message' in Branch 2 witha a change in few fields as per the table below:
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Message Type | Illustrated Message    |
| Title                   | 'Carrier Updated'|
| Text        | 'Shipment Id ${context.startEvent.shipmentid} created successfully in GTT'  |
| Illustration      | Success Check Mark  |

<br>In the Action Button section, Click on Add Button and enter the values from the table below:
| Field Name              | Value                |
|--------------------------|-----------------------------|
| Title                   | 'View Shipment'|
| url        | https://coenagtt.gtt-flp-lbnplatform.cfapps.eu10.hana.ondemand.com/cp.portal/site?sap-language=en#Shipment-track?sap-ui-app-id-hint=com.sap.gtt.app.sts  |

<img width="1563" height="856" alt="image" src="https://github.com/user-attachments/assets/b85f17a6-3a1c-4c63-b17e-149ab3adb13e" />
<br><br>Save you Skill


<br> <br>  - [Next Exercise - > Exercise 4.4 - Configure the Output Parameter](https://github.com/SAP-samples/teched2025-AD169/tree/6d4d185a4dc5c192ce2f65d6a286b84d98ff7772/exercises/ex4/README.md/ex4.4/README.md)
