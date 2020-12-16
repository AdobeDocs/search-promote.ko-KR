---
description: 쿼리 정리 규칙을 사용하여 들어오는 쿼리를 분석하고 수정합니다.
seo-description: 쿼리 정리 규칙을 사용하여 들어오는 쿼리를 분석하고 수정합니다.
seo-title: 쿼리 정리 규칙 정보
solution: Target
title: 쿼리 정리 규칙 정보
topic: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1611'
ht-degree: 1%

---


# 쿼리 정리 규칙 정보{#about-query-cleaning-rules}

쿼리 정리 규칙을 사용하여 들어오는 쿼리를 분석하고 수정합니다.

## 쿼리 정리 규칙 사용 {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

이 기능은 사이트 검색/머천다이징 비헤이비어를 수정하려는 경우에 종종 사용됩니다. 예를 들어 빈 검색을 &quot;*&quot; 검색 대신 인기 있는 키워드로 변경하여 인기 있는 제품을 홍보할 수 있습니다. 쿼리 정리 규칙을 사용하여 URL로 리디렉션하는 직접 히트를 수행할 수도 있습니다. 이 기능은 다른 사람이 제품 SKU를 검색하고 있는 경우 검색을 건너뛰고 해당 제품의 페이지로 리디렉션하려는 경우에 특히 유용합니다. 쿼리 청소는 또한 쿼리를 확인하고 나중 처리 흐름 단계에 사용할 수 있는 사용자 지정 변수를 설정할 수도 있습니다. 쿼리 정리 규칙은 모든 쿼리에 대해 순서대로 실행됩니다. 규칙 순서를 변경하려면 드래그 앤 드롭을 사용할 수 있습니다. 실제 주문은 저장할 때까지 변경되지 않습니다.

쿼리 정리 모듈의 쿼리 정리 규칙은 쿼리 매개 변수를 수정해야 하는지 또는 사용자 지정 변수를 설정해야 하는지 결정하기 위해 검사합니다. 각 쿼리 정리 규칙은 다음 두 가지 주요 요소로 구성됩니다.규칙의 작업 및 선택적 조건. 규칙 및 조건 수를 제한 없이 지정할 수 있습니다. 사이트 검색/머천다이징은 규칙별로 규칙 세트 규칙을 반복하므로 이러한 규칙의 순서가 중요합니다. 규칙의 조건이 일치하면 관련된 모든 작업이 수행됩니다.

쿼리 청소가 완료되면 결과 CGI 매개 변수가 계속 사용됩니다. 설정된 모든 사용자 지정 변수는 처리 흐름의 이후 단계에서 사용할 수 있습니다. 기본적으로 시스템은 쿼리 용어에서 선행 및 후행 공백을 자동으로 제거합니다.

## 쿼리 정리 조건 정보 {#section_BF6F25F94FED4DDEA8600D921EA43A66}

조건은 선택 사항입니다. 모든 쿼리에 대해 작업이 지정되도록 결정하는 경우 작업이 항상 수행됩니다. 조건은 이전 규칙이 설정한 CGI 쿼리 매개 변수, 기존 쿠키 또는 사용자 지정 변수를 기반으로 할 수 있습니다. 첫 번째 쿼리 정리 규칙이 모든 쿼리에 대해 실행되도록 &quot;우수 사례&quot;로 간주됩니다. 여기서 이 규칙은 사용하려는 모든 사용자 지정 변수를 정의하고 초기화합니다.

## 쿼리 정리 작업 정보 {#section_78F74A9B48DE484191CDA95F5B4E7154}

조건이 일치하는 쿼리 정리 규칙 내의 모든 작업이 적용됩니다. 작업은 일반적으로 작업, 작업을 수행할 데이터 및 사용할 값으로 구성됩니다.

[쿼리 정리 규칙 추가](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)의 옵션 표를 참조하십시오.

## 리디렉션 정보 {#section_597481E6194440C0A7B9E6FC901A81C0}

