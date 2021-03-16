---
description: 검색 전 규칙을 사용하여 들어오는 쿼리를 분석하고 사용할 프레젠테이션 템플릿을 결정합니다. 사전 검색 규칙은 모든 쿼리에 대해 차례로 실행됩니다. 규칙 순서를 변경하려면 드래그 앤 드롭을 사용할 수 있습니다. 실제 주문은 저장하기 전까지 변경되지 않습니다.
solution: Target
title: 사전 검색 규칙 정보
topic: 규칙, 사이트 검색 및 머천다이징
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 1%

---


# 사전 검색 규칙 정보{#about-pre-search-rules}

검색 전 규칙을 사용하여 들어오는 쿼리를 분석하고 사용할 프레젠테이션 템플릿을 결정합니다. 사전 검색 규칙은 모든 쿼리에 대해 차례로 실행됩니다. 규칙 순서를 변경하려면 드래그 앤 드롭을 사용할 수 있습니다. 실제 주문은 저장하기 전까지 변경되지 않습니다.

## 사전 검색 규칙 사용 {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

사전 검색 규칙은 일반적으로 들어오는 쿼리를 기반으로 결과를 표시하는 프레젠테이션 템플릿을 선택하는 데 사용됩니다. 프레젠테이션 템플릿에 대해 수행되는 검색에 사용되는 쿼리를 변경하는 데 고급 기능을 사용할 수 있습니다. 필요에 따라 쿼리 매개 변수의 값을 추가, 삭제 또는 변경할 수 있습니다. 들어오는 모든 쿼리에 대해 사전 검색 처리 모듈은 사전 검색 규칙을 검토하여 쿼리가 수정되었는지 여부와 어떤 프레젠테이션 템플릿이 사용되는지 확인합니다. 각 사전 검색 규칙은 다음 두 가지 주요 요소로 구성됩니다.규칙의 작업 및 선택적 조건. 규칙 및 조건 수를 제한 없이 지정할 수 있습니다. 규칙 세트는 규칙별로 반복되므로 이러한 규칙의 순서가 중요합니다. 규칙의 조건이 일치하면 연관된 모든 작업이 수행됩니다.

사전 검색 처리 모듈에서 각 검색에는 cgi 매개 변수의 로컬 복사본이 제공되므로 정의된 모든 템플릿과 해당 이름이 지정된 검색이 인스턴스화됩니다. 그 결과, 템플릿이 사용하는 다른 이름의 검색을 변경하거나 다른 템플릿에 영향을 주지 않고 검색하는 데 사용하는 cgi 매개 변수 중 하나를 추가, 삭제 또는 변경하여 검색을 사용자 정의할 수 있습니다. 따라서 두 개 이상의 결과 세트를 표시하는 프레젠테이션 템플릿이 있는 경우 각 검색을 개별적으로 사용자 정의할 수 있습니다. 각 템플릿에 대한 각 검색에 복사되기 전에 글로벌 CGI 매개 변수에 대한 변경 사항을 수행하려면 쿼리 정리 모듈을 사용합니다.

## 사전 검색 규칙 조건 {#section_B5568ADEB28546A280720309498B045D}

조건은 선택 사항입니다. 모든 쿼리에 대해 작업을 지정하도록 선택하면 작업이 항상 수행됩니다. 기본 프레젠테이션 템플릿을 선택하는 경우 모든 쿼리에 대해 첫 번째 규칙이 실행되는 것이 가장 좋습니다. 이렇게 하면 들어오는 쿼리가 무엇이든지 사용할 최악의 시나리오 프레젠테이션 템플릿을 선택했는지 확인할 수 있습니다. 조건은 이전 규칙이 설정한 CGI 쿼리 매개 변수, 쿠키 또는 사용자 지정 변수 또는 시스템 변수를 기반으로 할 수 있습니다.

## 사전 검색 규칙 작업 {#section_3B8E19D287554C1C969F5B8D81226981}

