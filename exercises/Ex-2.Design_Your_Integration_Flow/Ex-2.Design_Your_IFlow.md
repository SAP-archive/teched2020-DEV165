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

Here's a short clip that show you how to do this:
![Add flow step](/exercises/Images/design_iflow/add-flow-step.gif)

13. In the step settings, enter the name as **Read Employee ID**. It is a good design practice to name every flow step based on its purpose in the scenario so that it is easy for everyone else who uses the same integration flow to understand the design. 
![Create iflow 13](/exercises/Images/design_iflow/cpi-create-iflow-13.png)

14. Select **Exchange Property > Add** to add an exchange property. 
![Create iflow 14](/exercises/Images/design_iflow/cpi-create-iflow-14.png)

15. In the **Name** field, enter ***empid***. In the **Type** dropdown, select **XPath**.
![Create iflow 15](/exercises/Images/design_iflow/cpi-create-iflow-15.png)

16. In the **Data Type** field, enter ***java.lang.String***. In the **Value** field, enter ***/eid/text()***. Here, you are creating an exchange property where the property value is set based on the XPath value. 
![Create iflow 16](/exercises/Images/design_iflow/cpi-create-iflow-16.png)

17. Select the **Read Employee ID** step and select the **+** icon to add a new step. Then, select **Request Reply**. 
![Create iflow 17](/exercises/Images/design_iflow/cpi-create-iflow-17.png)

18. Rename the step to ***Fetch Employee Data from BambooHR***. 
![Create iflow 18](/exercises/Images/design_iflow/cpi-create-iflow-18.png)

19. From the palette, select the **Receiver**.
![Create iflow 19](/exercises/Images/design_iflow/cpi-create-iflow-19.png)

20. Place the receiver below **Fetch Employee Data** but *outside the **Integration Process*** as shown in the image below.
![Create iflow 20](/exercises/Images/design_iflow/cpi-create-iflow-20.png)

21. Select the **Receiver** and rename it as ***BambooHR***.
![Create iflow 21](/exercises/Images/design_iflow/cpi-create-iflow-21.png)

22. Connect the **Fetch Employee Data** to **BambooHR**. When the **Adapter Type** dialog pops up, select the **Open Connectors** adapter. 
![Create iflow 22](/exercises/Images/design_iflow/cpi-create-iflow-22.png)

23. In the **Open Connectors** setting, enter the **Base URI** that you noted while configuring your Open Connectors connector. Refer to **Step 9** of the [**BambooHR** configuration document](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.2.Create_BambooHR_Instance.md) for this information. Then, click on **Select** in the **Credential Name** field.
![Create iflow 23](/exercises/Images/design_iflow/cpi-create-iflow-23.png)

24. From the list of credentials, select the one that you created for **BambooHR**.
![Create iflow 24](/exercises/Images/design_iflow/cpi-create-iflow-24.png)

25. Click on the **Select** icon in **Resource** field.
![Create iflow 25](/exercises/Images/design_iflow/cpi-create-iflow-25.png)

26. In the **List of resources**, choose **/employees/{id}**.
![Create iflow 26](/exercises/Images/design_iflow/cpi-create-iflow-26.png)

27. Replace the **{id}** part with ***${property.empid}***.
![Create iflow 27](/exercises/Images/design_iflow/cpi-create-iflow-27.png)

28. Add the flow step **JSON to XML**. 
![Create iflow 30](/exercises/Images/design_iflow/cpi-create-iflow-30.png)

29. Rename the flow step to **Convert response to XML**.
![Create iflow 31](/exercises/Images/design_iflow/cpi-create-iflow-31.png)

30. Add the flow step **Content Modifier**. 
![Create iflow 32](/exercises/Images/design_iflow/cpi-create-iflow-32.png)

31. Rename the **Content Modifier** to ***Read Employee Details**.
![Create iflow 32.1](/exercises/Images/design_iflow/cpi-create-iflow-32.1.png)

32. Select the **Exchange Property** tab and click on **Add**. Here, you are reading the value of a field from the response that you received from **BamboHR** system.
![Create iflow 32.1](/exercises/Images/design_iflow/cpi-create-iflow-32.2.png)

33. Add the values in respective field based on the table below

|Field|Description|
|:-----:|:------:|
|Name|***workemail***|
|Type|Select **XPath** from dropdown list|
|Data Type|***java.lang.String***|
|Value|***/root/workEmail***|

