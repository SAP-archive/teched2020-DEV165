# Set Up Gmail Connectivity

In this exercise, you will set up connectivity between your **Cloud Integration** tenant and your **Gmail** account. You will use the **Connectivity Tests** feature available in the **Cloud Integration** ***Monitoring*** view to connect to your email account. Once the connectivity test is successful, you will download the Gmail server certificates and then import it into your **Cloud Integration** tenant. This will ensure that the connectivity will be validated with the requisite server certificates when you call your **GMail** account with your integration flow. 

## Prerequisites 

Please ensure that you have completed all the steps specific to the **GMail** account in the [prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md). 

## Deploying GMail Credentials on Cloud Integration
In this step, you will deploy your username and password on your **Cloud Integration** tenant. 

1. Launch the **Cloud Integration** application from your **Integration Suite** launchpad.
![Launch Cloud Integration](/exercises/Images/Launchpad/launchpad-select-cpi.png)

2. Navigate to the security material by choosing **Monitor > Security Material**.
![Access security material](/exercises/Images/Deploy_Credentials_CPI/access-security-material.png)

3. Create user credentials by choosing **Create > User Credentials**.
![Create user credentials](/exercises/Images/Deploy_Credentials_CPI/create-user-credentials.png)

4. In the **Name** and **Description** fields, enter a name and description that indicates that the credentials is for GMail account. In the **User** field, enter your GMail ID and enter your password in the **Password** field. Re-enter the password in the **Repeat Password** field and choose **Deploy**
![Deploy GMail Credentials](/exercises/Images/Deploy_Credentials_CPI/create-deploy-gmail-credentials.png)

## Performing a Connectivity Test with Your Deployed Credentials


