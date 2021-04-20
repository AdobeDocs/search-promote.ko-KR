---
description: 템플릿을 사용하여 프레젠테이션 템플릿과 전송 템플릿을 관리할 수 있습니다.
solution: Target
title: 템플릿 정보
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '2652'
ht-degree: 1%

---


# 템플릿 정보{#about-templates}

**[!UICONTROL Templates]**&#x200B;을 사용하여 프레젠테이션 템플릿과 전송 템플릿을 관리할 수 있습니다.

## 템플릿 정보 {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

프레젠테이션 템플릿과 전송 템플릿을 추가, 편집, 복사, 이름 변경 또는 삭제할 수 있습니다. [템플릿] 테이블에서 기존 템플릿 이름을 클릭하면 편집(또는 뷰어) 창에 열리면서 변경할 수 있습니다.

템플릿 테이블의 템플릿 이름 드롭다운 목록에서 내역 기능을 사용하여 템플릿에 적용한 모든 변경 사항을 되돌릴 수 있습니다.

템플릿 테이블에서 템플릿의 해당 **[!UICONTROL Minimize]** 확인란을 선택하여 프레젠테이션 템플릿의 페이지 가중치를 줄일 수 있습니다. 템플릿의 페이지 두께를 줄여 인라인 JavaScript 및 CSS를 동적으로 최소화할 수 있습니다. HTML에서 불필요한 공백도 제거합니다. 프레젠테이션 템플릿의 페이지 무게를 최소화하면 검색 결과를 보다 신속하게 전달할 수 있습니다.

파일 이름 옆에 있는 드롭다운 목록을 클릭한 다음 **[!UICONTROL Preview minimized]**&#x200B;을 클릭하여 최소화된 템플릿의 모양을 미리 볼 수 있습니다. 기본 프레젠테이션 템플릿을 최소화할 경우 `guided-include` 태그와 함께 포함된 템플릿을 최소화해야 합니다. 이 옵션은 상속할 수 없으므로 이 옵션을 사용해야 합니다.

프레젠테이션 템플릿을 최소화하더라도 동일한 템플릿의 &quot;최소화&quot; 버전을 계속 편집할 수 있습니다.

사전 검색 규칙, 사후 검색 규칙 및 비즈니스 규칙을 사용하여 다른 프레젠테이션 템플릿 중 하나를 사용할 시기를 결정할 수 있습니다. &quot;모든 검색에 대해 타깃팅된 템플릿을 xxxx로 설정&quot;과 같은 규칙을 사용하는 것이 일반적입니다. 이러한 규칙을 적용하면 템플릿 테이블에서 &quot;기본&quot; 템플릿을 변경하면 효과가 없는 것으로 나타납니다.

[사전 검색 규칙 정보](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)를 참조하십시오.

[사후 검색 규칙 정보](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)를 참조하십시오.

[비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

## 프레젠테이션 템플릿 정보 {#section_ACDDEA5C499E481C828A517C230D4596}

프레젠테이션 템플릿은 고객이 웹 사이트에서 검색 결과를 볼 때 보는 HTML 템플릿입니다.

프레젠테이션 레이어에는 다양한 소스의 여러 검색 결과를 보여주는 단일 프레젠테이션 템플릿이 있을 수 있습니다. 원하는 만큼 프레젠테이션 템플릿을 정의할 수 있고 다른 템플릿이 `include` 명령을 사용하여 공유하는 프레젠테이션 템플릿을 정의할 수도 있습니다. 프레젠테이션 템플릿은 패싯, 메뉴 및 탐색 표시와 같은 모든 디자인 구성 요소가 함께 표시되는 곳입니다. 다양한 디자인 구성 요소를 표시하려면 프레젠테이션 템플릿 태그를 사용해야 합니다.

[프레젠테이션 템플릿 태그](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)를 참조하십시오.

둘 이상의 프레젠테이션 템플릿이 있는 경우 다양한 프레젠테이션 템플릿이 사용되는 조건 아래에서 정의합니다. 들어오는 CGI 매개 변수 및 쿠키를 기반으로 사용할 프레젠테이션 템플릿을 선택할 수 있습니다. 또는 이전 검색 결과에 따라 사용 중인 프레젠테이션 템플릿을 전환할 수 있습니다.

여러 프레젠테이션 템플릿을 사용할 때는 검색 결과를 처음에 표시할 템플릿을 명시해야 합니다. 템플릿 테이블의 **[!UICONTROL Default]** 열을 사용하여 이 작업을 수행할 수 있습니다.

## 전송 템플릿 정보 {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

전송 템플릿은 백엔드 검색에서 검색 안내 프레젠테이션 레이어로 데이터를 전달하는 XML 또는 JSON 템플릿이 될 수 있습니다.

기본적으로 계정은 XML 전송 템플릿을 사용하도록 구성됩니다. 그러나 JSON을 사용하여 데이터를 검색 안내 서비스에 전달하려면 Adobe 컨설팅을 통해 도움을 받을 수 있습니다.

프레젠테이션 레이어에서 여러 검색 결과를 보여 주는 단일 프레젠테이션 템플릿을 사용할 수 있습니다. 각 검색은 동일한 전송 템플릿 또는 사용자 지정 전송 템플릿을 사용하여 데이터를 프레젠테이션 레이어로 전달할 수 있습니다. 전송 템플릿은 프레젠테이션 레이어로 데이터를 전달하는 데만 사용되므로 검색 결과를 표시하는 데 사용되는 HTML이 없어야 합니다. 템플릿은 전송 템플릿 태그를 사용하여 검색 결과와 패싯을 채우는 결과를 전달합니다. 이러한 태그 내에서 표준 검색 템플릿 태그가 실제 값을 표시하는 데 사용됩니다.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)를 참조하십시오.

