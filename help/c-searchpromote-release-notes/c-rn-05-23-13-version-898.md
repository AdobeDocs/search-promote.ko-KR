---
description: 'null'
seo-description: 'null'
seo-title: Search&Amp;Promote 8.9.8 릴리스 노트(05/23/2013)
solution: Target
title: Search&Amp;Promote 8.9.8 릴리스 노트(05/23/2013)
topic: Release Notes,Site search and merchandising
uuid: ff4bfc53-1d0e-4b7d-83ad-54c81d3f9769
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 57%

---


# Search &amp; Promote 8.9.8 릴리스 노트(05/23/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>새로운 기능 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 일반 구문 - 정확한 일치 지원 </p> </td> 
   <td colname="col2"> <p> 일반 구문에는 "부트 컷" 또는 "탱크 탑"과 같이 전체적으로 검색되는 두 개 이상의 단어가 포함되며 별도의 부분으로 검색되지 않습니다. 일반 구문은 고유하며 각 부분과는 다른 의미를 갖습니다. </p> <p> 비즈니스와 관련된 일반 구문 사전을 유지 관리하십시오. 고객이 여러 단어가 들어 있는 검색 쿼리를 수행하면 이 사전에서 정확히 일치하는 항목을 검색하게 됩니다. </p> <p>일반 구문은 추가, 편집 또는 삭제할 수 있습니다. 도메인 사전과 유사하게 일반 구문을 그룹화할 수도 있습니다. 예를 들어, 의류, 직물, 보석류, 측정, 쇼핑 및 일반별로 일반 구문을 그룹화할 수 있습니다. </p> <p><a href="../c-about-linguistics-menu/c-about-common-phrases.md#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local"> 일반 구문 정보 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

**수정 사항 및 개선 사항**

* 백엔드 검색 CGI 매개 변수 `sp_date_range_#`이(가) 사용자 정의 필드에 대해 작동하지 않았습니다.

   [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오.

* **[!UICONTROL History]** 버전을 되돌리면 URL 시작 지점 필드 내용이 업데이트되지 않았습니다.

   [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   [URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)도 참조하십시오.

* JSON 인코딩이 잘못 인코딩된 문자를 관리하지 않는 문제를 해결했습니다.
* 단계적으로 만들어진 색인을 원격에서 실시간으로 적용할 수 있도록 해주는 지원이 추가되었습니다.

   색인](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F)에 대한 [원격 제어 정보를 참조하십시오.

