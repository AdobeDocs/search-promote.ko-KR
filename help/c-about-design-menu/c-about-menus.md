---
description: 메뉴를 사용하여 프레젠테이션 레이어를 사용자 정의할 수 있습니다.
seo-description: 메뉴를 사용하여 프레젠테이션 레이어를 사용자 정의할 수 있습니다.
seo-title: 메뉴 정보
solution: Target
subtopic: Navigation
title: 메뉴 정보
topic: Design,Site search and merchandising
uuid: 011050cd-21b6-4150-9503-18fa3f771626
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 1%

---


# 메뉴 정보{#about-menus}

메뉴를 사용하여 프레젠테이션 레이어를 사용자 정의할 수 있습니다.

## 메뉴 사용 {#concept_68123CE5CF4447B59217B5D721424E32}

검색 내의 설정에 매핑되는 메뉴를 추가합니다. 메뉴 내의 각 항목은 메뉴의 설정 값을 지정합니다. 메뉴 레이블을 사용자 정의할 수도 있습니다.

프레젠테이션 템플릿에서 정의된 메뉴를 참조할 수 있습니다. 그런 다음 선택 컨트롤과 같이 원하는 HTML 구성 요소에 배치할 수 있습니다. 이 조합을 통해 사용자가 검색 결과를 사용자 정의할 수 있습니다. 지원되는 메뉴 유형은 다음과 같습니다.정렬, 카운트 및 탐색.

## 새 메뉴 {#task_EE171532D3AE477FAFE8C2F4077A6D73} 추가

검색 결과 내의 설정에 매핑되는 메뉴를 추가할 수 있습니다.

<!-- 

t_adding_a_new_menu.xml

 -->

>[!NOTE]
>
>프레젠테이션 템플릿이 웹 사이트에 표시되도록 하려면 해당 메뉴를 사용해야 합니다.

