# Deploy Credentials on Cloud Integration

You will be using the **Open Connector** instances for **BambooHR** and **Slack** in your **Cloud Integration** tenant for building the integration scenario. To do this, you must first deploy the credentials, or authorization details, for your connector instances on your **Cloud Integration** tenant. Also, you will have to deploy your **GMail** username and password to enable connectivity between **Integration Suite** and **GMail** account. 

## Prerequisites 

- You have set up **Integration Suite** trial anad activated the **Cloud Integration** capability. If you have not done this yet, please refer to [Prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md) for detailed guidance.
- You have created **Open Connectors** instances for both **Slack** and **BambooHR**. If you have not done this, please refer to [Create Slack Instance](/exercises/exercise1/Ex-1.1.1.Create_Slack_Instance.md) and [Create BambooHR Instance](/exercises/exercise1/Ex-1.1.2.Create_BambooHR_Instance.md).
- If you do not have a **GMail** account to be used in this exercise, you can create one using this link: [Create A New GMail Account](https://accounts.google.com/signup/v2/webcreateaccount?hl=en&flowName=GlifWebSignIn&flowEntry=SignUp)
- Access the **Cloud Integration** application from the **Integration Suite** launchpad. 
  ![Launch Clooud Integration](/exercises/Images/Launchpad/launchpad-select-cpi.png)

## Deploy Slack and Open Connectors Credentials

1. Navigate to **Security Material** by choosing **Monitor > Security Material**.
![Access Security Material](/exercises/Images/Deploy_Credentials_CPI/access-security-material.png)

2. Create user credentials by choosing **Create > User Credentials**.
![Create user credentials](/exercises/Images/Deploy_Credentials_CPI/create-user-credentials.png)

3. In the **Type** dropdown list, select the type **Open Connectors**.
![Select Type Open Connectors](/exercises/Images/Deploy_Credentials_CPI/select-type-open-connectors.png)

4. Enter a **Name** and **Description** that identifies this credential as the one specific to your **Slack** Open Connectors instance. 
   - In the **User** and **Organization** field, enter the **User Secret** and **Organization Secret** from your **Open Connnectors** application. 
   - In the **Element** field, enter the **Instance Token** specific to the **Slack** instance in your **Open Connectors** application. 
   - **`TIP:`** Click on the ![Copy](/exercises/Images/Deploy_Credentials_CPI/copy-icon.png) icon next to each of the fields to copy the values of the respective fields and then paste it in the **Cloud Integration** application.
   - Refer to the screenshot below to learn how you can obtain the values for the respective fields from your **Open Connectors** application and the corresponding fields in your **Cloud Integration** tenant. 
   - After entering all the details, select **Deploy** to deploy or activate the credentials. 
![Create Slack Credentials](/exercises/Images/Deploy_Credentials_CPI/create-deploy-slack-credentials.png)

5. Follow the same steps as in the previous step to deploy **BambooHR Open Connectors** credentials on your **Cloud Integration** tenant. Please ensure that you choose a unique name to identify the **BambooHR** credentials. 
![Create BambooHR Credentials](/exercises/Images/Deploy_Credentials_CPI/create-deploy-bambooHR-credentials.png)

## Deploy GMail Credentials

1. Navigate to **Security Material** by choosing **Monitor > Security Material**.
![Access Security Material](/exercises/Images/Deploy_Credentials_CPI/access-security-material.png)

2. Create user credentials by choosing **Create > User Credentials**.
![Create user credentials](/exercises/Images/Deploy_Credentials_CPI/create-user-credentials.png)

3. Enter values in fields based on description in table:
| Field | Description |
|-------|-------------|
|Name|Name of your GMail credentials|

