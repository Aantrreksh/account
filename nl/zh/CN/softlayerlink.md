---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 切换到 IBM 标识并链接帐户
{: #unifyingaccounts}

现在，在 SoftLayer 中进行认证将使用 IBM 标识来提供对所有 {{site.data.keyword.Bluemix}} 的单点登录。IBM 标识是您用于登录到 {{site.data.keyword.Bluemix_notm}} 帐户以访问和购买基础架构、服务和应用程序功能的单个标识。所有新帐户都将自动接收 IBM 标识，并且支持现有 SoftLayer 帐户（SAML 联合帐户除外）切换到 IBM 标识认证。
{:shortdesc}

## 切换到 IBM 标识
{: #switchtoIBMid}

开始切换到 IBM 标识的过程后，只要尚未完成切换过程，随时都可以将其取消。然而，您每次登录时，都会显示切换到 IBM 标识的提示。计划链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个 SoftLayer 帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识所拥有。

要从现有 SoftLayer 帐户切换到 IBM 标识，请创建 IBM 标识，然后使用注册代码进行确认。

### 请求 IBM 标识和注册代码
{: #reqIBMidandregcode}

1. 登录到 SoftLayer 帐户，在显示切换到 IBM 标识的提示时，单击**确定**。

   如果您是主用户并且在 {{site.data.keyword.BluSoftlayer_full}} 基础架构客户门户网站中未显示切换到 IBM 标识的提示，请联系 IBM 支持以获取帮助。有关联系支持人员的更多信息，请参阅 [IBM 支持](/docs/get-support/howtogetsupport.html#getting-customer-support)。

   如果您先前已登录并在提示时单击了**稍后**，但在当前会话中又希望切换到 IBM 标识认证，请转至“编辑用户个人档案”页面，然后单击**切换到 IBM 标识**。

2. 遵循向导提示来创建 IBM 标识。

   输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址将用作新 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

### 使用注册代码确认 IBM 标识
{: #confIBMiduseregcode}

1. 收到注册代码后，请单击电子邮件中的链接或将相应 URL 复制到浏览器中，然后输入注册代码。

   注册代码有效期为 7 天，并且只能使用一次。

2. 提交了注册代码后，使用 IBM 标识登录到客户门户网站。

   在“帐户登录”提示中，转至 **IBM 标识帐户登录**部分，并单击**使用 IBM 标识登录**。不要使用先前用于 SoftLayer 标识的**用户名**和**密码**字段。

如果您是新客户，在检查订单时，系统会要求您输入现有 IBM 标识或创建新的 IBM 标识。
  * 要使用现有 IBM 标识，请输入 IBM 标识的用户名或电子邮件地址（如果唯一，即未在多个 IBM 标识之间共享）。
  * 要创建新的 IBM 标识，请输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址是该 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

要解决使用 IBM 标识登录的任何问题，请参阅[有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断](/docs/troubleshoot/ts_accessing.html#accessing)。

## 链接 IBM 标识用户帐户
{: #link_user_accounts}

用户帐户切换到 IBM 标识认证后，经销商和分销商可以链接 SoftLayer 帐户和 {{site.data.keyword.Bluemix_notm}} 帐户，以利用组合的基础架构即服务 (IaaS) 和平台即服务 (PaaS) 资源。然后，可以在 {{site.data.keyword.BluSoftlayer_full}} 基础架构客户门户网站中访问 IaaS 资源，在 {{site.data.keyword.Bluemix_notm}} 控制台中访问 PaaS 资源，全都通过单次登录进行访问。链接帐户还为您提供了针对您使用的所有 PaaS 和 IaaS 资源的单个帐单。

要链接帐户，您必须是 SoftLayer 主用户。作为帐户主用户的 IBM 标识必须是要链接到的 {{site.data.keyword.Bluemix_notm}} 平台帐户的所有者。请务必查看有关链接帐户的以下重要说明：

  * 要链接的 SoftLayer 帐户的主用户必须具有 IBM 标识。
  * 链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个用户帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识所拥有。尽管一个 IBM 标识可以拥有多个 SoftLayer 帐户，但您仍必须将主用户更改为对于每个帐户都唯一的 IBM 标识。请联系支持人员，以更改 SoftLayer 帐户的主用户。有关更多信息，请参阅[获取对 {{site.data.keyword.Bluemix_notm}} 基础架构的支持](/docs/customer-portal/cpsupport.html)。
  * 将新用户添加到链接的帐户时，必须将这些用户同时添加到 SoftLayer 帐户和 {{site.data.keyword.Bluemix_notm}} 帐户，这样这些用户才能访问统一控制台的所有功能。
  * 如果您有品牌帐户，使用 Brand Agent Portal (BAP) 并且在链接帐户时需要支持，请通过发送电子邮件至 softlayer_revenue_services_team@wwpdl.vnet.ibm.com 以联系税务服务团队。
  * {{site.data.keyword.Bluemix_notm}} 中的所有链接帐户都必须是现买现付帐户。您可以创建新的现买现付帐户，链接现有的现买现付帐户，或者链接现有试用帐户（此帐户随后将升级为现买现付帐户）。但不能链接到 {{site.data.keyword.Bluemix_notm}} 预订帐户。

要将每个 SoftLayer 帐户链接到现有 {{site.data.keyword.Bluemix_notm}} 平台帐户或创建新帐户，请完成以下步骤：

   1. 使用您的主用户帐户 IBM 标识登录到 {{site.data.keyword.BluSoftlayer_full}} 基础架构客户门户网站。
   2. 在 {{site.data.keyword.Bluemix_notm}} 基础架构客户门户网站中，单击**链接 Bluemix 帐户**。
   3. 阅读并接受链接 SoftLayer 和 {{site.data.keyword.Bluemix_notm}} 帐户的条款。
   4. 请遵循向导提示，包括将 SoftLayer 帐户中的用户添加到 {{site.data.keyword.Bluemix_notm}} 帐户。
   5. 系统提示时，执行以下其中一个操作：
     * 如果您已有 {{site.data.keyword.Bluemix_notm}} 帐户，请提供与该帐户关联的电子邮件地址来链接帐户。
     * 如果您没有 {{site.data.keyword.Bluemix_notm}} 帐户，请提供要使用的电子邮件地址，然后遵循指示信息受邀加入 {{site.data.keyword.Bluemix_notm}} 并创建帐户。
   6. 链接帐户后，请通知每个帐户的最终用户通过执行先前[切换到 IBM 标识](/docs/account/softlayerlink.html#switchtoIBMid)部分中所述的过程来迁移到 IBM 标识。

仅将最终用户帐户迁移到 IBM 标识。请勿迁移品牌帐户，品牌帐户是最终用户帐户的父帐户，不包含任何资源。迁移到 IBM 标识的 Brand 帐户用户将无法再登录到 Brand Agent Portal (BAP)。
{: tip}

链接的帐户将登录到 [{{site.data.keyword.Bluemix}} 控制台 ![外部链接图标](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}。

另外，在链接帐户后，请注意以下更改：
  * 必须使用 IBM 标识凭证来访问 SoftLayer 和 {{site.data.keyword.Bluemix_notm}} 帐户。
  * 将对全体 {{site.data.keyword.Bluemix_notm}} 费用应用所有现有的 SoftLayer 折扣。
  * 您将收到一张以美元 (USD) 计费的发票。如果您有现有的 {{site.data.keyword.Bluemix_notm}} 帐户，那么通过 {{site.data.keyword.Bluemix_notm}} 对基础架构资源进行记帐会在链接帐户之后启动的新记帐周期生效。
  * 您可以在 {{site.data.keyword.Bluemix_notm}} 控制台中监视基础架构资源的使用情况。

帐户链接之后即无法对其取消链接。
{: tip}

## 链接帐户中的多因子认证使用情况
{: #2fa}

如果您有链接的帐户，那么可以使用身份和访问权**设置**页面为帐户启用多因子认证。这通常也称为双因子验证 (2FA)，它会添加一个安全层，以支持使用除了标准的必需 IBM 标识和密码之外的其他方式访问帐户。帐户的多因子认证会应用于链接的 {{site.data.keyword.Bluemix_notm}} 帐户中的所有资源。帐户支持多因子认证时，多因子认证还会应用于已添加到该帐户的所有用户。

多因子认证不是按 IBM 标识进行的。该认证仍是按帐户进行的。当一个 IBM 标识与多个帐户相关联，而您在各帐户之间进行切换时，每次切换到要求双因子认证的不同帐户时都必须确认身份。即使优先帐户和新帐户是使用相同的双因子认证机制配置的，也是如此。