직접 히트 인터페이스를 사용하면 들어오는 쿼리 용어를 기반으로 리디렉션 집합을 정의할 수 있습니다. 쿼리 정리 내의 리디렉션은 이 아이디어를 확장합니다. 하지만 리디렉션을 사용하면 조건 지정을 통해 리디렉션이 언제 실행되는지 세부적으로 확인할 수 있으며 정적 URL이 아닌 동적 URL로 리디렉션할 수 있습니다. 리디렉션 작업을 선택하면 리디렉션할 URL을 지정하는 텍스트 상자가 표시되도록 행이 업데이트됩니다. URL에서 이중 중괄호로 묶은 후 대체할 변수 또는 매개 변수를 지정할 수 있습니다. 사용자 지정 변수는 대체에서 CGI 매개 변수보다 우선 순위가 높습니다.

## 예 {#section_DB5047CC38FB4A57B15CAAF9848073E3}

웹 사이트가 있는 의류 소매점이 있다고 가정합니다. 사용자가 검색어 없이 검색을 클릭하는 경우, 그것이 국제적으로 알려진 것이기 때문에 청바지에 대한 검색을 반환하려고 합니다. 나중에 각 성별에 대해 다른 프레젠테이션 템플릿을 사용하는 사용자 지정 변수를 기준으로 사전 검색 규칙을 만들 수 있도록 쿼리 용어를 성별을 구문 분석하려고 합니다.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

메가일렉트로닉스는 대형 전자 제품 매장이다. MegaElectronic은 검색 데이터를 분석함으로써 많은 전문 고객들이 단일 제품에 대한 검색 결과를 반환하는 대신 해당 SKU와 연관된 웹 페이지로 리디렉션하고자 하는 경우가 많습니다.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## 쿼리 정리 규칙 {#task_47F43988D3D9485F8AE1DFDA7E00BF54} 추가

고객으로부터 들어오는 검색 쿼리를 정리하거나 편집하는 규칙을 정의할 수 있습니다.

현재 존재하는 템플릿만 선택할 수 있습니다. 템플릿이 없는 경우에는 먼저 템플릿을 정의해야 합니다.

[템플릿 정보](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)를 참조하십시오.

