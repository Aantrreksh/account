---

copyright:
  years: 2015, 2021
lastupdated: "2021-09-22"

keywords: account types, Lite, free account, trial account, paid account, buy account, account difference, compare account, subscription, Pay As You Go with Committed Use, PayGo with Commit

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:row-headers: .row-headers}

# Account types
{: #accounts}

{{site.data.keyword.Bluemix}} has three different account types: Lite, Pay-As-You-Go, and Subscription. You get a free Lite account as soon as you sign up. Pay-As-You-Go and Subscription are billable account types and each offers different features. The PayGo with Committed Use billing model is available for the Pay-As-You-Go and Subscription account types. Compare each type of account and billing model to choose the one that best suits your needs.
{: shortdesc}

## Comparing accounts
{: #compare}

The following table provides a comparison of Lite, Pay-As-You-Go, and Subscription accounts. For more details about each account, see the sections that follow.

|                                         | Lite               | Pay-As-You-Go      | Subscription       | 
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Free Cloud Foundry memory** | 256 MB [^1]            |             |              |              |
| **[Free community buildpacks](/docs/cloud-foundry-public?topic=cloud-foundry-public-available_buildpacks)** | 186 GBH [^2]              |   186 GBH       |    186 GBH          |
| **Access to [Lite service plans](https://{DomainName}/catalog/?search=label:lite){: external}** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to all free plans**            |                    | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |  
| **Access to the full {{site.data.keyword.Bluemix_notm}} catalog** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to multiple Cloud Foundry regions** |               | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Guaranteed zero cost**                | ![Feature available](../icons/icon_enabled.svg) |  |         |
| **Discounted pricing**                  |                    |                    | ![Feature available](../icons/icon_enabled.svg) |
| **Fit for production use cases**        |                    | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg)|
| **Available for enterprise account hierarchy**         |                    |  | ![Feature available](../icons/icon_enabled.svg) |
| **Invoiced on monthly consumption**        |                    | ![Feature available](../icons/icon_enabled.svg) |                     | 
{: row-headers}
{: class="comparison-table"}
{: caption="Table 1. Comparison of {{site.data.keyword.Bluemix_notm}} accounts" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

[^1]: Not available for Lite accounts created after 12 August 2021. 

[^2]: Not available for Lite accounts created after 12 August 2021.

## Lite account
{: #liteaccount}

Sign up for a Lite account to start building your apps and exploring services with select free Lite plans, which are displayed with a **Lite** tag ![Lite tag](../icons/Lite.svg "Lite") in the {{site.data.keyword.Bluemix_notm}} console. Your Lite account doesn't expire and your credit card isn't required.

You have access to a single resource group that's created for you and named `Default`. All of your service's instances that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/account?topic=account-rgs#rename_rgs) for the detailed steps.

Each resource group is free. When you create a connection between a service that is managed by IAM and an app, you create an alias, which is a service instance, that counts toward your quota. See [Managing connections](/docs/account?topic=account-connect_app).
{: tip}

### What's available?
{: #lite-account-features}

Check out the following list of key features that are available in a Lite account:

* The account is free - no credit card required.
* The account never expires.
* You receive email notifications about your account status and quota limits.
* You can provision one instance of any service in the [{{site.data.keyword.Bluemix_notm}} catalog](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: external} that has a Lite plan.
* After 10 days of no development activity, your apps go to sleep. You can wake up your apps by continuing to work on them.
* After 30 days of no development activity, your service instances with Lite plans are deleted.

Only Lite accounts created before 12 August 2021 can use Cloud Foundry apps that can access up to 256 MB of free, instantaneous runtime memory per month. You can use one org in one {{site.data.keyword.Bluemix_notm}} region.
{: note}

## Pay-As-You-Go account
{: #paygo}

With a Pay-As-You-Go account, you can access the full {{site.data.keyword.Bluemix_notm}} catalog, including all free plans. You pay only for billable services that you use, with no long-term contracts or commitments. When you upgrade to a Pay-As-You-Go account, you receive a [$200 credit](/docs/account?topic=account-upgrading-account) to help get you started. You can use the $200 credit on {{site.data.keyword.Bluemix_notm}} products.

You can create multiple resource groups to easily manage quota and view billing usage for a set of resources. Your charges are based on your use of {{site.data.keyword.Bluemix_notm}} computing and services. If you use more than the free runtime and service allowances, you receive a monthly invoice that provides details about your resource charges.

Basic support is included with your {{site.data.keyword.Bluemix_notm}} Pay-As-You-Go. It is provided for non-production environments or workloads where traditional severities are not used and specific response times are not stipulated. Also, with a Pay-As-You-Go account, you can order Advanced or Premium support plans to get extra help with your production workloads. Learn more in [Support plans](/docs/get-support?topic=get-support-support-plans).

A subset of Pay-As-You-Go accounts are eligible for the new Pay-As-You-Go with Committed Use model. For more information, see [Pay as you go with Committed Use billing model](/docs/account?topic=account-accounts#commitment-model).

## Subscription account
{: #subscription-account}

Subscription accounts offer many of the same benefits as Pay-As-You-Go accounts, including access to the full {{site.data.keyword.Bluemix_notm}} catalog and the ability to create multiple resource groups. In addition, Subscription accounts provide discounts for platform services and support and more consistent billing through subscriptions.

When you purchase a subscription, you commit to a minimum spending amount for a certain period of time and receive a discount on the overall cost. For example, if you commit to spend $1,000 a month for 6 months, you might get a 5% discount. For the duration of the subscription, you get $6,000 of usage but pay only $5,700 for it. The larger the subscription, the better the discount. 

Large organizations and other users with large cloud workloads can benefit from the savings and predictable billing that are provided by subscriptions. {{site.data.keyword.Bluemix_notm}} offers multiple types of subscriptions to fit your usage needs. 

A subset of subscription accounts are eligible for the new Pay-As-You-Go with Committed Use model. For more information, see [Pay as you go with Committed Use billing model](/docs/account?topic=account-accounts#commitment-model).

### Platform subscriptions
{: #platform-subscriptions}

When you purchase a subscription for the {{site.data.keyword.Bluemix_notm}} platform, you get discounted credit that pays for services and other resources that you create from the [{{site.data.keyword.Bluemix_notm}} catalog](/catalog){: external}.

Your resource usage is deducted from your total subscription amount. Even if your usage varies from month to month, you get predictable, consistent billing. If your usage exceeds your total subscription amount, you're charged the non-discounted rate for the overage. For more information about tracking your subscription usage, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions).

Your subscription applies to most services in the catalog. However, some services use a specific pricing plan that requires you to purchase it separately.

### Support subscriptions
{: #support-subscriptions}

Basic support is included with your Subscription account. If you want to enhance your support experience for production-critical resources, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://cloud.ibm.com/catalog?contactmodule){: external} to purchase a support subscription for an Advanced or Premium support plan. With a support subscription, you commit to a monthly spending amount that goes towards your support costs. 

Support subscription credit is separate from any platform or service subscription credit in your account and can't be spent on resource usage. For more information, see [How subscription credit is spent](/docs/billing-usage?topic=billing-usage-subscriptions#subscription-basics).

### Service bundle subscriptions
{: #service-subscriptions}

Service bundle subscriptions give you access and credit towards a set of services within a particular domain that are targeted for popular use cases. You can choose from service bundles that span AI, analytics, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT), and cloud-native services. If your needs cross-multiple domains, you can purchase multiple service bundle subscriptions.

You can add services bundles to any type of existing account, including Lite accounts. Service bundle subscriptions are subject to the [{{site.data.keyword.Bluemix_notm}} Terms of Use](/docs/overview/terms-of-use?topic=overview-terms).

Service bundle subscriptions aren't available through the {{site.data.keyword.Bluemix_notm}} console. To learn more and purchase a service bundle, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://cloud.ibm.com/catalog?contactmodule){: external}.
{: tip}

After you purchase a service bundle subscription, you'll receive an email with a subscription code that you apply to add the bundle to your account. For more information about how to apply subscription codes, see [Subscription credit](/docs/billing-usage?topic=billing-usage-subscriptions#subscription-codes). When your service bundle expires or you use all of the credit, you can continue to use any of the services, with usage charged at the Pay-As-You Go rate.

### Expiring subscriptions 
{: #expiring-subscription-account}

When your subscription is about to expire, you are notified by email 60, 30, 14, and 1 day before the expiration date of the last subscription on the account. After your subscription expires, your account is converted to a Pay-As-You-Go account, which means you pay only for billable services that you use with no contracts or commitments. In addition, the discounts that are associated with your subscription account won't apply to the Pay-As-You-Go account. Go to the [Subscriptions](/billing/subscriptions) page to check whether any of your subscriptions are approaching their expiration date.

You can work with [{{site.data.keyword.Bluemix_notm}} Sales](https://cloud.ibm.com/catalog?contactmodule){: external} to renew your subscription account. 