**새 메뉴를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**&#x200B;를 클릭합니다.
1. [!DNL Menus] 페이지에서 **[!UICONTROL Add New Menu]**&#x200B;을 클릭합니다.
1. [!DNL Add Menu] 페이지에서 원하는 옵션을 설정합니다.

   이러한 설정은 탐색 표시의 동작과 기본 표시 모두에 영향을 줍니다. 프레젠테이션 템플릿의 설정을 통해 이러한 설정 중 일부를 재정의할 수 있습니다.

   [메뉴 정보](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32)를 참조하십시오.

   <!-- 
   r_add_menu_options.xml
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
      <td colname="col1"> <p>메뉴 이름 </p> </td> 
      <td colname="col2"> <p>메뉴의 이름입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>메뉴 유형 </p> </td> 
      <td colname="col2"> <p>다음 3가지 메뉴 유형 중 하나를 설정합니다. </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
      <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> 정렬  </span> <p>정의된 메타데이터 유형별로 검색을 구성합니다. </p> <p>예를 들어 다음과 같은 메타데이터 유형을 사용하여 정렬 메뉴를 정의할 수 있습니다.연관성 3개 항목;가용성 코드와 같은 사용자 지정 메타데이터 필드;및 가격. 3개의 항목에는 각각 "관련성별 정렬", "가용성별 정렬" 및 "가격별 정렬" 레이블이 지정될 수 있습니다. 프레젠테이션 템플릿에 이 컨트롤을 포함하면 고객이 검색 결과를 정렬할 수 있습니다. </p> </li> 
      <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> 계수 </span> <p>표시할 검색 결과의 수를 정의합니다. 이 메뉴 유형은 cgi 매개 변수 <span class="varname"> sp_c </span>에 매핑됩니다. </p> <p><a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> 백엔드 검색 CGI 매개 변수 </a>를 참조하십시오. </p> </li> 
      <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> 탐색 </span> <p>메뉴 항목과 연결된 정적 URL 세트를 지정합니다. 일반적으로 탐색 메뉴는 검색 결과 페이지에 최상위 탐색 막대를 만드는 데 사용됩니다. </p> <p>예를 들어 여성, 남성, 남자, 여자 등 메뉴 항목이 다음과 같은 메뉴를 만들 수 있습니다. 
      <code>
        /?q1=womens;x1=gender 
      </code>, 
      <code>
        /?q1=mens;x1=gender 
      </code> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>머천다이징 </p> 
        <!--DONT' KNOW WHAT THIS DOES--> </td> 
      <td colname="col2"> <p>이 옵션은 <span class="uicontrol"> 정렬 메뉴 유형을 선택한 경우에만 사용할 수 있습니다.</span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>메뉴의 항목 수 </p> </td> 
      <td colname="col2"> <p>메뉴의 항목 수를 지정합니다. 이 설정을 변경하면 양식에서 필드가 추가되거나 삭제됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 항목 </p> </td> 
      <td colname="col2"> <p>기본적으로 표시되는 메뉴 항목을 선택할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>항목 값 </p> </td> 
      <td colname="col2"> <p>항목 값은 설정한 메뉴 유형에 따라 달라집니다. </p> 
        <ul id="ul_2F14E6AA673640578A2D5161FD9D13EF"> 
        <li id="li_5017EC6E4ACB4B8E99E0AA61CBAAFFAE"> 정렬 메뉴 유형 <p>메뉴에서 선택한 항목이 정렬해야 하는 항목을 식별합니다. 선택 항목은 정렬 가능한 메타데이터 필드로 채워집니다. </p> <p>단일 항목의 경우 3개의 메타데이터 필드별로 정렬할 수 있습니다. 정렬은 지정된 순서대로 수행됩니다. </p> </li> 
        <li id="li_CC6BAFBF969C4367A71B55F08E0758D1"> 카운트 메뉴 유형 <p>고객이 이 메뉴 항목을 선택할 때 반환할 결과 수를 지정할 수 있습니다. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>항목 레이블 </p> </td> 
      <td colname="col2"> <p>항목 레이블은 설정한 메뉴 유형에 따라 달라집니다. </p> 
        <ul id="ul_957BF01235F84748B5EB7062D6AEAC41"> 
        <li id="li_03FB2E2C96134A2B8E08154F87F0CD55"> 정렬 메뉴 유형 <p>고객이 메뉴에서 이 항목을 볼 때 확인할 사용자 지정 레이블을 식별합니다. </p> </li> 
        <li id="li_C9FE2BC46D9443FB85FEB837C7CA45E1"> 카운트 메뉴 유형 <p>이 메뉴 항목에 표시하려는 사용자 지정 레이블을 식별합니다. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) [!DNL Menus] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## {#task_0770DBFD0C7046169097FB6F771B9114} 메뉴 편집

추가한 모든 메뉴의 설정을 편집할 수 있습니다.

<!-- 

t_editing_a_menu.xml

 -->

>[!NOTE]
>
>프레젠테이션 템플릿이 웹 사이트에 표시되도록 하려면 해당 메뉴를 사용해야 합니다.

**메뉴를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**&#x200B;를 클릭합니다.
1. [!DNL Menus] 페이지에서 메뉴 이름의 맨 오른쪽에 있는 **[!UICONTROL Edit]**&#x200B;을 클릭합니다.
1. [!DNL Edit Menu] 페이지에서 원하는 옵션을 설정합니다.

   [새 메뉴 추가](../c-about-design-menu/c-about-menus.md#task_EE171532D3AE477FAFE8C2F4077A6D73) 아래의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Menus] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## {#task_645E212311A045CD8D9D906878165F47} 메뉴 삭제

추가한 모든 메뉴를 삭제할 수 있습니다.

<!-- 

t_deleting_a_menu.xml

 -->

**메뉴를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**&#x200B;를 클릭합니다.
1. [!DNL Menus] 페이지에서 메뉴 이름의 맨 오른쪽에 있는 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. [!DNL Confirmation] 대화 상자에서 **[!UICONTROL OK]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

