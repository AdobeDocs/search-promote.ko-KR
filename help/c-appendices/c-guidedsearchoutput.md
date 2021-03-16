---
description: XML 또는 JSON을 비롯한 모든 텍스트 기반 포맷으로 출력을 사용자 지정하는 방법을 살펴봅니다.
solution: Target
title: 검색 안내 출력
topic: 부록, 사이트 검색 및 머천다이징
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '6289'
ht-degree: 2%

---


# 검색 안내 출력{#guided-search-output}

XML 또는 JSON을 비롯한 모든 텍스트 기반 포맷으로 출력을 사용자 정의할 수 있습니다.

## 검색 안내 출력 사용 {#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

출력 형식은 디자인 프로세스 중에 수행되는 인사이트, 정렬 및 기타 구현 관련 결정을 지원하도록 사용자 정의할 수 있습니다. 필요한 경우 포맷 자체를 변경하여 고객의 프런트 엔드 개발을 간소화할 수 있습니다.

전체 출력은 `<result>` 태그 내에 포함되며 대부분의 동적 데이터는 `<![CDATA[ ]]>` 태그 내에 포함됩니다. 이러한 조직에서는 결과에 HTML 및 기타 비 XML 엔티티가 포함될 수 있습니다.

다른 페이지로 연결되는 링크가 제공되는 경우 상대 URL 형식으로 표시됩니다. 이 결과에는 원하는 결과를 생성하기 위해 전달된 쿼리 문자열 매개 변수도 포함됩니다.

## 검색 안내 구현 이해 {#section_95483980930C4325BAB50A40BD47245A}

검색 안내 구현을 시작하면 [!DNL Adobe Search&Promote]이(가) 비즈니스 레이어에 책임이 있음을 기억하십시오. 즉, 어떤 결과와 패싯이 지정된 시간에 고객에게 보여지는 지에 대한 논리입니다.

결과를 HTML로 구문 분석하고 표시하는 웹 응용 프로그램 프런트 엔드를 구현할 때 기능만 표시하도록 제한합니다. 즉, 프레젠테이션 레이어를 만드는 데 사용하는 서버측 논리는 필요한 경우가 아니면 고객에게 제공할 항목을 결정하지 않습니다. 프런트 엔드 스크립트가 검색 결과를 변경하는 경우에는 비즈니스 규칙이 예상대로 작동하지 않습니다.

[!DNL Adobe Search&Promote] URL 매개 변수를 통해 선택한 검색 세부 조정 옵션의 사용자 상태를 유지합니다. 모든 `<link>` 노드에는 고객이 선택한 관련 매개 변수가 포함되어 있습니다. 이러한 매개 변수에는 탐색 표시, 페이지 매김, 정렬 및 패싯 선택 사항이 포함될 수 있습니다. 해당하는 경우 고객이 선택 항목 중 &quot;뒤로&quot; 이동할 수 있도록 `<undolink>` 노드가 반환됩니다. 패싯 및 탐색 표시는 이러한 유형의 링크를 제공합니다.

## 검색 서버 작업 {#section_8DBEACDECD714E59BDED6315E6041B8D}

검색을 수행하고 결과를 받기 위해 상호 작용할 수 있는 REST 좋아요 API가 사용됩니다. 결과에 사용되는 가장 일반적인 형식은 XML 또는 JSON입니다.

기본 URI는 특정 계정 및 단계 또는 라이브 환경과 연결됩니다. 계정 관리자에서 기본 URI에 대해 여러 별칭을 요청할 수 있습니다. 예를 들어 Megacorp라는 가상 회사는 다음과 같은 두 개의 기본 URL을 계정과 연관시킵니다.

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

이전 URI는 자신의 스테이지수에 대해 라이브 색인과 후기 URI를 검색합니다.

검색 요청은 기본 URI와 기본 URI와 연결된 계정에 대해 원하는 검색을 나타내는 CGI 매개 변수 또는 키-값 쌍 집합으로 구성됩니다.

CGI 매개 변수의 세 가지 형식이 지원됩니다. 다음 예와 같이 기본적으로 계정은 세미콜론( `;`)으로 CGI 매개 변수를 구분하도록 구성됩니다.

* `https://search.megacorp.com?q=shoes ;page=2`

원하는 경우 계정 관리자가 앰퍼샌드( `&`)를 사용하여 CGI 매개 변수를 구분하도록 다음 예와 같이 계정을 구성할 수 있습니다.

* `https://search.megacorp.com?q=shoes &page=2`

다음 예제와 같이 슬래시( `/`)를 구분 문자 대신 사용하고 등호를 사용하여 &quot;클린&quot; 링크를 생성하는 세 번째 형식도 지원됩니다.

* `https://search.megacorp.com/q/shoes/page/2`

SEO 형식을 사용하여 요청을 보낼 때마다 모든 출력 링크가 동일한 형식으로 반환됩니다.

## 검색 쿼리 매개 변수 {#section_7ADA5E130E3040C9BE85D0D68EDD3223}

다음 표에서는 사용할 수 있는 표준 &quot;특별&quot; 검색 쿼리 매개 변수에 대해 설명합니다. 처리 규칙 및 비즈니스 규칙은 사용자 정의 쿼리 매개 변수를 기반으로 작성하여 회사와 관련된 사용자 정의 비즈니스 논리를 구현할 수 있습니다. 컨설팅 팀과 함께 이러한 매개 변수에 대한 설명서를 볼 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>검색 쿼리 매개 변수 </p> </th> 
   <th colname="col2" class="entry"> <p>예 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q= 문자열  </span> </p> </td> 
   <td colname="col3"> <p> 검색에 대한 쿼리 문자열을 지정합니다. 이 매개 변수는 <span class="codeph"> sp_q </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#= 문자열  </span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> q </span> 및 <span class="codeph"> x </span> 매개 변수에 번호가 매겨진  매개 변수를 사용하여 이벤트를 수행하거나 지정된 필드 내에서 검색합니다. </p> <p><span class="codeph"> q </span> 매개 변수는 패싯에서 검색하는 용어를 해당 번호 <span class="codeph"> x </span> 매개 변수가 나타내는 것으로 정의합니다. 예를 들어 크기와 색상으로 이름이 지정된 두 개의 패싯이 있는 경우 다음과 같은 요소를 가질 수 있습니다. </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>이 매개 변수는 <span class="codeph"> sp_q_exact_# </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#= 문자열  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> q </span> 및 <span class="codeph"> x </span> 매개 변수에 번호가 매겨진  매개 변수를 사용하여 이벤트를 수행하거나 지정된 필드 내에서 검색합니다. </p> <p><span class="codeph"> q </span> 매개 변수는 패싯에서 검색하는 용어를 해당 번호 <span class="codeph"> x </span> 매개 변수가 나타내는 것으로 정의합니다. 예를 들어 크기와 색상으로 이름이 지정된 두 개의 패싯이 있는 경우 다음과 같은 요소를 가질 수 있습니다. </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>이 매개 변수는 <span class="codeph"> sp_x_# </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컬렉션 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collection= string  </span> </p> </td> 
   <td colname="col3"> <p> 검색에 사용할 컬렉션을 지정합니다. 이 매개 변수는 <span class="codeph"> sp_k </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> count  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= 숫자  </span> </p> </td> 
   <td colname="col3"> <p> 표시되는 결과의 총 개수를 지정합니다. 기본값은 <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 검색 </span> &gt; <span class="uicontrol"> 검색 </span>에 정의됩니다. 이 매개 변수는 <span class="codeph"> sp_c </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> page </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= number  </span> </p> </td> 
   <td colname="col3"> <p> 반환되는 결과 페이지를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 계급  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> rank= 필드  </span> </p> </td> 
   <td colname="col3"> <p> 정적 등급에 사용할 등급 필드를 지정합니다. 필드는 0보다 큰 관련성이 있는 등급 유형의 필드여야 합니다. 이 매개 변수는 <span class="codeph"> sp_sr </span> 백엔드 매개 변수에 매핑됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= 문자열  </span> </p> </td> 
   <td colname="col3"> <p> 검색할 스토어를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sort  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= number  </span> </p> </td> 
   <td colname="col3"> <p> 정렬 순서를 지정합니다. "0"은 기본값이며 관련성 점수에 따라 정렬합니다."1"은 날짜별로 정렬합니다."-1"은(는) 정렬되지 않습니다. </p> <p>사용자는 <span class="codeph"> sp_s </span> 매개 변수의 값에 대한 필드 이름을 지정할 수 있습니다. 예를 들어 <span class="codeph"> sp_s=title </span> 은 제목 필드에 포함된 값에 따라 결과를 정렬합니다. 필드 이름이 <span class="codeph"> sp_s </span> 매개 변수의 값에 사용될 경우 결과는 해당 필드별로 정렬된 다음 관련별로 하위 정렬됩니다. </p> <p>이 기능을 활성화하려면 다음을 수행합니다. </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">제품 메뉴에서 <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 메타데이터 </span> &gt; <span class="uicontrol"> 정의 </span>를 클릭합니다. </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D"><span class="wintitle"> 단계 정의 </span> 페이지에서 다음 중 하나를 수행합니다. 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB"><span class="uicontrol"> 새 필드 추가 </span>를 클릭합니다. </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">특정 필드 이름에 대해 <span class="uicontrol"> </span> 편집을 클릭합니다. </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903"><span class="wintitle"> </span> 정렬 드롭다운 목록에서 <span class="uicontrol"> 오름차순 </span> 또는 <span class="uicontrol"> 내림차순 </span>을 클릭합니다. <p>이 매개 변수는 <span class="codeph"> sp_s </span> 백엔드 검색 매개 변수에 매핑됩니다. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## 시스템 {#section_91261B19A44A4E579B3FC9FAB9AD3665}과 통합

