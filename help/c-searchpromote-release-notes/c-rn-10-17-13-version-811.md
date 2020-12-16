---
description: 'null'
seo-description: 'null'
seo-title: Search&Amp;Promote 8.11.0 릴리스 노트(10/29/2013)
solution: Target
title: Search&Amp;Promote 8.11.0 릴리스 노트(10/29/2013)
topic: Release Notes,Site search and merchandising
uuid: 973f9608-a5c7-4571-ae2b-6f1fa05bc862
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 58%

---


# Search &amp; Promote 8.11.0 릴리스 노트(10/29/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>새로운 기능 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 덴마크어 디컴파운더 </p> </td> 
   <td colname="col2"> <p> 이제 Adobe에서 제공하는 언어(덴마크어) 탐지, 디컴파운딩, 스테밍 및 세그멘터 서비스에 액세스할 수 있도록 <span class="keyword"> Adobe Search &amp; Promote</span>에 대한 메커니즘이 제공됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**향상된 기능 및 수정 사항**

* 기존 [!DNL Search&Promote] 테이블 일치 기능이 개선되었습니다. 향상된 기능에서는 SKU와 제품 데이터 간의 점점 복잡해지는 관계와 관련된 고객 요구 사항을 더 잘 지원합니다.

   >[!NOTE]
   >
   >이 기능은 기본적으로 활성화되어 있지 않습니다. Search&amp;Promote의 기능을 사용할 수 있게 활성화하려면 Adobe 고객 지원 센터에 문의하십시오.

* 계정의 언어 설정을 사용하여 검색 안내에서 패싯을 정렬하는 옵션을 추가했습니다.

   >[!NOTE]
   이 기능은 기본적으로 활성화되어 있지 않습니다. Search&amp;Promote의 기능을 사용할 수 있게 활성화하려면 Adobe 고객 지원 센터에 문의하십시오.

* 사용자가 다중 선택 패싯을 지정할 수 있는 패싯 값 수를 늘리는 옵션을 추가했습니다.

   >[!NOTE]
   이 기능은 기본적으로 활성화되어 있지 않습니다. Search&amp;Promote의 기능을 사용할 수 있게 활성화하려면 Adobe 고객 지원 센터에 문의하십시오.

* **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**&#x200B;에 확인란 옵션 **[!UICONTROL Only allow searches that use HTTPS]**&#x200B;을(를) 추가했습니다.

   [제한 정보](../c-about-settings-menu/c-about-searching-menu.md#concept_B5B527E04EBF4E9AB5956EEF881DDBF1)를 참조하십시오.

* **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]** > **[!UICONTROL Generic Feed]**&#x200B;에 옵션을 추가하여 마법사의 [!DNL File Submission] 패널에서 탭 문자를 유지합니다.

   [피드 만들기](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250)를 참조하십시오.

* 새 패싯 정의 양식의 맨 위 및 맨 아래 필드 각각에서 허용되는 데이터 크기를 80자에서 1000자로 늘렸습니다.

   [패싯 정보](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5)를 참조하십시오.

* 이제 검색 안내 디버그 매개 변수가 비즈니스 규칙 번호를 올바르게 보고합니다.
* 비즈니스 규칙이 이제 라이브 환경에 적용됩니다.
* 이제 경도/위도로 검색할 때 언어 = &quot;덴마크어(덴마크)&quot;로 구성된 계정에 대해 근접 검색이 작동합니다.
* 일정이 지정되지 않은 결과 기반 트리거가 이제 트리거됩니다.
* 이제 **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**&#x200B;에서 **[!UICONTROL Ignore Apostrophes]** 옵션을 사용할 때 일관된 결과가 보고됩니다.

   [단어 및 언어 정보](../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79)를 참조하십시오.

* 자동 완성 단어 목록 사용자 인터페이스가 이제 많은 수의 패싯에서 작동합니다.

