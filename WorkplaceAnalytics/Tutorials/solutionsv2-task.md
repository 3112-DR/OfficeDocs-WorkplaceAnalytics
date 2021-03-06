---
# Metadata Sample
# required metadata

title: Workplace Analytics solution walkthrough
description: A walkthrough of the steps required to create a plan by using the Workplace Analytics solution
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Solution walkthrough

You can use the solutions feature of Workplace Analytics to create improvement plans for employees, with the goal of changing their work habits for the better. By using solutions, you can create a plan, track it while it is in progress, and examine it after it completes.
 
People in the following roles can work on improvement plans in various ways:

 * **Analysts**, **limited analysts**, and **program managers** can identify groups of employees and opportunities for change, design and start plans, track plans that are underway, and examine plans that have completed.

<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: 
 * **Group managers** can start plans to improve the work habits of employees in their reporting structure. 
-->

 * **MyAnalytics users** participate in plans. For more information, see [The experience of plan participants](solutionsv2-participants.md).  

> [!Note]  
> If you have been assigned multiple roles, your capabilities are expanded. See [User roles in Workplace Analytics](../use/user-roles.md).

## Create a plan

**Role:** If you have the role of analyst, limited analyst, or program manager, the steps in the following sections apply to you.
<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: If you are a group manager, see [Plan creation for group managers](#plan-creation-for-group-managers). -->

To create a plan, follow these steps:

1. [Define the plan](#define-the-plan).

2. [Select a group](#select-a-group).

3. [Start the plan](#start-the-plan).

### Define the plan

**Role:** analyst, limited analyst, or program manager

1. Open [Workplace Analytics](https://workplaceanalytics.office.com). If prompted, sign in with your work account.

2. In **Solutions** > **New plan**, you can learn about and select the type of plan you want to create, such as a _Focus plan_, a _Collaboration plan_, or a _Wellbeing plan_.

    ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)

    > [!Note]  
    > On this page, the **Analyze** option is available only to people with the role of Analyst or Limited analyst.

3. Do you have a group of employees in mind for participation in a plan? If so, select **Start now** for the plan that you want that group to use, and go to step 5. If you do not already have a group picked out, go to [Find the group through analysis](#find-the-group-through-analysis), which is only available to people with an analyst role in Workplace Analytics.

4. For this example, select **Start now** for the _Focus plan_. This opens the **Set up new plan** pane for a Focus plan, which shows default values for the plan, such as its name:

    ![Set up a new plan](../images/wpa/tutorials/set-up-new-plan.png)

5. Go to [Select a group](#select-a-group) for next steps.

### Select a group

**Role:** analyst, limited analyst, or program manager

If you have a particular group in mind, you can identify the group either by [uploading a .csv file](#upload-a-csv-file) or by [using filters](#use-filters). (If you don’t have a group in mind, go to [Find the group through analysis](#find-the-group-through-analysis).

#### Upload a .csv file

1. Locate the .csv file to upload. The format of this file is simple: a list of email addresses in a single column. To obtain this file, you might have exported it from an HR system. 

2. Select **Upload .csv file**.

3. Select **Browse**, select a .csv file, and then select **Open**.
 
4. After the file is uploaded, select **Validate**.

5. After the group is successfully validated, you'll see any applicable warnings about the participants. For more information, see [Validation](solutionsv2-conceptual.md#validation).

6. Go to [Start the plan](#start-the-plan).

#### Use filters

1. Select **Use filters**. This opens the filter controls:

    ![Filter to find a group](../images/wpa/tutorials/filter-to-find-group.png)
 
2. Add filters to define your group. For example, select **FunctionType**, **Equals**, and **Marketing** in the fields to select the people who work in business strategy as your group. Optionally, add more function types to expand this group, or add more filtering criteria to refine the selection.

3. Select **Validate**. After the group is successfully validated, you'll see any  applicable warnings. For more information, see [Validation](solutionsv2-conceptual.md#validation).

4. Go to [Start the plan](#start-the-plan).

### Find the group through analysis

If you do not already have a group in mind for a plan, you can analyze the work habits of a larger segment of your organization to identify a group that could potentially benefit from a plan.

> [!Tip] 
> These steps work best after you’ve decided on the type of plan. Where might people in your organization have a problem? The available plans address too few focus hours (Focus plan), too many hours of meetings (Collaboration plan), or too much collaboration after the workday ends (Wellbeing plan).

   ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)

#### To identify a group by using filters and charts

1. On the **Solutions** page, in the card for one of the plans under **Available plans**, select **Analyze**. For this walkthrough example, select **Analyze** on the Focus plan card to open the **Filter and analyze** page.

2. (Optional) Although you just selected a plan, you can change it by selecting it (such as **after hours**) in **Filter and analyze**:

    ![Filter and analyze](../images/wpa/tutorials/filter-and-analyze.png)

3. Scope your data. To start, narrow the focus to specific people by applying filters in the **Page settings** pane. If it's not open, select **Settings and filters** at the top right of the page:

    ![Filter and analyze](../images/wpa/tutorials/settings-and-filters.png)

    ![Page settings](../images/wpa/tutorials/page-settings.png)

4. In **Page settings**, refine your selection of employees and change how the employees are grouped. For example, you can add a filter to show only employees in the East and Southeast regions and you can change the maximum number of groups to 10. After you finish adding filters, select **Apply**. The main section of the page changes to reflect these new changes.

5. To select a more precise group of people to include in the plan and continue with your analysis, you can use the **Select a question to change the view of your chart** options, such as: **Which groups attend the highest number of meetings?**

    ![Select a question](../images/wpa/tutorials/select-a-question.png)

    Selecting a question shows the answer to the question in the chart. By selecting a question that is relevant to the collaboration problem that you want to solve, you will see groups of employees who are most likely to exhibit symptoms of that problem. Selecting a question also orders the groups shown by their metrics (such as meeting hours, focus hours, or number of meetings) based on what the question asks about.

    The chart has vertical bars that represent different groups of people. Each bar that represents a group that meets or exceeds the minimum group size. Any groups smaller than the minimum group size do not show up in the chart because they are too small to analyze. (Also see [Minimum group size](solutionsv2-conceptual.md#minimum-group-size).) 

    <!-- For example, if the organization you are analyzing has a minimum group size of five, you can change it to a level that you consider more relevant for your organization. However, you cannot set the group size lower than five. In the following chart, the Data & Applied Sciences group contains fewer than five people, so its bar is shown as grayed out: -->
 
    See also [Available and selected employees](solutionsv2-conceptual.md#available-and-selected-employees).

6. Select one or more groups for analysis. To deselect a group, select it again. For more information about what happens with selected groups when you change settings on this page, see [Persistence of group selections](solutionsv2-conceptual.md#persistence-of-group-selections).

7. After you select one or more groups to analyze, you'll see additional information about this group’s work habits below the chart, such as:

    ![Three cards](../images/wpa/tutorials/three-cards-start-now.png)

8. After you identify the groups, select **Start now** to open **Set up new plan** to show the filters that you set in the charts and in page settings:

    ![Set up new plan](../images/wpa/tutorials/set-up-new-plan.png)

    > [!Note]  
    > Because these steps are using analysis to find the group and filters are an important part of that analysis, **Use filters** is the default option. However, you can select **Upload .csv file** to upload participant data instead.

9. (Optional) Change the selected filters or add new filters to further refine the group.

10. Select **Validate**. After validation completes, you'll see results with any applicable warnings, such as:

    ![Validation warnings](../images/wpa/tutorials/three-warnings.png)

11. Any warnings reduce the number of potential members in the group. If the remaining group size is above the minimum group size, you can proceed. If you are satisfied with the group at this point, select **Save as draft**, and then go to [Start the plan](#start-the-plan) for next steps.

## Start the plan

**Role:** analyst, limited analyst, or program manager

After the selected group validates successfully, you'll see insights about the group. They show you how the group’s numbers differ from company averages for the context that you chose. For example, if you chose to create a Focus time plan, Workplace Analytics shows metrics, such as the number of hours in meetings per week, that show why the people in this group could benefit from more focus time. Although these insights are informative, they are not interactive.

1. Select **Solutions** > **Manage** to see a list of plans, and then in **Show**, select **Drafts** to view your new plan.

2. (Optional) Select **Edit** next to your new plan to change the **Plan name** to a name more meaningful to you than the suggested value.

3. (Optional) Change the **Plan target** to a different value. Note that you can select only percentage-based targets, such as a 10% decrease in after-hours work.

4. (Optional) Set the **Plan duration**. To do this, set the start date. (You must choose a Sunday because all plans start on Sundays.) The plan’s end date is then calculated and shown.

5. (Optional) In **How Solutions will help**, select **See preview** to see examples of inline suggestions, dashboard information, and the email digest that people will experience while participating in the plan. Similar to plan insights, these previews are informative but not interactive:

    ![How solutions help](../images/wpa/tutorials/plan-preview.png)
  
    In these previews, you can see a brief description of "habits" that participants will learn about. Following these habits can help them reach their plan’s target. For example, rescheduling meetings that conflict with their focus time is a habit that can help a participant reach a target of increased focus time. Three habits are suggested for each plan type.

6. Select **Create plan**. This schedules the plan you chose for the group you selected to start and end on the dates that you set for the **Plan duration**. Or select **Save as draft** to finish up later or set the plan duration later.

## Track plans

**Role:** analyst, limited analyst, or program manager. 
<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: (For Group managers, see [Track progress (Group manager role)](#track-progress-group-manager-role)) -->

You can use the **Track** page to measure progress on the target since the plan started, as well as ROI for the plan.

### To track an active plan

1. Select **Solutions** > **Track**.
2. In **Progress for**, select the plan you want to see progress information about up to this point in time.

<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: 
## Plan creation for group managers

The role of group managers (GM) differs from other Workplace Analytics roles in that its scope is predefined and unalterable: All employees in the reporting structure under a GM are automatically assigned to their group. (The GM is also included in this group.)

For more information about roles in Workplace Analytics, see [User roles](../use/user-roles.md). 

### Create a plan (group manager role)

A plan that a GM creates automatically contains the data of the GM's group (the GM's reporting structure). All members of the group, including the GM, are automatically signed up for the plan. 

**Role:** Group manager

1.	As a GM, when you open Workplace Analytics, you go directly to the **Solutions** page: 

    ![Group manager view](../images/wpa/tutorials/gm-view-solns-2.png)
 
    This page shows three plans: _Focus plan_, _Collaboration plan_, and _Wellbeing plan_. Consider the type of plan that you want to create. The card for each plan describes the plan and offers **Start now** and **Analyze** options. 

2.	(Optional) For a particular plan, select **Analyze**. This shows read-only summary data about your team as a whole. This data pertains to that plan’s area of focus. For example, if you select **Analyze** on the _Focus plan_ card, you will see data that pertains to that plan with regard to your team. After you view this information, select **Start now** and then go to step 4.

    > [!Note]  
    > You cannot view summary data about your team if its size does not exceed the minimum group size. Workplace Analytics admins can set a minimum group size for GM teams that differs from the general Workplace Analytics setting for minimum group size. 

3.	For one of the three plans, select **Start now**. This opens the **Set up new plan** panel:

    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan.png) 

4.  Check the figure that is shown on this page for **Number of direct and indirect reports**. If this team size looks incorrect, contact your admin. They should examine the organizational data (HR) file and the manager hierarachy within that file for errors.
 
5.	Select **Validate**. 
  
    After validation finishes, Workplace Analytics shows any resulting details, warnings, and insights about the group. The warnings might indicate that some potential participants are ineligible for various reasons. If, after validation, there are enough participants for the plan, select **Start plan**. This shows the _Your plan was successfully submitted_ page: 
    
    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan-2.png) 
 
### Track progress (Group manager role)

After the plan starts, you can view the plan’s progress on the **Track** page. Note that you can see progress for your team only, and only for a single plan. This is because your team can have only one plan underway at a time. (You cannot subdivide your team into smaller groups that run different plans simultaneously.)
-->

## Related topics

[Solution: Introduction](solutionsv2-intro.md)  

[Solution: Participants](solutionsv2-participants.md)  

[Solution: Concepts](solutionsv2-conceptual.md)


