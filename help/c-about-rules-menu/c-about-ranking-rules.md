---
description: 등급 규칙을 사용하여 포함된 메타 태그 컨텐츠 및 관련 Adobe Analytics 지표를 기반으로 고객의 검색 결과의 상대적 위치 또는 등급을 제어할 수 있습니다.
seo-description: 등급 규칙을 사용하여 포함된 메타 태그 컨텐츠 및 관련 Adobe Analytics 지표를 기반으로 고객의 검색 결과의 상대적 위치 또는 등급을 제어할 수 있습니다.
seo-title: 등급 규칙 정보
solution: Target
subtopic: Ranking Rules
title: 등급 규칙 정보
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: f4f69e6bdb37fb39045f8f25cffa4bf616834e54

---


# 등급 규칙 정보{#about-ranking-rules}

등급 규칙을 사용하여 포함된 메타 태그 컨텐츠 및 관련 Adobe Analytics 지표를 기반으로 고객의 검색 결과의 상대적 위치 또는 등급을 제어할 수 있습니다.

## 등급 규칙 사용 {#concept_F555C076759B4E81B925441CFE707397}

각 문서의 컨텐츠를 기반으로 검색 결과 내의 문서의 상대적 배치에 영향을 줄 등급 규칙을 정의합니다. 메타 태그 컨텐츠, Adobe Analytics 지표(계정이 Adobe Analytics와 작동하도록 구성된 경우) 또는 Adobe Analytics HBX 지표(계정이 Adobe Analytics HBX와 작동하도록 구성된 경우)를 기반으로 등급 규칙을 설정할 수 있습니다.

특정 브랜드 이름이나 가격과 같은 원하는 특성을 가진 메타 태그가 포함된 웹 페이지나 고유 뷰어와 같은 Adobe Analytics 주요 성능 지표가 있는 웹 페이지를 설정하여 그렇지 않은 웹 페이지보다 순위가 더 높은 웹 페이지를 표시할 수 있습니다. 등급 규칙을 추가하거나 편집한 다음 웹 사이트를 다시 색인화하여 &quot;바람직한&quot; 특성을 손쉽게 업데이트할 수 있습니다.

&quot;등급&quot; 유형의 메타 태그가 두 개 이상 정의된 경우, 다양한 등급 필드를 계산하는 데 사용할 별도의 규칙 모음을 만들 수 있습니다. 등급 규칙 그룹을 추가한 다음 정의된 등급 필드 중 하나에 할당할 수 있습니다. 규칙 그룹에는 일반적으로 하나 이상의 규칙 정의가 포함되지만, 다른 규칙 그룹을 참조할 수도 있으므로, 여러 등급을 계산하는 동안 공유되는 하나 이상의 공통으로 사용되는 규칙 그룹을 만들 수 있습니다.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.

긍정적인 등급 값은 검색 결과를 위쪽으로 올립니다.음수 등급 값은 검색 결과의 맨 아래에 대한 검색 결과를 나타냅니다. 등급 값에 대한 표준 범위는 검색 결과 내의 최대 판촉 행사인 1.0이고, 최대 강등은 -1.0입니다. 메타데이터 정의에서 등급 필드를 편집하여 이 범위를 사용자 지정할 수 있지만 일반적으로 이러한 유형의 사용자 지정은 필요하지 않습니다.

