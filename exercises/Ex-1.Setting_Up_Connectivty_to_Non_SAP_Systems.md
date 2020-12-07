# Setting Up Connectivity to Non-SAP Systems

In this exercise, you will configure all the components that are required to build, deploy and test your non-SAP integration scenario. You will perform the following steps:

## Authenticate Open Connector Instances with Non-SAP Applications

To enable connectivty between **Integration Suite** and non-SAP applications, you create ***Instances*** in the **Open Connectors** capability. Here, you will find the connector for the non-SAP applications, ***Slack*** and ***BambooHR*** and authenticate them with the required credntials. You can then use these authenticated instances to build your integration scenario. 

### [Create Slack Instance](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.1.Create_Slack_Instance.md)

### [Create Bamboo HR Instance](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.2.Create_BambooHR_Instance.md)

## [Deploy Credentials of Non-SAP Applications on Cloud Integration](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex.1.3.Deploy_Credentials_on_CloudIntegartion.md)

Since there are three non-SAP systems that you will be using in this hands-on exercise, you will have to deploy the credentials (login details of your **GMail** account and Open Connectors instances) of all these applications on your **Cloud Integration** tenant. 

## [Configure Connectivity to Your Gmail Account](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex.1.4.Set_Up_Gmail_Connectivity.md)

You will be using the ***Mail*** adapter in the **Cloud Integration** capability to send an email to the **GMail** account of the new hire. To do this, you have to setup connectivity between **Cloud Integration** and **GMail** server by following these steps:
- Test connectivity between **Cloud Integration** and **GMail** account using connectivity test
- Download **GMail** server certificates and deploy them on your **Cloud Integration** tenant. 
