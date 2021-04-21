---
description: 비즈니스 규칙을 사용하여 검색을 상품화할 수 있습니다.
solution: Target
title: 비즈니스 규칙 정보
topic-legacy: Rules,Site search and merchandising
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
exl-id: 6a52e0f5-29c2-4a48-b996-d217eeb52011
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '3115'
ht-degree: 1%

---

# 비즈니스 규칙 정보{#about-business-rules}

비즈니스 규칙을 사용하여 검색을 상품화할 수 있습니다.

## 비즈니스 규칙 사용 {#concept_2A93D76216754D3D8412CDEA00BD26BD}

예를 들어 배너가 표시되는 시기 또는 결과가 나타나는 순서 및 순서를 구성할 수 있습니다. 패싯에서 항목의 위치와 주어진 검색에 사용되는 템플릿을 구성할 수도 있습니다. 규칙은 정의된 순서대로 실행됩니다.규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. 규칙을 드래그하여 놓아 순서를 변경하거나 규칙 순서 텍스트 상자에 새 번호를 입력하여 순서를 변경할 수 있습니다.

각 비즈니스 규칙은 트리거 및 작업으로 구성됩니다.

트리거는 규칙이 실행되는 시기를 정의합니다. 예를 들어 쿼리 용어가 &quot;mens&quot;인 경우 또는 결과가 대부분 모자를 사용하는 경우 트리거는 전체 트리거를 true로 설정하려면 모든 조건 또는 모두 true여야 하는 여러 조건으로 구성됩니다. 트리거 연산자를 변경하여 우선 순위를 지정할 수 있습니다.

작업은 트리거 조건이 충족될 때 발생하는 상황을 정의합니다. 예를 들어 배너를 설정하여 지정된 결과를 표시하거나 위치 1로 이동합니다. 규칙 표는 규칙에 대한 요약 정보를 보여줍니다. 규칙 이름을 클릭하여 열고 추가 정보를 볼 수 있습니다.

규칙 표에는 모든 비즈니스 규칙 목록이 표시됩니다. 기본적으로 이 표는 추가된 마지막 10개의 규칙을 내림차순으로 표시합니다. 테이블의 열 머리글을 클릭하여 오름차순 또는 내림차순으로 규칙을 정렬할 수 있습니다.

비즈니스 규칙은 다음 3개 주 중 하나를 가질 수 있습니다.승인, 일시 중단 또는 WIP(진행 중인 작업)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>비즈니스 규칙 상태 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>승인됨 </p> </td> 
   <td colname="col2"> <p>승인된 비즈니스 규칙은 라이브 환경과 스테이징 환경에서 실행됩니다. 고급 규칙 빌더에서 비즈니스 규칙을 승인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일시 중단됨 </p> </td> 
   <td colname="col2"> <p>일시 중단된 비즈니스 규칙은 스테이지 환경 또는 라이브 환경에서 실행되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP(진행 중)는 승인되지 않았거나 일시 중지되지 않은 비즈니스 규칙입니다. 즉, 아직 작업 중이거나 승인을 하기 전에 먼저 테스트할 수 있습니다. WIP 상태의 비즈니스 규칙은 단계 환경에서만 실행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

비즈니스 규칙을 승인하고 라이브 환경에서 실행할 수 있도록 규칙을 라이브로 푸시합니다. 현재 *모든* 규칙만 라이브로 푸시할 수 있습니다. 그러나 규칙 상태를 변경하여 규칙이 실행되고 라이브 환경에서 실행되지 않도록 제어할 수 있습니다.

기본적으로 관련 트리거가 충족될 때마다 규칙이 실행됩니다. 그러나 특정 날짜 및 시간 범위에 대해 규칙 실행을 선택적으로 예약할 수 있습니다.

또한 기본적으로 규칙은 모든 스토어에 대해 관련 트리거가 충족될 때마다 실행됩니다. 규칙이 특정 스토어에만 적용되도록 하려면 [스토어] 패널을 사용하여 규칙이 적용되는 하나 이상의 스토어를 선택할 수 있습니다.

## 새 비즈니스 규칙 {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7} 추가

[!DNL Visual Rule Builder] 또는 [!DNL Advanced Rule Builder]을 사용하여 고객의 검색 경험을 맞춤화하는 비즈니스 규칙을 추가할 수 있습니다.

**새 비즈니스 규칙을 추가하려면**

