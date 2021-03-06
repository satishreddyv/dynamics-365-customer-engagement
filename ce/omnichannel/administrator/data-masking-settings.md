---
title: "Create and manage data masking rules | MicrosoftDocs"
description: "Instructions on how to create and manage data masking rules in Omnichannel for Customer Service."
keywords: ""
author: lalexms
ms.author: lalexms
manager: shujoshi
applies_to: 
ms.date: 12/06/2019
ms.service: dynamics-365-customerservice
ms.topic: article
---

# Create and manage data masking rules

[!INCLUDE[cc-use-with-omnichannel](../../includes/cc-use-with-omnichannel.md)]

Data masking allows you to block sensitive data such as credit card information, social security numbers (SSN), or even profanity in a conversation. You can create a masking rule and define a regular expression to identify the sensitive information and replace it with the masked characters. Any text that is masked in a conversation will also be masked in the conversation transcript.

Masking rules can be configured to apply to messages sent by a customer, an agent, or both. You must make sure that that the masking rules you want applied are set to "Active"; otherwise they will not apply to the selection(s) you make.

   > [!div class=mx-imgBorder]
   > ![Data masking rules](../media/general-masking-rules.png "Data masking rules")


You can choose to:

- **Mask private agent data from the customer**: Data the agent sends is masked for both the customer and agent for live chat and SMS.
- **Mask private customer data from the agent**: Data the customer sends is masked for both the customer and agent for live chat, but only for the agent when using SMS. 


The following masking rules are provided out of the box:
- **Credit Card**: Masks the credit card number, if provided in a message.
- **Email**: Masks the email address, if provided in a message.
- **SSN**: Masks the social security number, if provided in a message.

As an administrator, you can delete or modify out-of-the-box masking rules and create new masking rules. Note that the expressions provided in the out-of-box rules can be edited if an admin wants to use an alternative. 

> [!NOTE]
> - Only an administrator can access and edit data masking rules.
> - Only 10 data masking rules, including out-of-the-box masking rules, can exist in Omnichannel for Customer Service. 

## Create a data masking rule

   > [!div class=mx-imgBorder]
   > ![Create masking rule](../media/new-masking-rule.png "Create masking rule")
    
1.	Sign in to Omnichannel Administration.

2.	Go to **Settings** > **Data Masking**.

3.	In **Masking rules**, select **New Masking Rule** under the ellipsis to create a new data masking rule. 

4.	On the **New Masking Rule** page, provide the following information:

    - **Name**: Name of the masking rule.

    - **Description**: Optional description of the masking rule.

    - **Regular expression**: Regular expression to identify the data to be masked.
        
5. Note that by default, the # symbol is used to mask the sensitive data. To test the data masking as per the specified regular expression, enter a value in the **Enter test data** field. The masked value is displayed in the **Masked test data** field.

   > [!div class=mx-imgBorder]
   > ![Email masking rules](../media/email-masking-rule.png "Email masking rules")

6. Select **Save**.

## Manage data masking rules

Once a masking rule is created, you can edit, activate, deactivate, or permanently delete it. 

   > [!div class=mx-imgBorder]
   > ![Manage masking rules](../media/masking-rule-card.png "Manage masking rules")

1.	Sign in to Omnichannel Administration.

2.	Go to **Settings** > **Data Masking Settings**.

3.  Under **Masking rules**, click the ellipsis to see the options for managing an existing masking rule.

4.  To activate, deactivate, or delete a masking rule, select the rule, and then click the appropriate action from the list.


