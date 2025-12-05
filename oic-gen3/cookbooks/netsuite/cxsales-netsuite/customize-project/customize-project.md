# Customize Project

## Introduction

This lab walks you through the steps to customize and activate the project.

### Objectives

* Customize project by modifying integration flows
* Activate the CX Sales to NetSuite Project using Deployment option

### Prerequisites

This lab assumes you have:

* Completed the previous lab successfully

## Task 1: Customize Project

The main flow uses a filter expression to only trigger when an Opportunity is Won event occurs. You will modify the integration by adding a parameter to also filter for a custom value entered in a text box.

1. In the **Project** workspace, click **Design** tab.

2. Click on the **Opportunity to Order Sync** integration. Ensure you are in EDIT mode. 

3. 

## Task 3: Activate Project

After the connections have been configured, you will activate the project. Project activation or deactivation results in bulk processing of the selected integrations in the project. Before you can activate a project, ensure there is a project deployment and explicitly select the integrations and their versions to include in the deployment.

1. In the **Project** workspace, click **Deploy** tab.

2. With the default project deployment selected, hover to the right and click **Activate**.

    The **Activate project** panel opens.

3. Select the default deployment name, choose **Audit** tracing level, then click **Activate**.

    Wait until all integrations in the Project workspace have status **Active**.

    ```
    Note: If there are deployments available or if you want a separate one, then create a project deployment under the Deploy tab and select the specific integrations and integration versions to include in the project deployment.
    ```

You may now **proceed to the next lab**.

## Learn More


## Acknowledgements

* **Author:** Ravi Chablani, Product Management - Oracle Integration
* **Last Updated:** Ravi Chablani, December 2025
