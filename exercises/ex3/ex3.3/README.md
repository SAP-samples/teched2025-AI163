## Exercise 4.3 - Add a Send message in Joule Skill
<br> 1: Below the Action call, click on the ‘+’ button and choose Send Response. Click on ‘Send message’
<br><br> <img width="940" height="461" alt="image" src="https://github.com/user-attachments/assets/297092e9-0f24-493a-8048-090cf9c1b817" />
<br><br>2: On the right, change the step name as ‘Simulate Workload Message’ and save.
<br><br>3: Click on ‘Open message Editor’
<br><br><img width="940" height="788" alt="image" src="https://github.com/user-attachments/assets/a260c5e9-5868-4e7d-8a37-2031d540f5e1" />
<br><br>4: In the ‘Edit user Interaction’ pop-up window, choose the ‘Message Type’ as ‘List’.
<br> - Enter the Title as ‘Simulated Optimization Results’ 
<br> - Enter the Text as ‘Workforce Optimization Results’
<br><br>5: In the ‘List Item’ section, click on ‘Edit List Item’
<br><br><img width="939" height="423" alt="image" src="https://github.com/user-attachments/assets/28bab2d7-47b1-4adb-b981-3bf72b53774c" />
<br><br>6: In the field, ‘List Content’, click on the ‘<>’ button to do the data mapping. Expand the Joule Action result section and map the ‘value’ 
<br><br><img width="940" height="455" alt="image" src="https://github.com/user-attachments/assets/c453aeb1-b250-4606-b437-9be2be8d9899" />

<br><br>7: In the Title field, click on the ‘<>’ button and map the data, Joule Action result->value->Resource
<br><br><img width="940" height="512" alt="image" src="https://github.com/user-attachments/assets/c8ba3f90-5790-4bef-9ff3-c90f5622de81" />
<br><br>8: In the ‘Text’ field, click on the ‘<>’ button and map the data, Joule Action result->value->status_text
<br><br><img width="940" height="528" alt="image" src="https://github.com/user-attachments/assets/b9aab3ba-7398-4247-bb73-e39b8918db0c" />
<br><br>9: In the Status field, click on the ‘<>’ button and map the data, Joule Action result->value->status
<br><br><img width="940" height="462" alt="image" src="https://github.com/user-attachments/assets/4dd20600-2640-4f1b-b218-735498aea174" />

<br><br>10: In the ‘Attributes’ section, click on ‘Add Attribute’ to add 4 attributes as below
<br>Title: Optimization Details
<br>
<table>
  <tr>
    <th>Type</th>
    <th>Label</th>
    <th>Value (Click on the <> button)</th>
   </tr>
  <tr>
    <td>Text</td>
    <td>Resource</td>
    <td>Joule.action.results->value->resource</td>
   </tr>
  <tr>
    <td>Text</td>
    <td>Status</td>
    <td>Joule.action.results->value->status</td>
    
  </tr>
  <tr>
    <td>Text</td>
    <td>Activity area</td>
    <td>Joule.action.results->value->activity_area</td>
    
  </tr>
  <tr>
    <td>Text</td>
    <td>Resource Type</td>
    <td>Joule.action.results->value->resource_type</td>
    
  </tr>
</table>

<br><br>Click on Save button
<br><br>Once the details are added the ‘Preview’ should be seen in the right panel
<br><br><img width="939" height="522" alt="image" src="https://github.com/user-attachments/assets/4b3f86a9-cd84-4926-a175-00626e4d7b22" />
<br>Click on back button on top left to return to the skill builder.
<br> <br>  - [Next Exercise - > Exercise 4.4 - Configure the Output Parameter](https://github.com/SAP-samples/teched2025-AD169/tree/6d4d185a4dc5c192ce2f65d6a286b84d98ff7772/exercises/ex4/README.md/ex4.4/README.md)