다음 단계에서는 시각적 규칙 빌더를 사용한다고 가정합니다.

1. 다음 중 하나를 수행하십시오.

   * 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다. [!DNL Business Rules] 페이지에서 **[!UICONTROL Add New Rule]**&#x200B;을 클릭합니다.

   * 제품 메뉴에서 **[!UICONTROL Simulator]**&#x200B;을 클릭합니다. **[!UICONTROL Simulator for Today]** 페이지에서 **[!UICONTROL Options]** 드롭다운 메뉴의 오른쪽에 있는 **[!UICONTROL Add New Rule]**&#x200B;을 클릭합니다.

      페이지에 **[!UICONTROL Add New Rule]** 옵션이 표시되지 않으면 **[!UICONTROL Options]** 드롭다운 메뉴에서 **[!UICONTROL Simulate Staged]**&#x200B;를 클릭합니다.

      ![](assets/Simulator.png)

1. **[!UICONTROL Name]** 텍스트 필드에 비즈니스 규칙의 새 이름을 입력합니다.

   아직 **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭하지 마십시오.
1. (선택 사항) 많은 수의 비즈니스 규칙을 관리하는 경우 특정 레이블이 있는 비즈니스 규칙에 태그를 지정할 수 있습니다. **[!UICONTROL Tags]** 필드에 하나 이상의 태그 레이블, 쉼표 사용, Tab 또는 구분 기호로 Enter를 입력합니다.

   [!DNL Business Rules] 페이지에서 **[!UICONTROL Filter by tag]** 기능을 사용하여 지정된 레이블과 일치하는 규칙을 필터링합니다. 1. [!DNL Business Rule Builder] 페이지에서 사용할 트리거 및 작업을 설정합니다.

   **트리거 옵션**

   트리거는 비즈니스 규칙이 실행되려면 충족되어야 하는 조건입니다. 비즈니스 규칙에 여러 트리거가 있는 경우 다음 3가지 방법 중 하나를 사용하여 트리거가 응답하는 방식을 구성할 수 있습니다.

   * 다음 예제와 같이 모든 트리거가 true(기본 설정)여야 하는 응답입니다.

      `if a AND b AND c then ...`

   * 다음 예제와 같이 트리거가 true여야 하는 응답입니다.

      `if a OR b OR c then ...`

   * 사용자 정의 트리거 조합이 지정된 응답입니다. 즉, 개별 트리거 또는 &quot;조건&quot;을 `AND` 연산자 및 `OR` 연산자와 결합합니다.

      다음 예제와 같이 왼쪽 및 오른쪽 괄호 조합을 추가하여 평가 우선순위를 변경할 수도 있습니다.

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >`AND` 연산자를 사용자 지정 비즈니스 규칙 세트에 `OR` 연산자와 결합하는 경우, 괄호를 적절하게 지정하여 트리거가 올바른 순서로 평가되도록 하십시오.

      트리거의 조합을 사용자 정의할 수 있는 이 특정 기능은 기본적으로 활성화되지 않습니다. 이 기능을 사용하려면 기술 지원에 문의하십시오.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>트리거 옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>키워드 일치 </p> </td> 
      <td colname="col2"> <p>Trigger는 검색어가 지정된 대/소문자 구분 키워드와 일치할 때 true입니다. 트리거는 언어학 사전에 정의된 대로 키워드와 모든 동의어에 대해 모두 적용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 쿼리 일치 </p> </td> 
      <td colname="col2"> <p> 모든 검색 매개 변수가 일치하면 트리거가 true입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 결과 그룹이 지배적입니다. </p> </td> 
      <td colname="col2"> <p> 트리거는 주어진 검색에 의해 정의된 결과 그룹이 결과 집합을 지배할 때 true입니다. </p> <p>기본적으로 우위는 50%로 설정됩니다. 이 설정은 설정할 수 있는 머천다이징 기본 설정입니다. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>이 트리거를 true로 설정하려면 결과 집합 내에 전체 그룹이 있어야 합니다. 결과 그룹은 동적입니다. 색인 작업 후 원본 검색 기준과 일치하는 결과에 따라 변경할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과 그룹이 있음 </p> </td> 
      <td colname="col2"> <p> 트리거는 주어진 검색에 의해 정의된 결과 그룹이 결과 세트에 있을 때 true입니다. 이 트리거를 충족하려면 결과 집합 내에 전체 그룹이 있어야 합니다(결과가 모든 페이지에 나타날 수 있음). 결과 그룹은 동적이며 원래 검색 기준과 일치하는 결과에 따라 색인 작업 후에 변경될 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 결과 있음 </p> </td> 
      <td colname="col2"> <p> 결과 집합 내에서 개별 결과가 발견되면 트리거가 true입니다. 결과는 결과 세트의 아무 위치에나 있을 수 있으며 사용자가 현재 보고 있는 페이지에 있을 필요는 없습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **작업 옵션**

   비즈니스 규칙의 트리거가 충족되면 규칙과 연관된 작업이 수행됩니다. 시각적 규칙 빌더를 사용하면 다음 작업을 만들 수 있지만 고급 규칙 빌더를 사용하여 추가 작업 유형을 만들 수 있습니다.

   다음 표의 패싯 항목 제거, 패싯 항목 표시, 패싯 표시, 패싯 제거, 패싯 항목 푸시 작업에는 패싯이 필요합니다. 패싯을 선택하는 인터페이스는 계정 구성 방식에 따라 다릅니다. 예를 들어 일반적인 계정은 패싯을 선택하는 드롭다운 목록을 사용합니다. 그러나 계정에 패싯이 연결된 경우 패싯의 이름을 입력할 수 있는 자동 완성 텍스트 상자가 나타납니다. 패싯 이름을 입력할 때 자동 완성에서는 드롭다운 목록에 패싯을 제안합니다. 제안에는 현재 정의된 패싯이 포함됩니다. 계정에 슬롯 맵이 있는 경우 분할된 패싯을 제안하기도 합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>작업 옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>푸시 그룹 </p> </td> 
      <td colname="col2"> <p> 지정된 검색 조건에 정의된 검색 결과 그룹을 특정 위치로 푸시합니다. </p> <p>검색 결과 그룹을 푸시해도 그룹이 암시적으로 추가되지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>그룹 추가 </p> </td> 
      <td colname="col2"> <p> 지정된 검색 조건에 정의된 검색 결과 그룹을 추가합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>그룹 제거 </p> </td> 
      <td colname="col2"> <p> 지정된 검색 조건에 의해 정의된 검색 결과 그룹을 제거합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>단일 푸시 </p> </td> 
      <td colname="col2"> <p> 개별 검색 결과를 선택한 위치로 푸시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>단일 추가 </p> </td> 
      <td colname="col2"> <p> 선택한 위치에 개별 검색 결과를 추가합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>단일 제거 </p> </td> 
      <td colname="col2"> <p> 검색 결과 세트에서 개별 검색 결과를 제거합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>모든 결과 제거 </p> </td> 
      <td colname="col2"> <p>검색 결과 집합에서 모든 결과를 제거합니다. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다른 배너 선택 </p> </td> 
      <td colname="col2"> <p> 선택한 배너 영역의 배너를 변경합니다. </p> <p>이 옵션은 웹 페이지 보기 영역에서 배너를 마우스 오른쪽 단추로 클릭하면 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>배너 명령 추가 </p> </td> 
      <td colname="col2"> <p>Adobe Dynamic Media Classic 템플릿에만 적용됩니다. </p> <p>배너 템플릿에 사용되는 기본 매개 변수를 변경할 수 있습니다. </p> <p>Adobe Dynamic Media Classic </a>을(를) 사용하여 배너 추가의 옵션 표를 참조하십시오.<a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> </a></p> <p>Adobe Dynamic Media Classic </a>을(를) 사용하여 배너 편집을 참조하십시오.<a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> </a></p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>배너 제거 </p> </td> 
      <td colname="col2"> <p> 선택한 배너 영역에서 배너를 제거합니다.배너를 설정하는 다른 규칙이 없으면 배너가 표시되지 않습니다. </p> <p>이 옵션은 웹 페이지 보기 영역에서 배너를 마우스 오른쪽 단추로 클릭하면 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 항목 푸시 </p> </td> 
      <td colname="col2"> <p> 단면화 내의 항목을 선택한 위치로 푸시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>영역 제거 </p> </td> 
      <td colname="col2"> <p> 검색 결과 페이지에서 영역을 제거합니다. </p> <p>아래의 패싯 제거 작업을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>영역 표시 </p> </td> 
      <td colname="col2"> <p> 검색 결과 페이지에 영역을 표시합니다. </p> <p>아래 패싯 표시 작업을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 항목 제거 </p> </td> 
      <td colname="col2"> <p> 패싯에서 패싯 항목을 제거합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 항목 표시 </p> </td> 
      <td colname="col2"> <p> 특정 패싯 항목을 표시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 표시 </p> </td> 
      <td colname="col2"> <p> 특정 단면화를 표시합니다. 이 작업은 영역 표시 작업보다 선호됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 제거 </p> </td> 
      <td colname="col2"> <p> 특정 단면화를 제거합니다. 이 작업은 영역 제거 작업보다 선호됩니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   활성(제공)인 규칙 빌더 패널에 따라 다음을 수행하여 트리거 및 액션을 설정할 수도 있습니다.

   * **[!UICONTROL Triggers]** 패널이 열리면 - 비즈니스 규칙 빌더 페이지의 프레젠테이션 템플릿 영역에서 검색 결과 또는 검색 패싯을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add "result present" trigger]** 을 클릭합니다.

      트리거 패널에서 트리거의 왼쪽에 있는 &quot;X&quot;를 클릭하여 트리거 목록에서 제거합니다.

   * **[!UICONTROL Actions]** 패널이 열리면 - 비즈니스 규칙 빌더 페이지의 프레젠테이션 템플릿 영역에서 검색 결과를 마우스 오른쪽 단추로 클릭합니다. **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]** 또는 **[!UICONTROL Push to #`<n>`]**(여기서 `<n>`는 숫자임)을 클릭합니다.


1. (선택 사항) 비즈니스 규칙 빌더 패널( [!DNL Triggers], [!DNL Actions] 또는 [!DNL Schedule])에서 다음 중 하나를 수행합니다.

   * 비즈니스 규칙 빌더 페이지 영역의 프레젠테이션 템플릿 영역에서 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Select different banner]**&#x200B;을 클릭합니다. **[!UICONTROL Pick Banner]** 페이지에서 배너 축소판 아래 **[!UICONTROL Pick this banner]**&#x200B;를 클릭하여 프레젠테이션 템플릿에 추가합니다. 프레젠테이션 템플릿의 원래 배너의 크기 및 영역과 일치하는 배너만 선택할 수 있습니다.

      배너 추가 작업이 [!DNL Actions] 패널에 추가됩니다.

   * [!DNL Business Rule Builder] 페이지의 프레젠테이션 템플릿 영역에서 매개 변수를 변경할 Adobe Dynamic Media Classic 템플릿 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add banner commands]** 을 클릭합니다. [!DNL Change Parameters] 대화 상자에서 원하는 매개 변수 옵션을 설정합니다.

      Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)을(를) 사용하여 배너 추가의 옵션 표를 참조하십시오.[

      클릭 **[!UICONTROL Save]**.

      매개 변수 변경 사항이 [!DNL Actions] 패널에 추가됩니다.

      Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)을(를) 사용하여 배너 편집을 참조하십시오.[

   * 비즈니스 규칙 빌더 페이지의 프레젠테이션 템플릿 영역에서 페이지에서 삭제할 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Remove banner]**&#x200B;을 클릭합니다. 배너 제거 동작이 [액션] 패널에 추가됩니다.

