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

    This open the Design canvas.

3. Double-click the **Trigger** action. Alternatively, you can click on the **Overflow menu (...)**, then **Edit** option.

4. On the **Edit Basic Info** panel, click **Continue**.

5. Scroll down until the **Filter Expr for Opportunity Updated Event** text area.

6. Replace below code

    ```
    $eventPayload/ns3:result/ns2:StatusCode="WON"
    ```
    With this code

    ```
    <copy>
    $eventPayload/ns3:result/ns2:StatusCode="WON" and $eventPayload/ns3:result/ns2:GSECode_c="<unique-value>"
    </copy>
    ```

7. Substitute the `<unique value>` with a distinct value (Example: your initials or first name).

    ```
    Note: Remember this unique value as you will need it when you create an opportunity in the testing phase.
    ```

8. Click **Continue**, then **Finish**.

9. Click **Save** at the top of the screen to persist all changes.

## Task 2: Activate Project

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
