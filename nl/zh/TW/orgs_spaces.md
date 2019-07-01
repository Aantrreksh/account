---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: account, add orgs, add spaces, cloud foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 新增組織及空間
{: #orgsspacesusers}

身為 {{site.data.keyword.Bluemix}} 帳戶擁有者，您可以將組織及空間新增至您的帳戶。如果您是組織管理員，則可以管理帳戶中的組織。
{:shortdesc}

## Cloud Foundry 組織概念
{: #cf-org-concepts}

您可以移至**管理** > **帳戶**然後選取**帳戶資源 > Cloud Foundry 組織**，來管理 Cloud Foundry 組織及空間。


組織可使用下列方式，啟用使用者間之間協同作業，並促進專案資源的邏輯分組：

   * 您可以一組空間、應用程式、服務、網域、路徑及使用者一起分組成為組織。
   * 您可以根據個別基準來管理使用者對組織及空間的存取權。

組織可以跨越多個地區，而且是由下列項目所定義：

<dl>
<dt>空間</dt>
<dd>組織內的子群組，您可以用來組織應用程式、服務和使用者。在 {{site.data.keyword.Bluemix_notm}} 中，空間關聯於特定地區。</dd>
<dt>使用者</dt>
<dd>組織及空間中具有基本許可權的角色。您必須先指派到組織，然後才能向您授權對該組織中的空間的其他許可權。有關更多詳細資料，請參閱 [Cloud Foundry 存取權](/docs/iam?topic=iam-cfaccess)。</dd>
<dt>網域</dt>
<dd>提供網際網路上配置給組織的路徑。路徑具有子網域和網域。子網域一般是應用程式名稱。網域可能是系統網域，或您針對應用程式所登錄的自訂網域。<br/>
<p>如果您新增自訂網域，則必須配置 DNS 伺服器來解析自訂網域，以指向 {{site.data.keyword.Bluemix_notm}} 系統網域。使用此方式，{{site.data.keyword.Bluemix_notm}} 接到您的自訂網域的要求時，可以將它適當地遞送至您的應用程式。</p></dd>
<dt>配額</dt>
<dd>代表組織可用的資源，包括可配置供組織使用的服務數和記憶體數量。在建立組織時會配置配額。組織空間中的任何應用程式或服務都會使用配額。使用「隨收隨付制」或「訂閱」帳戶，您可以在組織需要變更時，調整 Cloud Foundry 應用程式及容器的配額。</dd>
</dl>

在「訂閱」帳戶中，配額是起始消費通知的使用者定義限制。
{: tip}

## 新增組織
{: #createorg}

如果您具有計費帳戶，則可以新增所需數目的組織。精簡帳戶只能有一個組織，這已在您的帳戶裡建立。

1. 移至**管理** > **帳戶**，然後選取**帳戶資源 > Cloud Foundry 組織**。按一下**建立**。
2. 輸入組織名稱。名稱在 {{site.data.keyword.Bluemix_notm}} 中必須是唯一的。

   如果另一位 {{site.data.keyword.Bluemix_notm}} Public、Dedicated 或 Local 使用者已使用此組織名稱，則您必須指定不同的名稱。
3. 按一下**新增**。

新增組織之後，您會自動獲得指派「組織管理員」許可權，讓您可以編輯組織名稱、新增使用者，以及在組織中建立或刪除空間。

您可以為組織中的使用者指派下列 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)。依預設，會為被邀請到該帳戶的所有使用者指派審核員角色。

   * 組織管理員
   * 組織帳單管理員
   * 組織審核員

## 新增空間
{: #spaceinfo}

在組織內，您可以使用空間來群組一組應用程式、服務及使用者。空間定義於單一 {{site.data.keyword.Bluemix_notm}} 地區內。您可以根據交付生命週期，在組織中建立空間。例如，您可以建立 `dev` 空間作為開發環境、`test` 空間作為測試環境，以及 `production` 空間作為正式作業環境。然後，您可以建立應用程式與空間的關聯。

若要將空間新增至組織，請完成下列步驟。

1. 在「Cloud Foundry 組織」頁面上，按一下您要新增空間的組織名稱。
2. 按一下**新增空間**。
3. 選取地區並輸入名稱。
4. 按一下**儲存**。

將使用者新增至組織之後，即可將空間的許可權授與給他們。與組織類似，空間也會有一組 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)，其具有指派給團隊成員的特定許可權：

  * 空間管理員
  * 空間開發人員
  * 空間審核員

使用者必須至少獲指派空間中的一個許可權。
{: tip}
