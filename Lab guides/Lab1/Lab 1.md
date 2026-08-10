# Lab 1: Setting up and managing Pay-as-you-go billing in Microsoft 365 copilot

Create a Pay-as-you-go billing policy from scratch, then connect,
monitor, and retire it across its full lifecycle in the Microsoft 365
admin center.

|  |  |
|---|---|
| **Estimated duration** | 30 minutes |
| **Level** | Intermediate |
| **Required role** | Global administrator or Billing administrator |
| **Environment** | Microsoft 365 test/lab tenant with an Azure subscription |

## Lab overview

You first build a policy from the ground up — billing details, user
scope, and an optional budget — then connect it to a Copilot service. In
the second half you manage that same policy: connecting a service after
the fact, adding a budget later, monitoring spend, and finally
disconnecting the service and deleting the policy.

Pay-as-you-go billing lets your organization pay only for the Copilot
Credits it consumes, using an Azure subscription as the billing
backbone. Working through the create-then-manage flow end to end gives
you a complete operational picture rather than an isolated setup task.

## What you will learn

- Create a **Pay-as-you-go billing** policy with billing details,
  subscription, resource group, and region.

- Scope a policy to all users or to a specific group.

- Set an optional budget with reset cadence and percentage-based
  spending alerts.

- Connect a **Pay-as-you-go** service to a policy — both during creation
  and afterward.

- Add a budget to a policy that was created without one.

- Monitor organizational spending in the admin center and in Microsoft
  Cost Management.

- Disconnect a service and delete a billing policy cleanly.

## Prerequisites

- Access to a Microsoft 365 test/lab tenant.

- An account with the Global administrator or Billing administrator
  role.

- An existing Azure subscription (or permission to create one) to
  associate with the policy.

- At least one security or distribution group in the tenant for policy
  scoping.

[TABLE]

# Part A — Create a pay-as-you-go billing policy

# Exercise 1 — Create a billing policy and add billing details

# 

1.  Sign in to the **Microsoft 365 admin centre**
    [admin.microosft.com](%3ca%20href=%22https:/login.microsoftonline.com/common/oauth2/authorize?client_id=00000006-0000-0ff1-ce00-000000000000&amp;response_type=code%20id_token&amp;scope=openid%20profile&amp;state=OpenIdConnect.AuthenticationProperties%3Dt6jMHseTkWXAad9AB7ThzZlS8WzT6LARlRE5VxRDYrtvO1MOLYRMJbbRyZuZDUz8F9NMKbz_lQZ_SCfNSpR9c7mxxoRN4WBCM9J5PRVNN1_7_bXrwh4oIDy9ICK8NRDbol14toaeC41zQEWIRZDC2DHOv-dbgACTJNYB2V_jsZmke4cTCsgqN_Y1YDWlXCHD2U--bp__RFqVNuRl4BsmOg&amp;response_mode=form_post&amp;nonce=639209129157633155.NDI4MjZjNGEtYzg3My00OWY4LWIyNWYtMmU0NDQ3YzUzNWU1MjQ2MzNmZTQtNDJhMi00NGFlLTk3MzQtYTBiZjE4MTM2Nzgx&amp;redirect_uri=https%3A%2F%2Fadmin.microsoft.com%2Flanding&amp;ui_locales=en-US&amp;mkt=en-US&amp;client-request-id=0ab614a7-a1b3-4682-9df2-d9494d40a0b6&amp;claims=%7B%22id_token%22%3A%7B%22xms_cc%22%3A%7B%22values%22%3A%5B%22CP1%22%5D%7D%7D%7D&amp;x-client-SKU=ID_NET472&amp;x-client-ver=8.19.2.0%22%3eSign%20in%20to%20your%20account%3c/a%3e),
    enter the **Username and Password** ![A screenshot of a computer
    AI-generated content may be incorrect.](./media/image1.png)

> ![](./media/image2.png)

- Click **Yes** to stay signed-in

> ![](./media/image3.png)

- Approve the **MAF** if asked

> ![A screenshot of a sign in AI-generated content may be
> incorrect.](./media/image4.png)

2.  In **M365 admin centre** home page, go to **Copilot** from left pane
    \> **Billing & usage.**

> ![](./media/image5.png)

3.  On the **Billing policies** tab, select **Add a billing policy.**

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image6.png)

4.  On the Billing details page, enter a name for the billing policy.

- **Billing policy name:** Copilot Chat PAYG - Pilot Group

> ![A screenshot of a computer screen AI-generated content may be
> incorrect.](./media/image7.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image8.png)

- **Select the resource group**: ODL-Copilot-2335709

5.  From the **Subscription** drop-down list, select an existing **Azure
    subscription,** or select Create a new subscription.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image9.png)

6.  From the Resource group drop-down list, select an existing resource
    group, or select Create a new resource group.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image10.png)

7.  From the **Region** drop-down list, select a region **(East-US)**.
    This selection determines where the tenant ID and usage data are
    stored.

> ![](./media/image11.png)

8.  Read the Pay-as-you-go billing terms of service and privacy
    statement, then select the I accept the Pay-as-you-go billing terms
    of service checkbox.

