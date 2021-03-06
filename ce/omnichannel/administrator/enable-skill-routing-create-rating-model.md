---
title: "Enable skill-based routing and create rating model | MicrosoftDocs"
description: "Learn about how to enable skill-based routing and create rating model in Omnichannel for Customer Service app."
author: kabala123
ms.author: kabala
manager: shujoshi
ms.date: 10/15/2019
ms.service: 
  - "dynamics-365-customerservice"
ms.topic: article
---

# Preview: Enable skill-based routing and create rating model

[!INCLUDE[cc-use-with-omnichannel](../../includes/cc-use-with-omnichannel.md)]

[!include[cc-beta-prerelease-disclaimer](../../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - A preview is a feature that is not complete, as it may employ reduced privacy, security, and/or compliance commitments, but is made available before it is officially released for general availability so customers can get early access and provide feedback. Previews are provided “as-is,” “with all faults,” “as available,” and without warranty.​
> - This preview features does not come with technical support and Microsoft Dynamics 365 Technical Support won’t be able to help you with issues or questions.  If Microsoft does elect to provide any type of support, such support is provided "as is," "with all faults," and without warranty, and may be discontinued at any time.​
> - Previews are not meant for production use, especially to process Personal Data or other data that is subject to heightened compliance requirements, and any use of "live" or production data is at your sole risk.  All previews are subject to separate [Terms and Conditions](../../legal/dynamics-insider-agreement.md).

## Enable skill-based routing

To use skill-based routing, as an administrator, you must enable skill-based routing in the Omnichannel Administration app.

To enable skill-based routing, follow these steps:

1. Sign in to the Omnichannel Administration app.

2. Select **Skill Based Routing** under **Settings** in the sitemap.

3. Set the **Enable Skill Based Routing** toggle to **Yes**.

4. Select a rating model from the list for the **Rating Model** field. 
 
    If there is no rating mode, create a new rating model. To learn more, see [Create rating model](enable-skill-routing-create-rating-model.md#create-rating-model).

    After you select a rating model, the Rating Model Details section displays the **Name**, **Min Rating Value**, **Max Rating Value** and the **Rating Values (Rating Model)** grid.

    You can add a new rating value in the grid itself. To add, follow these steps:

    1. Select **+ New Rating Value**. The **Quick Create: Rating Value** pane appears.

    2. Specify a name and value.

    3. Select **Save and Close** to save and add the rating value.

5. Select **Save**.

## Rating value of skills

When you add a skill to an agent, you also need to rate the proficiency of the skill. This enables the system to do an exact or closest match against the requirement of a conversation and distribute the conversation accordingly. You can use the default rating model, edit it, or create a new one to match the needs of your organization.

You must provide the minimum and maximum rating value. Also, in the **Rating Values** section, you must create rating value text against each score between the minimum and maximum rating value. This text appears while updating an agent's skill and proficiency.

### Create rating model

1. Sign in to the Omnichannel Administration app.

2. Select **Skill Based Routing** under **Settings** in the sitemap.

3. Select **+ New Rating Model** in the **Rating Model** section. The **New Rating Model** page appears.

4. Specify the following in the **New Rating Model** page.

    | Tab | Field | Description | Example value  |
    |------------|-----------------|----------------|--------------------------------------------|
    | General | Name | Specify a name for the rating model. | Language rating model |
    | General | Min Rating Value | Provide a minimum rating value. | 1 |
    | General | Max Rating Value | Provide a maximum rating value. | 10 |

5. Select **Save** to save the rating model. After you save, the **Rating Values** section appears.

6. Select **+ New Rating Value**. The **Quick Create: Rating Value** pane appears.

7. Specify the following in the **Rating Value** page.

    | Field | Description | Value  |
    |-----------------|----------------|--------------------------------------------|
    | Name | Specify a name for the rating value. | ★★★★★★★★★★ <br> **Note:** <br>This is an example value.|
    | Value | Provide a value. | 10 <br> **Note:** <br>This is an example value.|

8. Select **Save and Close** to save and add the rating value to the grid.

9. Select **+ New** to add other rating values and repeat step 7 and 8.

10. Select **Save** to save the rating model changes.

### Recommended proficiency level

We recommend that you use a rating model with minimum value as 1 and maximum value as 10, and define the rating values accordingly.

For example:

| Rating value name | Value |
|-------------------|-------|
| ★★★★★★★★★★| 10 star|
| ★★★★★★★★★ | 9 star|
| ★★★★★★★★ | 8 star|
| ★★★★★★★ | 7 star |
| ★★★★★★ | 6 star|
| ★★★★★ | 5 star|
| ★★★★ | 4 star|
| ★★★ | 3 star|
| ★★ | 2 star|
| ★ | 1 star|

## See also

[Overview of skill-based routing](overview-skill-work-distribution.md)

[Set up skills and assign agents](setup-skills-assign-agents.md)

[Attach skills to conversation](attach-skills.md)
