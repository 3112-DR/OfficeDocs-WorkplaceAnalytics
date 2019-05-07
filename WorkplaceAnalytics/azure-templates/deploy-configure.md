---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Deploy and configure Workplace Analytics Azure Templates 
description: Learn how to deploy and configure Workplace Analytics Azure Templates
author: madehmer
ms.author: v-midehm
ms.date: 05/07/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Deploy and configure Workplace Analytics Azure Templates

_These templates are only available as part of a Microsoft service engagement._

Before you can use Workplace Analytics Azure Templates for advanced data analysis, you need to do the following:

 - [Review the security considerations](#security-considerations)
 - [Confirm the prerequisites](#prerequisites)
 - [Deploy the templates](#deployment)
 - [Configure the templates](#configuration-add-users-and-assign-roles)
 - [Process the data](#process-the-data)

## Security considerations

Before deploying and configuring these templates, review the following security principles.

* Data is stored in your Azure subscription.
* Data is encrypted on disk and all access to and communication between Azure Resources and these templates are enabled and secured with the Secure Sockets Layer (SSL) certification.
* Authentication leverages Azure Active Directory.
* Authorization is set at the Azure Databricks and Azure Templates level by the Azure administrator who installs and sets up the Workplace Analytics Azure Templates.
* An Azure Template Configuration log is created during installation.

## Prerequisites

Before deploying Workplace Analytics Azure Templates, confirm or complete the following:

1. Confirm that [Workplace Analytics is set up](../setup/set-up-workplace-analytics.md) and ready to use.

2. Enable [Workplace Analytics data export](../data-access/data-access.md) for the Azure tenant.

3. Do the following for the Azure subscription that will host these templates and the data exported from Workplace Analytics:

   a. Confirm you have either an Azure Admin or an Azure Contributor role to deploy these templates.

   b. Get [applicable Azure AD permissions](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-how-applications-are-added) for yourself (or the admin doing the deployment) from your Office 365 global administrator.

   c. If the Workplace Analytics team is deploying the templates, confirm that vendor accounts are set up for the team and that the Technical Operations engineer also has the applicable Azure AD permissions to install and set up the templates.

## Deployment

1. Get an Azure deployment link for the Workplace Analytics Azure Templates from the Workplace Analytics team.

2. When prompted, select the Azure subscription.
3. For **Resource group**, you can select to:

   * **Create new** to create a new resource group.
   * **Use existing** to use an existing resource group and append the existing group with what's needed for this template, including any updates for any of the other templates in this group.

4. Select the applicable **Region** and then select **Next**.

5. On the **Deployment Review** page, confirm the selections and then select **Next**.
6. After the Azure Databricks workspace deployment is done, you are automatically signed in to Azure Databricks. If you’re not, you need to sign in manually.

7. On the **Databricks Token** page, you need to [generate the Azure Databricks Token](https://docs.azuredatabricks.net/api/latest/authentication.html#generate-a-token) for the App source.

8. On the **Summary** page, select a SKU for the data cluster, which must be about 30 percent larger than your Workplace Analytics dataset (ask your Workplace Analytics Admin for help with this), for the following Azure components:

   * [Azure Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview#resource-groups)
   * [Azure Blob storage account](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)
   * [Azure Databricks](https://docs.microsoft.com/azure/azure-databricks/)
   * [Azure SQL database](https://docs.microsoft.com/azure/sql-database/)
   * [Azure Analysis Services](https://docs.microsoft.com/azure/analysis-services/)
   * [Azure Web Apps (App Service)](https://docs.microsoft.com/azure/app-service/)
   * [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)

9. Select **Run** to deploy resources for the Azure components.

10. After the deployment is complete, open, copy, and save the deployed website link for the templates, as shown in the following graphic.

   >[!Important]
   >You must save this deployment link because you and the other users you add need it to configure and use the templates.

   ![Azure Templates deployment](./images/deployed-website-link.png)

## Configuration: Add users and assign roles

As the Azure Templates Admin, you can use the Admin page to manage security, privacy settings, and other administrative processes. Before other people can use the templates, you need to add them as users and assign them one of the following roles based on the tasks they need to accomplish with the templates:

* **Azure Templates Admin**

  * Can add other users and assign roles for the templates.
  * Can share the templates website link with other users.
  * Can share the link to access the [Azure Databricks Workspace](https://docs.azuredatabricks.net/user-guide/workspace.html) with the assigned Data scientists.

* **Analyst**

  * Can access, use, and customize the analytical templates available through the Workplace Analytics Azure Templates website link.
  * Can access, use, and customize the Power BI reports and dashboards connected to the Workplace Analytics Azure Templates.

* **Data scientist**

  * Can access, use, and customize the same analytical templates and Power BI reports and dashboards as the Analyst.
  * Can also access the Azure Databricks Workspace and use Python or R scripts to derive new insights.

**To add users and assign them roles:**

1. Use the website link (from the last step in Deployment) to open the Workplace Analytics Azure Templates.

2. Select **Admin** > **User Management** > **Add New User**.

3. Type the email address for the new user and select the applicable role for this user, as shown in the following graphic.

     ![Add Workplace Analytics users](./images/add-user.png)

## Process the data

After adding users, you need to process the Workplace Analytics data that you want to use with these templates:

1. In Azure Resource groups, locate the folder that the deployment just created. The new resource group name begins with **wpaappsrg** and includes the deployment date and time, as shown in the following graphic.
  
   ![Workplace Analytics Resource group](./images/resource-group-a.png)

    The new storage group contains a **rawdata** folder, as shown in the following graphic.

     ![Workplace Analytics rawdata folder](./images/rawdata-folder.png)

2. Confirm that the following .csv files are in the new **rawdata** folder:

   * **MailParticipants.csv**
   * **Mails.csv, MeetingParticipants.csv**
   * **Meetings.csv**
   * **PersonalHistorical.csv**

   If these .csv files are not already in the **rawdata** folder, you need to use the Azure Storage Explorer (or other comparable tool) to connect to the Azure storage group that currently stores your Workplace Analytics data set, and select and copy these files into that folder.

3. In the Workplace Analytics Azure Templates app, select **Admin** > **Scenario Execution**, select the **rawdata** folder, and then select **Process data**.

   ![Process Rawdata in Workplace Analytics](./images/rawdata-folder-n.png)

## Get support

* For help with Workplace Analytics Azure Templates, email your questions or feedback to wpaazuretemplates@microsoft.com.
* For setup and data analysis help with Workplace Analytics, open [Workplace Analytics](https://workplaceanalytics.office.com), select the **smiley face** icon (at the top of the UI), enter your question or feedback, and then select **Send**.
* For general help with Office 365 and Azure subscriptions, components, assigning licenses, and issues with user access and permissions, contact [Microsoft Support](https://support.microsoft.com/).

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Organization Network Analysis Azure Template](./organization-network-analysis.md)
* [Topic Analysis Azure Template](./topic-analysis.md)
* [Process Explorer Azure Template](./process-explorer.md)
