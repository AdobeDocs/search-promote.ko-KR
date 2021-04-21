---
description: Adobe Analytics 메뉴를 사용하여 Adobe Analytics 지표 인증을 설정하거나, 보고서 세트의 Adobe Analytics 지표를 관리하거나, SAINT을 사용하여 외부 소스에서 표 형식으로 데이터를 받아 Adobe Analytics 보고서를 향상시킵니다.
solution: Target
subtopic: Adobe Analytics
title: Adobe Analytics 메뉴 정보
topic-legacy: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
exl-id: e1f7b8f0-45d4-457a-a9d3-a8cb4b785059
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '3407'
ht-degree: 1%

---

# Adobe Analytics 메뉴 {#about-the-adobe-analytics-menu} 정보

Adobe Analytics 메뉴를 사용하여 Adobe Analytics 지표 인증을 설정하거나, 보고서 세트의 Adobe Analytics 지표를 관리하거나, SAINT을 사용하여 외부 소스에서 표 형식으로 데이터를 받아 Adobe Analytics 보고서를 향상시킵니다.

## Adobe Analytics 지표 인증 설정 {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Adobe Analytics 지표를 사이트 검색/머천다이징 등급에 통합하려면 먼저 Adobe Analytics 웹 서비스 로그인을 획득해야 합니다. 로그인 정보를 얻은 후 이를 사용하여 사이트 검색/머천다이징에서 Adobe Analytics 인증을 설정할 수 있습니다.

**Adobe Analytics 지표 인증을 설정하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**&#x200B;를 클릭합니다.
1. [!DNL Setup Adobe Analytics Metrics Authentication] 페이지에서 각 필드에 요청한 정보를 지정합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>텍스트 필드 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 회사 이름 </p> </td> 
      <td colname="col2"> <p>Adobe Analytics 계정에 로그인하는 데 사용되는 동일한 회사 이름 설정입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>웹 서비스 사용자 이름 </p> </td> 
      <td colname="col2"> <p>Adobe Analytics 계정과 연결된 웹 서비스 사용자 이름입니다. </p> <p>Adobe Analytics에서 이 정보를 얻을 수 있습니다. Adobe Analytics 메뉴 모음에서 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b>를 클릭합니다. 웹 서비스</b> </span>. 정보는 API 액세스 정보 표에 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>웹 서비스 공유 암호 </p> </td> 
      <td colname="col2"> <p>Adobe Analytics 계정과 연결된 웹 서비스 공유 암호 </p> <p>Adobe Analytics에서 이 정보를 얻을 수 있습니다. Adobe Analytics 메뉴 모음에서 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b>를 클릭합니다. 웹 서비스</b> </span>. 정보는 API 액세스 정보 표에 있습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## Adobe Analytics 보고서 세트 정보 {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

사이트 검색/머천다이징 내에서 Adobe Analytics 보고서 세트 데이터를 사용하려면 먼저 사이트 검색/머천다이징 계정에 Adobe Analytics 데이터 사본을 만들어야 합니다.

Adobe Analytics 보고서 세트 정의를 새로 만들거나 기존 Adobe Analytics 보고서 세트 및 관련 지표를 보거나 수정할 수 있습니다.

사이트 검색/머천다이징에서 처음으로 Adobe Analytics에 액세스하면 회사에서 사용할 수 있는 보고서 세트 목록이 다운로드되고 캐시됩니다. 새 보고서 세트가 최근에 추가되었거나 기존 보고서 세트가 제거된 경우 보고서 세트 목록을 새로 고쳐 보고서 세트 목록을 다시 다운로드할 수 있습니다.

## Adobe Analytics 보고서 세트 {#task_6DE17305EA7146DA8C30FF8FDF68A3C0} 추가

사이트 검색/머천다이징 등급 규칙을 기준으로 할 Adobe Analytics 보고서 세트를 선택할 수 있습니다.

선택할 수 있는 목록은 Adobe Analytics 계정 내에서 사용할 수 있는 보고서 세트와 일치해야 합니다. 선택한 보고서 세트에 따라 사이트 검색/머천다이징 등급 규칙 내에서 사용할 수 있는 지표가 결정됩니다.

