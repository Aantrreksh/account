---

copyright:

  years: 2021

lastupdated: "2021-08-31"

keywords: troubleshooting software, troubleshooting resources, software instance, suspended, removed, deleted

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

# Why is my software instance not usable?
{: #ts-swinstance-unavail}
{: troubleshoot}

When a software product is removed or temporarily suspended from the {{site.data.keyword.cloud}} catalog, any related software instances are not usable.
{: shortdesc}

When you access your software instance from your resource list, the following error message is displayed:
{: tsSymptoms}

`The instance is not usable.`

This problem happens if the software product that is used to create the instance is removed or suspended from the {{site.data.keyword.cloud_notm}} catalog. Suspension is a temporary state while removal is permanent. In both states, the software instance cannot retrieve necessary information from the product, including updates for new features and fixes for vulnerabilities.
{: tsCauses}

In the case of the software being removed from the catalog, you should delete your instance. If necessary, you can create a new instance from a different software product in the catalog.  
{: tsResolve}
