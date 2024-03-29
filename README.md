# DEV165 -  Non-SAP Integration with SAP Integration Suite

[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2020-DEV165)](https://api.reuse.software/info/github.com/SAP-samples/teched2020-DEV165)


## Description

In this session, you will learn how to use SAP Integration Suite to implement an integration scenario involving non-SAP applications. You will implement a hire-to-retire scenario, a use case involving HR applications, collaboration tools like Slack and email receiver. You will execute this exercise on the trial environment of SAP Business Technology Platform and also use a trial account in non-SAP applicatons. 

## Overview

This session introduces you to the capabilities of **Integration Suite** that help you with all your non-SAP integration needs. You will work on a HR scenario related to the *Hire-to-Retire* business process of the Intelligent Enterprise. 

You will work with **BambooHR**, a cloud based non-SAP application that provides HR related services. You will use this application's trial offering to create and onboard a new employee. In addition, you will also use **<em>Slack</em>** and **<em>GMail</em>** as target systems. Since all these applications are available for personal use or on free trial, you will use one of these modes to get access to them. 

### Scenario Setup
In this exercise, you are implementing an integration scenario where your use-case is to integrate **<em>Bamboo HR</em>** with ***Slack*** and ***GMail*** accounts. Your Human Resources team has requested you to implement a scenario where the system should perform two actions as soon as a new employee is created:
1. Send a welcome email to the new employee, welcoming her/him to your company.
2. Send a notification in the ***Slack*** channel of the HR team, notifying them about the new employee and look into the subsequent onboarding tasks for the new employee. 

You will send a request to a HTTP endpoint, similar to a REST API. This request will contain the **ID** of the new employee. You will trigger the request using the Postman client. Here's an overview of the how the scenario architecture will look like:

<br>![Scenario architecture overview](/exercises/Images/Others/scenario_sol_diagram_1.png)

Here's a high-level overview of the steps you will perform:
1. You will get started with **Integration Suite** by activating **Cloud Integration** and **Open Connectors** capabilities.
2. In the **Open Connectors** capability, you will create two instances for **<em>Bamboo HR</em>** and **<em>Slack</em>** accounts.
3. In the **Cloud Integration** capability, you will deploy the credentials for your **<em>Bamboo HR</em>**, **<em>Slack</em>** and **<em>GMail</em>** accounts. 
4. You will then perform a connectivity test with your **<em>GMail</em>** account and import the server certificates into your **Cloud Integration** tenant. 
5. You design an integration flow in **Cloud Integration** capability to implement the aforementioned scenario. 
6. You will test the scenario by creating a new user in your **<em>Bamboo HR</em>** account and monitor how the message is processed in the **Cloud Integration** **<em>Monitor</em>** tab. 

## Requirements

There are no prior requirements to this exercise. You can perform this even if you do not have any experience with integration solutions. However, you will be able to derive a lot of value from this session if you have some knowledge on what **Integration Suite** is and how it helps with enterprise-wide integration needs. Here are a few links that can help you get started with it:
- [Simplify Integration with SAP Integration Suite](https://www.sap.com/documents/2018/11/6661f73c-277d-0010-87a3-c30de2ffd8ff.html)
- [Integration Suite in Service Catalog](https://discovery-center.cloud.sap/serviceCatalog/integration-suite)
- Lecture session from TechEd 2019: [Integrate it All with SAP Cloud Platform Integration Suite](https://www.youtube.com/watch?v=ikTKJ97GvRc)
- [Why SAP Integration Suite Should Be Your Preferred Choice for Enterprise-Wide (incl. Non-SAP) Integration](https://blogs.sap.com/2020/04/22/why-sap-cloud-platform-integration-suite-should-be-your-preferred-choice-for-enterprise-wide-incl.-non-sap-integration/#)

## Exercises

You can use this section as an index or table of contents. All pages have a link on top of the page to **Go back to Table of Contents** for easy navigation. 

### [Prerequisites](/exercises/Prerequisites_for_DEV165.md)
- [Create SAP Business Technology Platform Trial Account](/exercises/Prerequisites_for_DEV165.md#you-need-a-trial-account-on-sap-cloud-platform-you-can-create-a-new-trial-account-by-following-the-steps-in-this-tutorial)
- [Set up Integration Suite Trial](/exercises/Prerequisites_for_DEV165.md#set-up-integration-suite-trial-by-following-the-steps-mentioned-in-this-tutorial)
- [Create Cloud Integration Service Instance and Key](/exercises/Prerequisites_for_DEV165.md#you-should-create-a-service-instance-and-service-key-for-the-process-integration-capability-by-following-the-steps-in-this-exercise)
- [Create BambooHR Trial Account](/exercises/Prerequisites_for_DEV165.md#get-a-free-trial-account-on-bamboo-hr-here-register-for-bamboo-hr-trial)
- [Create Slack Account](/exercises/Prerequisites_for_DEV165.md#create-an-account-on-slack-here-get-started-with-slack-follow-the-instructions-to-create-an-account)

### [Setting Up Connectivity to Non-SAP Systems](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems.md)
- [Create Slack Instance](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.1.Create_Slack_Instance.md)
- [Create BambooHR Instance](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex-1.2.Create_BambooHR_Instance.md)
- [Deploy Open Connectors Credentials on Cloud Integration](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex.1.3.Deploy_Credentials_on_CloudIntegartion.md)
- [Configure Connectivity to GMail Account](/exercises/Ex-1.Setting_Up_Connectivty_to_Non_SAP_Systems/Ex.1.4.Set_Up_Gmail_Connectivity.md)

### [Design and Deploy Your Integration Flow](/exercises/Ex-2.Design_Your_IFlow.md)

### [Testing your Integration Scenario](/exercises/Ex-3.Testing_Your_Integration_Scenario.md)
- [Creating Employee on BambooHR](/exercises/Ex-3.Testing_Your_Integration_Scenario.md#creating-a-new-employee-in-bamboohr)
- [Testing your Integration Flow](/exercises/Ex-3.Testing_Your_Integration_Scenario.md#testing-your-integration-flow)

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2020 SAP SE or an SAP affiliate company. All rights reserved. This file is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