조건이 일치하는 사전 검색 규칙 내의 모든 작업이 적용됩니다. 작업은 일반적으로 작업, 작업을 수행할 데이터 및 사용할 값으로 구성됩니다. 가장 간단한 작업은 쿼리가 검색 전 규칙의 조건과 일치할 때 사용할 프레젠테이션 템플릿을 지정하는 것입니다. 그런 다음 대상 템플릿을 프레젠테이션 템플릿의 이름으로 설정합니다. 템플릿의 검색 매개 변수에 대한 작업을 수행하여 주어진 템플릿에 사용되는 검색을 변경하는 데 보다 복잡한 작업을 사용할 수 있습니다. 템플릿의 검색 매개 변수에서 작업을 수행할 때는 프레젠테이션 템플릿 및 검색을 지정합니다.

## 일반 규칙 {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

템플릿의 검색 매개 변수에서 작업을 수행할 때 다음과 같은 두 개의 특수 값이 있습니다.*프레젠테이션 템플릿과 이름이 지정된 검색에 대해 각각 타깃팅된 및 *기본 사항. 이러한 값을 사용하여 현재 타깃팅된 템플릿의 기본 검색을 기반으로 규칙을 만들 수 있습니다. 이러한 구문을 사용하면 현재 타깃팅된 템플릿 또는 기본 검색을 호출할 필요가 없는 일반 규칙을 만들 수 있습니다. 분명히 이전 사전 검색 규칙은 현재 타깃팅된 템플릿이 무엇인지 정의합니다. 그렇지 않으면 초기 프레젠테이션 템플릿이 선택되므로 원치 않는 결과가 생성됩니다.

## 예 {#section_EA153A151987454EA44A4A6862466DF6}

사용자가 lang이라는 cgi 매개 변수를 전달하여 알려진 언어로 설정하면 기본 템플릿을 guided.tmpl로 설정합니다.

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## 우수 사례 {#section_31EBAE5E54174DEE8986CBB636746A98}

* 첫 번째 규칙은 모든 쿼리에 대한 기본 템플릿을 선택합니다.
* 쿼리의 데이터 마이닝은 쿼리 정리 규칙 내에서 수행됩니다. 사전 검색 처리에서 참조할 수 있습니다.
* 사전 검색 규칙에 도입된 새 사용자 지정 변수를 다른 사전 검색 규칙이 참조하기 전에 모든 쿼리에 대해 실행되는 사전 검색 규칙에 추가합니다.

## 새 사전 검색 규칙 {#task_182B95918462490D8BDA7F16A81CAC11} 추가

[!DNL Pre-Search Rules]을 사용하여 들어오는 쿼리를 기반으로 검색 결과를 표시하는 데 사용할 프레젠테이션 템플릿을 선택할 수 있습니다.

**새 사전 검색 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**&#x200B;을 클릭합니다.
1. [!DNL Pre-Search Rules] 페이지에서 **[!UICONTROL Add New Rule]**&#x200B;을 클릭합니다.
1. [!DNL Name] 필드에 새 쿼리 정리 규칙의 이름을 입력합니다.
1. [!DNL Add Pre-Search Rule] 페이지에서 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

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
      <td colname="col2"> <p>HTTP 쿠키. 쿠키 이름 및 값은 균일 리소스 식별자로 인코딩되어야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>사용자 지정 변수 </p> </td> 
      <td colname="col2"> <p>사용자 정의 변수. 사용자 정의 변수를 제한 없이 추가, 삭제 또는 설정할 수 있습니다. </p> <p>사전 검색 규칙 내에서 쿼리 정리 모듈에서 정의한 변수를 참조할 수 있습니다. </p> </td> 
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
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 </p> </td> 
      <td colname="col2"> <p>특정 패싯과 연관된 글로벌 컬렉션의 특수 CGI 매개 변수. 모든 CGI 매개 변수는 쿼리 정리 후 템플릿 내에서 이름이 지정된 각 검색에 복사됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>쿼리 매개 변수 </p> </td> 
      <td colname="col2"> <p>글로벌 컬렉션의 CGI 매개 변수. 이러한 매개 변수는 쿼리 정리 후 템플릿 내에서 이름이 지정된 각 검색에 복사됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>템플릿의 검색 매개 변수 </p> </td> 
      <td colname="col2"> <p>프레젠테이션 템플릿과 연관된 명명된 검색에 로컬인 CGI 매개 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>템플릿의 백엔드 매개 변수 </p> </td> 
      <td colname="col2"> <p>들어오는 쿼리 매개 변수는 검색을 수행하는 데 사용되는 백엔드 매개 변수로 최종 변환됩니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 백엔드 검색 CGI 매개 변수 </a>를 참조하십시오. </p> <p>백엔드 매개 변수가 탐색 요소에 표시되지 않습니다. 따라서 고객의 검색에 적용할 추가 매개 변수를 숨길 수 있습니다. 이 매개 변수는 프레젠테이션 템플릿 내의 특정 검색에 대해 로컬입니다. 백엔드 매개 변수에 대한 작업은 늦은 바인딩입니다.즉, 검색이 전송되기 직전에 적용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>타깃팅된 템플릿 </p> </td> 
      <td colname="col2"> <p>삭제할 수 없는 시스템 정의 사용자 지정 변수의 특수 인스턴스입니다. 이 변수에는 현재 타깃팅된 프레젠테이션 템플릿이 포함되어 있습니다. 사용자 지정 변수 "targeted_template"을 지정하여 이 변수를 읽거나 설정할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>등급 </p> </td> 
      <td colname="col2"> <p>검색에 사용할 등급 규칙을 지정할 수 있습니다. 이 옵션은 등급 필드 및 등급 규칙을 정의한 경우에만 나타납니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>스토어 </p> </td> 
      <td colname="col2"> <p>검색 엔진은 호스트 이름 또는 <span class="codeph"> gs_store </span> 쿼리 매개 변수를 기반으로 고객이 속한 스토어를 자동으로 감지하고 후자의 우선 순위가 높습니다. 매장 밖에서 조건을 만들 수 있습니다. 쿼리 청소에서만 작업을 사용하여 현재 스토어를 오버라이드할 수도 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>마지막 규칙 </p> </td> 
      <td colname="col2"> <p>이 확인란을 선택하면 검색 전 처리 모듈이 일치 규칙 작업 후 추가 규칙을 수행하지 않습니다. 이 작업은 이후 규칙이 일치하지만 이후 규칙을 실행하지 않도록 하는 작업을 설정한 경우에 유용합니다. </p> </td> 
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