1. (선택 사항) **[!UICONTROL Schedule]** 패널에서 다음 중 하나를 수행합니다.

   * 연결된 트리거가 충족될 때마다 규칙을 실행하려면 **[!UICONTROL Run Indefinitely]**&#x200B;을 클릭합니다. 이 옵션은 기본값입니다.
   * **[!UICONTROL Fixed Schedule]**&#x200B;을 클릭한 다음 연관된 트리거가 충족될 때마다 규칙이 실행할 시작 날짜와 시간, 종료 날짜 및 시간을 지정합니다.

1. 클릭 **[!UICONTROL Save Rule]**.
1. (선택 사항) [!DNL Business Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙 편집 {#task_375CFA75D1D94D9E92A35DE1228E5087}

시각적 규칙 빌더 또는 고급 규칙 빌더를 사용하여 추가한 비즈니스 규칙을 편집할 수 있습니다.

**새 비즈니스 규칙을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. [!DNL Business Rules] 페이지에서 다음 중 하나를 수행합니다.

   * [!DNL Name] 열에서 변경할 비즈니스 규칙의 이름을 클릭합니다.

      비즈니스 규칙은 **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]**&#x200B;에 지정된 기본 인터페이스에서 열립니다.

   * 편집할 비즈니스 규칙 이름 옆의 드롭다운 목록에서 **[!UICONTROL Edit in advanced mode]** 또는 **[!UICONTROL Edit in visual mode]**&#x200B;을 클릭합니다.

1. [!DNL Name] 텍스트 필드에 비즈니스 규칙의 새 이름을 입력합니다.

   아직 **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭하지 마십시오. 1. [!DNL Business Rule Builder] 페이지에서 사용할 트리거 및 작업을 설정합니다.

   [새 비즈니스 규칙 추가](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7) 아래의 옵션 표를 참조하십시오.
1. (선택 사항) **[!UICONTROL Business Rule Builder]** 패널( [!DNL Triggers], [!DNL Actions] 또는 [!DNL Schedule]에서 다음 중 하나를 수행합니다.

   * [!DNL Business Rule Builder] 페이지의 프레젠테이션 템플릿 영역에서 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Select different banner]** 을 클릭합니다. [!DNL Pick Banner page]에서 배너 축소판 아래의 **[!UICONTROL Pick this banner]**&#x200B;을 클릭하여 프레젠테이션 템플릿에 추가합니다. 프레젠테이션 템플릿의 원래 배너의 크기 및 영역과 일치하는 배너만 선택할 수 있습니다.

      배너 추가 작업이 [!DNL Actions] 패널에 추가됩니다.

   * [!DNL Business Rule Builder] 페이지의 프레젠테이션 템플릿 영역에서 매개 변수를 변경할 Adobe Dynamic Media Classic 템플릿 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add banner commands]** 을 클릭합니다. [!DNL Change Parameters] 대화 상자에서 원하는 매개 변수 옵션을 설정합니다.

      Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3)을(를) 사용하여 배너 추가의 옵션 표를 참조하십시오.[

      클릭 **[!UICONTROL Save]**.

      매개 변수 변경 사항이 [!DNL Actions] 패널에 추가됩니다.

      Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9)을(를) 사용하여 배너 편집을 참조하십시오.[

   * [!DNL Business Rule Builder] 페이지의 프레젠테이션 템플릿 영역에서 페이지에서 삭제할 배너를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Remove banner]** 을 클릭합니다. 배너 제거 동작이 [!DNL Actions] 패널에 추가됩니다.

