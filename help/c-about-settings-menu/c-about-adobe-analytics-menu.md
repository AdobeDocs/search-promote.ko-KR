---
description: Adobe Analytics 메뉴를 사용하여 Adobe Analytics 지표 인증을 설정하거나, 보고서 세트의 Adobe Analytics 지표를 관리하거나, SAINT를 사용하여 외부 소스에서 표 형식의 데이터를 허용하여 Adobe Analytics 보고서를 향상시킵니다.
seo-description: Adobe Analytics 메뉴를 사용하여 Adobe Analytics 지표 인증을 설정하거나, 보고서 세트의 Adobe Analytics 지표를 관리하거나, SAINT를 사용하여 외부 소스에서 표 형식의 데이터를 허용하여 Adobe Analytics 보고서를 향상시킵니다.
seo-title: Adobe Analytics 메뉴 정보
solution: Target
subtopic: Adobe Analytics
title: Adobe Analytics 메뉴 정보
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Adobe Analytics 메뉴 정보{#about-the-adobe-analytics-menu}

Adobe Analytics 메뉴를 사용하여 Adobe Analytics 지표 인증을 설정하거나, 보고서 세트의 Adobe Analytics 지표를 관리하거나, SAINT를 사용하여 외부 소스에서 표 형식의 데이터를 허용하여 Adobe Analytics 보고서를 향상시킵니다.

## Adobe Analytics 지표 인증 설정 {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Adobe Analytics 지표를 사이트 검색/머천다이징 등급에 통합하려면 먼저 Adobe Analytics 웹 서비스 로그인을 획득해야 합니다. 로그인 정보를 얻은 후 이를 사용하여 사이트 검색/머천다이징에서 Adobe Analytics 인증을 설정할 수 있습니다.

**Adobe Analytics 지표 인증을 설정하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**&#x200B;을 클릭합니다.
1. 페이지에서 각 [!DNL Setup Adobe Analytics Metrics Authentication] 필드에 요청한 정보를 지정합니다.

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
      <td colname="col2"> <p>Adobe Analytics 계정과 연결된 웹 서비스 사용자 이름입니다. </p> <p>이 정보는 Adobe Analytics에서 얻을 수 있습니다. Adobe Analytics 메뉴 모음에서 관리 &gt; <span class="uicontrol"> 관리 콘솔 <b>&gt;</b> 관리 </span> 회사 <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span>&gt; Web Services를 클릭합니다. 정보는 API 액세스 정보 표에 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>웹 서비스 공유 암호 </p> </td> 
      <td colname="col2"> <p>Adobe Analytics 계정과 관련된 웹 서비스 공유 암호. </p> <p>이 정보는 Adobe Analytics에서 얻을 수 있습니다. Adobe Analytics 메뉴 모음에서 관리 &gt; <span class="uicontrol"> 관리 콘솔 <b>&gt;</b> 관리 </span> 회사 <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span>&gt; Web Services를 클릭합니다. 정보는 API 액세스 정보 표에 있습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## Adobe Analytics 보고서 세트 정보 {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

사이트 검색/머천다이징 내에서 Adobe Analytics 보고서 세트 데이터를 사용하려면 먼저 사이트 검색/머천다이징 계정에서 Adobe Analytics 데이터 사본을 만들어야 합니다.

새 Adobe Analytics 보고서 세트 정의를 만들거나 기존 Adobe Analytics 보고서 세트 및 관련 지표를 보거나 수정할 수 있습니다.

사이트 검색/머천다이징 내에서 Adobe Analytics에 처음 액세스하는 경우 회사의 사용 가능한 보고서 세트 목록이 다운로드되고 캐시됩니다. 새 보고서 세트가 최근에 추가되었거나 기존 보고서 세트가 제거된 경우 보고서 세트 목록을 새로 고쳐 보고서 세트 목록을 다시 다운로드할 수 있습니다.

## Adobe Analytics 보고서 세트 추가 {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

사이트 검색/머천다이징 등급 규칙을 기준으로 할 Adobe Analytics 보고서 세트를 선택할 수 있습니다.

선택할 수 있는 목록은 Adobe Analytics 계정 내에서 사용할 수 있는 보고서 세트와 일치해야 합니다. 선택한 보고서 세트에 따라 사이트 검색/머천다이징 등급 규칙 내에서 사용할 수 있는 지표가 결정됩니다.

[등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

Adobe Analytics 보고서 세트를 추가한 후 해당 지표를 편집할 수 있습니다.

보고서 [세트의 Adobe Analytics 지표 편집을 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Adobe Analytics 보고서 세트를 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. Adobe Analytics 보고서 세트 페이지에서 을 클릭합니다 **[!UICONTROL Add Report Suite]**.
1. 새로 추가된 테이블 행의 드롭다운 목록에서 원하는 보고서 세트를 선택합니다.
1. 보고서 세트의 Adobe Analytics 지표를 편집합니다.

## 보고서 세트의 Adobe Analytics 지표 편집 {#task_360904CCBBB140238ADA036C3CC07664}

사이트 검색/머천다이징에서 Adobe Analytics 지표를 등급 규칙에 통합하려면 선택한 보고서 세트와 관련된 지표 중 하나 이상을 선택합니다. 그런 다음 Adobe Analytics 웹 서비스를 통해 지표 데이터를 가져오는 데 사용되는 옵션을 구성합니다.

Adobe [Analytics 보고서 세트 추가를 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

고급 [Adobe Analytics 옵션](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19)구성을 참조하십시오.

**보고서 세트의 Adobe Analytics 지표를 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Adobe Analytics Report Suites] 열에서 지표를 구성할 보고서 세트를 **[!UICONTROL Actions]** **[!UICONTROL Edit]** 클릭합니다.
1. 페이지에서 필요한 지표를 [!DNL Edit Adobe Analytics Metrics] 설정합니다. 지표 이름 옆에 별표(*)가 없는 지표는 선택 사항입니다.

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
      <td colname="col2"> <p>선택한 보고서 세트와 함께 사용할 보고서 유형 값을 지정합니다. 이 값은 반환된 각 결과 행에 대한 키를 식별합니다. </p> <p>보고서 유형을 Adobe Analytics 요소라고도 합니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>상호 참조 필드 이름 </p> </td> 
      <td colname="col2"> <p>값이 보고서 세트의 데이터에 대한 조회 "키"로 사용되는 메타데이터 필드를 지정합니다. </p> <p>선택된 값이 없는 경우("— None —") 이 보고서 세트의 데이터를 계산(" <span class="uicontrol"> None")에 사용할 수 없습니다 <b>([U.S.O. N. R. A. T.]</b> &gt; [Ranking Rules </span> Paging Rules <span class="uicontrol"> ] <b>None</b> &gt; Ranking RulesPagainingRanks </span> <span class="uicontrol"> <b></b> </span>). </p> <p>값을 선택하면 이 필드의 값이 이전에 설정한 선택된 보고서 유형 값을 사용하여 이 보고서 세트의 Adobe Analytics 데이터로 사이트 검색/머천다이징 문서를 상호 참조하는 데 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색어 보고서 </p> </td> 
      <td colname="col2"> <p>단계 Adobe Analytics 데이터 미리 보기 페이지에서 비즈니스 규칙을 만들고 <b>검색어를 시뮬레이션할 수</b> 있습니다. </p> <p>Adobe <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Analytics 데이터 미리 보기를 참조하십시오</a>. </p> <p>두 가지 옵션이 포함된 모든 행에 풀다운 메뉴가 나타납니다.검색어를 <b>시뮬레이션하고</b> 새 <b>비즈니스 규칙 만들기를 참조하십시오</b>. </p> <p>두 옵션 모두 보고서 유형의 데이터를 검색어로 사용합니다. 따라서 이 기능은 보고서 유형이 검색어를 나타내는 경우에만 의미가 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>지표 </p> </td> 
      <td colname="col2"> <p>사이트 검색/머천다이징 등급 규칙 내에서 다운로드하고 사용하려는 지표 값을 식별합니다. </p> <p>여기에서 구성하는 지표는 [ <span class="uicontrol"> 규칙 <b>] &gt; [규칙</b> ] &gt; [규칙 편집 </span><span class="uicontrol"> ] <b>[규칙 편집</b> ] &gt; [구성원 센터] 페이지에서 규칙의 데이터 유형이 [Adobe Analytics 지표(Analytics 번호)로 설정된 경우 [규칙 </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> </span>] &gt; [규칙 편집]을 선택하여 나타납니다. 선택 사항에는 보고서 세트 이름 또는 보고서 세트 보기 이름(지정된 경우)과 개별 지표 이름의 조합이 표시됩니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 지표 값 </p> </td> 
      <td colname="col2"> <p>0이 아닌 값을 입력하여 지표의 최소 값을 지정할 수 있습니다. </p> <p>비어 있거나 0인 경우 지표에 대한 모든 값이 다운로드됩니다.그렇지 않으면 최소 지표 값이 전달되면 이 지표에 대한 다운로드가 중지됩니다. </p> <p>Adobe Analytics 지표는 내림차순으로 검색됩니다. </p> <p>추가 지표 정의를 추가하려면 <span class="uicontrol"><b>+</b> </span> 를 클릭합니다.더 이상 <span class="uicontrol"> 필요 <b>또는 필요 없는 지표 정의를 제거하려면 클릭-</b> </span> 을 클릭합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 지표 집계 기간(일) </p> </td> 
      <td colname="col2"> <p> 가져올 Adobe Analytics 지표의 일수를 제어하여 어제 날짜로부터 다시 계산합니다. 현재 날짜의 데이터를 가져오려고 시도하지 않습니다. </p> <p>기본값은 7입니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adobe Analytics 다운로드 새로 고침 빈도(일) </p> </td> 
      <td colname="col2"> <p> 등급 계산에 사용되는 Adobe Analytics 데이터의 다운로드 간 최소 간격을 설정합니다. </p> <p>다운로드 새로 고침 빈도 간격 내에 발생하는 색인 트리거 다운로드는 무시됩니다. 그러나 수동 다운로드는 이 값을 무시합니다. </p> <p>이 값을 기본값 1로 설정하면 Adobe Analytics 데이터가 24시간 내에 두 번 이상 다운로드되지 않습니다. 다운로드 새로 고침 빈도 간격 내에 발생하는 모든 검색 색인은 마지막으로 다운로드한 데이터 세트를 사용합니다. </p> <p>이 지표는 필수입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   See also [About Ranking Rules](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. 클릭 **[!UICONTROL Save Changes]**.

   단계 [!DNL Adobe Analytics Report Suites] 페이지로 돌아갑니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## Adobe Analytics 보고서 세트 삭제 {#task_0ACA172214D14654ABDB139F417B9F7D}

삭제를 사용하여 [!DNL Adobe Analytics Report Suites] 페이지에서 보고서 세트를 제거할 수 있습니다. 보고서 세트를 삭제하면 사이트 검색/머천다이징 서버에서 데이터 복사본만 제거됩니다.Adobe Analytics 시스템의 데이터는 영향을 주지 않습니다.

**Adobe Analytics 보고서 세트를 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Adobe Analytics Report Suites] 열 아래에서 제거할 보고서 **[!UICONTROL Actions]** **[!UICONTROL Delete]** 세트를 클릭합니다.
1. 페이지에서 [!DNL Adobe Analytics Delete Report Suite] 을 클릭합니다 **[!UICONTROL Delete]**.

## Adobe Analytics 데이터 미리 보기 {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

미리 보기를 사용하여 최근에 로드한 Adobe Analytics 지표를 볼 수 있습니다.

표의 행 열에는 Adobe Analytics 지표가 로드되었던 원래 순서를 나타내는 각 지표 데이터 행 수가 표시됩니다.

제품 열에는 각 지표 데이터 행과 연관된 Adobe Analytics 요소가 표시됩니다. 이 열의 값은 등급 정의에 구성된 대로 사이트 검색/머천다이징 페이지를 해당 지표 값과 연결하는 데 사용됩니다.

[등급 규칙 정보](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397)를 참조하십시오.

등급 [구성을](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)참조하십시오.

나머지 열에는 각 항목과 연관된 지표 값이 표시됩니다.

테이블이 비어 있으면 Adobe Analytics 데이터를 아직 로드하지 않았음을 의미합니다. 페이지를 닫은 다음 Adobe Analytics 데이터를 로드할 수 [!DNL Adobe Analytics Data Preview] 있습니다.

Adobe [Analytics 데이터](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)로드를 참조하십시오.
표를 검색어 보고서로 지정한 경우 모든 행에 작은 삼각형이 나타납니다. 드롭다운 목록을 클릭하고 검색어 시뮬레이션 또는 **새 비즈니스 규칙 만들기를** 선택할 **수 있습니다**. 선택한 작업이 해당 행의 검색어, 두 번째 열에 있는 데이터에 적용됩니다

**Adobe Analytics 데이터를 미리 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. 페이지의 [!DNL Adobe Analytics Report Suites] 열에서 다운로드한 데이터를 보려는 보고서 세트를 [!DNL Actions] **[!UICONTROL Preview]** 클릭합니다.

   * 클릭 **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. 페이지의 [!DNL Adobe Analytics Terms Report] 열에서 다운로드한 데이터를 보려는 보고서 세트를 [!DNL Actions] **[!UICONTROL Preview]** 클릭합니다.

1. 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 데이터를 봅니다. [!DNL Adobe Analytics Data Preview]

   테이블의 열 머리글을 클릭하여 데이터를 내림차순이나 오름차순으로 정렬합니다.
1. 다음 중 하나를 수행합니다.

   * 을 **[!UICONTROL Download to Desktop]** 클릭하여 표를 다운로드하고 `.xlt` 파일로 저장합니다.

   * Adobe Analytics 데이터 미리 보기를 마치면 페이지를 닫고 이전에 본 페이지로 돌아갑니다.

## 최신 Adobe Analytics 데이터 로드에서 로그 보기 {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

로그 보기를 사용하여 최신 다운로드 프로세스의 Adobe Analytics 데이터 로그 파일을 검사할 수 있습니다. 로그 보기를 사용하여 실행 중인 다운로드를 모니터링할 수도 있습니다.

Adobe [Analytics 데이터](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)로드를 참조하십시오.

**최신 Adobe Analytics 데이터 로드에서 로그를 보려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Adobe Analytics Report Suites] 을 클릭합니다 **[!UICONTROL View Log]**. 로그 페이지,
1. 페이지에서 페이지 위쪽과 아래쪽에 있는 탐색 및 보기 옵션을 사용하여 로그 정보를 봅니다. [!DNL Adobe Analytics Data Log]
1. 완료되면 페이지를 닫고 [!DNL Adobe Analytics Report Suites] 페이지로 돌아갑니다.

## Adobe Analytics 데이터 로드 {#task_2F3C55189B0A4049AB2113F2291CC181}

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
   <td colname="col2"> <p>마지막 데이터 로드 시도가 성공했는지 실패했는지 나타냅니다. 또는 이미 진행 중인 데이터 로드 작업의 상태가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 시도 동안 다운로드된 지표 데이터 행 수를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시작 시간 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 작업이 시작된 날짜와 시간을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중지 시간 </p> </td> 
   <td colname="col2"> <p>마지막 데이터 로드 작업의 완료 날짜 및 시간을 표시합니다. 또는 현재 데이터 로드 작업이 진행 중임을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Adobe Analytics 데이터를 로드하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Stage Adobe Analytics Report Suites] 을 클릭합니다 **[!UICONTROL Load Adobe Analytics Data]**.
1. 페이지에서 **[!UICONTROL Adobe Analytics Data Load]** 다음 중 하나를 수행합니다.

   * 을 **[!UICONTROL Start Load]** 클릭하여 로드 작업을 시작합니다.

      데이터 로드 작업 중에 **진행** 행은 진행 상태에 대한 정보를 제공합니다.

   * 을 **[!UICONTROL Stop Load]** 클릭하여 로드 작업을 중지합니다.

1. 을 **[!UICONTROL Close]** 클릭하여 [!DNL Stage Adobe Analytics Reports Suite] 페이지로 돌아갑니다.

## 보고서 세트 목록 새로 고침 {#task_EA6215D438CA4185B106657D9712ED34}

사이트 검색/머천다이징 사용자 인터페이스에서 처음으로 Adobe Analytics에 액세스하면 회사의 사용 가능한 Adobe Analytics 보고서 세트 목록이 다운로드되고 캐시됩니다. 새 보고서 세트가 최근에 추가되었거나 기존 보고서 세트가 삭제된 경우 보고서 세트 목록 새로 고침을 사용하여 사이트 검색/머천다이징에 현재 표시된 목록을 업데이트할 수 있습니다.

Adobe [Analytics 보고서 세트 추가를 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Adobe [Analytics 보고서 세트 삭제를 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D).

**보고서 세트 목록을 새로 고치려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Adobe Analytics Report Suites] 을 클릭합니다 **[!UICONTROL Refresh Report Suite List]**.

## 고급 Adobe Analytics 옵션 구성 {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

Adobe Analytics 보고서 세트 다운로드 프로세스의 동작을 세밀하게 조정하는 데 도움이 되는 설정을 제어하는 [!DNL Advanced Adobe Analytics Options] 데 사용할 수 있습니다.

보고서 [세트의 Adobe Analytics 지표 편집을 참조하십시오](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**고급 Adobe Analytics 옵션을 구성하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Advanced Adobe Analytics Options] 다음 옵션을 설정합니다.

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
      <td colname="col2"> <p> 한 번에 가져올 Adobe Analytics 지표 값의 수를 제어합니다. 지표 데이터 행은 모든 데이터를 검색하거나 최대 행 제한에 도달할 때까지 반복적으로 반입됩니다. </p> <p>일반적으로 이 설정을 변경할 필요가 없습니다. 그러나 사이트의 전체 재인덱스의 지표 다운로드 단계를 최적화하는 것이 도움이 될 수 있습니다. </p> <p>기본값은 5000입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## SAINT 분류 피드 정보 {#concept_C55609DA24914BBC92CD90ED0259199D}

Adobe Analytics SAINT 파섹 예를 들어 사이트 검색/머천다이징을 사용하여 자체 인덱스에서 데이터를 검색하고 해당 데이터를 Adobe Analytics로 내보낼 수 있습니다.

사이트 검색/머천다이징에서 Adobe Analytics SAINT 기능을 성공적으로 사용하려면 다음 요구 사항을 알고 있어야 합니다.

* Adobe Analytics 회사와 보고서 세트가 있어야 합니다.

   Adobe [Analytics 메뉴](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411)정보를 참조하십시오.
* Adobe Analytics 사용자 계정에는 보고서 세트를 수정할 수 있는 권한이 있어야 합니다.

   Adobe [Analytics 지표 인증](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42)설정을 참조하십시오.
* Adobe Analytics 사용자는 Adobe Analytics 웹 API를 사용할 수 있도록 웹 API 그룹에 속해야 합니다.
* 검색 색인에는 데이터가 올바른 형식으로 있는 경우와 같이 Adobe Analytics에서 사용할 수 있는 데이터가 있어야 합니다.

피드를 만들기 전에 SAINT 피드 마법사를 성공적으로 완료할 수 있도록 다음 질문과 정보를 검토하십시오.

* 어떤 보고서 세트와 함께 작업하시겠습니까?
* 제품, e-var 등과 같은 분류 세트를 사용할 데이터를 제공하시겠습니까?
* 보고서에 어떤 분류가 있습니까? 이 질문에 대한 답변은 사이트 검색/머천다이징에서 쉽게 사용할 수 있는 데이터 유형과 Adobe Analytics가 바람직한 보고서 유형에 따라 결정됩니다.
* SAINT는 사이트 검색/머천다이징의 데이터를 텍스트 유형으로 허용합니다. 해당 데이터의 형식은 Adobe Analytics 보고서의 프레젠테이션에 영향을 줍니다.

## Adobe Analytics SAINT 피드 만들기 {#task_914B5AB821E84627953D8EF9339A7DD0}

Adobe Analytics SAINT 파섹

예를 들어 사이트 검색/머천다이징을 사용하여 자체 인덱스에서 데이터를 검색하고 해당 데이터를 Adobe Analytics로 내보낼 수 있습니다.

**Adobe Analytics SAINT 피드를 만들려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL SAINT Classification Feeds] 을 클릭합니다 **[!UICONTROL Create SAINT Feed]**.
1. 대화 [!DNL Create Feed] 상자의 피드 **이름** 텍스트 필드에 새 피드 이름을 입력한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   이때 피드가 저장되고 [!DNL SAINT Classification Feed] 페이지에 추가됩니다. 선택하는 경우 나중에 피드를 종료하고 편집하여 마법사를 완료할 수 있습니다.
1. 페이지에서 [!DNL Authentication] 각 텍스트 필드에 Adobe Analytics 회사 이름, 사용자 이름 및 웹 암호를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics에서 웹 API를 사용할 수 있도록 인증되었는지 확인합니다.
1. 페이지에서 보고서 **[!UICONTROL Report Suite]** 세트와 해당 분류 데이터 세트를 선택한 다음 을 클릭합니다 **[!UICONTROL Next]**.
1. 페이지에서 Adobe [!DNL Field Maps] Analytics 분류를 사이트 검색/머천다이징 메타 데이터 필드에 매핑한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics 분류를 조정하려면 Adobe Analytics **[!UICONTROL Edit]** 분류를 클릭하여 Adobe Analytics에 로그인합니다. 변경을 완료하면 을 클릭하여 분류 선택을 새로 **[!UICONTROL Refresh Classifications]** 고칩니다.
1. 페이지에서 사이트 검색/머천다이징의 데이터를 Adobe Analytics SAINT에 제출하기 전에 필터링할 수 있습니다. [!DNL Search Criteria] 규칙 빌더 인터페이스를 사용하여 여기에 필터 규칙을 구성한 다음 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 페이지에서 FTP [!DNL Configure FTP] 서버를 선택합니다. 데이터 업로드 빈도를 지정한 다음 을 **[!UICONTROL Next]**&#x200B;클릭합니다.

   각 피드에는 실수로 데이터가 손실되지 않도록 하기 위한 자체 FTP 계정이 있는 것이 좋습니다. 여기에서 새 Adobe Analytics FTP 계정을 만들 수 있습니다.
1. 페이지에서 [!DNL Verification] 을 클릭하여 출력의 데이터 보기 표현을 **[!UICONTROL Show Data View]** 검토합니다. 실제 피드 파일이 있으면 여기에 나열되며 다운로드할 수 있습니다.
1. 클릭 **[!UICONTROL Close]**.

## Adobe Analytics SAINT 피드 편집 {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

만든 기존 SAINT 피드의 모든 측면을 편집할 수 있습니다.

**Adobe Analytics SAINT 피드를 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Saint Classification Feeds] 열에서 피드 옆에 있는 **[!UICONTROL Name]** 드롭다운 목록에서 을 클릭합니다 **[!UICONTROL Edit feed]**.
1. SAINT 피드 대화 상자의 피드 **이름** 텍스트 필드에 새 피드 이름을 입력한 다음 을 **[!UICONTROL Next]**&#x200B;클릭합니다.

   이때 피드가 저장되고 [!DNL SAINT Classification Feed] 페이지에 추가됩니다. 선택하는 경우 나중에 피드를 종료하고 편집하여 마법사를 완료할 수 있습니다.
