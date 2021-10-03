# Exercise 16: Implement single sign-on for Microsoft Teams apps

## Task 1: Register an Azure AD application to support single sign-on (SSO)

![image01](images/image01.png)

![image02](images/image02.png)

### Configure authentication

![image03](images/image03.png)

### Create a client secret

![image04](images/image04.png)

### Configure API permissions

![image05](images/image05.png)

![image06](images/image06.png)

### Expose an API for the app

![image07](images/image07.png)

![image08](images/image08.png)

![image09](images/image09.png)

![image10](images/image10.png)

![image11](images/image11.png)

![image12](images/image12.png)

![image13](images/image13.png)

![image14](images/image14.png)

![image15](images/image15.png)

![image16](images/image16.png)

![image17](images/image17.png)

![image18](images/image18.png)

![image19](images/image19.png)

![image20](images/image20.png)

## Review

At this point, you've now registered an Azure AD application that can be used by Microsoft Teams apps to support SSO for your users.

While the application has been registered, you'll need to come back and make a few changes depending on the features of your custom Microsoft Teams app:

### Update the app's URL

When you create the Microsoft Teams app, you'll need to revisit this Azure AD application to update the places where you entered the URL where the application is hosted. This is true both during development and when the application is deployed to production.

Anywhere you entered **REPLACE.ngrok.io** will need to be updated with the location of the web app that implements the custom Microsoft Teams app.

### Add more API permissions

The Azure AD app you've registered only has the most basic permissions to identify the user (**email**, **offline_access**, **openid**, and **profile**).

It also contains the Microsoft Graph **User.Read** permission to obtain basic information about the user. If your custom Microsoft Teams app needs extra permissions to Microsoft Graph or another app, you'll need to add them to the Azure AD app's registration.