> ![](./media/image12.png)

9.  Select Next.

# Exercise 2 — Add users or groups to the billing policy

[TABLE]

10. On the Choose users page, select All users or a Specific group. If
    you select Specific group, search for and add a single group.

> Click on **Add a group** select the **OTU WA MSB-106259** from the
> dropdown
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image13.png)
>
> Note: When you select a group, only the first 1,000 groups are
> displayed, in alphabetical order.

11. Select **Next**.

# Exercise 3 — Set a budget for the billing policy 

[TABLE]

12. On the Budget page, if you want to set a budget, select the Set a
    budget for this policy checkbox.

> Set budget- $ 200

13. Enter a value for the budget limit.

**Select when to reset the budget spending:**

- On the first day of the month.

- On the first day of the quarter.

- On the first day of the year.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image14.png)

14. When you finish configuring the budget, select Next.

# Exercise 4 — Review, create, and connect during setup

15. On the Review and create policy page, verify all the details you
    entered. Make any needed changes, then select Create policy.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image15.png)
>
> ![](./media/image16.png)

16. On the New billing policy created page, select Connect your services
    to connect the policy to a pay-as-you-go service now, or select Done
    to connect it later (Part B).

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image17.png)

17. If you selected Connect your services, you're redirected to the
    Pay-as-you-go services tab. Select the name of the service to
    connect.

> Service selected: Microsoft 365 Copilot Chat
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image18.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image19.png)

18. In the Manage billing policy connections panel, find the policy to
    connect to, then set the Connection status toggle to Connected.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image20.png)
>
> ![A screenshot of a chat AI-generated content may be
> incorrect.](./media/image21.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image22.png)

19. To apply Microsoft Copilot Studio credits to Microsoft 365 Copilot
    Chat, select the Apply available credits to Microsoft 365 Copilot
    Chat checkbox. When credits run out, billing switches to the
    pay-as-you-go policy to keep the service active.

[TABLE]

20. Select Save, then close the side panel.

> ![A screenshot of a chat AI-generated content may be
> incorrect.](./media/image23.png)

# Exercise 5 — View spending for your organization

21. In the Microsoft 365 admin center, go to Copilot \> Billing & usage.

> ![](./media/image24.png)

22. On the Billing policies tab, select **Copilot Chat PAYG- Pilot
    Group** billing policy.

> ![](./media/image25.png)
>
> ![](./media/image26.png)

23. In the top bar select the Budget tab. The Spending option displays
    data for the current month and includes a chart covering the last
    six months.

> ![](./media/image27.png)
>
> ![](./media/image28.png)

24. Click on **Users** tab to view the users associated with billing
    policy, Click **Edit** to change the users group

> ![](./media/image29.png)

25. Click Close from top right corner to exit the pop-up

> ![](./media/image30.png)

You can also monitor pay-as-you-go usage and costs in Microsoft Cost
Management for Azure. Ensure you have at least read access to the
billing resource group.

# Exercise 6 — Disconnect a pay-as-you-go service

26. In the Microsoft 365 admin center, go to Copilot \> Billing & usage.

> ![](./media/image31.png)

27. On the Billing & usage page, select the Pay-as-you-go services tab.

> ![](./media/image32.png)

28. Select the service you want to disconnect.

> ![](./media/image33.png)

29. In the Manage billing policy connections panel, set the Connected
    toggle to off.

> ![](./media/image34.png)
>
> ![](./media/image35.png)

30. Select Save, then close the side panel.

> ![](./media/image36.png)

***Important:** If multiple services connect to a single policy, repeat
these steps for each service.*

[TABLE]

# Exercise 7 — Delete the billing policy

*After you disconnect a **pay-as-you-go service**, you can delete the
billing policy.*

31. In the **Microsoft 365 admin center**, go to **Copilot** \>
    **Billing & usage.**

> ![](./media/image37.png)

32. On the **Billing policies** tab, select a billing policy, then
    select **Delete billing policy**.

> ![](./media/image38.png)![](./media/image39.png)

33. Accept the confirmation dialog. The process disconnects any services
    still connected to the policy.

> ![](./media/image40.png)

## Lab validation checklist

- A pay-as-you-go billing policy exists on the Billing policies tab with
  the name you chose.

- The policy is scoped correctly (All users or your specified group).

- A budget with a reset cadence and at least one alert threshold is
  attached to the policy.

- A Copilot service shows Connected against the policy on the
  Pay-as-you-go services tab.

- Spending data is visible on the Budget tab and (optionally) in
  Microsoft Cost Management.

- The service can be disconnected and the policy deleted without errors.

## Summary

You created a Microsoft 365 Copilot pay-as-you-go billing policy from
scratch — configuring billing details, user scope, and an optional
budget — and connected it to a Copilot service. You then managed that
policy end to end: connecting a service after creation, adding a budget
later, monitoring spend in both the admin center and Microsoft Cost
Management, and finally disconnecting the service and deleting the
policy. You now understand the complete pay-as-you-go billing lifecycle
in a single continuous workflow.