1. 페이지에서 [!DNL Authentication] 각 텍스트 필드에 Adobe Analytics 회사 이름, 사용자 이름 및 웹 암호를 지정한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics에서 웹 API를 사용할 수 있도록 인증되었는지 확인합니다.
1. 페이지에서 보고서 **[!UICONTROL Report Suite]** 세트와 해당 분류 데이터 세트를 선택한 다음 을 클릭합니다 **[!UICONTROL Next]**.
1. 페이지에서 Adobe [!DNL Field Maps] Analytics 분류를 사이트 검색/머천다이징 메타 데이터 필드에 매핑한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   Adobe Analytics 분류를 조정하려면 Adobe Analytics **[!UICONTROL Edit]** 분류를 클릭하여 Adobe Analytics에 로그인합니다. 변경을 완료하면 을 클릭하여 분류 선택을 새로 **[!UICONTROL Refresh Classifications]** 고칩니다.
1. 페이지에서 사이트 검색/머천다이징의 데이터를 Adobe Analytics SAINT에 제출하기 전에 필터링할 수 있습니다. [!DNL Search Criteria] 규칙 빌더 인터페이스를 사용하여 여기에 필터 규칙을 구성한 다음 을 **[!UICONTROL Next]**&#x200B;클릭합니다.
1. 페이지에서 FTP [!DNL Configure FTP] 서버를 선택합니다. 데이터 업로드 빈도를 지정한 다음 을 **[!UICONTROL Next]**&#x200B;클릭합니다.

   각 피드에는 실수로 데이터가 손실되지 않도록 하기 위한 자체 FTP 계정이 있는 것이 좋습니다. 여기에서 새 Adobe Analytics FTP 계정을 만들 수 있습니다.
