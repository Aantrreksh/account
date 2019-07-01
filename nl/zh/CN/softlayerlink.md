---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-20"

keywords: SoftLayer account, link account, complete account, IBM Cloud account, IBMid, switch to IBMid

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# 切换到 IBM 标识并链接帐户
{: #unifyingaccounts}

IBM 标识是您用于登录到 {{site.data.keyword.Bluemix}} 帐户以访问和购买基础架构、服务和应用程序功能的单个标识。所有新帐户会自动收到 IBM 标识。支持除了 SAML 联合帐户外的现有 SoftLayer 帐户切换到 IBM 标识认证。您还可以链接帐户以获取帐户、计费和使用情况的单一视图。
{:shortdesc}

## 切换到 IBM 标识
{: #switchtoIBMid}

开始切换到 IBM 标识的过程后，只要尚未完成切换过程，随时都可以将其取消。然而，您每次登录时，都会显示切换到 IBM 标识的提示。计划链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个 SoftLayer 帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识拥有。

要从现有 SoftLayer 帐户切换到 IBM 标识，请创建 IBM 标识，然后使用注册代码进行确认。

### 请求 IBM 标识和注册代码
{: #reqIBMidandregcode}

1. 登录到 SoftLayer 帐户，在显示切换到 IBM 标识的提示时，单击**确定**。

   如果您是主用户并且在客户门户网站中未显示切换到 IBM 标识的提示，请联系 IBM 支持人员以获取帮助。有关联系支持人员的更多信息，请参阅[获取支持](/docs/get-support?topic=get-support-getting-customer-support)。

   如果您先前已登录并在提示时单击了**稍后**，但在当前会话中又希望切换到 IBM 标识认证，请转至“编辑用户个人档案”页面，然后单击**切换到 IBM 标识**。

2. 遵循向导提示来创建 IBM 标识。

   输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址将用作新 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

### 使用注册代码确认 IBM 标识
{: #confIBMiduseregcode}

1. 收到注册代码后，请单击电子邮件中的链接或将相应 URL 复制到浏览器中，然后输入注册代码。注册代码有效期为 7 天，并且只能使用一次。

2. 提交了注册代码后，使用 IBM 标识登录到客户门户网站。

   在“帐户登录”提示中，转至 **IBM 标识帐户登录**部分，并单击**使用 IBM 标识登录**。不要使用先前用于 SoftLayer 标识的**用户名**和**密码**字段。

如果您是新客户，在检查订单时，系统会要求您输入现有 IBM 标识或创建新的 IBM 标识。
  * 要使用现有 IBM 标识，请输入该 IBM 标识的用户名或电子邮件地址（不能是在多个 IBM 标识之间共享的用户名或电子邮件地址）。
  * 要创建新的 IBM 标识，请输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址是该 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

要解决使用 IBM 标识登录的任何问题，请参阅[有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断](/docs/account?topic=account-accessing)。


## 链接 IBM 标识帐户
{: #link_accounts}

帐户切换到 IBM 标识帐户后，您可以链接 SoftLayer 帐户和 {{site.data.keyword.Bluemix_notm}} 帐户，使得您登录一次就可以访问基础架构和平台资源。链接帐户还针对您使用的所有基础架构和平台资源为您提供单个帐单。您可以链接自己的帐户，或者如果您是主用户，那么可以链接您的用户帐户。

### 链接 IBM 标识帐户
{: #link_user_account}

如果您是经典基础架构客户，并且还具有 {{site.data.keyword.Bluemix_notm}} 帐户，那么您可以链接帐户以获取帐户、计费和使用情况的单一视图。要链接帐户，请完成以下步骤：
1. 登录到 SoftLayer 帐户。
2. 从“帐户摘要”页面，单击**链接 IBM Cloud 帐户**。
3. 复查使用条款，然后单击以确认接受这些条款。
4. 根据帐户的设置方式，完成以下其中一个最终步骤：
  * 如果 IBM 标识具有关联的 {{site.data.keyword.Bluemix_notm}} 帐户，那么会将您定向到授权页面，然后返回到最终确认步骤。
  * 如果没有关联的 {{site.data.keyword.Bluemix_notm}} 帐户，那么系统会提示您创建新帐户。

要查看有关链接帐户的常见问题及解答，请查看[常见问题](/docs/account?topic=account-al_login)。

### 链接 IBM 标识用户帐户
{: #link_customer_accounts}

您的用户帐户切换为 IBM 标识认证后，经销商和分销商可以链接他们的用户帐户。要链接客户帐户，您必须是 SoftLayer 主用户。作为帐户主用户的 IBM 标识必须是要链接到的 {{site.data.keyword.Bluemix_notm}} 平台帐户的所有者。

一旦链接帐户，就无法取消链接。
{: note}

请务必查看有关链接帐户的以下重要说明：

  * 要链接的 SoftLayer 帐户的主用户必须具有 IBM 标识。
  * 链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个用户帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识拥有。尽管一个 IBM 标识可以拥有多个 SoftLayer 帐户，但您仍必须将主用户更改为对于每个帐户都唯一的 IBM 标识。请联系支持人员，以更改 SoftLayer 帐户的主用户。有关更多信息，请参阅[获取对 {{site.data.keyword.Bluemix_notm}} 基础架构的支持](/docs/customer-portal?topic=customer-portal-customerportal_support)。
  * 将新用户添加到链接的帐户时，必须将这些用户同时添加到 SoftLayer 帐户和 {{site.data.keyword.Bluemix_notm}} 帐户，这样这些用户才能访问统一控制台的所有功能。
  * 如果您有品牌帐户，使用 Brand Agent Portal (BAP) 并且在链接帐户时需要支持，请通过发送电子邮件至 softlayer_revenue_services_team@wwpdl.vnet.ibm.com 以联系税务服务团队。

要将每个 SoftLayer 帐户链接到现有 {{site.data.keyword.Bluemix_notm}} 平台帐户或创建新帐户，请完成以下步骤：

   1. 使用您的主用户帐户 IBM 标识登录到客户门户网站。
   2. 从客户门户网站，单击**链接 IBM Cloud 帐户**。
   3. 阅读并接受链接 SoftLayer 和 {{site.data.keyword.Bluemix_notm}} 帐户的条款。
   4. 请遵循向导提示，包括将 SoftLayer 帐户中的用户添加到 {{site.data.keyword.Bluemix_notm}} 帐户。
   5. 系统提示时，执行以下其中一个操作：
     * 如果您已有 {{site.data.keyword.Bluemix_notm}} 帐户，请提供与该帐户关联的电子邮件地址来链接帐户。
     * 如果您没有 {{site.data.keyword.Bluemix_notm}} 帐户，请提供要使用的电子邮件地址，然后遵循指示信息受邀加入 {{site.data.keyword.Bluemix_notm}} 并创建帐户。
   6. 链接帐户后，请通知每个帐户的最终用户通过执行先前[切换到 IBM 标识](#switchtoIBMid)部分中所述的过程来迁移到 IBM 标识。

      仅将最终用户帐户迁移到 IBM 标识。请勿迁移品牌帐户，品牌帐户是最终用户帐户的父帐户，不包含任何资源。迁移到 IBM 标识的品牌帐户用户将无法再登录到 Brand Agent Portal (BAP)。
      {: important}

在链接帐户后，请注意以下更改：

  * 您现在将登录到 [{{site.data.keyword.Bluemix}} 控制台 ![外部链接图标](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}。
  * 必须使用 IBM 标识凭证来访问 SoftLayer 和 {{site.data.keyword.Bluemix_notm}} 帐户。
  * 将对全体 {{site.data.keyword.Bluemix_notm}} 费用应用所有现有的 SoftLayer 折扣。
  * 您将收到一张以美元 (USD) 计费的发票。如果您有现有的 {{site.data.keyword.Bluemix_notm}} 帐户，那么通过 {{site.data.keyword.Bluemix_notm}} 对基础架构资源进行计费会在链接帐户之后启动的新计费周期生效。
有关更多信息，请参阅[链接帐户的合并帐单](/docs/customer-portal?topic=customer-portal-unifybillaccounts)。
  * 您可以在 {{site.data.keyword.Bluemix_notm}} 控制台中监视经典基础架构资源的使用情况。

## 链接帐户中的多因子认证使用情况
{: #2fa}

如果您拥有链接的帐户，那么可以使用 {{site.data.keyword.Bluemix_notm}} IAM **设置**页面对帐户启用多因子认证 (MFA)。通常，这也称为双因子认证 (2FA)，它会为帐户提供额外一层的安全保护，用户在访问帐户时除了必须提供标准的 IBM 标识和密码之外，还需要提供其他验证信息。帐户的 MFA 会应用于链接的 {{site.data.keyword.Bluemix_notm}} 帐户中的所有资源。帐户支持多因子认证时，多因子认证还会应用于已添加到该帐户的所有用户。

其他多因子认证方法不是按 IBM 标识进行的。而是按帐户进行的。当一个 IBM 标识与多个帐户相关联，而您在各帐户之间进行切换时，每次切换到要求双因子认证的不同帐户时都必须确认身份。即使旧帐户和新帐户都配置了相同的双因子认证机制，也是如此。

如果先前已针对经典基础架构资源[在客户门户网站中启用了 2FA](/docs/customer-portal?topic=customer-portal-cp_setup-2fa)，然后又启用了 {{site.data.keyword.Bluemix_notm}} 帐户的 MFA 设置，那么 MFA 帐户设置会覆盖在客户门户网站中设置的 2FA。这意味着，您可以禁用在客户门户网站中购买的 2FA，而使用帐户的 MFA 设置。
