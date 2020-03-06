---
description: 'null'
seo-description: 'null'
seo-title: 템플릿
solution: Target
title: 템플릿
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# 템플릿{#templates}

## 템플릿 {#concept_A5CFB6BD805D49459A96219AF1B17842}

## 프레젠테이션 템플릿 태그 {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

프레젠테이션 템플릿의 사이트 검색/머천다이징 태그 및 속성 목록입니다.


프레젠테이션 템플릿은 사이트 검색/머천다이징에서 정의하는 프레젠테이션 템플릿 태그를 포함하는 HTML 파일입니다. 이러한 태그는 고객이 보는 검색 결과의 형식을 나타냅니다.

템플릿 [정보를 참조하십시오](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

다음 프레젠테이션 태그 그룹 중에서 선택할 수 있습니다.

* [선언](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [결과](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [패싯](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [탐색 표시](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [메뉴](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [최근 검색](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [원하는 작업](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [자동 완성](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [스토어](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [영역](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [루프 표시기](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [기타 언어](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## 선언 {#section_82C5CA734D2941EB858FEFE3B695D2EC}

선언은 최상위 프레젠테이션 템플릿의 맨 위에 설정할 수 있는 특별한 안내 선언 태그입니다. 포함된 템플릿의 선언을 포함하여 이후의 모든 선언은 무시됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>기본적으로 프레젠테이션 템플릿은 MIME 유형의 텍스트/html과 함께 다시 전송됩니다. 이 태그에 사용되는 콘텐츠 형식을 변경할 수 있습니다. </p> <p>프레젠테이션 템플릿에서 이 태그를 가능한 한 높게 선언합니다. 이 태그와 같은 행에 다른 텍스트를 추가하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> XML을 반환하는 경우 이 태그를 사용하여 XML 선언을 만들 수 있습니다. 이 태그를 프레젠테이션 템플릿의 첫 번째 줄로 만듭니다. 이 태그를 사용하면 첫 번째 행에 <span class="codeph"> &lt;guided-content-type-header&gt; </span> 를 사용하여 규칙을 오버레이하지 않는 한, 내용 유형이 자동으로 text/xml로 설정됩니다. charset을 지정하지 않으면 기본적으로 UTF-8이 사용됩니다. 이 태그로 인해 XML 문서에서 다음 출력물이 생성됩니다. </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> &lt;guided-results [gsname="searchname"]&gt;&lt;/guided-results&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>안내 결과 태그는 결과 루프의 경계를 정의합니다. gsname <span class="codeph"> </span> 속성을 지정하여 모든 결과 세트에 액세스할 수 있습니다. gsname을 <span class="codeph"> </span> 지정하지 않으면 기본 검색 결과가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> &lt;guided-result-link [gsname="fieldname"] [attr="value"]+&gt;&lt;/guided-result-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>지정된 결과에 대한 링크를 만들려면 <span class="codeph"> 안내 결과 링크 </span> 태그를 사용합니다. gsname <span class="codeph"> </span> 속성을 정의하여 "search-url"을 참조하는 표준 "loc" 태그 대신 인덱스의 필드를 사용할 수 있습니다. 클래스 및 대상과 같은 다른 모든 속성도 전달될 수 있으며 결과 앵커 태그로 출력됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> &lt;guided-result-img gsname="fieldname" [attr="value"]+&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>&lt;guided-result-img&gt; <span class="codeph"> 태그는 원시 </span> img <span class="codeph"> </span> 태그 내에 변수를 내장하지 않고 이미지 태그를 만드는 데 도움이 됩니다. </p> <p>gsname <span class="codeph"> </span> 속성에서 이미지 경로에 사용할 필드를 지정합니다. 그 결과는 <span class="codeph"> img </span> 태그로, 사용자가 정의하거나 전달한 표준 HTML 속성이 있습니다. 다음 예를 참조하십시오. </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> &lt;guided-result-field gsname="fieldname" [escape="html|url|js|json|json|0"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 결과에 표시할 모든 정보는 <span class="codeph"> &lt;guided-result-field&gt; </span> 태그로 표시됩니다(&lt;guided-result-img&gt; <span class="codeph"> </span> 태그와 같은 자동 생성 태그를 사용하는 경우는 제외). </p> <p>gsname에서 검색 인덱스 필드의 이름을 <span class="codeph"> 지정합니다 </span>. 전달된 정확한 문자열은 템플릿에 출력됩니다. </p> <p>이 필드를 전송 템플릿에서 지정한 내용과 다르게 이스케이프 옵션을 지정할 수 있습니다. </p> <p>이 인코딩은 전송 템플릿에 지정된 인코딩의 맨 위에 적용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="fieldname&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그 세트는 표시할 특정 필드에 컨텐츠가 있으면 적용됩니다. 컨텐츠가 없으면 조건이 false입니다. 이 태그를 사용하여 값이 없는 경우 주변 HTML을 표시할지 또는 다른 이미지가 표시되는지 등을 결정할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>결과를 열에 표시할 때 이 태그는 현재 결과가 열의 끝을 표시하는지 여부를 식별하는 데 사용됩니다. </p> <p>부울 조건이 true이면 HTML이 결과 끝에 추가되어 행을 끝내고 새 행을 시작합니다. 마지막 행이면 새 행이 시작되지 않습니다. </p> <p>해당 태그에 대한 자세한 내용은 <span class="codeph"> &lt;guided-if-not-last&gt; </span> 를 참조하십시오. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> &lt;guided-results-found [gsname="searchname"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>백엔드 검색 요청이 결과를 반환하면 1을 반환하고 그렇지 않으면 0을 반환합니다. 지정된 <span class="codeph"> </span> gsname이 없으면 태그는 기본 검색을 가정합니다. 이 태그는 JavaScript 루틴으로 논리를 전달하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-results-total [gsname="searchname"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>지정된 결과 세트의 총 결과 수를 반환합니다. gsname이 제공되지 않을 때 <span class="codeph"> 기본 검색을 </span> 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-results-lower [gsname="searchname"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>지정된 결과 집합에 대한 페이지에서 낮은 결과의 결과 수를 반환합니다. gsname이 제공되지 않을 때 <span class="codeph"> 기본 검색을 </span> 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-results-upper [gsname="searchname"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>지정된 결과 집합에 대한 페이지의 상위 결과의 결과 수를 반환합니다. gsname이 제공되지 않을 때 <span class="codeph"> 기본 검색을 </span> 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>결과를 찾을 때 컨텐츠를 표시합니다. 또는 결과가 없을 때 HTML 결과를 표시하지 않습니다. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided- <span class="codeph"> result-title&gt; </span> 태그는 <span class="codeph"> &lt;title&gt; </span> 전송 태그로 지정된 제목 전송 템플릿 필드의 값을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided- <span class="codeph"> result-description&gt; </span> 태그는 <span class="codeph"> &lt;description&gt; </span> 전송 태그로 지정된 설명 전송 템플릿 필드의 값을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt; <span class="codeph"> guided-result-loc&gt; </span> 태그는 <span class="codeph"> &lt;loc&gt; </span> 전송 태그로 지정된 위치 전송 템플릿 필드의 값을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>표시할 특정 필드에 컨텐츠가 있으면 true입니다. 컨텐츠가 없으면 조건이 false입니다. 태그를 사용하여 주변 HTML의 표시 여부 또는 값이 없는 경우, 또는 다른 이미지가 표시되는 경우 등을 결정할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tabename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 <span class="codeph"> &lt;attribute_table&gt; </span> 전송 태그로 전송 템플릿에 정의된 속성 테이블을 통해 루프를 제공합니다. 속성 테이블 필드 값을 표시하기 위한 <span class="codeph"> &lt;guided-result-attribute-table-field&gt; </span> 태그가 있습니다. 또한 다른 결과 필드를 표시하기 위해 루프 내에 일반 <span class="codeph"> 안내 결과 필드 </span> 태그를 사용할 수도 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>전송 템플릿에 정의된 대로 속성 테이블 필드를 표시합니다. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;lt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;lt;li&amp;gt;
    &amp;nbsp;&amp;nbsp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;&amp;nnbsp; lt;a&amp;nbsp;nbsp;nbsp;href=&quot;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&amp;nbsp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp; nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;nbsp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;alt;&amp;;nbsp;;lt;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&quot;gt;)nbsp&amp;nbsp&amp;lt/lt;gt;lt&amp;gt;lt/lt-result-amp;gt&amp;gt;guided;lt&amp;guided&amp;gop;gov
    
    
    
    
    
    
    
    ;goodl&amp;
    
    &amp;lt;/guided-results&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> &lt;guided-trace [gsname="searchname"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>지정된 검색에 대한 전송 템플릿을 통해 JSON 데이터 출력의 일반 섹션 내에 있는 추적 데이터에 있는 추적 정보를 출력합니다. </p> <p>검색 이름을 지정하지 않으면 <span class="codeph"> 기본값이 </span> 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> &lt;guided-result-trace/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>현재 검색 결과에 대한 전송 템플릿으로 JSON 데이터 출력의 결과 &gt; 추적 정보 내에 있는 JSON 콘텐츠를 출력합니다. </p> <p>이 태그는 <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> 루프 내에서만 유효합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 패싯 {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

패싯은 검색 결과로 드릴다운할 수 있는 탐색 구성 요소입니다. 패싯 태그를 사용하여 프레젠테이션 템플릿의 다양한 패싯을 표시할 수 있습니다. 이름별로 패싯을 참조합니다.

패싯 [정보를 참조하십시오](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

[단면 레일 정보](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB)를 참조하십시오.

동적 패싯 [정보를 참조하십시오](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> &lt;guided-dynamic-facet&gt;&lt;/guided-dynamic-facet&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>지정된 검색에 대한 동적 패싯에 대한 루핑 컨텍스트. </p> <p>&lt;guided- <span class="codeph"> facet&gt; </span> 프레젠테이션 템플릿 태그가 편집되어 gsname 속성이 <span class="codeph"> &lt;guided-dynamic-facets&gt; 루핑 </span> 컨텍스트에서 자동으로 제공됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>패싯의 표시 레이블을 반환합니다. </p> <p>패싯이 전송 템플릿에서 <span class="codeph"> &lt;display-name&gt; </span> &gt; 태그를 사용하는 경우 해당 태그의 컨텐츠가 레이블이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 패싯 레일의 각 패싯에 대한 반복 패턴으로 사용되는 프레젠테이션 템플릿의 섹션을 정의합니다. </p> <p> 패싯 레일에 속하는 각 패싯은 이 섹션을 사용하여 출력을 평가합니다. </p> <p>다음은 패싯 레일의 예입니다. </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>&lt;guided-facet-rail&gt; <span class="codeph"> 태그 내에서 값이 검색 시 동적으로 결정되고 올바르게 대체되므로 다음 태그는 </span> gsname <span class="codeph"> </span> 속성이 필요하지 않습니다. </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">guided-facet </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">guided-facet-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">guided-facet-behavior </li> 
    </ul> <p>패싯 레일 <span class="wintitle"> 페이지의 정렬 </span> 기준은 패싯의 위치를 결정합니다. 패싯 정렬 방법 드롭다운 목록에서 정렬 순서를 선택할 수 있습니다. </p> <p> 
     <!--NEW 02/27/2014-->이 태그는 선택적으로 _dynamic_facets의 <span class="codeph"> gsname 속성 값을 허용할 수 있습니다. 이 </span>값은 이 검색에 대한 모든 동적 패싯에 대한 루프 컨텍스트를 제공합니다. 이 사전 정의된 패싯 레일은 패싯 레일 '_dynamic_facets'의 작업 <span class="codeph"> 푸시 패싯 X에 대한 Business Rules 사용자 인터페이스에서도 노출되어 Y </span>"를 배치합니다. </p> <p><a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">단면 레일 정보</a>를 참조하십시오 . </p> <p>동적 패싯 <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 정보도 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>안내 <span class="codeph"> 패싯 </span> 태그를 사용하여 모든 패싯 태그가 특정 패싯과 관련된 영역을 정의합니다. 이 태그는 패싯에 값이 없을 경우 모든 컨텐츠를 숨기는 부울 태그이기도 합니다. 이러한 경우 패싯 값을 출력하는 데 포인트가 없습니다.) </p> <p>높이 및 폭 속성은 선택 사항이며 크기는 픽셀(px)로 지정됩니다. VRB(Visual Rule Builder)는 이러한 두 가지 특성을 사용하고 패싯이 숨겨져 있을 때 점선 상자를 대화형 자리 표시자로 표시합니다. </p> <p> 표시 이름이 패싯에 있고 패싯이 숨겨져 있으면 이름도 숨겨집니다. 하지만 이름이 패싯 외부에 있는 경우 <span class="codeph"> 영역 </span> 태그 또는 <span class="codeph"> 도우미-if-facet-visible </span> 태그가 패싯 주위에 래핑된 경우에만 이름을 숨길 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 패싯 값의 수가 구성에 정의된 길이 임계값을 초과할 때 적용됩니다. 목록이 너무 길면 패싯을 다른 UI 요소(예: 잘린 목록 또는 스크롤 상자)로 표시할 수 있습니다. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 패싯을 한 번 이상 클릭하고 현재 패싯 값을 선택한 경우 적용됩니다. 패싯을 클릭했는지 여부에 따라 HTML 또는 gs 태그를 표시하거나 숨기는 데 사용됩니다. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> &lt;guided-if[-not]-facet-single [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-single&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 단면화 값이 하나만 있으면 true입니다. 결과를 조정할 수 없는 경우 태그를 사용하여 패싯 표시를 변경합니다. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>패싯이 다중 선택인 경우 이 조건부 태그는 true입니다. 태그를 사용하여 <span class="codeph"> &lt;guided-facet-rail&gt; </span> 또는 <span class="codeph"> &lt;guided-dynamic-facet&gt; </span> 태그 내의 패싯 표시를 변경합니다. </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-facet-values [gsname=" <span class="codeph"> facetname <span class="varname"> </span>"]&gt;&lt;/guided-facet-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>이것은 패싯 값 루프 반복기 태그입니다. 이름이 지정된 <span class="codeph"> 안내에 패싯 </span> 블록의 컨텍스트 내에서 정의할 수 있습니다. 이 경우 <span class="codeph"> gsname을 <span class="varname"> 생략할 수 </span> </span>있습니다. 또는 임의의 <span class="codeph"> 안내에 패싯 </span> 블록 외부에서 정의할 수 있지만, <span class="codeph"> gsname <span class="varname"> </span> </span> 속성이 어떤 패싯 값 세트를 표시할지를 식별해야 합니다. </p> <p>이 태그를 사용하여 지정된 <span class="codeph"> 안내 패싯 </span> 블록의 컨텍스트 외부에 패싯 값을 표시할 수도 있습니다. gsname <span class="codeph"><span class="varname"> </span> </span> 속성을 사용하여 직접 특정 패싯을 참조합니다. </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> &lt;guided-facet-value [escape="html|url|js|json|0"]/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>현재 패싯 값의 문자열을 출력합니다. </p> <p>기본적으로 값은 HTML escape입니다. escape 옵션을 사용하여 값의 이스케이프 처리를 변경할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> &lt;guided-facet-count/&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>현재 패싯 값과 일치하는 결과 수를 출력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> &lt;guided-facet-value-link [attr="value"]+&gt;&lt;/guided-facet-value-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>사이트 방문자가 클릭할 패싯 값 문자열 주위에 링크를 만듭니다. 현재 패싯 값으로 결과 범위를 좁히기 위해 경로가 자동으로 생성됩니다. 앵커 태그에 바로 속성을 전달할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>패싯 값이 현재 선택된 경우 해당 값의 표시를 변경합니다. 이미 선택한 경우 대부분의 경우 더 이상 연결할 수 없습니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-value-ghost&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>패싯 값이 고스트 값일 때 해당 값의 표시를 변경합니다. 패싯 값이 고스트 값이면 값이 누락되었거나 "ghosted"임을 나타내기 위해 일반적으로 기울임체 텍스트로 표시됩니다. </p> <p>다음 코드 발췌문은 패싯 블록의 예입니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> &lt;guided-facet-undo-link gsname=" <span class="codeph"> facetname <span class="varname"> </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>지정된 패싯에 대한 실행 취소 링크를 표시합니다. 다중 선택 패싯이 있는 경우, 이 링크는 지정된 패싯의 모든 값을 선택 취소합니다. 패싯에 이름을 지정합니다. 패싯이 현재 선택되지 않은 경우 링크는 현재 경로입니다. </p> <p>다음은 이 태그 사용의 예입니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 패싯 값의 수가 구성에 정의된 길이 임계값을 초과할 때 적용됩니다. 목록이 너무 길면 패싯을 다른 사용자 인터페이스 요소(예: 잘린 목록 또는 스크롤 상자)로 표시할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> <span class="varname"> </span> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 패싯을 한 번 이상 클릭하고 현재 패싯 값을 선택한 경우 적용됩니다. 패싯을 클릭했는지 여부에 따라 HTML 또는 gs 태그를 표시하거나 숨기는 데 사용할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 단면화 값이 하나만 있으면 true입니다. 결과를 조정할 수 없는 경우 패싯의 표시를 변경하는 데 사용할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>gsname <span class="codeph"> 속성을 사용하여 직접 특정 패싯을 참조하여 명명된 </span> 안내 패싯 <span class="codeph"> <span class="varname"> </span> </span> 블록의 컨텍스트 외부에서 이 조건을 사용할 수도 있습니다. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>이 조건을 사용하면 지정된 패싯에 값이 있는지 여부를 확인할 수 있습니다. 빈 패싯이 아닌 다른 패싯을 표시하는 데 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>주어진 패싯 내에 있는 총 결과 수를 출력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> 관련 사용자 지정 패싯 값 </span>" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>패싯과 연결된 값의 문자열을 출력합니다. 패싯에 0개 이상의 필드를 연결할 수 있습니다. 연관된 필드가 있는 것은 드물고 이러한 필드를 지원하는 것은 전송 템플릿을 구성합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> associated custom facet value </span>"/&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>패싯 값에 연결된 필드 값이 있는지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [attr=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>고객이 클릭할 패싯 값 문자열 주위에 링크를 만듭니다. 현재 패싯 값으로 결과 범위를 좁히기 위해 경로가 자동으로 생성됩니다. 앵커 태그에 바로 속성을 전달할 수 있습니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>패싯 값에 대한 링크를 만듭니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>기본적으로 값은 URL escape입니다. 그러나 escape 매개 변수를 통해 사용할 이스케이프 모드를 지정하여 다른 인코딩 레이어를 추가할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;guided- <span class="codeph"> facet-values&gt;는 각 패싯 값을 </span> 반복하여 중첩 패싯의 모든 하위 값을 반복합니다. 이 태그 내에서 링크를 만들고, 실행 취소 링크를 만들고, 패싯 값을 표시하기 위해 일반적인 패싯 태그를 사용합니다. 이 태그는 중첩된 루프를 <span class="codeph"> &lt;guided-facet-values&gt; 내에 있어야 </span> 합니다. </p> <p>이 태그를 사용하는 예는 다음과 같습니다. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 패싯 값에 하위 값이 있는지 테스트합니다. &lt;guided-facet-value-children&gt; <span class="codeph"> </span> 태그를 사용하기 전에 사용하는 것이 좋습니다. "else" 절은 선택 사항입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-above-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-above-length-threshold&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>패싯 값 루프 내의 현재 패싯 값이 길이 임계값을 초과하는지 여부를 결정합니다. 일반적으로 사용자가 이전에 패싯 아래에 표시된 "자세히 보기" 링크를 선택하지 않은 경우 긴 패싯의 임계값 미만 값만 표시하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>패싯 값 루프 내의 현재 패싯 값이 길이 임계값과 같은지 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>지정된 패싯 값에 대한 실행 취소 링크를 표시합니다. 선택한 패싯 값 옆에 실행 취소 링크를 표시하는 데 사용합니다. 이 실행 취소 링크는 특정 선택한 값만 취소하므로 선택한 모든 값을 선택 취소하는 <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> 와 다릅니다. </p> <p> <p>참고: 패싯에 다중 선택 비헤이비어가 없는 경우 두 실행 취소 링크의 동작이 동일합니다. 즉, 패싯은 하나의 선택된 값만 가질 수 있습니다. </p> </p> <p>패싯이 현재 선택되지 않은 경우 링크는 현재 경로입니다. 이 태그는 <span class="codeph"> 안내 패싯 값 </span> 루프 내에서만 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>직접 패싯 값 실행 취소 링크를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>나만의 패싯 실행 취소 링크를 만듭니다. </p> <p> 자체 실행 취소 링크를 만들 수 있는 원시 경로를 제공한다는 점을 제외하고 <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> 태그와 유사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>주어진 패싯에 선택한 값 또는 단일 값 "값"이 있으면 조건부로 HTML을 표시합니다. 이 태그 집합은 다른 패싯에서 선택한 값을 기준으로 패싯을 표시하는 데 종종 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>단면화 동작(예: 일반, 고정 또는 다중 선택)을 결정합니다. XML 결과를 받고 패싯의 작동 방식을 동적으로 변경하려는 고객에게 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> <varname></varname>

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>이 태그가 래핑하는 컨텐츠는 패싯의 가시성 상태에 따라 숨겨지거나 표시됩니다. 비즈니스 규칙이 패싯을 직접 숨기거나 표시하는 경우 패싯 내의 모든 컨텐츠가 숨겨지거나 표시됩니다. 이러한 태그는 패싯을 둘러싸는 데 필요하지 않습니다. </p> <p> 이 태그의 일반적인 사용은 이름이 패싯 외부에 있을 때 표시 이름을 숨기는 것입니다. 표시 이름 주위에 이 태그를 둘러싸면 패싯이 숨겨져 있을 때 이름이 사라집니다. </p> <p>이 태그는 영역을 대체하며 영역을 사용하는 것과 동일한 성능 이점을 많이 제공합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 탐색 표시 {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

탐색 [표시 정보를 참조하십시오](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb [gsname=" <span class="varname"> breadcrumname </span>"]&gt;&lt;/guided-breadcrumb&gt; </span> </p> </td> 
   <td colname="col2"> <p>탐색 표시에 대한 루프 태그입니다. 열기 태그와 닫기 태그 사이의 모든 컨텐츠는 현재 상태의 각 쿼리 번호에 대해 반복됩니다. </p> <p>gsname <span class="codeph"> 을 <span class="varname"> </span> </span> 생략하면 "default"라는 브레드크럼이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/guided-breadcrumb-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>탐색 경로에서 링크를 만듭니다. 기본 동작은 "goto" 동작입니다. 링크가 다르게 동작하는 경우 gsname <span class="codeph"> <span class="varname"> </span> </span> 선택적 속성을 사용하여 "remove" 또는 "drop"을 지정합니다. 태그에 포함된 모든 속성은 결과 앵커 태그로 전달됩니다. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> &lt;guided-breadcrumb-value /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>값 태그는 현재 탐색 표시 반복의 변형된 값을 인쇄합니다. 이것은 <span class="codeph"> 안내 탐색 표시 </span> 블록의 컨텍스트에서만 사용됩니다. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> &lt;guided-breadcrumb-label /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>레이블 태그는 탐색 표시 항목을 생성하기 위해 선택한 패싯을 자세히 설명하는 탐색 표시 값에 대한 레이블을 출력합니다. 이것은 <span class="codeph"> 안내 탐색 표시 </span> 블록의 컨텍스트에서만 사용됩니다. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그는 현재 탐색 표시 값에 레이블이 있는 경우 조건부로 컨텐츠를 표시하는 데 사용됩니다. 레이블이 실제로 존재하는 경우에만 레이블을 표시하고 내용을 연결하는 데 사용됩니다. 이것은 <span class="codeph"> 안내 탐색 표시 </span> 블록의 컨텍스트에서만 사용됩니다. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path [gsname="goto|remove|drop"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>나만의 탐색 표시 링크를 만드는 데 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 메뉴 {#section_1D489ADF041F4351A66E5D5742125CA8}

메뉴 [정보를 참조하십시오](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>메뉴 값 루프 반복기 태그입니다. gsname <span class="codeph"> </span> 속성을 사용하여 표시되는 메뉴 항목 세트를 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu-item-link [attr="value"]+&gt;&lt;/guided-menu-item-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>메뉴 항목에 대한 현재 검색을 세부적으로 조정할 수 있는 URL을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu-item-option [attr="value"]+ /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>일반적으로 메뉴는 템플릿의 선택 컨트롤에 표시됩니다. 이 태그는 select 컨트롤에 대한 옵션을 생성하기 위한 HTML을 생성하므로 선택 컨트롤을 쉽게 구성할 수 있습니다. </p> <p>예를 들어, 다음 코드 블록은 다음과 같습니다. </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>다음과 같이 HTML을 생성할 수 있습니다. </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu-item-value /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>메뉴와 연관된 값의 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu-item-label /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>메뉴와 연관된 레이블의 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-menu-item-path /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>경로 문자열을 반환합니다. 경로에 매개 변수를 추가하고 사용자 지정 링크를 만들려면 태그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 메뉴 항목을 선택했는지 여부를 나타내는 1 또는 0을 반환합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

페이지 탐색 태그를 사용하여 사용자가 검색 결과를 통해 페이지를 이동할 수 있는 링크 집합을 만들 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-pages&gt;&lt;/guided-pages&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>페이지 탐색을 위한 루프 태그입니다. 여는 태그와 닫는 태그 사이의 모든 컨텐츠는 각 페이지에 대해 반복됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-page-link [attr="value"]+&gt;&lt;/guided-page-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>페이지 탐색에 링크를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-page-link gsname="first|prev|next|last|viewpages|viewpages" [attr="value"]+&gt;&lt;/guided-page-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>첫 번째, 이전, 다음 또는 마지막 페이지에 대한 링크를 만듭니다. 링크를 만들어 한 페이지에서 모든 페이지를 볼 수도 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-page-number /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 현재 페이지 번호가 있는 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그 집합은 현재 반복되는 페이지를 선택한 경우 적용됩니다. 일반적으로 페이지 탐색 컨트롤에서 페이지 번호를 다르게 표시하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> 이 조건부 태그 집합은 현재 페이지에 이전 페이지가 있는 경우 적용됩니다. 일반적으로 페이지 탐색 시 이전 링크를 표시하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> 현재 페이지에 다음 페이지가 있는 경우 이 조건부 태그 세트가 적용됩니다. 일반적으로 페이지 탐색 시 이전 링크를 표시하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> 검색에서 큰 결과 집합을 반환하는 경우 모든 결과를 볼 수 있는 기능을 제공하지 않을 수 있습니다. 따라서 이 조건부 태그 집합을 사용하여 모든 보기 링크를 표시할 시기를 결정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건부 태그 집합을 사용하여 페이지 보기 링크를 표시할 시기를 결정할 수 있습니다. 일반적으로 고객이 특정 페이지를 보도록 허용하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>페이지 탐색에 첫 번째 페이지, 이전 페이지, 다음 페이지 등이 있는지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> &lt;guided-page-total /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 검색 결과의 총 페이지 수를 포함하는 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>페이지 탐색 설정이 거의 정의되지 않은 경우 <span class="codeph"> 안내 페이지 </span> 태그를 사용하여 모든 페이지 매김 태그가 특정 페이지 매김 설정과 관련된 영역을 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewwall|viewpages]/&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>페이지 탐색에 자신만의 링크를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>페이지 탐색에서 가장 높은 페이지가 총 페이지 수와 같은지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>페이지 탐색의 가장 낮은 페이지가 가장 같은지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>결과 한 페이지나 여러 페이지가 있는지 테스트합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 최근 검색 {#section_8CD907521F584257B475595B01A5964B}

다음 예와 같이 최근 검색 태그를 사용하여 사용자가 이전 검색을 빠르게 실행할 수 있는 링크 세트를 만들 수 있습니다.

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

최근 [검색](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562)구성을 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>최근 검색을 위한 루프 태그입니다. 여는 태그와 닫는 태그 사이의 모든 컨텐츠는 각 페이지에 대해 반복됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>최근 검색에 대한 링크를 만들 수 있습니다. 또한 모든 HTML 속성을 앵커 태그로 직접 전달할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>최근 검색 <span class="codeph"> 안내 </span> 루프 내에서 최근 검색에 대한 상대 URL 경로를 선택할 수 있습니다. 일반적으로 <span class="codeph"> 안내 검색 링크를 사용합니다 </span>. 그러나 자신의 링크를 빌드하려는 경우 이 태그를 사용할 수 있습니다. 다음은 예입니다. </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>최근 검색과 관련된 쿼리 용어를 선택할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link [attr="value"]+&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>고객에게 최근에 저장한 검색을 지울 수 있는 기능을 제공할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>직접 링크를 만들 수 있도록 <span class="codeph"> &lt;guided-recent-searches-clear-link&gt; </span> 에서 사용하는 경로를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-recent-searches&amp;gt;&lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>고객이 최근 검색을 수행한 최근 검색을 표시할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 원하는 작업 {#section_C1EB3B9D8E1242798A6E04609D1E3543}

검색 결과가 반환되지 않고 검색어가 계정의 사전에 없는 경우 태그를 사용하여 제안 링크 집합을 만들 수 있습니다. 다음은 Did You Mean 태그를 사용하는 예입니다.

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

[다음을 찾으려고 하셨습니까? 정보](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)를 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> &lt;guided-suggestions&gt;&lt;/guided-suggestions&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>제안 사항을 루프하기 위한 루프 태그입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> &lt;guided-provision-link [attr="value"]+&gt;&lt;/guided-provision-link&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>주어진 제안에 대한 링크를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> &lt;guided-provision-value /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>제안이 있는지 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-propose-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>제안에 대한 경로 문자열을 반환합니다. 이를 사용하여 고유한 앵커 태그를 만들 수 있습니다. 일반적으로 <span class="codeph"> 안내 제안 링크가 </span> 대신 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-propose/&gt; </span> </p> </td> 
   <td colname="col2"> <p>제안. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-propose-result-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>제안의 결과 카운트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 기능이 켜진 경우에 대비하여 0개의 결과로 자동 검색이 수행되었는지 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-propoision-original-query/&gt; </span> </p> </td> 
   <td colname="col2"> <p>자동 검색이 수행된 경우 원래 쿼리를 반환합니다. </p> <p>사용 예: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 기능이 켜진 경우에 대비하여 낮은 결과 카운트로 인해 제안이 있는 경우 이 조건이 적용됩니다. </p> <p>다음은 이 태그를 사용하는 예입니다. </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 자동 완성 {#section_897316BEE1454E839A56B565CA4AF018}

다음 태그를 사용하여 검색 양식에 자동 완성 기능을 추가할 수 있습니다. 자동 완성 기능을 올바르게 만들려면 헤드 컨텐츠 및 양식 컨텐츠 태그가 필요합니다. 프레젠테이션 템플릿에 자동 완성 Javascript 및 CSS를 하드 코딩하는 대신 태그를 사용하는 것이 좋습니다. 이유는 태그를 사용하면 템플릿을 수동으로 업데이트하지 않고 자동 완성 설정을 변경할 때마다 템플릿에서 새로운 실패 캐시 ID를 선택할 수 있기 때문입니다.

자동 [완성 정보를 참조하십시오](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>자동 완성 기능이 활성화되어 있는지 여부를 검색합니다. 태그를 사용하여 자동 완성에 필요한 헤드 및 양식 컨텐츠를 선택적으로 가져올 수 있습니다. 이렇게 하면 프레젠테이션 템플릿을 변경할 필요 없이 기능을 켜거나 끌 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>프레젠테이션 템플릿의 헤드에 사용되고 자동 완성 기능을 위한 해당 CSS 스크립트로 대체됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content/&gt; </span> </p> </td> 
   <td colname="col2"> <p>양식 내의 자동 완성 태그를 하드 코딩하는 대신 프레젠테이션 템플릿의 검색 양식( <span class="codeph"> &lt;form&gt; </span> 및 <span class="codeph"> &lt;/form&gt; </span> 태그 사이)에 사용됩니다. 태그가 자동 완성 작업에 필요한 HTML로 대체됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>자동 완성 JavaScript에 대한 링크를 생성합니다. 최상의 성능을 위해 이 태그를 닫는 "body" 태그 앞에 페이지 하단에 배치하는 것이 좋습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Store {#section_A33E25DB5E67404A823BD9618665B773}

다음 태그를 사용하여 사용자가 현재 있는 스토어를 테스트하고 표시합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store/&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 스토어를 출력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>사용자가 스토어에 있는지 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>사용자가 <span class="codeph"> gsname </span> 매개 변수가 지정하는 스토어에 있는지 검색합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영역 {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area" [search="associated search"] [facet="associated facet"] [width="xx" height="yy"]&gt; </span> </p> </td> 
   <td colname="col2"> <p>영역 태그의 모든 컨텐츠를 둘러싸서 영역 밖으로 영역을 만들 수 있습니다. 이를 통해 필요에 따라 비즈니스 규칙을 사용하여 영역을 표시할 수 있습니다. 기본적으로 영역은 항상 표시됩니다. 선택 사항인 검색 및 패싯 매개 변수를 사용하여 해당 영역과 연관된 검색 또는 패싯을 표시할 수 있습니다. 이러한 기능을 사용하면 영역이 숨겨져 있을 때 검색 또는 패싯을 건너뛰고 검색 시간 성능을 개선할 수 있습니다. 높이 및 너비 속성은 선택 사항이며 영역이 제거될 때 시각적 규칙 빌더에서 자리 표시자가 표시되는 방식을 구성하는 데 사용됩니다. </p> <p> 가능하면 영역 대신 <span class="codeph"> guided-if-facet[-not]-visible </span> 태그를 사용하십시오. 프레젠테이션 템플릿을 간소화할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 세트를 사용하면 영역이 현재 표시되어 있는 경우 테스트할 수 있습니다. 영역이 표시될 때만 표시하려는 컨텐츠가 페이지의 다른 곳에 있을 때 유용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 루프 표시기 {#section_387322CA0AA843A2ACF2795C328673E9}

이러한 루프 블록 중 하나에서 다음 루프 표시기를 사용할 수 있습니다.

* 안내 결과
* guided-facet-values
* guided-breadcrumb
* 안내 메뉴 항목
* 안내 페이지

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프의 첫 번째 반복일 때 적용됩니다. 첫 번째 결과나 첫 번째 페이지를 의미할 필요는 없지만 첫 번째 결과가 표시됩니다. 사이트 방문자가 페이지당 10인 결과 세트의 2페이지에 있는 경우 첫 번째 반복은 11입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프의 마지막 반복일 때 적용됩니다. 이는 반드시 마지막 결과나 마지막 페이지를 의미하지는 않지만 현재 컨텍스트(페이지)에 표시된 마지막 결과를 의미합니다. 사이트 방문자가 200개의 결과를 포함하는 결과 집합의 1페이지에 있지만 페이지당 10개의 결과만 있는 경우 마지막 반복은 결과 200이 아닌 10개의 결과가 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프의 홀수 반복일 때(짝수 반복 비교) 적용됩니다. 이것은 다양한 행 색상을 표시하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프의 짝수 반복일 때(홀수 반복 비교) 적용됩니다. 이것은 다양한 행 색상을 표시하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프 반복 단위인 경우 적용됩니다. 이것은 다양한 행 색상을 표시하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 이터레이션이 첫 번째 또는 마지막 이터레이션이 아닌 경우 두 항목 사이에 있는 텍스트를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 이터레이션이 첫 번째 또는 마지막 이터레이션인 경우 두 항목 사이에 있는 텍스트를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>루프의 각 반복에 대해 값이 증가되는 정수(0부터 시작)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>루프의 각 반복에 대해 값이 증가되는 정수(1부터 시작)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 기타 언어 {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

다음 태그를 사용하여 나만의 미니 패싯 작성과 같은 더 많은 고급 작업을 수행할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> &lt;guided-current-path [escape="html|url|js|json|0"] /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>사용되는 현재 경로를 제공합니다. 일반적으로 기존 검색에 새 매개 변수를 추가하는 링크를 만드는 데 사용됩니다. 기본적으로 경로는 URL 이스케이프됩니다. escape 매개 변수를 통해 사용할 이스케이프 모드를 지정할 수 있습니다. </p> <p>예: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>이 예에서 검색 처리 규칙은 lang을 사용하여 프랑스어 버전을 선택합니다. </p> <p>현재 경로에는 항상 하나 이상의 쿼리 매개 변수가 있습니다. 다른 쿼리 매개 변수가 없는 경우 q <span class="codeph"> =*로 설정되므로 더 많은 매개 변수를 쉽게 추가할 </span> 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> 기본 경로 </span> </p> </td> 
   <td colname="col2"> <p> basepath를 사용하여 링크를 만들려면 <span class="codeph"> href의 시작 부분에 </span> /를 사용하고 매개 변수에 <span class="codeph"> </span> 추가합니다. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> &lt;guided-query-param gsname="query_parameter" [escape="html|url"] /&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>URL에 있는 쿼리 매개 변수의 기존 값을 선택할 수 있도록 해줍니다. 매개 변수가 없으면 이 태그는 빈 문자열을 반환합니다. escape 옵션을 지정하지 않으면 반환된 문자열이 자동으로 HTML escape되는 경우 HTML 또는 URL escape를 지정할 수 있습니다. </p> <p>예: </p> <p> 

    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;q&amp;nbsp;/&amp;gt;nbsp;you&amp;nbsp;value&amp;nbsp;value&amp;nbsp;lt
    ;guided-query-param&amp;nbsp;nbsp;guided-query-param&amp;nbsp;nbsp;;get;
    
    gives&amp;nbsp;you&amp;nbsp;the&amp;nbsp;value&amp;nbsp;en
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;
    
    gsname;nbsp&amp;nbsp;you&amp;nbsp&amp;nbsp&amp;nbsp;string
    &amp;nbsp;nbsp;
    
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>안내 검색에는 탐색 표시 컨트롤에 사용되는 쿼리 번호의 개념이 있습니다. <span class="codeph"> guided-query-param-name </span> 을 사용하면 안내 검색이 올바른 쿼리 번호를 계산하는 프레젠테이션 템플릿의 링크의 일부로 매개 변수를 정의할 수 있습니다. gsname <span class="codeph"> </span> 에는 "x"가 있으며, 검색 안내 기능이 올바른 번호로 바뀝니다. 오프셋 값은 0 - 15일 수 있습니다. 여기서 0은 사용 가능한 다음 쿼리 번호가 사용되었음을 나타냅니다. 1은 1을 추가하려는 경우등을 나타냅니다. </p> <p>안내 <span class="codeph"> 현재 경로와 함께 </span>미니 패싯 링크를 만들거나 추가 드릴 다운 수준을 허용할 수 있습니다. </p> <p>예: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> 다른 템플릿 파일을 포함할 수 있습니다. 이 기능은 하위 템플릿을 모듈로 사용하여 여러 템플릿을 만들 수 있음을 의미합니다. </p> <p>다음 예제에서는 탐색 표시 <span class="filepath"> 및 </span> 패싯 <span class="filepath"> </span> 파일이 포함됩니다. </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>동적 포함은 지원되지 않습니다. 즉, gsfile은 <span class="codeph"> 변수일 </span> 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> &lt;guided-search-time&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 검색에 걸린 시간을 식별합니다. 반환된 검색 시간 값은 ms로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> 검색 결과 페이지를 작성하는 데 사용되는 코어 검색 수를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>핵심 검색 수가 1보다 큰지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프의 짝수 반복일 때(홀수 반복 비교) 적용됩니다. 이것은 다양한 행 색상을 표시하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>이 조건은 현재 반복이 루프 반복 단위인 경우 적용됩니다. 이것은 다양한 행 색상을 표시하는 데 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 이터레이션이 첫 번째 또는 마지막 이터레이션이 아닌 경우 두 항목 사이에 있는 텍스트를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>현재 이터레이션이 첫 번째 또는 마지막 이터레이션인 경우 두 항목 사이에 있는 텍스트를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>초기 검색에 있는지 여부를 확인할 수 있습니다(쿼리는 검색 상자의 검색 결과). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>템플릿에서 이 태그를 사용하여 검색 양식의 동작을 하드코딩하지 않도록 저장할 수 있습니다. 스테이지 또는 라이브 환경에 있는 경우를 감지하여 그에 따라 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합을 사용하면 검색 경로에서 정의된 CGI 매개 변수를 테스트할 수 있습니다. 매개 변수가 정의된 경우에만 매개 변수의 값을 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number [gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>템플릿을 구동하는 검색 안내 엔진은 엔진이 생성하는 새 링크가 생성되어 사용 가능한 다음 쿼리 번호를 사용하는 부동 쿼리 번호라는 개념을 가지고 있습니다. 이 태그를 사용하면 다음 쿼리 번호나 오프셋을 선택하여 결과 세트로 드릴다운하는 사용자 지정 링크를 만들 수 있습니다. 오프셋을 사용하면 다음 쿼리 번호로 오프셋할 수 있습니다. 예를 들어 하나의 패싯을 선택한 경우 다음 쿼리 번호는 2이고 오프셋이 1이면 반환되는 쿼리 번호는 3입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>처리 규칙이 정의하는 사용자 지정 변수의 기존 값을 선택할 수 있도록 해줍니다. escape 옵션을 지정하지 않으면 반환된 문자열이 자동으로 HTML로 이스케이프됩니다. html, <span class="codeph"> url </span>또는 Flash Player <span class="codeph"> 0 </span><span class="codeph"> </span><span class="codeph"> </span>을 지정할 수 있습니다. 처리 규칙을 사용하여 들어오는 CGI 매개 변수를 사용자 지정 변수에 복사한 다음 이스케이프된 설정을 none 또는 js로 설정하여 템플릿에 해당 변수를 표시하거나 사용하는 경우 검색에서 XSS 취약점을 만들 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 변수가 처리 규칙(쿼리 정리, 사전 검색 처리 및 사후 검색 처리)에 정의되어 있는지 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>전송 템플릿에 정의된 일반 필드의 내용을 표시할 수 있습니다. escape 옵션을 지정하지 않으면 반환된 문자열이 해당 필드에 대해 전송 템플릿에서 지정한 형식으로 인코딩됩니다. 이스케이프 옵션을 지정하면 전송 템플릿에서처럼 필드를 인코딩하는 형식 위에 적용됩니다. html, <span class="codeph"> url, js </span>, <span class="codeph"> js, verizing, verizing </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>0 중 하나를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>전송 템플릿에 정의된 대로 일반 필드의 내용이 있는지 여부를 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name" [escape="html|url|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>쿠키를 사용할 수 있다고 가정할 때 쿠키의 값을 선택할 수 있습니다. escape 옵션을 지정하지 않으면 반환된 문자열이 자동으로 HTML이 되는 경우 html, <span class="codeph"> url, JSON, JSON </span>Escape 또는 <span class="codeph"> 0 중 하나를 지정할 수 </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>쿠키가 있는 경우 테스트를 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area" [escape="html|url|js|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>지정된 영역에 대한 배너를 출력합니다. 시각적 규칙 빌더에서 너비와 높이 속성(선택 사항)을 사용하여 의미 있는 자리 표시자를 표시하여 사용자가 배너를 선택할 수 있도록 합니다. 기본적으로 배너는 이스케이프되지 않습니다. 대신 프레젠테이션 템플릿에 HTML을 삽입해야 합니다. 그러나 JSON 템플릿을 빌드하는 경우 js escape 옵션을 사용하는 것이 좋습니다. </p> <p>예: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>배너 영역이 설정된 경우 테스트를 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>시뮬레이터 또는 시각적 규칙 빌더에서 검색을 볼 때를 감지할 수 있습니다. 일반적으로 추가 디버그 정보를 표시하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Adobe Target <span class="keyword"> 캠페인을 참조하는 비즈니스 규칙이 있는지 감지할 </span> 수 있습니다. Adobe Target과의 통합의 일부로 일반적으로 <span class="keyword"> Target </span> 서버가 <span class="keyword"> 필요하지 않을 때 Target </span> 서버를 히트하지 않도록 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect/&gt; </span> </p> </td> 
   <td colname="col2"> <p>기본적으로 리디렉션은 자동으로 수행됩니다. 그러나 웹 애플리케이션에 XML 또는 JSON 응답을 반환하도록 사이트 검색/머천다이징을 구성한 경우 웹 애플리케이션의 302/301 응답을 분석하거나 결과 세트의 일부로 사용자에게 전달된 리디렉션을 선택할 수 있습니다. 결과 집합의 일부로 리디렉션을 전달하는 경우 이 태그를 템플릿에서 사용하여 리디렉션 위치를 출력할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>결과 세트에서 리디렉션을 반환하도록 사이트 검색/머천다이징을 구성한 경우 이 태그 집합을 사용하여 출력으로의 리디렉션이 있는지 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt/&gt; &lt;guided-gt/&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 집합을 사용하면 HTML 속성 내에 안내 템플릿 태그를 포함할 수 있습니다. </p> <p>예: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 전송 템플릿 태그 {#reference_227D199F5A7248049BE1D405C0584751}

전송 템플릿은 백엔드 검색에서 검색 안내 프레젠테이션 레이어로 데이터를 전달하는 XML 템플릿입니다.

<!-- 

r_transport_template_tags.xml

 -->

프레젠테이션 레이어에서 여러 검색 결과를 보여주는 단일 프레젠테이션 템플릿을 사용할 수 있습니다. 각 검색은 동일한 전송 템플릿 또는 사용자 지정 전송 템플릿을 사용하여 데이터를 프레젠테이션 레이어로 전달할 수 있습니다.

전송 템플릿은 프레젠테이션 레이어로 데이터를 전달하는 데만 사용되므로 검색 결과 표시와 관련된 HTML이 없습니다. 전송 템플릿은 전송 템플릿 XML 태그를 사용하여 패싯, 탐색 표시 및 메뉴와 같은 검색 구성 요소를 채우는 검색 결과를 전달합니다. 이러한 태그 내에서 표준 검색 템플릿 태그는 실제 값을 표시하는 데 사용됩니다.

프레젠테이션 [또는 전송 템플릿](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)편집을 참조하십시오.

템플릿 [태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)검색을 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>전송 템플릿 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>프레젠테이션 레이어에서 전송 템플릿에서 구문 분석되는 내용을 검색하는 데 사용하는 루트 XML 태그입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;일반&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>결과 집합을 기반으로 요약 데이터를 제공하는 태그 서라운드 검색 템플릿 태그 일반적으로 이러한 태그에는 총 결과 수, 낮은 결과 및 가장 높은 결과에 대한 검색 태그가 포함됩니다. 다음 예와 같이 <span class="codeph"> 일반 필드 </span> 태그로 원하는 추가 글로벌 필드를 정의할 수 있습니다. </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>태그가 검색 결과에 래핑되므로 안내 검색이 검색 위치를 알 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>다음 예와 같이 검색 결과 하나에 대한 컨텐츠가 시작되고 끝나는 위치를 검색 결과 주위에 태그가 래핑됩니다. </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tabename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>다중 값 목록의 각 항목을 반복하여 하나의 결과를 얻을 수 있습니다. 결과 내에서만 이 태그를 사용하십시오. 다음 예와 같이 결과 필드에 속하는 속성을 반복할 수 있도록 하기 위해 사용됩니다. </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;패싯&gt;&lt;/패싯&gt; </span> </p> </td> 
   <td colname="col2"> <p>패싯을 채우는 결과를 전달합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> 패싯을 동적 패싯과 패싯 레일의 멤버로 지정할 수 있습니다. 그러나 이러한 방식은 관련 프레젠테이션 템플릿 태그와 관련하여 독립적입니다. </p> <p>즉, 동적 패싯 루핑 컨텍스트 내 또는 그 반대로 패싯 레일 반복 컨텍스트의 중첩은 허용되지 않습니다. </p> <p>동적 패싯과 레일 모두 있는 패싯의 경우 지정된 검색에 대해 반환되는 동적 패싯만 패싯 레일 반복 컨텍스트 내에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> 각 패싯에는 이름 매개 변수가 패싯 이름과 일치하는 자체 패싯 태그가 있습니다. 검색 태그는 다음 예와 같이 패싯 값에 대한 패싯 태그 내에 사용됩니다. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> 분리된 패싯을 사용하는 계정은 다이내믹 태그 및 표시 이름 태그를 사용할 수 있습니다. 이러한 태그 모두 비즈니스 규칙을 만드는 동안 단면화 및 실제 단면화 간의 매핑을 용이하게 하는 데 도움이 됩니다. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>separator <span class="codeph"> </span> 속성을 사용하면 목록에 대한 search-display-field 데이터를 출력할 때 사용되는 구분 기호를 변경할 수 있습니다. 기본값은 쉼표입니다. </p> <p>일반적으로 사용하는 구분 기호는 필드 컨텐츠에 쉽게 표시되지 않는 것이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;제안&gt;&lt;/제안&gt; </span> </p> </td> 
   <td colname="col2"> <p> 추천 단어 제안 태그를 태그로 래핑하여 검색 안내 기능에서 제안이 포함된 XML 노드를 인식할 수 있습니다. </p> <p><a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">다음을 찾으려고 하셨습니까? 정보</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;추천&gt;&lt;/제안&gt; </span> </p> </td> 
   <td colname="col2"> <p>다음 예와 같이 각 추천 목록을 태그로 래핑합니다. </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p><a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">다음을 찾으려고 하셨습니까? 정보</a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 태그 검색 {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

검색 템플릿은 사이트 검색/머천다이징에서 정의하는 템플릿 태그를 포함하는 HTML 파일입니다. 이러한 태그는 검색 결과의 서식 지정을 나타냅니다. 다음 참조에는 각 검색 템플릿 태그 및 해당 속성에 대한 간단한 설명이 포함되어 있습니다.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>전송 템플릿 파일(.tpl)에는 검색 템플릿 태그만 사용합니다.

다음 검색 템플릿 태그 그룹 및 참조 자료 중에서 선택할 수 있습니다.

결과 루프 내에서만 유효한 태그에는 다음이 포함됩니다.

* [결과 루프 태그 정보](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [결과 루프 문자열 태그](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [결과 루프 조건부 태그](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [결과 루프 앵커 링크 태그](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [루프 위치 조건부 태그](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

템플릿 전체에서 유효한 태그에는 다음이 포함됩니다.

* [필드 값 목록 태그](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [필드 값 목록 루프 태그](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [태그 제안](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [템플릿 문자열 태그](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [템플릿 앵커 링크 태그](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [템플릿 조건부 태그](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [템플릿 양식 제어 태그](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

템플릿 참조 항목 검색

* [날짜 형식 문자열](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [언어 식별자](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [컨텐츠 유형 HTTP 헤더 지정](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [HTML 템플릿에서 문자 집합 지정](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [XML 템플릿에서 문자 집합 지정](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [다른 검색 템플릿 포함](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## 결과 루프 태그 정보 {#section_D4DC7B4560144663972E8DBC3369C629}

results 루프 태그는 템플릿 시스템의 워크플로우입니다. 검색 중에 태그가 발견되면 HTML이 반복되고 시작 및 종료 결과 루프 태그 사이에 다른 태그가 추가되어 다른 태그를 검색 결과로 바꿉니다.

`<search-results> ... </search-results>`

결과 루프 태그는 검색 결과를 표시하는 HTML 주위에 있습니다. 태그 사이의 HTML은 모든 결과에 대해 반복되며 페이지에 표시됩니다.

다음 태그는 결과 루프 내에서만 유효합니다.

* [결과 루프 문자열 태그](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [결과 루프 조건부 태그](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [결과 루프 앵커 링크 태그](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [루프 위치 조건부 태그](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## 결과 루프 문자열 태그 {#section_80D68334E8D04A33937A6E58ABAAA320}

다음 태그는 문자열을 반환합니다.

결과 [루프 태그](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)정보를 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 숫자 인덱스를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 페이지 제목을 반환합니다. 선택적 length 속성은 기본적으로 80자로 표시된 문자열의 길이를 제한하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>페이지 상단에서 시작하는 본문 텍스트를 반환합니다. 관련 용어는 굵게 표시됩니다. 선택적 length 속성은 기본적으로 80자로 표시된 문자열의 길이를 제한하는 데 사용됩니다. 인코딩 속성은 선택 사항이며 HTML 인코딩(기본값), Javascript 인코딩, Perl 인코딩 또는 없음을 사용하여 출력 문자를 인코딩할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 현재 결과의 설명을 반환합니다. 메타 설명 태그가 존재하고 content 속성이 비어 있지 않으면 해당 텍스트가 표시됩니다. 그렇지 않으면 페이지의 본문 텍스트 시작 부분이 표시됩니다. 선택적 length 속성은 기본적으로 80자로 표시된 문자열의 길이를 제한하는 데 사용됩니다. </p> <p>선택적 <span class="codeph"> 인코딩 </span> 속성은 결과 페이지에서 출력하기 위해 출력이 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. 인코딩의 기본값은 <span class="codeph"> html </span> <span class="codeph"> </span>입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>0 - 100인 현재 결과의 점수를 반환합니다. [옵션] &gt; [메타데이터] &gt; [정의] <span class="uicontrol"> 아래에 등급 필드를 정의한 </span> 경우 등급 속성 동적( <span class="uicontrol"> </span> <span class="uicontrol"> </span><span class="codeph"> </span>&lt;search-score="dynamic")을 설정하여 동적 페이지 등급을 표시할 수 있습니다. 등급 속성을 정적( <span class="codeph"> &lt;search-score rank="static"&gt;)으로 설정하여 정적 페이지 등급을 표시할 수 </span>있습니다. 선택적 정밀도 속성을 사용하여 표시할 소수 자릿수를 지정할 수 있습니다. 기본값은 정수 점수를 표시하는 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 날짜를 반환합니다. 현재 결과와 연결된 날짜가 없는 경우 선택적 "없음" 텍스트 값이 표시됩니다. 선택 사항인 "없음" 값을 지정하지 않으면 현재 결과와 연결된 날짜가 없는 경우 "날짜 없음" 텍스트가 표시됩니다. </p> <p>"date-format" 특성은 "%A, %B %d, %Y"(2016년 7월 25일 월요일)와 같은 UNIX 스타일 날짜 형식 문자열을 가져옵니다. "gmt"의 기본값은 "yes"로 설정되며 날짜 문자열의 시간 부분을 GMT("yes")로 출력할지 또는 계정의 표준 시간대("no")로 출력할지를 제어합니다. </p> <p>"language" 속성은 출력 날짜 문자열의 언어 및 로케일 규칙을 제어합니다. "0"(기본값)은 "계정 언어 사용"을 의미합니다. "2"는 "문서 언어 사용"을 의미합니다. "language" 값 "1"은 나중에 사용하도록 예약되어 있습니다. 기타 모든 "언어" 값은 특정 언어 식별자로 해석됩니다. 예를 들어 "en_US"는 "영어(미국)"를 의미합니다. </p> <p>선택적 length 속성은 기본적으로 80자로 표시된 문자열의 길이를 제한하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 크기(바이트)를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 URL을 반환합니다. </p> <p>선택적 <span class="codeph"> length </span> 속성을 사용하여 표시된 문자열의 길이를 제한(기본값: 제한 없음)합니다. </p> <p>인코딩 <span class="codeph"> </span> 속성은 선택 사항이며 HTML 인코딩, JavaScript 인코딩, Perl 인코딩 또는 없음을 사용하여 출력 문자를 인코딩할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 결과의 URL의 물음표를 포함하여 경로 및 쿼리 부분을 반환합니다. </p> <p>선택적 <span class="codeph"> length </span> 속성을 사용하여 표시된 문자열의 길이를 제한(기본값: 제한 없음)합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>검색어에 대한 다음 컨텍스트 행을 반환합니다. 관련 용어는 굵게 표시됩니다. 현재 결과에 대해 두 개 이상의 컨텍스트 라인을 표시하려면 이 태그를 반복적으로 호출합니다. </p> <p>선택적 <span class="codeph"> length </span> 속성을 사용하여 표시된 문자열의 길이를 80자로 제한합니다. 이 태그를 <span class="codeph"> &lt;search-if-context&gt; </span> 또는 <span class="codeph"> &lt;search-if-any-context&gt; </span> 길이 속성이 포함된 태그 세트로 둘러싸면 length <span class="codeph"> </span> 속성이 무시됩니다. </p> <p>인코딩 <span class="codeph"> </span> 속성은 선택 사항이며 HTML 인코딩(기본값), Javascript 인코딩, Perl 인코딩 또는 없음을 사용하여 출력 문자를 인코딩할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" 쉼표="yes/no" units="miles/km" separator="|" </span> </p> </td> 
   <td colname="col2"> <p>이 고급 태그는 현재 결과에 대해 이름 <span class="uicontrol"> </span> <span class="uicontrol"> </span> <span class="codeph"> </span> 속성에 지정된 메타데이터 필드(url, 제목, 설명, 키, 대상, 본문, 대체, 날짜, 차트, 언어 또는 옵션 &gt; 메타데이터 &gt; 정의 아래에 정의된 필드)의 컨텐츠를 표시합니다. 예: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>검색 결과에 대한 페이지 제목을 출력합니다. 선택 사항 <span class="codeph"> 없음 </span> 속성이 지정된 경우 해당 값은 필드와 연결된 컨텐츠가 없는 경우에만 결과 페이지에 표시됩니다. </p> <p>날짜, <span class="codeph"> gmt </span>및 <span class="codeph"> 언어 </span> 속성은 지정된 필드의 컨텐츠 유형이 <span class="codeph"> </span> <span class="codeph"> </span>날짜-인 경우에만 관련이 있습니다. </p> <p>date- <span class="codeph"> format </span> 속성은 <span class="codeph"> %A, %B %d, %Y(2016년 7월 25일 월요일)와 같은 UNIX 스타일 날짜 형식 문자열을 </span> 사용합니다. <span class="codeph"> gmt </span> 는 기본적으로 <span class="codeph"> yes </span> 로 설정되며 날짜 문자열의 시간 부분이 GMT( <span class="codeph"> 예 </span>) 또는 계정의 표준 시간대( <span class="codeph"> 아니요 </span>)로 출력되는지 여부를 제어합니다. </p> <p>날짜 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 형식 문자열을</a>참조하십시오. </p> <p>언어 <span class="codeph"> </span> 속성은 출력 날짜 문자열의 언어 및 로케일 규칙을 제어합니다. <span class="codeph"> 0 </span> (기본값)은 "계정 언어 사용"을 의미합니다. <span class="codeph"> 2 </span> 는 "문서 언어 사용"을 의미합니다. 언어 <span class="codeph"> 값 </span> 1 <span class="codeph"> </span> 은 나중에 사용하도록 예약되어 있습니다.) 다른 모든 <span class="codeph"> 언어 </span> 값은 특정 언어 식별자로 해석됩니다. 예를 들어 <span class="codeph"> en_US는 "영어(미국)" </span> 를 의미합니다. </p> <p>언어 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 식별자를</a>참조하십시오. </p> <p>선택적 <span class="codeph"> 길이 </span> 속성은 기본적으로 80자로 표시된 문자열의 길이를 제한하는 데 사용됩니다. </p> <p>선택적 <span class="codeph"> 인코딩 </span> 속성은 결과 페이지에서 출력하기 위해 출력이 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. 인코딩의 기본값은 <span class="codeph"> html </span> <span class="codeph"> </span>입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. </p> <p>선택적 <span class="codeph"> 따옴표 </span> 속성은 개별 항목 출력을 큰따옴표로 둘러싸는지(또는 encoding=perl인 경우 작은따옴표)를 제어합니다 <span class="codeph"> </span>. 따옴표의 기본값은 no <span class="codeph"> 입니다 </span> <span class="codeph"> </span>. </p> <p>선택적 <span class="codeph"> 쉼표 </span> 속성은 개별 항목 출력을 쉼표로 구분할지 여부를 제어합니다. 기본값은 <span class="codeph"> yes </span> 입니다 <span class="codeph"> </span>. 쉼표 <span class="codeph"> </span> 속성은 목록 형식이 아닌 필드에 대해 무시됩니다. </p> <p>옵션 <span class="codeph"> units </span> 속성은 근접 검색 출력 필드에 적용되는 거리 단위를 제어합니다. 단위의 기본값은 주어진 근접 검색 출력 필드와 관련된 위치 유형 필드의 "기본 단위" 설정에서 <span class="codeph"> </span> 결정됩니다. </p> <p>근접 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 검색</a>정보를 참조하십시오. </p> <p>선택적 <span class="codeph"> separator </span> 속성은 목록 유형 필드의 출력 값 사이에 삽입되는 단일 문자 또는 구분 기호를 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt;...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 결과에 대한 메타데이터 필드 값(url, 제목, 설명, 키, 대상, 본문, 대체, 날짜, 문자, 언어 또는 옵션 &gt; 메타데이터 <span class="uicontrol"> &gt; </span> 정의 아래에 정의된 필드)을 열거하는 루프를 만듭니다 <span class="uicontrol"> </span> <span class="uicontrol"> </span>. 이 태그를 다른 <span class="codeph"> &lt;search-display-field-values&gt; </span> 태그 내부에 중첩하지 마십시오. name <span class="codeph"> </span> 속성은 열거할 값이 들어 있는 필드의 이름을 지정합니다. 이 태그는 [옵션] &gt; [메타데이터] &gt; [정의]에서 [목록 <span class="uicontrol"> 허용] </span> 속성을 선택한 <span class="uicontrol"> 필드에 가장 유용합니다(옵션 </span> &gt; <span class="uicontrol"> [메타데이터] </span> &gt; <span class="uicontrol"> [정의] </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 <span class="uicontrol"> &lt;search-display-field-values&gt; 루프에 대한 메타데이터 필드 값(url, title, desc, keys, target, body, alt, date, charset, and fields thelds these definitions under </span> [ <span class="uicontrol"> ] &gt; </span> 메타데이터 <span class="uicontrol"> &gt; </span>정의] <span class="codeph"> </span> )을 출력합니다. 이 태그는 <span class="codeph"> &lt;search-display-field-values&gt; </span> 루프 내에서만 유효합니다. 이 <span class="codeph"> 속성, </span>gmt <span class="codeph"> 및 </span> 언어 <span class="codeph"> 속성은 바깥쪽 &lt;search-display-field-values&gt;에 지정된 필드 이름의 컨텐트 유형이 </span> <span class="codeph"> </span> <span class="codeph"> </span>게시 날짜인 경우에만 관련이 있습니다. 이 <span class="codeph"></span> 특성은 <span class="codeph"> "%A, </span><span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span>%B %Date-Date Date Date 형식 문자열("월요일, 2016년 7월 25일")을 사용합니다. gmt <span class="codeph"> 속성은 기본적으로 yes로 설정되며 날짜 문자열의 시간 부분이 GMT( </span> 예) 또는 계정의 표준 시간대( <span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span>지연 없음)로 출력되는지 여부를 제어합니다. </p> <p>언어 <span class="codeph"> </span> 속성은 출력 날짜 문자열의 언어 및 로케일 규칙을 제어합니다. <span class="codeph"> 0 </span> (기본값)은 "계정 언어 사용"을 의미합니다. 다른 모든 <span class="codeph"> 언어 </span> 값은 특정 언어 식별자로 해석됩니다. 예를 들어 <span class="codeph"> en_US는 "영어(미국)" </span> 를 의미합니다. </p> <p>선택적 <span class="codeph"> 인코딩 </span> 속성은 결과 페이지에서 출력하기 위해 출력이 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. 인코딩의 기본값은 <span class="codeph"> html </span> <span class="codeph"> </span>입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이름 속성으로 지정된 메타데이터 필드(url, title, desc, keys, target, body, alt, date, charset, 언어 또는 옵션 &gt; 메타데이터 <span class="uicontrol"> &gt; </span> 정의 아래에 정의된 필드)에 대한 현재 결과의 총 값 수를 출력합니다 <span class="uicontrol"> </span> <span class="uicontrol"> </span>. 이 태그는 결과 루프의 어느 위치에나 나타날 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 <span class="codeph"> &lt;search-display-field-values&gt; </span> 루프 반복에 대한 서수 카운터(1, 2, 3 등)를 출력합니다. 이 태그는 <span class="codeph"> &lt;search-display-field-values&gt; </span> 루프 내에서만 유효합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 검색에 대해 반환되는 모든 동적 패싯 필드에 대한 루핑 컨텍스트를 시작합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 루프 반복에 대한 현재 동적 패싯 필드의 이름을 출력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>결과 위치에 영향을 준 결과 기반 작업과 같이 현재 결과의 배치와 관련된 정보를 출력합니다. </p> <p>이 태그의 출력 형식은 다음 예와 같이 JSON입니다. </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>인코딩 <span class="codeph"> </span> 속성은 선택 사항입니다.기본값은 <span class="codeph"> html </span>입니다. </p> <p> <p>참고: 이 태그는 <span class="codeph"> </span> sp_trace=1이 핵심 검색 쿼리 매개 변수와 함께 지정된 경우에만 출력됩니다. </p> </p> <p>백 엔드 검색 CGI 매개 변수에 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>있는 표에서 48행을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 루프 조건부 태그 {#section_35C367969E384A06A9865E388F1F9360}

다음 태그는 두 태그 사이의 HTML을 조건부로 포함합니다.

결과 [루프 태그](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)정보를 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt;..&lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt;...&lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>다음 호출에서 <span class="codeph"> &lt;search-title&gt;을(를) 호출하면 문서 제목에서 텍스트가 반환되거나 반환되지 않는 경우 이러한 태그에는 그 사이에 HTML이 포함됩니다 </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; .../search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt;...&lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이러한 태그에는 다음 호출에서 <span class="codeph"> &lt;search-description&gt;을 </span> 호출하면 문서 설명에서 텍스트가 반환되거나 반환되지 않는 경우 태그 사이에 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt;...&lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt;..&lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 <span class="codeph"> &lt;search-bodytext&gt;을(를) 다음에 호출하면 문서 본문에서 텍스트를 반환하거나 반환하지 않을 경우 그 사이에 HTML이 포함됩니다 </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ...&lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt;...&lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 <span class="codeph"> &lt;search-context&gt;에 대한 다음 호출이 비어 있지 않은 컨텍스트 문자열을 반환(또는 반환하지 않음) </span> 하는 경우 그 사이에 HTML이 포함됩니다. length 속성은 <span class="codeph"> 동봉된 &lt;search-context&gt; </span> 태그의 length 속성을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; .../search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt;...&lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 결과와 연결된 컨텍스트 문자열이 있거나 없는 경우 태그 사이에 HTML이 포함됩니다. length 속성은 <span class="codeph"> 동봉된 &lt;search-context&gt; </span> 태그의 length 속성을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt;..&lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX upper=yy rank="dynamic/static"&gt;...&lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 결과의 점수가 XX와 YY 사이에 있거나 HTML이 아닌 경우 그 사이에 있는 HTML이 포함됩니다. 글머리 기호나 그래픽을 추가하여 결과의 연관성을 보여주는 데 유용합니다. [옵션] &gt; [메타데이터] &gt; [정의]에서 등급 유형 필드를 정의했다면, <span class="uicontrol"> 등급 속성을 동적으로 </span> ( <span class="uicontrol"> &lt;search-if-score="dynamic" lower=XX upper=YY&gt;) </span> <span class="uicontrol"> </span><span class="codeph"> </span>으로 설정하여 동적 페이지 등급을 확인할 수 있습니다. 등급 속성을 정적( <span class="codeph"> &lt;search-if-score rank="static" lower=XX upper=YY&gt;)으로 설정하여 정적 페이지 등급을 확인할 수 </span>있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt;...&lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt;...&lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 고급 태그에는 "name" 속성에 지정된 필드에 컨텐츠가 있는지 여부에 따라 그 사이에 HTML이 포함됩니다. 선택적 "value" 속성이 지정된 경우, 태그에는 주어진 값이 현재 결과의 필드 값과 일치하는지(또는 일치하지 않음) 여부를 기준으로 그 사이에 HTML이 포함됩니다. 이러한 태그는 결과 루프( <span class="codeph"> &lt;search-results&gt; </span> 및 <span class="codeph"> &lt;/search-results&gt; </span> 태그 사이)에서만 작동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 루프 앵커 링크 태그 {#section_C5FAEF520E9E42ADAD1F90651922AA02}

결과 [루프 태그](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)정보를 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt; ...&lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 쌍은 태그 사이의 HTML 주위에 앵커 링크를 만듭니다. 링크를 클릭하면 결과 페이지가 표시됩니다. 선택적 target 속성은 프레임 지원 브라우저가 결과 페이지를 표시할 명명된 창을 지정합니다. </p> <p>hbx-enable 속성을 "yes"로 설정하여 HBX를 통해 사용할 수 있는 분석을 활용합니다. hbox-linkid-name을 추적할 메타 데이터 필드의 이름으로 설정합니다. 예를 들어 SKU 번호로 검색 결과를 추적하려면 hbx-linkid-name을 SKU 정보가 포함된 메타 데이터 필드의 이름으로 설정합니다. </p> <p>현재 날짜 유형 필드는 지원되지 않습니다. hbox-linkid-name의 값은 생성된 앵커의 링크 ID에 추가됩니다. hbx-linkid-none 속성의 값은 명명된 메타 데이터 필드가 비어 있을 때마다 링크 ID에 추가됩니다. hbox-linkid-length 값은 메타 태그에서 가져오고 표시되는 문자 수를 제한합니다. 기본 문자 수는 12자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt;...&lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그 쌍은 <span class="codeph"> &lt;search-link&gt; 와 유사합니다...&lt;/search-link&gt; </span> 태그. 생성된 앵커 링크를 클릭하면 결과 페이지가 표시되지만 결과 앞의 가장 가까운 앵커 태그로 페이지가 스크롤됩니다. PDF 링크의 경우 Acrobat 뷰어에 결과가 포함된 페이지가 표시됩니다. 선택적 target 속성은 프레임 지원 브라우저가 결과 페이지를 표시할 명명된 창을 지정합니다. </p> <p>hbx-enable 속성을 "yes"로 설정하여 HBX를 통해 사용할 수 있는 분석을 활용합니다. hbox-linkid-name을 추적할 메타 데이터 필드의 이름으로 설정합니다. 예를 들어 SKU 번호로 검색 결과를 추적하려면 hbx-linkid-name을 SKU 정보가 포함된 메타 데이터 필드의 이름으로 설정합니다. </p> <p>현재 날짜 유형 필드는 지원되지 않습니다. hbox-linkid-name의 값은 생성된 앵커의 링크 ID에 추가됩니다. hbx-linkid-none 속성의 값은 명명된 메타 데이터 필드가 비어 있을 때마다 링크 ID에 추가됩니다. hbox-linkid-length 값은 메타 태그에서 가져오고 표시되는 문자 수를 제한합니다. 기본 문자 수는 12자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt;...&lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt;...&lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>값 속성이 결과에 대한 URL의 끝과 일치하는 확장을 지정하는 경우 이러한 태그에는 그 사이에 HTML이 포함됩니다. 이 태그는 링크 확장명을 기반으로 검색 결과에 그래픽을 포함할 때 유용합니다. value 속성은 다음과 같이 하나 이상의 확장(공백으로 구분)의 목록입니다.VALUE=".pdf" 또는 VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## 루프 위치 조건부 태그 {#section_E0C29DDA09E043C9A396F36334F05EBB}

다음 태그에는 두 태그 사이의 텍스트가 조건부로 포함됩니다. &quot;반복&quot; 태그 내에만 표시될 수 있습니다.&lt; `search-results>` 및 `<search-field-values>`. 결과 집합 내에서 현재 결과의 위치를 테스트하는 데 사용됩니다.

결과 [루프 태그](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)정보를 참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt;...&lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt;...&lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 결과가 페이지의 첫 번째 결과( <span class="codeph"> &lt;search-results&gt; 내에서 사용될 때) </span>또는 첫 번째 필드 값( <span class="codeph"> &lt;search-field-values&gt; 내에서 사용될 때)인 경우 두 필드 사이의 텍스트가 포함됩니다 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt;...&lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt;...&lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 결과가 페이지의 마지막 결과( <span class="codeph"> &lt;search-results&gt; 내에서 사용될 때) </span>또는 마지막 필드 값( <span class="codeph"> &lt;search-field-values&gt; 내에서 사용될 때)인 경우 그 사이에 있는 텍스트가 포함됩니다 </span>. 이 태그는 결과 사이에 구분 기호를 삽입하는 데 사용할 수 있습니다. 예를 들어 결과 사이에 <span class="codeph"> &lt;hr&gt; </span> 태그가 삽입됩니다. </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt;...&lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt;...&lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그에는 현재 결과가 페이지의 첫 번째 또는 마지막 결과가 아닌 경우( <span class="codeph"> &lt;search-results&gt; 내에서 사용될 경우) </span>또는 첫 번째 또는 마지막 필드 값이 아닌 경우(&lt;search-field-values&gt; 내에서 사용될 때) <span class="codeph"> </span>태그 사이의 텍스트가 포함됩니다. 태그가 아닌 버전에서는 결과가 첫 번째 또는 마지막 중 어느 것인지 테스트합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt;..&lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt;...&lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 결과가 페이지의 대체 결과이거나 그렇지 않은 경우(&lt;search-results&gt; 내에서 사용될 경우) 또는 대체 필드 값(&lt;search-field-values&gt; 내에서 사용될 때)이 들어 <span class="codeph"> 있습니다 </span><span class="codeph"> </span>. "대체" 결과는 페이지에서 두 번째, 네 번째, 여섯 번째 등의 결과입니다. 이 예는 다른 클래스를 대체 테이블 행에 적용합니다. &lt;search-lt&gt; 및 <span class="codeph"> &lt;search-gt&gt;를 </span> 사용하여 <span class="codeph"> &lt;search-if-alt 태그가 </span> &lt;tr&gt; 태그 안에 "inside" <span class="codeph"> 가 되도록 </span> <span class="codeph"> </span> 하십시오. </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt;...&lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt;...&lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 결과가 짝수 결과이거나 아닐 경우( <span class="codeph"> &lt;search-results&gt; 내에서 사용될 경우) 또는 짝수 필드 값( </span>&lt;search-field-values&gt; 내에서 사용할 경우) <span class="codeph"> ( </span>)이 포함됩니다. 검색 결과의 <span class="codeph"> &lt;search-index&gt; </span> 값이 짝수이면 검색 결과에 번호가 지정됩니다. 즉, 전체 결과 세트 내의 위치가 짝인 경우 전체 결과 집합 내에서가 아니라 <span class="codeph"> &lt;search-if-alt&gt; </span> 페이지에서 결과 위치를 테스트하는 것과 다를 수 있습니다. 다음 두 표는 차이를 보여 줍니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

### 첫 페이지, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>색인 </p> </th> 
   <th colname="col2" class="entry"> <p>결과 </p> </th> 
   <th colname="col3" class="entry"> <p>심지어? </p> </th> 
   <th colname="col4" class="entry"> <p>대체? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>첫 번째 결과 </p> </td> 
   <td colname="col3"> <p>아니오 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>두 번째 결과 </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>세 번째 결과 </p> </td> 
   <td colname="col3"> <p>아니오 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>네 번째 결과 </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>다섯 번째 결과 </p> </td> 
   <td colname="col3"> <p>아니오 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
 </tbody> 
</table>

### 이후 페이지, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>색인 </p> </th> 
   <th colname="col2" class="entry"> <p>결과 </p> </th> 
   <th colname="col3" class="entry"> <p>심지어? </p> </th> 
   <th colname="col4" class="entry"> <p>대체? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>10번째 결과 </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>11번째 결과 </p> </td> 
   <td colname="col3"> <p>아니오 </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>12차 결과 </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>13번째 결과 </p> </td> 
   <td colname="col3"> <p>아니오 </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>14번째 결과 </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>아니오 </p> </td> 
  </tr> 
 </tbody> 
</table>

마지막으로, 필드 값이 페이징되지 않기 때문에 `<search-if-even>` 항상 검색 필드 `<search-if-alt>` 값과 같습니다.

## 필드 값 목록 태그 {#section_D3298B5F976447DBA0032B883DCC91B1}

전체 검색 결과 집합의 다음 고급 태그 출력 필드 값 및 관련 데이터. 이러한 태그는 검색 쿼리의 CGI 매개 변수에 의해 지정된 `sp-sfvl-field` 필드에 대해서만 출력합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" 쉼표="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-string" gmt="yes/no" language="javassign="html/asby cript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 전체 결과 집합 내에서 고유한 필드 값, 값 수 또는 결과 카운트의 목록을 표시합니다. </p> <p>이 태그는 검색 쿼리에서 <span class="codeph"> sp_sfvl_field </span> CGI 매개 변수에 의해 지정된 필드에 대한 출력만 산출합니다. 선택적 "인용 부호" 속성은 개별 항목 출력을 큰따옴표(encoding=perl의 경우 작은따옴표)로 둘러싸는지 여부를 제어합니다. "quotes"의 기본값은 "yes"입니다. 선택적 "쉼표" 속성은 개별 항목 출력을 쉼표로 구분할지 여부를 제어합니다. "쉼표"의 기본값은 "yes"입니다. 선택적 "data" 속성은 각 고유 필드 값이 출력되는지(data="values"), 각 고유 필드 값의 총 카운트가 출력인지(data="counts") 또는 각 고유 값이 들어 있는 결과 수(data="results")가 출력인지를 제어합니다. "data"의 기본값은 "values"입니다. 목록 형식이 아닌 필드의 경우 data="counts" 및 data="results"는 동일합니다. separator 속성은 출력 값 사이에 삽입할 단일 문자 또는 구분 기호를 정의합니다. 선택적 "정렬" 속성은 출력 순서를 제어합니다.sortby="none"은 특정 순서를 의미하지 않고, sortby="values"는 필드 값(필드의 정렬 속성에 따라 오름차순 또는 내림차순)으로 정렬하는 것을 의미하며, sortby="counts"는 필드 값 카운트의 내림차순으로 정렬하는 것을 의미하며, sortby="results"는 각 값을 포함하는 결과 수의 내림차순으로 정렬하는 것을 의미합니다. </p> <p>sortby="counts" 및 sortby="results"는 목록 형식이 아닌 필드에 해당합니다. 선택적 "max-items" 속성은 출력할 항목 수를 제한합니다. "max-items"의 기본값은 -1이며, 이것은 "모든 항목 출력"을 의미합니다. </p> <p>최대 항목에 대해서는 절대 제한이 100입니다. "date-format", "gmt" 및 "language" 속성은 지정된 필드의 컨텐츠 유형이 "date"인 경우에만 관련이 있습니다. "date-format" 특성은 "%A, %B %d, %Y"(2016년 7월 25일 월요일)와 같은 UNIX 스타일 날짜 형식 문자열을 가져옵니다. "gmt"의 기본값은 "yes"로 설정되며 날짜 문자열의 시간 부분을 GMT("yes")로 출력할지 또는 계정의 표준 시간대("no")로 출력할지를 제어합니다. </p> <p>날짜 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 형식 문자열을</a>참조하십시오. </p> <p>"language" 속성은 출력 날짜 문자열의 언어 및 로케일 규칙을 제어합니다. "0"(기본값)은 "계정 언어 사용"을 의미합니다. 기타 모든 "언어" 값은 특정 언어 식별자로 해석됩니다. 예를 들어 "en_US"는 "영어(미국)"를 의미합니다. 선택적 "인코딩" 속성은 출력 문자열 문자가 결과 페이지에서 출력하기 위해 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. "encoding"의 기본값은 "html"입니다. </p> <p>언어 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 식별자를</a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 지정된 검색 필드 값 목록에 대한 카운트 정보를 표시합니다. 이 태그에는 세 가지 뚜렷한 사용 방법이 있습니다. "name" 속성만 제공되는 경우 이 태그는 전체 결과 집합 내에서 명명된 필드에 대한 고유한 값의 수를 출력합니다. "name" 및 "value" 속성이 모두 제공되면 이 태그는 전체 결과 집합(results="no") 내에서 지정된 값의 총 개수를 출력하거나 전체 결과 집합(results="yes")에 지정된 값을 포함하는 총 결과 수를 출력합니다. "results"의 기본값은 "no"입니다. 참고:목록 형식이 아닌 필드의 경우 results="yes" 및 results="no"가 해당합니다. "value" 속성이 제공되지 않으면 "results"의 값이 무시됩니다. 이 태그는 검색 쿼리에서 <span class="codeph"> sp-sfvl-field </span> CGI 매개 변수로 지정된 필드에 대한 출력만 산출합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt;...&lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt;...&lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>지정된 특성을 사용하여 <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> 에 상응하는 호출이 0보다 큰 값을 반환하거나 반환하지 않을 경우 이러한 태그는 그 사이에 HTML을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt;...&lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그는 지정된 특성을 사용하여 <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> 에 상응하는 호출이 단일 값을 반환하거나 반환하지 않을 경우 두 태그 사이의 컨텐츠를 표시합니다. 이것은 일반적으로 계정에서 패싯 슬롯을 사용하는 경우에 사용됩니다. 패싯 슬롯에서는 일반적으로 연결된 이름-슬롯에 단일 항목이 있을 때만 값-슬롯을 표시하려고 합니다. 전송 템플릿에서 이 검사를 수행하는 것이 프레젠테이션 레이어에서 수행하는 것보다 더 효율적입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 필드 값 목록 루프 태그 {#section_0717FA09F0FC449CB916883B0500A60E}

다음 고급 태그는 루핑 구문을 사용하여 전체 검색 결과 집합의 필드 값 및 관련 데이터를 열거하고 출력합니다. 이러한 태그는 검색 쿼리의 CGI 매개 변수에 의해 지정된 `sp-sfvl-field` 필드에 대해서만 출력합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt;..&lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 전체 결과 집합 내의 특정 필드에 대한 필드 값과 관련 데이터를 열거하는 루프를 만듭니다. 이 태그를 다른 <span class="codeph"> &lt;search-field-values&gt; </span> 태그 내에 중첩하지 마십시오. "name" 속성은 열거할 값이 들어 있는 필드의 이름을 지정합니다. 선택적 "sortby" 속성은 열거형 순서를 제어합니다."none"은 특정 순서를 의미하지 않으며, "values"는 필드 값(필드의 정렬 속성에 따라 오름차순 또는 내림차순)으로 정렬함을 의미하며, sortby="counts"는 필드 값 카운트의 내림차순으로 정렬하는 것을 의미하며, sortby="results"는 각 값이 들어 있는 결과 수의 내림차순으로 정렬합니다. </p> <p>sortby="counts" 및 sortby="results"는 목록 형식이 아닌 필드에 해당합니다.. 선택적 "max-items" 속성은 반복 횟수를 지정된 값으로 제한합니다. "max-items"의 기본값은 -1이며, 이는 "모든 값 열거"를 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 &lt;search-field-values&gt; 루프 반복에 대한 필드 값을 출력합니다. 이 태그는 <span class="codeph"> &lt;search-field-values&gt; </span> 루프 내에서만 유효합니다. "date-format", "gmt" 및 "language" 속성은 바깥쪽 &lt;search-field-values&gt; 태그에 지정된 필드 이름의 컨텐트 유형이 "date"인 경우에만 관련이 있습니다. "date-format" 특성은 "%A, %B %d, %Y"(2020년 7월 25일 월요일)와 같은 UNIX 스타일 날짜 형식 문자열을 가져옵니다. </p> <p>날짜 <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> 형식 문자열을</a>참조하십시오. </p> <p>선택적 "인코딩" 속성은 출력 문자열 문자가 결과 페이지에서 출력하기 위해 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. "encoding"의 기본값은 "none"입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. "gmt"의 기본값은 "yes"로 설정되며 날짜 문자열의 시간 부분을 GMT("yes")로 출력할지 또는 계정의 표준 시간대("no")로 출력할지를 제어합니다. "language" 속성은 출력 날짜 문자열의 언어 및 로케일 규칙을 제어합니다. "0"(기본값)은 "계정 언어 사용"을 의미합니다. 기타 모든 "언어" 값은 특정 언어 식별자로 해석됩니다. 예를 들어 "en_US"는 "영어(미국)"를 의미합니다. </p> <p>언어 <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> 식별자를</a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 <span class="codeph"> &lt;search-field-values&gt; </span> 루프 반복과 연결된 카운트를 출력합니다. 출력 개수는 필드 값(results="yes")을 포함하는 전체 결과 집합의 결과 수 또는 전체 결과 집합의 필드 값에 대한 총 수입니다. "results"의 기본값은 "no"입니다. </p> <p>목록 형식이 아닌 필드의 경우 results="yes" 및 results="no"가 해당합니다. 이 태그는 <span class="codeph"> &lt;search-field-values&gt; </span> 루프 내에서만 유효합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 <span class="codeph"> &lt;search-field-values&gt; </span> 루프 반복에 대한 서수 카운터를 출력합니다. 이 태그는 <span class="codeph"> &lt;search-field-values&gt; </span> 루프 내에서만 유효합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 태그 제안 {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

사용자에게 익숙한 &quot;추천 단어: 서비스를 참조하십시오. 예를 들어 사용자가 검색어의 맞춤법이 틀린 경우, [제안]을 사용하면 사용자가 올바른 맞춤법을 제안하여 결과를 찾을 수 있습니다. 시스템에서 사용자가 결과를 검색하는 데 도움이 되는 관련 키워드를 제안할 수도 있습니다. 제안 서비스는 제안을 생성할 때 다음 두 가지 사전을 사용합니다.계정 언어( **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**&#x200B;아래에 설정)와 계정 인덱스의 키워드에서 고유하게 작성된 계정 언어를 기반으로 합니다.

>[!NOTE]
>
>제안 서비스는 중국어, 일본어 또는 한국어에 적용되지 않습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-suggestions&gt;...&lt;/search-if-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그를 <span class="codeph"> &lt;search-propose&gt;, </span>&lt;search-propose-link&gt; 등과 같은 "추천" 템플릿 태그로 둘러싸십시오. <span class="codeph"> </span>이렇게 하십시오. 검색이 제안을 생성하면 검색 엔진은 열린 태그와 닫기 태그 사이의 모든 항목을 출력하고 처리합니다. 검색에 제안이 생성되지 않으면 중첩된 콘텐츠 중 아무 것도 출력되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestions&gt;...&lt;/search-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 원래 "의도"로 입력된 쿼리에 대해 제안된 검색어 목록(예: "의도된", "의도된" 및 "의도된")을 포함하는 "제안" 루프를 생성합니다. 용어 목록을 생성할 때 검색 엔진은 중첩된 HTML 및/또는 템플릿 태그를 최대 5배까지 반복하며, 이것은 최대 제안 수입니다. count 속성을 사용하여 생성된 제안 수(0-5 사이)를 지정합니다. </p> <p>&lt;search- <span class="codeph"> suggestions&gt; </span> 태그가 페이지에 여러 번 표시되어 제안 목록을 반복할 수 있습니다. 여러 제안은 각 산출의 결과에 따라 정렬됩니다. </p> <p>&lt;search- <span class="codeph"> suggestions&gt; </span> 태그를 열고 닫는 <span class="codeph"> &lt;search-if-suggestions&gt; </span> 태그 사이에 중첩합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-propoision-link&gt;...&lt;/search-proposal-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 원래 용어 대신 선택한 제안된 검색어를 사용하여 원래 검색 쿼리에 대한 링크를 생성합니다. 이 태그는 클래스, 대상 및 스타일과 같은 모든 HTML 속성을 수락하고 출력합니다. 태그는 URL 속성을 허용할 수도 있습니다. 이 속성은 생성된 링크의 기본 URL로 사용됩니다. 태그는 <span class="codeph"> &lt;search-suggestions&gt; </span> 루프 내에만 나타날 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-inpropose-text/&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 제안된 쿼리 용어(예: 원래 "의도"로 입력한 쿼리에 대해 "의도함"을 인쇄합니다.) 태그에 특성이 없으며 <span class="codeph"> &lt;search-suggestions&gt; </span> 루프 내에만 나타날 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggestions&gt;...&lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>검색에서 제안이 생성되지 않으면 검색 엔진은 열린 태그와 닫기 태그 사이의 모든 항목을 출력하고 처리합니다. 검색에서 제안이 생성되면 중첩된 컨텐츠 중 하나도 출력되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-inposification&gt;...&lt;/search-if[-not]-first-proposal&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 조건부 태그에는 제안된 용어가 제안 루프의 첫 번째 용어인지 여부를 기반으로 두 용어 간의 HTML이 포함됩니다. 태그는 열기 및 닫기 <span class="codeph"> &lt;search-proposal&gt; </span> 태그 사이에 나타나야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-proposal&gt;...&lt;/search-if[-not]-last-proposal&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 조건부 태그에는 제안된 용어가 제안 루프의 마지막 용어인지 여부를 기반으로 두 용어 간의 HTML이 포함됩니다. 태그는 열기 및 닫기 <span class="codeph"> &lt;search-proposal&gt; </span> 태그 사이에 나타나야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-propose-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 현재 제안된 검색어의 숫자 인덱스를 반환합니다. 태그는 열기 및 닫기 <span class="codeph"> &lt;search-propose&gt; </span> 태그 사이에 나타나야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-propoision-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 제안된 총 검색 용어 수를 반환합니다. 태그는 열기 및 닫기 <span class="codeph"> &lt;search-propose&gt; </span> 태그 사이에 나타나야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-propose-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그는 제안된 검색어에 대한 총 결과 수를 반환합니다. 태그는 열기 및 닫기 <span class="codeph"> &lt;search-propose&gt; </span> 태그 사이에 나타나야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 문자열 태그 {#section_67E3D529661F4F03A1FF469D9D658CAF}

다음 태그는 템플릿의 해당 지점에서 문자열을 HTML로 출력합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>템플릿 링크 아래에 기본 모양 섹션이 설정하는 검색 링크 색상 설정이 있는 HTML 본문 태그입니다. 이 태그에 배경 속성을 추가하여 결과 페이지에 배경 이미지를 표시합니다. 이 태그에 추가된 모든 색상 속성은 기본 Look 섹션에 설정된 검색 링크 색상 설정을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>템플릿 링크 아래의 기본 모양 섹션에서 설정된 검색 결과 머리글의 HTML입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt;...&lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>search-data 태그는 해당 XML 태그로 대체됩니다.&lt;search-data&gt; <span class="codeph"> 는 </span> <span class="codeph"> &lt;![CDATA[" 및 &lt;/search-cdata&gt; </span> 태그가 " <span class="codeph"> ]]&gt; </span>"로 대체되었습니다. XML 파서는 열린 태그와 닫기 태그 사이의 정보를 구문 분석하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query-query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>방문자가 입력한 쿼리입니다. 고급 선택적 "쿼리 번호" 속성은 번호가 매겨진 쿼리 문자열이 이 태그로 출력되는 것을 제어합니다. 예를 들어 <span class="codeph"> &lt;search-query-query-number=1&gt; </span> 는 <span class="codeph"> sp_q_1 </span> cgi 매개 변수의 컨텐츠를 출력합니다. "query-number"가 지정되지 않았거나 쿼리 번호가 "0"인 경우 기본 쿼리( <span class="codeph"> sp_q </span>)가 출력됩니다. 선택적 "인코딩" 속성은 출력이 결과 페이지에서 출력하기 위해 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. "encoding"의 기본값은 "html"입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 검색에 대한 총 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 페이지에 대해 보고된 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 페이지에 대해 보고된 첫 번째 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 페이지에 대해 보고된 마지막 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>이전 페이지에 대해 보고된 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>다음 페이지에 대해 보고된 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 검색에 대한 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>계정에 대해 구성된 검색 로고의 HTML(있는 경우) 이 로고는 사이트 검색/머천다이징에 크레딧을 부여하는 이미지입니다 </p> <p>현재 대부분의 계정에 연결된 검색 로고가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 검색에 대한 결과 컬렉션입니다. 선택적 "all" 속성은 전체 웹 사이트를 나타내는 컬렉션의 이름을 지정하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt;...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>시작 및 끝 양식 태그를 삽입합니다. 메서드 및 작업 속성을 시작 양식 태그에 삽입합니다. 언어뿐만 아니라 JavaScript 관련 "name" 및 "onSubmit" 속성을 위한 dir="RTL" 속성을 비롯한 추가 속성을 수락합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>계정 번호를 지정하는 양식 입력 태그를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>갤러리 번호를 지정하는 양식 입력 태그를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query-query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>쿼리 문자열을 지정하는 양식 입력 태그를 삽입합니다. 고급 선택적 "쿼리 번호" 속성은 번호가 매겨진 쿼리를 양식 입력 태그에 사용할 수 있도록 제어합니다. 예를 들어 <span class="codeph"> &lt;search-input-query-number=1&gt; </span> 는 <span class="codeph"> sp_q_1 </span> 쿼리에 대한 양식 입력 태그를 출력합니다. "query-number"가 지정되지 않았거나 "query-number"가 "0"인 경우 기본 <span class="codeph"> sp_q </span> 쿼리에 대한 입력 태그가 삽입됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>컬렉션 선택 메뉴를 표시하는 양식 선택 태그 및 관련 HTML을 삽입합니다. 선택적 "all" 속성은 전체 웹 사이트를 나타내는 컬렉션의 이름을 지정하는 데 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>검색 템플릿 태그 중 하나의 출력을 결과 페이지의 다른 HTML 또는 템플릿 태그 내에 삽입합니다. <span class="codeph"> &lt;search-lt&gt; </span> 는 보다 작은 문자를 삽입합니다. &lt;search-lt&gt; <span class="codeph"> 및 </span> &lt;search-gt&gt; <span class="codeph"> </span> 를 사용하면 태그 정의를 escape하여 속성 값으로 검색 템플릿 태그를 사용할 수 있습니다. 템플릿에 대한 응답이 렌더링되면 &lt;search-lt&gt; <span class="codeph"> </span> 태그가 보다 작음 기호(&lt;)로 바뀝니다. 예를 들어 <span class="codeph"> &lt;search-link&gt; </span> 는 <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>와 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>검색 템플릿 태그 중 하나의 출력을 결과 페이지의 다른 HTML 또는 템플릿 태그 내에 삽입합니다. <span class="codeph"> &lt;search-gt&gt; </span> 는 보다 큰 문자를 삽입합니다. &lt;search-lt&gt; <span class="codeph"> 및 </span> &lt;search-gt&gt; <span class="codeph"> </span> 를 사용하면 태그 정의를 escape하여 다른 템플릿 태그를 속성 값으로 사용할 수 있습니다. 검색에 대한 응답으로 템플릿이 렌더링되면 보다 큼 기호(&gt;)가 <span class="codeph"> &lt;search-gt&gt; </span> 태그를 대체합니다. 예를 들어 <span class="codeph"> &lt;search-link&gt; </span> 는 <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>와 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>현재 검색 요청에서 "param-name"이라는 cgi 매개 변수의 값을 반환합니다. 선택적 "인코딩" 속성은 출력이 결과 페이지에서 출력하기 위해 HTML 인코딩, JavaScript 인코딩, Perl 인코딩, URL 인코딩 또는 인코딩되지 않았는지 여부를 제어합니다. "encoding"의 기본값은 "html"입니다. 일반적으로 인코딩 속성을 지정할 필요가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; <span class="codeph"></span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>인코딩 <span class="codeph"> </span> 속성은 선택 사항입니다.기본값은 <span class="codeph"> json </span>입니다. </p> <p> <p>참고: 이 태그는 <span class="codeph"> </span> sp_trace=1이 핵심 검색 쿼리 매개 변수와 함께 지정된 경우에만 출력됩니다. </p> </p> <p>백 엔드 검색 CGI 매개 변수에 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>있는 표에서 48행을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 앵커 링크 태그 {#section_3A51D27616C541E2B818CC52B2B856BA}

다음은 앵커 링크가 두 태그 사이의 HTML을 둘러싸도록 하는 태그입니다. 앵커 링크를 클릭하면 다른 결과 페이지가 표시되도록 요청합니다. 선택적 속성 &quot;count&quot;는 페이지에 표시되는 결과를 많이 요청합니다. 지정하지 않으면 현재 페이지에서 요청한 카운트가 사용됩니다. 고급 선택적 &quot;URL&quot; 속성은 연결된 링크가 연결되는 도메인을 제어합니다. 기본적으로 도메인은 `https://search.atomz.com/search/`으로 설정되지만 URL 속성을 사용하여 변경할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt;...&lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>결과의 다음 또는 이전 페이지를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>날짜 또는 연관성별로 결과를 정렬합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summary URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-show-summary&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summary URL="https://search.yourdomain.com/search/"&gt; ...&lt;/search-hide-summary&gt; </span> </p> </td> 
   <td colname="col2"> <p>요약을 표시하거나 숨깁니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 조건부 태그 {#section_18D9BC66DE484881932FD2F7EA9D170D}

두 태그 사이에 HTML을 조건부로 포함할 수 있는 태그입니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt;...&lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt;...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그에는 현재 페이지에 검색 결과가 있거나 없는 경우 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt;...&lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt;...&lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt;...&lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt;...&lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 이전 페이지 또는 다음 페이지에 연관된 결과가 있는 경우 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt;...&lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt;...&lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt;...&lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt;...&lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 페이지가 연관성 또는 날짜별로 정렬되어 있거나 없는 경우 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summary&gt;...&lt;/search-if-show-summary&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summary&gt;...&lt;/search-if-hide-summary&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 현재 페이지에서 요약을 표시하거나 숨기는 경우 HTML이 포함됩니다. 이러한 태그를 사용하여 검색 결과의 일부를 포함하거나 제외할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt;...&lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt;...&lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>이 태그에는 현재 페이지에 대한 검색 결과 생성에 컬렉션이 지정된 경우 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt;...&lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt;...&lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그에는 <span class="codeph"> sp_advanced=1 CGI </span> 매개 변수가 검색 쿼리에 지정된 경우 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt;...&lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt;...&lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 태그는 지정된 매개 변수가 잘못되었거나 유효하지 않은 경우 태그 사이에 HTML을 포함하거나 제외합니다. </p> <p>현재 <span class="codeph"> sp_q_location[_#] </span> 매개 변수만 지원됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt;...&lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt;...&lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 고급 태그에는 "name" 속성에 지정된 CGI 매개 변수가 "value" 속성에 지정된 값을 가지고 있는지 여부에 따라 그 사이에 HTML이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt;...&lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt;...&lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 고급 태그에는 현재 페이지가 지정된 필드 이름으로 정렬되어 있거나 없는 경우 그 사이에 있는 HTML이 포함됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 양식 제어 태그 {#section_45AFC414ACA74825B72FEAA8456F8DD2}

검색 템플릿에서 확인란, 라디오 단추 및 목록 상자의 기본 선택 상태를 제어할 `<form>` 수 있는 태그입니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;input&gt; <span class="codeph"> 태그 대신 템플릿에 </span> 사용됩니다. 태그가 브라우저에 작성되면 단어 <span class="codeph"> input이 </span> 검색 입력을 <span class="codeph"> </span> 대체하며 태그에 있는 다른 모든 정보는 그대로 출력됩니다. 또한 태그에 <span class="codeph"> 지정된 </span> 이름이 CGI 매개 변수로 나열되고 태그에 <span class="codeph"> 지정된 </span> 값이 해당 CGI 매개 변수의 값이면 <span class="codeph"> </span> 확인된 단어가 태그 끝에 추가됩니다. 이렇게 하면 검색 결과의 기본 라디오 단추 또는 확인란 상태를 현재 쿼리와 동일하게 자동으로 만들 수 있습니다. </p> <p>예를 들어, 확인란에 대한 HTML 코드는 다음과 같을 수 있습니다. </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;유사한 사운드 일치 없음 </span> </p> <p>해당 확인란을 위한 해당 템플릿 코드는 다음과 같습니다. </p> <p> <span class="codeph"> &lt;search-input type=checkbox name="sp_w" value="exact"&gt;유사한 사운드 일치 없음 </span> </p> <p>쿼리에 대한 CGI 매개 변수 문자열에 <span class="codeph"> sp_w=exact </span>가 있는 경우 검색 결과가 포함된 태그가 다음과 같이 표시됩니다(선택한 단어가 태그 끝에 <span class="codeph"> </span> 삽입됨). </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact" checked&gt;유사한 사운드 일치 없음 </span> </p> <p>쿼리에 대한 CGI 매개 변수 문자열에 <span class="codeph"> sp_w=exact </span>가 없으면 검색 결과가 있는 브라우저에 기록된 태그가 다음과 같이 표시됩니다(선택한 단어는 태그에 <span class="codeph"> </span> 나열되지 않음). </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;유사한 사운드 일치 없음 </span> </p> <p>&lt;search-input&gt; <span class="codeph"> </span> 태그는 검색 템플릿에 확인란 및 라디오 단추를 입력하는 데 유용합니다. 검색 템플릿의 <span class="codeph"> &lt;form&gt; </span> 에 추가하려는 확인란 또는 라디오 단추가 있는 경우 <span class="codeph"> &lt;input...&gt; </span> 대신 <span class="codeph"> &lt;search-input...&gt; </span>을 사용하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt;...&lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt;...&lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>&lt;form&gt; <span class="codeph"> 태그의 </span> 드롭다운 목록 상자는 <span class="codeph"> &lt;select&gt; </span> 태그로 시작되어 <span class="codeph"> &lt;/select&gt; </span> 태그로 끝납니다. 연결된 CGI 매개 변수의 <span class="codeph"> 이름이 </span> &lt;select&gt; <span class="codeph"> </span> 태그 내에 나열됩니다. &lt; <span class="codeph"> select&gt; </span> 태그 아래는 목록 상자 내에 표시할 값을 지정하는 <span class="codeph"> &lt;option&gt; </span> 태그 목록입니다. </p> <p>&lt;search-select&gt; <span class="codeph"> , </span>&lt;/search-select&gt; <span class="codeph"> , </span>&lt;search-option&gt; <span class="codeph"> 및 </span>search-option &lt;/search- <span class="codeph"> </span> <span class="codeph"> </span> option&gt; 태그는 &lt;search-input&gt; 태그와 유사한 기능을 제공합니다. 즉, <span class="codeph"> 선택한 </span> 단어가 <span class="codeph"> &lt;옵션&gt;의 끝에 자동으로 </span> 추가되는데, 이 경우 <span class="codeph"> 에서 [선택 </span> &gt; 태그의 이름이 CGI 매개 변수로 표시되고, CGI 매개 변수의 값이 <span class="codeph"> 특정 검색 옵션 &lt;선택 사항&gt;에 있는 값으로 CGI 매개 변수가 </span> <span class="codeph"> </span> <span class="codeph"> </span> <span class="codeph"> </span> 나열되는 경우, &lt;옵션&gt;이 브라우저에 추가됩니다. 이렇게 하면 검색 결과에서 기본 목록 상자를 현재 쿼리와 동일하게 자동으로 선택할 수 있습니다. </p> <p>예를 들어 일반적인 목록 상자는 다음과 같습니다. </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>해당 목록 상자의 해당 템플릿 코드는 다음과 같습니다. </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>검색 템플릿에서 &lt; <span class="codeph"> form&gt; </span> 에 추가하려는 경우 <span class="codeph"> &lt;search-select.&gt; </span> 대신 <span class="codeph"> &lt;search-select.&gt; </span>를 사용하십시오. &lt;&lt;select <span class="codeph"> 를 선택합니다.&gt; </span> 를 먼저 사용하십시오. &lt;&lt;search-select&gt;를 선택합니다. &lt;&lt;search-option&gt;을 선택합니다. &lt;검색 위치&gt; <span class="codeph"> &lt;위치&gt;를 선택합니다. &lt;검색 위치&gt;를 선택합니다. &lt;위치&gt; &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 선택하면 &lt;검색 옵션 &lt;를 선택합니다.&gt; &lt;를 선택합니다. &lt;를 선택합니다.&gt; &lt;를 &lt;위치 &lt;를 선택합니다.&gt; &lt;를 선택합니다.&gt; &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 </span>&gt; &lt;를 선택합니다. &lt;를 선택합니다.&gt;. &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 <span class="codeph"> &gt; &lt;를 선택합니다. &lt;를 선택하면 &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 선택합니다. &lt;를 &lt;를 선택합니다. &lt;를 선택합니다.&gt; &lt;를 선택합니다. &lt;를 선택합니다.&gt;. &lt;위치 &lt;를 </span> &gt;. &lt;를 선택합니다.&gt; &lt;위치 &lt;를 선택합니다.&gt; &lt;를 <span class="codeph"> </span><span class="codeph"> </span> <span class="codeph"> </span>&gt;.&gt;.&gt;. &lt;를 선택합니다.&gt; &lt;를 &lt;를 //option&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ...&lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>이러한 고급 태그는 이러한 태그 사이의 HTML 주위에 앵커 링크를 만듭니다. 이 앵커를 클릭하면 지정된 필드에 정렬된 결과 페이지가 표시됩니다. 선택적 <span class="codeph"> count </span> 속성은 결과 페이지에 표시할 결과 수를 지정합니다. 카운트를 <span class="codeph"> </span> 생략하면 현재 페이지에 사용된 카운트가 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 날짜 형식 문자열 {#section_4BBDBBEF2B96414497617CD4B52D96E4}

날짜 형식 문자열에서 다음 변환 사양을 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>날짜 형식 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p> "월요일"과 같이 전체 평일 이름의 국가 표현과 일치합니다. 언어학 &gt; <span class="uicontrol"></span> 단어 및 <span class="uicontrol"> 언어 </span> &gt; <span class="uicontrol"> 언어의 설정에 따라 국가 </span> 표현이 결정됩니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> 약자가 처음 세 문자인 "월"과 같이 요일 이름의 축약된 국가 표현과 일치합니다. 언어학 &gt; <span class="uicontrol"></span> 단어 및 <span class="uicontrol"> 언어 </span> &gt; <span class="uicontrol"> 언어의 설정에 따라 국가 </span> 표현이 결정됩니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> "June"와 같이 전체 월 이름의 국가 표현과 일치합니다. 언어학 &gt; <span class="uicontrol"></span> 단어 및 <span class="uicontrol"> 언어 </span> &gt; <span class="uicontrol"> 언어의 설정에 따라 국가 </span> 표현이 결정됩니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> 약자가 "Jun"과 같이 처음 세 문자인 축약된 월 이름의 국가 표현과 일치합니다. 언어학 &gt; <span class="uicontrol"></span> 단어 및 <span class="uicontrol"> 언어 </span> &gt; <span class="uicontrol"> 언어의 설정에 따라 국가 </span> 표현이 결정됩니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>"%m/%d/%y"에 해당합니다(예: "07/25/13"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> 월의 일을 십진수(01-31)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> 월의 일을 십진수(1-31)로 찾습니다. 한 자리 앞에 빈 자리가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> 24시간 시계를 소수(00-23)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> 축약된 월 이름의 국가 표현과 일치합니다. 여기서 약어는 처음 세 문자입니다(예: "Jun"(%b와 동일). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> 12시간 시계를 소수(01-12)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> 연도의 요일을 소수(001-366)로 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> (24시간 시계를 소수점 숫자(0-23)로 찾습니다. 한 자리 앞에 빈 자리가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> 12시간 시간을 소수점 숫자(1-12)로 찾습니다. 한 자리 앞에 빈 자리가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> 분을 소수(00-59)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> 월을 십진수(01-12)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> "PM"과 같이 "ANTE" 또는 "post merdiem"의 국가 표현을 적절히 일치시킵니다. 언어학 &gt; <span class="uicontrol"></span> 단어 및 <span class="uicontrol"> 언어 </span> &gt; <span class="uicontrol"> 언어의 설정에 따라 국가 </span> 표현이 결정됩니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>"%H:%M"에 해당합니다(예: "13:23"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>"%I:%M:%S %p"에 해당합니다(예: "01:23:45 PM"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> 둘째 숫자를 십진수(00-60)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>"%H:%M:%S"에 해당합니다(예: "13:26:47"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> 연도의 주 번호(일요일은 주의 첫째 날)를 십진수(00-53)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>"%e-%b-%Y"에 해당합니다(예: "2013년 7월 25일). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> "2013"과 같이, 세기가 있는 연도를 십진수로 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> 세기가 없는 연도를 십진수(00-99)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> 시간대 이름과 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p>  "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## 언어 식별자 {#section_0490DECC00E34691ADE5A9ED90A6D911}

다음 표는 지원되는 각 언어에 대한 언어 식별자를 포함합니다. 다음 템플릿 태그에서 이러한 식별자를 선택적 &quot;언어&quot; 속성의 값으로 사용할 수 있습니다.

* `search-date` 및 `search-display-field`.

   결과 [루프 문자열 태그를](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)참조하십시오.

* `search-field-value-list` 필드 [값 목록 태그를](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)참조하십시오.

* `search-field-value` 필드 [값 목록 루프 태그를](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)참조하십시오.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>언어 </p> </th> 
   <th colname="col2" class="entry"> <p>언어 identifier </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>불가리아어(불가리아) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어 </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어(홍콩) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어(싱가포르) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어(대만) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>체코어(체코) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>덴마크어(덴마크) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>네덜란드어(벨기에) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>네덜란드어(네덜란드) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>영어(오스트레일리아) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>영어(캐나다) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>영어(영국) </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>영어(미국) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프랑스어(벨기에) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프랑스어(캐나다) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 핀란드어(핀란드) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프랑스어(프랑스) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>프랑스어(스위스) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>독일어(오스트리아) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>독일어(독일) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>독일어(스위스) </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>그리스어(그리스) </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>아일랜드어(아일랜드) </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이탈리아어(이탈리아) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일본어(일본) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>한국어 </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>노르웨이어(노르웨이) </p> </td> 
   <td colname="col2"> <p> no_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>폴란드어(폴란드) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>포르투갈어(브라질) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>포르투갈어(포르투갈) </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>러시아어(구 소련) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>슬로바키아어(슬로바키아) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>슬로바키아어(슬로베니아) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>스페인어(멕시코) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>스페인어(스페인) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>스웨덴어(스웨덴) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## 컨텐츠 유형 HTTP 헤더 지정 {#section_AEED823E9938448A9EDB2F286D9CFD90}

다음 태그를 사용하여 Content-Type HTTP 응답 헤더를 지정할 수 있습니다.

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

및 `content` 속성은 선택 `charset` 사항입니다. 이 태그는 템플릿에 가능한 한 빨리 나타나야 합니다. 또한, `<search-html-meta-charset>` 또는 태그의 동작에 영향을 주므로, `<search-xml-decl>`또는 그 앞에나타나는 것이 좋습니다.

속성을 지정하지 `content` 않으면 `MIME-type` 기본값은 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** >에서 설정된 값으로 설정됩니다 **[!UICONTROL Content Types]**. 속성을 지정하면 `content` 태그의 기본 `content` 속성으로 사용됩니다 `<search-html-meta-charset>` .

속성을 지정하지 않으면 `charset` `charset` `content-type` 헤더에 값이 기록되지 않습니다.

지정하는 `charset="1"` 경우 실제 값은 CGI 매개 변수의 `charset-name` 값입니다 `sp_f` . 검색과 `sp_f` 함께 제출된 CGI 매개 변수가 없는 경우 계정 설정에서 실제 값을 `charset-name` 읽습니다. > > > **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** **[!UICONTROL Personal Information]** **[!UICONTROL Character Encoding]**&#x200B;아래에서 계정과 연결된 문자 집합을 보거나 변경할 수 있습니다.

개인 [사용자 정보](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)구성을 참조하십시오.

또는 같은 `charset` 값으로 나열하여 특정 문자 집합 이름을 선택할 `charset="iso-8859-1"` 수 `charset="Shift-JIS"`있습니다.

속성을 지정하면 `charset` 및 태그의 기본 `charset` 속성으로 `<search-html-meta-charset>` 사용되고 헤더로 출력됩니다 `<search-xml-decl>` `content-type` .

## HTML 템플릿에서 문자 집합 지정 {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

기본 HTML 검색 결과 템플릿은 다음 태그를 통해 현재 계정과 연결된 문자 집합을 지정합니다.

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

컨텐츠 및 차트 속성은 선택 사항입니다. 이 태그는 템플릿의 HTML `<head>` 섹션에 나타나야 합니다. 이 태그로 인해 템플릿에서 생성된 HTML 페이지에서 다음 태그가 생성됩니다.

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

content 속성을 지정하지 않으면 실제 값의 `MIME-type` 기본값은 두 값 중 하나로 설정됩니다. 태그가 속성을 `<search-content-type-header>` 지정하면 해당 `content` 값이 사용됩니다. 그렇지 않으면 사용된 값은 **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]** 탭에 설정된 값입니다.

속성을 지정하지 않으면 `charset` 실제 값의 `charset-name` 기본값은 두 값 중 하나로 설정됩니다. 태그가 속성을 `<search-content-type-header>` 지정하면 해당 `charset` 값이 사용됩니다. 그렇지 않으면 계정 설정에서 실제 값을 `charset-name` 읽습니다. > > > **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** **[!UICONTROL Personal Information]** **[!UICONTROL Character Encoding]**&#x200B;아래에서 계정과 연결된 문자 집합을 보거나 변경할 수 있습니다.

개인 [사용자 정보](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)구성을 참조하십시오.

지정하는 `charset="1"` 경우 실제 값은 CGI 매개 변수의 `charset-name` 값입니다 `sp_f` . 검색과 함께 `sp_f` 제출되는 CGI 매개 변수가 없는 경우, 실제 `charset-name` 값은 `<search-content-type-header>` 태그에 설정된 값 또는 계정 설정에서 설정된 값입니다.

에서와 같이 특정 문자 집합 이름을 지정할 수 `charset="charset-name"`있습니다. 예를 들어 `charset="iso-8859-1"` 또는 `charset="Shift-JIS"`을 입력합니다.

이 `<search-html-meta-charset>` 태그는 선택 사항입니다. 이 값을 제거하면 브라우저가 `content-type`다음 기본값을 사용합니다. `content="text/html; charset=ISO-8859-1"`Adobe 태그를 `<search-html-meta-charset>` 자신의 `http-equiv` 태그로 바꾸도록 선택할 수도 있습니다.

## XML 템플릿에서 문자 집합 지정 {#section_17DC31CDCC104F5F8081466B41A96E9D}

기본 XML 검색 결과 템플릿은 다음 태그를 통해 현재 계정과 연결된 문자 집합을 지정합니다.

`<search-xml-decl [charset="charset-name"]>`

속성은 `charset` 선택 사항입니다. 이 태그는 템플릿의 맨 위에 표시되어야 하지만 `<search-content-type-header>` 태그 뒤에 표시됩니다. 이 태그로 인해 템플릿에서 생성된 XML 문서에 다음 태그가 생성됩니다.

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

이 값을 지정하지 `charset`않으면 실제 값의 `charset-name` 기본값은 두 값 중 하나로 설정됩니다. 속성을 `<search-content-type-header>` 지정하면 해당 `charset` 값이 사용됩니다. 그렇지 않으면 계정 설정에서 실제 값을 `charset-name` 읽습니다. > > > **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** **[!UICONTROL Personal Information]** **[!UICONTROL Character Encoding]**&#x200B;아래에서 계정과 연결된 문자 집합을 보거나 변경할 수 있습니다.

개인 [사용자 정보](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)구성을 참조하십시오.

지정하는 `charset="1"` 경우 실제 값은 CGI 매개 변수의 `charset-name` 값입니다 `sp_f` . 검색과 함께 `sp_f` 제출된 CGI 매개 변수가 없는 경우 에 대한 실제 `charset-name` 값은 `<search-content-type-header>` 태그에 설정된 값 또는 계정 설정에 설정된 값입니다.

원할 경우 특정 문자 집합 이름을 지정할 수 `charset="charset-name"`있습니다. 예, `charset="iso-8859-1" or charset="Shift-JIS"`.

태그를 `<search-xml-decl>` 자신의 `?xml` 태그로 바꾸도록 선택할 수 있습니다.

## 다른 검색 템플릿 포함 {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

다른 검색 템플릿을 포함하려면 `<search-include>` 태그를 사용하여 파일 속성을 다음 예와 같이 포함할 템플릿 파일의 이름으로 설정합니다.

`<search-include file="seo/seo_search_title.tpl" />`

SEO 검색 템플릿 세그먼트는 `seo/` 하위 폴더에 있고 일반 검색 템플릿은 `templates/` 하위 폴더에 있습니다. .tpl 파일만 이 컨텍스트에 포함할 수 있습니다.

## 웹 사이트의 여러 전송 템플릿 관리 {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

각 영역에 대해 서로 다른 검색 전송 템플릿을 사용하여 웹 사이트 전체의 검색 결과 모양을 제어할 수 있습니다.

<!-- 

r_managing_multiple_templates.xml

 -->

이러한 종류의 검색 기능을 수행하려면 사이트 검색/머천다이징에서 전송 템플릿을 관리할 수 있습니다. 또는 게시에서 전송 템플릿을 관리할 수 있습니다. 사이트 검색/머천다이징과 마찬가지로 게시를 사용하면 여러 검색 전송 템플릿을 편집하고 미리 보고 게시할 수 있습니다.

특정 전송 템플릿(기본값 제외)을 사용하도록 검색 양식을 설정하려면 `sp_t` 쿼리 매개 변수를 사용합니다. 예를 들어 웹 사이트의 표시된 판매 영역에 대해 &quot;clearance&quot;라는 검색 템플릿이 있다고 가정합니다. 다음과 같은 추가 양식 코드와 함께 표준 HTML 검색 양식을 사용합니다.

`<input type=hidden name="sp_t" value="clearance">`

고객이 이 코드 줄이 포함된 표준 양식을 클릭하면 &quot;클리어런스&quot; 검색 전송 템플릿이 해당 검색 결과와 함께 표시됩니다.

검색 [양식에서](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)컬렉션 사용을 참조하십시오.

양식에 [프레임](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)사용을 참조하십시오.

고급 [검색 양식](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)샘플링을 참조하십시오.
