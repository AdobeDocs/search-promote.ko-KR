---
description: 직접 히트를 사용하면 고객이 일치하는 용어를 검색할 때 지정된 URL로 고객을 리디렉션할 수 있습니다. 이러한 종류의 기능을 사용하면 웹 사이트 검색의 탐색을 개선할 수 있습니다.
solution: Target
title: 직접 히트 정보
topic: 규칙, 사이트 검색 및 머천다이징
uuid: 374d63c8-2b82-4165-b543-05b587757baa
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 1%

---


# 직접 히트 정보{#about-direct-hits}

직접 히트를 사용하면 고객이 일치하는 용어를 검색할 때 지정된 URL로 고객을 리디렉션할 수 있습니다. 이러한 종류의 기능을 사용하면 웹 사이트 검색의 탐색을 개선할 수 있습니다.

## 직접 히트 사용 {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

직접 히트는 두 개의 기본 요소로 구성됩니다.웹 사이트의 URL 및 하나 이상의 쉼표로 구분된 검색어. 직접 히트는 다음과 같이 지정됩니다.

```
    website_URL: term
    website_URL: term, term, term
```

예를 들어 모든 약관을 지정하는 페이지가 있는 회사 웹 사이트가 있다고 가정합니다. 고객이 결과를 표시하지 않고 약관을 검색할 때 고객을 약관 페이지로 리디렉션할 수 있습니다.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

쿼리 용어가 직접 히트와 일치하지 않으면 검색 결과가 일반적인 방법으로 반환됩니다.

## 직접 히트 구성 {#task_64DFB8C554874C699FCC0C2F26C3669F}

검색 결과를 반환하는 대신 웹 브라우저를 URI로 리디렉션하는 검색어를 지정할 수 있습니다.

<!-- 

t_configuring_direct_hits.xml

 -->

&#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.

**직접 히트를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**&#x200B;을 클릭합니다.
1. [!DNL Direct Hits] 필드에 웹 사이트의 URL과 하나 이상의 쉼표로 구분된 검색어를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 직접 히트 테스트 {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

직접 히트 규칙을 라이브로 푸시하기 전에 용어를 입력하여 직접 히트를 테스트할 수 있습니다.

<!-- 

t_testing_direct_hits.xml

 -->

직접 히트 규칙이 적용되지 않는 용어를 테스트하는 경우 사용자에게 알려주는 메시지가 표시됩니다. 이러한 시나리오에서 직접 히트 규칙이 웹 사이트에 활성 상태인 경우 검색 결과가 평소대로 반환됩니다. 직접 히트 규칙으로 적용되는 용어를 테스트하는 경우 지정된 URL로 리디렉션된 정보를 알려주는 메시지가 표시됩니다.

**직접 히트를 테스트하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**&#x200B;을 클릭합니다.
1. [!DNL Test Direct Hits] 필드에 검색어를 입력한 다음 **[!UICONTROL Test]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

