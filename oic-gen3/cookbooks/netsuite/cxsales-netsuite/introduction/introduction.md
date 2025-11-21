# Introduction

Welcome to the hands-on workshop on integrating NetSuite with a CRM cloud application using Oracle Integration. In this training, you will gain real-world experience connecting NetSuite with Oracle CX Sales, Oracle’s cloud-based CRM solution. Through guided exercises, you’ll learn how to configure integrations, synchronize data, and automate workflows to streamline business processes across sales and finance operations.

By the end of this workshop, you will have the skills to use Oracle Integration for seamless communication and improved productivity between NetSuite and Oracle CX Sales, empowering your organization with unified, real-time business insights.

## Use Case: Oracle CX Sales Opportunity to NetSuite Sales Order

This use case demonstrates the use of Oracle Integration to receive a request from Oracle CX Sales when an Opportunity is won and automatically generate the corresponding Sales Order in NetSuite.

We will break down the use case in the following sequences:

1. The integration is triggered by Oracle CX Sales when an Opportunity is won.
2. Oracle Integration calls the Customer Service module to create a corresponding customer in NetSuite, receiving the Internal ID of the customer as response.
3. Oracle Integration calls the Inventory Item module to create a corresponding item in NetSuite, receiving the Internal ID of the inventory item as response.
4. Oracle Integration creates a corresponding Sales Order in NetSuite.

## About this Workshop

You will build an integration workflow that synchronizes **CX Sales Opportunities and NetSuite Sales Orders**. Instead of building the workflow from scratch, we will use an existing Recipe as baseline, and add customizations, in this workshop

### Workshop Flow

1. Use the AI Assistant to find the recipe **Synchronize Opportunities in Oracle CX Sales and B2B Service with Oracle NetSuite Orders**.
2. Install the recipe as a project.
3. Configure the connection for the REST, NetSuite and CX Sales adapters.
4. Add an action to capture details of the NetSuite Sales Order (e.g. persist as file, insert as Database record, send as email notification, etc).
5. Activate and run the recipe.

Estimated Workshop Time: 2 hours

### Objectives

Workshop goals:

* Gain a fundamental understanding of Oracle Integration concepts, such as Projects and Adapters.
* Create a Project using natural language with the built-in AI Assistant.
* Manage secure and reliable connectivity with Oracle CX Sales and NetSuite.
* Build and enhance integrations with Oracle CX Sales and NetSuite.
* Capture real-time events from Oracle CX Sales, such as Opportunity Won, into Oracle Integration for downstream processing.
* Create a Sales Order in NetSuite, immediately after an Opportunity is Won in Oracle CX Sales.
* Practice mapping and transforming data attributes between the different systems to ensure compatibility and accurate data processing.
* Run the integration by creating an Opportunity with Won status in Oracle CX Sales to initiate the creation of a corresponding Sales Order in NetSuite.
* Monitor the integration flow run in Oracle Integration.
* Log in to NetSuite and validate the new customer, inventory item records and sales order.

### Prerequisites

Before beginning the workshop, please verify that you have access to the following resources:

* Oracle Integration
* Oracle NetSuite
* Oracle CX Sales
* Oracle Autonomous Database (Optional)
* Chrome browser

## Learn More

* [Get Started with Oracle Integration 3](https://docs.oracle.com/en/cloud/paas/application-integration/index.html)
* [Using the Oracle NetSuite Adapter with Oracle Integration 3](https://docs.oracle.com/en/cloud/paas/application-integration/netsuite-adapter)
* [Using the Oracle CX Sales and B2B Service Adapter with Oracle Integration 3
](https://docs.oracle.com/en/cloud/paas/application-integration/sales-adapter)
* [Synchronize Opportunities in Oracle CX Sales and B2B Service with Oracle NetSuite Orders
](http://docs.oracle.com/en/cloud/paas/application-integration/sync-cx-opportunities)

## Acknowledgements

* **Author:** Ravi Chablani, Product Management - Oracle Integration
* **Last Updated:** Ravi Chablani, November 2025
