---

copyright:
  years: 2019, 2021
lastupdated: "2021-09-28"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Managing your enterprise
{: #enterprise-settings}

From the dashboard of your {{site.data.keyword.Bluemix}} enterprise, you can view enterprise details, take common actions such as adding accounts and inviting users, and view billing information. You can also rename your enterprise on the dashboard or by using the CLI or API.
{: shortdesc}

To manage enterprise settings, you need the Administrator or Editor role on the Enterprise service in the enterprise account.
{: tip}

## Managing your enterprise in the console
{: #enterprise-manage}
{: ui}

To view your enterprise dashboard, go to **Manage > Enterprise** in the {{site.data.keyword.Bluemix_notm}} console. The dashboard provides an overview of accounts, users, and subscription credit in your enterprise. The dashboard has quick links so that you can perform the following common actions:
* [Add new or existing accounts to your enterprise](/docs/account?topic=account-enterprise-add)
* [Invite users to the enterprise account](/docs/account?topic=account-iamuserinv)
* [View and manage subscription credit](/docs/billing-usage?topic=billing-usage-subscriptions)

Also, you can rename your enterprise by clicking **Rename** in the Enterprise details section.

## Managing your enterprise from the CLI
{: #enterprise-manage-cli}
{: cli}

* View enterprise information such as the name, domain, owner, and creation and update dates.

   ```bash
   ibmcloud enterprise show
   ```
   {: codeblock}
  
* Rename the enterprise by specifying the new name on the `-n` option in the following command.

   ```bash
   ibmcloud enterprise update -n NEW_NAME
   ```
   {: codeblock}

## Managing your enterprise by using the API
{: #enterprise-manage-api}
{: api}

You can programmatically update an enterprise by calling the Enterprise Management API as shown in the following sample request. You can update the enterprise name by passing the new values on the API call. For detailed information about the API, see the [Enterprise Management API documentation](/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```bash
curl -X PATCH "https://enterprise.cloud.ibm.com/v1/account-groups/$ACCOUNT_GROUP_ID" 
-H "Authorization: Bearer <IAM_Token>" 
-H 'Content-Type: application/json' 
-d '{
  "name": "Updated Example Account Group",
}'
```
{: codeblock}
{: curl}

```java
UpdateAccountGroupOptions updateAccountGroupOptions = new UpdateAccountGroupOptions.Builder()
    .accountGroupId(accountGroupId)
    .name("Updated Example Account Group")
    .build();

Response<Void> response = service.updateAccountGroup(updateAccountGroupOptions).execute();
```
{: codeblock}
{: java}

```javascript
const params = {
  accountGroupId: accountGroupId,
  name: 'Updated Example Account Group',
};

enterpriseManagementService.updateAccountGroup(params)
  .then(res => {
    done();
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
response = enterprise_management_service.update_account_group(
  account_group_id=account_group_id,
  name='Updated Example Account Group',
)
```
{: codeblock}
{: python}

```go
uupdateAccountGroupOptions := enterpriseManagementService.NewUpdateAccountGroupOptions(
  accountGroupID,
)
updateAccountGroupOptions.SetName("Updated Example Account Group")

response, err := enterpriseManagementService.UpdateAccountGroup(updateAccountGroupOptions)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}