**XML 전송 템플릿 관련 태그**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>XML 전송 템플릿 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>프레젠테이션 레이어가 전송 템플릿에서 구문 분석해야 하는 내용을 검색하는 데 사용하는 루트 XML 태그입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>결과 집합을 기반으로 요약 데이터를 제공하는 이 태그 집합 서라운드 검색 템플릿 태그입니다. 일반적으로 이러한 태그에는 총 결과 수, 가장 낮은 결과 및 가장 높은 결과에 대한 검색 태그가 포함됩니다. <span class="codeph"> 일반 필드 </span> 태그로 원하는 추가 전역 필드를 정의할 수 있습니다. </p> <p> <b>예</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합은 검색 결과 주위에 표시되므로 안내 검색을 통해 검색 위치를 알 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합은 각 검색 결과에 둘러싸여 있으므로, 검색 안내 기능에서 단일 검색 결과의 컨텐츠가 시작되고 끝나는 위치를 인식합니다. </p> <p> <b>예</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그를 사용하면 단일 결과를 위해 다중 값 목록의 각 항목을 반복할 수 있습니다. 결과 내에만 태그를 사용합니다. 이 변수의 주요 목적은 결과 필드에 속하는 속성을 반복하도록 하는 것입니다. </p> <p> <b>예</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합은 패싯을 채우는 결과를 전달합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>각 패싯에는 이름 매개 변수가 패싯 이름과 일치하는 고유한 패싯 태그가 있어야 합니다. 검색 태그는 패싯 값에 대한 패싯 태그 내에 사용됩니다. </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> 패싯 </a> 정보를 참조하십시오. </p> <p> <b>예</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합은 검색 안내 기능에서 제안 사항이 포함된 XML 노드를 인식할 수 있도록 추천 여부를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합은 각 추천 했습니까? </p> <p> <b>예</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**JSON 전송 템플릿 관련 태그**

검색 엔진에서 JSON과 XML을 전달하는 것이 페이로드가 적고 더 빠른 구문 분석기이기 때문에 더 빠른 것으로 알려져 있습니다. 그러나 JSON을 사용하여 구문 분석기가 허용하지 않으므로 출력 내용이 엄격한 JSON인지 확인하십시오.

JSON을 처음 사용하는 경우 다음 링크와 예제를 사용하여 시작하는 데 도움을 줄 수 있습니다.