1. 페이지에서 [!DNL Verification] 을 클릭하여 출력의 데이터 보기 표현을 **[!UICONTROL Show Data View]** 검토합니다. 실제 피드 파일이 있으면 여기에 나열되며 다운로드할 수 있습니다.
1. 클릭 **[!UICONTROL Close]**.

## Adobe Analytics SAINT 피드 삭제 {#task_5319B1F4CA1A406393CFD7AE97258CEB}

더 이상 필요하거나 사용하지 않는 기존 Adobe Analytics SAINT 피드를 삭제할 수 있습니다.

**Adobe Analytics SAINT 피드를 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Saint Classification Feeds] 열 아래에 있는 **[!UICONTROL Name]** 드롭다운 목록에서 제거할 피드를 클릭합니다 **[!UICONTROL Delete feed]**.
1. 삭제 대화 상자에서 예를 클릭하여 **피드** 삭제를 확인합니다.

## Adobe Analytics SAINT 피드 파일 보기 {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

기존 SAINT 피드의 [!DNL Verification] 페이지를 열어 출력의 데이터 보기 표현을 검토할 수 있습니다.

실제 피드 파일이 있으면 여기에 나열되며 텍스트 파일로 다운로드할 수 있습니다.

**Adobe Analytics SAINT 피드 파일을 보려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Saint Classification Feeds] 열에서 피드 옆에 있는 **[!UICONTROL Name]** 드롭다운 목록에서 을 클릭합니다 **[!UICONTROL View Feed Files]**.
1. (선택 사항) 을 **[!UICONTROL Download File]** 클릭하여 피드 파일을 텍스트 파일로 저장합니다.
1. 을 **[!UICONTROL Close]** 클릭하여 [!DNL SAINT Classification Feeds] 페이지로 돌아갑니다.

