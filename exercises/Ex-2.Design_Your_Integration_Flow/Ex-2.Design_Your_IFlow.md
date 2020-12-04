# Design Your Integration Flow
In this part of the exercise, you will design, configure and deploy the integration flow in Cloud Integration. You will see the convenience of the drag and drop user interface for desgning integration flow. 

## Prerequisites 
- You have completed all the steps mentioned in the [Prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md)
- You have set up and tested connectivity to all the non-SAP systems like **Slack**, **GMail** and **BambooHR** - [Setting Up Connectivity to Non-SAP Systems](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems.md)

**NOTE:** This part of the exercise will be a little more time consuming compared to the other sections you have completed till now. This is by design since we want you to experience the usability of the web-based integration flow designer. In case you want to speed up this process, you can download the integration flow from the **Assets** folder and deploy it on **Cloud Integration**. The folder contains a document explaining how you can import and deploy the integration flow. 

## Designing Your Integration Flow

1. Launch **Cloud Integration** from the **Integration Suite** launchpad. 
![Launch CPI](/exercises/Images/Launchpad/launchpad-select-cpi.png)

2. Select **Design > Create** to create a new integration package for this exercise.
![Create iflow 1](/exercises/Images/design_iflow/cpi-create-iflow-1.png)

3. Ener a unique name and description that identifies the purpose of the package and select **Save**.
![Create iflow 2](/exercises/Images/design_iflow/cpi-create-iflow-2.png)

4. Select **Artifacts > Add > Integration Flow** to create a new integration flow. 
![Create iflow 3](/exercises/Images/design_iflow/cpi-create-iflow-3.png)

5. Enter a unique name for your integration flow in the **Name** field. The **ID** gets populated automatically. Select **OK** to save the integration flow. 
![Create iflow 4](/exercises/Images/design_iflow/cpi-create-iflow-4.png)

6. Select **Save** to save the integration package with the integration flow that you have created. Select the integration flow to start editing it. 
![Create iflow 5](/exercises/Images/design_iflow/cpi-create-iflow-5.png)

7. Select **Edit**.
![Create iflow 6](/exercises/Images/design_iflow/cpi-create-iflow-6.png)

8. Connect the **Sender** to the **Start** step.
![Create iflow 7](/exercises/Images/design_iflow/cpi-create-iflow-7.png)

9. In the **Adapter Type** dialog, select **HTTPS**. 
![Create iflow 8](/exercises/Images/design_iflow/cpi-create-iflow-8.png)

Here's a short clip of the process:
![Add Adapter GIF](/exercises/Images/design_iflow/add-adapter.gif)

10. In the adapter settings, choose the **Connection** tab. In the **Address** field, enter ***/dev165demo***. You can enter any value of your choice; please follow the convention of adding a "**/**" before the value. Disable the **CSRF Protected** checkbox. 
![Create iflow 10](/exercises/Images/design_iflow/cpi-create-iflow-10.png)

11. Click on the **Start** step and select the **+** icon.
![Create iflow 11](/exercises/Images/design_iflow/cpi-create-iflow-11.png)

12. In the **Add Flow** step, select **Content Modifier**.
![Create iflow 12](/exercises/Images/design_iflow/cpi-create-iflow-12.png)

13. In the step settings, enter the name as **Read Employee ID**. It is a good design practice to name every flow step based on its purpose in the scenario so that it is easy for everyone else who uses the same integration flow to understand the design. 
![Create iflow 13](/exercises/Images/design_iflow/cpi-create-iflow-13.png)

14. Select **Exchange Property > Add** to add an exchange property. 
![Create iflow 14](/exercises/Images/design_iflow/cpi-create-iflow-14.png)

15. In the **Name** field, enter ***empid***. In the **Type** dropdown, select **XPath**.
![Create iflow 15](/exercises/Images/design_iflow/cpi-create-iflow-15.png)

16. In the **Data Type** field, enter ***java.lang.String***. In the **Value** field, enter ***/eid/text()***. Here, you are creating an exchange property where the property value is set based on the XPath value. 
![Create iflow 16](/exercises/Images/design_iflow/cpi-create-iflow-16.png)

17. 