## 사전 검색 규칙 편집 {#task_25F77050C5DA42B29DFD1C9718FB8C64}

[!DNL Pre-Search Rules] 페이지에 추가한 기존 사전 검색 규칙을 편집할 수 있습니다.

**사전 검색 규칙을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**&#x200B;을 클릭합니다.
1. [!DNL Pre-Search Rules] 페이지의 테이블의 **[!UICONTROL Actions]** 열에서 편집할 관련 규칙의 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Edit Pre-Search Rule] 페이지에서 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

   [새 사전 검색 규칙 추가](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 사전 검색 규칙 삭제 {#task_128B6A79CA6C451C991AEDAD58F51743}

더 이상 필요하거나 사용하지 않는 사전 검색 규칙을 삭제할 수 있습니다.

규칙을 삭제하면 나머지 규칙이 실행되는 순서가 자동으로 조정되어 삭제가 적용됩니다.

**사전 검색 규칙을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**&#x200B;을 클릭합니다.
1. [!DNL Pre-Search Rules] 페이지의 테이블의 **[!UICONTROL Actions]** 열에서 삭제할 연관된 규칙의 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. [!DNL Confirmation] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 사전 검색 규칙이 {#task_C18817276A3C459089C97448076365D1} 실행하는 순서 변경

프레젠테이션 템플릿에서 사전 검색 규칙을 실행하는 순서를 변경하려면 사전 검색 규칙을 다시 정렬할 수 있습니다.

사전 검색 규칙은 정의된 순서대로 실행됩니다. 규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. [!DNL Pre-Search Rules] 페이지의 테이블의 [순서] 열에 새 번호를 입력하여 규칙 순서를 변경합니다. 또한 규칙을 드래그 앤 드롭하여 실행 순서를 변경할 수도 있습니다.

**사전 검색 규칙이 실행되는 순서를 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**&#x200B;을 클릭합니다.
1. [!DNL Pre-Search Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL Order]** 열 헤더를 클릭하여 오름차순 또는 내림차순으로 규칙을 정렬합니다.
   * **[!UICONTROL Order]** 열의 사전 검색 규칙 이름 왼쪽에 있는 텍스트 필드에 규칙을 실행할 순서 번호를 입력합니다.
   * 테이블 행을 규칙 실행 위치로 드래그하여 놓습니다. 모든 주문 번호는 규칙이 실행되는 새 순서를 반영하도록 업데이트됩니다.

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

