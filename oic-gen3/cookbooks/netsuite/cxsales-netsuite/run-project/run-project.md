# Run the Project

## Introduction

This lab walks you through the steps to run the project created in the previous lab. That requires accessing Oracle CX Sales and submitting an Opportunity, which will trigger the integration to orchestrate the Sales Order creation in NetSuite.

### Objectives

* Create an Opportunity in Oracle CX Sales.
* Monitor the results from the Observability Dashboard in Oracle Integration.
* Verify the Sales Order in NetSuite.

### Prerequisites

This lab assumes you have:

* Completed all prerequisites successfully
* All Integrations and Connections in **Configured** status

## Task 1: Create an Opportunity in Oracle CX Sales

1. Log in to the Oracle CX Sales instance using a valid user account with privileges to create an Opportunity.

2. Click **Opportunities** on the home page.

3. On the **Opportunities** page, click **Create Opportunity (+)**.

4. On the **Create Opportunity** page, enter the following details:

    * Enter a name for the opportunity. Example: `RC-20251102-1506`. Keep note of this code as you will need it later.
    * Select an account for the opportunity (mandatory). Example: `ABC Application Software`
    * Set a close date. Example: `<set one week from today>`
    * Leave all other fields as default.
    * Click **Save and Continue**.

5. On the **Summary** page, enter the following details:

    * Select **Won** in the Status field. 
    * Choose a suitable reason in the Win/Loss Reason field. Example: `Product`

6. Under the **Products** section, click **Add** to add a product line with the following details:

    * With Group selected in the Type field, select a product group in the Name field. Example: `Fit Cardio`
    * Enter **Quantity**.
    * Enter **Estimated Price**.

7. Click **Save and Close**.

## Task 2: Monitor the results from the Observability Dashboard in Oracle Integration

The Opportunity Event from Oracle CX Sales will trigger the main integration, which will trigger two child flows. We will monitor these three integrations from the Observability dashboard.

1. From the Oracle Integration console, click on Projects.

2. In the project workspace, click **Observe** tab, then **Instances**.

    You'll see a list of integration flows (instances) which are either running or completed. Find the integrations which were triggered after you created an Opportunity in Oracle CX Sales.

3. Find each of the below instances and click on the **View Details** (eye) button:

    a. Sales Order: Look for the entry under **Primary Identifier** column where **Name** has the value of your Opportunity number.

    b. Customer: This flow contains a switch statement to determine if a customer record already exists with corresponding id. If it does not exist, then a customer will be created.

    c. Inventory Item:  This flow contains a switch statement to determine if an inventory item record already exists with corresponding id. If it does not exist, then an inventory item will be created.

4. Ensure each instance has status **Succeeded**. If the status is **Error** or **Aborted**, then you must troubleshoot to identify root cause.

## Task 3: Verify the Sales Order in NetSuite

If the Create Sales Order integration completed with status **Succeeded**, then a Sales Order was created in NetSuite. We will verify the details of this order. Additionally, we will also review the corresponding customer and inventory item records.

    ```
    Note: Ensure you access the NetSuite instance as a user with sufficient privileges to check list sales order, customer, and inventory item records.
    ```

1. Log in to the NetSuite instance.

2. Verify the sales order by navigating to **Transactions** > **Sales** > **Enter Sales Orders** > **List**.

3. Verify the customer record by navigating to **Lists** > **Relationships** > **Customers**.

4. Verify the inventory item record by navigating to **Lists** > **Accounting** > **Items**.

## Acknowledgements

* **Author:** Ravi Chablani, Product Management - Oracle Integration
* **Last Updated:** Ravi Chablani, December 2025