![Create iflow 33](/exercises/Images/design_iflow/cpi-create-iflow-33.png)

34. Similarly, add the remaining peroperty values indicated by the screenshot below. You will be using all these properties in the creating the email template and the **Slack** message.
![Create iflow 34](/exercises/Images/design_iflow/cpi-create-iflow-34.png)

35. Add a **Parallel Multicast** step.
![Create iflow 35](/exercises/Images/design_iflow/cpi-create-iflow-35.png)

36. Add **Content Modifier** step.
![Create iflow 36](/exercises/Images/design_iflow/cpi-create-iflow-36.png)

37. Rename the **Content Modifier** to ***Set EMail Message***.
![Create iflow 37](/exercises/Images/design_iflow/cpi-create-iflow-37.png)

38. Select the **Message Body** tab. In the **Body** field, paste the following code:

```HTML
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:o="urn:schemas-microsoft-com:office:office">

<head>
    <meta charset="UTF-8">
    <meta content="width=device-width, initial-scale=1" name="viewport">
    <meta name="x-apple-disable-message-reformatting">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta content="telephone=no" name="format-detection">
    <title></title>
    <!--[if (mso 16)]>
    <style type="text/css">
    a {text-decoration: none;}
    </style>
    <![endif]-->
    <!--[if gte mso 9]><style>sup { font-size: 100% !important; }</style><![endif]-->
    <!--[if gte mso 9]>
<xml>
    <o:OfficeDocumentSettings>
    <o:AllowPNG></o:AllowPNG>
    <o:PixelsPerInch>96</o:PixelsPerInch>
    </o:OfficeDocumentSettings>
</xml>
<![endif]-->
</head>

<body>
    <div class="es-wrapper-color">
        <!--[if gte mso 9]>
			<v:background xmlns:v="urn:schemas-microsoft-com:vml" fill="t">
				<v:fill type="tile" color="#f6f6f6"></v:fill>
			</v:background>
		<![endif]-->
        <table class="es-wrapper" width="100%" cellspacing="0" cellpadding="0">
            <tbody>
                <tr>
                    <td class="esd-email-paddings" valign="top">
                        <table class="es-content esd-header-popover" cellspacing="0" cellpadding="0" align="center">
                            <tbody>
                                <tr>
                                    <td class="esd-stripe" align="center">
                                        <table class="es-content-body" width="600" cellspacing="0" cellpadding="0" bgcolor="#ffffff" align="center">
                                            <tbody>
                                                <tr>
                                                    <td class="esd-structure" align="left">
                                                        <table width="100%" cellspacing="0" cellpadding="0">
                                                            <tbody>
                                                                <tr>
                                                                    <td class="esd-container-frame" width="600" valign="top" align="center">
                                                                        <table style="border-left:2px solid #959595;border-right:2px solid #959595;border-top:2px solid #959595;border-bottom:2px solid #959595;" width="100%" cellspacing="0" cellpadding="0">
                                                                            <tbody>
                                                                                <tr>
                                                                                    <td class="esd-block-image" align="center" style="font-size: 0px;"><a target="_blank"><img class="adapt-img" src="https://cdn.smartrecruiters.com/blog/wp-content/uploads/2020/03/welcome_email_tempalte_greeting.jpg" alt style="display: block;" width="596"></a></td>
                                                                                </tr>
                                                                            </tbody>
                                                                        </table>
                                                                    </td>
                                                                </tr>
                                                            </tbody>
                                                        </table>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                        <table class="es-content" cellspacing="0" cellpadding="0" align="center">
                            <tbody>
                                <tr>
                                    <td class="esd-stripe" align="center">
                                        <table class="es-content-body" width="600" cellspacing="0" cellpadding="0" bgcolor="#ffffff" align="center">
                                            <tbody>
                                                <tr>
                                                    <td class="esd-structure es-p30t es-p20r es-p20l" align="left">
                                                        <table width="100%" cellspacing="0" cellpadding="0">
                                                            <tbody>
                                                                <tr>
                                                                    <td class="esd-container-frame" width="560" valign="top" align="center">
                                                                        <table width="100%" cellspacing="0" cellpadding="0">
                                                                            <tbody>
                                                                                <tr>
                                                                                    <td class="esd-block-text es-p5b" align="left">
                                                                                        <h2>Welcome&nbsp; ${property.fname} ${property.lname},</h2>
                                                                                    </td>
                                                                                </tr>
                                                                                <tr>
                                                                                    <td class="esd-block-text es-m-txt-c es-p10b" align="left">
                                                                                        <p style="color: #333333;">On behalf of everyone at our company, we would like to extend a warm welcome to you!</p><br>
                                                                                        <p>We know you’re going to be a valuable asset and can’t wait to see what you accomplish.Your details have been added in the HR System and our team is working on getting all the paperwork done.</p><br>
                                                                                        <p>Please expect a welcome kit and further details on the next steps for getting started. We are looking forward to having you on board!</p>
                                                                                    </td>
                                                                                </tr>
                                                                            </tbody>
                                                                        </table>
                                                                    </td>
                                                                </tr>
                                                            </tbody>
                                                        </table>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                        <table class="es-content esd-footer-popover" cellspacing="0" cellpadding="0" align="center">
                            <tbody>
                                <tr>
                                    <td class="esd-stripe" align="center">
                                        <table class="es-content-body" style="background-color: #ffffff;" width="600" cellspacing="0" cellpadding="0" bgcolor="#ffffff" align="center">
                                            <tbody>
                                                <tr>
                                                    <td class="esd-structure es-p20t es-p20b es-p20r es-p20l" align="left">
                                                        <!--[if mso]><table width="560" cellpadding="0" 
                        cellspacing="0"><tr><td width="270" valign="top"><![endif]-->
                                                        <table class="es-left" cellspacing="0" cellpadding="0" align="left">
                                                            <tbody>
                                                                <tr>
                                                                    <td class="es-m-p20b esd-container-frame" width="270" align="left">
                                                                        <table width="100%" cellspacing="0" cellpadding="0">
                                                                            <tbody>
                                                                                <tr>
                                                                                    <td class="esd-block-text es-m-txt-c" align="left">
                                                                                        <p style="color: #333333;"><br><br>Best Regards,<br>Your HR Team
                                                                                    </td>
                                                                                </tr>
                                                                            </tbody>
                                                                        </table>
                                                                    </td>
                                                                </tr>
                                                            </tbody>
                                                        </table>
                                                        <!--[if mso]></td><td width="20"></td><td width="270" valign="top"><![endif]-->
                                                        <table class="es-right" cellspacing="0" cellpadding="0" align="right">
                                                            <tbody>
                                                                <tr>
                                                                    <td class="esd-container-frame" width="270" align="left">
                                                                        <table width="100%" cellspacing="0" cellpadding="0">
                                                                            <tbody>
                                                                                <tr>
                                                                                    <td class="esd-block-social es-p5t es-m-txt-c" align="right" style="font-size:0">
                                                                                        <table class="es-table-not-adapt es-social" cellspacing="0" cellpadding="0">
                                                                                            <tbody>
                                                                                                <tr>
                                                                                                    <td class="es-p10r" valign="top" align="center"><a target="_blank" href><img title="Facebook" src="https://hqitqh.stripocdn.email/content/assets/img/social-icons/logo-black/facebook-logo-black.png" alt="Fb" width="32"></a></td>
                                                                                                    <td class="es-p10r" valign="top" align="center"><a target="_blank" href><img title="Twitter" src="https://hqitqh.stripocdn.email/content/assets/img/social-icons/logo-black/twitter-logo-black.png" alt="Tw" width="32"></a></td>
                                                                                                    <td class="es-p10r" valign="top" align="center"><a target="_blank" href><img title="Instagram" src="https://hqitqh.stripocdn.email/content/assets/img/social-icons/logo-black/instagram-logo-black.png" alt="Inst" width="32"></a></td>
                                                                                                    <td class="es-p10r" valign="top" align="center"><a target="_blank" href><img title="Youtube" src="https://hqitqh.stripocdn.email/content/assets/img/social-icons/logo-black/youtube-logo-black.png" alt="Yt" width="32"></a></td>
                                                                                                </tr>
                                                                                            </tbody>
                                                                                        </table>
                                                                                    </td>
                                                                                </tr>
                                                                            </tbody>
                                                                        </table>
                                                                    </td>
                                                                </tr>
                                                            </tbody>
                                                        </table>
                                                        <!--[if mso]></td></tr></table><![endif]-->
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

