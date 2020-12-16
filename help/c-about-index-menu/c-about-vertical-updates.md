---
description: 대량의 데이터를 처리할 필요 없이 수직 업데이트를 사용하여 인덱스의 일부를 빠르게 업데이트할 수 있습니다.
seo-description: 대량의 데이터를 처리할 필요 없이 수직 업데이트를 사용하여 인덱스의 일부를 빠르게 업데이트할 수 있습니다.
seo-title: 수직 업데이트 정보
solution: Target
subtopic: Vertical Update
title: 수직 업데이트 정보
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---


# 수직 업데이트 정보{#about-vertical-update}

대량의 데이터를 처리할 필요 없이 수직 업데이트를 사용하여 인덱스의 일부를 빠르게 업데이트할 수 있습니다.

## 수직 업데이트 사용 {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

세로 인덱스는 수행하는 데 단 몇 초 걸리고 전체 또는 증분적으로 색인화하는 데 많은 시간이 걸릴 수 있는 대용량 e커머스 웹 사이트에서 유용합니다.

세로 색인을 생성할 때 색인 작성 프로세스 중 시작 시간, 경과 시간 및 오류와 같은 상태 정보가 표시됩니다.

언제든지 수직 색인 프로세스를 중지하거나 다시 시작할 수 있습니다.

새로운 세로 색인이 라이브 웹 사이트를 업데이트하지만 고객은 현재 색인을 사용하여 사이트를 계속 검색할 수 있습니다.

>[!NOTE]
>
>이 기능은 기본적으로 [!DNL Adobe Search&Promote]에서 활성화되지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오.

수직 업데이트는 특히 IndexConnector를 사용하여 검색 색인에 대한 컨텐트를 제공하는 eCommerce 스타일 [!DNL Adobe Search&Promote] 계정에 사용하도록 되어 있습니다. 일반적인 사용 사례는 [!DNL Adobe Search&Promote] 색인이 검색 가능한 제품 카탈로그를 나타내는 것이며 현재고, 가용성 및/또는 가격과 같이 자주 변경되는 값을 신속하게 업데이트할 필요가 있는 경우입니다. 수직 업데이트는 각 문서의 부분만 업데이트하는 반면 증분 색인은 전체 문서를 새 버전으로 대체한다는 점을 제외하면 증분 색인과 다소 유사합니다.

&quot;수직 업데이트&quot;라는 용어는 [!DNL Adobe Search&Promote] 색인을 열 표로, [!DNL Adobe Search&Promote] 메타데이터 필드 정의에 해당하는 각 열과 문서에 해당하는 각 행을 포함하는 개념입니다. 수직 업데이트 프로세스는 다른 열의 컨텐츠를 변경하지 않고도 하나 이상의 열을 대체합니다.

콘텐트의 기본 소스 IndexConnector 피드가 인덱스를 만드는 데 필요한 모든 데이터 요소를 포함하는 경우, 수직 업데이트 피드는 동일한 IndexConnector &quot;schema&quot;를 사용하여 데이터 요소를 정의하지만 업데이트해야 하는 데이터 항목만 *이 포함됩니다.*

최소한 수직 업데이트 피드에는 &quot;기본 키&quot; 요소(IndexConnector 구성에서 **기본 키** 확인란과 함께 식별됨)와 하나 이상의 데이터 요소를 업데이트해야 합니다.

예를 들어, 기본 IndexConnector 피드는 다음과 같이 보일 수 있습니다(일반적으로 더 많은 데이터 항목이 있음).

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

이러한 값은 고객 사이트에서 빠르게 변경될 수 있으므로 `<price>` 및 `<inventory>` 값만 빠르게 업데이트할 수 있어야 합니다. 세로 업데이트 피드는 다음과 같이 표시됩니다.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

이 정보는 일반적으로 고객 서버의 개별 파일에 저장되며 IndexConnector &quot;Vertical File Path&quot; 구성 설정은 이 파일을 가리킵니다. 수직 업데이트 프로세스는 이 새 내용을 읽고 기존 [!DNL Adobe Search&Promote] 인덱스를 업데이트하며 이 경우 `<price>` 및 `<inventory>`에 대한 값만 업데이트합니다. 이후 검색을 수행하면 새로 업데이트된 컨텐츠가 반환됩니다.

>[!NOTE]
이 예제에서 `<price>` 및 `<inventory>` 메타데이터 필드는 **수직 업데이트 필드** 옵션이 선택된 상태로 정의해야 합니다.

색인[ 및 ](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)새 메타 태그 필드 추가[도 참조하십시오.](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)

## 단계 웹 사이트 {#task_46A367B0786C4C90BFFA5D3F95FD86C0}의 수직 업데이트 구성

URL을 지정하여 수직 업데이트에 포함할 색인 커넥터 소스를 구성할 수 있습니다.

**단계 웹 사이트의 수직 업데이트를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Vertical Update Configuration]** 페이지의 URL 업데이트 필드에서 색인화할 페이지의 URL을 지정합니다.

   검색 로봇은 지정된 색인 커넥터 소스에서 식별된 문서만 업데이트합니다.

   이 필드는 다음 예제와 같이 색인 커넥터 URL을 포함해야 합니다.

   `index:product_catalog`를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 라이브 또는 스테이지된 웹 사이트 {#task_E668E1F1240C476DAA1CA783DC728232}의 수직 업데이트 로그 보기

라이브 수직 업데이트 또는 스테이지된 수직 업데이트가 완료되면 연결된 로그를 보고 발생한 오류를 해결할 수 있습니다.

수직 업데이트 로그 파일은 내보낼 수 없으며 저장할 수 없습니다. 다음 인덱스가 발생할 때까지 로그 파일을 볼 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 수직 업데이트 로그를 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. 로그 페이지의 맨 위 또는 아래에서 다음 중 하나를 수행합니다.

   * 탐색 옵션 **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** 또는 **[!UICONTROL Go to line]**&#x200B;을 사용하여 로그를 통해 이동합니다.

   * 표시 옵션 **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** 또는 **[!UICONTROL Show]**&#x200B;을 사용하여 표시되는 내용을 세밀하게 수정할 수 있습니다.