정의 [정보를 참조하십시오](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

설정 > 메타데이터 > 정의 아래에 둘 이상의 등급 필드를 정의한 경우 각 등급 필드에 대해 하나씩, 등급 규칙 세트를 추가로 만들 수 있습니다. 등급 필드와 직접 연결되지 않고 등급 규칙 세트를 추가로 정의할 수 있습니다. 이러한 유연성을 통해 하나 이상의 등급 값 계산에 공유할 수 있는 공통 규칙 세트를 만들 수 있습니다.

**중요**:등급 규칙을 사용하려면 먼저 완료해야 하는 몇 가지 계정 구성 단계가 있습니다.

등급 [구성을 참조하십시오.](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## 등급 구성 {#task_4CEBC13925B047FC95BDC217B48089C5}

등급 규칙을 사용하려면 먼저 완료해야 하는 몇 가지 계정 구성 단계가 있습니다.

**등급을 구성하려면**

1. 다음 중에서 선택합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>작업 </p> </th> 
      <th colname="col2" class="entry"> <p>구성 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>메타 태그를 기반으로 하는 등급 규칙을 만들려면 </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> 제품 메뉴에서 설정 &gt; <span class="uicontrol"> 메타데이터 </span> &gt; <span class="uicontrol"> 정의를 </span> 클릭합니다 <span class="uicontrol"></span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> 정의 페이지에서 새 필드 <span class="uicontrol"> 추가를 클릭합니다 </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> 필드 추가 페이지의 필드 이름 <span class="uicontrol"></span> 텍스트 필드에 
      <userinput>
        순위 
      </userinput>;메타 <span class="uicontrol"> 태그 이름 </span> 텍스트 필드에 
      <userinput>
        순위 
      </userinput>;데이터 <span class="uicontrol"> 유형 </span> 드롭다운 목록에서 등급을 <span class="uicontrol"> 선택합니다 </span> 다른 모든 필드 옵션은 그대로 두십시오. <p>백엔드 검색 CGI 매개 변수의 쿼리 매개 변수 <span class="codeph"> sp_sr </span> 을 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 참조하십시오 </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE"><span class="uicontrol">추가를 클릭합니다 </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 지표를 기반으로 하는 등급 규칙을 만들려면 </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> 사이트 검색/머천다이징 내에서 Adobe Analytics 인증을 설정해야 합니다. <p>Adobe <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Analytics 지표 인증 설정을 </a>참조하십시오. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> 사용 가능한 보고서 세트를 선택하고 추가합니다. <p>Adobe <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Analytics 보고서 세트 추가를 </a>참조하십시오. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> 새 등급 규칙 만들기에 사용할 수 있도록 하려는 Adobe Analytics 지표 목록을 구성합니다. <p>보고서 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> 세트의 Adobe Analytics 지표 편집을 참조하십시오 </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> 웹 사이트 페이지에 대한 초기 Adobe Analytics 지표를 로드합니다. <p>Adobe <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Analytics 데이터 로드를 참조하십시오 </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 등급 규칙을 하나 이상 추가합니다.

   등급 [규칙](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)추가를 참조하십시오.

1. 을 **[!UICONTROL regenerate your staged site index]** 클릭하여 웹 사이트의 전체 다시 색인을 수행합니다( **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.
1. > > > 의 등급 열에서 값을 확인하여 등급 규칙이 올바르게 적용되었는지 **[!UICONTROL Settings]** **[!UICONTROL Metadata]** **[!UICONTROL Definitions]** 확인합니다.

## 연령별 등급 문서 정보 {#topic_770815CF1B2A491F83FF765871B6F1B8}

기하급수적인 감소 기능을 사용하여 HTML 문서의 등급을 해당 페이지별로 지정할 수 있습니다. 감소율은 선택된 반감량 상수로 지정되며 값이 초기 값의 1/2로 떨어지기 전에 경과해야 하는 시간입니다.

연령 등급은 다음 두 방정식을 기반으로 합니다.

`K = -ln(2) / H`

`RANK = e^(K * T)`

변수 `H` 및 `T` 은 다음 함수에 대한 입력입니다.원하는 반수명 `H` 기간이며, `T` 이 문서의 나이는 초 단위로 표시됩니다. `K` 은 계산된 반감이며, `RANK` 이것은 지정된 연령 값의 지수 감소입니다. 결과 값은 0부터 1까지입니다. 최근 문서는 이전 문서와 비교하여 1에 가까운 등급 값을 가집니다. 이론적으로, 문서는 0 값에 도달하지 않아야 하지만 라운딩 오류는 0이 될 수 있습니다.

## 연령 순위 사용 요구 사항 {#section_D716507D589442C6B7848892BD28F966}

* 등급 지정을 위해 계정을 이미 올바르게 구성해야 합니다. 구성되어 있지 않으면 등급 [구성을](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)참조하십시오.
* HTML 문서에는 생년월일, 또는 시작일을 나타내는 HTML 메타 태그 필드 또는 기타 의미 있는 날짜 값이 있어야 합니다.
* 등급 규칙 추가 또는 `search_get_age_rank()`편집 페이지에 지정된 특수 내장 함수를 사용하여 문서의 연령 등급을 계산합니다. 다음 섹션에서는 연령 등급 기능의 일반적인 사용에 대해 자세히 설명합니다. 연령 순위 기능을 보여주는 예도 제공됩니다.

## 등급 규칙 추가 페이지 또는 등급 규칙 편집 페이지에서 search_get_age_rank() 사용 {#section_34BC5276F2AB4419AD92872A397CA0AF}

다음과 `search_get_age_rank()` 같이 지정합니다.

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* 생년월일 - 파일의 생년월일 또는 시작 날짜는 필드의 날짜 형식에 따라 날짜 형식의 문자열이어야 합니다. 이 날짜 형식 문자열은 에서와 같이 필드 참조여야 합니다 `{field_name}`.
* Half_Life - 반올림은 값이 초기 값의 1/2로 떨어지기 전에 경과해야 하는 시간입니다. 이 값은 일 수로 표현되며 정수 또는 부동 소수점 숫자입니다.
* Default_Rank - 기본 등급은 생년월일이 유효하지 않거나 날짜가 미래 상태인 경우 안전점으로 사용됩니다. 연결된 메타데이터 필드에도 유효한 기본값이 있으면 이 기본값을 사용할 수 없습니다. 이 값은 부동 소수점 숫자 또는 정수입니다. 기본값이 사용되는 문제가 발생하면 아래를 참조하십시오.

등급 [규칙](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)추가를 참조하십시오.

See [Editing a ranking rule](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**예**

다음 예제에서는

`search_get_age_rank({birthdate}#28#0.20)`

문서 `birthdate` 필드에 포함된 날짜가 타임스탬프로 전달됩니다. 반수명은 28일입니다. 날짜가 잘못된 경우 기본 등급 값은 0.20입니다.

등급 규칙 [추가의 옵션 테이블을](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)참조하십시오.

등급 규칙 추가 페이지 또는 등급 규칙 편집 페이지의 값/등급 섹션에서 사용자 지정 규칙에만 사용할 수 `search_get_age_rank` 있습니다. 따라서 값/등급 **드롭다운** 목록에서 사용자 지정을 선택해야 합니다. 규칙이 연령 등급 함수를 사용할 경우 규칙의 값 부분에 공백이 허용되지 않습니다. 함수 인수나 함수 사이에 공백이 없어야 합니다. 그리고 수학적 연산자나 조건부 연산자 사이에는 공백이 없습니다.

다음은 값/등급 규칙의 예입니다. 텍스트 필드와 관련된 규칙입니다.

`regexp .* search_get_age_rank({other_field}#365#0.20)`

이 예에서는 날짜 값이 `other_field` 포함되어 있다고 가정합니다. 이 필드 자체가 날짜 유형 필드가 아닌 경우 이 값은 사전 정의된 날짜 필드와 연결된 날짜 형식을 사용하여 해석됩니다. 그렇지 않으면 이 필드의 날짜 형식이 사용됩니다. 이 값/등급 항목은 문서의 필드, 규칙의 데이터 소스가 식별할 때마다, 비어 있지 않고, 함수의 반환 값(0부터 1까지)이 지정된 등급입니다.

숫자 필드와 연결된 규칙의 경우, 특히 날짜 필드는 다음과 같습니다.

`9999999999 search_get_age_rank({other_field}#365#0.20)`

각 문서가 처리되면 필드의 날짜 형식 정의를 사용하여 의 값이 Unix &quot;epoch&quot; 양식으로 `other_field` 변환됩니다. 이 값은 `search_get_age_rank()` 호출에 사용됩니다. 모든 &quot;epoch&quot; 값이 999999999999(적어도 현재는) 미만이므로, 규칙은 함수의 반환 값(0~1)을 등급으로 제공합니다.

앞의 두 가지 예에서, 일반적으로 규칙의 데이터 소스가 `search_get_age_rank()` 함수에서 사용되는 필드와 동일한 필드입니다( `other_field` 이 경우).

## 연령 등급을 등급 규칙에 통합하는 예 {#section_A86D909687CC45E19D4EA7A4A9283F28}

다음은 연령 등급을 등급 규칙에 통합하는 방법의 예입니다. 이 예에서는 연령 등급 함수의 원시 결과와 등급 규칙의 결과를 보여줍니다. 이 예에서는 다음을 가정합니다.

* 크롤링되는 웹 페이지에는 &quot;생년월일&quot;이라는 HTML 메타 태그가 있습니다. 이 태그의 내용은 문서와 관련된 타임스탬프입니다.
* 메타데이터 정의에는 생년월일 태그에 대해 정의된 메타데이터 필드가 있습니다. 이 필드는 &quot;날짜&quot; 유형으로 설정됩니다.

**등급 규칙**

새 [메타 태그 필드](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)추가를 참조하십시오.

이제 새 등급 규칙을 추가합니다. 이 규칙은 문서에서 &quot;생년월일&quot; 필드를 사용하도록 정의됩니다. 다음과 같은 속성 세트로 새 등급 규칙이 추가됩니다.

* 데이터 소스 유형:메타 태그
* 데이터 소스 이름:생년월일
* 가중치/조건:10 - 최대 중요도
* 값/등급:99999999999 search_get_age_rank({생년월일}#14#0.10)
* 기본 등급:-1

이 규칙은 몇 가지 일을 합니다. 규칙의 가중치는 10으로 설정됩니다. 등급 값은 0부터 1까지의 값인 연령 등급 함수의 결과일 뿐입니다. 와 함께 공백을 사용할 수 `search_get_age_rank()`없습니다. 또한 필드 &quot;생년월일&quot;이 중괄호로 묶여 있습니다. 마지막으로 이 규칙을 저장할 때 값/등급 정의의 쉼표는 `#` 문자로 대체됩니다.이 동작은 정상입니다.

**결과 보기**

데이터 보기 기능을 사용하여 연령 등급 함수의 결과를 신속하게 확인할 수 있습니다. 적절한 메타데이터 필드를 추가합니다. 이 예제에서 `age_val` 와 `myrank` 는 데이터 보기에 추가해야 하는 두 개의 메타데이터 필드입니다. 이 `myrank` 필드는 연령 등급이 등급 값에 미치는 영향을 보여줍니다. 이 `age_val` 필드는 해당 문서의 지수 감소 기능의 원시 출력을 보여줍니다.

## 기본값 {#section_CB109EF78F914E92955D512ACFC3310E}

다음은 함수와 관련된 세 가지 기본 값입니다 `search_get_age_rank()`.

* 함수 자체에 입력할 수 있는 `search_get_age_rank()` 기본값.
* 등급 규칙의 기본 등급 값입니다.
* 메타데이터 정의의 기본값.

오류가 발생하는 위치에 따라 다른 기본값을 얻을 수 있습니다.

예를 들어 등급 및 필터링이 제대로 구현된 경우 메타데이터 정의의 기본값은 발생하지 않아야 합니다. 이 기본값은 해당 메타데이터 필드에 대해 유효하거나 알려진 컨텐트가 없을 때의 마지막 리조트 값입니다. 등급 규칙의 기본값은 자체 관련 태그를 참조하고 `search_get_age_rank()` 문서에서 태그가 누락된 경우에 나타날 수 있습니다. 이 경우 이 규칙은 규칙의 기본값으로 바로 이동합니다. 연령 등급 함수가 다른 등급 규칙의 태그를 참조하는 경우, 참조된 태그가 없거나 잘못된 경우 해당 연령 등급 함수에 전달된 기본값이 사용될 수 있습니다.

## 등급 규칙 추가 {#task_A132789FD4E5423DAD090DCDA7311E8A}

각 웹 페이지의 컨텐츠를 기반으로 검색 결과 내의 웹 페이지의 상대적 배치에 영향을 주도록 추가할 [!DNL Ranking Rules] 수 있습니다.

등급 [구성을](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)참조하십시오.

**등급 규칙을 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. (선택 사항) 규칙 그룹을 만들고 그룹에 규칙을 추가한 경우 [!DNL Define Ranking Rules] 페이지의 **[!UICONTROL Select Rule Group]** 드롭다운 목록에서 편집할 규칙이 포함된 규칙 그룹을 선택합니다.

   등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.
1. 페이지에서 을 클릭하여 새 등급 규칙을 [!DNL Define Ranking Rules] **[!UICONTROL Add Rule]** 추가하거나 규칙 세트에 참조를 추가합니다.
1. 페이지에서 원하는 옵션을 [!DNL Add Ranking Rule] 설정합니다. 별표(*)로 표시된 필드는 필수입니다.

   선택하는 데이터 소스 유형은 [!DNL Data Source Name] 드롭다운 목록에서 사용할 수 있는 선택 사항에 영향을 줍니다. 예를 들어 데이터 소스 **[!UICONTROL Meta Tag]** 유형으로 선택한 경우 데이터 소스 이름은 웹 사이트 페이지에서 메타 태그의 이름을 나타냅니다. 이 옵션을 선택한 **[!UICONTROL Adobe Analytics Metric (Number)]**&#x200B;경우 데이터 소스 이름은 사이트 검색/머천다이징의 페이지에 있는 것처럼 보고서 세트에서 선택한 Adobe Analytics 지표 이름 중 하나를 **[!UICONTROL Edit Adobe Analytics Metrics]** 나타냅니다.

   보고서 [세트의 Adobe Analytics 지표 편집을 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>데이터 소스 유형 </p> </td> 
      <td colname="col2"> <p>이 등급 규칙에 대한 입력으로 사용되는 데이터 소스의 특성을 결정합니다. </p> <p>선택할 수 있는 데이터 소스 유형에는 다음이 포함됩니다. 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> 메타 태그 </span> <p> 이 규칙은 웹 사이트 페이지의 명명된 메타 태그 내에 저장되는 숫자 데이터 또는 텍스트 데이터를 기반으로 합니다. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Adobe Analytics 지표(숫자) </span> <p>이 규칙은 사이트 페이지와 연결된 숫자 Adobe Analytics 지표를 기반으로 합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>데이터 소스 이름 </p> </td> 
      <td colname="col2"> <p>메타 태그를 <span class="uicontrol"> 데이터 소스 </span> 유형으로 선택한 경우 웹 사이트의 페이지 내에 있는 메타 태그의 이름입니다. 드롭다운 메뉴의 이름은 설정 &gt; 메타데이터 &gt; 정의에 구성된 정의된 메타데이터 값 목록에서 가져옵니다. </p> <p>새 <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> 메타 태그 필드 추가를 참조하십시오 </a>. </p> <p>Adobe Analytics 지표(숫자)를 데이터 소스 유형으로 선택한 경우, 이것은 Adobe Analytics 지표의 이름입니다. 드롭다운 메뉴의 이름은 설정 &gt; Adobe Analytics &gt; 지표 &gt; 편집에 구성된 사용 가능한 Adobe Analytics 지표가 정의된 목록에서 가져옵니다. </p> <p>보고서 <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> 세트의 Adobe Analytics 지표 편집을 참조하십시오 </a>. </p> <p>선택한 Adobe Analytics 지표 이름이 설정 &gt; 메타데이터 &gt; 정의에 <span class="uicontrol"> 아직 정의되어 있지 않으면 텍스트 </span> 필드와 <span class="uicontrol"> 추가 </span> <span class="uicontrol"> </span>버튼이 표시됩니다. 메타데이터 필드 이름을 입력하고(메타데이터 필드 이름은 20자를 초과할 수 없음) 추가를 <span class="uicontrol"> 클릭합니다 </span>. </p> <p>여러 Adobe Analytics 키가 있는 페이지가 발견되면 제품 페이지에 여러 제품이 표시되는 것과 마찬가지로 복합 구성표는 해당 페이지와 연결된 여러 Adobe Analytics 지표 값을 처리하는 방법을 지정합니다. 다음 중 하나를 선택합니다. </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> 합 </span> <p>지표 값의 합계를 반환합니다. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> 평균 </span> <p>값의 평균(합을 값의 수로 나눈 값)을 반환합니다. </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> 최대 </span> <p>값 중 가장 큰 값을 반환합니다. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> 첫 번째 날 </span> <p>첫 번째 키에 해당하는 값을 반환합니다. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> 마지막 </span> <p>마지막 키에 해당하는 값을 반환합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>가중치/조건 </p> </td> 
      <td colname="col2"> <p>간단한 단일 규칙 가중치 번호나 규칙 가중치 번호 및 테스트 조건 쌍을 이룬 목록을 포함합니다. </p> <p>규칙 가중치 번호는 문서의 전체 등급을 결정할 때 이 등급 규칙이 다른 등급 규칙과 얼마나 중요한지를 나타내는 1-10의 값입니다. 규칙 가중치가 높을수록 중요도가 높아집니다. 가중치가 0이면 규칙이 무시됩니다. </p> <p>규칙 <span class="uicontrol"> 두께/테스트 조건 쌍의 목록을 정의하여 다양한 페이지에 대한 규칙 두께를 사용자 정의하려면 </span> 드롭다운 목록에서 사용자 지정을 선택합니다. 테스트 조건은 데이터 소스 값을 테스트하는 데 사용되는 Perl의 조각이나 사용자 정의 필터 스크립트(예: 다음 예와 같이 가격, 브랜드, 시즌 또는 페이지 보기)에 정의된 전역 변수입니다. 테스트 조건이 "true"로 평가되면 연결된 규칙 가중치 값이 적용됩니다. 테스트 조건이 "false"로 평가되면 목록의 다음 조건이 평가됩니다. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>위의 사용자 지정 생성 두께/조건 예에서 첫 번째 테스트 조건이 "true"로 평가되면 규칙 가중치 0이 적용됩니다. 즉, 가격은 50보다 큰 값을 포함하고 브랜드는 "Kuhl")을 포함합니다. 첫 번째 테스트 조건이 "false"로 평가되면 다음 조건이 평가됩니다. 이전 조건이 충족되지 않으면 규칙 무게 5가 할당됩니다. </p> <p>항상 목록의 끝에 조건 없이 규칙 가중치를 제공해야 합니다. 이렇게 하지 않으면 조건 테스트가 "true"로 평가되지 않는 경우 규칙의 가중치가 0입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>값/등급 </p> </td> 
      <td colname="col2"> <p>기본 제공 순위 기능 중 하나 또는 원하는 순서와 함께 가능한 데이터 소스 컨텐츠로 구성됩니다. </p> <p>데이터 소스 <span class="uicontrol"> 유형으로 Adobe Analytics 지표(숫자) </span> 를 선택한 경우 다음 옵션이 있는 드롭다운 목록이 표시됩니다. 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> 주문별 자동 등급(기본값) </span> <p>Adobe Analytics 지표에 따라 문서의 상대 위치를 기반으로 하는 등급을 계산합니다. 예를 들어, 문서의 위치가 최상위 문서에 근접하면 순위가 높아집니다. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> 값별 자동 등급 지정 </span> <p>Adobe Analytics 지표에 따라 문서의 상대적 값을 기반으로 등급을 계산합니다. 예를 들어, 문서의 값이 최상위 문서의 값에 가까울수록 순위가 높습니다. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> 사용자 지정 </span> <p>사용자 정의 설정을 지정합니다. 예를 들어 이름이 "brand"인 데이터 소스에는 특정 제품의 브랜드 이름이 포함될 수 있습니다. 등급을 함께 나열하여 각 브랜드의 상대적 중요도를 지정할 수 있습니다. </p> </li> 
      </ul> </p> <p>자동 등급 계산에서 반환되는 등급 값은 0.0(최저) - 1.0(최고) 범위에 있습니다. 설정 &gt; 메타데이터 &gt; 정의 아래에 등급 필드에 정의된 범위에 따라 조정되지 않습니다. </p> <p>다음 예에서는 특정 검색 결과에 대한 브랜드 데이터 소스가 정확히 "DKNY"와 일치하는 경우 해당 결과에 적용된 등급은 0.5입니다.그렇지 않으면 브랜드가 "Levis"인 경우 적용된 등급은 0.1입니다.데이터 소스 컨텐츠는 설정된 값과 일치해야 합니다. 즉, 데이터 소스 컨텐츠가 "Levis Corp."이면 "Levis" 값과 일치하지 않습니다. 대/소문자를 무시하므로 "DKNY"는 "dkny" 및 "Dkny"와 일치합니다. <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>고급 옵션으로 값을 정규 표현식으로 지정할 수 있습니다. 예를 들어 일부 사이트 페이지에 브랜드 값이 "Levis"이고 다른 사이트 페이지에 브랜드 값이 "Levis 청바지"인 경우 키워드와 함께 지정된 정규 표현식을 사용할 수 있습니다 
      <userinput>
        regexp 
      </userinput>. </p> <p>정규 <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 표현식을 참조하십시오 </a>. </p> <p>다음 예에서는 브랜드 컨텐트 "Levis jeans"가 포함된 검색 결과 문서에 0.1 등급이 지정됩니다.표준 비교와 마찬가지로 일반 표현식에서도 대/소문자가 무시됩니다. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 등급 </p> </td> 
      <td colname="col2"> <p> 지정된 값과 일치하지 않는 검색 결과 문서에 적용할 등급을 지정합니다. 위의 예에서 "간격"이 정의된 값과 일치하지 않기 때문에 "브랜드" 데이터 소스가 포함된 검색 결과 문서에 기본 등급 값이 할당됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>참고 </p> </td> 
      <td colname="col2"> <p>등급 규칙 정의 또는 만든 규칙 그룹 정의와 관련된 정보를 추가합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   유효한 등급 값의 범위는 일반적으로 다음과 같이 -1.0에서 1.0까지입니다.

   * `-1.0` 가 &quot;최소 등급(검색 결과에 더 낮게 표시)&quot;입니다.
   * `0.0` 은 &quot;중립 등급(검색 결과 순서를 변경하지 않음)&quot;입니다.
   * `1.0` 가 &quot;최대 등급(검색 결과에 더 높은 표시)&quot;입니다.
   정의된 등급은 모든 규칙에 대해 동일한 범위 내에 있어야 합니다. 등급 범위는 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;아래에 있는 등급 필드에 대해 정의된 범위와 일치해야 합니다.

   새 [메타 태그 필드](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)추가를 참조하십시오.

   등급 [규칙](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)편집을 참조하십시오.
1. 클릭 **[!UICONTROL Add]**.
1. 규칙 추가 결과를 미리 보려면 을 클릭하여 스테이지된 웹 사이트 인덱스를 다시 **[!UICONTROL regenerate your staged site index]** 빌드합니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 편집 {#task_5EBF55A43D6545FEA46BAE5E586FA275}

이미 추가한 기존 등급 규칙을 편집할 수 있습니다.

등급 [구성을](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)참조하십시오.

**등급 규칙을 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. (선택 사항) 규칙 그룹을 만들고 그룹에 규칙을 추가한 경우 **[!UICONTROL Define Ranking Rules]** 페이지의 **[!UICONTROL Select Rule Group]** 드롭다운 목록에서 편집할 규칙이 포함된 규칙 그룹을 선택합니다.

   등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.
1. 테이블의 **[!UICONTROL Actions]** 열 머리글에서 변경할 데이터 소스 이름을 **[!UICONTROL Edit]** 클릭합니다.
1. 페이지에서 원하는 옵션을 [!DNL Edit Ranking Rule] 설정합니다. 별표(*)로 표시된 필드는 필수입니다.

   등급 규칙 [추가](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 편집 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 삭제 {#task_742A3BCC2A6E4164BE84CC7408807EBB}

더 이상 사용할 필요가 없는 등급 규칙을 삭제할 수 있습니다.

등급 [구성을](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)참조하십시오.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.

**등급 규칙을 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. (선택 사항) 규칙 그룹을 만들고 그룹에 규칙을 추가한 경우 [!DNL Define Ranking Rules] 페이지의 **[!UICONTROL Select Rule Group]** 드롭다운 목록에서 삭제할 규칙이 포함된 규칙 그룹을 선택합니다.
1. 테이블의 **[!UICONTROL Actions]** 열 머리글에서 변경할 데이터 소스 이름을 **[!UICONTROL Delete]** 클릭합니다.
1. 페이지에서 [!DNL Delete Ranking Rule] 을 클릭합니다 **[!UICONTROL Delete]**.

   페이지로 돌아갑니다. [!DNL Define Ranking Rules]
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 삭제 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 그룹 추가 {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

&quot;등급&quot; 유형의 메타 태그를 두 개 이상 정의한 경우 다양한 등급 필드를 계산하는 데 사용할 별도의 규칙 모음을 만들 수 있습니다. 등급 규칙 그룹을 추가한 다음 정의된 등급 필드 중 하나에 할당할 수 있습니다.

규칙 그룹에는 일반적으로 추가한 규칙이 하나 이상 포함됩니다. 하지만 규칙 그룹은 다른 규칙 그룹을 참조할 수도 있습니다. 예를 들어 하나 이상의 규칙 그룹을 만든 다음 일반적으로 사용되는 규칙을 각 규칙 그룹에 추가할 수 있습니다. 그런 다음 여러 등급을 계산하는 동안 해당 규칙이 공유됩니다.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)편집을 참조하십시오.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)삭제를 참조하십시오.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E)검토를 참조하십시오.

**등급 규칙 그룹을 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Define Ranking Rules] 드롭다운 목록 오른쪽에 있는 을 **[!UICONTROL Select Rule Group]** **[!UICONTROL Add]**&#x200B;클릭합니다.
1. 페이지의 [!DNL Add Ranking Rule Group] **[!UICONTROL Rule Group Name]** 필드에 새 규칙 그룹의 고유한 이름을 입력합니다.
1. 드롭다운 **[!UICONTROL Rank Field Name]** 목록에서 새 규칙 그룹과 연결할 등급 메타데이터 필드 이름을 선택합니다. 등급을 지정하지 않으려면 **[!UICONTROL None]** 선택합니다.

   등급 필드 이름 목록은 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** >에 추가된 메타데이터 정의에서 가져옵니다 **[!UICONTROL Definitions]**.

   새 메타 태그 필드 [추가의 옵션 표를](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)참조하십시오.
1. 클릭 **[!UICONTROL Add]**.
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 추가 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 그룹 편집 {#task_D3EC0437E47144BC9E754FEF99C725E5}

기존 등급 규칙 그룹의 설정을 편집할 수 있습니다.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.

**등급 규칙 그룹을 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Define Ranking Rules] 드롭다운 목록 오른쪽에 있는 을 **[!UICONTROL Select Rule Group]** **[!UICONTROL Edit]**&#x200B;클릭합니다.
1. 페이지의 [!DNL Edit Ranking Rule Group] 필드에 **[!UICONTROL Rule Group Name]** 규칙 그룹의 고유한 이름을 입력합니다.
1. 드롭다운 **[!UICONTROL Rank Field Name]** 목록에서 규칙 그룹과 연결할 등급 메타데이터 필드 이름을 선택합니다. 등급을 지정하지 않으려면 **[!UICONTROL None]** 선택합니다.

   등급 필드 이름 목록은 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** >에 추가된 메타데이터 정의에서 가져옵니다 **[!UICONTROL Definitions]**.

   새 메타 태그 필드 [추가의 옵션 표를](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 추가 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 그룹 삭제 {#task_BE5BE01F377843BEA9846E094A07F2EA}

더 이상 필요하지 않거나 사용하지 않는 등급 규칙 그룹을 삭제할 수 있습니다. 그룹을 삭제하면 그룹에 추가된 모든 규칙도 삭제됩니다. 기본 &quot;등급 규칙&quot; 그룹은 삭제할 수 없습니다.

삭제 그룹에 포함된 규칙 그룹의 내용은 삭제되지 않습니다.이러한 그룹에 대한 참조만 제거됩니다.

변경 사항이 검색 결과에 제대로 반영되도록 웹 사이트를 다시 색인화해야 합니다.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.

**등급 규칙 그룹을 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Define Ranking Rules] **[!UICONTROL Select Rule Group]** 드롭다운 목록에서 삭제할 그룹을 선택합니다.
1. 드롭다운 **[!UICONTROL Select Rule Group]** 목록 오른쪽에서 을 클릭합니다 **[!UICONTROL Delete]**.
1. 페이지에서 [!DNL Delete Ranking Rule Group] 을 클릭합니다 **[!UICONTROL Delete]**.
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 추가 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 그룹 검토 {#task_5694459D050C4254A25186038CD66B6E}

등급 규칙 그룹 개요를 사용하여 각 그룹 등급 필드 이름, 연결된 데이터 소스 및 가중치를 볼 수 있습니다.

등급 [규칙 그룹](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)추가를 참조하십시오.

**등급 규칙 그룹을 검토하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Define Ranking Rules] 드롭다운 목록 오른쪽에 있는 을 **[!UICONTROL Select Rule Group]** **[!UICONTROL Overview]**&#x200B;클릭합니다.
1. 페이지에서 을 클릭하여 [!DNL Ranking Rule Groups Overview] **[!UICONTROL Close]** [!DNL Define Ranking Rules] 페이지로 돌아갑니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙 테스트 {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

설정한 등급 규칙 정의를 적절한 URL 테스트를 제공할 수 있습니다. 계산에 사용된 지표가 계산된 등급 값과 함께 표시됩니다.

[등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

**등급 규칙을 테스트하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Define Ranking Rules] **[!UICONTROL Test URL]** 영역에서 웹 사이트에 있는 웹 페이지의 URL을 입력합니다.
1. 클릭 **[!UICONTROL Test]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 등급 규칙과 연결된 두께 조정 {#task_3CB6FC92A66F4D99874A42D55825DB64}

개별 등급 규칙의 상대적 기여도와 최종 검색 결과에 대한 등급 기여도를 변경할 수 있습니다.

등급이 정의되지 않은 경우 검색 결과는 **[!UICONTROL Natural Relevance]** 페이지의 [규칙 및 관련성] 슬라이더 막대 **[!UICONTROL Adjust Ranking Weights]** 측면에 100%가 있습니다. 이 균형은 단순히 검색 결과가 검색어만을 기반으로 주문됨을 의미합니다.

등급이 정의되면 연관된 등급 메타데이터 필드에 1-10의 연관성 값이 지정됩니다. 값이 1이면 계산된 등급은 검색 결과 순서의 10%를 구성하고, 자연어 연관성은 나머지 90%를 의미합니다.

규칙 그룹에 정의된 규칙이 두 개 이상 있는 경우 각 규칙의 가중치 값에 따라 규칙의 결과가 계산된 총 등급에 기여하는 정도가 결정됩니다. 예를 들어 80%의 자연어 관련성이 있다고 가정해 봅시다. 즉, 연관된 등급 필드의 연관성은 2입니다. 또한 두 개의 규칙을 정의했습니다.1은 3이고 2은 7이다. 이 경우 최종 결과에 대한 첫 번째 규칙의 기여도는 6%((3 / (3+7)) * 20%)입니다. 두 번째 규칙의 최종 결과에 대한 기여도는 14%((7 / (3+7)) * 20%입니다.

**등급 규칙과 연관된 가중치를 조정하려면**

1. 제품 메뉴에서 > **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Adjust Ranking Weights] **[!UICONTROL Select Rule Group]** 드롭다운 목록에서 등급 가중치를 조정할 그룹을 선택합니다.
1. 슬라이더를 드래그하여 해당 기여도 값을 변경합니다.

   파이 차트는 변경 사항을 그래픽으로 반영합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. 스테이지된 웹 사이트 인덱스를 다시 작성하여 규칙 추가 결과를 미리 봅니다.

   라이브 [또는 스테이지 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   라이브 [또는 스테이지된 웹 사이트의 증분 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.
