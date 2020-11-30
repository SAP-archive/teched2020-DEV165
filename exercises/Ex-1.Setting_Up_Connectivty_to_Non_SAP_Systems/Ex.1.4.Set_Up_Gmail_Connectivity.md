# Set Up Gmail Connectivity

In this exercise, you will set up connectivity between your **Cloud Integration** tenant and your **Gmail** account. You will use the **Connectivity Tests** feature available in the **Cloud Integration** ***Monitoring*** view to connect to your email account. Once the connectivity test is successful, you will download the Gmail server certificates and then import it into your **Cloud Integration** tenant. This will ensure that the connectivity will be validated with the requisite server certificates when you call your **GMail** account with your integration flow. 

## Prerequisites 

Please ensure that you have completed all the steps specific to the **GMail** account in the [prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md). 

## Deploying GMail Credentials on Cloud Integration
In this part of the exercise, you will deploy your username and password on your **Cloud Integration** tenant. 

1. Launch the **Cloud Integration** application from your **Integration Suite** launchpad.
![Launch Cloud Integration](/exercises/Images/Launchpad/launchpad-select-cpi.png)

2. Navigate to the security material by choosing **Monitor > Security Material**.
![Access security material](/exercises/Images/Deploy_Credentials_CPI/access-security-material.png)

3. Create user credentials by choosing **Create > User Credentials**.
![Create user credentials](/exercises/Images/Deploy_Credentials_CPI/create-user-credentials.png)

4. In the **Name** and **Description** fields, enter a name and description that indicates that the credentials is for GMail account. In the **User** field, enter your GMail ID and enter your password in the **Password** field. Re-enter the password in the **Repeat Password** field and choose **Deploy**
![Deploy GMail Credentials](/exercises/Images/Deploy_Credentials_CPI/create-deploy-gmail-credentials.png)

## Performing Connectivity Test with Your Deployed Credentials
In this part of the exercise, you will use the credentials you deployed to perform a connectivity test with your **GMail** account. Upon successful completion of the test, you will download the server certificates and import them into your **Cloud Integration** tenant. This will ensure that when you send an email using an integration flow, the valid server certificates for the connections are already available. 

1. Launch the **Connectivity Tests** in the **Monitor** view of your **Cloud Integration** tenant.
![Launch connectivity test](/exercises/Images/Gmail_Setup/cpi-launch-connectivity-test.png)

2. Select the **SMTP** tab. In the host, enter `smtp.gmail.com` and choose **STARTTLS Mandatory** in the **Protection** dropdown list. 
![Gmail connectivity 1](/exercises/Images/Gmail_Setup/gmail-connectivity-1.png)

3. In the **Authentication** field, select the **Plain User/Password** radio button. In the **Credential Name** dropdown list, choose the credential for your **GMail** account. 
![Gmail connectivity 2](/exercises/Images/Gmail_Setup/gmail-connectivity-2.png)

4. Uncheck the **Valid Server Certificate Required** checkbox and click on **Send**.
![Gmail connectivity 3](/exercises/Images/Gmail_Setup/gmail-connectivity-3.png)

5. If the connection test is successful, you will see a success message as indicated below. If you do not see it, please verify if you have performed all the aforementioned steps, including the [prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md). 

   Once you see the success message, click on the download icon (arrow pointing down) to download the GMail server certificates and save it on a identifiable folder in your file system. You will learn how to import it and deploy it on your **Cloud Integration** tenant in the next section.
   
   You should have a zip file that contains two server certificates from **GMail**, namely **GTS CA 1O1.cer** and **smtp.gmail.com.cer**. 
![Gmail connectivity 4](/exercises/Images/Gmail_Setup/gmail-connectivity-4.png)

## Import and Deploy GMail Server Certificates on Cloud Integration
In this part of the exercise, you will import the **GMail** server certificates you downloaded in the previous step and deploy them on your **Cloud Integration** tenant. 

1. Access the **Cloud Integration Keystore** by selecting **Monitor > Keystore**. 
![GMail Import Certificate 1](/exercises/Images/Gmail_Setup/gmail-import-cert-1.png)

2. Choose **Add > Certificate** to import the GMail server certificate that you downloaded to your local file system.
![GMail Import Certificate 1.1](/exercises/Images/Gmail_Setup/gmail-import-cert-1.1.png)

3. In the **Add Certificate** pop-up, enter an **Alias** name and click on **Browse**.
![GMail Import Certificate 2](/exercises/Images/Gmail_Setup/gmail-import-cert-2.png)

4. Navigate to the folder where you downloaded the server certificates in the previous part of this exercise, choose one of the certificates and import it to the **Cloud Integration** tenant.
![GMail Import Certificate 3](/exercises/Images/Gmail_Setup/gmail-import-cert-3.png)

5. In the prompt to **Confirm Certificate**, chooe **Confirm**.
![GMail Import Certificate 4](/exercises/Images/Gmail_Setup/gmail-import-cert-4.png)

6. Repeat steps **2** to **5** to import the other certificate as well.  



