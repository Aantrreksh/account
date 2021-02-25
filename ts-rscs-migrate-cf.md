---

copyright:

  years: 2015, 2021

lastupdated: "2021-02-25"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, Cloud Foundry instance, migrate, resource group, migration error, Cloud Foundry access, Cloud Foundry roles

subcollection: account

content-type: troubleshoot

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I migrate a Cloud Foundry service instance to a resource group?
{: #ts_migrate_instance}
{: troubleshoot}

As a user in the {{site.data.keyword.Bluemix}} account, you're having trouble when you try migrate a service instance to a resource group.
{:shortdesc}

You can't migrate an eligible Cloud Foundry instance. 
{: tsSymptoms}

If you're unable to migrate an eligible instance, you might not have the correct access. 
{: tsCauses}

You must have specific access to migrate an instance. To check out what access you have, click **Manage** &gt; **Access (IAM)** from the console menu bar, and then click **Users**. Click your name and review your access policies for assigned IAM roles and Cloud Foundry access to view which orgs you have access to and your assigned Cloud Foundry roles. 
{: tsResolve}


