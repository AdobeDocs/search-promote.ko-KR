---
description: 메타데이터 메뉴를 사용하여 검색 정의 및 색인 주입을 사용자 정의합니다.
seo-description: 메타데이터 메뉴를 사용하여 검색 정의 및 색인 주입을 사용자 정의합니다.
seo-title: 메타데이터 메뉴 정보
solution: Target
subtopic: Metadata
title: 메타데이터 메뉴 정보
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '8039'
ht-degree: 1%

---


# 메타데이터 메뉴 {#about-the-metadata-menu} 정보

메타데이터 메뉴를 사용하여 검색 정의 및 색인 주입을 사용자 정의합니다.

## 정의 정보 {#concept_AE48035C210145169BE067D396975620}

[!DNL Definitions]을 사용하여 고객이 검색 쿼리를 제출할 때 고려되는 HTML 및 메타데이터 필드의 내용과 관련성을 사용자 지정할 수 있습니다.

이미 사전 정의된 필드를 편집할 수 있습니다. 또는 메타데이터 태그 컨텐츠를 기반으로 새 사용자 정의 필드를 만들 수도 있습니다. 각 정의는 [!DNL Staged Definitions] 페이지의 한 줄에 표시됩니다.

[데이터 보기 정보](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)도 참조하십시오.

## 새 메타 태그 필드 {#task_6DF188C0FC7F4831A4444CA9AFA615E5} 추가

고유한 메타데이터 태그 필드를 정의하고 추가할 수 있습니다.

새 메타 태그 정의의 효과가 고객에게 표시되기 전에 사이트 인덱스를 다시 만들어야 합니다.