다음은 시스템 통합을 위한 권장 사항입니다.

* 검색 서버와 통신합니다.

   http GET 요청을 사용하여 [!DNL Adobe Search&Promote] 웹 서버와 통신할 수 있습니다. 서버에서 이러한 요청을 생성하거나 Ajax 요청을 수행하는 클라이언트측에서 해당 요청을 생성합니다.
* 검색 내역 저장.

[!DNL Adobe Search&Promote] 는 http 요청에서 전체 상태가 전달되는 상태 비국적입니다.
* 반환된 결과를 구문 분석하는 중입니다.

   SAX 기반 XML 파서를 사용하여 XML 응답을 구문 분석하는 것이 좋습니다. Ajax 요청을 생성하는 경우 이러한 요청에 대한 JSON 응답을 반환하도록 [!DNL Adobe Search&Promote]을 구성하여 응답을 보다 쉽게 구문 분석할 수 있습니다.

## 검색 안내 JSON 출력 {#reference_EB8182A564DE4374BB84158F2AABEF74}

표준 JSON 응답 출력을 설명하는 표.

[검색 안내 JSON 출력](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74)도 참조하십시오.

JSON 응답은 다음에 대해 검토할 수 있습니다.

* [배너](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [탐색 표시](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [패싯](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
* [머리글 및 쿼리](../c-appendices/c-guidedsearchoutput.md#section_1D57062259CA46E0B4F598FA4EB37065)
* [페이지 매김](../c-appendices/c-guidedsearchoutput.md#section_504E7AB570BD49AF9839530DC438EE96)
* [최근 검색](../c-appendices/c-guidedsearchoutput.md#section_525816A0355C48F8970D89B8FC3F1FFF)
* [결과](../c-appendices/c-guidedsearchoutput.md#section_41AC56BB0A084BF59379B06C8BEF2157)
* [검색 양식](../c-appendices/c-guidedsearchoutput.md#section_434DA13EA295474C99FFE9F14801CD0E)
* [정렬](../c-appendices/c-guidedsearchoutput.md#section_558853CD376F4D71BACF211D53085D55)
* [제안](../c-appendices/c-guidedsearchoutput.md#section_6EC104E1DDD94AC799B65E6E61A2FB3C)
* [영역](../c-appendices/c-guidedsearchoutput.md#section_AE53A498B440465EAF2286F2AE87D548)

## 배너 {#section_88519CAAD25F4BD49D5E517077745B0E}

예:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>배너의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 배너 노드. 여러 배너 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> 배너가 표시되는 웹 페이지의 영역입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;콘텐츠&gt; </span> </p> </td> 
   <td colname="col2"> <p> 배너 영역에 대한 HTML 내용. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 탐색 표시 {#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

다음 예제에서는 고객이 패싯을 통해 범위를 더 좁힐 때마다 선택 사항이 탐색 표시에 추가됩니다. 각 항목은 `<breadcrumb-item>`으로 표시됩니다.

예:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>탐색 표시의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 원하는 보기를 표시하는 검색 결과에 대한 상대적 링크입니다. 탐색 표시 링크를 클릭하면 후속 세부 조정이 모두 제거되는 보기로 이동합니다. 기타 옵션도 제공됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> 탐색 표시 항목의 고객 표시 텍스트입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 패싯 {#section_65932C95931743A1BFAF1DF16D7E6D92}

패싯은 고객에게 결과를 필터링할 수 있는 다듬기 옵션입니다. 패싯은 일반적으로 범주화, 가격 범위, 색상 선택 및 기타 속성 다듬기에 사용됩니다. 인덱스의 메타데이터는 패싯을 유도하는 것입니다.

고객이 범주화를 통해 아래로 이동할 때 분류 패싯을 숨기거나 표시하는 것이 일반적입니다. 가장 높은 수준의 분류(카테고리)를 계층 1이라고 합니다. 고객이 계층 1 옵션을 클릭하면 계층 2(하위 카테고리) 다듬기 옵션이 나타나고 계층 1 옵션이 사라집니다. 고객이 계층 2 옵션을 클릭하면 계층 3(하위 카테고리) 다듬기 옵션이 나타나고 계층 2 옵션이 사라집니다. 위에서 설명한 바와 같이 이러한 옵션은 숨겨지고 표시됩니다. 웹 응용 프로그램은 영향을 받지 않습니다.

각 패싯은 `<facet-item>` 태그 내에 포함됩니다. 다음 예에서는 고객이 &quot;휴일&quot;별로 검색 결과를 세분화할 수 있는 하나의 패싯을 보여줍니다.

예:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item> 
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>패싯의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> 패싯에 대한 고객 대면 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> 패싯 옵션에 대한 고객 대면 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 옵션이 다운된 결과에 대한 상대적 링크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> 세분화된 결과 세트의 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> 단면화 값을 선택하면 고객이 결과를 되돌릴 수 있는 "실행 취소 링크"를 반환합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 및 쿼리 {#section_1D57062259CA46E0B4F598FA4EB37065}

예:

```xml
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

이러한 태그는 함께 사용되어 다음과 같은 메시지를 제공합니다.&quot;신년에 대한 621의 1-16을 보여.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>머리글 및 쿼리의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> 요청과 함께 제출된 키워드 쿼리 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지에서 첫 번째 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 마지막 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 사용자 쿼리와 일치하는 총 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> 검색 결과에 전역적으로 적용되는 선택적 필드입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 페이지 매김 {#section_504E7AB570BD49AF9839530DC438EE96}

예:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>페이지 매김의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> 결과 수를 페이지당 결과 수로 나눈 값을 기준으로 총 결과 페이지 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 이미 페이지 1을 보고 있는 경우를 제외하고 결과 세트의 첫 번째 페이지에 대한 상대 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 마지막 페이지를 보고 있지 않는 한 결과 세트의 마지막 페이지에 대한 상대적 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 페이지 1을 보고 있지 않는 한 결과 세트에서 이전 페이지에 대한 상대 링크를 포함합니다.이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 마지막 페이지를 보고 있지 않는 한 결과 세트의 마지막 페이지에 대한 상대적 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> 특정 페이지 번호에 대한 상대 링크를 포함합니다. 연속적인 10개의 페이지 번호가 표시됩니다. 1페이지에서는 1-10페이지가 됩니다. 결과 세트의 끝 부분(이 경우 39)에는 30-39페이지가 있습니다. 예를 들어 결과 세트의 중앙, 15페이지는 11-20페이지였습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> 현재 선택한 페이지에 속성으로 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 최근 검색 {#section_525816A0355C48F8970D89B8FC3F1FFF}

최근 검색은 쿠키 정보를 서버로 릴레이하는 경우에만 작동하는 쿠키 기반 기능입니다.

예:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>최근 검색의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 최근 검색 노드입니다. 최근 검색 노드를 여러 개 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 이전에 검색했던 용어. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이전 검색에 대한 링크. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 {#section_41AC56BB0A084BF59379B06C8BEF2157}

결과 집합은 JSON 응답의 사용자 지정 가능한 영역입니다. 각 인덱스는 메타데이터의 필드 이름 지정 메커니즘에서 고유합니다. 제목, 설명 및 URL과 같이 각 결과에 대해 반환되는 공통 필드가 있습니다. 하지만 색인의 페이지에 대해 정의된 모든 메타데이터는 각 결과 노드에서 사용할 수 있게 될 수 있습니다. 범주화, 가격, 색상 및 축소판은 보다 매력적인 검색 결과를 생성하는 데 결과에 적용할 수 있는 옵션 중 일부에 불과합니다.

결과 형식은 구현 관련 메타데이터를 기반으로 사용자 지정됩니다. 축소판 이미지 URL을 포함하여 결과에 표시할 모든 결과 데이터는 여기에 포함됩니다.

또한 &quot;주요 결과&quot;와 같은 페이지 내의 여러 결과 영역을 구성하거나 &quot;제품&quot; 및 &quot;컨텐트&quot; 결과 섹션을 분리할 수 있습니다. 이러한 경우 패싯은 기본 결과 집합에만 연결되어 있지만 여러 결과 영역이 HTML 내에 제공됩니다.

예:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>결과의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 결과 집합 내의 결과 일련 번호입니다. 이 예에서 페이지당 10개의 결과가 표시되고 결과의 페이지 2에서는 첫 번째 항목의 인덱스가 11입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 고객을 위한 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 URL. 고객이 결과를 클릭스루할 수 있는 하이퍼링크를 만드는 데 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 검색 양식 {#section_434DA13EA295474C99FFE9F14801CD0E}

예:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>검색 양식의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택적. JSON에 있을 때, 값 1은 계정이 <span class="keyword"> Test&amp;Target </span>에 연결되어 있고 A:B 테스트에 있는 비즈니스 규칙이 하나 이상 있음을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택적. 자동 완성 기능을 사용할 때 이 노드는 CSS 및 JavaScript가 양식에 있는 컨텐츠와 함께 페이지에 있음을 나타내기 위해 표시됩니다. 이러한 필드는 자동 완성 설정을 변경하지 않는 한 일반적으로 변경되지 않습니다. 이러한 경우 xxx_cache_ver 필드가 증가하여 고객 브라우저에 캐시된 컨텐츠의 무효화를 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성과 연결된 CSS입니다. 페이지 렌더링을 향상시키려면 이 태그를 페이지에 높게 배치하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성 유틸리티에서 올바른 컨트롤에 연결하는 데 필요한 내용. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성에 필요한 사용자 지정 JavaScript. 페이지 렌더링을 향상시키려면 이 태그를 페이지에 낮게 배치하는 것이 좋습니다. 자동 완성에 YUI JavaScript도 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> 검색 양식에 포함할 모든 숨겨진 매개 변수(이름 및 값)를 포함합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section_558853CD376F4D71BACF211D53085D55} 정렬

다음 예제는 3옵션 정렬 메뉴에 대한 데이터를 보여줍니다. 이 메뉴를 통해 고객은 연관성, 제목 또는 등급별로 정렬할 수 있습니다. 현재 선택된 항목에는 &quot;selected=true&quot; 특성이 포함됩니다. &quot; 고객이 원래 표시된 기본 검색 결과로 돌아갈 수 있도록 항상 관련성 옵션을 제공합니다.

예:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>정렬 메뉴의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> 옵션에 대한 고객 대상 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 옵션에 대한 "sort" 쿼리 문자열 매개 변수의 값을 나타냅니다. 이 태그는 <span class="codeph"> &lt;link&gt; </span> 값을 사용하는 경우에는 필요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택되지 않은 옵션의 경우 <span class="codeph"> &lt;link&gt; </span> 매개 변수에는 새 정렬 매개 변수로 정렬된 동일한 결과 세트를 반환하는 상대 링크가 포함되어 있습니다. 현재 선택한 정렬 옵션에 대해 이 필드는 비어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 제안 {#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

결과가 몇 개이거나 결과가 없을 때 제안이 반환됩니다. 이 노드에는 성공적인 쿼리를 생성하는 용어가 들어 있으며 &quot;결과 없음&quot; 페이지에 표시할 수 있습니다. 또한 새 쿼리로 이동할 수 있도록 링크가 반환됩니다.

예:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제안 내용의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p>추천 용어에 대한 검색 결과에 대한 하이퍼링크를 만드는 데 사용되는 상대 링크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>제안된 용어. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영역 {#section_AE53A498B440465EAF2286F2AE87D548}

예:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>영역의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 영역 노드입니다. 여러 영역 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;이름&gt; </span> </p> </td> 
   <td colname="col2"> <p> 영역의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 또는 0을 클릭하여 영역이 표시되는지 여부를 나타냅니다. 실제 영역 컨텐츠는 웹 페이지나 검색 결과에서 정적인 영역(예: 베스트셀러 또는 관련 제품)일 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 검색 안내 XML 출력 {#reference_D93E859A277643068B10AE7A61C973EA}

표준 XML 응답 출력을 설명하는 표.

XML 응답을 다음과 같이 검토할 수 있습니다.

* [배너](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [탐색 표시](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [패싯](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
* [머리글 및 쿼리](../c-appendices/c-guidedsearchoutput.md#section_802835E19BCB48239C6770A1B72DFFF8)
* [페이지 매김](../c-appendices/c-guidedsearchoutput.md#section_72DB86DDE1284B1EA295CFFBC16A3150)
* [최근 검색](../c-appendices/c-guidedsearchoutput.md#section_BCA2DDD17F264CF6BA11634E1A514E28)
* [결과](../c-appendices/c-guidedsearchoutput.md#section_EC496F5CA2634158891455E2F6DF6833)
* [검색 양식](../c-appendices/c-guidedsearchoutput.md#section_F92D8C3D37174A10A4E26CAFF3F3DF89)
* [정렬](../c-appendices/c-guidedsearchoutput.md#section_32DC50A103BF491BA3665A5CADCCAADE)
* [제안](../c-appendices/c-guidedsearchoutput.md#section_D81BCE46F0AF443695DF9C4BA084B716)
* [영역](../c-appendices/c-guidedsearchoutput.md#section_15D8AA585F3246799968BA88EE2C9FC2)

## 배너 {#section_6A19EC26DD3B494194AAA788151B78B5}

예:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>배너의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 배너 노드. 여러 배너 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> 배너가 표시되는 웹 페이지의 영역입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;콘텐츠&gt; </span> </p> </td> 
   <td colname="col2"> <p> 배너 영역에 대한 HTML 내용. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 탐색 표시 {#section_E48A71B0EBDB4EDDA7587009AD865488}

다음 예제에서는 고객이 패싯을 통해 범위를 더 좁힐 때마다 선택 사항이 탐색 표시에 추가됩니다. 각 항목은 `<breadcrumb-item>`으로 표시됩니다.

예:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>탐색 표시의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 원하는 보기를 표시하는 검색 결과에 대한 상대적 링크입니다. 탐색 표시 링크를 클릭하면 후속 세부 조정이 모두 제거되는 보기로 이동합니다. 기타 옵션도 제공됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> 탐색 표시 항목의 고객 표시 텍스트입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 패싯 {#section_5CEB1F966C004FFEA3CF675638966E25}

패싯은 고객에게 결과를 필터링할 수 있는 다듬기 옵션입니다. 패싯은 일반적으로 범주화, 가격 범위, 색상 선택 및 기타 속성 다듬기에 사용됩니다. 인덱스의 메타데이터는 패싯을 유도하는 것입니다.

고객이 범주화를 통해 아래로 이동할 때 분류 패싯을 숨기거나 표시하는 것이 일반적입니다. 가장 높은 수준의 분류(카테고리)를 계층 1이라고 합니다. 고객이 계층 1 옵션을 클릭하면 계층 2(하위 카테고리) 다듬기 옵션이 나타나고 계층 1 옵션이 사라집니다. 고객이 계층 2 옵션을 클릭하면 계층 3(하위 카테고리) 다듬기 옵션이 나타나고 계층 2 옵션이 사라집니다. 위에서 설명한 바와 같이 이러한 옵션은 숨겨지고 표시됩니다. 웹 응용 프로그램은 영향을 받지 않습니다.

각 패싯은 `<facet-item>` 태그 내에 포함됩니다. 다음 예에서는 고객이 &quot;휴일&quot;별로 검색 결과를 세분화할 수 있는 하나의 패싯을 보여줍니다.

예:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item>  
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>패싯의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> 패싯에 대한 고객 대면 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> 패싯 옵션에 대한 고객 대면 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 옵션이 다운된 결과에 대한 상대적 링크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> 세분화된 결과 세트의 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> 단면화 값을 선택하면 고객이 결과를 되돌릴 수 있는 "실행 취소 링크"를 반환합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 및 쿼리 {#section_802835E19BCB48239C6770A1B72DFFF8}

예:

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

이러한 태그는 함께 사용되어 다음과 같은 메시지를 제공합니다.&quot;신년에 대한 621의 1-16을 보여.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>머리글 및 쿼리의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> 요청과 함께 제출된 키워드 쿼리 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지에서 첫 번째 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 마지막 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> 사용자 쿼리와 일치하는 총 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> 검색 결과에 전역적으로 적용되는 선택적 필드입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 페이지 매김 {#section_72DB86DDE1284B1EA295CFFBC16A3150}

예:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>페이지 매김의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> 결과 수를 페이지당 결과 수로 나눈 값을 기준으로 총 결과 페이지 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 이미 페이지 1을 보고 있는 경우를 제외하고 결과 세트의 첫 번째 페이지에 대한 상대 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 마지막 페이지를 보고 있지 않는 한 결과 세트의 마지막 페이지에 대한 상대적 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 페이지 1을 보고 있지 않는 한 결과 세트에서 이전 페이지에 대한 상대 링크를 포함합니다.이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 마지막 페이지를 보고 있지 않는 한 결과 세트의 마지막 페이지에 대한 상대적 링크를 포함합니다. 이 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> 특정 페이지 번호에 대한 상대 링크를 포함합니다. 연속적인 10개의 페이지 번호가 표시됩니다. 1페이지에서는 1-10페이지가 됩니다. 결과 세트의 끝 부분(이 경우 39)에는 30-39페이지가 있습니다. 예를 들어 결과 세트의 중앙, 15페이지는 11-20페이지였습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> 현재 선택한 페이지에 속성으로 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 최근 검색 {#section_BCA2DDD17F264CF6BA11634E1A514E28}

최근 검색은 쿠키 정보를 서버로 릴레이하는 경우에만 작동하는 쿠키 기반 기능입니다.

예:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>최근 검색의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 최근 검색 노드입니다. 최근 검색 노드를 여러 개 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> 고객이 이전에 검색했던 용어. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이전 검색에 대한 링크. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 {#section_EC496F5CA2634158891455E2F6DF6833}

결과 집합은 XML 응답의 사용자 지정 가능한 영역입니다. 각 인덱스는 메타데이터의 필드 이름 지정 메커니즘에서 고유합니다. 제목, 설명 및 URL과 같이 각 결과에 대해 반환되는 공통 필드가 있습니다. 하지만 색인의 페이지에 대해 정의된 모든 메타데이터는 각 결과 노드에서 사용할 수 있게 될 수 있습니다. 범주화, 가격, 색상 및 축소판은 보다 매력적인 검색 결과를 생성하는 데 결과에 적용할 수 있는 옵션 중 일부에 불과합니다.

결과 형식은 구현 관련 메타데이터를 기반으로 사용자 지정됩니다. 축소판 이미지 URL을 포함하여 결과에 표시할 모든 결과 데이터는 여기에 포함됩니다.

또한 &quot;주요 결과&quot;와 같은 페이지 내의 여러 결과 영역을 구성하거나 &quot;제품&quot; 및 &quot;컨텐트&quot; 결과 섹션을 분리할 수 있습니다. 이러한 경우 패싯은 기본 결과 집합에만 연결되어 있지만 여러 결과 영역이 HTML 내에 제공됩니다.

예:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>결과의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 결과 집합 내의 결과 일련 번호입니다. 이 예에서 페이지당 10개의 결과가 표시되고 결과의 페이지 2에서는 첫 번째 항목의 인덱스가 11입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 고객을 위한 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 페이지의 URL. 고객이 결과를 클릭스루할 수 있는 하이퍼링크를 만드는 데 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 검색 양식 {#section_F92D8C3D37174A10A4E26CAFF3F3DF89}

예:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>검색 양식의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택적. XML에 있는 값 1은 계정이 <span class="keyword"> Test&amp;Target </span>에 연결되어 있고 A:B 테스트에 있는 비즈니스 규칙이 하나 이상 있음을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택적. 자동 완성 기능을 사용할 때 이 노드는 CSS 및 JavaScript가 양식에 있는 컨텐츠와 함께 페이지에 있음을 나타내기 위해 표시됩니다. 이러한 필드는 자동 완성 설정을 변경하지 않는 한 일반적으로 변경되지 않습니다. 이러한 경우 xxx_cache_ver 필드가 증가하여 고객 브라우저에 캐시된 컨텐츠의 무효화를 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성과 연결된 CSS입니다. 페이지 렌더링을 향상시키려면 이 태그를 페이지에 높게 배치하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성 유틸리티에서 올바른 컨트롤에 연결하는 데 필요한 내용. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> 자동 완성에 필요한 사용자 지정 JavaScript. 페이지 렌더링을 향상시키려면 이 태그를 페이지에 낮게 배치하는 것이 좋습니다. 자동 완성에 YUI JavaScript도 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> 검색 양식에 포함할 모든 숨겨진 매개 변수(이름 및 값)를 포함합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section_32DC50A103BF491BA3665A5CADCCAADE} 정렬

다음 예제는 3옵션 정렬 메뉴에 대한 데이터를 보여줍니다. 이 메뉴를 통해 고객은 연관성, 제목 또는 등급별로 정렬할 수 있습니다. 현재 선택된 항목에는 &quot;selected=true&quot; 특성이 포함됩니다. &quot; 고객이 원래 표시된 기본 검색 결과로 돌아갈 수 있도록 항상 관련성 옵션을 제공합니다.

예:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>정렬 메뉴의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> 옵션에 대한 고객 대상 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> 이 옵션에 대한 "sort" 쿼리 문자열 매개 변수의 값을 나타냅니다. 이 태그는 <span class="codeph"> &lt;link&gt; </span> 값을 사용하는 경우에는 필요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p> 선택되지 않은 옵션의 경우 <span class="codeph"> &lt;link&gt; </span> 매개 변수에는 새 정렬 매개 변수로 정렬된 동일한 결과 세트를 반환하는 상대 링크가 포함되어 있습니다. 현재 선택한 정렬 옵션에 대해 이 필드는 비어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 제안 {#section_D81BCE46F0AF443695DF9C4BA084B716}

결과가 몇 개이거나 결과가 없을 때 제안이 반환됩니다. 이 노드에는 성공적인 쿼리를 생성하는 용어가 들어 있으며 &quot;결과 없음&quot; 페이지에 표시할 수 있습니다. 또한 새 쿼리로 이동할 수 있도록 링크가 반환됩니다.

예:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제안 내용의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;링크를 클릭합니다&gt; </span> </p> </td> 
   <td colname="col2"> <p>추천 용어에 대한 검색 결과에 대한 하이퍼링크를 만드는 데 사용되는 상대 링크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>제안된 용어. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영역 {#section_15D8AA585F3246799968BA88EE2C9FC2}

예:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>영역의 태그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> 개별 영역 노드입니다. 여러 영역 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;이름&gt; </span> </p> </td> 
   <td colname="col2"> <p> 영역의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 또는 0을 클릭하여 영역이 표시되는지 여부를 나타냅니다. 실제 영역 컨텐츠는 웹 페이지나 검색 결과에서 정적인 영역(예: 베스트셀러 또는 관련 제품)일 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Experience Manager {#reference_DBE13C606C3A4BB185DE53F88D0D3048}에 대한 검색 XML 출력

AEM(Adobe Experience Manager)의 표준 XML 응답 출력을 설명하는 표.

을 참조하십시오. [검색 안내 XML 출력](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

XML 응답을 다음과 같이 검토할 수 있습니다.

* [배너](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [브레드크럼](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [사용자 정의 필드](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [패싯](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [헤더](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [메뉴 및 정렬](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [페이지 매김](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [쿼리](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [최근 검색](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [결과](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [검색 양식](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [제안](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [템플릿](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [영역](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## 배너 {#section_B16EDC5533FA4494AC9983AA7357CBE3}

사이트 검색/머천다이징은 웹 페이지의 다양한 부분에 배너를 연결하여 고객의 배너를 관리할 수 있습니다.

배너 예:

다음은 &quot;top&quot;이라는 페이지 영역에 배치되는 배너의 예입니다.

```xml
   <banners> 
       <banner> 
           <area><![CDATA[top]]></area> 
           <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
       </banner> 
    </banners> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>배너 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>각 배너 영역과 해당 영역에 연결된 컨텐츠를 나타내는 0-n 배너 노드가 포함되어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>배너 </p> </td> 
   <td colname="col2"> <p>배너 </p> </td> 
   <td colname="col3"> <p>개별 배너 노드. 여러 배너 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지역 </p> </td> 
   <td colname="col2"> <p>배너 </p> </td> 
   <td colname="col3"> <p>배너가 표시되는 웹 페이지의 영역입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>콘텐츠 </p> </td> 
   <td colname="col2"> <p>배너 </p> </td> 
   <td colname="col3"> <p>배너 콘텐츠 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 브레드크럼 {#section_49EA7043FBE44315A79A4E738BE30114}

여러 탐색 표시를 지원합니다. 탐색 표시 및 해당 비헤이비어는 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**&#x200B;에서 정의할 수 있습니다. 또한 정의한 각 탐색 표시에 고유한 이름을 지정해야 합니다. 탐색 표시 XML 노드는 정의된 모든 탐색 표시를 반복합니다. 검색 결과에 탐색 표시를 하나만 표시하는 것이 좋습니다.

다음 예제에서는 고객이 패싯을 통해 범위를 더 좁힐 때마다 선택 사항이 탐색 표시에 추가됩니다. 각 항목은 `<breadcrumb-item>`으로 표시됩니다.

탐색 표시 노드 예:

```xml
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;sp_cs=UTF-8;view=xml]]></link> 
   <value><![CDATA[mens]]></value> 
                <label><![CDATA[]]></label> 
      </breadcrumb-item> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;q1=Channel;sp_cs=UTF-8;view=xml;x1=brand]]></link> 
   <value><![CDATA[Channel]]></value> 
                <label><![CDATA[brand]]></label> 
      </breadcrumb-item> 
   </breadcrumb> 
    </breadcrumbs> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>탐색 표시 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p> 각 탐색 표시를 정의하는 0-n 탐색 표시 노드를 포함합니다. 대부분의 고객은 한 가지 탐색 표시를 가지고 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>탐색 경로 </p> </td> 
   <td colname="col2"> <p>탐색 표시 </p> </td> 
   <td colname="col3"> <p> 탐색 표시의 정의를 정의하는 하위 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p>탐색 경로 </p> </td> 
   <td colname="col3"> <p> 탐색 표시의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>탐색 표시 항목 </p> </td> 
   <td colname="col2"> <p>탐색 표시 내의 개별 항목입니다. 사용자가 결과 집합을 좁힐 때 각 항목은 트레일에서 단계를 나타냅니다. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크를 클릭합니다 </p> </td> 
   <td colname="col2"> <p>탐색 표시 항목 </p> </td> 
   <td colname="col3"> <p> 원하는 보기를 표시하는 검색 결과에 대한 상대적 링크입니다. 탐색 표시 링크를 클릭하면 후속 세부 조정이 모두 제거되는 보기로 이동합니다. 드롭 및 제거와 같은 다른 옵션도 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>탐색 표시 항목 </p> </td> 
   <td colname="col3"> <p> 탐색 표시 항목의 고객 표시 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>탐색 표시 항목 </p> </td> 
   <td colname="col3"> <p> label 태그는 탐색 표시 항목을 생성하기 위해 선택한 패싯을 자세히 설명하는 탐색 표시 값에 대한 레이블을 출력합니다. 안내 탐색 표시 블록의 컨텍스트에서만 사용됩니다. 쿼리 용어 단계의 경우 이 항목은 비어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용자 지정 필드 {#section_38DD31AFE5DD4263A63644AFF484E0F4}

사용자 지정 필드는 글로벌 컨텍스트가 있는 기타 변수 모음입니다. 일반적으로 검색 결과 페이지의 메타데이터에 설정된 SEO 용도로 변수를 전달하는 데 사용됩니다.

사용자 정의 필드 노드 예:

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>사용자 정의 필드 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p> 사용자 지정 필드를 정의하는 0n개의 하위 노드를 포함할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>custom-field </p> </td> 
   <td colname="col2"> <p>사용자 정의 필드 </p> </td> 
   <td colname="col3"> <p> 선택적. name 속성에 지정된 사용자 정의 필드의 값을 포함합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 패싯 {#section_BE98990E3DD748A1BD4E0CA322314B79}

패싯은 고객에게 결과를 필터링할 수 있는 다듬기 옵션입니다. 패싯은 일반적으로 범주화, 가격 범위, 색상 선택 및 기타 속성 다듬기에 사용됩니다. 패싯은 색인의 메타데이터 위에 만들어집니다.

고객이 범주화를 통해 아래로 이동할 때 분류 패싯을 숨기거나 표시하는 것이 일반적입니다. 가장 높은 수준의 분류(카테고리)를 계층 1이라고 합니다. 고객이 계층 1 옵션을 클릭하면 계층 2(하위 카테고리) 다듬기 옵션이 나타나고 계층 1 옵션이 사라집니다. 고객이 계층 2 옵션을 클릭하면 계층 3(하위 카테고리) 다듬기 옵션이 나타나고 계층 2 옵션이 사라집니다. 위에서 설명한 바와 같이 이러한 옵션은 숨겨지고 표시됩니다.웹 응용 프로그램은 영향을 주지 않습니다.

각 패싯은 `<facet-item>` 태그 내에 포함됩니다. 다음 예에서는 고객이 &quot;휴일&quot;별로 검색 결과를 세분화할 수 있는 하나의 패싯을 보여줍니다.

패싯 블록의 예:

```xml
<facets>          
     <facet> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undo-link> 
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;q2=Mens;sp_staged=1;view=xml;x1=brand;x2=leveli]]></link> 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undolink> 
      </facet-value> 
      </facet> 
     <facet> 
         <facet-title><![CDATA[Sub-Category]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>0</selected> 
      <facet-value>           
              <label><![CDATA[Apparel]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans;q3=Apparel;sp_staged=1;view=xml;x1=leveli;x2=brand;x3=levelii]]></link> 
       <count><![CDATA[3]]></count>                         
      </facet-value>   
      </facet>         
     <facet> 
         <facet-title><![CDATA[Brand]]></facet-title> 
                <behavior><![CDATA[multi-select]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undo-link> 
      <facet-value>        
              <label><![CDATA[Amoura]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Amoura;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[9]]></count>                         
      </facet-value>   
      <facet-value>         
              <label><![CDATA[Armora]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[12]]></count>                        
      </facet-value>   
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Armora Jeans]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora+Jeans;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undolink> 
      </facet-value>   
      <facet-value>           
              <label><![CDATA[Art of Grooming]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Art+of+Grooming;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count>                         
      </facet-value>   
      <facet-value>          
              <label><![CDATA[Bear Co.]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Bear+Co.;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[1]]></count> 
      </facet-value> 
      <facet-value>      
              <label><![CDATA[Citizens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Citizens;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[D&amp;B]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|D%26B;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[17]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[David Yuri]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|David+Yuri;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[2]]></count>    
      </facet-value>   
      </facet> 
    </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>단면 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>각 패싯을 나타내는 0n개의 하위 노드가 있는 컨테이너 패싯 노드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>단면 </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p> 단일 패싯 인스턴스입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet-title </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p>패싯에 대한 고객 대면 제목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>행동 </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p>패싯 동작입니다. 예: 보통, 고정 또는 다중 선택. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>선택됨 </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p>1패싯에 선택한 값이 없으면 0이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p> 패싯을 선택한 경우에만 표시됩니다. 실행 취소 링크는 전체 패싯을 되돌립니다. 예를 들어 다중 선택 패싯인 경우 패싯에 대해 선택된 모든 옵션을 선택 취소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet-value </p> </td> 
   <td colname="col2"> <p>단면 </p> </td> 
   <td colname="col3"> <p>패싯에 속하는 모든 개별 패싯 항목을 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>선택됨 </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>패싯이 있는 현재 항목이 선택된 경우 이 노드가 있고 "true"로 설정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>패싯 옵션에 대한 고객 대면 레이블입니다. 기본적으로 이것은 이미 HTML 이스케이프되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크를 클릭합니다 </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p> 옵션에 더 많은 벌금을 부과하는 결과에 대한 상대적 링크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>count </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>세분화된 결과 세트의 결과 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>패싯 값을 선택하면 노드에서 고객이 개별 패싯 선택을 다시 선택할 수 있도록 하는 "실행 취소 링크"를 반환합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 {#section_5305B1DC5774439485CA0665DB683F9C}

예:

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## 메뉴 및 정렬 {#section_A34CBB645DBF4C70A12A5B7E81211295}

결과를 정렬하기 위한 메뉴가 지원되며 페이지당 반환되도록 결과 수를 변경할 수 있습니다. 또한 &quot;탐색으로 검색&quot;을 사용하는 데 유용한 탐색 메뉴를 지원합니다. 계정은 동일한 유형의 여러 메뉴를 정의하고 해당 프레젠테이션에 메뉴를 사용할 수 있습니다.

메뉴 노드 예:

다음 예제에서는 3옵션 정렬 메뉴와 탐색 메뉴에 대한 데이터를 보여 줍니다. 정렬 메뉴를 통해 고객은 연관성, 제목 또는 등급별로 정렬할 수 있습니다. 현재 선택된 항목에는 &quot;selected=true&quot; 특성이 포함됩니다. &quot; 고객이 원래 표시된 기본 검색 결과로 돌아갈 수 있도록 항상 관련성 옵션을 제공합니다.

```xml
<menus> 
        <menu> 
           <name><![CDATA[sort]]></name>         
             <item selected="true"> 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>   
                    <item> 
                        <label><![CDATA[WOMEN'S]]></label> 
          <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[MEN'S]]></label> 
          <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
          <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
          <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
          <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
          <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[GIFTS & HOME]]></label> 
          <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[CHILDREN & TOYS]]></label> 
          <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[ELECTRONICS]]></label> 
          <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link> 
                    </item> 
        </menu> 
    </menus> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>메뉴 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>각 메뉴를 정의하는 0-n개의 하위 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>메뉴 </p> </td> 
   <td colname="col2"> <p>메뉴 </p> </td> 
   <td colname="col3"> <p>메뉴의 단일 인스턴스(<span class="uicontrol"> 디자인 </span> &gt; <span class="uicontrol"> 탐색 </span> &gt; <span class="uicontrol"> 메뉴 </span>에 정의된 메뉴에 해당합니다). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p>메뉴 </p> </td> 
   <td colname="col3"> <p>메뉴의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>항목 </p> </td> 
   <td colname="col2"> <p>메뉴 </p> </td> 
   <td colname="col3"> <p>메뉴의 각 항목을 정의합니다. 주어진 메뉴 항목이 현재 선택된 경우 선택한 선택적 속성이 true로 설정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>항목 </p> </td> 
   <td colname="col3"> <p>메뉴 항목에 대한 고객을 위한 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>항목 </p> </td> 
   <td colname="col3"> <p>메뉴 항목의 값을 나타냅니다(메뉴가 설정된 쿼리 매개 변수 값). &lt;link&gt; 값을 사용하는 경우에는 이 태그가 필요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크를 클릭합니다 </p> </td> 
   <td colname="col2"> <p>항목 </p> </td> 
   <td colname="col3"> <p>선택되지 않은 옵션의 경우 &lt;link&gt; 매개 변수에는 동일한 결과 세트를 반환하지만 메뉴 옵션이 적용된 상대 링크가 포함됩니다. 현재 선택한 정렬 옵션에 대해 이 필드는 비어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 페이지 매김 {#section_E52F81C6A6EB4B8F996157B657EC540F}

결과 세트는 여러 페이지에 분할됩니다. 일반적으로 고객은 한 페이지에 10 - 20개의 결과를 표시합니다. 다음 페이지에 결과가 표시됩니다. 페이지 매김 XML을 사용하면 고객이 결과 집합을 통해 탐색, 페이지별 페이지를 탐색할 수 있도록 일련의 탐색 링크를 만들 수 있습니다. 4개의 탐색 링크가 있습니다.첫 번째, 마지막, 다음 및 이전 각 유형의 링크를 통해 신속하게 페이지를 이동할 수 있으므로 원하는 내용을 손쉽게 검토하고 조정할 수 있습니다.

다음 예는 5개 페이지에 대한 링크를 표시하도록 구성된 페이지 매김이 있는 첫 번째 페이지에 있는 검색에 대한 페이지 매김을 보여줍니다.

페이지 매김 예:

```xml
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
        </pages> 
    </pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>페이지 매김 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p> 결과 수를 페이지당 결과 수로 나눈 값을 기준으로 총 결과 페이지 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>총 페이지 수 </p> </td> 
   <td colname="col2"> <p>페이지 매김 </p> </td> 
   <td colname="col3"> <p>검색 결과가 분산되는 총 페이지 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 </p> </td> 
   <td colname="col2"> <p>페이지 매김 </p> </td> 
   <td colname="col3"> <p>페이지 매김에서 각 페이지를 정의하는 0-n 페이지 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>page </p> </td> 
   <td colname="col2"> <p>페이지 </p> </td> 
   <td colname="col3"> <p>4개의 특수 페이지 노드가 있습니다.첫 번째, 마지막, 이전 및 다음. 이 4개 페이지는 선택 사항이며, 의미가 있는 경우에만 결과 세트에 표시됩니다. 예를 들어, 1페이지에 있는 경우 "이전" 링크가 없습니다. 다른 모든 페이지는 위치를 나타냅니다. 나열되는 페이지 수는 페이지 매김 사용자 인터페이스에 구성된 "페이지에 대한 링크 수"에 따라 다릅니다. "selected" 속성은 고객이 현재 있는 페이지를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 쿼리 {#section_3DAA1013F09742869B80F6A361816E6C}

쿼리 노드 예:

```xml
    <query> 
        <user-query><![CDATA[mens]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[265]]></total-results> 
    </query> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p> 쿼리에 대한 개요를 제공하는 글로벌 노드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 쿼리 </p> </td> 
   <td colname="col2"> <p>쿼리 </p> </td> 
   <td colname="col3"> <p> 검색한 키워드입니다. 원래 용어에 결과가 없는 것으로 인해 </span>이(가) 제안된 용어를 자동으로 검색했습니까?<span class="uicontrol"> </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>낮은 결과 </p> </td> 
   <td colname="col2"> <p>쿼리 </p> </td> 
   <td colname="col3"> <p> 이 페이지에서 첫 번째 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상위 결과 </p> </td> 
   <td colname="col2"> <p>쿼리 </p> </td> 
   <td colname="col3"> <p> 이 페이지의 마지막 결과의 항목 번호입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>총 결과 수 </p> </td> 
   <td colname="col2"> <p>쿼리 </p> </td> 
   <td colname="col3"> <p> 사용자 쿼리와 일치하는 총 결과 수입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 최근 검색 {#section_17F942F6EC07456DABED7A483AC08446}

최근 검색은 쿠키 정보를 사이트 검색/머천다이징 서버로 중계하는 경우에만 작동하는 쿠키 기반 기능입니다.

최근 검색의 예:

```xml
    <recent-searches> 
        <clear-link><![?q=womens&gscr=clear]]></clear-link> 
        <recent-search> 
            <link><![?q=mens]]></link> 
            <label><![CDATA[mens]]></label> 
        <recent-search> 
    </recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>최근 검색 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>노드는 검색에 최근 검색이 있는 경우에만 존재합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크 지우기 </p> </td> 
   <td colname="col2"> <p>최근 검색 </p> </td> 
   <td colname="col3"> <p>모든 고객의 최근 검색을 삭제하는 상대 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>최근 검색 </p> </td> 
   <td colname="col2"> <p>최근 검색 </p> </td> 
   <td colname="col3"> <p>최근 검색을 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크를 클릭합니다 </p> </td> 
   <td colname="col2"> <p>최근 검색 </p> </td> 
   <td colname="col3"> <p>사용자가 최근 수행한 검색을 수행하는 링크를 만드는 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>최근 검색 </p> </td> 
   <td colname="col3"> <p>최근 검색에 대한 고객 표시 레이블. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 결과 {#section_155A80B8C4F641678DD9C8F257108412}

결과 집합은 XML 응답의 사용자 지정 가능한 영역입니다. 각 인덱스는 메타데이터의 필드 이름 지정 메커니즘에서 고유합니다. 제목, 설명 및 URL과 같이 각 결과에 대해 반환되는 공통 필드가 있습니다. 하지만 색인의 페이지에 대해 정의된 모든 메타데이터는 각 결과 노드에서 사용할 수 있게 될 수 있습니다. 범주화, 가격, 색상 및 축소판은 보다 매력적인 검색 결과를 생성하는 데 결과에 적용할 수 있는 옵션 중 일부에 불과합니다.

결과 형식은 구현 관련 메타데이터를 기반으로 사용자 지정됩니다. 축소판 이미지 URL을 포함하여 결과에 표시할 모든 결과 데이터는 여기에 포함됩니다.

또한 &quot;주요 결과&quot;와 같은 페이지 내의 여러 결과 영역을 구성하거나 &quot;제품&quot; 및 &quot;컨텐트&quot; 결과 섹션을 분리할 수 있습니다. 이러한 경우 패싯은 기본 결과 집합에만 연결되어 있지만 여러 결과 영역이 HTML 내에 제공됩니다.

결과 노드 예:

```xml
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
                    <field name="sku"><![CDATA[200190]]></field> 
                    <field name="pagename"><![CDATA[Relaxed Paint Splattered]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>   
         <result> 
                    <field name="index"><![CDATA[2]]></field> 
                    <field name="sku"><![CDATA[200195]]></field> 
                    <field name="pagename"><![CDATA[Tumbled Jeans]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[235]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>    
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
                    <field name="sku"><![CDATA[200196]]></field> 
                    <field name="pagename"><![CDATA[Montana Relaxed]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[220]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>         
        </result-set>   
    </results> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>0-n 결과 집합에 대한 컨테이너 노드입니다. 결과 집합이 없다는 것은 특별한 결과가 없는 랜딩 페이지에 있음을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>결과 집합 </p> </td> 
   <td colname="col2"> <p>결과 </p> </td> 
   <td colname="col3"> <p>들어오는 검색에서 여러 검색을 실행할 수 있습니다. 각 결과 집합에는 수행된 특정 명명된 검색에 대한 결과가 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p>결과 집합 </p> </td> 
   <td colname="col3"> <p>결과 세트가 속하는 검색의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>결과 집합 </p> </td> 
   <td colname="col3"> <p>결과 세트에 대한 개별 결과와 연관된 모든 필드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필드를 사용하여 참조할 수 있습니다 </p> </td> 
   <td colname="col2"> <p>결과 </p> </td> 
   <td colname="col3"> <p>name 속성은 표시되는 인덱스 내의 필드 이름을 정의합니다. 값은 해당 필드에 대한 실제 값입니다. 일부 결과에 해당 개별 결과와 관련이 없는 필드가 누락될 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 검색 양식 {#section_9E4B99D4FEDC49629F6C7E866F3A7493}

검색 양식은 고객이 검색 양식을 동적으로 작성할 수 있도록 결과 세트에 포함됩니다. 이 단계는 선택 사항입니다. 대부분의 고객은 고정된 검색 양식을 가지고 있습니다. 하지만 A:B 테스트를 수행하는 비즈니스 규칙이 하나 이상 있는 것을 기준으로 검색 양식에 Test&amp;Library mbox가 필요한지 여부를 고객이 결정할 수 있도록 해줍니다. 유사하게, 고객은 최신 자동 완성 CSS 및 JavaScript를 자동으로 선택할 수 있습니다.

검색 양식 XML의 예:

```xml
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>검색 양식 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>검색 양식을 유도하는 데이터를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>include-tnt-mbox </p> </td> 
   <td colname="col2"> <p> 검색 양식 </p> </td> 
   <td colname="col3"> <p>기술적으로 Test&amp;Target A:B 테스트를 수행하는 비즈니스 규칙이 하나 이상 있을 때만 검색 양식에 mbox가 필요합니다. 이 노드는 mbox가 필요하거나 Test&amp;Target 서버의 히트 수를 줄일 수 있도록 허용하지 않는지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자동 완성 </p> </td> 
   <td colname="col2"> <p>검색 양식 </p> </td> 
   <td colname="col3"> <p>자동 완성과 관련된 하위 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>활성화됨 </p> </td> 
   <td colname="col2"> <p>자동 완성 </p> </td> 
   <td colname="col3"> <p>검색 계정이 자동 완성 기능을 사용하는 경우 1로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> 자동 완성 </p> </td> 
   <td colname="col3"> <p> CSS를 사용하여 자동으로 완성 이 노드를 가능한 한 높은 페이지로 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 양식 컨텐츠 </p> </td> 
   <td colname="col2"> <p>자동 완성 </p> </td> 
   <td colname="col3"> <p>검색 양식에 삽입되는 컨텐츠. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>자동 완성 </p> </td> 
   <td colname="col3"> <p>자동 완성 기능을 위한 JavaScript 이 노드를 페이지에 가능한 낮게 배치합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 제안 {#section_2899FACB9AD84F60B3687C1B4EF09E15}

고객은 다음 3가지 방법으로 **[!UICONTROL Did You Mean]** 기능을 구성할 수 있습니다.결과가 없는 상태에서 제안을 하거나, 결과가 없을 때 첫 번째 제안을 자동으로 검색하거나, 결과가 낮은 경우(제안 결과가 더 많은 경우) 제안을 할 수 있습니다. 모든 제안 결과가 표시됩니다.

이 제안 노드에는 성공적인 쿼리를 생성하는 용어가 포함되어 있습니다. 또한 새 쿼리로 이동할 수 있도록 링크가 반환됩니다.

결과 0으로 인한 제안을 만들기 위한 예제 출력:

```xml
    <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>0</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=arcade;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[arcade]]></word> 
 </suggestion-item>    
    </suggestions>
```

제안을 자동으로 검색하는 출력 예:

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

결과가 낮기 때문에 제안을 만들기 위한 예제 출력:

```xml
   <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>1</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=coffee;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[coffee]]></word> 
 </suggestion-item>  
    </suggestions> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>제안 </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p> 제안이 있을 경우 제안을 정의하는 하위 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자동 검색 </p> </td> 
   <td colname="col2"> <p>제안 </p> </td> 
   <td colname="col3"> <p> 결과가 없는 경우 사이트 검색/머천다이징이 새 용어에 대해 자동으로 검색되는지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>원본 쿼리 </p> </td> 
   <td colname="col2"> <p>제안 </p> </td> 
   <td colname="col3"> <p> 사이트 검색/머천다이징이 첫 번째 제안을 자동으로 검색할 때 쿼리 노드의 사용자 쿼리는 검색된 키워드를 표시합니다. 이 노드는 원래 쿼리 용어를 표시합니다. 이 두 가지를 결합하면 "arcace 대신 아케이드 검색"과 같은 구조를 만들 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제안/결과가 낮음 </p> </td> 
   <td colname="col2"> <p>제안 </p> </td> 
   <td colname="col3"> <p>있는 경우, 현재 검색 기간이 낮은 결과를 제공하는 데 따른 사이트 검색/머천다이징이 제안인지 여부 및 제안의 결과가 상당히 높은지 여부를 나타냅니다. 두 임계값은 <span class="uicontrol"> </span>을(를) 의미했습니까? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제안 항목 </p> </td> 
   <td colname="col2"> <p>제안 </p> </td> 
   <td colname="col3"> <p>다양한 제안을 나타내는 0n 노드를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>링크를 클릭합니다 </p> </td> 
   <td colname="col2"> <p>제안 항목 </p> </td> 
   <td colname="col3"> <p>제안된 용어에 대한 링크를 만드는 경로를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>word </p> </td> 
   <td colname="col2"> <p>제안 항목 </p> </td> 
   <td colname="col3"> <p> 제안된 단어를 포함합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 템플릿 {#section_1E2BB2F274B04F5491A4CCCC38F507BD}

결과에 따라 고객 검색 경험을 전환할 수 있는 기능이 지원됩니다. 이 중 일부에는 다른 검색 결과 레이아웃으로 서로 다른 템플릿 간을 전환하는 작업이 포함됩니다. 예를 들어 제품이 많은 경우 제품의 격자 보기가 있는 템플릿이 있을 수 있습니다. 또는 세부 사항이 더 많은 단일 결과를 표시할 때 &quot;주목 받는&quot; 템플릿이 있을 수 있습니다. 검색에서 결과를 반환하지 않는 경우 &quot;결과 없음&quot; 템플릿이 있을 수도 있습니다. 템플릿 노드는 검색 결과를 표시하는 데 사용되는 템플릿을 나타냅니다.

예제 템플릿:

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>template </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>검색 결과를 표시하는 데 사용되는 템플릿의 이름을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영역 {#section_26C4A947E7B1474A8E37D86D9579B93E}

영역은 비즈니스 규칙으로 활성화 또는 비활성화할 수 있는 페이지의 섹션입니다. 영역에는 패싯, 검색, 탐색 표시, 정적 컨텐트를 포함하나 이에 제한되지 않는 모든 컨텐트가 포함될 수 있습니다. 고객 웹 페이지의 영역은 사이트 검색/머천다이징과 동일한 영역에 매핑해야 합니다.

영역 노드의 예:

```xml
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>노드 </p> </th> 
   <th colname="col2" class="entry"> <p>상위 노드 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zone </p> </td> 
   <td colname="col2"> <p>고객 결과 </p> </td> 
   <td colname="col3"> <p>0n 영역을 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zone </p> </td> 
   <td colname="col2"> <p>zone </p> </td> 
   <td colname="col3"> <p> 개별 영역 노드입니다. 여러 영역 노드를 가질 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p>zone </p> </td> 
   <td colname="col3"> <p>영역의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디스플레이 </p> </td> 
   <td colname="col2"> <p>1 또는 0(영역 이름에 해당하는 영역이 표시되거나 숨겨지는지 여부 표시) </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

Geometrixx라는 가상 웹 사이트에서 * 검색에 대한 예제 출력 및 예제 출력을 생성하는 데 사용되는 예제 프레젠테이션 템플릿입니다.

* [출력 예](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [프레젠테이션 템플릿 예](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## 출력 예 {#section_515C000A18B847D59097D0A9CCC02636}

가상 웹 사이트(Geometrixx)에서 * 검색에 대한 예제 출력입니다.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[*]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[1337]]></total-results> 
    </query> 
 
    <custom-fields> 
 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name>

             <item selected="true"> 
 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item>

             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=*;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>

                    <label><![CDATA[WOMEN'S]]></label> 
      <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link>

                    <label><![CDATA[MEN'S]]></label> 
      <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
      <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link>

                    <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
      <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
      <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link>

                    <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
      <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link>

                    <label><![CDATA[GIFTS & HOME]]></label> 
      <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link>

                    <label><![CDATA[CHILDREN & TOYS]]></label> 
      <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link>

                    <label><![CDATA[ELECTRONICS]]></label> 
      <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link>

        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
       
  <breadcrumb-item> 
    <link><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></link> 
    <value><![CDATA[*]]></value> 
                        <label><![CDATA[]]></label> 
   </breadcrumb-item> 
          
   </breadcrumb> 
 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched>0</auto-searched> 
         
        <suggestions-low-results>0</suggestions-low-results> 
         
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
      
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

        </pages> 
    </pagination> 
 
    <facets>  
         
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected>0</selected>

      <facet-value> 
           
              <label><![CDATA[Womens]]></label> 
 
       <link><![CDATA[?i=1;q=*;q1=Womens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[219]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Mens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[202]]></count> 
                         
      </facet-value> 
   
      <facet-value>

              <label><![CDATA[Beauty &amp; Fragrance]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Beauty+%26+Fragrance;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[169]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Children &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Children+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[209]]></count> 
                         
      </facet-value>

      <facet-value> 
           
              <label><![CDATA[Electronics &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Electronics+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[200]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Gifts &amp; Home]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Gifts+%26+Home;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[156]]></count>

      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Jewelry &amp; Accessories]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Jewelry+%26+Accessories;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[182]]></count> 
                         
      </facet-value> 
   
      </facet-item> 
  
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
               
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[2]]></field> 
      <field name="brand"><![CDATA[One For All]]></field> 
      <field name="price"><![CDATA[145]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[208]]></field> 
 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[4]]></field> 
      <field name="brand"><![CDATA[Vera Watson]]></field> 
      <field name="price"><![CDATA[850]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Dresses,  
          Day]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[5]]></field> 
 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[6]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[80]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[7]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[85]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[8]]></field> 
      <field name="brand"><![CDATA[Woolberry]]></field> 
 
      <field name="price"><![CDATA[280]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[9]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[10]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[55]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[11]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[45]]></field> 
 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[12]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[47]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
      
        </result-set>   
    </results>

    <banners> 
         
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
            </banner>

    </banners> 
 
    <zones> 
        <zone> 
 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

## 프레젠테이션 템플릿 예 {#section_AD42571DFB88491AA7F0FDF0929EBE97}

다음은 위의 예제 출력을 만드는 데 사용되는 예제 프레젠테이션 템플릿입니다.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[<guided-query-param gsname="q" />]]></user-query> 
 <lower-results><![CDATA[<guided-results-lower>]]></lower-results> 
 <upper-results><![CDATA[<guided-results-upper>]]></upper-results> 
 <total-results><![CDATA[<guided-results-total>]]></total-results> 
    </query> 
 
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[<guided-general-field gsname="default" field="seo_search_keywords"/>]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name> 
     <guided-menu gsname="sort"> 
         <guided-if-menu-item-selected> 
             <item selected="true"> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
        <guided-else-menu-item-selected> 
             <item> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[<guided-menu-item-path />]]></link>     
             </item> 
        </guided-if-menu-item-selected> 
    </guided-menu> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name> 
            <guided-menu gsname="ss_head_nav"> 
                <guided-if-menu-item-selected> 
                    <item selected="true"> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                <guided-else-menu-item-selected> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                </guided-if-menu-item-selected> 
            </guided-menu>  
        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
      <guided-breadcrumb gsname="default"> 
  <breadcrumb-item> 
    <link><![CDATA[<guided-breadcrumb-path gsname="goto">]]></link> 
    <value><![CDATA[<guided-breadcrumb-value />]]></value> 
                        <label><![CDATA[<guided-breadcrumb-label>]]></label> 
   </breadcrumb-item> 
         </guided-breadcrumb> 
   </breadcrumb> 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched><guided-if-suggestion-autosearch>1<guided-else-suggestion-autosearch>0</guided-if-suggestion-autosearch></auto-searched> 
        <guided-if-suggestion-autosearch><orig-query><![CDATA[<guided-suggestion-original-query/>]]></orig-query></guided-if-suggestion-autosearch> 
        <suggestions-low-results><guided-if-suggestion-low-results>1<guided-else-suggestion-low-results>0</guided-if-suggestion-low-results></suggestions-low-results> 
        <guided-suggestions> 
     <suggestion-item> 
         <link><![CDATA[<guided-suggestion-path />]]></link> 
  <word><![CDATA[<guided-suggestion />]]></word> 
     </suggestion-item> 
 </guided-suggestions> 
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[<guided-page-total />]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[<guided-page-path gsname="first" />]]></page> 
     <page position="last"><![CDATA[<guided-page-path gsname="last" />]]></page> 
     <guided-if-page-prev><page position="prev"><![CDATA[<guided-page-path gsname="prev" />]]></page></guided-if-page-prev> 
     <guided-if-page-next><page position="next"><![CDATA[<guided-page-path gsname="next" />]]></page></guided-if-page-next> 
     <guided-if-page-viewall><page position="viewall"><![CDATA[<guided-page-path gsname="viewall" />]]></page></guided-if-page-viewall> 
     <guided-if-page-viewpages><page position="viewall"><![CDATA[<guided-page-path gsname="viewpages" />]]></page></guided-if-page-viewpages> 
 
     <guided-pages> 
                <guided-if-page-selected><page position="<guided-page-number />" selected="true"><![CDATA[<guided-page-path />]]></page> 
  <guided-else-page-selected><page position="<guided-page-number />"><![CDATA[<guided-page-path />]]></page> 
  </guided-if-page-selected> 
     </guided-pages> 
        </pages> 
    </pagination> 
 
    <facets>  
        <guided-facet gsname="leveli"> 
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected><guided-if-facet-selected>1<guided-else-facet-selected>0</guided-if-facet-selected></selected> 
                <guided-if-facet-selected><undo-link><![CDATA[<guided-facet-undo-path gsname="leveli">]]></undo-link></guided-if-facet-selected> 
  <guided-facet-values> 
      <facet-value> 
          <guided-if-facet-value-selected><selected><![CDATA[true]]></selected></guided-if-facet-value-selected> 
              <label><![CDATA[<guided-facet-value>]]></label> 
       <link><![CDATA[<guided-facet-value-path />]]></link> 
       <count><![CDATA[<guided-facet-count>]]></count> 
                        <guided-if-facet-value-selected><undolink><![CDATA[<guided-facet-value-undo-path />]]></undolink></guided-if-facet-value-selected> 
      </facet-value> 
  </guided-facet-values> 
      </facet-item> 
 </guided-facet> 
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
            <guided-results gsname="default">   
         <result> 
                    <field name="index"><![CDATA[<guided-result-index />]]></field> 
      <field name="brand"><![CDATA[<guided-result-field gsname="brand" />]]></field> 
      <field name="price"><![CDATA[<guided-result-field gsname="price" />]]></field> 
      <field name="foundIn"><![CDATA[<guided-if-result-field gsname="leveli"><!--tmpl_var name='leveli'-->, </guided-if-result-field> 
            <guided-if-result-field gsname="levelii"><!--tmpl_var name='levelii'-->, </guided-if-result-field> 
          <guided-if-result-field gsname="leveliii"><!--tmpl_var name='leveliii'--></guided-if-result-field>]]></field> 
         </result>   
     </guided-results> 
        </result-set>   
    </results> 
 
    <guided-if-recent-searches> 
    <recent-searches> 
        <clear-link><guided-recent-searches-clear-path/></clear-link> 
        <guided-recent-searches> 
            <recent-search> 
                <link><guided-recent-searches-path></link> 
                <label><guided-recent-searches-value></label> 
            <recent-search> 
        </guided-recent-searches> 
    </recent-searches> 
    </guided-if-recent-searches> 
 
    <banners> 
        <guided-if-banner-set gsname="top"> 
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<guided-banner gsname="top">]]></content> 
            </banner> 
        </guided-if-banner-set> 
        <guided-if-banner-set gsname="bottom"> 
            <banner> 
                <area><![CDATA[bottom]]></area> 
                <content><![CDATA[<guided-banner gsname="bottom">]]></content> 
            </banner> 
        </guided-if-banner-set> 
    </banners> 
 
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display><guided-if-zone gsname="brand-facet">1<guided-else-zone>0</guided-if-zone></display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox><guided-if-tnt-business-rules>1<guided-else-tnt-business-rules>0</guided-if-tnt-business-rules></include-tnt-mbox> 
        <autocomplete> 
            <enabled><guided-if-autocomplete>1<guided-else-autocomplete>0</guided-if-autocomplete></enabled> 
            <css><![CDATA[<guided-ac-css/>]]></css> 
            <form-content><![CDATA[<guided-ac-form-content/>]]></form-content> 
            <javascript><![CDATA[<guided-ac-javascript/>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