[등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

Adobe Analytics 보고서 세트를 추가한 후 해당 지표를 편집할 수 있습니다.

보고서 세트](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)의 Adobe Analytics 지표 편집을 참조하십시오.[

**Adobe Analytics 보고서 세트를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. Adobe Analytics 보고서 세트 페이지에서 **[!UICONTROL Add Report Suite]**&#x200B;을 클릭합니다.
1. 새로 추가된 테이블 행의 드롭다운 목록에서 원하는 보고서 세트를 선택합니다.
1. 보고서 세트의 Adobe Analytics 지표를 편집합니다.

## 보고서 세트 {#task_360904CCBBB140238ADA036C3CC07664}의 Adobe Analytics 지표 편집

사이트 검색/머천다이징에서 Adobe Analytics 지표를 등급 규칙에 통합하려면 선택한 보고서 세트와 연관된 지표 중 하나 이상을 선택합니다. 그런 다음 Adobe Analytics 웹 서비스를 통해 지표 데이터를 가져오는 데 사용되는 옵션을 구성합니다.

[Adobe Analytics 보고서 세트 추가](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)를 참조하십시오.

[고급 Adobe Analytics 옵션 구성](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19)을 참조하십시오.

**보고서 세트의 Adobe Analytics 지표를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. [!DNL Adobe Analytics Report Suites] 페이지의 **[!UICONTROL Actions]** 열에서 지표를 구성할 보고서 세트에 대해 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Edit Adobe Analytics Metrics] 페이지에서 필요한 지표를 설정합니다. 지표 이름 옆에 별표(*)가 없는 지표는 선택 사항입니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>보고서 세트 </p> </td> 
      <td colname="col2"> <p>추가한 현재 보고서 세트의 이름을 표시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>보고서 세트 보기 이름 </p> </td> 
      <td colname="col2"> <p>Adobe Analytics 보고서 세트 이름에 대한 "별칭" 이름을 제공합니다. 이 대체 이름은 동일한 보고서 세트를 두 개 이상의 정의에 사용하는 경우에 유용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>보고서 유형 선택 </p> </td> 
      <td colname="col2"> <p>선택한 보고서 세트에 사용할 보고서 유형 값을 지정합니다. 이 값은 반환된 각 결과 행의 키를 식별합니다. </p> <p>보고서 유형을 Adobe Analytics 요소라고도 합니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>상호 참조 필드 이름 </p> </td> 
      <td colname="col2"> <p>값이 보고서 세트의 데이터에 대한 조회 "키"로 사용되는 메타데이터 필드를 지정합니다. </p> <p>값을 선택하지 않으면("— None —") 이 보고서 세트의 데이터를 등급 계산에 사용할 수 없습니다( <span class="uicontrol"> <b>규칙</b> </span> &gt; <span class="uicontrol"> <b> </b> </span> <span class="uicontrol"> <b> 규칙 편집</b>  규칙 편집&lt;a11 0/&gt; </span>). </p> <p>값을 선택할 때 이 필드의 값은 이전에 설정한 선택된 보고서 유형 값을 사용하여 이 보고서 세트의 Adobe Analytics 데이터로 사이트 검색/머천다이징 문서를 상호 참조하는 데 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색어 보고서 </p> </td> 
      <td colname="col2"> <p>비즈니스 규칙을 만들고 <b>스테이지 Adobe Analytics 데이터 미리 보기</b> 페이지에서 검색어를 시뮬레이트할 수 있는 액세스 권한을 제공합니다. </p> <p><a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Adobe Analytics 데이터 미리 보기</a>를 참조하십시오. </p> <p>두 가지 옵션이 포함된 모든 행에 풀다운 메뉴가 나타납니다.<b>검색어</b> 및 <b>새 비즈니스 규칙 만들기</b>를 시뮬레이션합니다. </p> <p>두 옵션 모두 보고서 유형의 데이터를 검색어로 사용합니다. 따라서 보고서 유형이 검색어를 나타내는 경우에만 이 기능이 적절합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>지표 </p> </td> 
      <td colname="col2"> <p>사이트 검색/머천다이징 등급 규칙 내에서 다운로드 및 사용할 지표 값을 식별합니다. </p> <p>여기에서 구성하는 지표는 규칙의 경우 <span class="uicontrol"> <b>규칙</b> </span> &gt; <span class="uicontrol"> <b> 등급 규칙</b> </span> &gt; <span class="uicontrol"> <b>규칙 편집</b> </span> 멤버 센터 페이지에 선택 항목으로 표시됩니다. 데이터 유형은 <span class="uicontrol"> Adobe Analytics 지표(숫자) </span>로 설정됩니다. 선택 사항에는 보고서 세트 이름 또는 보고서 세트 보기 이름(지정된 경우)과 개별 지표 이름의 조합이 표시됩니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 지표 값 </p> </td> 
      <td colname="col2"> <p>0이 아닌 값을 입력하여 지표의 최소 값을 지정할 수 있습니다. </p> <p>비어 있거나 0인 경우 지표에 대한 모든 값이 다운로드됩니다.그렇지 않으면 최소 지표 값이 전달되면 이 지표에 대한 다운로드가 중지됩니다. </p> <p>Adobe Analytics 지표는 내림차순으로 검색됩니다. </p> <p>추가 지표 정의를 추가하려면 <span class="uicontrol"> <b>+</b> </span>을 클릭합니다.더 이상 필요하거나 필요 없는 지표 정의를 제거하려면 <span class="uicontrol"> <b>-</b> </span>을 클릭합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 지표 집계 기간(일) </p> </td> 
      <td colname="col2"> <p> 가져올 Adobe Analytics 지표의 일수를 제어하여 어제 날짜로부터 다시 계산합니다. 현재 날짜의 데이터를 가져오려는 시도가 없습니다. </p> <p>기본값은 7입니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 다운로드 새로 고침 빈도(일) </p> </td> 
      <td colname="col2"> <p> 등급 계산에 사용되는 Adobe Analytics 데이터의 다운로드 간 최소 간격을 설정합니다. </p> <p>다운로드 새로 고침 빈도 간격 내에 발생하는 색인 실행 다운로드는 무시됩니다. 그러나 수동 다운로드에서는 이 값을 무시합니다. </p> <p>이 값을 기본값 1로 설정하면 Adobe Analytics 데이터가 24시간 내에 한 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 인덱스는 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   [등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)도 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.

   단계 [!DNL Adobe Analytics Report Suites] 페이지로 돌아갑니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## Adobe Analytics 보고서 세트 삭제 {#task_0ACA172214D14654ABDB139F417B9F7D}