**새 메타 태그 필드를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지에서 **[!UICONTROL Add New Field]**&#x200B;을 클릭합니다.
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
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> 이름에는 영숫자만 포함되어야 합니다. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> 대시는 이름에 사용할 수 있지만 공백은 사용할 수 없습니다. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> 최대 20자의 이름을 입력할 수 있습니다. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> 이름은 대/소문자를 구분하지 않지만 입력한 대로 정확하게 표시되고 저장됩니다. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> <span class="wintitle"> 단계 정의 </span> 페이지의 표에 표시된 대로 사전 정의된 필드에 존재하는 이름은 사용할 수 없습니다. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> 단어 "any"는 사용자 정의 필드 이름의 값으로 사용할 수 없습니다. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> 사전 정의된 필드의 이름은 편집할 수 없습니다. </li> 
      </ul> </p> <p> 필드 이름 예: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> author </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> 게시 날짜 </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> 야생적인 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>메타 태그 이름 </p> </td> 
      <td colname="col2"> <p>정의된 필드와 관련된 컨텐츠를 결정합니다. </p> <p>이름 목록은 최대 255자까지 사용할 수 있습니다. 또한 HTML 메타 태그의 name 속성에 허용되는 모든 문자를 이름에 포함할 수 있습니다. </p> <p>단일 필드 정의에서 여러 메타 태그를 지정할 수 있습니다. </p> <p>여러 값은 쉼표로 구분해야 하며, 지정된 웹 페이지에서 찾을 수 있는 가장 왼쪽 메타 태그 이름이 우선합니다. </p> <p>예를 들어 "auth"라는 필드를 정의했다고 가정합니다. 필드 이름에 연결된 메타 태그 "author, dc.author"가 있습니다. 이 경우 "작성자" 메타 태그의 컨텐츠는 인덱싱되어 "dc.author"의 컨텐츠가 검색됩니다. 두 메타 태그가 웹 페이지에 모두 표시됩니다. </p> <p>사용자 정의 필드에는 정의에 하나 이상의 메타 태그 이름이 있어야 합니다. 사전 정의된 필드에는 연관된 메타 태그가 없어도 됩니다. 하지만 하나 이상의 메타 태그가 지정된 경우 메타 태그의 컨텐츠는 각 태그의 현재 데이터 소스를 재정의합니다. </p> <p>예를 들어 메타 태그 "dc.title"이 미리 정의된 "title" 필드와 연결되어 있으면 "dc.title" 메타 태그의 컨텐츠는 
      특정 문서에 대한 <code>
        &lt;title&gt; 
      </code> 태그입니다. </p> <p>이러한 예로는 다음과 같은 경우가 있습니다. </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> 독점 태그 </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>데이터 유형 </p> </td> 
      <td colname="col2"> <p>모든 필드에는 텍스트, 번호, 날짜, 버전, 등급 또는 위치와 같은 관련 데이터 유형이 있습니다. 이 데이터 유형은 필드의 컨텐츠가 인덱싱되고, 검색되고, 선택적으로 정렬되는 방법을 결정합니다. </p> <p>필드 정의를 만든 후에는 데이터 유형을 변경할 수 없습니다. </p> <p>다음 정보를 사용하여 필드에 포함된 정보와 관련된 데이터 유형을 선택할 수 있습니다. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> 텍스트  </span> 데이터 유형 필드는 문자 문자열로 취급됩니다. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> 숫자  </span> 데이터 유형 필드는 정수 또는 부동 소수점 숫자 값으로 처리됩니다. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> 날짜  </span> 데이터 유형 필드는 날짜/시간 지정자로 처리됩니다. 새 필드를 추가하거나 편집할 때 허용되는 날짜/시간 형식을 사용자 지정할 수 있습니다. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> 버전  </span> 데이터 유형 필드는 자유형 숫자 데이터로 취급됩니다. 예를 들어 1.2.3은 1.2.2 전에 정렬합니다. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> 등급  </span> 데이터 유형 필드는 검색 결과의 등급/관련성 계산에 추가적인 영향을 준다는 점을 제외하고 "숫자" 유형 필드와 동일하게 처리됩니다. <p><a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">등급 규칙 정보</a>를 참조하십시오 . </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> 위치  </span> 데이터 유형 필드는 세계 어디에서나 물리적 위치로 처리됩니다. 허용되는 위치 형식은 다음과 같습니다. <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> DDD 또는 DDDD-DDD 형식의 5 또는 9자리 우편 번호. 여기서 각 "D"는 0-9자리 숫자입니다. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> DDD 형식의 3자리 영역 코드. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> DD.DDD DDD DDD.DDD 형식의 위도/경도 쌍입니다. 여기서 첫 번째 숫자는 위도를 지정하고 두 번째 숫자는 경도를 지정합니다. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>허용 목록 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 텍스트 </span> 또는 <span class="uicontrol"> 번호 </span>를 선택한 경우에만 사용할 수 있습니다. </p> <p>이 필드의 메타데이터 컨텐츠에 구분된 값을 별도로 색인화합니다. </p> <p>예를 들어 "허용 목록"을 선택하면 "빨강, 노랑, 녹색, 파랑" 내용이 4개의 개별 값으로 처리되고 1개가 아닌 4개가 개별 값으로 처리됩니다. 이 방법은 범위 검색( 
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
      </code>. </p> <p>버전 데이터 유형을 선택한 경우에는 사용할 수 없습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 동적 패싯 </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>참고: 이 기능은 기본적으로 활성화되어 있지 않습니다. 기술 지원에 문의하여 사용할 수 있도록 활성화합니다. 활성화되면 사용자 인터페이스에 표시됩니다. </p> </p> <p>식별된 패싯을 동적으로 설정합니다. </p> <p>패싯은 메타 태그 필드의 맨 위에 만들어집니다. 메타 태그 필드는 Adobe Search &amp; Promote의 낮은 수준의 핵심 검색 레이어입니다. 반면에 패싯은 Adobe Search &amp; Promote의 높은 수준의 프레젠테이션 레이어인 GS(Guided Search)의 일부입니다. 패싯은 고유한 메타 태그 필드를 가지지만, 메타 태그 필드는 패싯에 대해 아무것도 알지 못합니다. </p> <p><a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 동적 패싯 정보 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중복 제거 허용 </p> </td> 
      <td colname="col2"> <p>이 필드에 대해 데이터 중복 제거를 활성화하려면 이 옵션을 선택합니다. 즉, 이 필드를 
        <code>
          sp_dedupe_field 
        </code> CGI 매개 변수를 검색합니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI 매개 변수 검색 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테이블 이름 </p> </td> 
      <td colname="col2"> <p>지정된 필드를 지정된 테이블 이름과 영구적으로 연결합니다. </p> <p>코어 검색 CGI 매개 변수 또는 템플릿 태그 내에서 이러한 필드가 언급될 때마다 테이블 이름이 자동으로 제공됩니다. 이 기능을 사용하면 테이블 일치를 통한 동적 패싯을 선택할 수 있지만 원하는 경우 비동적 패싯 필드에 사용할 수도 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>목록 구분 기호 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 허용 목록 </span>을(를) 선택한 경우에만 사용할 수 있습니다. </p> <p>개별 목록 값을 구분하는 문자를 지정합니다. 여러 문자를 지정할 수 있으며 각 문자는 값 구분 문자로 처리됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본적으로 검색 </p> </td> 
      <td colname="col2"> <p>이 옵션을 선택하면 주어진 검색 쿼리에 필드를 명시적으로 지정하지 않아도 필드 내용이 검색됩니다. 이 옵션을 선택 취소하면 요청 시 필드가 검색됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>수직 업데이트 필드 </p> </td> 
      <td colname="col2"> <p> <p>참고: 이 기능은 기본적으로 활성화되어 있지 않습니다. 기술 지원에 문의하여 사용할 수 있도록 활성화합니다. 활성화되면 사용자 인터페이스에 표시됩니다. </p> </p> <p>식별된 필드를 수직 업데이트 필드로 설정합니다. </p> <p>수직 업데이트 필드는 수직 업데이트 프로세스( <span class="uicontrol"> 인덱스 </span> &gt; <span class="uicontrol"> 수직 업데이트 </span>)를 통해 업데이트할 후보자입니다. 수직 업데이트가 수행되는 방식으로 인해 이러한 필드의 내용은 자유 텍스트 검색에서 검색할 수 없습니다. 이 옵션을 선택하면 색인 작업 중에 이 필드의 내용이 "word" 색인에 추가되지 않습니다. 또한 수직 업데이트 작업 중에 이 필드를 업데이트할 수 있습니다. </p> <p>수직 업데이트에 대한 자세한 내용은 <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 수직 업데이트 </a> 정보를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>연관성 </p> </td> 
      <td colname="col2"> <p>사전 정의된 필드와 사용자 정의 필드의 연관성을 편집할 수 있습니다. </p> <p>관련성은 1-10 비율로 지정됩니다. 1을 설정하는 것은 관련성이 가장 적고 관련성이 가장 높은 10을 의미합니다. 이 값들은 소프트웨어가 각 필드에 있는 쿼리와 일치하는 것으로 간주할 때 고려됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>정렬 </p> </td> 
      <td colname="col2"> <p>결과를 
        <code>
          sp_s 
        </code> CGI 매개 변수를 검색합니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> CGI 매개 변수 검색 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>언어 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span>, <span class="uicontrol"> 번호 </span> 또는 <span class="uicontrol"> 날짜 </span>를 선택한 경우에만 사용할 수 있습니다. </p> <p>이 필드에 대한 날짜, 번호 및 등급 값을 인덱싱할 때 적용되는 언어 및 로케일 규칙을 제어합니다. </p> <p>계정 언어를 적용하도록 선택할 수 있습니다(언어 &gt; 단어 및 언어). 또는 각 숫자 또는 날짜 값이 포함된 문서와 연결된 언어 또는 특정 언어를 적용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>날짜 형식 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span>가 선택된 경우에만 사용할 수 있습니다. </p> <p>이 필드에 대한 날짜 값을 인덱싱할 때 인식되는 날짜 형식을 제어합니다. </p> <p>각 날짜 필드에 대해 날짜 형식 문자열의 기본 목록이 제공됩니다. 목록에 추가하거나 사이트의 요구에 맞게 목록을 편집할 수 있습니다. </p> <p><a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> 날짜 형식 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트 날짜 형식 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span>가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>지정한 날짜 형식을 미리 보고 형식이 올바른지 확인할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간대 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 날짜 </span>가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>표준 시간대를 지정하지 않는 이 필드에 대한 날짜 값을 인덱싱할 때 적용되는 예상 표준 시간대를 제어합니다. </p> <p>예를 들어 계정 시간대가 "미국/로스앤젤레스"로 설정되어 있고 <span class="uicontrol"> 계정 시간대 사용 </span>을 선택하면 지정된 시간대가 없는 다음 메타 날짜 값은 태평양 시간인 것처럼 취급되고 일광 절약 시간이 계산됩니다. </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>가장 중요하지 않은 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span>이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서의 최소 등급을 나타내는 등급 값을 제어합니다. </p> <p>문서 등급 범위가 가장 낮은 등급에 대해 0에서 가장 높은 등급에 대해 10까지 변경되면 이 값을 0으로 설정합니다. </p> <p>문서 등급이 가장 높은 등급에 대해 1부터 가장 낮은 등급에 대해 10까지 포함되는 경우 이 값을 10으로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span>이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서에 이 등급 필드에 대해 정의된 메타 태그가 포함되어 있지 않을 경우 사용되는 등급 값을 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>가장 중요한 등급 값 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 등급 </span>이 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>문서의 최대 등급을 나타내는 등급 값을 제어합니다. </p> <p>문서 등급 범위가 가장 낮은 등급에 대해 0에서 가장 높은 등급에 대해 10까지 변경되면 이 값을 10으로 설정합니다. </p> <p>문서 등급 범위가 가장 높은 등급에 대해 1에서 가장 낮은 등급에 대해 10까지 변경되면 이 값을 1로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 단위 </p> </td> 
      <td colname="col2"> <p>데이터 유형 <span class="uicontrol"> 위치 </span>가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p>근접 검색을 위한 거리 값 처리를 제어합니다. </p> <p>기본 단위를 <span class="uicontrol"> Miles </span>로 설정하면 이 필드에 적용되는 근접 검색 최소/최대 거리 기준( 
      <code>
        sp_q_min[_#] 
      </code> 또는 
      <code>
        sp_q_max[_#] 
      </code> CGI 매개 변수 검색)은 마일(킬로미터)로 처리됩니다. </p> <p>또한 이 옵션은 
      근접 검색 출력 필드에 적용할 때 <code>
        &lt;Search-Display-Field&gt; 
      </code> 검색 결과 템플릿 태그 </p> <p><a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> 근접 검색 </a> 정보를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 설명을 만드시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 번호 </span>가 데이터 유형으로 선택된 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 디자인 </span> &gt; <span class="uicontrol"> 탐색 </span> &gt; <span class="uicontrol"> 패싯 </span>에서 사용할 수 있도록 필드 범위 설명 자동 만들기를 제어합니다. </p> <p><a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> 패싯 </a> 정보를 참조하십시오. </p> <p> <p>참고: 이 필드에 <span class="uicontrol"> 수직 업데이트 필드 </span>가 선택되어 있으면 세로 업데이트 중에 생성된 필드 범위 설명 필드가 업데이트됩니다. 그러나 <span class="uicontrol"> 범위 필드 </span>에 식별된 필드에도 <span class="uicontrol"> 수직 업데이트 필드 </span>가 선택되어 있는 것이 좋습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 필드 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>가 선택된 경우에만 사용할 수 있습니다. </p> <p>현재 필드에 대한 범위 설명으로 업데이트할 <span class="uicontrol"> 텍스트 </span> 필드. 이 목록에는 필드 범위 생성을 위해 다른 필드와 함께 아직 사용되지 않는 <span class="uicontrol"> 텍스트 </span> 필드가 모두 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>범위 값 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>필드 범위 설명을 만들 때 사용할 데이터 포인트의 공백으로 구분된 목록입니다. 예: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>이러한 값을 원하는 순서대로 입력할 수 있습니다. 값이 정렬되고 저장되기 전에 중복된 값이 제거됩니다. 음수와 정수가 아닌 값을 지정할 수도 있습니다. </p> <p>이 필드의 각 값에 대해 다음을 수행합니다. 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;)보다 작으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다. </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;=)보다 크거나 같으면 <span class="uicontrol"> "보다 큼" 형식 </span>이 사용됩니다. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">그렇지 않으면 필드 값이 두 연속된 <span class="uicontrol"> 범위 값 </span>(보다 큼(&gt;) 보다 작음 값(&lt;=) 보다 작음) 사이에 있고 <span class="uicontrol"> 중간 형식 </span>이 사용되는 위치에서 "range"가 발견되었습니다. </li> 
    </ul> </p> <p>예를 들어 위의 예제 값 세트는 값에 대한 설명 집합을 정의합니다. 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">10 미만 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">10 이상 20 미만 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">20 이상 50 미만 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">50보다 크거나 같고 100보다 작음 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">100 이상 1000 미만 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">10000보다 크거나 같음 </li> 
      </ul> </p> <p><span class="uicontrol"> 보다 큼 사용 테스트를 참조하십시오. </span> 를 클릭하여 이러한 테스트가 수행되는 방식을 변경합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"보다 작음" 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p><span class="uicontrol"> 범위 값 </span>에 있는 가장 작은 값보다 작은 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 가장 작은 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~N~ </span>을 사용하여 표시됩니다. 예: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>또는: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>일반적으로 값의 형식은 "있는 그대로"(즉, <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 정의) 및 제공된 값 1인 경우, 생성된 범위 설명은 "5보다 작음"과 같습니다. 대신 "4.99 이하"로 하려면 <span class="uicontrol"> 정밀도 </span>를 <span class="uicontrol"> 2 </span>로 설정하고 다음 형식을 사용하십시오. </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p><span class="uicontrol"> "보다 작음" 형식 </span>에서 소문자 <span class="uicontrol"> ~n~ </span>은 <span class="uicontrol"> 정밀도 </span> 설정에 따라 <i>down</i>이(가) 반올림되도록 합니다. </p> <p>참고:범위 설명에 숫자 자리 표시자를 포함하려면, 예를 들어, 백슬래시(\) 접두어로 지정합니다.<span class="uicontrol"> \~N~ </span> 또는 <span class="uicontrol"> \~n~ </span>. 백슬래시 문자를 포함하려면 다른 백슬래시와 함께 지정합니다(예:<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중간 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>이 템플릿은 <span class="uicontrol"> 범위 값 </span>에 있는 가장 작은 값과 가장 큰 값 사이의 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 지정된 범위의 경우 낮은 범위 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~L~ </span>을 사용하여 표현되며 높은 범위 값은 토큰 <span class="uicontrol"> ~H~ </span>을 사용하여 표현됩니다. 예: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>또는: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>또는: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>일반적으로 값의 형식은 "있는 그대로"(즉, <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 정의) 및 제공된 값 8인 경우, 생성된 범위 설명은 "5에서 10 사이"와 같은 것일 수 있습니다. 대신 "5에서 9.99 사이"로 지정하고 싶은 경우, 높은 값이 <i>아래쪽</i>으로 조정된 상태에서 <span class="uicontrol"> 정밀도 </span> <span class="uicontrol"> 2 </span>로 설정하고 다음 형식을 사용합니다. </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>마찬가지로 <span class="uicontrol"> 정밀도 </span> 설정에 따라 <span class="uicontrol"> ~L~ </span>을(를) <span class="uicontrol"> ~l~</span>으로 대체하여 더 낮은 값을 <i>upwards</i>로 조정할 수 있습니다. 이것은 다음과 같은 정의를 의미합니다. </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p><span class="uicontrol"> 정밀도 </span> 값이 <span class="uicontrol"> 2 </span>이면 "5.01에서 10 사이"가 생성됩니다. </p> <p>소문자 <span class="uicontrol"> ~l~ </span>은 <span class="uicontrol"> Precision </span> 설정에 따라 낮은 값이 <i>up</i>로 반올림되고, 소문자 <span class="uicontrol"> ~h~ </span>은 더 높은 값이 <i>다운</i>으로 반올림됩니다. </p> <p>참고:범위 설명에 숫자 자리 표시자를 포함하려면, 예를 들어, 백슬래시(\) 접두어로 지정합니다.<span class="uicontrol"> \~L~ </span> 또는 <span class="uicontrol"> \~h~ </span>. 백슬래시 문자를 포함하려면 다른 백슬래시와 함께 지정합니다(예:<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>"보다 큼" 형식 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>이 템플릿은 <span class="uicontrol"> 범위 값 </span>에 있는 가장 큰 값보다 큰 값에 대한 범위 설명을 지정하는 데 사용되는 템플릿입니다. 가장 큰 값은 숫자 자리 표시자 토큰 <span class="uicontrol"> ~N~ </span>을 사용하여 표시됩니다. 예: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>또는: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>일반적으로 값의 형식은 "있는 그대로"(즉, <span class="uicontrol"> 범위 값 </span> 정의("5 10 20"의 정의) 및 제공된 값 30의 경우, 생성된 범위 설명은 "20보다 큼"과 같습니다. 대신 "20.01 이상"이 되도록 하려면 <span class="uicontrol"> 정밀도 </span>을 <span class="uicontrol"> 2 </span>으로 설정하고 다음 형식을 사용하십시오. </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p><span class="uicontrol"> "보다 큼" 형식 </span>에서 소문자 <span class="uicontrol"> ~n~ </span>은 <span class="uicontrol"> 정밀도 </span> 설정에 따라 값이 반올림됩니다. <i>up</i>. </p> <p>참고:범위 설명에 숫자 자리 표시자를 포함하려면, 예를 들어, 백슬래시(\) 접두어로 지정합니다.<span class="uicontrol"> \~N~ </span> 또는 <span class="uicontrol"> \~n~ </span>. 백슬래시 문자를 포함하려면 다른 백슬래시와 함께 지정합니다(예:<span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>정밀도 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>소수점 오른쪽의 숫자 수를 지정하는 정수 값. 이것은 반올림 작업도 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>선행 0을 삭제하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택되고 0이 아닌 <span class="uicontrol"> 정밀도 </span> 값이 설정된 경우에만 사용할 수 있습니다. </p> <p>"0.50"을 ".50"으로 표시해야 합니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>후행 0을 삭제하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택되고 0이 아닌 <span class="uicontrol"> 정밀도 </span> 값이 설정된 경우에만 사용할 수 있습니다. </p> <p>"10.00"을 "10"으로 표시해야 합니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>수천 개의 구분자를 표시하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>"10000"을 "10,000"으로 표시해야 합니까? 로케일별 값이 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>0 값을 조정하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>반올림된 0개 값이 표시되면 <span class="uicontrol"> 정밀도 </span> 설정에 따라 반올림하거나 아래로 맞출까요? 예: "0.01"을 표시하시겠습니까? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>보다 큼을 사용하여 테스트하시겠습니까? </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>각 값이 <span class="uicontrol"> 범위 값 </span>에 있는 값과 비교되고 <i><b>내림차순</b></i> 순서로 처리되므로, 기본적으로 이 테스트가 성공되면 중지되고 보다 큼 또는 같음(&gt;=) 연산자를 사용하여 비교됩니다. 즉, <span class="uicontrol"> 범위 값 </span> 집합("10 20 50 100 1000"), 값 100은 100부터 1000 범위에 포함되며, 100은 실제로 100보다 큽니다. 50~100 범위의 값을 유지하려면 이 옵션을 선택하면 비교 시 보다 큼(&gt;) 연산자를 대신 사용합니다. </p> <p>예를 들어, 이 옵션을 선택하면 이 필드의 각 값에 대해 다음을 수행합니다. 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;=)보다 작거나 같으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다. </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;)보다 크면 <span class="uicontrol"> "보다 큼" 형식 </span>이 사용됩니다. </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">그렇지 않으면 필드 값이 연속된 <span class="uicontrol"> 범위 값 </span> 사이에 있고(&gt;= 보다 크거나 같음), 더 작은 값 (&lt;) 보다 작음)에 있고 <span class="uicontrol"> 중간 형식 </span>이 사용되는 범위가 있습니다. </li> 
    </ul> </p> <p>선택 취소 시: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 작은 값(&lt;)보다 작으면 <span class="uicontrol"> "보다 작음" 형식 </span>이 사용됩니다. </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">값이 <span class="uicontrol"> 범위 값 </span>에서 가장 큰 값(&gt;=)보다 크거나 같으면 <span class="uicontrol"> "보다 큼" 형식 </span>이 사용됩니다. </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">그렇지 않으면 필드 값이 연속된 <span class="uicontrol"> 범위 값 </span> 사이에 있고(보다 큼(&gt;) 더 작은 값과 더 큰 값보다 작거나 같음(&lt;=)) 사이에 있고 <span class="uicontrol"> 중간 형식 </span>이 사용됩니다 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트 </p> </td> 
      <td colname="col2"> <p><span class="uicontrol"> 범위 설명 만들기 </span>이 선택되어 있고 <span class="uicontrol"> 범위 필드 </span> 항목이 선택된 경우에만 사용할 수 있습니다. </p> <p>샘플 숫자 값을 제공하고 <span class="uicontrol"> 테스트 </span> 단추를 눌러 범위 필드가 어떻게 생성되는지 확인합니다. 생성된 범위 설명이 창에 표시됩니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)도 참조하십시오.
1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 사전 정의 또는 사용자 정의 메타 태그 필드 편집 {#task_0A7657B63596421BB6DB3ED44F827AB3}

사전 정의된 메타 태그의 특정 필드만 편집하거나 사용자가 정의한 메타 태그의 모든 필드를 편집할 수 있습니다.

메타 태그 변경 사항의 효과가 고객에게 표시되기 전에 사이트 인덱스를 다시 만들어야 합니다.

**사전 정의된 또는 사용자 정의 메타 태그 필드를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지의 테이블의 [!DNL Actions] 열에서 변경할 메타 태그 필드 이름의 행에서 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Pinned Keyword Results Manager] 페이지의 표에서 변경할 키워드 행에서 **[!UICONTROL Edit]**&#x200B;을 클릭합니다.
1. [!DNL Edit Field] 페이지에서 원하는 옵션을 설정합니다.

   사전 정의된 메타 태그 필드를 변경하도록 선택한 경우 일부 필드는 편집할 수 없습니다.

   [새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 사용자 정의 메타 태그 필드 {#task_9361EF38B5E743038B6672FA6CF70FD3} 삭제

더 이상 필요하거나 사용할 필요가 없는 사용자 정의 메타 태그 필드를 삭제할 수 있습니다.

사전 정의된 메타 태그 필드는 삭제할 수 없습니다. 그러나 특정 필드를 편집할 수는 있습니다.

[사전 정의된 또는 사용자 정의 메타 태그 필드 편집](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)을 참조하십시오.

삭제 메타 태그의 효과가 고객에게 표시되기 전에 사이트 인덱스를 다시 만들어야 합니다.

**사용자 정의 메타 태그 필드를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**&#x200B;를 클릭합니다.
1. [!DNL Definitions] 페이지의 표의 [!DNL User-defined fields] 섹션에서 제거할 메타 태그 필드 이름의 행에서 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. 확인 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 주사제 정보 {#concept_DA091920671948A0A893A26B3A2FAAE5}

페이지 자체를 편집하지 않고도 [!DNL Injections]을 사용하여 웹 페이지에 컨텐츠를 삽입할 수 있습니다.

&quot;target&quot; 또는 &quot;body&quot;와 같은 특정 인덱스 필드에 컨텐츠를 추가하거나 인덱스 컨텐츠를 새 값으로 바꿀 수 있습니다. 예를 들어 새 컨텐츠를 &quot;target&quot; 메타 태그 필드에 삽입한 경우 이 정보는 페이지 컨텐츠가 하드 코딩되는 것처럼 처리됩니다. 사이트 페이지에 해당 컨텐츠가 있는지 여부에 관계없이 사전 정의된 메타 태그 필드의 컨텐츠를 편집할 수 있습니다. 예를 들어 다음과 같은 사전 정의된 메타 태그 필드 이름의 내용을 편집할 수 있습니다.

* alt
* body
* charset
* date
* desk
* keys
* language
* target
* title
* url

## 테스트 필드 주입 작업 {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

[!DNL Staged Injections] 페이지에서 **[!UICONTROL Test]**&#x200B;을(를) 선택적으로 사용할 수 있습니다. 테스트 필드 이름(예: &quot;제목&quot; 또는 &quot;본문&quot;), 원래 필드 값(예: &quot;홈 페이지&quot;) 및 웹 사이트의 테스트 URL을 입력합니다. 참조에 대한 결과 값이 표시됩니다. 테스트 중에는 현재 값이 변경되지 않습니다.

## 필드 삽입 정의 작업 {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

삽입 정의에는 다음 양식이 있습니다.

```
append|replace field [regexp] URL value
```

`append|replace`, `field`, `URL`. 및 `value` 항목은 필수입니다. 한 줄에 하나의 삽입 정의를 입력합니다. 다음 예에는 6개의 서로 다른 삽입 정의가 포함되어 있습니다.

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
   <td colname="col1"> <p> <span class="codeph"> 첨부|바꾸기  </span> </p> </td> 
   <td colname="col2"> <p>"추가"를 선택하여 삽입 정의("Adobe:문의" 또는 "지금 판매 중!" 위의 예에서)를 기존 필드의 컨텐츠에 추가합니다. "바꾸기"를 선택하여 기존 필드 내용을 정의된 값으로 덮어씁니다. 현재 필드에 내용이 없으면, 사용된 옵션(추가 또는 바꾸기)에 상관없이 정의된 값이 자동으로 추가됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 필드에서 하나의 URL 매개 변수를 지정하십시오 </span> </p> </td> 
   <td colname="col2"> <p>필드 이름은 필수입니다. 다음은 사용할 수 있는 10개의 사전 정의된 필드 이름입니다. </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt  </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date  </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desk  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> keys  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> 제목 </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>각 필드 이름은 사이트 페이지의 요소에 해당합니다. 예를 들어 필드 이름 <span class="codeph"> desc </span> 을 지정하는 경우, 삽입 정의 값을 사이트 페이지의 설명 Meta 태그에 해당하는 필드에 추가할 수 있습니다. </p> <p>설명 메타 태그가 페이지에 없으면 정의된 컨텐츠가 자동으로 태그를 만듭니다. <span class="codeph"> desc </span> 삽입에 지정된 컨텐츠는 하드 코딩된 메타 설명 컨텐츠처럼 결과 페이지에 표시됩니다. </p> <p>필드 이름이 같은 여러 정의를 만들 수도 있습니다. 예를 들어 다음과 같은 주사를 맞아야 합니다. </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>위의 예에서 모든 사이트 페이지에는 "내 사이트에 오신 것을 환영합니다."라는 삽입된 제목이 표시됩니다. "/company/" 폴더의 페이지는 "내 사이트:문의하기"를 참조하십시오. </p> <p>주사제는 <span class="wintitle"> 필드 삽입 정의 </span> 텍스트 상자에 표시되는 순서대로 적용됩니다. 동일한 위치의 페이지에 대해 동일한 필드("제목")가 두 번 이상 정의된 경우, 나중 정의가 우선합니다. </p> <p> <span class="codeph"> [regexp]  </span> - 선택 사항 <span class="codeph"> regexp </span> 옵션을 사용하도록 선택하면 정의된 URL이 일반 표현식으로 처리됩니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> <p>다음 정의에서: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "중요 정보"는 일반 표현식 <span class="codeph">^과 일치하는 모든 페이지의 "대상" 필드에 삽입됩니다.*/products/.*\.html$ </span>. </p> <p>따라서 다음과 같은 사항이 있습니다. </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>다음 예에서: </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>주사는 ".pdf" 파일 이름 확장자로 끝나는 모든 페이지의 "제목" 컨텐츠에 "Millennium Science"를 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>URL이 필요하며 주입할 문서를 지정합니다. </p> <p>URL은 다음 중 하나입니다. </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> https://www.mydomain.com/products.html에서와 같이 전체 경로 </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> https://www.mydomain.com/products에서와 같이 부분 경로 </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> https://www.mydomain.com/*.html에서와 같이 와일드카드를 사용하는 URL </li> 
     </ul> </p> <p>URL 값에 공백 문자가 있으면 안 됩니다. <span class="codeph"> regexp </span> 옵션을 사용하는 경우 URL은 일반 표현식으로 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>값이 필요하며 기존 필드 컨텐츠를 대체하거나 추가하는 데 사용됩니다. 동일한 필드 이름에 여러 값을 지정할 수 있습니다. 예: </p> <p><b>키 추가</b> https://www.mysite.com/travel/ <b>여름</b>, <b>해변</b>, <b>및 </b> </p> <p><b>keys</b> https://www.mysite.com/travel/fare/*.html <b>저렴한 티켓</b> 추가 </p> <p>위의 예에서 "summer, beach, sand"는 "/travel/" 디렉토리의 모든 페이지에서 "keys" 필드에 추가됩니다. "/travel/fare/" 디렉토리의 모든 페이지에 있는 "keys" 필드에 "price tickees"라는 단어가 추가됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

크롤링할 내용 유형 선택 및 인덱스[도 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)

## 필드 삽입 정의 추가 중 {#task_E86566FA1FF74CF68115C0ADA05172AE}

페이지 자체를 편집하지 않고도 [!DNL Injections]을 사용하여 웹 페이지에 컨텐츠를 삽입할 수 있습니다.

[!DNL Injections] 페이지에서 **[!UICONTROL Test]**&#x200B;을(를) 선택적으로 사용할 수 있습니다. 테스트 필드 이름(예: &quot;제목&quot; 또는 &quot;본문&quot;), 원래 필드 값(예: &quot;홈 페이지&quot;) 및 웹 사이트의 테스트 URL을 입력합니다. 참조에 대한 결과 값이 표시됩니다. 테스트 중에는 현재 값이 변경되지 않습니다.

**필드 삽입 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Injections] 페이지의 [!DNL Test Field Injections] 영역에서 테스트 필드, 테스트 원래 값 및 테스트 URL을 입력한 다음 **[!UICONTROL Test]**&#x200B;를 클릭합니다.
1. [!DNL Field Injection Definitions] 필드에 한 줄에 하나의 삽입 정의를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 속성 로더 정보 {#concept_9EF38E98811B42CDA41996432B9AD209}

[!DNL Attribute Loader]을(를) 사용하여 추가 입력 소스를 정의하여 웹 사이트에서 크롤된 데이터를 늘릴 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

데이터 피드 입력 소스를 사용하여 웹 사이트에서 일반적으로 검색된 내용과 다른 양식에 저장된 컨텐츠에 액세스할 수 있습니다. 사용 가능한 크롤링 메서드 중 하나를 사용하여 이 작업을 수행합니다. 그런 다음 이러한 소스의 데이터를 크롤된 컨텐츠의 데이터에 삽입할 수 있습니다.

[!DNL Staged Attribute Loader Definitions] 페이지에 속성 로더 정의를 추가하면 이름 값 및 유형 값을 제외한 모든 구성 설정을 변경할 수 있습니다

[!DNL Attribute Loader] 페이지에는 다음 정보가 표시됩니다.

* 구성하고 추가한 정의된 속성 로더 구성의 이름입니다.
* 추가한 각 커넥터에 대해 다음 데이터 소스 유형 중 하나:

   * **텍스트**  - 간단한 &quot;일반&quot; 파일, 쉼표로 구분된 파일, 탭으로 구분된 형식 또는 다른 일관되게 구분된 형식.
   * **피드**  - XML 피드.

* 다음 크롤링 및 색인화에 대한 구성이 활성화되었는지 여부.
* 데이터 소스의 주소입니다.

[텍스트 및 피드에 속성 삽입 프로세스가 작동하는 방법을 참조하십시오..](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

자세한 내용은 [여러 특성 로더 구성 정보](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

속성을 추가할 때 미리 보기 사용 정보 [를 참조하십시오..](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## 속성 로더 {#section_E059A33D61EE4DB0972A37B8A35E9E16}의 텍스트 및 피드 구성에서 속성 삽입 프로세스가 작동하는 방식

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
   <td colname="col3"> <p><span class="uicontrol"> 텍스트 </span>의 경우 각 줄바꿈 구분 텍스트 줄은 개별 문서에 해당하며, 쉼표 또는 탭과 같은 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p><span class="uicontrol"> 피드 </span>의 경우 각 문서의 데이터는 다음 형식의 정규 표현식 패턴을 사용하여 추출됩니다. </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle"> 속성 로더 추가 </span> 페이지에서 <span class="uicontrol"> 매핑 </span>을(를) 사용하여 데이터의 캐시된 복사본을 만든 다음 Crawler에 대한 링크 목록을 만듭니다. 데이터는 로컬 캐시에 저장되고 구성된 필드로 채워집니다. </p> <p>파싱된 데이터는 로컬 캐시에 기록됩니다. </p> <p>이 캐시는 나중에 읽고 크롤러에 필요한 간단한 HTML 문서를 만듭니다. 예: </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span> 요소는 제목 메타데이터 필드에 매핑이 있을 때만 생성됩니다. 마찬가지로 <span class="codeph"> &lt;body&gt; </span> 요소는 본문 메타데이터 필드에 매핑이 있을 때만 생성됩니다. </p> <p> <b>중요</b>:사전 정의된 URL 메타 태그에 대한 값 할당은 지원되지 않습니다. </p> <p>다른 모든 매핑의 경우, <span class="codeph"> &lt;meta&gt; </span> 태그가 원본 문서에서 찾은 데이터가 있는 각 필드에 대해 생성됩니다. </p> <p>각 문서에 대한 필드가 캐시에 추가됩니다. 캐시에 기록되는 각 문서에 대해 다음 예와 같이 링크가 생성됩니다. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>구성의 매핑에는 기본 키로 식별되는 필드가 하나만 있어야 합니다. 이 매핑은 캐시에서 데이터를 가져올 때 사용되는 키를 형성합니다. </p> <p>크롤러는 URL <span class="codeph"> 인덱스를 인식합니다.</span> 스키마 접두어를 사용하여 로컬에 캐시된 데이터에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>캐시된 문서 집합을 크롤링합니다. </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 인덱스:</span> 링크는 Crawler의 보류 중인 목록에 추가되고 일반 크롤링 시퀀스에서 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>각 문서를 처리합니다. </p> </td> 
   <td colname="col3"> <p>각 링크의 키 값은 캐시에 있는 항목에 해당되므로 각 링크를 검색하면 캐시에서 해당 문서의 데이터를 가져옵니다. 그런 다음 HTML 이미지로 "어셈블됨"이 처리되어 색인에 추가됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 여러 속성 로더 구성 정보 {#section_4CC49C74EF294608A184E233F215ADFF}

모든 계정에 대해 여러 속성 로더 구성을 정의할 수 있습니다.

속성 로더를 추가하면 선택적으로 기능 **[!UICONTROL Setup Maps]**&#x200B;을 사용하여 데이터 소스의 샘플을 다운로드할 수 있습니다. 그 데이터는 적합성을 검토한다.

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
   <td colname="col2"> <p>탭을 먼저 시도한 다음 세로 막대( <span class="codeph">)를 사용하여 구분 기호 값을 결정합니다. | </span>) 및 마지막으로 쉼표( <span class="codeph"> , </span>). <span class="uicontrol"> 설정 맵 </span>을(를) 클릭하기 전에 구분 기호 값을 이미 지정한 경우 이 값이 대신 사용됩니다. </p> <p>최적의 구성표는 맵 필드에서 적절한 태그 및 필드 값을 추측으로 채웁니다. 또한 파싱된 데이터의 샘플링이 표시됩니다. 파일에 머리글 행이 포함되어 있다는 것을 알고 있는 경우 첫 번째 행 <span class="uicontrol"> 헤더에 반드시 </span> 머리글을 선택합니다. 설정 함수는 이 정보를 사용하여 결과 맵 항목을 더 잘 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>피드 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드하고 간단한 XML 파싱을 수행합니다. </p> <p>결과 XPath 식별자는 맵 테이블의 태그 행에 표시되며, 필드 값도 유사합니다. 이러한 행은 사용 가능한 데이터만 식별하고 더 복잡한 XPath 정의를 생성하지 않습니다. 그러나 XML 데이터를 설명하고 Itemtag를 식별하므로 여전히 유용합니다. </p> <p> <p>참고: 설정 맵 함수는 전체 XML 소스를 다운로드하여 분석을 수행합니다. 파일이 크면 이 작업이 시간 초과될 수 있습니다. </p> </p> <p>이 함수는 성공 시 사용할 수 없는 모든 XPath 항목을 식별합니다. 결과 맵 정의를 검토하고 필요 없거나 원하는 맵 정의를 제거해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>파일 파서가 전체 파일을 메모리에 읽으려고 하므로 큰 XML 데이터 세트에서 설정 맵 기능을 사용할 수 없습니다. 결과적으로 메모리 부족 문제가 발생할 수 있습니다. 그러나 색인 작성 시 동일한 문서를 처리할 때 메모리에 읽을 수는 없습니다. 대신 대용량 문서는 &quot;이동 중&quot;에 처리되며 메모리에 처음부터 완전히 읽을 수는 없습니다.

## 속성 로더 {#section_E9CAB000A94C4D9189786C1EDB1CDB46}를 추가할 때 미리 보기 사용 정보

속성 로더 데이터는 색인 작업 전에 로드됩니다.

속성 로더를 추가할 때 저장 중인 것처럼 **[!UICONTROL Preview]** 기능을 사용하여 데이터를 확인할 수도 있습니다. 구성에 대해 테스트를 실행하지만 구성을 계정에 저장하지 않습니다. 테스트는 구성된 데이터 소스에 액세스합니다. 그러나 다운로드 캐시는 임시 위치에 씁니다.인덱싱 크롤러가 사용하는 기본 캐시 폴더와 충돌하지 않습니다.

미리 보기는 **Acct:IndexConnector-Preview-Max-Documents**&#x200B;에 의해 제어되는 5개의 문서 중 기본값인 5개만 처리합니다. 미리 본 문서는 인덱싱 크롤러에 제공되므로 소스 양식으로 표시됩니다. 이 표시는 웹 브라우저의 &quot;소스 보기&quot; 기능과 유사합니다. 표준 탐색 링크를 사용하여 미리 보기 세트에서 문서를 탐색할 수 있습니다.

이러한 문서는 직접 처리되고 캐시에 다운로드되지 않으므로 미리 보기는 XML 구성을 지원하지 않습니다.

## 속성 로더 정의 {#task_A735E5EF763343A9B675E1A3B09AFDBC} 추가

각 속성 로더 구성은 데이터 소스 및 매핑을 정의하여 해당 소스에 대해 정의된 데이터 항목을 인덱스의 메타데이터 필드에 연결합니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

새 정의 및 활성화된 정의 효과가 고객에게 표시되기 전에 사이트 색인을 다시 작성하십시오.

**속성 로더 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Stage Attribute Loader Definitions] 페이지에서 **[!UICONTROL Add New Attribute Loader]**&#x200B;을 클릭합니다.
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
      <td colname="col2"> <p>속성 로더 구성의 고유한 이름입니다. 영숫자 문자를 사용할 수 있습니다. "_" 및 "-" 문자도 허용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p>데이터의 소스. 선택하는 데이터 소스 유형은 <span class="wintitle"> 속성 로더 추가 </span> 페이지에서 사용할 수 있는 결과 옵션에 영향을 줍니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> 텍스트 </span> <p>간단한 플랫 텍스트 파일, 쉼표로 구분된 형식, 탭으로 구분된 형식 또는 다른 일관되게 구분된 형식. 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p>열 번호에서 참조하는 각 값 또는 열을 1부터 메타데이터 필드에 매핑할 수 있습니다. </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> 피드 </span> <p>여러 개의 "행" 정보가 포함된 기본 XML 문서를 다운로드합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형:텍스트</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>사용할 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 사용 여부를 방지할 수 있습니다. </p> <p> <b>참고</b>:비활성화된 속성 로더 구성은 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예제와 같이 데이터 소스 문서의 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>또는  </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다 </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>간단한 플랫 텍스트 파일, 쉼표로 구분된 파일, 탭으로 구분 또는 다른 일관되게 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용되는 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>필요한 경우 HTTP 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>필요한 경우 HTTPS 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간 초과 </p> </td> 
      <td colname="col2"> <p>FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 시간 초과(초)를 지정합니다. 이 값은 30에서 300 사이여야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다시 시도 </p> </td> 
      <td colname="col2"> <p>실패한 FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 최대 재시도 횟수를 지정합니다. 이 값은 0에서 10 사이여야 합니다. </p> <p>값이 0(0)이면 다시 시도하지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>인코딩 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일에 사용되는 문자 인코딩 시스템을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구분 기호 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일의 각 필드를 지정하는 데 사용할 문자를 지정합니다. </p> <p>쉼표 문자( <span class="codeph"> , </span>)는 구분 기호의 예입니다. 쉼표는 지정된 데이터 소스 파일에서 데이터 필드를 구분하는 데 도움이 되는 필드 구분 기호로 사용됩니다. </p> <p><span class="uicontrol"> 탭을 선택하십시오. </span> 를 클릭하여 가로 탭 문자를 구분 기호로 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 행의 머리글 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일의 첫 번째 행에 데이터가 아닌 헤더 정보만 포함됨을 나타냅니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부실 일 수 </p> </td> 
      <td colname="col2"> <p>Attribute Loader 데이터의 다운로드 사이의 최소 간격을 설정합니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 색인 실행 다운로드는 무시됩니다. 이 값을 기본값인 1로 설정하면 속성 로더 데이터가 24시간 기간 내에 한 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 인덱스는 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정합니다. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 열 </span> <p> 열 번호를 지정합니다. 첫 번째 열은 1입니다. 각 열에 대한 새 맵 행을 추가하려면 <span class="wintitle"> 작업 </span> 아래에서 <span class="uicontrol"> + </span>을 클릭합니다. </p> <p>데이터 소스의 각 열을 참조할 필요가 없습니다. 대신 값을 건너뛰도록 선택할 수 있습니다. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>이(가) 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>원하는 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 스크립트 필터링 </span>에서 사용하는 내용을 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보를 참조하십시오 </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> 기본 키?  </span> <p>한 필드만 기본 키로 식별됩니다. 이 필드는 색인의 해당 문서와 속성 로더 데이터를 일치시키는 "외래 키"로 사용됩니다. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML 제거?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형:피드</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>사용할 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 사용 여부를 방지할 수 있습니다. </p> <p> <b>참고</b>:비활성화된 속성 로더 구성은 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예제와 같이 데이터 소스 문서의 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>또는  </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 "행" 정보를 포함하는 기본 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용되는 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>필요한 경우 HTTP 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>필요한 경우 HTTPS 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 개별 XML 행을 식별하는 데 사용할 수 있는 XML 요소를 식별합니다. </p> <p>예를 들어 Adobe XML 문서의 다음 피드 조각에서 Itemtag 값은 <span class="codeph"> record </span>입니다. </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>속성 로더 구성 데이터에 대한 조회 "키"로 사용되는 값을 갖는 메타데이터 필드를 지정합니다. 값을 선택하지 않으면(<b>—None—</b>), 등급 계산에 이 구성의 데이터를 사용할 수 없습니다(<b>규칙</b> &gt; <b>등급 규칙</b> &gt; <b>규칙 편집</b>). 값을 선택하면 이 필드의 값이 이 구성 데이터를 사용하여 사이트 검색/머천다이징 문서를 상호 참조하는 데 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부실 일 수 </p> </td> 
      <td colname="col2"> <p>Attribute Loader 데이터의 다운로드 사이의 최소 간격을 설정합니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 색인 실행 다운로드는 무시됩니다. 이 값을 기본값인 1로 설정하면 속성 로더 데이터가 24시간 기간 내에 한 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 인덱스는 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>XPath 표현식을 사용하여 XML 요소-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> 태그 </span> <p>파싱된 XML 데이터의 XPath 표현을 지정합니다. 위의 Adobe XML 문서 예제를 사용하여 Itemtag 옵션 아래의 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 </span> 특성이 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다.<span class="codeph"> </span></p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 속성이 <span class="codeph"> title </span>인 </span> 레코드 &lt;a7/&gt; 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 안에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 제목 &lt;a11&gt; /&gt;.</span><span class="codeph"> </span></p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 &lt;a7/&gt; 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 &lt;a3/&gt; 메타 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> &lt;a111 /&gt;.<span class="codeph"><span class="codeph"></span></span> </span></p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 &lt;a7/&gt; 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 본문 &lt;a11&gt; /&gt;.<span class="codeph"></span> </span></p> </li> 
        </ul> </p> <p>XPath는 비교적 복잡한 표기법입니다. 자세한 내용은 다음 위치에 있습니다. </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> 참조 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> 필드 </span> <p>생성된 각 <span class="codeph"> &lt;meta&gt; </span> 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>이(가) 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>원하는 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 스크립트 필터링 </span>에서 사용하는 내용을 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보를 참조하십시오 </a>. </p> <p>Attribute Loader가 맵 필드에 여러 개의 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 해당 필드에는 <span class="wintitle"> 허용 목록 </span> 특성이 설정되어 있습니다. 이 경우, 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> 기본 키?  </span> <p>한 필드만 기본 키로 식별됩니다. 이 필드는 색인의 해당 문서와 속성 로더 데이터를 일치시키는 "외래 키"로 사용됩니다. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> HTML 제거?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) 데이터 소스의 샘플을 다운로드하려면 **[!UICONTROL Setup Maps]**&#x200B;을 클릭합니다. 그 데이터는 적합성을 검토한다.
1. **[!UICONTROL Add]**&#x200B;을 클릭하여 [!DNL Attribute Loader Definitions] 페이지에 구성을 추가합니다.
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]**&#x200B;을 클릭합니다.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 속성 로더 정의 편집 {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

정의한 기존 속성 로더를 편집할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

[!DNL Type] 드롭다운 목록에서 속성 로더 이름 또는 유형과 같이 일부 속성 로더 옵션을 변경할 수 없습니다.

**속성 로더 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 변경할 속성 로더 정의 이름에 대해 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Edit] 페이지에서 원하는 옵션을 설정합니다.

   [Adding an Attribute Loader definition](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]**&#x200B;을 클릭합니다.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 속성 로더 정의 {#task_9B40D5ECFC81411E9480F62A0FD5F2E0} 복사

기존 속성 로더 정의를 복사하여 새로 만들 속성 로더의 기초로 사용할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

속성 로더 정의를 복사할 때 복사된 정의는 기본적으로 비활성화됩니다. 정의를 활성화 또는 &quot;켜기&quot;하려면 [!DNL Attribute Loader Edit] 페이지에서 해당 정의를 편집하고 **[!UICONTROL Enable]**&#x200B;를 선택합니다.

[속성 로더 정의 편집](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)을 참조하십시오.

**속성 로더 정의를 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 복제할 속성 로더 정의 이름에 대해 **[!UICONTROL Copy]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Copy] 페이지에서 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Copy]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 속성 로더 정의 이름 바꾸기 {#task_58D5DFD7EBC04111BCB91118E4440DB4}

기존 속성 로더 정의의 이름을 변경할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

**속성 로더 정의 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 머리글 아래에서 변경할 속성 로더 정의 이름에 대해 **[!UICONTROL Rename]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Rename] 페이지의 [!DNL Name] 필드에 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Rename]**.
1. (선택 사항) [!DNL Attribute Loader Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 속성 로더 데이터 로드 중 {#task_2F3C55189B0A4049AB2113F2291CC181}

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
   <td colname="col2"> <p>마지막 데이터 로드 시도 성공 또는 실패를 나타냅니다. 또는 이미 진행 중인 데이터 로드 작업의 상태가 표시됩니다. </p> </td> 
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
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL Load Attribute Loader Data]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Attribute Loader Data Load]** 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL Start Load]**&#x200B;을 클릭하여 로드 작업을 시작합니다.

      데이터 로드 작업 중에 **진행** 행은 진행 상태에 대한 정보를 제공합니다.

   * 로드 작업을 중지하려면 **[!UICONTROL Stop Load]**&#x200B;을 클릭합니다.

