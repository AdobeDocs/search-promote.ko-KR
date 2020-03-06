---
description: 사후 검색 규칙을 사용하여 검색 결과를 검토하고 검색 결과가 표시된 컨텐트에 미치는 영향을 결정할 수 있습니다.
seo-description: 사후 검색 규칙을 사용하여 검색 결과를 검토하고 검색 결과가 표시된 컨텐트에 미치는 영향을 결정할 수 있습니다.
seo-title: 사후 검색 규칙 정보
solution: Target
title: 사후 검색 규칙 정보
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# 사후 검색 규칙 정보{#about-post-search-rules}

사후 검색 규칙을 사용하여 검색 결과를 검토하고 검색 결과가 표시된 컨텐트에 미치는 영향을 결정할 수 있습니다.

## 사후 검색 규칙 사용 {#concept_AF6ADFCC0ADF4A788003964939917FDE}

검색에 결과가 없는 경우 게시물 검색 규칙은 유사한 항목을 검색할 수 있습니다. 또는 찾을 수 없는 항목을 검색하는 고객에게 다른 항목을 추천하는 웹 페이지를 표시할 수 있습니다.

각 사후 검색 규칙은 다음 두 가지 주요 요소로 구성됩니다.규칙의 작업 및 선택적 조건. 규칙 및 조건 수를 제한 없이 지정할 수 있습니다. 규칙 세트는 규칙별로 반복되므로 이러한 규칙의 순서가 중요합니다. 규칙의 조건이 일치하면 관련된 모든 작업이 수행됩니다.

최대 3라운드의 검색을 위해 검색 결과 집합을 세분화할 수 있습니다. 이후에는 현재 사용 가능한 모든 것이 사용됩니다. 이 제한은 무한 루프를 방지하고 고객이 효율적인 응답을 받을 수 있도록 합니다. 검색을 다시 실행하는 시간이 많을수록 검색 결과를 반환하는 데 시간이 오래 걸립니다. 일치하는 규칙 중 하나가 현재 사용된 프레젠테이션 템플릿의 검색 중 하나를 변경하거나 템플릿을 전환하지 않으면 검색 결과 집합이 종결된 것으로 간주되고 이후 검색 종료 화면이 나타납니다.

검색 후 처리는 이전 처리 모듈 쿼리 정리 및 사전 검색 처리를 기반으로 구축됩니다. 따라서 이러한 모듈에 설정된 모든 사용자 지정 변수를 사후 검색 처리 규칙에 사용할 수 있습니다. 마찬가지로, 사전 검색 처리에서는 프레젠테이션 템플릿과 연결된 각 명명된 검색에 자체 CGI 매개 변수의 로컬 복사본이 있는 모든 템플릿을 인스턴스화했습니다. 각 검색을 개별적으로 사용자 정의할 수 있습니다.

