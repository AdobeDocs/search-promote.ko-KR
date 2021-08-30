---
description: 메타데이터 메뉴를 사용하여 검색 정의 및 인덱스 주입을 사용자 정의합니다.
solution: Target
subtopic: Metadata
title: 메타데이터 메뉴 정보
topic-legacy: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
exl-id: 53d62da9-c5bd-4c4a-bb89-743704f66f7f
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '8028'
ht-degree: 1%

---

# 메타데이터 메뉴 정보{#about-the-metadata-menu}

메타데이터 메뉴를 사용하여 검색 정의 및 인덱스 주입을 사용자 정의합니다.

## 정의 정보 {#concept_AE48035C210145169BE067D396975620}

[!DNL Definitions] 을 사용하여 고객이 검색 쿼리를 제출할 때 고려되는 HTML 및 메타데이터 필드의 콘텐츠와 관련성을 사용자 지정할 수 있습니다.

이미 사전 정의된 필드를 편집할 수 있습니다. 또는 메타데이터 태그 컨텐츠를 기반으로 새로운 사용자 정의 필드를 만들 수도 있습니다. 각 정의는 [!DNL Staged Definitions] 페이지의 단일 행에 표시됩니다.

또한 [데이터 보기 정보](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)를 참조하십시오.

## 새 메타 태그 필드 추가 {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

자신만의 메타데이터 태그 필드를 정의하고 추가할 수 있습니다.

고객에게 새 메타 태그 정의의 효과가 표시되려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