삭제를 사용하여 [!DNL Adobe Analytics Report Suites] 페이지에서 보고서 세트를 제거할 수 있습니다. 보고서 세트를 삭제하면 사이트 검색/머천다이징 서버에서 데이터 복사본만 제거됩니다.Adobe Analytics 시스템의 데이터는 영향을 주지 않습니다.

**Adobe Analytics 보고서 세트를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. [!DNL Adobe Analytics Report Suites] 페이지의 **[!UICONTROL Actions]** 열에서 제거할 보고서 세트에 대해 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. [!DNL Adobe Analytics Delete Report Suite] 페이지에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.

## Adobe Analytics 데이터 미리 보기 {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

미리 보기를 사용하여 최근에 로드한 Adobe Analytics 지표를 볼 수 있습니다.

표의 행 열에는 Adobe Analytics 지표가 로드된 원래 순서를 나타내는 지표 데이터의 각 행에 대한 번호가 표시됩니다.

제품 열에는 각 지표 데이터 행과 연관된 Adobe Analytics 요소가 표시됩니다. 이 열의 값은 등급 정의에 구성된 대로 사이트 검색/머천다이징 페이지를 해당 지표 값과 연결하는 데 사용됩니다.

[등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

[등급 구성](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)을 참조하십시오.

나머지 열에는 각 항목과 연관된 지표 값이 표시됩니다.

테이블이 비어 있으면 Adobe Analytics 데이터를 아직 로드하지 않았음을 의미합니다. [!DNL Adobe Analytics Data Preview] 페이지를 닫은 다음 Adobe Analytics 데이터를 로드할 수 있습니다.

[Adobe Analytics 데이터 로드](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.
표를 검색어 보고서로 지정한 경우 모든 행에 작은 삼각형이 나타납니다. 드롭다운 목록을 클릭하고 **검색어 시뮬레이션** 또는 **새 비즈니스 규칙 만들기**&#x200B;를 선택할 수 있습니다. 선택한 작업이 해당 행의 검색어, 두 번째 열에 있는 데이터에 적용됩니다

**Adobe Analytics 데이터를 미리 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. [!DNL Adobe Analytics Report Suites] 페이지의 [!DNL Actions] 열에서 다운로드된 데이터를 보려는 보고서 세트에 대해 **[!UICONTROL Preview]**&#x200B;를 클릭합니다.

   * 클릭 **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. [!DNL Adobe Analytics Terms Report] 페이지의 [!DNL Actions] 열에서 다운로드된 데이터를 보려는 보고서 세트에 대해 **[!UICONTROL Preview]**&#x200B;를 클릭합니다.

1. [!DNL Adobe Analytics Data Preview] 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 데이터를 봅니다.

   데이터를 내림차순이나 오름차순으로 정렬하려면 표의 열 머리글을 클릭합니다.
1. 다음 중 하나를 수행합니다.

   * **[!UICONTROL Download to Desktop]**&#x200B;을 클릭하여 테이블을 다운로드하고 `.xlt` 파일로 저장합니다.

   * Adobe Analytics 데이터 미리 보기를 마치면 페이지를 닫고 이전에 본 페이지로 돌아갑니다.

## 최근 Adobe Analytics 데이터 로드 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}에서 로그 보기

[로그 보기]를 사용하여 최신 다운로드 프로세스의 Adobe Analytics 데이터 로그 파일을 검사할 수 있습니다. 로그 보기를 사용하여 실행 중인 다운로드를 모니터링할 수도 있습니다.

[Adobe Analytics 데이터 로드](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)를 참조하십시오.

**최근 Adobe Analytics 데이터 로드에서 로그를 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. [!DNL Adobe Analytics Report Suites] 페이지에서 **[!UICONTROL View Log]**&#x200B;을 클릭합니다. 로그 페이지,
1. [!DNL Adobe Analytics Data Log] 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 로그 정보를 봅니다.
1. 완료되면 페이지를 닫고 [!DNL Adobe Analytics Report Suites] 페이지로 돌아갑니다.

## Adobe Analytics 데이터 로드 중 {#task_2F3C55189B0A4049AB2113F2291CC181}

구성된 Adobe Analytics 보고서 세트 데이터를 사이트 검색/머천다이징에 다운로드할 수 있습니다.

데이터 로드 페이지에는 다음 정보와 함께 마지막 Adobe Analytics 데이터 로드 작업의 상태가 표시됩니다.

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
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 시도 동안 다운로드한 지표 데이터 행 수를 표시합니다. </p> </td> 
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

**Adobe Analytics 데이터를 로드하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. [!DNL Stage Adobe Analytics Report Suites] 페이지에서 **[!UICONTROL Load Adobe Analytics Data]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Adobe Analytics Data Load]** 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL Start Load]**&#x200B;을 클릭하여 로드 작업을 시작합니다.

      데이터 로드 작업 중에 **Progress** 행은 진행 상태에 대한 정보를 제공합니다.

   * 로드 작업을 중지하려면 **[!UICONTROL Stop Load]**&#x200B;을 클릭합니다.

