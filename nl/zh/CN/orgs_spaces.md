---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account, add orgs, add spaces, manage users, user access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 添加组织和空间
{: #orgsspacesusers}

作为 {{site.data.keyword.Bluemix}} 帐户所有者，您可以向自己的帐户添加组织和空间。如果您是组织管理者，那么可以管理帐户中的组织。转至**管理** > **帐户**，然后选择 **Cloud Foundry 组织**。
{:shortdesc}

您可以通过以下方式，使用组织来启用用户间的协作并促进项目资源的逻辑分组：

   * 可以通过组织将一组空间、应用程序、服务、域、路径和用户分组到一起。
   * 可以分别管理用户对组织和空间的访问权。

## 添加组织
{: #createorg}

组织可以跨多个区域，并且组织通过以下各项进行定义：

<dl>
<dt>用户</dt>
<dd>在组织和空间中具有基本许可权的角色。您必须先分配到组织，然后才能向您授予对该组织中的空间的其他许可权。有关更多详细信息，请参阅[用户和角色](/docs/iam?topic=iam-userroles)。</dd>
<dt>域</dt>
<dd>提供因特网上分配给组织的路径。路径具有子域和域。子域通常是应用程序名称。域可能是系统域，或者为应用程序注册的定制域。<br/>
<p>如果您添加定制域，那么必须配置 DNS 服务器以将您的定制域解析为指向 {{site.data.keyword.Bluemix_notm}} 系统域。这样，当 {{site.data.keyword.Bluemix_notm}} 接收到定制域的请求时，它可以将其正确路由到您的应用程序。</p></dd>
<dt>配额</dt>
<dd>表示组织可用的资源，包括可分配供组织使用的服务数和内存量。在创建组织时会分配配额。组织内空间中的任何应用程序或服务都会使用一定的配额。通过现收现付帐户或预订帐户，可以根据您组织的需求变化来调整 Cloud Foundry 应用程序和容器的配额。</dd>
</dl>

在预订帐户中，配额是用户定义的限制，用于触发花费通知。
{: tip}

添加组织时，组织名称在 {{site.data.keyword.Bluemix_notm}} 中必须是唯一的。如果组织名称已经由其他 {{site.data.keyword.Bluemix_notm}} Public、Dedicated 或 Local 用户使用，那么必须指定新名称。添加组织之后，系统会自动为您分配“组织管理者”许可权，以便您可以编辑组织名称、添加用户以及在组织中创建或删除空间。如果您有计费帐户，那么可以根据需要添加任意数量的组织。但是，在轻量帐户中，您只能具有一个组织。

以下[用户角色](/docs/iam?topic=iam-userroles)可以分配给组织中的用户。缺省情况下，会为所有受邀加入帐户的用户分配审计员角色。

   * 组织管理者
   * 组织记帐管理者
   * 组织审计员

要添加组织，请完成以下步骤：

  1. 单击**添加组织**。
  2. 输入组织名称。  
  3. 单击**添加**。

<!-- Add info on Manage infrastructure option under a space -->

## 添加空间
{: #spaceinfo}

在组织内，您可以使用空间来对一组应用程序、服务和用户进行分组。空间与 {{site.data.keyword.Bluemix_notm}} 中的特定区域联系在一起。您可以基于交付生命周期在组织中创建多个空间。例如，可以创建 `dev` 空间（作为开发环境）、`test` 空间（作为测试环境）和 `production` 空间（作为生产环境）。然后，可以将应用程序与空间相关联。

在将用户添加到组织之后，您可以向其授予对空间的许可权。与组织类似，空间也具有一组 [Cloud Foundry 角色](/docs/iam?topic=iam-cfroles)，这些角色带有分配给团队成员的特定许可权：

  * 空间管理者
  * 空间开发者
  * 空间审计员

用户必须分配有空间中的至少一个许可权。
{: tip}

要添加空间，请完成以下步骤：

  1. 选择要向其添加空间的组织的名称。
  2. 单击**添加空间**。
  3. 选择区域并输入名称。
  4. 单击**保存**。
