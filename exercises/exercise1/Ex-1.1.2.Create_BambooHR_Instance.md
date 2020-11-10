# Create BambooHR Instance

## Prerequisites 

- You have set up **Integration Suite** trial anad activated the **Open Connectors** capability. If you have not done this yet, refer to [Prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md) for detailed guidance.
- You have created a trial account on **BambooHR**. 

## Generating API Key for BambooHR Account
You will use this API key as the credential for authenticating your **Open Connectors** BambooHR connector.

1. Login to your **BambooHR** account. Click on the ***Profile*** or image icon on the top right of your screen and select **API Keys**. 
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
![Authenticate BambooHR Connector 1](/exercises/Images/OCN/ocn-bamboohr-config-connection-1.png)

6. Enable the **Event Configuration** switch. This allows you to configure your connector instance to call a URL when a certain event occurs on the **BambooHR** system. 
    - In the **Event Notification Callback URL** field, enter the URL of your **Cloud Integration** tenant followed by ***http/teched20***. This is the configuration that you will enter in the HTTP sender adapter when you design the integration flow in **Cloud Integration**. 
    <br>**NOTE:** You can enter any value of your choice for the HTTP endpoint instead of ***teched20***. Please make sure that you use the same value when you configure your **Cloud Integration** iflow's HTTP sender adapter configuration. 
    - Enter your email ID and password for your SAP Cloud Platform Trial account in the **Event Notification Basic Authentication UserName** and **Event Notification Basic Authentication Password** fields respectively.
    - In the **Event poller refresh interval (mins)** field, enter the value as ***2***. This will configure the connector to check for new events in your BambooHR system every two minutes. 
    - Click on **Create Instance**. 
![Authenticate BambooHR Connector 2](/exercises/Images/OCN/ocn-bamboohr-config-connection-2.png)

7. You will see a confirmation message that the connector instance has been created. Please click on the **Test in the API Docs** to test the connector instance.
![Authenticate BambooHR Connector Confirmaton](/exercises/Images/OCN/ocn-authenticate-bamboohr-confirmation.png)

8. Search for the **GET /employees** resource and click on **Try it Out**. This resource should fetch the list of all employees available in your BambooHR system. 
![BambooHR Connector Test API Doc 1](/exercises/Images/OCN/ocn-bamboohr-testapidoc-1.png)

9.  Click on **Execute**. 
![BambooHR Connector Test API Doc 2](/exercises/Images/OCN/ocn-bamboohr-testapidoc-2.png)

10. If everything is working as expected, you will see the response code **200** and the list of employees in the response. 
    <br>Additionally, you can see the URL of your **Open Connectors** instance in the **Request URL** field that you will be using in the **Open Connectors** adapter in **Cloud Integration** when you design the integration flow. 
![BambooHR Connector Test API Doc 3](/exercises/Images/OCN/ocn-bamboohr-testapidoc-3.png)

You have now successfully created a **BambooHR** connector instance and tested it in **Open Connectors**. 



  
