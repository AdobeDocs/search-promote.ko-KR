---
description: Search&amp;Promote 8.9.3 릴리스 노트.
solution: Target
title: Search&Amp;Promote 8.9.3 릴리스 노트(11/01/2012)
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 82%

---


# Search &amp; Promote 8.9.3 릴리스 노트(11/01/2012){#search-promote-release-notes}

## Search &amp; Promote 8.9.3 릴리스 노트(11/01/2012) {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>새로운 기능 및 개선 사항 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Facet Rail </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390-->단면 모음 및 단면 이름의 순서(카운트별, 사전순 등)를 더 잘 제어할 수 있게 해 주는 새로운 <span class="uicontrol">단면 레일</span> 옵션이 추가되었습니다. </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">단면 레일 정보</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 중첩된 단면화 </p> </td> 
   <td colname="col2"> <p> 중첩된 측면의 대체 정렬 지원이 추가되었습니다. </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">단면 레일 정보</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>등급 규칙의 메모 필드 </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772--><span class="wintitle"> 등급 지표 추가</span> 대화 상자와 <span class="wintitle">등급 지표 편집</span> 대화 상자에 등급 규칙 및 규칙 그룹 정의에 사용되는 여러 줄의 <span class="wintitle">메모</span> 필드가 추가되었습니다. </p> <p>등급 규칙 메모는 <span class="wintitle">등급 규칙 정의</span> 페이지에 표시됩니다. 규칙 그룹 메모는 정의를 편집할 때 나타납니다. </p> <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local">등급 규칙 정보</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비즈니스 규칙 </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637--> 새로운 <span class="uicontrol">모든 결과 제거</span> 옵션을 사용하여 비즈니스 규칙에서 당연한 결과를 제거하는 방법으로 랜딩 페이지 지원을 개선했습니다. </p> <p>이 새로운 옵션을 다른 비즈니스 규칙 작업과 함께 사용하여 "자동 맞춤 랜딩 페이지"를 생성할 수 있습니다. 즉, 비즈니스 규칙 작업만을 기준으로 페이지의 컨텐트를 생성하면서 검색의 "당연한" 결과를 제거할 수 있습니다. </p> <p><a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local">새 비즈니스 규칙 추가</a> 또는 <a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local">비즈니스 규칙 편집</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>배너 및 비즈니스 규칙 </p> </td> 
   <td colname="col2"> <p> 배너를 참조하는 비즈니스 규칙이 라이브로 푸시된 경우 조건부로 배너를 라이브 푸시에서 제외하는 지원 옵션을 추가했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**수정 사항**

* [!DNL Stage] 색인이 있을 때 비즈니스 규칙이 일관되지 않게 작동했습니다.
* 이제 자동 맞춤 랜딩 페이지에 자동 등급 규칙이 적용됩니다.

   [등급 규칙 추가](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)의 옵션 표를 참조하십시오.

* [!DNL promosearch.cgi] 가 판촉을 반환하지 않았습니다.

   [검색 정보](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)를 참조하십시오.

* 많은 배너를 참조하는 푸시 규칙이 때때로 실패합니다.

   [배너 정보](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA)를 참조하십시오.

* **[!UICONTROL Did You Mean]** 이제 검색 쿼리 캐싱이 비활성화됩니다.

   [다음을 찾으려고 하셨습니까? 정보](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)를 참조하십시오.

