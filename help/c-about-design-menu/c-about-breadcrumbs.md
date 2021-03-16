---
description: 탐색 표시는 웹 사이트에 추가할 수 있는 탐색 컨트롤입니다. 탐색 표시는 고객이 검색 결과 세트 내 위치에 대한 피드백을 제공합니다. 또한 이전 단계로 빠르게 돌아갈 수 있습니다.
solution: Target
subtopic: Navigation
title: 탐색 표시 정보
topic: 디자인,사이트 검색 및 상품 판매
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---


# 탐색 표시 정보{#about-breadcrumbs}

탐색 표시는 웹 사이트에 추가할 수 있는 탐색 컨트롤입니다. 탐색 표시는 고객이 검색 결과 세트 내 위치에 대한 피드백을 제공합니다. 또한 이전 단계로 빠르게 돌아갈 수 있습니다.

## 탐색 표시 사용 {#concept_FB8A943C594A4A1593B118141DA61F03}

탐색 표시는 결과 세트의 범위를 좁히기 위해 검색된 용어 및 선택한 후속 패싯을 추적합니다.

탐색 표시 설정을 사용하여 검색 프레젠테이션 레이어의 탐색 표시 컨트롤을 사용자 정의합니다. 프레젠테이션 레이어에 검색 결과 집합이 두 개 이상 있으면 탐색 표시 컨트롤은 페이지의 기본 검색에 사용됩니다.

탐색 표시를 편집하여 기본 동작, 최대 값 너비 및 값 확장명을 변경하고 쿼리 용어를 포함할지 여부를 선택할 수 있습니다.

## 새 탐색 표시 {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B} 추가

고객이 웹 사이트에서 있는 위치를 추적할 수 있도록 탐색 표시 막대를 추가할 수 있습니다.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>웹 사이트에서 볼 수 있도록 프레젠테이션 템플릿의 탐색 표시를 참조해야 합니다.

**새 탐색 표시를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**&#x200B;를 클릭합니다.
1. [!DNL Breadcrumbs] 페이지에서 **[!UICONTROL Add Breadcrumb]**&#x200B;을 클릭합니다.
1. [!DNL Add Breadcrumb] 페이지에서 원하는 옵션을 설정합니다.

   이러한 설정은 탐색 표시의 동작과 기본 표시 모두에 영향을 줍니다. 프레젠테이션 템플릿의 설정을 통해 이러한 설정 중 일부를 재정의할 수 있습니다.

   <!-- 
   
   r_breadcrumb_options.xml
    
    -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>탐색 표시 이름 </p> </td> 
      <td colname="col2"> <p>탐색 표시의 이름입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>동작 </p> </td> 
      <td colname="col2"> <p>다음 3가지 탐색 표시 비헤이비어 중 하나를 설정합니다. </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> 이동  </span> <p>goto는 클릭한 탐색 표시를 클릭한 후 모든 탐색 표시를 제거하고 해당 지점에서 새 검색을 시작합니다. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> 제거 </span> <p>고객이 클릭한 탐색 경로에서 삭제를 제거한 다음 새 검색을 시작합니다. 이 동작은 고객이 검색을 통해 드릴다운 단계를 실행 취소하도록 하려는 경우에 유용합니다. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> 드롭  </span> <p>드롭은 모든 탐색 표시를 제거합니다. </p> </li> 
      </ul> </p> <p> 예를 들어 탐색 경로가 1 &gt; 2 &gt; 3 &gt; 4라고 가정할 경우 고객이 "2"를 클릭하면 선택한 행동에 따라 다음 결과가 표시됩니다. </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">이동 - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">제거 - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> 드롭 - 전체 브레드크럼이 삭제되어 드릴다운 시작 전에 고객이 원하는 위치로 돌아갑니다. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최대 값 너비 </p> </td> 
      <td colname="col2"> <p>탐색 표시 트레일에서 각 값의 길이를 지정합니다. 설정을 문자 수로 지정합니다. </p> <p>예를 들어 6으로 설정하면 탐색 경로 길이가 공백을 포함하여 최대 6자까지 가능합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>값 확장 </p> </td> 
      <td colname="col2"> <p>탐색 경로가 잘릴 때 사용할 줄임표를 지정합니다. </p> <p>기본적으로 "..." (줄임표)가 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>쿼리 용어 포함 </p> </td> 
      <td colname="col2"> <p>탐색 경로에서 쿼리 용어의 존재를 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>사용자 정의 표시 사용 </p> </td> 
      <td colname="col2"> <p>URL의 <span class="codeph"> uX=[name]&amp;[name]=[value] </span> 매개 변수를 사용하여 탐색 표시에 사용자 정의 항목을 사용할 수 있도록 확인하십시오. 처리 규칙을 사용하여 이 매개 변수를 원하는 방식으로 처리할 수 있습니다. </p> <p>예를 들어 이 기능이 활성화되어 있고 <span class="codeph"> <span class="varname"> 카테고리 </span> </span> 및 <span class="codeph"> <span class="varname"> 종류 </span> </span> 종류 <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> <span class="codeph">이 있는 경우, 탐색 암호는 &lt;cruma9/&gt; 의류 &gt; 남성 &gt; </span>과 같이 표시됩니다. . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>사용자 정의 표시 이름 </p> </td> 
      <td colname="col2"> <p>사용자 정의 탐색 표시 항목의 가능한 모든 이름의 쉼표로 구분된 목록. </p> <p>이 옵션은 <span class="uicontrol"> 사용자 정의 표시 활성화 </span>를 선택한 경우에만 사용할 수 있습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) [!DNL Breadcrumbs] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 탐색 표시 편집 {#task_583481D9A23E4E0F97AEB18E72CBE13F}

추가한 탐색 표시의 설정을 편집할 수 있습니다.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>웹 사이트에서 볼 수 있도록 프레젠테이션 템플릿의 탐색 표시를 참조해야 합니다.

**탐색 표시를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**&#x200B;를 클릭합니다.
1. [!DNL Breadcrumbs] 페이지에서 탐색 표시 이름의 맨 오른쪽에 있는 **[!UICONTROL Edit]**&#x200B;을 클릭합니다.
1. [!DNL Edit Breadcrumb] 페이지에서 원하는 옵션을 설정합니다.

   [새 탐색 표시 추가](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) **[!UICONTROL Breadcrumb]** 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 탐색 표시 {#task_401C6E481A744284906E15A29E04F757} 삭제

추가한 탐색 표시를 삭제할 수 있습니다.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**탐색 표시를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**&#x200B;를 클릭합니다.
1. [!DNL Breadcrumbs] 페이지에서 탐색 표시 이름의 맨 오른쪽에 있는 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. [!DNL Confirmation] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