1. [!DNL Attribute Loader Definitions] 페이지로 돌아가려면 **[!UICONTROL Close]**&#x200B;을 클릭합니다.

## 속성 로더 데이터 미리 보기 {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

미리 보기를 사용하여 최근에 로드된 속성 로더 데이터를 볼 수 있습니다.

테이블의 행 열에는 속성 로더 값이 로드되었던 원래 순서를 나타내는 각 데이터 행의 번호가 표시됩니다.

나머지 열에는 각 항목과 연관된 값이 표시됩니다.

테이블이 비어 있으면 속성 로더 데이터를 아직 로드하지 않았음을 의미합니다. [!DNL Attribute Loader Data Preview] 페이지를 닫은 다음 속성 로더 데이터를 로드할 수 있습니다.

[속성 로더 데이터 로드](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.

**속성 로더 데이터를 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지의 [!DNL Actions] 열에서 다운로드된 데이터를 보려는 구성의 **[!UICONTROL Preview]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Data Preview] 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 데이터를 봅니다.

   데이터를 내림차순이나 오름차순으로 정렬하려면 표의 열 머리글을 클릭합니다.
1. 다음 중 하나를 수행합니다.

   * **[!UICONTROL Download to Desktop]**&#x200B;을 클릭하여 테이블을 다운로드하고 .xlt 파일로 저장합니다.
   * 속성 로더 데이터 미리 보기를 마친 후 페이지를 닫고 이전에 본 페이지로 돌아갑니다.

