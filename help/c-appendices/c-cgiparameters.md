---
description: 'null'
seo-description: 'null'
seo-title: CGI 매개 변수
solution: Target
title: CGI 매개 변수
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# CGI 매개 변수{#cgi-parameters}

## CGI 매개 변수 {#concept_F395999090FE4926B38BC73D5E612800}

## CGI 매개 변수 검색 {#reference_DA27A8B0728246DA94994885E1353890}

검색 양식 코드는 사이트의 HTML( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**)을 복사하여 붙여넣을 수 있도록 제공됩니다.

검색 [양식의 HTML 코드 복사를 참조하십시오.](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

검색 양식 자체에 나열되거나 스크립트에서 나열되는 매개 변수를 설정할 수도 있습니다. 아래 나열된 매개 변수 외에 백엔드 검색 매개 변수를 사용하여 검색을 제어할 수도 있습니다.

백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오.

검색 요청은 기본 URL로 구성됩니다. 기본 URL은 고객이 검색하는 계정과 연결된 계정에 대해 원하는 검색 결과를 반환하는 방법을 나타내는 CGI 매개 변수(키-값 쌍) 세트를 나타냅니다.

기본 URL은 특정 계정 및 단계 또는 라이브 환경과 연결됩니다. 계정 관리자에서 기본 URL에 대해 여러 별칭을 요청할 수 있습니다. 예를 들어 Megacorp라는 회사는 계정과 연결된 두 개의 기본 URL을 가질 수 있습니다. `https://search.megacorp.com` 및 `https://stage.megacorp.com`Adobe 이전 URL은 라이브 색인을 검색하고 후자의 URL은 스테이지된 인덱스를 검색합니다.

세 가지 형식의 CGI 매개 변수가 지원됩니다. 기본적으로 계정은 다음 예와 같이 세미콜론을 사용하여 CGI 매개 변수를 구분하도록 구성됩니다.

`https://search.megacorp.com?q=shoes;page=2`

원하는 경우 계정 관리자가 앰퍼샌드를 사용하여 다음 예와 같이 CGI 매개 변수를 구분하도록 계정을 구성할 수 있습니다.

`https://search.megacorp.com?q=shoes&page=2`

다음 예와 같이 슬래시를 구분 문자 대신 사용하고 등호 기호를 사용하는 SEO 형식이라는 세 번째 형식도 지원됩니다. `/`

`https://search.megacorp.com/q/shoes/page/2`

SEO 형식을 사용하여 요청을 보낼 때마다 모든 출력 링크가 동일한 형식으로 반환됩니다.

| 검색 안내 매개 변수 | 예 | 설명 |
|--- |--- |--- |
| q | `q=string` | 검색에 대한 쿼리 문자열을 지정합니다. 이 매개 변수는 `sp_q` 백엔드 검색 매개 변수에 매핑됩니다.  백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| q# | `q#=string` | Faceting(주어진 필드 내에서 검색)은 q 및 x 매개 변수에 번호를 매기는 방식으로 수행됩니다.  q 매개 변수는 패싯에서 검색하는 용어를 해당 번호가 매겨진 x 매개 변수로 나타냅니다.<br>예를 들어, 크기와 색상이라는 두 개의 패싯이 있는 경우 q1=small;x1=size;q2=red;x2=color와 같은 것을 사용할 수 있습니다.  이 매개 변수는 `sp_q_exact_#` 백엔드 검색 매개 변수에 매핑됩니다.  <br>백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| x# | `q#=string` | Faceting(주어진 필드 내에서 검색)은 q 및 x 매개 변수에 번호를 매기는 방식으로 수행됩니다.  q 매개 변수는 패싯에서 검색하는 용어를 해당 번호가 매겨진 x 매개 변수로 나타냅니다. <br>예를 들어, 크기와 색상이라는 두 개의 패싯이 있는 경우 q1=small;x1=size;q2=red;x2=color와 같은 것을 사용할 수 있습니다.  이 매개 변수는 `sp_x_#` 백엔드 검색 매개 변수에 매핑됩니다.  <br>백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| 컬렉션 | `collection=string` | 검색에 사용할 컬렉션을 지정합니다.  이 매개 변수는 `sp_k` 백엔드 검색 매개 변수에 매핑됩니다.  백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| count | `count=number` | 표시되는 결과의 총 개수를 지정합니다.  기본값은 [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]에서 정의됩니다..  이 매개 변수는 `sp_c` 백엔드 검색 매개 변수에 매핑됩니다.  백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| page | `page=number` | 반환되는 결과 페이지를 지정합니다. |
| 순위 | `rank=field` | 정적 등급에 사용할 등급 필드를 지정합니다.  필드는 0보다 큰 연관성이 있는 등급 유형의 필드여야 합니다.  이 매개 변수는 `sp_sr` 백엔드 매개 변수에 매핑됩니다.  백엔드 [검색 CGI 매개 변수를](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오. |
| 정렬 | `sort=number` | 정렬 순서를 지정합니다.<br>&quot;0&quot;은 기본값이며 관련 점수에 따라 정렬합니다.&quot;1&quot;은 날짜별로 정렬합니다.&quot;-1&quot;은 정렬되지 않습니다.  사용자는 `sp_s` 매개 변수 값에 대한 필드 이름을 지정할 수 있습니다.  예를 들어 제목 필드에 포함된 값에 따라 결과를 `sp_s=title` 정렬합니다. 매개 변수 값에 필드 이름을 사용하면 해당 필드별로 결과가 정렬된 다음 관련성별로 하위 정렬됩니다. ` sp_s `  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. 정의 페이지에서 특정 필드 이름을 [!UICONTROL Add New Field ] 클릭하거나 [!UICONTROL Edit ] 클릭합니다. 드롭다운 [!UICONTROL Sorting ] 목록에서 [!UICONTROL Ascending ] 또는 을 선택합니다 [!UICONTROL Descending ]. 이 매개 변수는 `sp_s` 백엔드 검색 매개 변수에 매핑됩니다. <br>백엔드 [검색 CGI 매개 변수를]참조하십시오.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98CA9DF7918E8) |

## 백엔드 검색 CGI 매개 변수 {#reference_582E85C3886740C98FE88CA9DF7918E8}

일반적으로 고객은 Guided Search라는 프레젠테이션 레이어와 상호 작용합니다. 하지만 이 페이지에 설명된 CGI 매개 변수를 사용하여 검색 안내 레이어를 건너뛰고 백엔드 코어 검색과 직접 상호 작용할 수 있습니다.

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
   <td colname="col3"> <p> <span class="codeph"> sp_a= 문자열 </span> </p> </td> 
   <td colname="col4"> <p>계정 번호 문자열을 지정합니다. 이 매개 변수는 필수이며 올바른 계정 번호 문자열이어야 합니다. 설정 &gt; 계정 옵션 &gt; 계정 설정에서 <span class="uicontrol"> 계정 번호 문자열을 찾을 수 </span><span class="uicontrol"> 있습니다 </span> <span class="uicontrol"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 또는 1 </span> </p> </td> 
   <td colname="col4"> <p>sp_advanced=1 <span class="codeph"> 이 쿼리와 함께 제출되면 </span> &lt;search-if-advanced&gt; <span class="codeph"> 태그와 검색 템플릿의 </span> &lt;/search-if-advanced&gt; <span class="codeph"> </span> 태그 사이의 모든 코드가 검색 양식에 사용됩니다. &lt;search-if-not-advanced&gt; <span class="codeph"> </span> 태그와 <span class="codeph"> &lt;/search-if-not-advanced&gt; </span> 태그 사이의 모든 코드는 무시됩니다. sp_advanced=0 <span class="codeph"> </span> (또는 다른 값)이 제출되면 &lt;search-if-advanced&gt; 템플릿 블록이 무시되고 &lt;search-if-not-advanced&gt; 템플릿 블록이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= 숫자 </span> </p> </td> 
   <td colname="col4"> <p>표시할 총 결과 수를 지정합니다. 기본값은 10입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>해당 필드에 대한 컨텍스트 정보를 수집합니다. 수집된 정보는 <span class="codeph"> &lt;search-context&gt; </span> 템플릿 태그를 통해 검색 결과로 출력됩니다. The default value is <span class="codeph"> body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= 유형 </span> </p> </td> 
   <td colname="col4"> <p>수행할 날짜 범위 검색 유형을 지정합니다. 유형의 가능한 값은 모두 해당됩니다. 즉, 날짜 범위 검색을 수행하지 않고, custom을 <span class="codeph"> 수행한다는 것을 의미하며, </span> sp_date_date_ <span class="codeph"> specific의 값을 사용하여 날짜를 검색해야 함을 나타냅니다. 이것은 </span>sp_date_date_ <span class="codeph"> specific의 값을 사용해야 한다는 것을 나타냅니다. 즉, 은 sp_date_start_start_Start_Sp의 값을 결정하며, Sp_start_End_Sp의 값을 결정하며, Cue_Cue_Cue_Cend_Cue_Cue의를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를를 </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> End_End_End_End_End_Cue_Cue 검색할 날짜 범위를 결정하는 데 사용됩니다. <span class="codeph"> sp_d </span> 는 검색 양식에 사용자 지정 범위( <span class="codeph"> sp_date_range를 통해)나 특정 시작 및 종료 날짜 범위에 따라 검색하는 옵션이 포함된 경우에만 필요합니다 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>해당 <span class="codeph"> sp_q_# </span> 쿼리에 대해 수행할 날짜 범위 검색 유형을 지정합니다. "#"은 1과 16 사이의 숫자로 대체됩니다(예: <span class="codeph"> sp_d_8 </span>은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_8 </span>). </p> <p>원하는 유형으로 유형을 <span class="codeph"> 설정할 수 있습니다. 즉, 날짜 범위 검색을 수행하지 않습니다. custom은 </span> sp_date_range_# 값이 검색 날짜를 결정하는 데 사용되었음을 나타내고, 구체적인 값을 <span class="codeph"> 나타내는, 즉 </span> sp_date_range_# 값이 사용되었음을 나타내며, 이 값은 SP_q_min_min_day를에, SP_cq에 포함됨을 나타내고, min_cq를를 <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> 를 _ max_q_month, max_year_year_를 사용하여 날짜 범위를 결정해야 합니다. 검색 양식에 사용자 지정 범위( <span class="codeph"> sp_date_range_#)나 특정 시작 및 종료 날짜 </span> 범위에 따라 검색할 수 있는 옵션이 포함된 경우에만 sp_d_# <span class="codeph"> </span>사용이 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>검색에 적용할 사전 정의된 날짜 범위를 지정합니다. 0보다 크거나 같은 값은 오늘 이전에 검색할 일 수를 지정합니다. 예를 들어, "0"의 값은 "today"를, "1"의 값은 "today and yesterday"를, "30"의 값은 "지난 30일 이내"를 지정하는 등의 작업을 지정합니다. </p> <p>0 아래의 값은 다음과 같이 사용자 지정 범위를 지정합니다. </p> <p>-1 = "없음"으로, 날짜 범위를 지정하지 않는 것과 같습니다. </p> <p>-2 = "이번 주"로, 현재 주의 일요일부터 토요일까지 검색합니다. </p> <p>-3 = "지난 주"로, 현재 주 전 주의 일요일부터 토요일까지 검색합니다. </p> <p>-4 = "이번 달"이며 현재 월 내의 날짜를 검색합니다. </p> <p>-5 = "지난 달"이며, 현재 월 이전 달 내의 날짜를 검색합니다. </p> <p>-6 = "올해"로, 현재 연도 내의 날짜를 검색합니다. </p> <p>-7 = "Last year"로 이 값은 현재 연도 이전 년 내의 날짜를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>해당 <span class="codeph"> sp_q_# </span> 쿼리에 적용할 사전 정의된 날짜 범위를 지정합니다. "#"은 1과 16 사이의 숫자로 대체됩니다(예: <span class="codeph"> sp_date_range_8 </span>은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_8 </span>). </p> <p>0보다 크거나 같은 값은 오늘 이전에 검색할 일 수를 지정합니다. 예를 들어 0의 값은 오늘 값을 지정합니다.값 1은 오늘 및 어제 지정합니다.값이 30이면 지난 30일 이내에 지정되는 등 </p> <p>0 아래의 값은 다음과 같이 사용자 지정 범위를 지정합니다. </p> <p>-1 = "없음"으로, 날짜 범위를 지정하지 않는 것과 같습니다. </p> <p>-2 = "이번 주"로, 현재 주의 일요일부터 토요일까지 검색합니다. </p> <p>-3 = "지난 주"로, 현재 주 전 주의 일요일부터 토요일까지 검색합니다. </p> <p>-4 = "이번 달"이며 현재 월 내의 날짜를 검색합니다. </p> <p>-5 = "지난 달"이며, 현재 월 이전 달 내의 날짜를 검색합니다. </p> <p>-6 = "올해"로, 현재 연도 내의 날짜를 검색합니다. </p> <p>-7 = "Last year"로 이 값은 현재 연도 이전 년 내의 날짜를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>검색 결과를 중복 제거할 단일 필드를 지정합니다. 해당 필드의 중복 결과는 모두 검색 결과에서 제거됩니다. 예를 들어 <span class="codeph"> sp_dedupe_field=title에 </span>대해 주어진 제목에 대한 상위 결과만 검색 결과에 표시됩니다(두 개의 결과가 동일한 제목 필드 컨텐츠를 갖지는 않음). 다중 값(목록 허용) 유형 필드의 경우 전체 필드 내용이 비교에 사용됩니다. 필드를 하나만 지정할 수 있습니다. 필드 이름에 "테이블 한정자"를 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= number </span> </p> </td> 
   <td colname="col4"> <p>쿼리 문자열에서 문자 수가 넘는 모든 단어에 대해 자동 와일드카드 확장이 수행되도록 지정합니다. 즉, <span class="codeph"> sp_e=5는 "query" 또는 "number"와 같이 5개 이상의 문자를 포함하는 단어를 와일드카드 문자 '*'로 확장하도록 </span> 지정하여 "query*" 또는 "number*"를 검색하는 것과 동일한 검색을 수행합니다. 문자 수가 적은 단어는 확장되지 않으므로 "word"에 대한 검색에는 자동 와일드카드 확장이 포함되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= number </span> </p> </td> 
   <td colname="col4"> <p>해당 <span class="codeph"> </span> sp_q_# 쿼리 문자열에서 모든 단어에 대해 자동 와일드카드 확장이 수행되도록 지정합니다. 즉, <span class="codeph"> sp_e_2=5는 </span> sp_q_2 쿼리 문자열에서 "query" 또는 "number"와 같은 5개 이상의 문자가 포함된 단어를 와일드카드 문자 ' <span class="codeph"> * </span> <span class="codeph"> </span>'로 확장하도록 지정하여 "query*" 또는 "number*"를 검색하는 것과 동일한 검색을 수행합니다. 문자 수가 적은 단어는 확장되지 않으므로 <span class="codeph"> sp_q_2에서 "word"를 검색해도 자동 와일드카드 확장이 </span> 발생하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>이 세 개의 값은 검색에 대한 종료 날짜 범위를 지정하며 세트로 제공되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f= 문자열 </span> </p> </td> 
   <td colname="col4"> <p>쿼리 매개 변수 문자열( <span class="codeph"> sp_q </span>)의 문자 집합을 지정합니다. 이 문자열은 항상 검색 양식이 포함된 페이지의 문자 집합과 일치해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>지정된 필드로 구성된 논리 데이터 테이블을 정의합니다. 예를 들어 "color", "size" 및 "price" 필드로 구성된 "items"라는 테이블이 다음과 같이 정의됩니다. </p> <p> <span class="codeph"> sp_field_table=items:color,size,price </span> </p> <p>논리 테이블은 "목록 허용"을 선택한 필드와 함께 가장 유용합니다(설정 &gt; 메타데이터 &gt; 정의 아래 <span class="uicontrol"></span> ) <span class="uicontrol"> . </span> <span class="uicontrol"> </span> 필드 이름을 값으로 가져오는 모든 CGI 매개 변수 및 템플릿 태그는 원할 경우, 테이블 이름 다음에 "."를 지정할 수 있습니다. 필드 이름 앞에 추가합니다(예: <span class="codeph"> sp_x_1=tabename.fieldname </span>). </p> <p>예를 들어 "large" 크기의 하나 이상의 "red" 항목이 포함된 문서를 검색하려면 다음을 사용할 수 있습니다. </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> 값 </span></span> </p> </td> 
   <td colname="col4"> <p>보고서를 생성할 때 검색을 무시합니다. </p> <p>이 쿼리를 사용하여 사용자가 생성한 검색이나 관리자가 멤버 센터에서 생성하는 검색과 같은 특정 백엔드 검색을 마스크 처리할 수 있습니다. 최종 사용자는 이러한 유형의 검색을 생성하지 않으므로 다양한 Adobe Search&amp;Promote 보고서에 표시되지 않습니다. </p> <p>유효한 값은 <span class="codeph"> sp_i=1 </span> 및 <span class="codeph"> sp_i=2 </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= 문자열 </span> </p> </td> 
   <td colname="col4"> <p> 검색에 사용할 컬렉션을 지정합니다. 기본값은 컬렉션이 아닙니다. 즉, 검색에는 전체 사이트가 포함되어야 합니다. </p> <p>검색 <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> 양식에서 컬렉션 사용을 </a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= 문자열 </span> </p> </td> 
   <td colname="col4"> <p>쿼리 매개 변수 문자열( <span class="codeph"> sp_q </span>)의 언어를 지정합니다. ISO-639 언어 코드 뒤에 선택적으로 ISO-3166 국가 코드가 따르는 표준 로케일 ID가 <i> 문자열이어야 <span class="codeph"> </span></i> 합니다. 예를 들어, 영어의 경우 "en" 또는 "en_US", 일본어의 경우 "ja" 또는 "ja_JP"입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 또는 1 </span> </p> </td> 
   <td colname="col4"> <p> sp_ <span class="codeph"> literal=1을 </span> 설정하면 쿼리에서 단어를 해석할 수 있는 모든 기능이 일시적으로 비활성화됩니다. 이 매개 변수를 사용하면 동의어, 대체 단어 양식 및 유사 일치와 상관없이 쿼리의 문자 단어만 문서와 일치합니다. </p> <p>sp_literal=0 <span class="codeph"> </span> 은 의미가 없으며, 이 경우 무시됩니다. </p> <p>사전 <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> 정보를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= 번호 </span> </p> </td> 
   <td colname="col4"> <p> 요약이 표시되는지 여부를 지정합니다. 1은 yes, 0은 no입니다. 기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= 숫자 </span> </p> </td> 
   <td colname="col4"> <p> 검색 결과를 시작하는 결과 수를 지정합니다. 기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> 검색 결과가 없는 경우 지정된 URL로 리디렉션할지 여부를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p> 수행할 검색의 기본 유형을 지정합니다. 임의 사용은 쿼리 문자열에서 단어가 들어 있는 문서를 검색하는 <span class="codeph"> </span> 것을 의미합니다. 모두를 사용하면 쿼리 문자열의 모든 단어가 포함된 문서를 검색할 <span class="codeph"> </span> 수 있습니다. 구문의 사용은 쿼리 문자열이 인용된 구문으로 처리되고 모든 사용자 입력 따옴표가 무시됨을 <span class="codeph"> </span> 의미합니다. </p> <p>구문 <span class="codeph"> 및 </span> 모든 <span class="codeph"> </span>경우 검색어 앞에 있는 "+" 및 "-"의 사양이 비활성화되어 해당 문자가 무시됩니다. sp_p가 <span class="codeph"> </span> 없거나 빈 문자열 또는 임의의 문자열로 설정된 경우 표준 "+" 및 "-" 단어 접두사가 허용됩니다. </p> <p>검색에서 더하기("+") 및 빼기("-") 사용에 대한 자세한 내용은 검색 팁 설명을 참조하십시오. </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">검색 정보</a>를 참조하십시오 . </p> <p>sp_p <span class="codeph"> </span> 매개 변수 사용에 대한 예는 샘플 고급 검색 양식을 참조하십시오. </p> <p>고급 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> 검색 양식 샘플링을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p>해당 <span class="codeph"> sp_q_# </span> 쿼리를 사용하여 수행할 기본 검색 유형을 지정합니다. "#"은 1과 16 사이의 숫자로 대체됩니다(예: <span class="codeph"> sp_p_8 </span> 은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_8 </span>). 임의 사용은 쿼리 문자열의 단어가 들어 있는 문서를 반환한다는 <span class="codeph"> </span> 것을 의미합니다. 모두를 사용하면 쿼리 문자열의 모든 단어가 포함된 문서를 <span class="codeph"> </span> 반환합니다. 구문의 사용은 쿼리 문자열을 전체 구문으로 간주하는 <span class="codeph"> </span> 것을 의미합니다(모든 사용자 입력 인용 부호는 무시됨). </p> <p>모든 <span class="codeph"> 또는 </span> 구문을 지정하면 검색어 앞에 더하기 기호 및 빼기 기호가 <span class="codeph"> </span>무시됩니다. sp_p_# <span class="codeph"> 을 생략하거나 빈 문자열 또는 </span> 임의의 문자열로 설정하면 <span class="codeph"> </span>표준 "+" 및 "-" 접두사가 허용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> 적용할 대상 일치 유형을 지정합니다. 정확한 <span class="codeph"> 정확성을 </span> 사용하면 타겟 컨텐츠 내의 쿼리 문자열과 정확히 일치하는 문서에서만 yield target이 일치함을 의미합니다. 단어의 순서가 중요하지 않다는 점을 제외하면 <span class="codeph"> 이와 같은 </span> 의미의 사용은 정확히 일치합니다. 호환을 사용하면 <span class="codeph"> sp_p </span> 매개 변수의 값을 기반으로 대상 일치 유형이 자동으로 <span class="codeph"> </span> 설정됩니다. 이 사용은 <span class="codeph"> sp_p </span> 구문이 <span class="codeph"> 모두 </span> 정확히 사용되고, 그 외의 경우에는 그에 상응하는 구문이 <span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span> 모두 사용된 경우에 사용됩니다. sp_pt의 기본값은 <span class="codeph"> 호환됩니다 </span> <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>해당 <span class="codeph"> sp_q_# </span> 쿼리에 적용할 대상 일치 유형을 지정합니다. "#"은 1과 16 사이의 숫자로 대체됩니다(예: <span class="codeph"> sp_p_8 </span> 은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_8 </span>). 정확한 <span class="codeph"> 정확성을 </span> 사용하면 타겟 컨텐츠 내의 쿼리 문자열과 정확히 일치하는 문서에서만 yield target이 일치함을 의미합니다. 단어의 순서가 중요하지 않다는 점을 제외하고, <span class="codeph"> 이와 </span> 같은 단어의 사용은 <span class="codeph"> 정확한 </span>것과 같습니다. 호환되는 <span class="codeph"> 유형을 사용하면 해당 </span> sp_p_# <span class="codeph"> </span> 매개 변수의 값을 기반으로 대상 일치 유형이 자동으로 설정됩니다. <span class="codeph"> exact </span> 는 <span class="codeph"> sp_p_# </span> 이 모두 또는 구문인 경우 사용되며, 그 외에는 <span class="codeph"> 이에 상응하는 </span> 것이 사용됩니다. sp_pt_#의 기본값은 <span class="codeph"> 호환됩니다 </span> <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= 문자열 </span> </p> </td> 
   <td colname="col4"> <p> 검색에 대한 쿼리 문자열을 지정합니다. 빈 문자열을 사용하면 결과가 표시되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= text </span> </p> </td> 
   <td colname="col4"> <p>이 매개 변수를 사용하면 검색 양식에 여러 쿼리를 만들 수 있습니다. sp_q_# <span class="codeph"> </span> 매개 변수에는 지정된 번호가 지정된 쿼리에 사용할 쿼리 문자열이 포함됩니다. 검색 요청은 최대 16개의 서로 다른 번호가 매겨진 쿼리( <span class="codeph"> sp_q_1 </span> 에서 <span class="codeph"> sp_q_16 </span>)를 참조할 수 있습니다. </p> <p>예를 들어 다음 양식을 제출하면 "great" 및 "books"라는 단어가 포함된 모든 문서가 반환됩니다. </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q _day_#, sp_q _month_#, sp_q _year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= 정수 값 </span> </p> <p> <span class="codeph"> sp_q_month= 정수 값 </span> </p> <p> <span class="codeph"> sp_q_year= 정수 값 </span> </p> <p> <span class="codeph"> sp_q_day_#= 정수 값 </span> </p> <p> <span class="codeph"> sp_q_month_#= 정수 값 </span> </p> <p> <span class="codeph"> sp_q_year_#= 정수 값 </span> </p> </td> 
   <td colname="col4"> <p>이러한 매개 변수는 특정 쿼리의 정확한 날짜를 지정하는 데 사용됩니다. sp_day <span class="codeph"> , </span>sp_q_month <span class="codeph"> 및 </span>sp_q_year <span class="codeph"> 매개 변수가 기본 쿼리( </span> <span class="codeph"> </span>sp_q)에 적용됩니다. </p> <p># <span class="codeph"> 매개 </span>변수는 1과 16 사이의 숫자로 바뀝니다(예: 번호가 매겨진 쿼리 <span class="codeph"> sp_q_6 </span><span class="codeph"> </span>에 적용되는 sp_q_day_6). 기본적으로 모든 날짜는 그리니치 평균 시간을 기준으로 검색됩니다. </p> <p>다음 코드 섹션에서는 "Jan"이라는 이름의 문서에서 "주황색"이라는 단어를 검색할 수 있습니다. PublishDate라는 사용자 정의 필드의 첫 번째, <span class="codeph"> 2000" </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>이러한 매개 변수는 위치를 주 쿼리 또는 번호 매김 쿼리와 연결합니다. sp_q_location의 사용은 기본 쿼리인 <span class="codeph"> sp_q_location_# </span> (여기서 # <span class="codeph"> </span> <span class="codeph"> </span> 는 1-16의 숫자로 대체됨)에 영향을 주므로 지정된 번호가 있는 쿼리에 영향을 줍니다. 이러한 매개 변수는 각 사이트 페이지에 대해 인덱스화된 위치 데이터에 대해 최소 및/또는 최대 근거리 검색을 수행하는 데 사용됩니다. 값의 형식은 해석을 결정합니다. </p> <p>DDD(3자리) 형식의 값은 미국 전화 번호로 해석됩니다.DDDD 또는 DDDDD-DDD 형식의 값은 US zipcode로 해석됩니다.그리고 DD.DDD DDD.DDD 형식의 값은 위도/경도 쌍으로 해석됩니다. 각 값에 대해 기호가 필요합니다. 예를 들어 +38.6317+120.5509는 위도 38.6317, 경도 120.5509를 지정합니다. </p> <p>근접 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 검색 정보를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_related_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_related_distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>이러한 매개 변수는 근접 검색에 적용되는 관련성 계산을 제어합니다. sp_q_max_related_distance <span class="codeph"> 를 사용하면 기본 쿼리인 </span> sp_q_max_related_distance_ <span class="codeph"> #(여기서 # </span> <span class="codeph"> </span> 가 1에서 16까지의 숫자로 대체됨)에 영향을 주고, 지정된 번호가 지정된 쿼리에 영향을 줍니다. </p> <p>sp_q_max_related_distance의 기본값은 100 <span class="codeph"> </span> 입니다. </p> <p>근접 구성 요소에 대한 완벽한 연관성 점수는 0의 거리를 나타냅니다. 근접 구성 요소에 대한 최소 관련성 점수는 지정된 <span class="codeph"> sp_q_max_related_distance_# </span> 값 바로 위의 거리를 나타냅니다. </p> <p>근접 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 검색 정보를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_month, sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_month_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>이러한 매개 변수는 특정 쿼리에 대한 최소 및 최대 날짜 범위를 설정하는 데 사용됩니다. sp_min_day, <span class="codeph"> _q_min_ </span>month, <span class="codeph"> _q_min_ </span>, <span class="codeph"> sp_day_day, </span><span class="codeph"> </span><span class="codeph"> </span><i></i> <span class="codeph"> </span>_q_max_q_max_month, andMax_q max_month, andSp_max_yearSP의 기본 쿼리( sp_q 기본 쿼리)에 매개 변수가 적용됩니다. </p> <p>매개 변수 <span class="codeph"> 이름의 </span>#은 1과 16 사이의 숫자로 바뀝니다(예: <span class="codeph"> sp_q_min_day_6 </span> 은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_6 </span>). </p> <p>최소 날짜, 최대 날짜 또는 최소 및 최대 날짜 모두를 지정하는 것은 합법적입니다. 그러나 지정된 최소 또는 최대 세트의 경우 세 개의 날짜 매개 변수(일, 월 및 년)를 모두 지정해야 합니다. 기본적으로 모든 날짜는 그리니치 평균 시간을 기준으로 검색됩니다. </p> <p>다음 코드 섹션에서는 2000년 1월 1일부터 2000년 12월 31일 사이의 날짜가 있는 문서에서 "주황색"이라는 단어를 검색할 수 <span class="codeph"> 있습니다 </span>. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q _min_#, sp_q _max_#, sp_q _exact_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= 값 </span> </p> <p> <span class="codeph"> sp_q_max= 값 </span> </p> <p> <span class="codeph"> sp_q_min_#= 값 </span> </p> <p> <span class="codeph"> sp_q_max_#= 값 </span> </p> <p> <span class="codeph"> sp_q_exact_#=value </span> </p> </td> 
   <td colname="col4"> <p>이러한 매개 변수는 주 쿼리 또는 번호 매기기에 적용할 최소(및/또는 최대) 값을 지정합니다. sp_q_min, <span class="codeph"> sp_q_max 및 </span>sp_q_exact의 사용은 기본 쿼리( <span class="codeph"> </span><span class="codeph"> </span> <span class="codeph"> </span>sp_q)에 영향을 줍니다. </p> <p>매개 변수 <span class="codeph"> 이름의 </span>#을 1에서 16 사이의 숫자로 바꿉니다(예: <span class="codeph"> sp_q_min_8 </span> 은 번호가 매겨진 쿼리 <span class="codeph"> sp_q_8 </span>에 적용됩니다). </p> <p>sp_q_exact_# <span class="codeph"> 의 사용은 </span> sp_q_min_# <span class="codeph"> 및 </span> sp_q_max_# <span class="codeph"> </span> 를 동일한 값으로 지정하는 축약입니다. sp_q_exact_# <span class="codeph"> 을 지정하면 해당 </span> sp_q_min_# <span class="codeph"> 또는 </span> sp_q_max_# <span class="codeph"> </span> 매개 변수가 모두 무시됩니다. </p> <p>sp_q_min_# <span class="codeph"> , </span>sp_q_max_# <span class="codeph"> 및 </span> sp_q_exact_# <span class="codeph"> </span> 매개 변수는 선택적으로 여러 개의 "|" 구분 값을 지정할 수 있습니다. 예를 들어 "color" 필드 내에서 녹색 또는 빨간색 값이 포함된 문서를 검색하려면 다음을 수행합니다. <span class="codeph"> ...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q_nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 또는 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 또는 0 </span> </p> </td> 
   <td colname="col4"> <p>기본 매개 변수 값은 <span class="codeph"> 0입니다. </span> 즉, 일반 구문 확장이 수행됩니다. </p> <p>해당 검색 쿼리에 대해 <span class="codeph"> 1로 </span> 설정하면 일반 구문 확장이 수행되지 않습니다. </p> <p>sp_q_nocp를 사용하는 <span class="codeph"> 것은 기본 검색 쿼리 매개 변수 </span> sp_q <span class="codeph"> </span>에 영향을 줍니다. 번호가 매겨진 검색 쿼리에 이 매개 변수를 적용하려면 매개 변수 이름의 <span class="codeph"> # </span> 을 해당 번호로 바꿉니다. 예를 들어 <span class="codeph"> sp_q_nocp_8 </span> 은 번호가 매겨진 검색 쿼리 <span class="codeph"> sp_q_8 </span>에 적용됩니다. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q_required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1 또는 0 또는 -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 또는 0 또는 -1 </span> </p> </td> 
   <td colname="col4"> <p>이 매개 변수는 결과 페이지에서 문서를 반환하기 위해 해당 쿼리에서 일치를 (1), 5월 또는 (-1)이 발생하지 않아야 하는지 여부를 결정합니다. </p> <p>sp_q_required의 사용은 기본 쿼리( <span class="codeph"> sp_q </span> <span class="codeph"> </span>)에 영향을 줍니다. </p> <p>번호가 매겨진 쿼리에 적용하려면 매개 변수 이름의 <span class="codeph"> #을 해당 번호로 바꿉니다(예: </span> sp_q_required_8 <span class="codeph"> 은 번호가 매겨진 쿼리 </span> sp_q_8 <span class="codeph"> </span>에 적용). 매개 변수의 기본값은 1(일치해야 함)입니다. </p> <p>사용자 정의 "platform" 필드에 "calc"라는 단어를 포함하지만 HTML에 "mac", "win" 또는 "all"을 포함하지 않는 문서를 검색하려면 HTML 검색 양식에 다음 줄이 포함될 수 있습니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>검색 결과가 하나만 있는 경우 검색 결과 URL로 리디렉션할지 여부를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_referrer </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_referrer= url </span> </p> </td> 
   <td colname="col4"> <p>검색에 대한 레퍼러 URL을 지정합니다. 검색 결과가 검색 양식과 동일한 사이트로 다시 연결되는 검색 다시 작성 규칙에 유용합니다. </p> <p>기본값은 브라우저가 제공하는 표준 CGI HTTP_REFERRER 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> 필드 </span>:연관성 <span class="varname"> </span></span> </p> </td> 
   <td colname="col4"> <p>필드 이름당 검색 시간, 연관성 컨트롤을 선택적으로 사용할 수 있습니다. 매개 변수 <span class="codeph"> 이름의 </span> 로는 "관련성 재정의"를 나타냅니다. 매개 변수는 하나 이상의 필드 이름을 허용하며, 그 다음에 콜론 문자를 사용하고 0-10의 관련성 값을 사용합니다. </p> <p>예를 들어, 고객이 검색을 수행할 때 필드 이름 "body"에 대한 연관성 값을 10으로 설정하려면 다음과 같이 매개 변수가 나타납니다. </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>또는 매개 변수 문자열에서 여러 필드 관련성 무시를 지정하려면 파이프 구분 기호를 사용할 수 있습니다. 예를 들어, 고객이 검색을 수행할 때 필드 이름 "body" 및 "title"에 대한 연관성 값을 9로 설정하려면 매개 변수가 다음과 같이 표시됩니다. </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>참고: 연결된 검색에 포함되지 않은 필드를 지정해도 아무런 효과가 없습니다. 예를 들어 <span class="codeph"> sp_ro=title:10 </span>을 설정했지만 <span class="codeph"> 제목 </span> 필드 이름이 검색되지 않으면 <span class="codeph"> </span> sp_ro 매개 변수에 영향을 주지 않습니다. 즉, <span class="codeph"> </span> sp_ro 매개 변수를 사용하여 필드 이름을 지정하면 해당 필드가 자동으로 검색되지 않습니다.대신 필드의 관련 연관성 설정만 무시합니다. </p> </p> <p>미리 <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> 정의된 메타 태그 필드 또는 사용자 정의 메타 태그 필드 편집을 참조하십시오 </a>. </p> <p>쿼리 <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> 정리 규칙 정보를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= number </span> </p> </td> 
   <td colname="col4"> <p>정렬 순서를 지정합니다. 0은 기본값이며 관련성 점수로 정렬하는 수단입니다. 하나는 날짜별로 정렬하는 것을 의미하고 -1은 정렬하지 않는 것을 의미합니다. </p> <p>sp_s <span class="codeph"> </span> 매개 변수의 값에 대한 필드 이름을 지정할 수 있습니다. 예를 들어 <span class="codeph"> sp_s=title은 제목 필드에 포함된 값에 따라 결과를 </span> 정렬합니다. sp_s 매개 변수의 값에 필드 이름을 사용하면 <span class="codeph"> </span> 해당 필드별로 결과가 정렬된 다음 관련성별로 하위 정렬됩니다. </p> <p>참조된 필드 정렬을 [설정] &gt; [메타데이터 설정] &gt; [ <span class="uicontrol"> 내림차순 정의]에서 [오름차순] </span> 또는 [ <span class="uicontrol"> 오름차순]으로 설정하여 이 기능을 활성화할 </span> 수 <span class="uicontrol"> </span> <span class="uicontrol"> </span> <span class="uicontrol"> </span> 있습니다. </p> <p>검색 양식에서 <span class="codeph"> sp_s </span> 매개 변수를 여러 번 설정하여 단일 쿼리에 여러 정렬 필드를 할당할 수도 있습니다. 다음 템플릿 줄은 검색 결과를 먼저 아티스트 이름별로 정렬한 다음 앨범 이름별로 정렬한 다음 트랙 이름별로 정렬합니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>또한 필드 이름 앞에 테이블 이름 한정자를 지정하여 테이블 일치 필드 데이터를 정렬할 수 있습니다(예: items.price). 테이블 일치에 대한 자세한 내용은 <span class="codeph"> sp_field_table </span> 매개 변수를 참조하십시오. </p> <p>근접 방식으로 검색하는 경우 "근접 출력 필드"를 지정하여 근접 결과에 따라 결과를 정렬할 수 있습니다. </p> <p>근접 <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 검색 정보를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= 필드 </span> </p> </td> 
   <td colname="col4"> <p>정적 등급에 사용할 등급 필드를 지정합니다. 필드는 0보다 큰 연관성이 있는 등급 유형의 필드여야 합니다. 쿼리에 <span class="codeph"> </span> sp_sr 매개 변수가 제공되지 않으면 등급 유형의 필드가 자동으로 선택됩니다. </p> <p>특정 쿼리에 대한 정적 등급을 비활성화하려면 <span class="codeph"> sp_sr에 대해 NULL 값을 포함하십시오(예: </span> &lt;input type="hidden" name="sp_sr" value=""&gt; <span class="codeph"> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= 문자열 </span> </p> </td> 
   <td colname="col4"> <p>검색 템플릿의 <span class="codeph"> &lt;search-field-value-list&gt; </span> 태그와 함께 사용할 필드의 이름을 지정합니다. </p> <p>여러 <span class="codeph"> sp_sfvl_field </span> 매개 변수를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;integer_value&gt; </span></span> </p> </td> 
   <td colname="col4"> <p> 
     <!--NEW 2/2/2014-->이 검색에 대해 최대 <span class="codeph"> &lt;integer_value&gt; <span class="varname"></span> search-field-value-list </span> dynamic-facet 필드를 <span class="codeph"> </span> 요청합니다. </p> <p>기본값은 0입니다. 허용되는 최대 값은 주어진 인덱스에 대해 정의된 동적 패싯 필드, 동적 패싯 필드 필드 수입니다. 0보다 작은 정수 값은 0으로 처리됩니다. dynamic-facet-field-count 위에 지정된 정수 값은 <span class="codeph"> dynamic-facet-field-count </span> <span class="codeph"> </span>로 제한됩니다. 정수가 아닌 값은 무시됩니다.이 값은 기본값으로 처리됩니다. </p> <p>지정된 슬라이스의 검색은 이 슬라이스의 <span class="codeph"> 동적 패싯 필드 수 </span> 값의 최대 허용 <span class="codeph"> sp_sfvl_df_count </span> 값으로 제한됩니다. 슬라이스 결과를 병합할 때 <span class="codeph"> sp_sfvl_df_count의 유효 최대 </span> 값은 모든 슬라이스에 걸쳐 실제 <span class="codeph"> sp_sfvl_df_count </span> 의 최대 최대값입니다. </p> <p>동적 <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 패싯 구성을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> &gt; </span>|... </p> </td> 
   <td colname="col4"> <p> 이 검색에 대해 제외할 특정 동적 패싯 필드 목록을 지정합니다. </p> <p>기본적으로 모든 동적 패싯 필드가 고려됩니다. </p> <p>동적 <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 패싯 구성을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> field_name </span>&gt;[|&lt; <span class="varname"> field_name </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> 검색 결과에 포함할 특정 동적 패싯 필드 목록을 지정합니다. </p> <p> <p>참고: sp_ <span class="codeph"> sfvl_df_count </span> 매개 변수는 <span class="codeph"> sp_sfvl_df_include를 통해 지정된 모든 것을 포함하여 반환할 동적 패싯 필드의 총 수를 </span>결정합니다. 즉, <span class="codeph"> sp_sfvl_df_include를 사용하면 반환된 동적 패싯 필드의 총 수가 </span> sp_sfvl_df_count를 초과할 <span class="codeph"> </span>수 없습니다. </p> </p> <p>동적 <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> 패싯 구성을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 또는 1 </span> </p> </td> 
   <td colname="col4"> <p>sp_staged=1 <span class="codeph"> </span> 이 쿼리와 함께 제출되면 실행되는 쿼리는 스테이지된 검색입니다. </p> <p>단계 검색은 인덱스 및 템플릿을 포함하여 현재 스테이징된 모든 구성 요소를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day, sp_start_month, sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= number </span> </p> <p> <span class="codeph"> sp_start_month= number </span> </p> <p> <span class="codeph"> sp_start_year= number </span> </p> </td> 
   <td colname="col4"> <p>이 세 개의 값은 검색에 대한 시작 날짜 범위를 지정하고 세트로 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_추천_q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_suggest_q= number </span> </p> </td> 
   <td colname="col4"> <p>sp_suggest_q <span class="codeph"> 매개 변수는 </span> sp_q[_#] <span class="codeph"> </span> 매개 변수를 확인하여 제안 서비스와 함께 사용할 수 있습니다. </p> <p>sp_suggest_q의 기본값은 <span class="codeph"> 0입니다. 즉, 검색 엔진은 </span> sp_q <span class="codeph"> </span> 값을 사용하여 제안을 결정합니다. </p> <p>sp_ <span class="codeph"> suggest_q=1을 </span> 설정하여 <span class="codeph"> sp_q_1 값을 </span> 사용하여 제안 등을 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= 문자열 </span> </p> </td> 
   <td colname="col4"> <p>사용할 전송 템플릿을 지정합니다. </p> <p>이 매개 변수는 검색 계정의 각 영역에 대해 다른 검색 전송 템플릿을 사용하여 웹 사이트 전체에서 핵심 검색 결과의 모양을 제어하려는 경우 유용합니다. </p> <p>기본 전송 템플릿은 "검색"입니다. </p> <p>웹 <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> 사이트에 대한 여러 전송 템플릿 관리를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 또는 1 </span> </p> </td> 
   <td colname="col4"> <p>sp_stage=1 <span class="codeph"> 로 설정되면 시뮬레이터에서 핵심 검색 추적 기능을 </span>활성화합니다. </p> <p>시뮬레이터 <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> 정보를 참조하십시오 </a>. </p> <p> <p>참고: 이 매개 변수를 지정하지 않으면 핵심 검색에서 추적 정보를 수집하지 않으며 관련 핵심 검색 템플릿 태그에는 출력이 없습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>이 특정 쿼리에 대해 유사한 일치를 활성화하거나 비활성화하도록 지정합니다. </p> <p>'Exact'에 대한 sp_w_control은 무시됩니다. 유사한 검색은 비활성화되어 있습니다. </p><p>'동일함'에 대한 sp_w_control이 무시되었습니다. 유사 일치 사용</p><p>다른 항목에 대한 sp_w_control은 1입니다. 유사한 검색은 비활성화되어 있습니다. </p><p>Anything에 대한 sp_w_control은 다른 어떤 것입니다. 유사 일치 기능이 활성화되었습니다. </p>sp_w_control <span class="codeph"> </span> 매개 변수를 사용하면 사운드 유사 일치를 최종 사용자가 제어할 수 있도록 부정적인 글자나 긍정적으로 쓰인 확인란을 만들 수 있습니다. </p> <p>sp_w_control=0 <span class="codeph"> 을 사용하는 경우 다음 예와 같이 </span> sp_w <span class="codeph"> </span> 매개 변수를 설정하는 데 부정적인 내용의 확인란이 사용됩니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_control=1을 <span class="codeph"> 사용하는 경우 </span> sp_w <span class="codeph"> </span> 매개 변수를 다음과 같이 설정하는 데 긍정적인 내용의 확인란이 사용됩니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>sp_w_control 및 <span class="codeph"> sp_w </span> <span class="codeph"> </span> 매개 변수 사용에 대한 자세한 예는 샘플 고급 검색 양식을 참조하십시오. </p> <p>고급 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> 검색 양식 샘플링을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= 필드 </span> </p> </td> 
   <td colname="col4"> <p>쿼리 문자열을 검색할 필드를 지정합니다. 임의)는 모든 필드를 검색한다는 의미입니다. title은 검색 전용 제목 필드를 의미합니다. desc는 검색만 문서 설명 필드를 의미합니다. 키는 문서 키워드만 검색함을 의미합니다. body는 본문 텍스트만 검색함을 의미합니다. alt는 대체 텍스트만 검색함을 의미합니다. url은 URL 값만 검색함을 의미합니다. target은 검색 대상 키워드만 의미합니다. 이러한 경우 해당 <span class="codeph"> sp_q 매개 변수 내의 "text:", "desc:", "keys:", "body:", "alt:", "url:" 및 "target:" 필드 접두사는 </span> 무시됩니다. sp_x가 <span class="codeph"> </span> 없거나 빈 문자열 또는 임의의 문자열로 설정된 경우 표준 사용자 필드 접두사가 허용됩니다. 필드 접두사에 대한 자세한 내용은 검색 팁 설명을 참조하십시오. </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">검색 정보</a>를 참조하십시오 . </p> <p>sp_x 매개 변수를 사용하는 예제는 <span class="codeph"> 고급 검색 양식 </span> 설명 샘플을 참조하십시오. </p> <p>고급 <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> 검색 양식 샘플링을 참조하십시오 </a>. </p> <p>[옵션] &gt; [메타데이터 정의]에서 [ <span class="uicontrol"> 기본적으로 검색]으로 설정된 모든 필드를 검색할 수 있습니다. [옵션] </span> &gt; [ <span class="uicontrol"> 메타데이터 정의]에서 sp_ </span> <span class="uicontrol"> </span> <span class="uicontrol"> </span> <span class="codeph"> </span>x=any를 설정하는 쿼리를 만들 수 있습니다. 사전 및 사용자 정의 필드 모두 <span class="codeph"> sp_x </span> 매개 변수의 값으로 사용할 수 있습니다. </p> <p>또한 <span class="codeph"> sp_x </span> 매개 변수를 여러 번 설정하여 단일 쿼리에 여러 필드를 할당할 수도 있습니다. 다음 템플릿 줄을 사용하면 "Great Books"에 대해 "title"과 "author" 필드를 모두 쿼리할 수 있습니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= field-name </span> </p> </td> 
   <td colname="col4"> <p>이 매개 변수는 해당 <span class="codeph"> sp_q_# </span> 쿼리에서 검색할 필드를 지정합니다. # <span class="codeph"> 는 1~16 사이의 숫자(예: <span class="codeph"> sp_x_8 </span> </span> <span class="codeph"> </span>)로 바뀝니다. 필드 이름은 사전 또는 사용자 정의 필드입니다. </p> <p>특정 번호가 있는 쿼리에 대해 <span class="codeph"> _x_# 매개 변수가 제공되지 않으면 [설정] &gt; [메타데이터 검색]에 설정된 </span> 기본 검색으로 정의된 모든 필드가 해당 쿼리에 의해 검색되는 SP <span class="uicontrol"> 의 [기본 설정] &gt; [메타데이터 검색됨]에 </span> <span class="uicontrol"> </span> <span class="uicontrol"> </span> <span class="uicontrol"> </span> 설정되어 있습니다. </p> <p>예를 들어, 다음 양식을 제출하면 "작성" 필드에 "Fitzgerald"라는 단어가 포함된 모든 문서가 반환됩니다. </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>단일 검색 요청에서 동일한 <span class="codeph"> sp_x </span> 또는 <span class="codeph"> sp_x_# </span> 매개 변수의 인스턴스를 두 개 이상 제공하여 여러 필드 이름을 특정 쿼리 또는 숫자 쿼리와 연결할 수 있습니다. </p> <p>예를 들어 "body" 필드와 "keys" 필드 모두에서 "flower"라는 단어를 검색하려면 다음 정보가 포함된 검색 양식을 만들 수 있습니다. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 백엔드 검색 CGI 매개 변수 사용의 일반적인 예 {#section_260012BBC2514CC9A8E02E53DE8B41EE}

다음 링크는 검색 쿼리로 &quot;음악&quot;을 사용하여 검색을 시작하고 모든 기본 매개 변수를 사용합니다. URL은 가독성을 위해 두 줄로 분할됩니다. HTML에서 이 링크는 모두 한 줄에 있어야 합니다.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

동일한 기능은 일반적으로 양식에 정의되어 있습니다.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

일반적으로 검색을 시작할 때 기본 매개 변수를 사용해야 합니다. 이렇게 하면 첫 번째 페이지가 표시되고 연관성을 기준으로 정렬되며 고객이 다른 페이지와 옵션을 선택할 수 있습니다. 사이트의 검색 양식에 컬렉션에 대한 옵션이 포함되어 있는 경우 컬렉션 이름을 매개 변수로 전달합니다.

## 백엔드 검색 CGI 매개 변수 사용에 대한 자세한 예 {#section_5FA3C620D5124FB2AB28857F8D8473F6}

다음 양식 쿼리는 결과부터 시작하는 `25` 결과를 표시합니다 `10`. 요약이 표시되지 않고 정렬 순서는 날짜별로 지정되며 이름이 지정된 컬렉션이 `support` 사용됩니다. 지난 30일 이내에 발급된 문서만 반환됩니다.

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

