---
description: Search&amp;Promote 15.1.1 릴리스 노트.
solution: Target
title: Search&Amp;Promote 15.1.1 릴리스 노트(01/15/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 16%

---


# Search &amp; Promote 15.1.1 릴리스 노트(01/15/2015){#search-promote-release-notes}

## 새로운 기능 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 이전에는, 형태소 분석, 동의어 등과 같은 언어적인 사항들이 항상 검색 안내 규칙의 키워드에 적용되었습니다. 이제 키워드가 그대로 사용되도록 이러한 확장 기능을 비활성화할 수 있습니다.

   비즈니스 규칙에 트리거 조건을 적용하려면 [!DNL Advanced Rule Builder], **[!UICONTROL If any/all of the following conditions are met]** 아래의 첫 번째 드롭다운 목록에서 **[!UICONTROL keyword]**&#x200B;를 선택한 다음 두 번째 드롭다운 목록에서 새 연산자 **[!UICONTROL equal exact]**&#x200B;를 선택합니다.

   [비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

## 수정 사항 및 개선 사항 {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] MDI(머천다이징 문서 ID) 필드 값을 더 이상 자르지  [!DNL Advanced Rule Builder] 않습니다.
* RBTA 관련 색인 오류가 이제 수정되었습니다.
* 상태가 &quot;승인됨&quot;인 기존 비즈니스 규칙을 편집하면 &quot;승인됨&quot; 상태가 취소됩니다. [!DNL Advanced Rule Builder] 옵션을 다시 확인한 다음 규칙을 평소대로 저장해야 합니다. **[!UICONTROL Approved]** 편집된 규칙을 재승인하지 않으면 규칙 상태는 자동으로 [!DNL Business Rules] 페이지에서 WIP(진행 중)로 설정됩니다.
* 규칙 필터링을 개선하기 위해 이제 [!DNL Business Rules] 페이지에서 새 **[!UICONTROL Advanced Search]** 옵션을 사용할 수 있습니다.
* 단어 분리를 쉽게 지정할 수 있도록 [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] 및 [!DNL Business Rules]의 규칙 트리거에 **[!UICONTROL contains word]** 조건을 추가했습니다.
* 이제 규칙을 볼 때와 같이 비즈니스 규칙 메모에 대한 개선 사항을 사용하여 해당 규칙의 노트 내역을 검색할 수 있습니다. 또한 이제 메모가 **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**&#x200B;에 기록됩니다.
* 0이 아닌 `sp_i` 값이 있는 쿼리는 더 이상 [!DNL Adobe Analytics] 리디렉터를 통해 실행되지 않습니다.

   [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)의 표에 있는 15행을 참조하십시오.

