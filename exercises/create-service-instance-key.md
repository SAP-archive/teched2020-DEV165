# Create Service Instance and Service Key

In this exercise, you will create a service instance and service key for your **Cloud Integration** capability. When you deploy an integration flow with a HTTP endpoint in one of the next exercises, you will use the **clientID** and **clientSecret** from this service key as authentication details. 

1. From your trial account cockpit, access the space created for your suaccount. If your subaccount does not have a space, please click on **Create Space** and follow the guided process to create a new space and access it. 
![Create service instance and key 1](/exercises/Images/create-service-instance-key/create-service-inst-key-1.png)

2. Select the **Service Marketplace** tab. Filter for ***Process Integration*** and select the **Process Integration Runtime** tile. 
![Create service instance and key 2](/exercises/Images/create-service-instance-key/create-service-inst-key-2.png)

3. Click on **Create Instance**.
![Create service instance and key 3](/exercises/Images/create-service-instance-key/create-service-inst-key-3.png)

4. From the **Service Plan** dropdown list, select **integration-flow**. 
![Create service instance and key 4](/exercises/Images/create-service-instance-key/create-service-inst-key-4.png)

5. Provide a name for your instance in the **Instance Name** field and choose **Next**.
![Create service instance and key 5](/exercises/Images/create-service-instance-key/create-service-inst-key-5.png)

6. Enter the following parameters for the role **ESBMessaging.send** and click on **Next**
```JSON
{
"roles":["ESBMessaging.send"]
}
```
![Create service instance and key 6](/exercises/Images/create-service-instance-key/create-service-inst-key-6.png)

7. Click on **Create Instance**.
![Create service instance and key 7](/exercises/Images/create-service-instance-key/create-service-inst-key-7.png)

8. In the **Success**, select **View Instance**.
![Create service instance and key 8](/exercises/Images/create-service-instance-key/create-service-inst-key-8.png)

9. In the newly created instance, select ***More options*****> Create Service Key**.
![Create service instance and key 9](/exercises/Images/create-service-instance-key/create-service-inst-key-9.png)

10. Enter a unique nam for the service key, enter the following parameters for the role and click on **Create**.
![Create service instance and key 10](/exercises/Images/create-service-instance-key/create-service-inst-key-10.png)

11. Once the instance is created, click on ***More options*****> View**. 
![Create service instance and key 11](/exercises/Images/create-service-instance-key/create-service-inst-key-11.png)

12. Please note down the values of **clientid** and **clientsecret** parameters. You will use these values are the user ID and password respectively when you are making a call to the integration flow endpoint using **Postman** client. 
![Create service instance and key 12](/exercises/Images/create-service-instance-key/create-service-inst-key-12.png)
