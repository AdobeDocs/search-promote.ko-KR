---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 8.9.4 릴리스 노트(2013년 1월 17일)
solution: Target
title: Search&amp;Promote 8.9.4 릴리스 노트(2013년 1월 17일)
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.4 Release Notes (01/17/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>새로운 기능 및 개선 사항 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>규칙 </p> </td> 
   <td colname="col2"> <p> 쿼리 정리 규칙, 검색 전 규칙 및 검색 후 규칙을 만들 때 인라인 메모를 만드는 기능이 추가되었습니다. 메모 필드에서 규칙을 문서화하고 설명할 수 있습니다. </p> <p>쿼리 <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> 정리 규칙 정보를 참조하십시오</a>. </p> <p>See <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> About Pre-Search Rules</a>. </p> <p>See <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> About Post-Search Rules</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 안내 </p> </td> 
   <td colname="col2"> <p> 검색에 걸린 총 시간을 가리키는 검색 안내 태그가 추가되었습니다. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> - 검색 시간을 식별합니다. 반환된 검색 시간 값은 ms로 지정됩니다. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> - 검색 결과 페이지를 작성하는 데 사용되는 코어 검색 수를 반환합니다. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - 핵심 검색 수가 1보다 큰 경우 테스트합니다. </p> <p>프레젠테이션 템플릿 태그의 <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> 기타 언어를</a>참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

**수정 사항**

* 이제 용어 보고서에서는 별표 문자가 무시됩니다.

   용어 [보고서 보기 또는 Null 검색어 보고서 보기...를 참조하십시오.](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* 보고서 > Null 검색 용어 보고서를 열고 시간 슬롯을 선택한 다음 보고서를 봅니다. 보고서에서 한 단어를 클릭하여 검색을 연 다음 보고서 보기를 다시 클릭합니다. 클릭한 키워드의 검색 수가 2배로 증가했었습니다. 이제 이 문제가 수정되었습니다.

   용어 [보고서 보기 또는 Null 검색어 보고서 보기...를 참조하십시오.](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* 비즈니스 규칙을 활성화하면 즉시 성능 최적화가 수행되었습니다.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* 방문 경로의 제거 기능이 가끔 작동하지 않았습니다.

   탐색 [표시 정보를 참조하십시오](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* 재생성을 사용하지 않는 한 등급 다시 지정 기능에서는 변경된 등급 규칙이 검색 결과에 적용되지 않았습니다.

   [등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

   색인 [등급 다시 지정을 참조하십시오](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).