1. [!DNL Stage Adobe Analytics Reports Suite] 페이지로 돌아가려면 **[!UICONTROL Close]**&#x200B;을 클릭합니다.

## 보고서 세트 목록 {#task_EA6215D438CA4185B106657D9712ED34} 새로 고침

사이트 검색/머천다이징 사용자 인터페이스에서 처음으로 Adobe Analytics에 액세스하면 회사에서 사용할 수 있는 Adobe Analytics 보고서 세트 목록이 다운로드되고 캐시됩니다. 새 보고서 세트가 최근에 추가되었거나 기존 보고서 세트가 삭제된 경우 보고서 세트 목록 새로 고침을 사용하여 사이트 검색/머천다이징에 현재 표시된 목록을 업데이트할 수 있습니다.

[Adobe Analytics 보고서 세트 추가](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)를 참조하십시오.

[Adobe Analytics 보고서 세트 삭제](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D)를 참조하십시오.

**보고서 세트 목록을 새로 고치려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;를 클릭합니다.
1. [!DNL Adobe Analytics Report Suites] 페이지에서 **[!UICONTROL Refresh Report Suite List]**&#x200B;을 클릭합니다.

## 고급 Adobe Analytics 옵션 구성 중 {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

[!DNL Advanced Adobe Analytics Options]을(를) 사용하여 Adobe Analytics 보고서 세트 다운로드 프로세스의 동작을 세밀하게 조정하는 데 도움이 되는 설정을 제어할 수 있습니다.

