---

copyright:
  years: 2019, 2021
lastupdated: "2021-08-31"

keywords: catalog, private catalogs, visibility, filter catalog, hide product, catalog filtering, enterprise, account group, child account, account, restrict

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Managing catalog settings
{: #filter-account}

As the account owner or administrator, you can manage the settings for all catalogs across your account. Management tasks include setting the visibility of the {{site.data.keyword.cloud}} catalog and controlling access to products in the public catalog and private catalogs for users in your account.
{: shortdesc}

You need the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to perform these tasks.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog in the console
{: #set-public-visibility}
{: ui}

Users in your account have access to all products in the public catalog by default. To update what products are visible to users, go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console. 

If you don't have any private catalogs in your account and you turn off the visibility of the public catalog, users can't create instances of any products. Be sure to [create a private catalog](/docs/account?topic=account-restrict-by-user) before you update this setting. 
{: note}

## Managing access to products for all users in the console
{: #set-account-filters}
{: ui}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. 

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict). 
{: tip}

1. In the console, go to **Manage** > **Catalogs** > **Settings**. 
2. Confirm that the visibility of the public catalog is set to **On**.
3. In the What products are available? section, select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category.
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Use the **Preview** table to confirm your selections, and click **Update**.

## Managing access to products for specific users in the console
{: #set-private-filters}
{: ui}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.   

1. In the console, go to **Manage** > **Catalogs**, **Private catalogs**. 
2. Select a catalog from the list to navigate to its details page. 

   The **Products in the {{site.data.keyword.cloud_notm}} catalog** table that's displayed on the page shows the list of products that are available at the account level. The availability is based on the filters the account owner or administrator set. Account-level filters apply to all the private catalogs in the account. 
   {: tip}
  
3. Click **Manage filters**.
3. Select to include or exclude all products in the public catalog. 
4. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category. 
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Click **Update**. 
7. Go to the Settings page and turn off the visibility of the public catalog.  
7. To give users access to work with the products in the private catalog, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

   For more detailed examples of how you can leverage filtering at the private catalog level, see [Customizing your private catalogs](/docs/account?topic=account-restrict-by-user).

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the CLI
{: #set-public-visibility-cli}
{: cli}

Users in your account have access to all products in the {{site.data.keyword.cloud_notm}} public catalog by default. You can make products available only to the users you choose by turning off visibility to the {{site.data.keyword.cloud_notm}} catalog and adding the products to your private catalogs. Use the following command to turn off visibility of the public catalog to all users in your account.

```
ibmcloud catalog filter hide-ibm-public-catalog
```
{: codeblock}

## Managing access to products for all users by using the CLI
{: #set-account-filters-cli}
{: cli}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. 

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict). 
{: tip}

1. Create a new filter. 

   ```
   ibmcloud catalog filter create [--catalog CATALOG] [--category CATEGORY] [--compliance COMPLIANCE] [--deployment-target TARGET] [--exclude-list LIST] [--include-all ALL] [--include-list LIST] [--offering-format FORMAT] [--pricing-plan PLAN] [--provider PROVIDER] [--release RELEASE] [--type TYPE]
   ```
   {: codeblock}

   If you don't specify the `--catalog CATALOG` command, the filter is created at the account level.

1. Target an account group by specifying the command option `--account-group ACCOUNT GROUP`.
1. Update the filter to include or exclude a particular product or products. See the [Catalog management CLI](https://cloud.ibm.com/docs/cli?topic=cli-manage-catalogs-plugin#create-filter) guidance for command options or run the `ibmcloud catalog filter options` command to retrieve the filter options for each filter category.

## Managing access to products for specific users by using the CLI
{: #set-private-filters-cli}
{: cli}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.

1. Create a new filter. 

   ```
   ibmcloud catalog filter create [--catalog CATALOG] [--category CATEGORY] [--compliance COMPLIANCE] [--deployment-target TARGET] [--exclude-list LIST] [--include-all ALL] [--include-list LIST] [--offering-format FORMAT] [--pricing-plan PLAN] [--provider PROVIDER] [--release RELEASE] [--type TYPE]
   ```
   {: codeblock}

   If you don't specify the `--catalog CATALOG` command, the filter is created at the account level.

1. Target an account group by specifying the command option `--account-group ACCOUNT GROUP`.
1. Update the filter to include or exclude a particular product or products. See the [Catalog management CLI](https://cloud.ibm.com/docs/cli?topic=cli-manage-catalogs-plugin#create-filter) guidance for command options or run the `ibmcloud catalog filter options` command to retrieve the filter options for each filter category.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #set-public-visibility-api}
{: api}

Users in your account have access to all products in the {{site.data.keyword.cloud_notm}} public catalog by default. You can make products available only to the users you choose by turning off visibility to the {{site.data.keyword.cloud_notm}} catalog and adding the products to your private catalogs. Use the following command to turn off visibility of the public catalog to all users in your account.

```bash
curl -X "PUT" "https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogaccount" 
-H "accept: */*" 
-H "Authorization: {iam-bearer-token}" 
-d '{"id":"string","hide_IBM_cloud_catalog":true,"account_filters":{"include_all":true,"category_filters":{"additionalProp1":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp2":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp3":{"include":true,"filter":{"filter_terms":["string"]}}},"id_filters":{"include":{"filter_terms":["string"]},"exclude":{"filter_terms":["string"]}}}}'
```
{: codeblock}

Make sure the `hide_IBM_cloud_catalog` field has a Boolean value of `true` to hide the public catalog in this account. Alternatively, you can give the `include_all` field a Boolean value of `false` for each `account_filters` object to exclude all of the public catalog.

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=curl#update-catalog-account){: external} for more information.

## Managing access to products for all users by using the API
{: #set-account-filters-api}
{: api}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. 

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict). 
{: tip}

```bash
curl -X "PUT" "https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogaccount" 
-H "accept: */*" 
-H "Authorization: {iam-bearer-token}" 
-d '{"id":"string","hide_IBM_cloud_catalog":true,"account_filters":{"include_all":true,"category_filters":{"additionalProp1":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp2":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp3":{"include":true,"filter":{"filter_terms":["string"]}}},"id_filters":{"include":{"filter_terms":["string"]},"exclude":{"filter_terms":["string"]}}}}'
```
{:codeblock}

The options for `{accountFilters}` are: `include_all`, `category_filters`, and `id_filters`.

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=curl#update-catalog-account){: external} for more information.

## Managing access to products for specific users by using the API
{: #set-private-filters-api}
{: api}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose. The following example applies the filter `id_filters` where `AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea` is an offering ID. 

```bash
curl -X 'PUT' \                                         
'https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogs/<catalog-id>'
 -H 'accept: application/json' \
 -H 'Content-Type: application/json' \
 -H "Authorization: ${IC_IAM_TOKEN}" \
 -d '{"label": "testcurlcatalog4", "short_description": "testing creating a catalog through curl", "catalog_filters": { "include_all": false, "id_filters": { "include": { "filter_terms": [ "AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea" ] } } }}'
```
{: codeblock}

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=curl#replace-catalog){: external} for more information. 

## Catalog filters
{: #catalog-filters-customize}

The following table lists the filters that you can use to customize which products in the public catalog are available to users in your account. 

| Option | Description |
|------------------|-------|
| AI / Machine Learning | Products that enable systems to learn from data rather than through explicit programming. |
| Analytics | Products that facilitate the analysis of data, typically large sets of business data, by the use of mathematics, statistics, and other means. |
| Blockchain | Products that facilitate the process of recording transactions and tracking assets in a business network. |
| Compute | Infrastructure resources that serve as the basis for building apps in the cloud. |
| Containers | A standard unit of software that packages up code and all its dependencies so the app runs quickly and reliably from one computing environment to another. |
| Databases | Products that provide some form of access to a database without the need for setting up physical hardware, installing software, or configuring for performance. |
| Developer tools | Products that support developing, testing, and debugging software. |
| Integration | Products that facilitate the connection of data, apps, APIs, and devices across an organization to be more efficient, productive, and agile. |
| Internet of Things | Products that support receiving and transferring data over wireless networks without human intervention. |
| Logging and Monitoring | Products that support receiving and transferring data over wireless networks without human intervention. |
| Mobile | Products with specific or special utility for users creatings things to be used on mobile devices. |
| Networking | Products that support or augment the linking of computers so they can operate interactively. |
| Security | Products that provide the protection of stored data from theft, leakage, and deletion. |
| Storage  | Products that support data to be created, read, updated, and deleted. |
{: caption="Table 1. Options for filtering by category" caption-side="top"}
{: #category-custom}
{: tab-title="Category"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| EU Supported | Support for the service is provided by {{site.data.keyword.cloud_notm}} support team members that are located in the European Union (EU) region. |
| Financial Services Validated | Services are designated as Financial Services Validated when the {{site.data.keyword.cloud_notm}} service or SaaS, or independent software vendor (ISV) offering, evidences compliance with the {{site.data.keyword.cloud_notm}} Framework for Financial Services. |
| HIPAA Enabled | The service is designated as HIPAA ready, meaning processing, storing, and handling Protected Health Information (PHI) in the service is supported. |
| IAM-enabled | The service is enabled to use {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) for access control. Access policies are used to assign users and service IDs access to specific resources in an account.|
| Service Endpoint Supported | The service can be connected to over the {{site.data.keyword.cloud_notm}} private network instead of the public network. Connecting directly to service endpoints doesn't require internet access, providing increased security. |
{: caption="Table 2. Options for filtering by compliance" caption-side="top"}
{: #compliance-custom}
{: tab-title="Compliance"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Community | The product is provided by open source communities outside of {{site.data.keyword.IBM_notm}}. If the root cause analysis determines that the issue is a defect in the product, {{site.data.keyword.IBM_notm}} isn't required to provide a fix. |
| {{site.data.keyword.IBM_notm}} | The lifecycle and operations of the product are the responsibility of {{site.data.keyword.IBM_notm}}. |
| Third Party | Support for the product is the responsibility of the third-party provider. If the root cause analysis determines that the issue is a defect in the product, {{site.data.keyword.IBM_notm}} isn't required to provide a fix. However, {{site.data.keyword.IBM_notm}} shares analysis with the third-party provider, if needed, and can work with the third-party provider to help solve the issue. |
{: caption="Table 4. Options for filtering by provider" caption-side="top"}
{: #provider-custom}
{: tab-title="Provider"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."} 

| Option | Description |
|--------------|-------|
| Beta | The product is available for evaluation and testing purposes. Beta products are not intended for production use. |
| Experimental | The product is available for evaluation and testing purposes, and might be unstable or not compatible with previous versions. The product can be discontinued with short notice.
| Deprecated | The product is supported but no longer recommended and that might become obsolete. |
{: caption="Table 5. Options for filtering by release" caption-side="top"}
{: #release-custom}
{: tab-title="Release"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| IBM Kubernetes Service | Used to create a Kubernetes cluster of compute hosts to deploy and manage containerized apps on {{site.data.keyword.cloud_notm}}. |
| Red Hat OpenShift | Used to create a {{site.data.keyword.openshiftshort}} cluster of compute hosts to deploy and manage containerized apps on {{site.data.keyword.cloud_notm}}. |
| VMware vCenter Server | Provides deployment and management of VMware virtualized environments. |
{: caption="Table 3. Options for filtering by deployment target" caption-side="top"}
{: #deploymenttarget-custom}
{: tab-title="Deployment target"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Cloud Paks | A cloud solution that integrates a container platform, containerized {{site.data.keyword.IBM_notm}} middleware and open source components, and common software services for development and management. |
| Helm charts | A format for packaging a collection of files that describe specific configurations of infrastructure in the form of code.   |
| Terraform |  Infrastructure as code to deploy your application. |
| Operators | A method of packaging and deploying a Kubernetes-native application. |
| OVAs | Open Virtual Appliance that contains a compressed installable version of a virtual machine. |
| Virtual server images | A template that is used to create instances of virtual servers. |
{: caption="Table 6. Options for filtering by delivery method" caption-side="top"}
{: #software-custom}
{: tab-title="Delivery method"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| SAP Certified | An infrastructure service that is certified by SAP to run production SAP workloads. For more information, see [{{site.data.keyword.ibm_cloud_sap}}](/docs/sap).|
| Satellite Enabled | A service that is enabled for use with {{site.data.keyword.cloud_notm}} Satellite. You can run apps consistently across on-premises, edge computing, and public cloud environments. |
| Quantum Technologies | A service that is compatible with quantum technologies. For more information, see [{{site.data.keyword.IBM_notm}} Quantum services](http://cloud.ibm.com/quantum){: external}.|
{: caption="Table 4. Options for filtering by runtime environment" caption-side="top"}
{: #works-with-custom}
{: tab-title="Works with"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}
