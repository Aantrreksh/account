---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 계정 유형
{: #accounts}

{{site.data.keyword.Bluemix_notm}}에는 세 개의 서로 다른 계정 유형(Lite, 종량과금제, 구독)이 있습니다. 등록 즉시 무료 Lite 계정을 받을 수 있습니다. 종량과금제 및 구독은 청구 가능한 계정 옵션이며, 각각 서로 다른 기능을 제공합니다. 각 계정을 비교하고 사용자의 요구사항에 가장 적합한 계정을 선택하십시오.
{:shortdesc}


## 계정 비교
{: #compare}

다음 표에는 Lite, 종량과금제 및 구독 계정이 비교되어 있습니다. 각각의 계정에 대한 추가 세부사항은 후속 절을 참조하십시오.

|                                         |Lite               |종량과금제      |구독       |
|-----------------------------------------|--------------------|--------------------|--------------------|
|**무료 Cloud Foundry 메모리에 액세스** |256MB             |512MB             |512MB             |
| **[Lite 서비스 플랜에 액세스 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**모든 무료 플랜에 액세스**            |                    | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**전체 {{site.data.keyword.Bluemix_notm}} 카탈로그에 액세스** |  | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**다중 Cloud Foundry 지역에 액세스** |               | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**시간 제한사항 없음** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**보증된 제로 코스트**                | ![기능 사용 가능](../icons/icon_enabled.svg) |  |         |
|**중단된 가격**                  |                    |                    | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**개념 증명 학습 또는 빌드에 최적임** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |  |
|**프로덕션 유스 케이스에 최적임**        |                    | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
{: caption="표 1. {{site.data.keyword.Bluemix_notm}} 계정의 비교" caption-side="top"}


## Lite 계정
{: #liteaccount}

{{site.data.keyword.Bluemix_notm}} 콘솔에서 Lite 태그 ![Lite 태그](../icons/Lite.svg)와 함께 표시된, 무료로 선택할 수 있는 Lite 플랜을 통해 Lite 계정으로 가입하여 앱 빌드 및 서비스 탐색을 시작하십시오. Lite 계정은 만료되지 않으며 신용카드가 필요하지 않습니다.

본인용으로 작성된 `Default`로 이름 지정된 단일 리소스 그룹에 대한 액세스를 보유합니다. {{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM)에서 관리하는 모든 서비스 인스턴스는 자동으로 이 리소스 그룹에 추가됩니다. 언제든지 이 리소스 그룹의 이름을 업데이트할 수 있습니다. 세부 단계는 [리소스 그룹 이름 바꾸기](/docs/resources?topic=resources-rgs#rename_rgs)를 참조하십시오.

각각의 리소스 그룹은 무료입니다. Cloud Foundry 앱 및 IAM에서 관리되는 서비스 간의 연결을 작성할 때 할당량으로 계수되는 별명(서비스 인스턴스임)을 작성합니다. [연결 관리](/docs/resources?topic=resources-connect_app)를 참조하십시오.
{: tip}

### 사용 가능한 기능
{: #lite-account-features}

Lite 계정에 사용 가능한 다음 주요 기능 목록을 확인하십시오.

   * 계정이 무료로 제공됨 - 신용카드가 필요하지 않습니다.
   * 계정이 만료되지 않습니다.
   * 하나의 {{site.data.keyword.Bluemix_notm}} 지역에서 하나의 조직을 사용할 수 있습니다.
   * 기본 {{site.data.keyword.Bluemix_notm}} 지원은 무료입니다. 기본 지원은 기존의 심각도가 사용되지 않고 특정 응답 시간이 규정되지 않은 프로덕션 이외의 환경 또는 워크로드에 제공됩니다.
   * 계정 상태 및 할달량 한계에 대한 이메일 알림을 받습니다.
   * Cloud Foundry 앱이 최대 256MB의 바로 사용 가능한 무료 런타임 메모리에 액세스할 수 있습니다.
   * Lite 플랜을 보유하는 [{{site.data.keyword.Bluemix_notm}} 카탈로그 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window}에서 서비스의 1개 인스턴스를 프로비저닝할 수 있습니다.
   * 개발 활동이 없는 상태로 10일 후에는 앱이 휴면 상태가 됩니다. 앱에 대한 작업을 재개하여 앱의 휴면 상태를 해제할 수 있습니다.
   * 개발 활동이 없는 상태로 30일 후에는 Lite 플랜의 서비스 인스턴스가 삭제됩니다.

### Lite 계정 업그레이드
{: #upgrade-lite-account}

종량과금제 계정 또는 구독 계정을 업그레이드할 수 있습니다. 자세한 정보는 [내 계정 유형을 업그레이드하거나 변환하려면 어떻게 해야 합니까?](/docs/account?topic=account-changeacct)를 참조하십시오.

종량과금제 계정으로 업그레이드하면 프로모션을 위한 $200 크레딧을 받을 수 있으며, 크레딧은 계정에 자동으로 적용됩니다. 이 $200 크레딧은 30일 동안 유효하며 청구서에 자동으로 적용됩니다. 이 크레딧은 서드파티 오퍼링에 사용할 수 없습니다.

## 종량과금제 계정
{: #paygo}

종량과금제 계정이 있으면 여러 개의 리소스 그룹을 작성하여 할당량을 손쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다. 비용은 {{site.data.keyword.Bluemix_notm}} 컴퓨팅 및 서비스의 사용을 기준으로 청구됩니다. 무료 런타임 및 서비스 허용량을 제공받을 수 있습니다. 무료 사용량을 초과하여 사용하면 월별 {{site.data.keyword.Bluemix_notm}} 청구서를 받습니다. 청구서는 미국 달러(USD) 단위를 사용하며 리소스 비용에 대한 세부사항을 제공합니다.

또한 종량과금제 계정에서는 고급 또는 프리미엄 지원 옵션과 같은 선택적 항목을 주문할 수도 있습니다. 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg)에 문의하십시오.


### 종량과금제 계정 업그레이드
{: #upgrade-to-subscription}

종량과금제 계정을 구독 계정으로 업그레이드하려면 [{{site.data.keyword.Bluemix_notm}} 영업 팀](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에 문의하십시오.

## 구독 계정
{: #subscription-account}

구독 계정이 있으면 여러 개의 리소스 그룹을 작성하여 할당량을 손쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다. 매월 결합된 최소 지출 금액을 지불하며 해당 최소 비용에 적용되는 구독 할인을 받습니다. 총 구독 금액을 초과한 사용량에 대해 할인되지 않은 요금이 청구됩니다. 구독을 보려면 **관리 > 청구 및 사용량**으로 이동하여 **구독**을 선택하십시오.

구독 계정이 있으면 [{{site.data.keyword.Bluemix_notm}} 카탈로그](https://cloud.ibm.com/catalog/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 사용 가능한 대부분의 서비스를 작성할 수 있습니다. 그러나 일부 서비스는 별도 구매를 요구하는 특정 가격 플랜을 사용합니다.

### {{site.data.keyword.Bluemix_dedicated_notm}} 계정
{{site.data.keyword.Bluemix_dedicated_notm}}에서는 다음을 포함하여 최소 기간인 1년 동안은 등록해야 합니다.

   * VPN 연결을 인프라에 다시 연결
   * {{site.data.keyword.BluSoftlayer_notm}} 데이터 센터의 완전한 중복 환경
   * 지원되는 모든 런타임({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} 및 기본 제공 오픈 소스 런타임)
   * 선택한 모든 데디케이티드 서비스 및 모든 퍼블릭 {{site.data.keyword.Bluemix_notm}} 서비스
   * 표준 {{site.data.keyword.Bluemix_notm}} 지원

{{site.data.keyword.BluDirectLink}} 또는 고급 또는 프리미엄 지원 옵션 등의 선택적 항목을 주문할 수도 있습니다. 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg)에 문의하십시오.

해당 기간 동안 매월 지불하는 항목은 원하는 데디케이티드 서비스 및 모든 퍼블릭 서비스에 대한 액세스를 제공하는 구독 계정을 기반으로 합니다. {{site.data.keyword.Bluemix_notm}} 퍼블릭에서 서비스의 사용 비용은 구독 계정 계약을 기반으로 계산됩니다. 해당 구독 계약 외에 추가로 사용하는 모든 서비스에 대해 송장이 발급됩니다. 계약에 착수하려면 IBM이 지정한 계정 담당자 또는 [{{site.data.keyword.Bluemix_notm}} 영업 팀](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg)에 문의하십시오.