보고서 세트](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)의 Adobe Analytics 지표 편집을 참조하십시오.[

**고급 Adobe Analytics 옵션을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**&#x200B;를 클릭합니다.
1. [!DNL Advanced Adobe Analytics Options] 페이지에서 다음 옵션을 설정합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>최대 행, 모든 지표 </p> </td> 
      <td colname="col2"> <p>너무 많은 Adobe Analytics 데이터를 다운로드할 수 없도록 하는 최적화 설정입니다. </p> <p>이 옵션을 0이 아닌 값으로 설정하면 각 지표에 대해 반입된 총 행 수가 지정된 값을 초과할 때 Adobe Analytics 데이터 가져오기가 중지됩니다. </p> <p>기본값은 0입니다.최대 값이 적용되지 않았습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>지표 반복 가져오기 크기(행) </p> </td> 
      <td colname="col2"> <p> 한 번에 가져올 Adobe Analytics 지표 값의 수를 제어합니다. 모든 데이터를 검색하거나 최대 행 제한에 도달할 때까지 지표 데이터 행을 반복적으로 가져옵니다. </p> <p>일반적으로 이 설정을 변경할 필요가 없습니다. 그러나 사이트의 전체 재색인의 지표 다운로드 단계를 최적화하는 것이 도움이 될 수 있습니다. </p> <p>기본값은 5000입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## SAINT 분류 피드 정보 {#concept_C55609DA24914BBC92CD90ED0259199D}

Adobe Analytics SAINT을 사용하여 외부 소스에서 표 형식의 데이터를 받아 분석 보고서를 향상시킬 수 있습니다. 예를 들어 사이트 검색/머천다이징을 사용하여 자체 인덱스에서 데이터를 검색하고 해당 데이터를 Adobe Analytics으로 내보낼 수 있습니다.

사이트 검색/머천다이징에서 Adobe Analytics SAINT 기능을 성공적으로 사용하려면 다음 요구 사항을 인식하십시오.

* Adobe Analytics 회사와 보고서 세트가 있어야 합니다.

   [Adobe Analytics 메뉴 ](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411) 정보를 참조하십시오.
* Adobe Analytics 사용자 계정에는 보고서 세트를 수정할 수 있는 권한이 있어야 합니다.

   [Adobe Analytics 지표 인증 설정](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42)을 참조하십시오.
* Adobe Analytics 사용자는 Adobe Analytics 웹 API를 사용할 수 있도록 웹 API 그룹에 속해야 합니다.
* 검색 색인에는 데이터가 올바른 형식으로 있는 등 Adobe Analytics에서 사용할 수 있는 데이터가 있어야 합니다.

피드를 만들기 전에 다음 질문과 정보를 검토하여 SAINT 피드 마법사를 성공적으로 완료할 수 있습니다.

* 어떤 보고서 세트와 함께 작업하시겠습니까?
* 제품, e-var 등과 같은 분류 세트를 사용할 수 있습니까?
* 보고서에는 어떤 분류가 있습니까? 이 질문에 대한 답변은 사이트 검색/머천다이징에서 바로 사용할 수 있는 데이터 유형과 Adobe Analytics에서 권장하는 보고서 유형에 따라 결정됩니다.
* SAINT은 사이트 검색/머천다이징의 데이터를 텍스트 유형으로 허용합니다. 해당 데이터의 형식은 Adobe Analytics 보고서 프레젠테이션에 영향을 줍니다.

## Adobe Analytics SAINT 피드 {#task_914B5AB821E84627953D8EF9339A7DD0} 만들기

Adobe Analytics SAINT을 사용하여 외부 소스에서 표 형식의 데이터를 받아 Adobe Analytics 보고서를 향상시킬 수 있습니다.

예를 들어 사이트 검색/머천다이징을 사용하여 자체 인덱스에서 데이터를 검색하고 해당 데이터를 Adobe Analytics으로 내보낼 수 있습니다.

**Adobe Analytics SAINT 피드를 만들려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL SAINT Classification Feeds] 페이지에서 **[!UICONTROL Create SAINT Feed]**&#x200B;을 클릭합니다.
1. [!DNL Create Feed] 대화 상자의 **피드 이름** 텍스트 필드에 새 피드 이름을 입력한 다음 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

   이때 피드가 저장되고 [!DNL SAINT Classification Feed] 페이지에 추가됩니다. 선택하는 경우 나중에 피드를 종료하고 편집하여 마법사를 완료할 수 있습니다.