* JSON 소개 [https://www.json.org/](https://www.json.org/)을(를) 참조하십시오.
* JSON을 테스트하여 유효한지 확인합니다. [https://jsonlint.com/](https://jsonlint.com/)을(를) 참조하십시오.

**JSON 템플릿 예**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**결과 특성 테이블이 있는 JSON 결과 섹션 예**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**연결된 필드가 있는 패싯에 대한 JSON 패싯 예**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**분할된 패싯에 대한 JSON 패싯 예**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## 새 프레젠테이션 또는 전송 템플릿 파일 {#task_73199757B6E748CAA604902FF913F012} 추가

**[!UICONTROL Add Template]**&#x200B;을 사용하여 프레젠테이션 템플릿(.tmpl) 또는 전송 템플릿(.tpl)을 [!DNL Templates] 페이지에 추가할 수 있습니다.

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**새 프레젠테이션 또는 전송 템플릿 파일을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지에서 **[!UICONTROL Add New Template]**&#x200B;을 클릭합니다.
1. [!DNL Add Template] 대화 상자에서 원하는 옵션을 설정합니다.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | 옵션 | 설명 |
   |--- |--- |
   | 새 파일 이름 | 추가할 템플릿의 이름을 지정합니다. 선택한 템플릿 유형에 따라 적절한 파일 확장자가 파일 이름에 자동으로 추가됩니다.  프레젠테이션 템플릿에는 .tmpl 파일 확장명이 있습니다.전송 템플릿에는 .tpl 파일 확장명이 있습니다. |
   | 새 템플릿 유형 | 추가할 전송 템플릿 또는 프레젠테이션을 선택할 수 있습니다.  [템플릿 정보](../c-about-design-menu/c-about-templates.md)를 참조하십시오. |

   [프레젠테이션 또는 전송 템플릿 편집](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)을 참조하십시오.
1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) [!DNL Templates] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 프레젠테이션 또는 전송 템플릿 편집 {#task_800E0E2265C34C028C92FEB5A1243EC3}

템플릿 편집기를 사용하여 프레젠테이션 및 전송 템플릿 파일의 컨텐츠를 보고 편집할 수 있습니다.

<!-- 

t_editing_a_template.xml

 -->

웹 사이트 방문자가 템플릿의 라이브 버전을 계속 사용하는 동안 스테이지된 프레젠테이션 및 전송 템플릿을 편집하고 테스트할 수 있습니다. 검색 도메인 URL의 단계 버전을 사용하여 스테이징 템플릿을 테스트합니다. 예를 들어 전송 템플릿의 이름으로 설정된 스테이지 쿼리( `sp_t`)를 실행하여 스테이지된 전송 템플릿을 테스트할 수 있습니다. `sp_staged=1` 레이아웃 표시 방식에 만족하면 템플릿 편집기 내에서 **[!UICONTROL Push Live]**&#x200B;을 사용하여 템플릿을 라이브로 푸시할 수 있습니다. 템플릿이 라이브되면 사이트 방문자가 템플릿을 사용하기 시작합니다.

프레젠테이션 템플릿 태그 참조를 사용하여 패싯, 탐색 표시 및 메뉴와 같은 검색 구성 요소에 프레젠테이션 템플릿을 연결하는 방법을 알아봅니다.

[프레젠테이션 템플릿 태그](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)를 참조하십시오.

전송 템플릿 태그 참조를 사용하여 전송 템플릿에서 사용할 태그에 대해 자세히 알아보십시오.

[전송 템플릿 태그](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)를 참조하십시오.

**[!UICONTROL To edit a presentation or a transport template]**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지에서 프레젠테이션 또는 전송 템플릿 파일 이름을 클릭합니다.
1. [!DNL Template Editor] 페이지에서 태그와 코딩에 대해 원하는 사항을 변경합니다.

   [!DNL Template Editor];에서 수행하는 변경 사항에 주의하십시오.실행 취소 기능은 없습니다. 원치 않는 변경 사항을 적용하고 이전 버전의 파일로 돌아가려면 **[!UICONTROL Cancel]**&#x200B;을 클릭하여 템플릿 테이블로 돌아갈 수 있습니다(변경 사항을 해당 시점까지 저장하지 않았다고 가정). 변경 내용을 이미 저장한 경우 편집기에서 **[!UICONTROL History]**&#x200B;을 사용하여 해당 변경 내용을 되돌릴 수 있습니다.
1. (선택 사항) 미국 영어 키보드에 해당 키가 없는 특수 문자 및 기호를 입력하려면 **[!UICONTROL Insert Symbol]**&#x200B;을 클릭합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

1. 완료되면 템플릿 편집기 페이지를 닫습니다.템플릿 페이지로 돌아갑니다.

## 프레젠테이션 또는 전송 템플릿 파일 {#task_B744AB3384C84DD59C33CD25E18C2C90} 복사

기존 프레젠테이션 템플릿(.tmpl) 또는 전송 템플릿(.tpl)을 복제하여 시간을 절약하고 템플릿 페이지에 추가할 수 있습니다.**[!UICONTROL Copy Template]**

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

템플릿 이름, 템플릿 유형 또는 둘 다를 변경해야 합니다. 변경하지 않으면 템플릿이 복사되지 않습니다.

템플릿을 복사할 수 있도록 이미 템플릿이 추가되어 있어야 합니다.

[새 프레젠테이션 또는 전송 템플릿 파일](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012) 추가를 참조하십시오.

**프레젠테이션 또는 전송 템플릿 파일을 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. 복사할 템플릿 이름 옆의 [!DNL Templates] 페이지의 드롭다운 목록에서 **[!UICONTROL Copy]**&#x200B;을 클릭합니다.
1. [!DNL Copy Template] 대화 상자에서 원하는 옵션 중 하나 이상을 설정합니다.
1. 클릭 **[!UICONTROL Copy]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 프레젠테이션 또는 전송 템플릿 파일 {#task_CC30050FC2DE4898BF44379D8378EB31} 이름 바꾸기

[!DNL Rename Template]을 사용하여 기존 프레젠테이션 템플릿(.tmpl) 또는 전송 템플릿(.tpl)의 이름을 변경할 수 있습니다.

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

원하는 경우 템플릿 유형을 변경할 수도 있습니다.

템플릿 이름을 변경하려면 이미 템플릿을 추가해야 합니다.

[새 프레젠테이션 또는 전송 템플릿 파일](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012) 추가를 참조하십시오.

**프레젠테이션 또는 전송 템플릿 파일의 이름을 바꾸려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. 이름을 변경할 템플릿 이름 옆의 [!DNL Templates] 페이지의 드롭다운 목록에서 **[!UICONTROL Rename]**&#x200B;을 클릭합니다.
1. [!DNL Rename Template] 대화 상자에서 원하는 옵션 중 하나 이상을 설정합니다.
1. 클릭 **[!UICONTROL Rename]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 프레젠테이션 또는 전송 템플릿 파일 {#task_67E532C2B83A449687737E3B06C5AA58} 삭제

**[!UICONTROL Delete Template]**&#x200B;을 사용하여 기존 프레젠테이션 템플릿(.tmpl) 또는 전송 템플릿(.tpl)을 제거할 수 있습니다.

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

라이브로 푸시된 스테이징 템플릿의 해당 버전이 이미 있을 수 있습니다. 그렇다면, 삭제된 템플릿이 라이브 환경에서도 삭제되도록 **[!UICONTROL Staging]**&#x200B;을 사용하여 실시간으로 푸시해야 합니다. 또는 템플릿 페이지에서 **[!UICONTROL Push Live]**&#x200B;을 사용할 수 있습니다.

[스테이징 정보](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7) 참조

[스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

템플릿을 삭제할 수 있도록 이미 템플릿이 추가되어 있어야 합니다.

[새 프레젠테이션 또는 전송 템플릿 파일 추가](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012) 참조

**프레젠테이션 또는 전송 템플릿 파일을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. 삭제할 템플릿 이름 옆의 [!DNL Templates] 페이지의 드롭다운 목록에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. [!DNL Delete Template] 대화 상자에서 **[!UICONTROL Delete.]**
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 프레젠테이션 템플릿 미리 보기 시 최소화된 {#task_1757B6207CC74221AE4BFFE5674D320B}

프레젠테이션 템플릿을 최소화하도록 선택하면 **[!UICONTROL Preview minimized]**&#x200B;을 사용하여 축소된 페이지 두께가 어떻게 표시되는지 확인할 수 있습니다.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

기본 프레젠테이션 템플릿을 최소화할 경우 이 옵션은 상속할 수 없으므로 포함 템플릿(안내 포함 태그 포함)을 최소화해야 합니다.

자세한 내용은 [프레젠테이션 템플릿의 페이지 무게 줄이기..](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

최소화된 템플릿을 미리 보려면 템플릿이 이미 추가되어 있어야 합니다.

[새 프레젠테이션 또는 전송 템플릿 파일 추가](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012) 참조

전송 템플릿 파일의 XML 코드를 미리 볼 수 있습니다.

전송 템플릿 파일](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)의 XML 미리 보기를 참조하십시오.[

**최소화 상태로 프레젠테이션 템플릿을 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지의 프레젠테이션 템플릿 이름 옆에 있는 드롭다운 목록에서 **[!UICONTROL Preview minimized]**&#x200B;을 클릭합니다.

   템플릿 테이블의 **[!UICONTROL Type]** 열을 사용하여 템플릿을 프레젠테이션 및 전송별로 정렬합니다.
1. (선택 사항) [!DNL Preview Minimized Template] 페이지에서 **[!UICONTROL Wrap lines]**&#x200B;을 선택하여 정의된 창에서 태그를 읽습니다.
1. 클릭 **[!UICONTROL Close]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 웹 사이트 {#task_B09BB3CE89714DEAAE8D9A899CF3009E}에 있는 프레젠테이션 템플릿의 페이지 가중치 감소

템플릿 테이블의 **[!UICONTROL Minimize]** 옵션을 사용하여 프레젠테이션 템플릿의 페이지 가중치를 줄일 수 있습니다.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

템플릿의 페이지 두께를 줄여 인라인 JavaScript 및 CSS를 동적으로 최소화할 수 있습니다. HTML에서 불필요한 공백도 제거합니다. 프레젠테이션 템플릿의 페이지 무게를 최소화하면 검색 결과를 보다 신속하게 전달할 수 있습니다.

**[!UICONTROL Preview minimized]**&#x200B;을 사용하여 최소화된 프레젠테이션 템플릿의 모양을 미리 볼 수도 있습니다.

[프레젠테이션 템플릿 미리 보기](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)를 참조하십시오.

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지의 [!DNL Minimize] 열에서 웹 사이트에서 최소한으로 푸시할 하나 이상의 프레젠테이션 템플릿 파일의 상자를 선택합니다.

   [!DNL Templates] 테이블의 **[!UICONTROL Type]** 열을 사용하여 프레젠테이션 및 전송별로 템플릿을 정렬합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 웹 사이트 {#task_C1E8CE817E4D43E096167A347C54DD53}에서 사용할 기본 프레젠테이션 템플릿 파일 설정

여러 프레젠테이션 템플릿이 있는 경우 검색 결과를 표시하는 데 처음에 사용할 템플릿을 표시할 수 있습니다.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

사전 검색 규칙, 사후 검색 규칙 및 비즈니스 규칙을 사용하여 다른 프레젠테이션 템플릿 중 하나를 사용해야 하는 시기를 결정할 수 있습니다.

[사전 검색 규칙 정보](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F)를 참조하십시오.

[사후 검색 규칙 정보](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE)를 참조하십시오.

[비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

&quot;모든 검색에 대해 타깃팅된 프레젠테이션 템플릿을 xxxx로 설정합니다&quot;와 같은 규칙을 사용하는 것이 일반적입니다. 이러한 규칙을 적용하면 템플릿 페이지에서 &quot;기본&quot; 템플릿을 변경해도 아무런 효과가 없는 것으로 나타납니다.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지의 [!DNL Default] 열에서 기본적으로 사용할 해당 프레젠테이션 템플릿 파일의 라디오 단추를 클릭합니다.

   [!DNL Templates] 테이블의 **[!UICONTROL Type]** 열을 사용하여 프레젠테이션 및 전송별로 템플릿을 정렬합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 전송 템플릿 파일 {#task_58C6C52078E14AD88D2B2F0B3C439AE8}의 XML 미리 보기

[!DNL Preview]을 사용하여 추가한 전송 템플릿의 XML을 검토할 수 있습니다.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

템플릿의 XML을 미리 보려면 전송 템플릿이 이미 추가되어 있어야 합니다.

[새 프레젠테이션 또는 전송 템플릿 파일](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012) 추가를 참조하십시오.

최소화된 프레젠테이션 템플릿 파일을 미리 볼 수 있으므로 페이지 두께가 줄어듭니다.

[프레젠테이션 템플릿 미리 보기](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)를 참조하십시오.

**전송 템플릿 파일의 XML을 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Templates]**&#x200B;을 클릭합니다.
1. [!DNL Templates] 페이지의 전송 템플릿 이름 옆에 있는 드롭다운 목록에서 **[!UICONTROL Preview]**&#x200B;을 클릭합니다.

   [!DNL Templates] 테이블의 **[!UICONTROL Type]** 열을 사용하여 프레젠테이션 및 전송별로 템플릿을 정렬합니다.
1. 보기 창을 닫고 [!DNL site search/merchandising]으로 돌아갑니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