**새 메타 태그 필드를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지에서 **[!UICONTROL Add New Field]** 을 클릭합니다.
1. [!DNL Add Field] 페이지에서 원하는 옵션을 설정합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>필드 이름 </p> </td> 
      <td colname="col2"> <p>필드를 참조하는 데 사용할 이름을 지정합니다. </p> <p>필드 이름은 다음 규칙을 준수해야 합니다. </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> 이름에는 영숫자만 사용할 수 있습니다. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> 대시는 이름에 사용할 수 있지만 공백은 사용할 수 없습니다. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> 최대 20자의 이름을 입력할 수 있습니다. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> 이름은 대/소문자를 구분하지 않지만, 입력하는 그대로 표시되고 저장됩니다. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> <span class="wintitle"> 스테이징된 정의 </span> 페이지의 표에 표시된 대로 미리 정의된 필드에 존재하는 이름을 사용할 수 없습니다. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> "any"라는 단어를 사용자 정의 필드 이름의 값으로 사용할 수 없습니다. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> 사전 정의된 필드의 이름은 편집할 수 없습니다. </li> 
      </ul> </p> <p> 필드 이름 예: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> 작성자 </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> 게시 날짜 </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> 뭔가 야생적인 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>메타 태그 이름 </p> </td> 
      <td colname="col2"> <p>정의된 필드와 관련된 컨텐츠를 결정합니다. </p> <p>이름 목록은 최대 255자까지 사용할 수 있습니다. 또한 이름에는 HTML 메타 태그의 이름 특성에 허용되는 모든 문자를 포함할 수 있습니다. </p> <p>단일 필드 정의에서 여러 메타 태그를 지정할 수 있습니다. </p> <p>여러 값은 쉼표로 구분해야 하며, 주어진 웹 페이지에서 맨 왼쪽 메타 태그 이름이 우선합니다. </p> <p>예를 들어 "auth"라는 필드를 정의했다고 가정합니다. 필드 이름에 연결된 메타 태그 "author, dc.author"가 있습니다. 이 경우, "author" 메타 태그의 컨텐츠는 인덱싱되어 두 메타 태그가 웹 페이지에 나타나는 경우 "dc.author"의 컨텐츠를 검색합니다. </p> <p>사용자 정의 필드에는 정의에 하나 이상의 메타 태그 이름이 있어야 합니다. 사전 정의된 필드에는 연관된 메타 태그가 필요하지 않습니다. 그러나 하나 이상의 메타 태그가 지정된 경우 메타 태그의 컨텐츠는 각 태그의 현재 데이터 소스를 덮어씁니다. </p> <p>예를 들어 메타 태그 "dc.title"이 사전 정의된 "title" 필드와 연결된 경우 "dc.title" 메타 태그의 컨텐츠가 페이지의 내용 위에 인덱싱됩니다 
      특정 문서에 대한 <code>
        &lt;title&gt; 
      </code> 태그입니다. </p> <p>이러한 예로는 다음과 같은 경우가 있습니다. </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> 설명 </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> 독점 태그 </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>데이터 유형 </p> </td> 
      <td colname="col2"> <p>모든 필드에는 텍스트, 숫자, 날짜, 버전, 등급 또는 위치와 같은 관련 데이터 유형이 있습니다. 이 데이터 유형은 필드의 컨텐츠가 인덱스화되고 검색되며 선택적으로 정렬되는 방식을 결정합니다. </p> <p>필드 정의를 만든 후에는 데이터 유형을 변경할 수 없습니다. </p> <p>다음 정보를 사용하여 필드에 포함된 정보와 관련된 데이터 유형을 선택할 수 있습니다. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> 텍스트  </span> 데이터 유형 필드는 문자 문자열로 처리됩니다. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> 숫자  </span> 데이터 유형 필드는 정수 또는 부동 소수점 숫자 값으로 처리됩니다. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> 날짜  </span> 데이터 유형 필드는 날짜/시간 지정자로 처리됩니다. 새 필드를 추가하거나 편집할 때 허용된 날짜/시간 형식을 사용자 지정할 수 있습니다. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> 버전  </span> 데이터 유형 필드는 자유 형식 숫자 데이터로 처리됩니다. 예를 들어 1.2.3은 1.2.2 앞에 정렬됩니다. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> 등급  </span> 데이터 유형 필드는 검색 결과의 등급/관련성 계산에 추가로 영향을 주지만 "숫자" 유형 필드와 동일하게 처리됩니다. <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">등급 규칙 정보</a>를 참조하십시오 . </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> 위치  </span> 데이터 유형 필드는 세계 어디에서든 물리적 위치로 처리됩니다. 허용되는 위치 형식은 다음과 같습니다. <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> DDD 또는 DDD-DDD 형식의 5 또는 9자리 ZIP 코드. 여기서 각 "D"는 0-9자리입니다. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> DDD 형식의 3자리 영역 코드입니다. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> DD.DDD DDD DDD.DDD 형식의 위도/경도 쌍입니다. 여기서 첫 번째 번호는 위도를 지정하고 두 번째 번호는 경도를 지정합니다. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>허용 목록 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 텍스트 </span> 또는 <span class="uicontrol"> 숫자 </span>를 선택한 경우에만 사용할 수 있습니다. </p> <p>이 필드의 메타데이터 컨텐츠에서 구분된 값을 별도로 색인화합니다. </p> <p>예를 들어 "허용 목록"을 선택하면 "빨강, 노랑, 녹색, 파랑" 컨텐츠가 "색상"이 아닌 4개의 개별 값으로 처리됩니다. 이 처리는 범위 검색(사용 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code> 또는 
      <code>
        sp_q_exact 
      </code>) 및 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code> 및 
      <code>
        &lt;search-display-field-values&gt; 
      </code> </p> <p>버전 데이터 유형을 선택한 경우에는 사용할 수 없습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 동적 패싯 </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>참고: 이 기능은 기본적으로 활성화되어 있지 않습니다. 기술 지원에 문의하여 사용할 수 있도록 활성화하십시오. 활성화되면 사용자 인터페이스에 표시됩니다. </p> </p> <p>식별된 패싯을 동적으로 설정합니다. </p> <p>패싯은 메타 태그 필드의 맨 위에 만들어집니다. 메타 태그 필드는 Adobe Search &amp; Promote의 낮은 레벨의 핵심 검색 레이어입니다. 반면 패싯은 GS(Guided Search)의 일부이며 Adobe Search &amp; Promote의 높은 수준의 프레젠테이션 레이어입니다. 패싯은 메타 태그 필드를 소유하지만 메타 태그 필드는 패싯에 대해 아무것도 알지 못합니다. </p> <p><a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 동적 패싯 정보 </a> 를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중복 제거 허용 </p> </td> 
      <td colname="col2"> <p>이 필드에 대해 중복 제거를 사용하려면 이 옵션을 선택합니다. 즉, 을 통해 검색 시 이 필드를 지정할 수 있습니다 
        <code>
          sp_dedupe_field 
        </code> CGI 매개 변수를 검색합니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI 매개 변수 검색 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테이블 이름 </p> </td> 
      <td colname="col2"> <p>주어진 필드를 주어진 테이블 이름과 영구적으로 연결합니다. </p> <p>코어 검색 CGI 매개 변수 또는 템플릿 태그 내에서 이러한 필드가 언급될 때마다 테이블 이름이 자동으로 제공됩니다. 이 기능을 사용하면 테이블 일치 항목을 통해 동적 패싯을 선택할 수 있지만 원하는 경우 비동적 패싯 필드에 사용할 수도 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>목록 구분 기호 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 허용 목록 </span>을 선택한 경우에만 사용할 수 있습니다. </p> <p>개별 목록 값을 구분하는 문자를 지정합니다. 여러 문자를 지정할 수 있으며 각 문자는 값 구분 기호로 처리됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본적으로 검색 </p> </td> 
      <td colname="col2"> <p>이 필드를 선택하면 주어진 검색 쿼리에 필드를 명시적으로 지정하지 않은 경우에도 필드 콘텐츠가 검색됩니다. 이 옵션을 선택 취소하면 요청한 경우에만 필드가 검색됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>수직 업데이트 필드 </p> </td> 
      <td colname="col2"> <p> <p>참고: 이 기능은 기본적으로 활성화되어 있지 않습니다. 기술 지원에 문의하여 사용할 수 있도록 활성화하십시오. 활성화되면 사용자 인터페이스에 표시됩니다. </p> </p> <p>식별된 필드를 수직 업데이트 필드로 설정합니다. </p> <p>수직 업데이트 필드는 수직 업데이트 프로세스를 통해 업데이트할 후보입니다( <span class="uicontrol"> 인덱스 </span> &gt; <span class="uicontrol"> 수직 업데이트 </span>). 수직 업데이트 방식으로 인해 이러한 필드의 콘텐츠를 자유 텍스트 검색에서 검색할 수 없습니다. 이 옵션을 선택하면 인덱스 작업 중에 이 필드의 콘텐츠가 "word" 인덱스에 추가되지 않습니다. 또한 수직 업데이트 작업 중에 이 필드를 업데이트할 수 있습니다. </p> <p>수직 업데이트에 대한 자세한 내용은 <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 수직 업데이트 정보 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>관련성 </p> </td> 
      <td colname="col2"> <p>사전 정의 및 사용자 정의 필드의 관련성을 편집할 수 있습니다. </p> <p>관련성은 1-10의 축에서 지정됩니다. 1을 설정하면 가장 관련이 없고 10이 가장 관련이 적음을 의미합니다. 이 값은 소프트웨어가 각 필드의 쿼리 일치 여부를 고려할 때 고려됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>정렬 </p> </td> 
      <td colname="col2"> <p>결과를 명명된 필드를 기준으로 정렬하는 시점을 
        <code>
          sp_s 
        </code> CGI 매개 변수를 검색합니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI 매개 변수 검색 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>언어 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span>, <span class="uicontrol"> 숫자 </span> 또는 <span class="uicontrol"> 날짜 </span>를 선택한 경우에만 사용할 수 있습니다. </p> <p>이 필드에 대한 날짜, 숫자 및 등급 값을 인덱싱할 때 적용되는 언어 및 로케일 규칙을 제어합니다. </p> <p>계정 언어를 적용하도록 선택할 수 있습니다(언어학 &gt; 단어 및 언어). 또는 각 번호 또는 날짜 값을 포함하는 문서와 연관된 언어나 특정 언어를 적용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>날짜 형식 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span>를 선택한 경우에만 사용할 수 있습니다. </p> <p>이 필드에 대한 날짜 값을 인덱싱할 때 인식되는 날짜 형식을 제어합니다. </p> <p>각 날짜 필드에 대해 날짜 형식 문자열의 기본 목록이 제공됩니다. 목록에 을 추가하거나 사이트의 요구에 맞게 목록을 편집할 수 있습니다. </p> <p><a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> 날짜 형식 </a> 을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트 날짜 형식 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span> 가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>형식을 올바르게 지정하도록 지정한 날짜 형식을 미리 볼 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간대 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span> 가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>시간대를 지정하지 않은 이 필드에 대한 날짜 값을 인덱싱할 때 적용되는 예상 시간대를 제어합니다. </p> <p>예를 들어, 계정 시간대가 "미국/로스앤젤레스"로 설정되어 있고 <span class="uicontrol"> 계정 시간대 사용 </span> 을 선택하면 지정된 시간대가 없는 다음 메타 날짜 값이 태평양 시간인 것처럼 처리되며 일광 절약 시간제가 적용됩니다. </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>가장 중요하지 않은 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span> 이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서의 최소 등급을 나타내는 등급 값을 제어합니다. </p> <p>문서 등급이 가장 낮은 랭크에 대해 0부터 가장 높은 랭크에 대해 10까지 범위인 경우 이 값을 0으로 설정합니다. </p> <p>문서 등급이 가장 높은 랭크에 대해 1부터 가장 낮은 랭크에 대해 10까지 범위인 경우 이 값을 10으로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span> 이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서에 이 등급 필드에 대해 정의된 메타 태그가 없는 경우 사용되는 등급 값을 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>가장 중요한 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span> 이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서의 최대 등급을 나타내는 등급 값을 제어합니다. </p> <p>문서 등급이 가장 낮은 랭크에 대해 0부터 가장 높은 랭크에 대해 10까지 범위인 경우 이 값을 10으로 설정합니다. </p> <p>문서 등급이 가장 높은 랭크에 대해 1부터 가장 낮은 랭크에 대해 10까지 범위인 경우 이 값을 1로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 단위 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 위치 </span> 가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>근접 검색에 대한 거리 값 처리를 제어합니다. </p> <p>기본 단위를 <span class="uicontrol"> Miles </span>(으)로 설정하면 이 필드에 적용되는 모든 근접 검색 최소/최대 거리 기준이 
      <code>
        sp_q_min[_#] 
      </code> 또는 
      <code>
        sp_q_max[_#] 
      </code> 검색 CGI 매개 변수)는 km로, 그렇지 않으면 km로 처리됩니다. </p> <p>또한 이 옵션은 
      <code>
        &lt;Search-Display-Field&gt; 
      </code> 근접 검색 출력 필드에 적용할 때 검색 결과 템플릿 태그입니다. </p> <p><a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 근접 검색 정보 </a> 를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 설명 만들기? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 숫자 </span>를 데이터 유형으로 선택한 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 디자인 </span> &gt; <span class="uicontrol"> 탐색 </span> &gt; <span class="uicontrol"> 패싯 </span>에 사용할 필드 범위 설명을 자동으로 만들 수 있도록 제어합니다. </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> 패싯 정보 </a> 를 참조하십시오. </p> <p> <p>참고:  이 필드에 <span class="uicontrol"> 수직 업데이트 필드 </span>가 선택되어 있으면 수직 업데이트 중에 생성된 필드 범위 설명 필드가 업데이트됩니다. 그러나 <span class="uicontrol"> 범위 필드 </span>에 식별된 필드에 <span class="uicontrol"> 수직 업데이트 필드 </span>도 선택되어 있는 것이 좋습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 필드 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택된 경우에만 사용할 수 있습니다. </p> <p>현재 필드에 대한 범위 설명을 사용하여 업데이트할 <span class="uicontrol"> 텍스트 </span> 필드. 이 목록에는 필드 범위 생성을 위해 다른 필드와 함께 아직 사용되지 않는 <span class="uicontrol"> 텍스트 </span> 필드가 모두 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 값 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>필드 범위 설명을 만들 때 사용할 데이터 포인트가 공백으로 구분됩니다. 예: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>이러한 값을 임의의 순서로 입력할 수 있습니다. 값이 정렬되고 중복 제거되어 저장되기 전에 반환됩니다. 음수 값과 정수가 아닌 값을 지정할 수도 있습니다. </p> <p>이 필드의 각 값에 대해 다음을 수행합니다. 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;)보다 작으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다 </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;=)보다 크거나 같으면 <span class="uicontrol"> "Greater Than" 형식 </span>이 사용됩니다. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">그렇지 않으면 필드 값이 두 개의 연속된 <span class="uicontrol"> 범위 값 </span>(보다 큼), 더 작은 값(&lt;=) 보다 작거나 같은 경우(&lt;=), <span class="uicontrol"> 중간 형식 </span> 이 사용되는 경우 "range"가 발생합니다. </li> 
    </ul> </p> <p>예를 들어 위의 값 세트 는 값에 대한 설명 세트를 정의합니다. 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">10 미만 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">10보다 크거나 같고 20보다 작음 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">20보다 크거나 같고 50보다 작음 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">50보다 크거나 같고 100보다 작음 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100보다 크거나 같고 10000 미만 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">크거나 10000 </li> 
      </ul> </p> <p><span class="uicontrol"> 보다 큰 테스트를 사용하시겠습니까? </span> 테스트 수행 방식을 변경하려면 다음을 수행하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"보다 작음" 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 범위 값 </span>에 있는 가장 작은 값보다 작은 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 가장 작은 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~N~ </span>을 사용하여 표시됩니다. 예: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>또는: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>일반적으로 값은 "as-is"(예: <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 경우) 및 제공된 값 1의 경우, 생성된 범위 설명은 "5 미만" 과 비슷합니다. 대신 "4.99 이하"인 경우 <span class="uicontrol"> Precision </span> 을 <span class="uicontrol"> 2 </span>로 설정하고 다음 형식을 사용하십시오. </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p><span class="uicontrol"> "Less Than" 형식 </span>에서 대소문자 <span class="uicontrol"> ~n~ </span>은(는) <span class="uicontrol"> Precision </span> 설정에 따라 <i>down</i>이 반올림됩니다. </p> <p>참고: 범위 설명에 숫자 자리 표시자를 그대로 포함하려면 백슬래시(\) 접두어를 사용하여 지정합니다(예: ). <span class="uicontrol"> \~N~ </span> 또는 <span class="uicontrol"> \~n~ </span> 백슬래시 문자를 포함하려면 다른 백슬래시로 지정합니다(예: ). <span class="uicontrol"> \\ </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중간 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 범위 값 </span>에 있는 가장 작은 값과 가장 큰 값 사이에 있는 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 지정된 범위의 경우 낮은 범위 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~L~ </span>을 사용하여 표시되고, 더 높은 범위 값은 토큰 <span class="uicontrol"> ~H~ </span>을 사용하여 표시됩니다. 예: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>또는: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>또는: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>일반적으로 값은 "as-is"(즉, <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 경우) 및 제공된 값 8의 경우, 생성된 범위 설명은 "5~10"의 형식이 됩니다. 대신 "5~9.99"가 되고 더 높은 값이 <i>아래쪽</i>로 조정되면 <span class="uicontrol"> 정밀도 </span> 를 <span class="uicontrol"> 2 </span>로 설정하고 다음 형식을 사용하십시오. </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>마찬가지로 <span class="uicontrol"> ~L~ </span>은 <span class="uicontrol"> ~l~ </span>로 대체하여 더 낮은 값을 <i>위쪽</i>으로 조정 <span class="uicontrol"> Precision </span> 설정에 따라 사용할 수 있습니다. 이것은 다음과 같은 정의를 의미합니다. </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p><span class="uicontrol"> Precision </span> 값이 <span class="uicontrol"> 2 </span>이면 "Between 5.01에서 10"이 만들어집니다. </p> <p>소문자 <span class="uicontrol"> ~l~ </span>을(를) 사용하면 <span class="uicontrol"> Precision </span> 설정에 따라 낮은 값이 <i>업</i>으로 반올림되고, 소문자 <span class="uicontrol"> ~h~ </span>을(를) 사용하면 더 높은 값이 <i>아래쪽</i>으로 반올림됩니다. </p> <p>참고: 범위 설명에 숫자 자리 표시자를 그대로 포함하려면 백슬래시(\) 접두어를 사용하여 지정합니다(예: ). <span class="uicontrol"> \~L~ </span> 또는 <span class="uicontrol"> \~h~ </span> 백슬래시 문자를 포함하려면 다른 백슬래시로 지정합니다(예: ). <span class="uicontrol"> \\ </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"보다 큼" 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 범위 값 </span>에 있는 가장 큰 값보다 큰 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 가장 큰 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~N~ </span>을 사용하여 표시됩니다. 예: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>또는: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>일반적으로 값은 "as-is"(예: <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 경우) 및 제공된 값 30의 경우, 생성된 범위 설명은 "20보다 큼"과 비슷합니다. 대신 "20.01 이상"이 되도록 하려면 <span class="uicontrol"> Precision </span> 을 <span class="uicontrol"> 2 </span>로 설정하고 다음 형식을 사용하십시오. </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p><span class="uicontrol"> "Greater Than" 형식 </span>에서 소문자는 <span class="uicontrol"> ~n~ </span>으로 인해 <span class="uicontrol"> Precision </span> 설정에 따라 값이 <i>up</i>반올림됩니다. </p> <p>참고: 범위 설명에 숫자 자리 표시자를 그대로 포함하려면 백슬래시(\) 접두어를 사용하여 지정합니다(예: ). <span class="uicontrol"> \~N~ </span> 또는 <span class="uicontrol"> \~n~ </span> 백슬래시 문자를 포함하려면 다른 백슬래시로 지정합니다(예: ). <span class="uicontrol"> \\ </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>정밀도 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>소수점 오른쪽에 자릿수를 지정하는 정수 값입니다. 반올림 작업도 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>선행 0 제거? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택되어 있고 0이 아닌 <span class="uicontrol"> 정밀도 </span> 값이 설정된 경우에만 사용할 수 있습니다. </p> <p>"0.50"을 ".50"으로 표시해야 합니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>후행 0을 제거하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택되어 있고 0이 아닌 <span class="uicontrol"> 정밀도 </span> 값이 설정된 경우에만 사용할 수 있습니다. </p> <p>"10.00"을 "10"으로 표시해야 합니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구분자를 수천개 보여? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>"10000"을 "10,000"으로 표시해야 합니까? 로케일별 값이 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>0 값을 조정하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>반올림된 0 값이 표시되는 경우 <span class="uicontrol"> 정밀도 </span> 설정에 따라 반올림하거나 축소해야 합니까? 즉, "0.01"을 표시하시겠습니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>보다 큼 사용 테스트? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>각 값은 <span class="uicontrol"> 범위 값 </span>, <i><b>내림차순</b></i> 순서로 처리된 값과 비교되므로 기본적으로 이보다 크거나 같음(&gt;=) 연산자를 사용하여 비교되며, 테스트가 성공하면 중지됩니다. 즉, <span class="uicontrol"> 범위 값 </span> 세트가 "10 20 50 100 1000"과 같이 있으면 100 값은 100 ~ 1000 범위에 포함되며, 100은 실제로 100 이상입니다. 50~100 범위에 포함하려면 이 옵션을 선택하면 보다 큼(&gt;) 연산자를 대신 사용할 비교 결과가 발생합니다. </p> <p>예를 들어, 이 필드의 각 값에 대해 이 옵션을 선택하면 다음과 같이 됩니다. 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;=)보다 작거나 같으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다 </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;)보다 큰 경우 <span class="uicontrol"> "보다 큼" 형식 </span>이 사용됩니다 </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">그렇지 않으면 필드 값이 두 개의 연속된 <span class="uicontrol"> 범위 값 </span>(보다 크거나 같음) 더 작은 값 및 더 작은 값(&lt;)) 사이에 있고 <span class="uicontrol"> 중간 형식 </span>이 사용되는 범위가 있습니다 </li> 
    </ul> </p> <p>및 을 선택 취소하면: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;)보다 작으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다 </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;=)보다 크거나 같으면 <span class="uicontrol"> "Greater Than" 형식 </span>이 사용됩니다 </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">그렇지 않으면 필드 값이 두 개의 연속된 <span class="uicontrol"> 범위 값 </span>(보다 큼) 보다 작으며 더 큰 값(&lt;=) 보다 작거나 같은 경우 범위가 발견되며 <span class="uicontrol"> 중간 형식 </span>이 사용됩니다 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span> 가 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>샘플 숫자 값을 제공하고 <span class="uicontrol"> 테스트 </span> 단추를 눌러 범위 필드가 생성되는 방식을 확인합니다. 생성된 범위 설명이 창에 표시됩니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)도 참조하십시오.
