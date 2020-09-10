---

copyright:
  years: 2020
lastupdated: "2020-09-10"

keywords: account known issues, catalog known issues, catalog management, private catalogs, catalogs, IBM Cloud catalog, IAM, maximum limits for creating IAM resources, delete users, Cloud Foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}
{:tip: .tip}

# Known issues and limitations
{: #known-issues}

Known issues and limitations include not being able to restrict access to some products in the {{site.data.keyword.cloud}} catalog, the maximum limits for creating {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) resources, and not being able to delete users from accounts that have too many Cloud Foundry orgs. 
{:shortdesc}

## Catalog management settings don't apply to some {{site.data.keyword.IBM_notm}} products
{: #settings-noapply}

Turning off {{site.data.keyword.cloud_notm}} catalog visibility or excluding all {{site.data.keyword.IBM}} products from the catalog or your private catalogs doesn't apply to the following products. Users in your account can still create instances of them by using an API or the CLI.

* {{site.data.keyword.block_storage_is_short}}
* {{site.data.keyword.vpx_full}}
* Fortigate Security Appliance
* Hardware Firewall
* Hardware Firewall Dedicated
* {{site.data.keyword.backup_notm}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.blockstorageshort}}
* {{site.data.keyword.cloud_notm}} Content Delivery Network
* {{site.data.keyword.cloud_notm}} Direct Link
* {{site.data.keyword.cloud_notm}} Direct Link on Classic
* {{site.data.keyword.IBM_notm}} {{site.data.keyword.openwhisk_short}}
* {{site.data.keyword.cloud_notm}} Gateway Appliance
* {{site.data.keyword.cloud_notm}} Hardware Security Modules
* {{site.data.keyword.containerlong_notm}}
* {{site.data.keyword.cloud_notm}} Load Balancer
* {{site.data.keyword.cos_full_notm}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.BluVirtServers_short}}
* Load Balancer for VPC
* Subnets and IPs
* Virtual Private Cloud
* Virtual Server for VPC
* VLANs
* VPN
* VPN for VPC

## {{site.data.keyword.Bluemix_notm}} IAM limits
{: #iam_limits}

The following table lists the maximum limits for IAM resources. These limits apply to any user who can create IAM resources. If a limit is exceeded, you receive an exception and are not allowed to create any new resources beyond that limit.
{:shortdesc}

| Resource                               | Max  |
|----------------------------------------|------|
| Access groups per account              | 500  |
| Access groups per user                 | 50   |
| Service IDs per account                | 2000 |
| API Keys per identity                  | 20   |
| Dynamic rules per access group         | 5    |
| Policies per account                   | 2010 |
| Policies per subject within an account | 500  |
| Custom roles per account               | 40   |
{:caption="Table 1. IAM Account Limits" caption-side="top"}

A maximum of 1,000 policies and service to service authorizations within one account is recommended to ensure optimal performance within your account. For more information about limiting the number of policies in your account, see the [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup).
{: tip}

If you need to check the number of policies in your account or request an increase in the account limit, see [Managing policy limits](/docs/account?topic=account-policy-limits).

## Resource group is inactive with state: SUSPENDED
{: #resource_inactive}

When the process to reactivate or upgrade a suspended account does not complete successfully, you might see the following error when creating a new service: "The resource group <name> is inactive with state: SUSPENDED"
 
To resolve the issue, [open a support case](/docs/get-support?topic=get-support-open-case) and include the group name from the error message in the case details.