1. (선택 사항) [!DNL Schedule] 패널에서 다음 중 하나를 수행합니다.

   * 연결된 트리거가 충족될 때마다 규칙을 실행하려면 **[!UICONTROL Run Indefinitely]**&#x200B;을 클릭합니다. 이 옵션은 기본값입니다.
   * **[!UICONTROL Fixed Schedule]**&#x200B;을 클릭한 다음 연관된 트리거가 충족될 때마다 규칙이 실행할 시작 날짜와 시간, 종료 날짜 및 시간을 지정합니다.

1. 클릭 **[!UICONTROL Save Rule]**.

   [!DNL Business Rule Builder] 페이지가 닫히고 **[!UICONTROL Business Rule]** 페이지로 돌아갑니다. 규칙이 표에 나타납니다. **[!UICONTROL Modified]** 열 헤더를 클릭하여 편집 날짜별로 규칙을 정렬합니다. 1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙 복사 중 {#task_89F1879C71A54EE9B7454439302C03EC}

생성할 새 비즈니스 규칙의 기초로 사용할 기존 비즈니스 규칙을 복사할 수 있습니다.

**비즈니스 규칙을 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. 복사하려는 비즈니스 규칙 이름 옆의 **[!UICONTROL Business Rules]** 페이지의 드롭다운 목록에서 **[!UICONTROL Copy rule]**&#x200B;을 클릭합니다.
1. 복사한 비즈니스 규칙을 평소대로 편집합니다.

   [비즈니스 규칙 편집](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)을 참조하십시오.

## 비즈니스 규칙 승인 중 {#task_BD569D18BF664272B8692294C162E2C1}

WIP(진행 중) 또는 일시 중단된 업무 규칙을 활성화할 수 있습니다.

**비즈니스 규칙을 승인하려면**

1. 제품 메뉴에서 **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. [!DNL Business Rules] 페이지의 비즈니스 규칙 테이블의 [!DNL Status] 열에 있는 상태 열 헤더를 사용하여 **[!UICONTROL WIP]** 또는 **[!UICONTROL suspended]** 상태인 규칙을 정렬합니다.

   표의 왼쪽에 있는 확인란 열 헤더를 사용하여 현재 페이지에 표시된 모든 규칙을 확인하거나 **[!UICONTROL WIP]** 또는 **[!UICONTROL suspended]** 상태인 규칙만 확인합니다. 1. 페이지 위쪽 근처의 메뉴 모음에서 **[!UICONTROL Approve]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Confirm Action]** 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙 일시 중단 {#task_364E1FFB905141C08E306C8F1794A20E}

WIP(진행 중인 작업) 또는 승인된 상태를 가진 비즈니스 규칙을 일시 중단할 수 있습니다.

규칙을 일시 중단하면 사용자 인터페이스에 일시적으로 비활성화한 규칙을 표시하고 다른 시간 동안 해당 규칙에 대한 작업을 유예하는 것입니다. 그러나 일시 중단된 규칙을 계속 편집할 수는 있습니다.

**비즈니스 규칙을 일시 중단하려면**

1. 제품 메뉴에서 **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. [!DNL Business Rules] 페이지의 비즈니스 규칙 테이블의 상태 열에 있는 상태를 사용하여 테이블의 맨 왼쪽 열에서 **[!UICONTROL WIP]** 또는 **[!UICONTROL approved]** 상태인 규칙을 확인합니다.
1. 페이지 위쪽 근처의 메뉴 모음에서 **[!UICONTROL Suspend]**&#x200B;을 클릭합니다.
1. **[!UICONTROL Confirm Action]** 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙 다시 시작 {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

일시 중단된 규칙을 다시 활성화하려면 비즈니스 규칙을 다시 시작할 수 있습니다. 비즈니스 규칙을 재개하면 해당 상태가 WIP(진행 중인 작업)로 설정됩니다.

**비즈니스 규칙을 재개하려면**

1. 제품 메뉴에서 **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. [!DNL Business Rules] 페이지의 비즈니스 규칙 테이블의 상태 열에 있는 상태를 사용하여 테이블의 맨 왼쪽 열에서 **[!UICONTROL suspended]** 상태인 규칙을 확인합니다.
1. 페이지 위쪽 근처의 메뉴 모음에서 **[!UICONTROL Resume]**&#x200B;을 클릭합니다.
1. [!DNL Confirm Action] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙이 실행하는 순서 변경 {#task_FE3B1C17307F49B49050C2EC5A063991}

프레젠테이션 템플릿에서 비즈니스 규칙이 실행되는 순서를 변경할 수 있습니다.

비즈니스 규칙은 정의된 순서대로 실행됩니다.규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. [!DNL Business Rules] 페이지의 테이블의 [순서] 열에 새 번호를 입력하여 규칙 순서를 변경합니다. 또한 규칙을 드래그 앤 드롭하여 실행 순서를 변경할 수도 있습니다.

**비즈니스 규칙이 실행되는 순서를 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. 표의 [!DNL Business Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL Order]** 열 헤더를 클릭하여 오름차순 또는 내림차순으로 규칙을 정렬합니다.
   * **[!UICONTROL Order]** 열의 비즈니스 규칙 이름의 왼쪽에 있는 텍스트 필드에 규칙을 실행할 순서 번호를 입력합니다.
   * 테이블 행을 규칙 실행 위치로 드래그하여 놓습니다. 모든 주문 번호는 규칙이 실행되는 새 순서를 반영하도록 업데이트됩니다.

1. 클릭 **[!UICONTROL Save Changes]**.

   이제 비즈니스 규칙이 지정한 순서대로 실행됩니다. 리디렉션 비즈니스 규칙이 지정된 경우는 예외입니다. 리디렉션 비즈니스 규칙이 트리거되거나 히트되면 비즈니스 규칙 처리가 리디렉션을 허용하도록 중지됩니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 비즈니스 규칙 삭제 중 {#task_AE37B42412044541BCC6D46CF8793DFF}

일괄 작업 드롭다운 메뉴를 사용하여 상태가 WIP, 일시 중지 또는 승인인 비즈니스 규칙을 삭제할 수 있습니다.

**비즈니스 규칙을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**&#x200B;을 클릭합니다.
1. [!DNL Business Rules] 페이지에서 다음 중 하나를 수행합니다.

   * 확인란 열 헤더를 사용하여 현재 페이지에 표시된 모든 규칙을 확인합니다.
   * 테이블의 상태 열의 상태를 기준으로 삭제할 비즈니스 규칙만 확인합니다.

1. [!DNL Bulk Actions] 드롭다운 목록에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. [!DNL Confirm Action] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.