쿼리 [정리 규칙 정보를 참조하십시오](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

## 사후 검색 규칙 조건 정보 {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

조건은 선택 사항입니다. 모든 쿼리에 대해 작업이 지정되도록 지정하면 작업이 항상 수행됩니다. 이전 규칙이 설정한 모든 CGI 쿼리 매개 변수, 쿠키, 검색 결과 또는 사용자 지정 변수를 기반으로 조건을 설정할 수 있습니다. 또는 현재 선택한 템플릿이 무엇인지에 대한 시스템 조건 또는 마지막 검색인지 기반으로 할 수 있습니다. 검색 결과 또는 CGI 매개 변수에 대한 조건을 작성할 때 템플릿과 검색 이름을 지정합니다.

## 사후 검색 규칙 작업 정보 {#section_0E15FE683A894ECAAA386267EEC7F7C5}

일치하는 조건이 있는 사후 검색 규칙의 모든 작업이 적용됩니다. 작업은 일반적으로 작업, 작업을 수행할 데이터 및 사용할 값으로 구성됩니다. 가장 간단한 작업은 게시물 검색 규칙의 조건에 따라 사용할 프레젠테이션 템플릿을 전환하는 것입니다. 더 많은 고급 작업을 사용하여 검색을 다시 수행하면 검색의 매개 변수를 변경할 수 있습니다. 템플릿의 검색 매개 변수에 대한 작업을 수행할 때 프레젠테이션 템플릿 및 검색을 지정합니다.

## 일반 규칙 {#section_AEE923988CC748FF9DEF2233FBF333B5}

템플릿의 검색 매개 변수에 대한 작업을 수행할 때 프레젠테이션 템플릿과 명명된 검색에 대해 각각 두 개의 특수 값, *타깃팅된 값 및 *primary가 있습니다. 이 값을 사용하여 현재 타깃팅된 템플릿의 기본 검색을 기반으로 규칙을 만듭니다. 이러한 구문을 사용하면 현재 타깃팅된 템플릿 또는 기본 검색을 호출할 필요가 없는 일반 규칙을 만들 수 있습니다. 이 과정이 검색 후 처리를 통한 첫 번째 과정인 경우 타깃팅된 템플릿은 검색 전 처리 과정에서 설정되는 모든 것입니다.

## 리디렉션 {#section_E5669A2F13C240F2968E31C75591CD6A}

쿼리 정리 내의 직접 히트 및 리디렉션을 사용하면 들어오는 검색 용어를 기반으로 URL로 리디렉션할 수 있습니다. 후행 검색 규칙 내의 리디렉션은 리디렉션을 수행할지 여부를 결정하기 전에 검색에서 반환된 결과 수를 확인할 수 있다는 점을 제외하고 이 아이디어를 확장합니다. 사후 검색 규칙을 사용하여 사용자 지정 변수 또는 쿼리 매개 변수로 대체할 수 있는 URL로 리디렉션할 수 있습니다. 또는 첫 번째 결과 내의 필드로 리디렉션할 수 있습니다. 결과 필드로 리디렉션할 때 전송 템플릿에서 필드를 정의하며 유효한 명시적 URL이 포함되어야 합니다. 그렇지 않으면 리디렉션을 건너뜁니다.

사후 검색 규칙 내에서 리디렉션 메커니즘을 사용하는 경우 검색에서 단일 결과를 반환하는 시기를 감지할 수 있습니다. 이러한 결과를 반환하는 대신 결과와 연결된 웹 페이지로 리디렉션할 수 있습니다.

게시물 검색 규칙과 함께 리디렉션을 사용하는 예는 아래 리디렉션 예제를 참조하십시오.

## 마지막 규칙 {#section_FC1E0050C9324278B171038E98F6C335}

옵션 **[!UICONTROL Last Rule]** 세트가 있는 규칙에 대한 조건이 충족되면, 사후 검색 처리 모듈은 일치 규칙의 작업 후에 추가 규칙을 수행하지 않습니다. 이 상황은 이후 규칙이 일치하지만 처리가 중지되도록 하는 작업을 설정한 경우에 유용합니다. 그리고 다음 검색 단계 후에 나중에 규칙이 잠재적으로 일치할 수 있도록 합니다.

## 예 {#section_DDB98383690941F9B44AD00FBA55BB56}

다음 예제에서는 두 개의 프레젠테이션 템플릿이 있다고 가정합니다. 한 템플릿은 여러 검색 결과를 표시하는 데 사용되며 다른 템플릿은 단일 결과 및 기본 검색과 관련된 액세서빌러티를 추가로 검색하는 데 사용됩니다. 결과가 하나뿐인 경우 이를 감지하여 다른 프레젠테이션 템플릿으로 전환해야 합니다. 이 작업을 수행하려면 다음 규칙을 사용할 수 있습니다.

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

메가일렉트로닉스는 대형 전자 매장이다. MegaElectronic은 검색 데이터를 분석한 후 많은 고객이 제품의 부품 번호를 사용하여 제품 검색을 수행한다는 것을 알립니다. 이러한 경우 MegaElectronic은 고객이 직접 검색한 웹 페이지에서 단일 제품만 찾은 경우 제품과 연결된 웹 페이지로 리디렉션하려고 합니다.

이 결과를 얻으려면 세 가지 조건이 있는 단일 규칙을 사용할 수 있습니다. 첫 번째 조건은 반환된 검색에 단일 결과만 있는지 확인합니다. 두 번째 조건에서는 쿼리 용어가 리디렉션을 발생시킬 결과에 대해 MegaElectronic의 부품 번호 형식과 일치하는지 확인합니다. 세 번째 조건에서는 부품 번호가 부분 부품 번호일 수 있고 두 개 이상의 결과를 반환할 수 있으므로 고객이 패싯을 사용하여 하나의 결과로 드릴다운하지 않도록 합니다. 작업이 결과 내의 필드로 리디렉션됩니다.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## 우수 사례 {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* 새 검색 라운드를 트리거하는 모든 규칙 집합에는 항상 조건부 절이 있어야 합니다. 이미 최대 검색 수를 수행한 경우 검색을 다시 실행할 수 없습니다.
* 모듈을 마지막으로 통과했지만 결과가 여전히 좋지 않은 경우 &quot;결과 없음&quot; 템플릿으로 전환할 수 있습니다.
* 다른 매개 변수가 있을 수 있는 검색 결과에 따라 프레젠테이션 템플릿을 변경해야 합니다. 들어오는 쿼리만을 기반으로 하는 템플릿을 선택하려면 사전 검색 규칙이 더 효율적입니다.
* 쿼리의 데이터 마이닝은 쿼리 정리 모듈에서 수행됩니다. 사후 검색 처리에서 사용자 지정 변수를 참조할 수 있습니다.
* 리디렉션을 수행할 때는 항상 고객이 패싯을 선택하지 않았는지 확인합니다. 고객이 패싯을 들이대고 갑자기 검색 결과에서 빠져나가면 불편하기 때문입니다. 고객은 단일 결과가 원하지 않는 경우 패싯을 선택 해제할 수 있습니다.

## 새 검색 후 규칙 추가 {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

을 [!DNL Post-Search Rules] 사용하여 들어오는 쿼리를 기반으로 검색 결과를 표시하는 데 사용할 프레젠테이션 템플릿을 선택할 수 있습니다.

**새 검색 후 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Post-Search Rules] 을 클릭합니다 **[!UICONTROL Add New Rule]**.
1. 필드에 [!DNL Name] 새 쿼리 정리 규칙의 이름을 입력합니다.
1. 페이지에서 [!DNL Add Post-Search Rule] 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

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
      <td colname="col2"> <p>HTTP 쿠키 쿠키 이름 및 값은 Uniform Resource Identifier로 인코딩되어야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>사용자 지정 변수 </p> </td> 
      <td colname="col2"> <p>사용자 정의 변수. 사용자 지정 변수를 제한 없이 추가, 삭제 또는 설정할 수 있습니다. </p> <p>쿼리 정리 및 검색 전 규칙 모듈에서 검색 후 규칙 내에서 정의한 사용자 지정 변수를 참조할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시스템 변수 </p> </td> 
      <td colname="col2"> <p>확인할 수 있는 내부 시스템에 의해 설정된 읽기 전용 변수. 지원되는 시스템 변수는 다음과 같습니다. </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname </span> <p>서버 호스트의 이름입니다. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>쿼리 문자열이 없는 요청된 Uniform 리소스 식별자입니다. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>전체 쿼리 문자열. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> 환경 </span> <p>들어오는 쿼리가 스테이징 환경이나 라이브 환경으로 전송되었는지 여부에 따라 "스테이지" 또는 "라이브"가 됩니다. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>고객이 가져온 Uniform Resource Locator. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시스템 변수 </p> </td> 
      <td colname="col2"> <p>현재 상태를 결정하기 위해 조건에 사용할 수 있는 읽기 전용 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>템플릿의 검색 패싯 </p> </td> 
      <td colname="col2"> <p>프레젠테이션 템플릿과 연결된 명명된 검색에 로컬에 있는 패싯 패싯은 기본적으로 고객이 선택한 패싯 내의 값을 나타내는 데 사용되는 특수 CGI 매개 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>템플릿의 검색 매개 변수 </p> </td> 
      <td colname="col2"> <p>프레젠테이션 템플릿과 연결된 명명된 검색에 로컬로 사용되는 CGI 매개 변수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>템플릿의 백엔드 매개 변수 </p> </td> 
      <td colname="col2"> <p>들어오는 쿼리 매개 변수는 검색을 수행하는 데 사용되는 백엔드 매개 변수로 변환됩니다. </p> <p>백엔드 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 검색 CGI 매개 변수를 참조하십시오 </a>. </p> <p>백엔드 매개 변수가 탐색 요소에 표시되지 않습니다. 따라서 고객의 검색에 적용할 추가 매개 변수를 숨길 수 있습니다. </p> <p>매개 변수는 프레젠테이션 템플릿 내의 특정 검색에 로컬로 사용됩니다. 백엔드 매개 변수에 대한 작업은 지연 바인딩입니다.즉, 검색이 전송되기 직전에 적용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>타깃팅된 템플릿 </p> </td> 
      <td colname="col2"> <p>삭제할 수 없는 시스템 정의 사용자 지정 변수의 특수 인스턴스입니다. 이 변수에는 현재 타깃팅된 프레젠테이션 템플릿이 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>등급 </p> </td> 
      <td colname="col2"> <p>검색에 사용할 등급 규칙을 지정할 수 있습니다. 이 옵션은 등급 필드 및 등급 규칙을 정의한 경우에만 나타납니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>마지막 규칙 </p> </td> 
      <td colname="col2"> <p>이 확인란을 선택하면 검색 후 처리 모듈이 일치 규칙 작업 후 추가 규칙을 수행하지 않습니다. 이 작업은 이후 규칙이 일치하지만 이후 규칙이 실행되지 않게 하는 작업을 설정한 경우에 유용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>일시 중단 </p> </td> 
      <td colname="col2"> <p>규칙 실행을 해제하지만 규칙을 삭제하지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 사후 검색 규칙 편집 {#task_ECB00334C0A74C87AF857DB3EB372119}

페이지에 추가한 기존 사후 검색 규칙을 편집할 수 [!DNL Post-Search Rules] 있습니다.

**사후 검색 규칙을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Post-Search Rules] 테이블 **[!UICONTROL Actions]** 열 아래에서 편집할 연결된 규칙을 **[!UICONTROL Edit]** 클릭합니다.
1. 페이지에서 [!DNL Edit Post-Search Rule] 드롭다운 목록과 텍스트 필드를 사용하여 쿼리를 작성합니다.

   새 사후 검색 규칙 [추가의 옵션 표를](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9)참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 사후 검색 규칙 삭제 {#task_0F4653AB20D54B769A4FA8D1491AB4CF}

더 이상 필요하거나 사용하지 않는 검색 후 규칙을 삭제할 수 있습니다.

규칙을 삭제하면 나머지 규칙 실행 순서가 자동으로 조정되어 삭제 고려됩니다.

**사후 검색 규칙을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Post-Search Rules] 테이블 **[!UICONTROL Actions]** 열 아래에서 삭제할 연결된 규칙을 **[!UICONTROL Delete]** 클릭합니다.
1. 대화 [!DNL Confirmation] 상자에서 을 클릭합니다 **[!UICONTROL OK]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 사후 검색 규칙 실행 순서 변경 {#task_40542FCD32234BBF881A81BF5477F78F}

게시물 검색 규칙의 순서를 변경하여 프레젠테이션 템플릿에서 규칙 실행 순서를 변경할 수 있습니다.

사후 검색 규칙은 정의된 순서대로 실행됩니다. 규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. 페이지의 테이블의 순서 열에 새 번호를 입력하여 규칙 순서를 [!DNL Post-Search Rules] 변경합니다. 또한 드래그 앤 드롭 방식으로 규칙을 사용하여 실행 순서를 변경할 수 있습니다.

**사후 검색 규칙이 실행되는 순서를 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Post-Search Rules] 다음 중 하나를 수행합니다.

   * 열 머리글을 클릭하여 규칙을 오름차순 또는 내림차순으로 정렬합니다. **[!UICONTROL Order]**
   * 사전 검색 규칙 이름의 왼쪽에 있는 [!DNL Order] 열의 텍스트 필드에 규칙을 실행할 순서 번호를 입력합니다.
   * 테이블 행을 규칙 실행 위치로 드래그하여 놓습니다. 모든 주문 번호는 규칙이 실행되는 새 순서를 반영하도록 업데이트됩니다.

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.
