---
description: 다양한 CGI 매개 변수를 사용하는 방법에 대해 알아봅니다.
solution: Target
title: CGI 매개 변수
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 1%

---


# CGI 매개 변수{#cgi-parameters}

## CGI 매개 변수 {#concept_F395999090FE4926B38BC73D5E612800}

## CGI 매개 변수 검색 {#reference_DA27A8B0728246DA94994885E1353890}

검색 양식 코드는 사이트의 HTML( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**)을 복사하여 붙여넣을 수 있도록 제공됩니다.

자세한 내용은 [검색 양식의 HTML 코드를](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

검색 양식 자체에 나열되거나 스크립트에서 나열되는 매개 변수를 설정할 수도 있습니다. 아래 나열된 매개 변수 외에 백엔드 검색 매개 변수를 사용하여 검색을 제어할 수도 있습니다.

[백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오.

검색 요청은 기본 URL로 구성됩니다. 기본 URL은 고객이 검색하는 계정과 연결된 계정에 대해 원하는 검색 결과를 반환하는 방법을 가리키는 CGI 매개 변수 집합(키-값 쌍)을 나타냅니다.

기본 URL은 특정 계정 및 단계 또는 라이브 환경과 연결됩니다. 계정 관리자에서 기본 URL에 대해 여러 별칭을 요청할 수 있습니다. 예를 들어 Megacorp라는 회사는 계정과 연결된 2개의 기본 URL을 가질 수 있습니다.`https://search.megacorp.com` 및 `https://stage.megacorp.com`. 이전 URL은 라이브 색인을 검색하고 후자의 URL은 스테이지된 색인을 검색합니다.

CGI 매개 변수의 세 가지 형식이 지원됩니다. 기본적으로 계정은 다음 예에서처럼 세미콜론을 사용하여 CGI 매개 변수를 구분하도록 구성됩니다.

`https://search.megacorp.com?q=shoes;page=2`

원하는 경우 계정 관리자가 앰퍼샌드를 사용하여 다음 예와 같이 CGI 매개 변수를 구분하도록 계정을 구성할 수 있습니다.

`https://search.megacorp.com?q=shoes&page=2`

다음 예제와 같이 슬래시(`/`)가 구분 기호 대신 사용되고 등호 기호가 사용되는 SEO 형식이라는 세 번째 형식도 지원됩니다.

`https://search.megacorp.com/q/shoes/page/2`

SEO 형식을 사용하여 요청을 보낼 때마다 모든 출력 링크가 동일한 형식으로 반환됩니다.

| 검색 안내 매개 변수 | 예 | 설명 |
|--- |--- |--- |
| q | `q=string` | 검색에 대한 쿼리 문자열을 지정합니다. 이 매개 변수는 `sp_q` 백엔드 검색 매개 변수에 매핑됩니다.  [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오. |
| q# | `q#=string` | 세그먼트(지정된 필드 내에서 검색)는 번호가 매겨진 q 및 x 매개 변수를 통해 수행됩니다.  q 매개 변수는 해당 번호가 매겨진 x 매개 변수로 표현되는 패싯에서 검색하는 용어를 정의합니다.<br>예를 들어 크기 및 색상이라는 두 개의 패싯이 있는 경우 q1=small;x1=size;q2=red;x2=color와 같은 요소를 가질 수 있습니다.  이 매개 변수는 `sp_q_exact_#` 백엔드 검색 매개 변수에 매핑됩니다.  <br>백엔드  [검색 CGI 매개 변수를 참조하십시오](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| x# | `q#=string` | 세그먼트(지정된 필드 내에서 검색)는 번호가 매겨진 q 및 x 매개 변수를 통해 수행됩니다.  q 매개 변수는 해당 번호가 매겨진 x 매개 변수로 표현되는 패싯에서 검색하는 용어를 정의합니다. <br>예를 들어 크기 및 색상이라는 두 개의 패싯이 있는 경우 q1=small;x1=size;q2=red;x2=color와 같은 요소를 가질 수 있습니다.  이 매개 변수는 `sp_x_#` 백엔드 검색 매개 변수에 매핑됩니다.  <br>백엔드  [검색 CGI 매개 변수를 참조하십시오](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| 컬렉션 | `collection=string` | 검색에 사용할 컬렉션을 지정합니다.  이 매개 변수는 `sp_k` 백엔드 검색 매개 변수에 매핑됩니다.  [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오. |
| count | `count=number` | 표시되는 결과의 총 개수를 지정합니다.  기본값은 [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]에 정의됩니다..  이 매개 변수는 `sp_c` 백엔드 검색 매개 변수에 매핑됩니다.  [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오. |
| page | `page=number` | 반환되는 결과 페이지를 지정합니다. |
| 계급 | `rank=field` | 정적 등급에 사용할 등급 필드를 지정합니다.  필드는 0보다 큰 관련성이 있는 등급 유형의 필드여야 합니다.  이 매개 변수는 `sp_sr` 백엔드 매개 변수에 매핑됩니다.  [백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)를 참조하십시오. |
| sort | `sort=number` | 정렬 순서를 지정합니다.<br>&quot;0&quot;은 기본값이며 관련성 점수에 따라 정렬합니다.&quot;1&quot;은 날짜별로 정렬합니다.&quot;-1&quot;은(는) 정렬되지 않습니다.  사용자는 `sp_s` 매개 변수의 값에 대한 필드 이름을 지정할 수 있습니다.  예를 들어 `sp_s=title`은 제목 필드에 포함된 값에 따라 결과를 정렬합니다. ` sp_s ` 매개 변수의 값에 필드 이름을 사용하면 해당 필드별로 결과가 정렬되고 관련성별로 하위 정렬됩니다.  이 기능을 활성화하려면 [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]를 클릭합니다. 정의 페이지에서 [!UICONTROL Add New Field ]을 클릭하거나 특정 필드 이름에 대해 [!UICONTROL Edit ]을 클릭합니다. [!UICONTROL Sorting ] 드롭다운 목록에서 [!UICONTROL Ascending ] 또는 [!UICONTROL Descending ] 중 하나를 선택합니다. 이 매개 변수는 `sp_s` 백엔드 검색 매개 변수에 매핑됩니다. <br>백엔드  [검색 CGI 매개 변수를 참조하십시오].(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## 백엔드 검색 CGI 매개 변수 {#reference_582E85C3886740C98FE88CA9DF7918E8}

일반적으로 고객은 Guided Search라는 프레젠테이션 레이어와 상호 작용합니다. 하지만 이 페이지에 설명된 CGI 매개 변수를 사용하여 직접 검색 안내 레이어를 건너뛰고 백엔드 핵심 검색과 상호 작용할 수 있습니다.

다음 표에서 백엔드 검색 CGI 매개 변수를 선택할 수 있습니다.
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>단일 쿼리 지원 </p> </th> 
   <th colname="col03" class="entry"> <p>다중 쿼리 지원 </p> </th> 
   <th colname="col3" class="entry"> <p>예 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>계정 번호 문자열을 지정합니다. 이 매개 변수는 필수이며 올바른 계정 번호 문자열이어야 합니다. <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 계정 옵션 </span> &gt; <span class="uicontrol"> 계정 설정 </span>에서 계정 번호 문자열을 찾을 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p><code>sp_advanced=1 </code>이(가) 쿼리와 함께 제출되면 검색 템플릿의 <code>&lt;search-if-advanced&gt; </code> 태그와 <code>&lt;/search-if-advanced&gt; </code> 태그 사이의 모든 코드가 검색 양식에 사용됩니다. <code>&lt;search-if-not-advanced&gt; </code> 태그와 <code>&lt;/search-if-not-advanced&gt; </code> 태그 사이의 모든 코드는 무시됩니다. <code>sp_advanced=0 </code>(또는 다른 값)이 제출되면 &lt;search-if-advanced&gt; 템플릿 블록이 무시되고 &lt;search-if-not-advanced&gt; 템플릿 블록이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>표시할 결과의 총 개수를 지정합니다. 기본값은 10입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>주어진 필드에 대한 컨텍스트 정보를 수집합니다. 수집된 정보는 <code>&lt;search-context&gt; </code> 템플릿 태그를 통해 검색 결과로 출력됩니다. 기본값은 <code>body </code>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>수행할 날짜 범위 검색 유형을 지정합니다. 유형에 사용할 수 있는 값은 모두 있습니다. 즉, 날짜 범위 검색, 사용자 지정을 수행하지 않습니다. 즉, <code>sp_date_range </code> 값을 사용하여 검색할 날짜와 특정 날짜를 결정해야 합니다. 즉, <code>sp_start_day </code>, <code>sp_start_month </code>, <code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code> 및 <code>sp_end_year </code>의 값이 검색할 날짜 범위를 결정하는 데 사용됨을 나타냅니다. <code>sp_d </code> 은 검색 양식에 사용자 지정 범위(예:)로 또는 특정 시작 및 종료 날짜 범위로 검색할 수 있는 옵션이 포함되어 있는 경우에만  <code>sp_date_range </code>필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>해당 <code>sp_q_# </code> 쿼리에 대해 검색할 날짜 범위 유형을 지정합니다. "#"은(는) 1에서 16 사이의 숫자로 대체됩니다(예: <code>sp_d_8 </code>, 번호가 매겨진 쿼리 <code>sp_q_8 </code>)에 적용됩니다.) </p> <p><code>type </code>을(를) 원하는 대로 설정할 수 있습니다. 즉, 날짜 범위 검색, 사용자 지정을 수행하지 않습니다. 즉, <code>sp_date_range_# </code> 값이 검색할 날짜와 특정 날짜를 결정하는 데 사용됨을 나타내고, <code>sp_q_min_day_# </code>, <code>sp_q_min_month_# </code>, <code>sp_q_min_year_# </code>, <code>sp_q_max_day_# </code>, <code>sp_q_max_month_# </code> 및 <code>sp_q_max_year_# </code>의 값을 사용하여 날짜 범위를 결정해야 합니다. <code>sp_d_# </code>의 사용은 검색 양식에 사용자 지정 범위(예: <code>sp_date_range_# </code>) 또는 특정 시작 및 종료 날짜 범위로 검색하는 옵션이 포함되어 있는 경우에만 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>검색에 적용할 사전 정의된 날짜 범위를 지정합니다. 0보다 크거나 같은 값은 오늘 이전에 검색할 일 수를 지정합니다. 예를 들어 "0"의 값은 "today"를, "1"의 값은 "today and yesterday"를, "30"의 값은 "최근 30일 이내"를 지정합니다. </p> <p>0 아래의 값은 다음과 같이 사용자 지정 범위를 지정합니다. </p> <p>-1 = "없음"으로, 날짜 범위를 지정하지 않는 것과 같습니다. </p> <p>-2 = "이번 주" - 현재 주의 일요일부터 토요일까지 검색합니다. </p> <p>-3 = "지난 주"로, 현재 주 이전 주의 일요일부터 토요일까지 검색합니다. </p> <p>-4 = "이번 달"이며 현재 달 내의 날짜를 검색합니다. </p> <p>-5 = "지난 달"이며 현재 월 이전 달 내의 날짜를 검색합니다. </p> <p>-6 = "올해"로, 현재 연도 내의 날짜를 검색합니다. </p> <p>-7 = "지난 해"로, 현재 연도 이전 년 내의 날짜를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>해당 <code>sp_q_# </code> 쿼리에 적용할 사전 정의된 날짜 범위를 지정합니다. "#"은(는) 1에서 16 사이의 숫자로 대체됩니다(예: <code>sp_date_range_8 </code>, 번호가 매겨진 쿼리 <code>sp_q_8 </code>)에 적용됩니다.) </p> <p>0보다 크거나 같은 값은 오늘 이전에 검색할 일 수를 지정합니다. 예를 들어 0의 값은 오늘 값을 지정합니다.값 1은 오늘 및 어제 지정합니다.값이 30이면 지난 30일 이내에 지정되는 등 </p> <p>0 아래의 값은 다음과 같이 사용자 지정 범위를 지정합니다. </p> <p>-1 = "없음"으로, 날짜 범위를 지정하지 않는 것과 같습니다. </p> <p>-2 = "이번 주" - 현재 주의 일요일부터 토요일까지 검색합니다. </p> <p>-3 = "지난 주"로, 현재 주 이전 주의 일요일부터 토요일까지 검색합니다. </p> <p>-4 = "이번 달"이며 현재 달 내의 날짜를 검색합니다. </p> <p>-5 = "지난 달"이며 현재 월 이전 달 내의 날짜를 검색합니다. </p> <p>-6 = "올해"로, 현재 연도 내의 날짜를 검색합니다. </p> <p>-7 = "지난 해"로, 현재 연도 이전 년 내의 날짜를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>검색 결과를 중복 해제할 단일 필드를 지정합니다. 해당 필드의 중복 결과는 모두 검색 결과에서 제거됩니다. 예를 들어 <code>sp_dedupe_field=title </code>의 경우 지정된 제목에 대한 상위 결과만 검색 결과에 표시됩니다(두 개의 결과에 동일한 제목 필드 컨텐츠가 없는 경우). 다중 값(허용 목록) 유형 필드의 경우 전체 필드 내용이 비교에 사용됩니다. 하나의 필드만 지정할 수 있습니다. 필드 이름에 "테이블 한정자"를 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>쿼리 문자열에서 문자 수가 넘는 모든 단어에 대해 자동 와일드카드 확장을 적용하도록 지정합니다. 즉, <code>sp_e=5 </code>은 "query" 또는 "number"와 같이 5자 이상의 단어가 와일드카드 문자 '*'로 확장되도록 지정하여 "query*" 또는 "number*"를 검색하는 것과 동일한 검색을 수행합니다. 문자 수가 적은 단어는 확장되지 않으므로 "word"에 대한 검색에는 자동 와일드카드 확장이 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>문자 수가 많은 해당 <code>sp_q_# </code> 쿼리 문자열에서 모든 단어에 대해 자동 와일드카드 확장을 적용하도록 지정합니다. 즉, <code>sp_e_2=5 </code>은 "query" 또는 "number"와 같이 <code>sp_q_2 </code> 쿼리 문자열에 5개 이상의 문자가 있는 단어가 와일드카드 문자 ' <code>* </code>'로 확장되도록 지정하여 "query*" 또는 "number*"를 검색하는 것과 동일한 검색을 수행합니다. 문자 수가 적은 단어는 확장되지 않으므로 <code>sp_q_2 </code>의 "word"에 대한 검색에는 자동 와일드카드 확장이 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>이 값의 트리플트는 검색에 대한 종료 날짜 범위를 지정하며 세트로 제공해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>쿼리 매개 변수 문자열(예: <code>sp_q </code>)의 문자 집합을 지정합니다. 이 문자열은 항상 검색 양식이 포함된 페이지의 문자 집합과 일치해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>지정된 필드로 구성된 논리 데이터 테이블을 정의합니다. 예를 들어 "color", "size" 및 "price" 필드로 구성된 "items"라는 테이블이 다음과 같이 정의됩니다. </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>논리 테이블은 <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 메타데이터 </span> &gt; <span class="uicontrol"> 정의 </span>에서 "허용 목록"을 선택한 필드와 함께 가장 유용합니다. 필드 이름을 값으로 사용하는 모든 CGI 매개 변수 및 템플릿 태그는 선택적으로 "." 뒤에 오는 테이블 이름을 지정할 수 있습니다. 필드 이름 앞(예: <code>sp_x_1=tablename.fieldname </code>). </p> <p>예를 들어, "large" 크기의 하나 이상의 "red" 항목이 포함된 문서(항목이 메타데이터의 병렬 행으로 표현되는 경우)를 검색하려면 다음을 사용할 수 있습니다. </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>search-field-value-list</code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

## 백엔드 검색 CGI 매개 변수 {#section_260012BBC2514CC9A8E02E53DE8B41EE}를 사용하는 일반적인 예

다음 링크 쿼리는 검색 쿼리로서 &quot;음악&quot;을 사용하여 검색을 시작하고 모든 기본 매개 변수를 사용합니다. URL은 가독성을 위해 두 줄로 분할됩니다. HTML에서 이 링크는 모두 한 줄에 있어야 합니다.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

동일한 기능은 일반적으로 다음과 같은 형태로 정의됩니다.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

일반적으로 검색을 시작할 때 기본 매개 변수를 사용해야 합니다. 이렇게 하면 첫 번째 페이지가 표시되고, 관련성별로 정렬되며, 고객이 다른 페이지 및 기타 옵션을 선택할 수 있습니다. 사이트의 검색 양식에 컬렉션의 옵션이 포함되어 있는 경우 컬렉션 이름을 매개 변수로 전달합니다.

## 백엔드 검색 CGI 매개 변수 {#section_5FA3C620D5124FB2AB28857F8D8473F6} 사용에 대한 자세한 예

다음 양식 쿼리는 결과 `10`에서 시작하는 `25` 결과를 표시합니다. 요약이 표시되지 않고 정렬 순서는 날짜별로 지정되며 `support` 컬렉션이 사용됩니다. 지난 30일 이내에 발급된 문서만 반환됩니다.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```