1. [!DNL Authentication] 페이지에서 각 텍스트 필드에 Adobe Analytics 회사 이름, 사용자 이름 및 웹 암호를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics에서 웹 API를 사용할 수 있는 권한이 있는지 확인합니다.
1. **[!UICONTROL Report Suite]** 페이지에서 보고서 세트와 그 분류 데이터 세트를 선택한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. [!DNL Field Maps] 페이지에서 Adobe Analytics 분류를 사이트 검색/머천다이징 메타 데이터 필드에 매핑한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics 분류를 조정하려면 **[!UICONTROL Edit]** Adobe Analytics 분류를 클릭하여 Adobe Analytics에 로그인합니다. 변경을 완료했으면 **[!UICONTROL Refresh Classifications]**&#x200B;을 클릭하여 분류 선택 사항을 새로 고칩니다.
1. [!DNL Search Criteria] 페이지에서 사이트 검색/머천다이징의 데이터를 Adobe Analytics SAINT에 제출하기 전에 필터링할 수 있습니다. 규칙 빌더 인터페이스를 사용하여 여기에 필터 규칙을 구성한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. [!DNL Configure FTP] 페이지에서 FTP 서버를 선택합니다. 데이터를 업로드할 빈도 수를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   각 피드에는 실수로 데이터가 손실되지 않도록 하는 자체 FTP 계정이 있습니다. 여기에서 새 Adobe Analytics FTP 계정을 만들 수 있습니다.
1. [!DNL Verification] 페이지에서 **[!UICONTROL Show Data View]**&#x200B;을 클릭하여 출력의 데이터 보기 표현을 검토합니다. 실제 피드 파일이 있으면 여기에 나열되며 다운로드할 수 있습니다.
1. 클릭 **[!UICONTROL Close]**.

## Adobe Analytics SAINT 피드 편집 {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

만든 기존 SAINT 피드의 모든 측면을 편집할 수 있습니다.

**Adobe Analytics SAINT 피드를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL Saint Classification Feeds] 페이지의 **[!UICONTROL Name]** 열의 피드 옆의 드롭다운 목록에서 **[!UICONTROL Edit feed]**&#x200B;를 클릭합니다.
1. SAINT 피드 대화 상자의 **피드 이름** 텍스트 필드에 새 피드 이름을 입력한 다음 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

   이때 피드가 저장되고 [!DNL SAINT Classification Feed] 페이지에 추가됩니다. 선택하는 경우 나중에 피드를 종료하고 편집하여 마법사를 완료할 수 있습니다.
1. [!DNL Authentication] 페이지에서 각 텍스트 필드에 Adobe Analytics 회사 이름, 사용자 이름 및 웹 암호를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics에서 웹 API를 사용할 수 있는 권한이 있는지 확인합니다.
1. **[!UICONTROL Report Suite]** 페이지에서 보고서 세트와 그 분류 데이터 세트를 선택한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. [!DNL Field Maps] 페이지에서 Adobe Analytics 분류를 사이트 검색/머천다이징 메타 데이터 필드에 매핑한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics 분류를 조정하려면 **[!UICONTROL Edit]** Adobe Analytics 분류를 클릭하여 Adobe Analytics에 로그인합니다. 변경을 완료했으면 **[!UICONTROL Refresh Classifications]**&#x200B;을 클릭하여 분류 선택 사항을 새로 고칩니다.
1. [!DNL Search Criteria] 페이지에서 사이트 검색/머천다이징의 데이터를 Adobe Analytics SAINT에 제출하기 전에 필터링할 수 있습니다. 규칙 빌더 인터페이스를 사용하여 여기에 필터 규칙을 구성한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.
1. [!DNL Configure FTP] 페이지에서 FTP 서버를 선택합니다. 데이터를 업로드할 빈도 수를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   각 피드에는 실수로 데이터가 손실되지 않도록 하는 자체 FTP 계정이 있습니다. 여기에서 새 Adobe Analytics FTP 계정을 만들 수 있습니다.
1. [!DNL Verification] 페이지에서 **[!UICONTROL Show Data View]**&#x200B;을 클릭하여 출력의 데이터 보기 표현을 검토합니다. 실제 피드 파일이 있으면 여기에 나열되며 다운로드할 수 있습니다.
1. 클릭 **[!UICONTROL Close]**.