**쿼리 정리 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**&#x200B;을 클릭합니다.
1. [!DNL Query Cleaning Rules] 페이지에서 **[!UICONTROL Add New Rule]**&#x200B;을 클릭합니다.
1. [!DNL Name] 필드에 새 쿼리 정리 규칙의 이름을 입력합니다.
1. [!DNL Add Query Cleaning Rule] 페이지에서 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>쿠키 </p> </td> 
      <td colname="col2"> <p>HTTP 쿠키. 도메인과 연결된 쿠키를 기반으로 조건을 정의할 수 있습니다. 또는 나가는 검색 결과로 기록된 쿠키를 설정할 수 있습니다. 쿠키 이름 및 값은 균일 리소스 식별자로 인코딩되어야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>사용자 지정 변수 </p> </td> 
      <td colname="col2"> <p>사용자 정의 변수. 사용자 정의 변수를 제한 없이 추가, 삭제 또는 설정할 수 있습니다. 사전 검색 규칙 및 사후 검색 규칙 내에서 사용자 정의 변수를 참조할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시스템 변수 </p> </td> 
      <td colname="col2"> <p>확인할 수 있는 내부 시스템에 의해 설정된 읽기 전용 변수. 지원되는 시스템 변수는 다음과 같습니다. </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname  </span> <p>서버 호스트의 이름입니다. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>쿼리 문자열 없이 요청된 URI입니다. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>전체 쿼리 문자열. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> 환경 </span> <p>들어오는 쿼리가 스테이지되거나 라이브 환경으로 전송되었는지 여부에 따라 "스테이지" 또는 "라이브"가 됩니다. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>고객이 보낸 URL. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> 사용자 에이전트  </span> <p>고객 브라우저의 "user-agent" 문자열입니다. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>쿼리 매개 변수 </p> </td> 
      <td colname="col2"> <p>쿼리에 전달된 CGI 매개 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>백엔드 매개 변수 </p> </td> 
      <td colname="col2"> <p>들어오는 쿼리 매개 변수는 검색을 수행하는 데 사용되는 백엔드 매개 변수로 최종 변환됩니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 백엔드 검색 CGI 매개 변수 </a>를 참조하십시오. </p> <p>백엔드 매개 변수가 탐색 요소에 표시되지 않습니다. 따라서 고객의 검색에 적용할 추가 매개 변수를 숨길 수 있습니다. 백엔드 매개 변수에 대한 작업은 늦은 바인딩입니다.즉, 검색이 전송되기 직전에 적용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 </p> </td> 
      <td colname="col2"> <p>주어진 패싯과 연결된 특수 CGI 매개 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>등급 </p> </td> 
      <td colname="col2"> <p>검색에 사용할 등급 규칙을 지정할 수 있습니다. 이 옵션은 일부 등급 필드와 등급 규칙이 정의된 경우에만 나타납니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>스토어 </p> </td> 
      <td colname="col2"> <p>검색 엔진은 사용자가 호스트 이름 또는 <span class="codeph"> gs_store </span> 쿼리 매개 변수를 기반으로 하는 스토어를 자동으로 감지합니다. 이 쿼리 매개 변수는 후자의 우선 순위가 높습니다. 매장 밖에서 조건을 만들 수 있습니다. 쿼리 청소에서만 작업을 사용하여 현재 스토어를 오버라이드할 수도 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>마지막 규칙 </p> </td> 
      <td colname="col2"> <p>마지막 규칙 세트가 있는 규칙에 대해 조건이 충족되면 쿼리 정리 처리 모듈은 일치 규칙 작업 후 추가 규칙을 수행하지 않습니다. 이 기능은 이후 규칙이 일치하지만 이후 규칙이 실행되지 않게 하는 작업을 설정한 경우에 유용합니다. 규칙 작업이 리디렉션을 수행하는 경우 리디렉션이 즉시 수행되므로 기본적으로 마지막 규칙이 설정된 것처럼 동작합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>일시 중단 </p> </td> 
      <td colname="col2"> <p>규칙 실행을 해제하지만 규칙을 삭제하지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 쿼리 정리 규칙 편집 {#task_FA2FF1A7E2634350AD703485CBC27CB3}

쿼리 정리 규칙 페이지에 추가한 기존 쿼리 정리 규칙을 편집할 수 있습니다.

**쿼리 정리 규칙을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**&#x200B;을 클릭합니다.
1. [!DNL Query Cleaning Rules] 페이지의 테이블의 **[!UICONTROL Actions]** 열에서 편집할 관련 규칙의 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Edit Query Cleaning Rule] 페이지에서 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

   [쿼리 정리 규칙 추가](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 쿼리 정리 규칙 삭제 중 {#task_C52D17226B824590B087CAB6970CBB01}

더 이상 필요하거나 사용하지 않는 쿼리 정리 규칙을 삭제할 수 있습니다.

규칙을 삭제하면 나머지 규칙이 실행되는 순서가 자동으로 조정되어 삭제가 적용됩니다.

**쿼리 정리 규칙을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**&#x200B;을 클릭합니다.
1. [!DNL Query Cleaning Rules] 페이지의 테이블의 **[!UICONTROL Actions]** 열에서 삭제할 연관된 규칙의 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. [!DNL Confirmation] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 쿼리 정리 규칙이 {#task_C24012C45A4445468A7FD998017388CA}을(를) 실행하는 순서 변경

쿼리 정리 규칙의 순서를 변경하여 프레젠테이션 템플릿에서 실행되는 순서를 변경할 수 있습니다.

쿼리 정리 규칙은 정의된 순서대로 실행됩니다. 규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. [!DNL Query Cleaning Rules] 페이지의 테이블의 [순서] 열에 새 번호를 입력하여 규칙 순서를 변경합니다. 또한 규칙을 드래그 앤 드롭하여 실행 순서를 변경할 수도 있습니다.

**쿼리 정리 규칙이 실행되는 순서를 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**&#x200B;을 클릭합니다.
1. [!DNL Query Cleaning Rules] 페이지에서 다음 중 하나를 수행합니다.

   * [!DNL Order] 열 헤더를 클릭하여 오름차순 또는 내림차순으로 규칙을 정렬합니다.
   * 쿼리 정리 규칙 이름의 왼쪽에 있는 텍스트 필드에 규칙을 실행할 순서 번호를 입력합니다.[!DNL Order]
   * 테이블 행을 규칙 실행 위치로 드래그하여 놓습니다. 모든 주문 번호는 규칙이 실행되는 새 순서를 반영하도록 업데이트됩니다.

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

