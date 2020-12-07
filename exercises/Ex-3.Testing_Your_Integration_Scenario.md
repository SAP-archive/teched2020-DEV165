# Testing Your Integration Scenario

In this exercise, you will test the integration scenario that you have designed. Please ensure that you have downloaded [**Postman**](https://www.postman.com/downloads/) client. You will create a new employee on **BambooHR** and then use the employee ID to trigger a request from **Postman** to your integration flow.

## Prerequisites 
- You have completed all the [prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md) including the [creation of service instance and key](/exercises/create-service-instance-key.md). 
- You have established [connectivity to Non-SAP systems](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems.md).
- You have [designed and deployed an integartion flow](/exercises/Ex-2.Design_Your_Integration_Flow/Ex-2.Design_Your_IFlow.md). 

## Creating A New Employee in BambooHR

1. Login to your **BambooHR** system. 

2. Select **New > New Employee**.
![Create Bamboo Employee 1](/exercises/Images/Create-Test-Bamboo-Employee/create-bamboo-emp-1.png)

3. Mandatorily enter the following values. If you wish, you can also enter values for the other fields as well. Once you have entered all the values, click on **Save**.

|Field|Descrption|
|:---:|:----:|
|**Employee#**|Enter an employee number of your choice|
|**Name**|Enter values for first and last name|
|**Preferred Name**|Enter the preferred name|
|**Gender**|Choose a gender from the dropdown list|
|**Address**|Mandatorily fill all values of the address, including the postcode and country|
|**Work Email**|Enter the emailID of your GMail account that you used for this exercise|

![Create Bamboo Employee 2](/exercises/Images/Create-Test-Bamboo-Employee/create-bamboo-emp-2.png)

4. You will see a success message that the employee has been added. From the browser URL, plese make a note of the employeeID. You will see it indicated by the **id** URL parameter. 
![Create Bamboo Employee 3](/exercises/Images/Create-Test-Bamboo-Employee/create-bamboo-emp-3.png)