## Adobe Analytics SAINT 피드 {#task_5319B1F4CA1A406393CFD7AE97258CEB} 삭제

더 이상 필요하거나 사용하지 않는 기존 Adobe Analytics SAINT 피드를 삭제할 수 있습니다.

**Adobe Analytics SAINT 피드를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL Saint Classification Feeds] 페이지의 **[!UICONTROL Name]** 열의 제거할 피드 옆의 드롭다운 목록에서 **[!UICONTROL Delete feed]**&#x200B;를 클릭합니다.
1. 삭제 대화 상자에서 **예**&#x200B;를 클릭하여 피드 삭제를 확인합니다.

## Adobe Analytics SAINT 피드 파일 {#task_F0C8BADD25E14E5DB30BF31D1F879FDB} 보기

기존 SAINT 피드의 [!DNL Verification] 페이지를 열어 출력의 데이터 보기 표현을 검토할 수 있습니다.

실제 피드 파일이 있으면 여기에 나열되며 텍스트 파일로 다운로드할 수 있습니다.

**Adobe Analytics SAINT 피드 파일을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL Saint Classification Feeds] 페이지의 **[!UICONTROL Name]** 열의 피드 옆의 드롭다운 목록에서 **[!UICONTROL View Feed Files]**&#x200B;를 클릭합니다.
1. (선택 사항) 피드 파일을 텍스트 파일로 저장하려면 **[!UICONTROL Download File]**&#x200B;을 클릭합니다.
1. [!DNL SAINT Classification Feeds] 페이지로 돌아가려면 **[!UICONTROL Close]**&#x200B;을 클릭합니다.

## Adobe Analytics SAINT 피드 테스트 {#task_9864D69BE3824FC29C10B36EE4855D25}

파일 업로드 없이 기존 Adobe Analytics SAINT 피드를 테스트할 수 있습니다.

[Adobe Analytics SAINT 피드 생성 및 업로드](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A)를 참조하십시오.

[Adobe Analytics SAINT 피드 파일 보기](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)를 참조하십시오.

**Adobe Analytics SAINT 피드 파일을 테스트하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL Saint Classification Feeds] 페이지의 **[!UICONTROL Name]** 열의 피드 옆의 드롭다운 목록에서 **[!UICONTROL Test Feed (No file upload)]**&#x200B;를 클릭합니다.
1. 피드의 처리가 완료되면 피드 이름의 드롭다운 목록에서 **[!UICONTROL View Feed Files]**&#x200B;을 클릭합니다.
1. [!DNL Verification] 페이지에서 **[!UICONTROL Download File]**&#x200B;을 클릭하여 피드 파일을 다운로드합니다.
1. [!DNL SAINT Classification Feeds] 페이지로 돌아가려면 **[!UICONTROL Close]**&#x200B;을 클릭합니다.

## Adobe Analytics SAINT 피드 생성 및 업로드 {#task_47AED946AA964334A877FDC8D4F6F00A}

만든 기존 Adobe Analytics 피드에 대한 피드 파일을 생성하고 업로드할 수 있습니다.

[Adobe Analytics SAINT 피드 테스트](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25)를 참조하십시오.

[Adobe Analytics SAINT 피드 파일 보기](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)를 참조하십시오.

**Adobe Analytics SAINT 피드 파일을 생성하고 업로드하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;를 클릭합니다.
1. [!DNL Saint Classification Feeds] 페이지의 **[!UICONTROL Name]** 열의 피드 옆의 드롭다운 목록에서 **[!UICONTROL Generate and Upload Feed]**&#x200B;를 클릭합니다.
1. 피드의 처리가 완료되면 피드 이름의 드롭다운 목록에서 **[!UICONTROL View Feed Files]**&#x200B;을 클릭합니다.
1. [!DNL Verification] 페이지에서 **[!UICONTROL Download File]**&#x200B;을 클릭하여 피드 파일을 다운로드합니다.
1. [!DNL SAINT Classification Feeds] 페이지로 돌아가려면 **[!UICONTROL Close]**&#x200B;을 클릭합니다.