## Adobe Analytics SAINT 피드 테스트 {#task_9864D69BE3824FC29C10B36EE4855D25}

파일 업로드 없이 기존 Adobe Analytics SAINT 피드를 테스트할 수 있습니다.

Adobe [Analytics SAINT 피드](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A)생성 및 업로드를 참조하십시오.

Adobe [Analytics SAINT 피드 파일](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)보기를 참조하십시오.

**Adobe Analytics SAINT 피드 파일을 테스트하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Saint Classification Feeds] 열에서 피드 옆에 있는 **[!UICONTROL Name]** 드롭다운 목록에서 을 클릭합니다 **[!UICONTROL Test Feed (No file upload)]**.
1. 피드 처리가 완료되면 피드 이름의 드롭다운 목록에서 을(를) 클릭합니다. **[!UICONTROL View Feed Files]**
1. 페이지에서 을 클릭하여 피드 파일을 [!DNL Verification] **[!UICONTROL Download File]** 다운로드합니다.
1. 을 **[!UICONTROL Close]** 클릭하여 [!DNL SAINT Classification Feeds] 페이지로 돌아갑니다.

## Adobe Analytics SAINT 피드 생성 및 업로드 {#task_47AED946AA964334A877FDC8D4F6F00A}

만든 기존 Adobe Analytics 피드에 대한 피드 파일을 생성하고 업로드할 수 있습니다.

Adobe [Analytics SAINT 피드](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25)테스트를 참조하십시오.

Adobe [Analytics SAINT 피드 파일](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)보기를 참조하십시오.

**Adobe Analytics SAINT 피드 파일을 생성하고 업로드하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Saint Classification Feeds] 열에서 피드 옆에 있는 **[!UICONTROL Name]** 드롭다운 목록에서 을 클릭합니다 **[!UICONTROL Generate and Upload Feed]**.
1. 피드 처리가 완료되면 피드 이름의 드롭다운 목록에서 을(를) 클릭합니다. **[!UICONTROL View Feed Files]**
1. 페이지에서 을 클릭하여 피드 파일을 [!DNL Verification] **[!UICONTROL Download File]** 다운로드합니다.
1. 을 **[!UICONTROL Close]** 클릭하여 [!DNL SAINT Classification Feeds] 페이지로 돌아갑니다.
