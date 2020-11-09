# Create BambooHR Instance

## Prerequisites 

- You have set up **Integration Suite** trial anad activated the **Open Connectors** capability. If you have not done this yet, refer to [Prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md) for detailed guidance.
- You have created a trial account on **BambooHR**. 

## Generating API Key for BambooHR Account
You will use this API key as the credential for authenticating your **Open Connectors** BambooHR connector.

1. Login to your **BambooHR** account. Click on the ***Settings*** or gear icon on the top right of your screen and select **API Keys**. 
![BambooHR API Key](/exercises/Images/OCN/bamboohr-apikey.png)

2. Click on **Add New Key**. 
![BambooHR API Key 1](/exercises/Images/OCN/bamboohr-add-apikey-1.png)

3. Enter a name for the API key and click on **Generate Key**.
![BambooHR API Key 2](/exercises/Images/OCN/bamboohr-add-apikey-2.png)

4. Click on the **COPY KEY** link to copy the API key. Click on **Done** to close the dialog. 
![BambooHR API Key 3](/exercises/Images/OCN/bamboohr-add-apikey-3.png)

## Authenticating BambooHR Connector
You will use the API key generated in the previous section to authenticate your **Open Connectors** BambooHR connector. 

1. Access your **Integration Suite Launchpad**.
![Access Integration Suite Launchpad](/exercises/Images/Launchpad/cockpit-access-launchpad.png)

2. Launch the **Open Connectors** capability.
![Launch OCN](/exercises/Images/Launchpad/launchpad-select-ocn.png)

3. Select the ***Connectors*** tab.
![Select Connectors Tab](/exercises/Images/OCN/ocn-select-connectors.png)

4. Filter for **BambooHR** and click on ***Authenticate***.
![Authenticate BambooHR Connector](/exercises/Images/OCN/ocn-authenticate-bamboohr.png)

5. Enter a **Name** for your instance. 
    - In the **Company Name** field, enter the first part of the URL from your BambooHR account as shown in the screenshot below. 
    - In the **API Key** field, enter the API key that you generated in the previous section. 
![Authenticate BambooHR Connector](/exercises/Images/OCN/ocn-bamboohr-config-connection-1.png)

6. 

  