## 속성 로더 정의 설정 보기 {#task_EA99A9694FE948ADA82C1DBA0667851B}

기존 속성 로더 정의의 구성 설정을 검토할 수 있습니다.

속성 로더 정의가 [!DNL Attribute Loader Definitions] 페이지에 추가되면 해당 유형 설정을 변경할 수 없습니다. 대신 정의를 삭제한 다음 새로 추가해야 합니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

**속성 로더 정의의 설정을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 검토하거나 편집할 속성 로더 정의 이름에 대해 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.

## 최신 속성 로더 데이터 로드인 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}에서 로그 보기

[!DNL View Log]을 사용하여 최신 다운로드 프로세스의 Attribute Loader 데이터 로그 파일을 검사할 수 있습니다. 로그 보기를 사용하여 실행 중인 다운로드를 모니터링할 수도 있습니다.

[속성 로더 데이터 로드](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.

**최신 속성 로더 데이터 로드에서 로그를 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지에서 **[!UICONTROL View Log]**&#x200B;을 클릭합니다. 로그 페이지,
1. [!DNL Attribute Loader Data Log] 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 로그 정보를 봅니다.
1. 완료되면 페이지를 닫고 [!DNL Attribute Loader Definitions] 페이지로 돌아갑니다.

## 속성 로더 정의 {#task_E8980F66888B476E98C228C1D307EDF8} 삭제

더 이상 필요하거나 사용하지 않는 기존 속성 로더 정의를 삭제할 수 있습니다.

>[!NOTE]
>
>Attribute Loader를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원에 의해 계정에서 활성화되어야 할 수 있습니다.

**속성 로더 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Definitions] 페이지의 [!DNL Actions] 열 머리글 아래에서 제거할 속성 로더 정의 이름에 대해 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. [!DNL Attribute Loader Delete] 페이지에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
