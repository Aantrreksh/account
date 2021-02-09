---

copyright:
  years: 2015, 2021
lastupdated: "2021-02-09"

keywords: platform notifications, email notifications, IBM Cloud notifications, notification preferences, email preferences, user notifications, infrastructure notifications

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:external: target="_blank" .external}


# Setting email preferences for notifications
{: #email-prefs}

Depending on your {{site.data.keyword.Bluemix_notm}} account type, you can choose to receive email notifications about {{site.data.keyword.Bluemix_notm}} platform-related items, such as announcements, billing and usage, additional notification preferences, and ordering. You can also update your preferences to receive email notifications about resource-related items, such as incidents, maintenance, security bulletins, or resource activity on the Notification preferences page. These notifications are for only the resources you use.
{: shortdesc}

To view the Notifications preferences page, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) in the {{site.data.keyword.Bluemix_notm}} console, and then click **Profile** > **Notification preferences**.

You can also visit the page if you click the **Notifications** icon ![Notification icon](../icons/Notification.svg) in the {{site.data.keyword.Bluemix_notm}} console. Then, click **Manage email preferences** in the upper-right corner of the page. 

If you set your email preferences but aren't receiving email notifications, make sure emails that are sent from `no_reply@cloud.ibm.com` aren't blocked or in your spam folder. See [Why am I not receiving email notifications?](/docs/account?topic=account-ts_email_notifications) for more information. 
{: tip}

## Setting platform notifications
{: #setting-platform-notifications}
{: help} 
{: support}

You can choose to receive email notifications about {{site.data.keyword.Bluemix_notm}} platform-related items across your account. When you set {{site.data.keyword.Bluemix_notm}} platform notifications, you receive email notifications that are associated with only the platform. You do not receive email notifications about events that are associated with {{site.data.keyword.Bluemix_notm}} services.

Your platform email notifications settings are tied to your profile, not the account. In other words, any changes to platform notification settings are shared across your profile in all accounts that you have access to.

  * To stay up to date with changes to the {{site.data.keyword.Bluemix_notm}} platform and products, go to **Notification preferences** > **Announcements**. To select a subcategory, set **Emails** to the on position.
  * To receive notifications about invoices, payments, subscription and promo codes, or spending and usage warnings, select **Billing and usage**. Then, click **Manage** to set up spending notifications.
  * To receive updates about the status of your infrastructure orders, select **Ordering**.  
  * To manage the notification distribution list in regard to your account, subscriptions or security and compliance alerts, click **Additional notification preferences** > **Manage**.

  By default, all {{site.data.keyword.Bluemix_notm}} platform notifications are turned off.
  {: tip}

## Setting resource notifications
{: #setting-resource-notifications}
{: help} 
{: support}

You can set your preferences to receive resource-related notifications for incidents, maintenance, security bulletins, and resource activity updates.  

1. In the console, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile**.
2. Click **Notification preferences** > **Resource**.
4. Select from the following options: 

  * Receive notifications about events that can cause an outage or restrict functionality. You can receive notifications for all incident severity levels (1, 2, 3, 4) or just a subset. 
  * Receive notifications about any important maintenance that keeps the platform operating at optimal status. You can receive notifications for all impact levels (high, medium, low), or just a subset.
  * Receive notifications about security vulnerabilities and the required actions to take.
  * Receive notifications about resource activity, such as status and service updates. 

  By default, all {{site.data.keyword.Bluemix_notm}} resource notifications are turned off.
  {: tip}

## Setting user notifications for classic infrastructure resources
{: #setting-user-notifications}

Setting user notifications is available for classic infrastructure resources only. If you're an account owner, you can subscribe users in your account to notifications for a specific set of developer services like {{site.data.keyword.autoscaling}} and Raid Alert Monitoring. When the user is subscribed to a service, they receive emails about that service. Changes that you make for a user take effect only for future notifications. A user is not notified about events that occurred before you set up notifications.

Users in your account receive notifications for the following types of important operational events:

  * Unplanned infrastructure issues or outages: Issues that might cause an outage based on certain conditions for specific customers.
  * Planned service or scheduled maintenance: Maintenance that is required to keep the infrastructure operating at optimal status.
  * Security vulnerabilities: The affected area is isolated. A patch is created to close the vulnerability, and tests are performed on the patch to ensure that no collateral function is affected.

The timing of the notification varies depending on whether the event is unplanned, planned, or scheduled. The {{site.data.keyword.BluSoftlayer_notm}} infrastructure policy is to remedy problems as quickly as possible to remove or minimize the risk of further issues that might have a larger impact. Sometimes even planned maintenance is performed with only a short advanced notification.

To set up subscription notifications for your users, complete the following steps:

  1. In the console, go to **Manage > Account**, and select **Subscriptions**.
  2. Select a service from the table.
  3. In the Subscribed column, select **Yes** for the user who wants to receive notifications.

  You can also set up subscriptions under **Additional notification preferences** category.

    To easily find the user you're looking for, click **Filter** and filter by given name, surname, or user name.
    {: tip}

### Assigning required access to receive notifications
{: #required-user-notification-access}

Users that you set up for classic infrastructure notifications must also have access to the devices, network, and services that send the notifications.

To ensure that a user has the correct access, go to **Manage** > **Access (IAM)** > **Users** in the console, select their name, and then select **Classic infrastructure**. From the **Permissions** option, assign users the following classic infrastructure permissions.

| Permission Category | Required Permissions |
| ------------------- | -------------------- |
| Device              | View Hardware Details <br/> View Virtual Server Details |
| Network             | Manage Network Gateways |
| Services            | Manage Lockbox <br/> Storage Manage |
{: caption="Table 1. Required classic infrastructure permissions for receiving user notifications" caption-side="top"}

Then, go to **Devices** to assign a user access to the specific devices and device types. You can also enable future access to all devices of a certain type. For more information about setting classic infrastructure permissions, see [Managing classic infrastructure access](/docs/account?topic=account-mngclassicinfra).

## Adding users to a distribution list 
{: distribution-list}

You can manage the notification distribution list under **Additional notification preferences**. You can create a list of up to 10 email addresses that can receive account-wide notifications. Users that are added to the distribution list are notified about any event that's affecting the account. You must have the editor role or higher on the account management service to add users to the distribution list. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

Adding users to the distribution list is different than updating your Notification preferences. Users added to the distribution list by the account owner receive any incident, maintenance, announcement, or security bulletin that appears on the account owners [{{site.data.keyword.Bluemix_notm}} - Notifications](https://cloud.ibm.com/notifications){: external} page. 
{: note}

To add users to a distribution list, complete the following steps: 
1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account**, > **Notification distribution list**. 
2. Select **Add**. 
3. Enter a name identifier and an email address. 

  You can add up to 10 email addresses to the distribution list. Users that are added don't need be IBM Cloud users. You can add any email address to the distribution list. 
  {: note}
  
4. Click **Add**. 

### Unsubscribing from the distribution list 

To unsubscribe, use the unsubscribe link in the footer of any email that is sent from the distribution list. 

