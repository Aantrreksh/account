---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: account settings, delete account, account errors, reassign account, view tags, batch registration, transfer account ownership

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# 帳戶的常見問題解答
{: #accountfaqs}

{{site.data.keyword.cloud}} 的常見問題可能包括有關精簡帳戶、重新指派使用者、帳戶錯誤或者帳戶標籤的問題。要尋找 {{site.data.keyword.cloud_notm}} 的所有常見問題，請參閱我們的常見問題庫。
{: shortdesc}

## 如何建立帳戶？
{: #create-account}
{: faq}

移至 [{{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")，然後按一下**建立 {{site.data.keyword.Bluemix_notm}} 帳戶**，以建立永不到期的「精簡」帳戶。如需所包括特性的詳細資料，請參閱[精簡帳戶](/docs/account?topic=account-liteaccount#liteaccount)。


## 如何解決建立我的帳戶時所發生的錯誤？
{: #account-error}
{: faq}

如果您可以登入 {{site.data.keyword.Bluemix_notm}} 帳戶，請移至[支援](https://test.cloud.ibm.com/unifiedsupport/supportcenter)，然後選擇下列其中一個選項。

* 如果您有進階或超值支援，請按一下**即時會談**來與 {{site.data.keyword.Bluemix_notm}} 支援代表交談。
* 按一下_需要更多協助_ 區段中的**建立案例**，以建立支援案例。

   在您開啟案例之後，系統即會向您發送一則電子郵件通知。請遵循指示來進行進一步的溝通。

如果無法登入 {{site.data.keyword.Bluemix_notm}} 帳戶，請[建立帳戶要求](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")。

## 何謂 Cloud Foundry？
{: #cloud-foundry}
{: faq}

Cloud Foundry 是可透過 {{site.data.keyword.Bluemix_notm}} Public 取得的開放程式碼平台即服務 (PaaS) 選項，可用來在雲端上建置及部署應用程式。Cloud Foundry 組織及空間用來組織特定地區內可用的資源及應用程式。

如需管理組織和空間的相關資訊，請參閱[新增組織及空間](/docs/account?topic=account-orgsspacesusers#orgsspacesusers)。此外，如果您有興趣進一步瞭解如何提供對 Cloud Foundry 空間內資源的存取權，請參閱 [Cloud Foundry 存取](/docs/iam?topic=iam-cfaccess#cfaccess)。


## 我可以將組織移到另一個帳戶嗎？
{: #move-org-diff-account}
{: faq}

目前，您無法將組織移至其他帳戶。不過您可以用相同的認證在不同帳戶中重建組織，來模擬此功能。如需相關資訊，請參閱[新增組織及空間](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg)。


## 可以使用哪些 Cloud Foundry 地區？
{: #whichregions}
{: faq}

在「精簡」帳戶中，您只能在一個地區中工作。在「隨收隨付制」或「訂閱帳戶」中，您可以存取所有可用的地區。


## 何謂服務的「精簡」定價方案服務？
{: #whatisliteplan}
{: faq}

「精簡」方案是以免費配額為基礎的服務方案。您可以使用服務「精簡」方案來建置應用程式，而不會產生任何費用。「精簡」方案可以是每月固定提供（每一個月更新一次）或一次性使用。每個「精簡」方案服務可以有一個實例。所有帳戶都提供「精簡」定價方案。如需「精簡」帳戶的相關資訊，請參閱[帳戶類型](/docs/account?topic=account-accounts#accounts)。


## 當精簡方案實例達到每月配額時會發生什麼情況？
{: #monthlyquota}
{: faq}

達到精簡方案若為任何配額限制會導致該月份暫停使用該服務。配額限制是根據組織，而不是根據實例。在相同組織中建立的新實例會反映先前實例的任何用量。配額限制會在每個月一日重設。

移至**管理 > 計費及用量**，然後選取**用量**，即可檢查您的用量。如需相關資訊，請參閱[檢視用量](/docs/billing-usage?topic=billing-usage-viewingusage)。

## 如何從我的帳戶中刪除服務？
{: #accounts-service-removal}
{: faq}

如果您要刪除服務，則可以從資源清單這麼做。請在[使用資源及服務](/docs/resources?topic=resources-resources-faq#service-removal)中進一步瞭解。

## 我可以建立多少資源群組、組織或空間？
{: #resourcelimit}
{: faq}

如果您具有計費帳戶，則可以在帳戶內建立的資源群組、組織或空間數量沒有限制。不過，如果您有精簡帳戶，則限制為一個組織及一個資源群組。

## 如何升級或轉換我的帳戶類型？
{: #changeacct}
{: faq}

若要升級「精簡」帳戶，請移至[帳戶設定](https://{DomainName}/account/settings)。在「帳戶升級」區段中，按一下**新增信用卡**以升級至「隨收隨付制」帳戶，或針對「訂閱」帳戶按一下**升級**。您也可以在「帳戶設定」頁面上套用促銷特性碼，將「精簡」帳戶轉換成試用帳戶。

若要在「隨收隨付制」與「訂閱」帳戶類型之間轉換，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} 聯絡。

如果您不確定現行帳戶類型為何，可以在「帳戶設定」頁面找到。請在[升級帳戶](/docs/account?topic=account-upgrading-account)中進一步瞭解。

## 如果我將「精簡」帳戶升級，還能繼續使用我的現有實例嗎？
{: #nochange}
{: faq}

可以，當您升級成計費帳戶時，可以繼續使用您以「精簡」帳戶建立的實例。

## 如何更新我的信用卡？
{: #updatepayment}
{: faq}

更新信用卡就像新增信用卡一樣。請移至[付款](https://{DomainName}/billing/payments)，並在「新增付款方法」區段中，輸入新信用卡的計費資訊，然後按一下**新增信用卡**。

若要切換為不同的付款方法，請選取**使用其他方式付款**，然後按一下**提交變更要求**。將為您建立一個變更付款方法的支援案例。

## 如何變更電子郵件通知設定？
{: #change-email-prefs}
{: faq}

您可以在設定檔設定中，變更要針對計劃性事件、非計劃性事件及公告收到哪些電子郵件通知。
1. 在設定檔設定中移至[通知](https://cloud.ibm.com/user/notifications)。
1. 選取針對每種事件類型是否接收電子郵件通知。

針對標準基礎架構服務，帳戶擁有者也可以讓使用者訂閱來自那些服務的通知，方法是移至**管理 > 帳戶 > 通知**。

如需相關資訊，請參閱[設定電子郵件喜好設定](/docs/account?topic=account-email-prefs)。

## 如何重設密碼？
{: #reset-password}
{: faq}

若要重設帳戶密碼，請移至「虛擬人像」圖示 ![「虛擬人像」圖示](../icons/i-avatar-icon.svg) **設定檔和設定**。然後，按一下帳戶使用者資訊磚中的**變更或重設**。

若要重設 VPN 密碼，請完成下列步驟：

  1. 移至**管理 > 存取 (IAM)**，然後選取**使用者**。
  2. 選取使用者。
  3. 從 VPN 子網路區段中，按一下「編輯」圖示 ![「編輯」圖示](../icons/icon_write.svg)，以輸入新的 VPN 密碼。
  5. 按一下**套用**。

## 如何取消我的帳戶？
{: #cancelaccount}
{: faq}

看到您要離開，我們覺得很遺憾！在您離開之前，如果有任何方法可以協助您使用帳戶，請透過與支援中心聯絡來聯繫我們。

如果您真的決定要離開，則帳戶的取消方式取決於您的帳戶類型。您可以移至[帳戶設定](https://cloud.ibm.com/account/settings)，然後在_帳戶類型_ 下尋找，來檢查您的帳戶類型。

* 針對隨收隨付制或訂閱帳戶，取消帳戶最快的方式就是透過[即時會談](https://{DomainName}/unifiedsupport/supportcenter)與我們聯絡，或是撥打 1-866-325-0045 並選取第三個選項。您也可以開立支援案例。
* 若要取消精簡帳戶，請移至[帳戶設定](https://cloud.ibm.com/account/settings)，然後按一下**取消啟動帳戶**。

## 如何刪除帳戶？
{: #deleteaccount}
{: faq}

請與 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window} 聯絡以開立支援案例，並要求刪除您的帳戶。如果您的資料與舊帳戶相關聯並且要移至新帳戶，請在電子郵件中包含此資訊。

## 如何從 {{site.data.keyword.Bluemix_notm}} 中移除我的個人資料？
{: #remove-pi}
{: faq}

若要瞭解 IBM 如何處理您的個人資訊，請參閱 [IBM 隱私權聲明 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/privacy/){: new_window}。在「您的權利」一節中，請檢閱您可以要求移除之項目的相關資訊。按一下本節中的鏈結，即可提交要求來移除您的個人資訊。

## 為什麼我的帳戶被停用了？
{: #account-deactivated}
{: faq}

停用您帳戶的原因如下：

- 對於試用帳戶，試用期間已結束。若要重新啟動帳戶，請登入您的帳戶並將其升級為「隨收隨付制」帳戶。
- 授權使用者已取消帳戶。
- 帳戶已暫停。如果帳戶違反 {{site.data.keyword.Bluemix_notm}} 服務可接受的使用行為，IBM 將逕行停權，而不另行通知。如果使用者在收到違規動作通知之後，更正其使用行為，可還原部分服務。

如果您相信您的帳戶遭錯誤停用，請致電 1-866-325-0045 並選取第三個選項與支援人員聯絡。

## 如何取得支援？
{: #contactsupport}
{: faq}

按一下主控台功能表列中的**支援**，以移至「支援中心」。請在[取得協助](/docs/get-support?topic=get-support-support-plans)中進一步瞭解支援。

## 我可以註冊免費試用嗎？
{: #freetrial}
{: faq}

{{site.data.keyword.Bluemix_notm}} 精簡帳戶可用來存取免費的精簡方案服務。只要您想要便可以一直使用這些服務，且不會被收費，您的帳戶也永不到期。[註冊精簡帳戶](https://{DomainName}/registration)。

{{site.data.keyword.Bluemix_notm}} 試用帳戶可在認證合格的學術機構中提供給教職師及學生。若要符合試用帳戶的資格，請移至 [Harness the Power of IBM ![外部鏈結圖示](../icons/launch-glyph.svg)](https://ibm.biz/academic){: new_window}，並驗證機構認證。與精簡帳戶不同，試用帳戶會在其試用期間結束之後到期。

## 鏈結我的帳戶之後，要如何登入？
{: #al_login}
{: faq}

鏈結您的帳戶之後，請使用您的 IBM ID 登入 {{site.data.keyword.Bluemix}} 主控台。

## 鏈結我的帳戶之後，對我的支援有什麼影響？
{: #al_support}
{: faq}

鏈結您的帳戶之後，您會維持與將 {{site.data.keyword.Bluemix_notm}} 平台新增至帳戶時相同的支援層次。

## 是否有其他方法可以取得鏈結帳戶的協助？
{: #al_morehelp}
{: faq}

  1. 請參閱 [Steps to Link your IaaS and PaaS Accounts 部落格](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")，以取得有用的資訊。
  2. 從 {{site.data.keyword.BluSoftlayer_full}} 客戶入口網站中，開啟 **Sales Live Chat** 來詢問帳戶問題。
  3. 從客戶入口網站開立問題單。選取**支援** > **新增問題單**，然後在**主旨**欄位中，選取**帳戶要求**，將您的帳戶問題遞送給正確的支援團隊。

## 如果我有數個帳戶，要怎麼鏈結我的帳戶？
{: #al_multacct}
{: faq}

如果您有多個 SoftLayer 帳戶，則必須鏈結具有相符 {{site.data.keyword.Bluemix_notm}} 平台帳戶的帳戶，以及隨附的 IBM ID。

如果您沒有相符的 {{site.data.keyword.Bluemix_notm}} 平台帳戶，以及相應的 IBM ID 帳戶，則可以建立新的 SoftLayer 帳戶來鏈結帳戶。

## 鏈結帳戶有獎勵嗎？
{: #al_incent}
{: faq}

當您鏈結帳戶時，可以使用 200 美元的促銷額度來試用 {{site.data.keyword.Bluemix_notm}} 服務。

若要進一步瞭解 200 美元的促銷額度，請參閱[隨收隨付制帳戶](/docs/account?topic=account-accounts#paygo)。

## 將 {{site.data.keyword.Bluemix_notm}} 平台服務新增至我的 SoftLayer 帳戶有什麼涵義？
{: #al_owaffslacct}
{: faq}

這表示您的帳戶可以存取所有 {{site.data.keyword.Bluemix_notm}} 平台供應項目。將 {{site.data.keyword.Bluemix_notm}} 平台供應項目新增至帳戶之後，您的帳戶管理員必須讓使用者能夠存取供應項目。

如需成為帳戶管理員的相關資訊，請參閱[處理使用者](/docs/iam?topic=iam-iamuserinv#iamuserinv)。

## 鏈結帳戶對我的 SoftLayer 主帳戶 ID 有什麼影響？
{: #al_howaffslmastacct}
{: faq}

您仍可以使用 SoftLayer 帳戶的 ID ，來登入客戶入口網站，因為可以使用 IBM ID 來存取 {{site.data.keyword.Bluemix_notm}} 主控台。

## 如何檢視我擁有的帳戶？
{: #accounts-owned}
{: faq}

IBM Cloud 主控台標頭會列出與您登入 ID 相連結的所有帳戶（包括您擁有的帳戶）。您可以在[使用者](https://{DomainName}/iam/users)頁面上檢視每個帳戶中的角色。

您也可以從 CLI 執行 `ibmcloud account list` 指令來尋找帳戶。

## 如何在多個帳戶之間切換？
{: #switch-between-accounts}
{: faq}

如果您有多個帳戶，則可以按一下主控台功能表列中的帳戶名稱來選取您有權存取的另一個帳戶。  

![主控台功能表列中帳戶選取器的畫面擷取。帳戶選取器會顯示帳戶名稱及帳號，而且您選取現行帳戶來顯示可存取的其他帳戶清單。](images/account-faq.svg "帳戶選取器會顯示帳戶名稱及帳號，而且您選取現行帳戶來顯示可存取的其他帳戶清單。")

## 我可以讓別人成為帳戶擁有者嗎？
{: #switch-account-owners}
{: faq}

您可以使用 `ibmcloud catalog` 指令，將帳戶內個別資源的所有權轉移給某個人。若要進一步瞭解，請參閱[轉移專用資源的所有權](/docs/account?topic=account-include#owners)。

若要轉移整個帳戶的所有權，請更新[公司設定檔](https://{DomainName}/account/company-profile)。如需相關資訊，請參閱[轉移帳戶的所有權](/docs/account?topic=account-transfer)。

## {{site.data.keyword.Bluemix_notm}} 是否支援批次登錄使用者？
{: #batch-registration}
{:faq}

當您向 {{site.data.keyword.Bluemix_notm}} 登錄使用者時，必須個別登錄每一個使用者。{{site.data.keyword.Bluemix_notm}} 不支援批次登錄使用者。

移至 [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")，然後按一下**建立 {{site.data.keyword.Bluemix_notm}} 帳戶**。然後，完成每一位個別使用者的帳戶登錄表單。

## 何謂標籤？
{: #know-about-tags}
{: faq}

您可以藉由過濾資源清單中的標籤，以使用標籤來組織及檢視帳戶中的資源。如需相關資訊，請參閱[使用標籤](/docs/resources?topic=resources-tag)。

## 誰可以在帳戶中檢視標籤？
{: #tags-visibility-account}
{: faq}

在您的帳戶中到處都能可看見標籤。如果您有權查看資源，即可檢視附加的所有標籤。如需相關資訊，請參閱[授與使用者對標籤資源的存取權](/docs/resources?topic=resources-access#access)。

## 新增或移除標籤需要哪些許可權？
{: #permissions-add-remove-tags}
{: faq}

您必須至少具有已啟用 IAM 功能之資源的編輯者，或是對於資源之 Cloud Foundry 空間中的開發人員角色，才能在該資源上新增或移除標籤。如需相關資訊，請參閱[授與使用者對標籤資源的存取權](/docs/resources?topic=resources-access#access)。

## 我可以刪除標籤嗎？
{: # delete-tag}
{: faq}

您必須先從所有資源移除標籤，才能刪除標籤。如果您仍然無法將它刪除，該標籤可能附加至您無權檢視的資源。相同計費帳戶中的不同使用者，可以將相同的標籤附加至數個資源。使用者對帳戶上所有資源的可見性並不相同。

## 我可以重新命名標籤嗎？
{: #rename-tag}
{: faq}

您無法編輯標籤的名稱。若要重新命名標籤，請將它移除，然後使用新標籤重新指派資源。  