1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 결과를 미리 보려면 준비된 사이트 인덱스를 다시 작성합니다.

   [준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 사전 정의 또는 사용자 정의 메타 태그 필드 편집 {#task_0A7657B63596421BB6DB3ED44F827AB3}

사전 정의된 메타 태그의 특정 필드만 편집하거나 사용자가 정의한 메타 태그의 모든 필드를 편집할 수 있습니다.

메타 태그 변경 사항이 고객에게 표시되려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

**사전 정의 또는 사용자 정의 메타 태그 필드를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지의 테이블의 [!DNL Actions] 열에서 변경할 메타 태그 필드 이름의 행에서 **[!UICONTROL Edit]** 를 클릭합니다.
1. [!DNL Pinned Keyword Results Manager] 페이지의 테이블에서 변경할 키워드 행에서 **[!UICONTROL Edit]** 을 클릭합니다.
1. [!DNL Edit Field] 페이지에서 원하는 옵션을 설정합니다.

   사전 정의된 메타 태그 필드를 변경하도록 선택한 경우 모든 필드를 편집할 수 있는 것은 아닙니다.

   [새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려면 준비된 사이트 인덱스를 다시 작성합니다.

   [준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 사용자 정의 메타 태그 필드 삭제 {#task_9361EF38B5E743038B6672FA6CF70FD3}

더 이상 필요하거나 사용하지 않는 사용자 정의 메타 태그 필드를 삭제할 수 있습니다.

사전 정의된 메타 태그 필드는 삭제할 수 없습니다. 그러나 특정 필드를 편집할 수 있습니다.

[사전 정의되거나 사용자 정의 메타 태그 필드 편집](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)을 참조하십시오.

삭제 메타 태그의 효과가 고객에게 표시되려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

**사용자 정의 메타 태그 필드를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지의 테이블의 [!DNL User-defined fields] 섹션에서 제거할 메타 태그 필드 이름의 행에서 **[!UICONTROL Delete]** 를 클릭합니다.
1. 확인 대화 상자에서 **[!UICONTROL OK]** 을 클릭합니다.
1. (선택 사항) 결과를 미리 보려면 준비된 사이트 인덱스를 다시 작성합니다.

   [준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 주입 정보 {#concept_DA091920671948A0A893A26B3A2FAAE5}

[!DNL Injections] 을 사용하여 페이지를 직접 편집하지 않고도 웹 페이지에 컨텐츠를 삽입할 수 있습니다.

&quot;target&quot; 또는 &quot;body&quot;와 같은 특정 인덱싱된 필드에 콘텐츠를 추가하거나 인덱싱된 컨텐츠를 새 값으로 바꿀 수 있습니다. 예를 들어 새 컨텐츠를 &quot;target&quot; 메타 태그 필드에 삽입한 경우 이 정보는 하드 코딩된 페이지 컨텐츠처럼 처리됩니다. 사이트 페이지에 해당 컨텐츠가 있는지 여부에 관계없이 미리 정의된 메타 태그 필드의 컨텐츠를 편집할 수 있습니다. 예를 들어 다음 사전 정의된 메타 태그 필드 이름의 컨텐츠를 편집할 수 있습니다.

* alt
* body
* charset
* date
* desc
* 키
* language
* target
* title
* url

## 현장주사제 {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

원할 경우 [!DNL Staged Injections] 페이지에서 **[!UICONTROL Test]**&#x200B;을 사용할 수 있습니다. 웹 사이트에서 테스트 필드 이름(예: &quot;title&quot; 또는 &quot;body&quot;), 원래 필드 값(예: &quot;홈 페이지&quot;) 및 테스트 URL을 입력합니다. 참조에 대한 결과 값이 표시됩니다. 테스트 중에는 현재 값이 변경되지 않습니다.

## 필드 삽입 정의 작업 {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

주입 정의는 다음과 같은 형식입니다.

```
append|replace field [regexp] URL value
```

`append|replace`, `field`, `URL`. 및 `value` 항목은 필수입니다. 라인당 한 개의 주입 정의를 입력합니다. 다음 예에는 6개의 다른 주입 정의가 포함되어 있습니다.

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>주입 정의 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 추가|바꾸기  </span> </p> </td> 
   <td colname="col2"> <p>삽입 정의("Adobe: 문의하기" 또는 "지금 판매 중!" 위의 예에서 ) 를 기존 필드의 컨텐츠에 추가할 수 있습니다. 기존 필드 콘텐츠를 정의된 값으로 덮어쓰려면 "바꾸기"를 선택합니다. 현재 필드에 컨텐츠가 없으면 어떤 옵션(추가 또는 바꾸기)이 사용되는지에 관계없이 정의된 값이 자동으로 추가됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 필드에서 하나의 URL 매개 변수를 지정하십시오 </span> </p> </td> 
   <td colname="col2"> <p>필드 이름이 필요합니다. 다음은 사용할 수 있는 열 개의 사전 정의된 필드 이름입니다. </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> Alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> 날짜 </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> 키  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> 제목 </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>각 필드 이름은 사이트 페이지의 요소에 해당합니다. 예를 들어 필드 이름 <span class="codeph"> desc </span> 를 지정하는 경우 삽입 정의 값을 사이트 페이지의 메타 태그에 대한 설명에 해당하는 필드에 추가할 수 있습니다. </p> <p>페이지에 설명 Meta 태그가 없는 경우 정의된 컨텐츠가 태그를 만듭니다. <span class="codeph"> desc </span> 주사에 지정된 컨텐츠가 하드 코딩된 메타 설명 컨텐츠가 표시되는 것처럼 결과 페이지에 표시됩니다. </p> <p>필드 이름이 같은 여러 정의를 만들 수도 있습니다. 예를 들어, 다음과 같은 주입을 해야 합니다. </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>위의 예에서 모든 사이트 페이지에는 "Welcome to My Site"라는 삽입된 제목이 표시됩니다. "/company/" 폴더의 페이지는 새 제목인 "My Site: 이전 항목을 대체하는 "Contact Us". </p> <p>주사제는 <span class="wintitle"> 필드 주입 정의 </span> 텍스트 상자에 표시되는 순서대로 적용됩니다. 동일한 위치에 있는 페이지에 대해 동일한 필드("제목")가 두 번 이상 정의된 경우 나중 정의가 우선합니다. </p> <p> <span class="codeph"> [regexp]  </span> - 선택 사항입니다. <span class="codeph"> regexp </span> 옵션을 사용하도록 선택하면 정의된 URL이 정규 표현식으로 처리됩니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> <p>다음 정의에서: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "중요 정보"는 일반 표현식 <span class="codeph"> ^과 일치하는 모든 페이지의 "target" 필드에 삽입됩니다.*/products/.*\.html$ </span>. </p> <p>따라서 다음 항목이 있습니다. </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>다음 예에서 </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>주사는 ".pdf" 파일 확장자로 끝나는 모든 페이지의 "제목" 컨텐츠에 "Millennium Science"를 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>URL이 필요하며 삽입할 문서를 지정합니다. </p> <p>URL은 다음 중 하나입니다. </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> https://www.mydomain.com/products.html에서와 같이 전체 경로 </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> https://www.mydomain.com/products과 같은 부분 경로 </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> https://www.mydomain.com/*.html에서와 같이 와일드카드를 사용하는 URL </li> 
     </ul> </p> <p>URL 값에는 공백 문자가 없어야 합니다. <span class="codeph"> regexp </span> 옵션을 사용하면 URL이 정규 표현식으로 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>값은 필수이며 기존 필드 콘텐츠를 바꾸거나 추가하는 데 사용됩니다. 동일한 필드 이름에 여러 값을 지정할 수 있습니다. 예: </p> <p><b>keys</b> https://www.mysite.com/travel/ <b>summer</b>, <b>beach</b>, <b>sand</b> 추가 </p> <p><b>키</b> https://www.mysite.com/travel/fare/*.html <b>저렴한 티켓</b> 추가 </p> <p>위의 예에서 "summer, beach, sand"라는 단어는 "/travel/" 디렉토리의 모든 페이지의 "keys" 필드에 추가됩니다. "price tickets"라는 단어는 "/travel/fare/" 디렉토리에 있는 모든 페이지의 "keys" 필드에 추가됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

[크롤링할 컨텐츠 유형 선택 및 인덱스](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)도 참조하십시오.

## 필드 삽입 정의 추가 {#task_E86566FA1FF74CF68115C0ADA05172AE}

[!DNL Injections] 을 사용하여 페이지를 직접 편집하지 않고도 웹 페이지에 컨텐츠를 삽입할 수 있습니다.

원할 경우 [!DNL Injections] 페이지에서 **[!UICONTROL Test]**&#x200B;을 사용할 수 있습니다. 웹 사이트에서 테스트 필드 이름(예: &quot;title&quot; 또는 &quot;body&quot;), 원래 필드 값(예: &quot;홈 페이지&quot;) 및 테스트 URL을 입력합니다. 참조에 대한 결과 값이 표시됩니다. 테스트 중에는 현재 값이 변경되지 않습니다.

**필드 삽입 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Injections] 페이지의 [!DNL Test Field Injections] 영역에서 테스트 필드, 테스트 원래 값 및 테스트 URL을 입력한 다음 **[!UICONTROL Test]** 를 클릭합니다.
1. [!DNL Field Injection Definitions] 필드에 라인당 하나의 주입 정의를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 속성 로더 정보 {#concept_9EF38E98811B42CDA41996432B9AD209}

추가 입력 소스를 정의하여 웹 사이트에서 크롤링된 데이터를 보강하려면 [!DNL Attribute Loader] 을 사용하십시오.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

데이터 피드 입력 소스를 사용하여 웹 사이트에서 일반적으로 검색되는 것과 다른 양식에 저장된 컨텐츠에 액세스할 수 있습니다. 사용 가능한 크롤링 메서드 중 하나를 사용하여 이 작업을 수행합니다. 그런 다음 이러한 소스의 데이터를 크롤링된 컨텐츠의 데이터에 삽입할 수 있습니다.

[!DNL Staged Attribute Loader Definitions] 페이지에 속성 로더 정의를 추가한 후 이름 값 및 유형 값을 제외한 모든 구성 설정을 변경할 수 있습니다

[!DNL Attribute Loader] 페이지에는 다음 정보가 표시됩니다.

* 구성하고 추가한 정의된 속성 로더 구성의 이름입니다.
* 추가한 각 커넥터에 대해 다음 데이터 소스 유형 중 하나:

   * **텍스트**  - 단순 &quot;플랫&quot; 파일, 쉼표로 구분, 탭으로 구분 또는 기타 일관되게 구분된 형식.
   * **피드**  - XML 피드.

* 다음 크롤링 및 인덱싱에 대한 구성을 사용할지 여부를 지정합니다.
* 데이터 소스의 주소입니다.

[텍스트 및 피드에 대한 속성 삽입 프로세스의 작동 방식.. 을 참조하십시오.](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

[여러 속성 로더 구성 정보](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)를 참조하십시오

속성을 추가할 때 미리 보기 사용 정보..](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)[

## 속성 로더의 텍스트 및 피드 구성에 대해 속성 삽입 프로세스가 작동하는 방식 {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>단계 </p> </th> 
   <th colname="col2" class="entry"> <p>프로세스 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드합니다. </p> </td> 
   <td colname="col3"> <p>텍스트 및 피드 구성의 경우 간단한 파일 다운로드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>다운로드한 데이터 소스를 개별 의사 문서로 분류합니다. </p> </td> 
   <td colname="col3"> <p><span class="uicontrol"> 텍스트 </span>의 경우, 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며, 쉼표 또는 탭과 같은 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p><span class="uicontrol"> 피드 </span>의 경우 각 문서의 데이터는 다음 형식의 정규 표현식 패턴을 사용하여 추출됩니다. </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle"> 속성 로더 추가 </span> 페이지에서 <span class="uicontrol"> 매핑 </span>을 사용하여 캐시에 저장된 데이터 사본을 생성한 다음 Crawler에 대한 링크 목록을 만듭니다. 데이터는 로컬 캐시에 저장되고 구성된 필드로 채워집니다. </p> <p>구문 분석된 데이터는 로컬 캐시에 기록됩니다. </p> <p>이 캐시는 나중에 읽어 Crawler에 필요한 간단한 HTML 문서를 만듭니다. 예: </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span> 요소는 제목 메타데이터 필드에 매핑이 있을 때만 생성됩니다. 마찬가지로 <span class="codeph"> &lt;body&gt; </span> 요소는 본문 메타데이터 필드에 매핑이 존재하는 경우에만 생성됩니다. </p> <p> <b>중요</b>: 사전 정의된 URL 메타 태그에 값을 할당할 수 없습니다. </p> <p>다른 모든 매핑의 경우, 원본 문서에서 찾은 데이터가 있는 각 필드에 대해 <span class="codeph"> &lt;meta&gt; </span> 태그가 생성됩니다. </p> <p>각 문서의 필드가 캐시에 추가됩니다. 캐시에 기록되는 각 문서에 대해 다음 예와 같이 링크가 생성됩니다. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>구성의 매핑에는 기본 키로 식별되는 필드가 하나 있어야 합니다. 이 매핑은 캐시에서 데이터를 가져올 때 사용되는 키를 형성합니다. </p> <p>Crawler는 URL <span class="codeph"> 인덱스를 인식합니다. </span> 스키마 접두사로, 로컬에서 캐시한 데이터에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>캐시된 문서 세트를 크롤링합니다. </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 인덱스: </span> 링크는 Crawler의 보류 목록에 추가되고 일반 크롤링 시퀀스에서 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>각 문서를 처리합니다. </p> </td> 
   <td colname="col3"> <p>각 링크의 키 값은 캐시의 항목에 해당하므로 각 링크를 크롤링하면 캐시에서 해당 문서의 데이터를 가져옵니다. 그런 다음 "assembled"를 HTML 이미지로 만들어 처리되고 인덱스에 추가합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 여러 속성 로드 구성 정보 {#section_4CC49C74EF294608A184E233F215ADFF}

모든 계정에 대해 여러 속성 로더 구성을 정의할 수 있습니다.

속성 로더를 추가할 때 선택적으로 기능 **[!UICONTROL Setup Maps]**&#x200B;을 사용하여 데이터 소스의 샘플을 다운로드할 수 있습니다. 그 자료는 적합성을 검토한다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> 속성 로더 유형 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>텍스트 </p> </td> 
   <td colname="col2"> <p>탭을 먼저 시도한 다음 세로 막대( <span class="codeph">)를 사용하여 구분 기호 값을 결정합니다 | </span>)와 마지막으로 쉼표( <span class="codeph"> , </span>)를 만듭니다. <span class="uicontrol"> 설정 맵 </span>을 클릭하기 전에 구분 기호 값을 이미 지정한 경우 해당 값이 대신 사용됩니다. </p> <p>가장 잘 맞는 구성표는 맵 필드에 적절한 태그 및 필드 값에 대한 추정이 입력됩니다. 또한 구문 분석된 데이터의 샘플링이 표시됩니다. 파일에 헤더 행이 포함되어 있음을 알고 있는 경우 첫 번째 행 <span class="uicontrol"> 헤더를 선택해야 합니다. </span> 설정 함수는 이 정보를 사용하여 결과 맵 항목을 더 잘 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>피드 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드하고 간단한 XML 구문 분석을 수행합니다. </p> <p>결과 XPath 식별자는 맵 테이블의 태그 행에 표시되고 필드의 비슷한 값이 표시됩니다. 이러한 행은 사용 가능한 데이터만 식별하고 더 복잡한 XPath 정의를 생성하지 않습니다. 그러나 XML 데이터를 설명하고 Itemtag를 식별하므로 여전히 유용합니다. </p> <p> <p>참고:  설정 맵 함수는 전체 XML 소스를 다운로드하여 분석을 수행합니다. 파일이 큰 경우 이 작업이 시간 초과될 수 있습니다. </p> </p> <p>성공하면 이 함수는 사용 가능한 모든 XPath 항목을 식별하며, 이 중 많은 항목은 사용하지 않는 것입니다. 결과 맵 정의를 검토하고 필요하지 않거나 원하는 정의를 제거해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>파일 파서가 전체 파일을 메모리로 읽으려고 하므로 큰 XML 데이터 집합에서 설정 맵 기능이 작동하지 않을 수 있습니다. 따라서 메모리 부족 상태를 경험할 수 있습니다. 하지만 인덱싱 시 동일한 문서를 처리하는 경우 메모리로 읽히지 않습니다. 대신 대용량 문서는 &quot;이동 중&quot;으로 처리되며 메모리로 완전히 읽지는 않습니다.

## 속성 로더를 추가할 때 미리 보기 사용 정보 {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

속성 로더 데이터는 인덱스 작업 전에 로드됩니다.

속성 로더를 추가할 때 선택적으로 **[!UICONTROL Preview]** 기능을 사용하여 데이터를 저장하는 것처럼 유효성을 확인할 수 있습니다. 구성에 대해 테스트를 실행하지만 구성을 계정에 저장하지 않습니다. 테스트는 구성된 데이터 소스에 액세스합니다. 그러나 다운로드 캐시를 임시 위치에 씁니다. 인덱싱 Crawler가 사용하는 주 캐시 폴더와 충돌하지 않습니다.

미리 보기는 **Acct:IndexConnector-Preview-Max-Documents**&#x200B;에 의해 제어된 5개의 문서만 처리합니다. 미리 본 문서는 인덱싱 Crawler에 표시될 때 소스 형태로 표시됩니다. 이 디스플레이는 웹 브라우저의 &quot;소스 보기&quot; 기능과 비슷합니다. 표준 탐색 링크를 사용하여 미리 보기 세트에서 문서를 탐색할 수 있습니다.

이러한 문서는 직접 처리되고 캐시에 다운로드되지 않으므로 미리 보기에서 XML 구성을 지원하지 않습니다.

## 속성 로더 정의 추가 {#task_A735E5EF763343A9B675E1A3B09AFDBC}

각 속성 로더 구성은 데이터 소스 및 매핑을 정의하여 해당 소스에 대해 정의된 데이터 항목을 인덱스의 메타데이터 필드에 연결합니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

고객이 새 정의 및 활성화된 정의의 효과를 보려면 사이트 인덱스를 다시 만드십시오.

**속성 로더 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Stage Attribute Loader Definitions] 페이지에서 **[!UICONTROL Add New Attribute Loader]** 을 클릭합니다.
1. [!DNL Attribute Loader Add] 페이지에서 원하는 구성 옵션을 설정합니다. 사용 가능한 옵션은 선택한 **[!UICONTROL Type]**&#x200B;에 따라 다릅니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>이름 </p> </td> 
      <td colname="col2"> <p>속성 로더 구성의 고유한 이름입니다. 영숫자를 사용할 수 있습니다. "_" 및 "-" 문자도 허용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p>데이터의 소스. 선택하는 데이터 소스 유형은 <span class="wintitle"> 속성 로더 추가 </span> 페이지에서 사용할 수 있는 결과 옵션에 영향을 줍니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> 텍스트 </span> <p>단순 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 기타 일관되게 구분된 형식. 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p>각 값 또는 열을 열 번호가 참조하는 메타데이터 필드에 1부터 매핑할 수 있습니다. </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> 피드 </span> <p>여러 "행" 정보를 포함하는 기본 XML 문서를 다운로드합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형: 텍스트</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>구성을 사용할 "켜기"로 설정합니다. 또는 구성을 "해제"하여 사용 여부를 방지할 수 있습니다. </p> <p> <b>참고</b>: 비활성화된 속성 로더 구성이 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예와 같이 데이터 소스 문서에 대한 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>또는  </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>단순 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 다른 일관적으로 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용할 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTP 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTPS 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간 초과 </p> </td> 
      <td colname="col2"> <p>FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 시간 제한(초)을 지정합니다. 이 값은 30에서 300 사이여야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다시 시도 </p> </td> 
      <td colname="col2"> <p>실패한 FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 최대 다시 시도 횟수를 지정합니다. 이 값은 0에서 10 사이여야 합니다. </p> <p>값이 0이면 다시 시도되지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>인코딩 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일에 사용되는 문자 인코딩 시스템을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구분 기호 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일의 각 필드를 표시하는 데 사용할 문자를 지정합니다. </p> <p>쉼표 문자( <span class="codeph"> , </span>)는 구분 기호의 예입니다. 쉼표는 지정된 데이터 소스 파일에서 데이터 필드를 구분하는 데 도움이 되는 필드 구분 기호로 작동합니다. </p> <p><span class="uicontrol"> 탭을 선택하십시오. </span> 가로 탭 문자를 구분 기호로 사용하려면 다음을 수행하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 행의 머리글 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일의 첫 번째 행에 데이터가 아닌 머리글 정보만 포함함을 나타냅니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부실 일 </p> </td> 
      <td colname="col2"> <p>속성 로더 데이터의 다운로드 사이의 최소 간격을 설정합니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 인덱스 트리거된 다운로드는 무시됩니다. 이 값을 기본값인 1로 설정하면 속성 로더 데이터가 24시간 내에 두 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 인덱스는 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정합니다. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 열 </span> <p> 열 번호를 지정합니다. 첫 번째 열은 1(1)입니다. 각 열에 대한 새 맵 행을 추가하려면 <span class="wintitle"> 작업 </span> 아래에서 <span class="uicontrol"> + </span> 를 클릭합니다. </p> <p>데이터 소스의 각 열을 참조할 필요가 없습니다. 대신 값을 건너뛰도록 선택할 수 있습니다. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>가 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>필요한 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 필터링 스크립트 </span>에 사용되는 컨텐츠를 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보 </a>를 참조하십시오. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 필드만 기본 키로 식별됩니다. 이 필드는 속성 로더 데이터를 인덱스의 해당 문서와 일치시키기 위해 "외래 키"로 사용됩니다. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML을 분리하시겠습니까?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형: 피드</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>구성을 사용할 "켜기"로 설정합니다. 또는 구성을 "해제"하여 사용 여부를 방지할 수 있습니다. </p> <p> <b>참고</b>: 비활성화된 속성 로더 구성이 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예와 같이 데이터 소스 문서에 대한 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>또는  </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 정보의 "행"을 포함하는 기본 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용할 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTP 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTPS 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 개별 XML 라인을 식별하는 데 사용할 수 있는 XML 요소를 식별합니다. </p> <p>예를 들어, Adobe XML 문서의 다음 피드 조각에서 Itemtag 값은 <span class="codeph"> 레코드 </span>입니다. </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>상호 참조 필드 이름 </p> </td> 
      <td colname="col2"> <p>속성 로더 구성 데이터에 값을 조회 "키"로 사용하는 메타데이터 필드를 지정합니다. 선택한 값이 없는 경우(<b>—None—</b>), 이 구성의 데이터는 등급 계산에서 사용할 수 없습니다(<b>규칙</b> &gt; <b>등급 규칙</b> &gt; <b>규칙 편집</b>). 값을 선택하면 이 필드의 값이 이 구성의 데이터로 사이트 검색/머천다이징 문서를 상호 참조하는 데 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부실 일 </p> </td> 
      <td colname="col2"> <p>속성 로더 데이터의 다운로드 사이의 최소 간격을 설정합니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 인덱스 트리거된 다운로드는 무시됩니다. 이 값을 기본값인 1로 설정하면 속성 로더 데이터가 24시간 내에 두 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 인덱스는 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>XPath 표현식을 사용하여 XML-요소-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> 태그 </span> <p>구문 분석된 XML 데이터의 XPath 표현을 지정합니다. 위의 Adobe XML 문서 예제 를 사용하여 Itemtag 옵션에서 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 <span class="codeph"> displayurl </span> 속성은 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 특성이 <span class="codeph"> 제목 </span>인 <span class="codeph"> 레코드 </span> 요소에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> 제목 </span>에 매핑됩니다. </span></p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph"> 레코드 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> desc </span>에 매핑됩니다.</span> </span></p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph"> 메타데이터 </span> 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 속성은 이름 특성이 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함되어 있으며 메타데이터 필드 <span class="codeph"> 본문 </span>에 매핑됩니다. </span></p> </li> 
        </ul> </p> <p>XPath는 상대적으로 복잡한 표기법입니다. 자세한 내용은 다음 위치에서 확인할 수 있습니다. </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xml/xpath_intro.asp </a> 을 참조하십시오. </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> 필드 </span> <p>생성된 각 <span class="codeph"> &lt;meta&gt; </span> 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>가 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>필요한 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 필터링 스크립트 </span>에서 사용하는 컨텐츠를 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보 </a>를 참조하십시오. </p> <p>속성 로더가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 이 필드에는 <span class="wintitle"> 허용 목록 </span> 속성이 설정되어 있습니다. 이 경우 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 필드만 기본 키로 식별됩니다. 이 필드는 속성 로더 데이터를 인덱스의 해당 문서와 일치시키기 위해 "외래 키"로 사용됩니다. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTML을 분리하시겠습니까?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) **[!UICONTROL Setup Maps]** 을 클릭하여 데이터 소스의 샘플을 다운로드합니다. 그 자료는 적합성을 검토한다.
1. **[!UICONTROL Add]** 을 클릭하여 [!DNL Attribute Loader Definitions] 페이지에 구성을 추가합니다.
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]** 을 클릭합니다.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 속성 로더 정의 편집 {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

정의한 기존 속성 로더를 편집할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

속성 로더 이름 또는 [!DNL Type] 드롭다운 목록에서 유형 과 같이 일부 속성 로더 옵션을 변경할 수 있는 것은 아닙니다.

**속성 로더 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 제목에서 설정을 변경할 속성 로더 정의 이름에 대해 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Edit] 페이지에서 원하는 옵션을 설정합니다.

   [속성 로더 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)에 있는 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]** 을 클릭합니다.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 속성 로더 정의 복사 {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

기존 속성 로더 정의를 복사하여 만들려는 새 속성 로더의 기준으로 사용할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

속성 로더 정의를 복사할 때 기본적으로 복사된 정의가 비활성화됩니다. 정의를 활성화하거나 &quot;켜기&quot;하려면 [!DNL Attribute Loader Edit] 페이지에서 해당 정의를 편집하고 **[!UICONTROL Enable]** 를 선택해야 합니다.

[속성 로더 정의 편집](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)을 참조하십시오.

**속성 로더 정의를 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 제목 아래에서 설정을 복제할 속성 로더 정의 이름에 대해 **[!UICONTROL Copy]** 를 클릭합니다.
1. [!DNL Attribute Loader Copy] 페이지에서 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Copy]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 속성 로더 정의 이름 바꾸기 {#task_58D5DFD7EBC04111BCB91118E4440DB4}

기존 속성 로더 정의의 이름을 변경할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

**속성 로더 정의 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 제목에서 변경할 속성 로더 정의 이름에 대해 **[!UICONTROL Rename]** 를 클릭합니다.
1. [!DNL Attribute Loader Rename] 페이지의 [!DNL Name] 필드에 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Rename]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 속성 로더 데이터 로드 {#task_2F3C55189B0A4049AB2113F2291CC181}

구성된 속성 로더 데이터를 사이트 검색/머천다이징에 다운로드할 수 있습니다.

[!DNL Data Load] 페이지에는 마지막 속성 로더 데이터 로드 작업의 상태에 대한 다음 정보가 표시됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>상태 필드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 시도에 대한 성공 또는 실패를 나타냅니다. 또는 이미 진행 중인 데이터 로드 작업의 상태를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시작 시간 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 작업이 시작된 날짜 및 시간을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중지 시간 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 작업의 완료 날짜 및 시간을 표시합니다. 또는 현재 데이터 로드 작업이 진행 중임을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**속성 로더 데이터를 로드하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL Load Attribute Loader Data]** 을 클릭합니다.
1. **[!UICONTROL Attribute Loader Data Load]** 페이지에서 다음 중 하나를 수행합니다.

   * 로드 작업을 시작하려면 **[!UICONTROL Start Load]** 를 클릭하십시오.

      데이터 로드 작업 중에&#x200B;**Progress** 행은 진행 상태에 대한 정보를 제공합니다.

   * 로드 작업을 중지하려면 **[!UICONTROL Stop Load]** 을 클릭하십시오.

1. **[!UICONTROL Close]** 을 클릭하여 [!DNL Attribute Loader Definitions] 페이지로 돌아갑니다.

## 속성 로더 데이터 미리 보기 {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

미리 보기 를 사용하여 가장 최근에 로드된 속성 로더 데이터를 볼 수 있습니다.

테이블의 행 열에는 각 데이터 행에 대한 숫자가 표시되며, 속성 로더 값이 로드되는 원래 순서를 나타냅니다.

나머지 열에는 각 항목과 연결된 값이 표시됩니다.

테이블이 비어 있으면 속성 로더 데이터를 아직 로드하지 않았음을 의미합니다. [!DNL Attribute Loader Data Preview] 페이지를 닫은 다음 속성 로더 데이터를 로드할 수 있습니다.

[속성 로더 데이터 로드](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.

**속성 로더 데이터를 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지의 [!DNL Actions] 열에서 다운로드한 데이터를 보려는 구성의 **[!UICONTROL Preview]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Data Preview] 페이지에서 페이지 상단과 하단에 있는 탐색 및 보기 옵션을 사용하여 데이터를 봅니다.

   데이터를 내림차순이나 오름차순으로 정렬하려면 표에 있는 열 머리글을 클릭합니다.
1. 다음 중 하나를 수행합니다.

   * **[!UICONTROL Download to Desktop]** 을 클릭하여 테이블을 다운로드하고 .xlt 파일로 저장합니다.
   * 속성 로더 데이터 미리 보기를 마치면 페이지를 닫고 이전에 본 페이지로 돌아갑니다.

## 속성 로더 정의 설정 보기 {#task_EA99A9694FE948ADA82C1DBA0667851B}

기존 속성 로더 정의의 구성 설정을 검토할 수 있습니다.

속성 로더 정의가 [!DNL Attribute Loader Definitions] 페이지에 추가되면 해당 유형 설정을 변경할 수 없습니다. 대신 정의를 삭제한 다음 새 정의를 추가해야 합니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

**속성 로더 정의 설정을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 제목 아래에서 설정을 검토하거나 편집할 속성 로더 정의 이름에 대해 **[!UICONTROL Edit]** 를 클릭합니다.

## 가장 최근 속성 로더 데이터 로드에서 로그 보기 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

[!DNL View Log] 을 사용하여 최신 다운로드 프로세스의 속성 로더 데이터 로그 파일을 검사할 수 있습니다. 로그 보기를 사용하여 실행 중인 다운로드를 모니터링할 수도 있습니다.

[속성 로더 데이터 로드](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.

**가장 최근 속성 로더 데이터 로드에서 로그를 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL View Log]** 을 클릭합니다. 로그 페이지,
1. [!DNL Attribute Loader Data Log] 페이지에서 페이지 상단과 하단에 있는 탐색 및 보기 옵션을 사용하여 로그 정보를 봅니다.
1. 완료되면 페이지를 닫고 [!DNL Attribute Loader Definitions] 페이지로 돌아갑니다.

## 속성 로더 정의 삭제 {#task_E8980F66888B476E98C228C1D307EDF8}

더 이상 필요하거나 사용하지 않는 기존 속성 로더 정의를 삭제할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 계정에 Attribute Loader를 활성화해야 할 수 있습니다.

**속성 로더 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지의 [!DNL Actions] 열 제목에서 제거할 속성 로더 정의 이름에 대해 **[!UICONTROL Delete]** 를 클릭합니다.
1. [!DNL Attribute Loader Delete] 페이지에서 **[!UICONTROL Delete]** 을 클릭합니다.
