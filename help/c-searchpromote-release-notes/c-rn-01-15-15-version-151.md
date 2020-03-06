---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 15.1.1 릴리스 노트(2015년 1월 15일)
solution: Target
title: Search&amp;Promote 15.1.1 릴리스 노트(2015년 1월 15일)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.1.1 Release Notes (01/15/2015){#search-promote-release-notes}

## 새로운 기능 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 이전에는, 형태소 분석, 동의어 등과 같은 언어적인 사항들이 항상 검색 안내 규칙의 키워드에 적용되었습니다. 이제 키워드가 그대로 사용되도록 이러한 확장 기능을 비활성화할 수 있습니다.

   When you want to apply trigger conditions to a business rule, in the [!DNL Advanced Rule Builder], following **[!UICONTROL If any/all of the following conditions are met]**, in the first drop-down list, select **[!UICONTROL keyword]**, and then select the new operator **[!UICONTROL equal exact]** in the second drop-down list.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] MDI(머천다이징 문서 ID) 필드 값을 더 이상 자르지 [!DNL Advanced Rule Builder] 않습니다.
* RBTA 관련 색인 오류가 이제 수정되었습니다.
* &quot;승인됨&quot; 상태의 기존 비즈니스 규칙을 편집하면 &quot;승인됨&quot; 상태가 취소됩니다. You must use [!DNL Advanced Rule Builder] to recheck the option **[!UICONTROL Approved]**, and then save the rule as usual. If you do not reapprove an edited rule, the rule&#39;s status is automatically set to WIP (Work In Progress) on the [!DNL Business Rules] page.
* A new **[!UICONTROL Advanced Search]** option is now available on the [!DNL Business Rules] page for improved filtering of rules.
* 단어 나누기를 쉽게 지정할 수 있도록 규칙 트리거에 **[!UICONTROL contains word]**[!DNL Query Cleaning]&#x200B;조건을 [!DNL Pre-Search Rules][!DNL Post Search Rules][!DNL Business Rules]추가했습니다.
* 규칙을 볼 때와 같이 비즈니스 규칙 메모에 대한 개선 사항이 적용되었으며, 이제 해당 규칙에 대한 메모 내역을 검색할 수 있습니다. 또한 이제 메모가 **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**&#x200B;에 로그인되어 있습니다.
* Queries with nonzero `sp_i` values are no longer run through the [!DNL Adobe Analytics] redirector.

   백 엔드 검색 CGI 매개 변수의 [](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)표에서 15행을 참조하십시오.

