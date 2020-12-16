---
description: 사용자 메뉴를 사용하여 사용자를 보고 추가하고, 역할을 보고 추가하거나, 역할 멤버십을 변경할 수 있습니다. [사용자] 메뉴에서 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.
seo-description: 사용자 메뉴를 사용하여 사용자를 보고 추가하고, 역할을 보고 추가하거나, 역할 멤버십을 변경할 수 있습니다. [사용자] 메뉴에서 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.
seo-title: 사용자 메뉴 정보
solution: Target
subtopic: Users
title: 사용자 메뉴 정보
topic: Settings,Site search and merchandising
uuid: 6242b73c-5e8a-44b7-9942-0684530940bc
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1487'
ht-degree: 0%

---


# 사용자 메뉴 {#about-the-users-menu} 정보

사용자 메뉴를 사용하여 사용자를 보고 추가하고, 역할을 보고 추가하거나, 역할 멤버십을 변경할 수 있습니다. [사용자] 메뉴에서 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

## 계정 사용자 {#task_FDDF30EE23C548DF8CFBB2FB2605303C} 보기

[!DNL View Users] 페이지를 사용하여 모든 기존 계정 사용자를 볼 수 있습니다. 계정 사용자를 제거할 수도 있습니다(계정 소유자 제외).

**[!UICONTROL User Admin]**&#x200B;이(가) 선택된 계정 사용자만 사용자를 제거하거나 사용자 역할을 수정할 수 있습니다.

계정 소유자를 제거하려면 먼저 계정 소유권을 다른 사용자에게 양도해야 합니다.

소유권을 이전하면 다른 사용자와 마찬가지로 계정을 제거할 수 있습니다. 제거된 사용자는 상태 변경을 알리는 전자 메일을 받습니다.

[다른 계정 사용자](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17)에게 계정 소유권 이전을 참조하십시오.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**계정 사용자를 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL View Users]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL User Admin] 열 머리글 아래에서 계정 사용자를 제거하거나 계정 사용자 역할을 편집할 수 있는 기능을 제공할 계정 사용자를 선택합니다.
1. (선택 사항) [!DNL Remove?] 열 머리글 아래에서 제거할 계정 사용자를 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL View Users] 페이지에서 하이퍼링크된 역할 이름을 클릭합니다. 사용자를 역할에 할당하거나 역할에서 사용자 할당을 취소할 수 있는 [!DNL Role Membership] 페이지가 열립니다.

   [역할 구성원 자격 구성](../c-about-settings-menu/c-about-users-menu.md#task_DAC596AAFFCE4EF0BE68CEEF7E365414)을 참조하십시오.

## 계정 사용자 추가 중 {#task_176C463A0C0849B29245C28EC9876326}

[!DNL Add Users] 페이지를 사용하여 사이트 검색/머천다이징에 새 계정 사용자를 추가할 수 있습니다.

새 사용자의 전자 메일 주소만 필요합니다. 새 사용자가 계정에 추가되면 새 사용자에게 계정 정보가 전송됩니다.

기본적으로 새 사용자는 사용자 관리자로 할당되지 않습니다. 사용자 관리자는 역할을 정의 및 편집하고 다른 사용자를 제거할 수 있습니다. 새 사용자를 [!DNL Add Users] 페이지에서 사용자 관리자로 선택할 수 있습니다. 또는 [사용자 보기] 페이지를 사용하여 새 사용자를 사용자 관리자로 만들 수 있습니다.

[계정 사용자 보기](../c-about-settings-menu/c-about-users-menu.md#task_FDDF30EE23C548DF8CFBB2FB2605303C)를 참조하십시오.

지정한 전자 메일 주소에는 ASCII 문자만 포함되어야 합니다. 표준 알파벳순 사용(a...z) 사용자 이름을 도메인과 구분하는 데 사용되는 문자가 정확히 하나의 `@`인 문자 또는 숫자(0..9)입니다. `_`, `+`, `-`, `.`, `!`, `#`, `'`, `%`, `&`, `*`, `=`, `?`, `^`, &lt;a13/>, a14/> 및 `}`도 허용됩니다. `$``{` 전자 메일 주소를 `.`으로 시작하지 마십시오.

새 사용자가 이미 Adobe 고객이 아닌 경우 해당 사용자에 대한 고객 로그인을 생성하라는 메시지가 표시됩니다. 새 사용자에게 로그인 암호 및 확인 메시지가 전송됩니다. 새 사용자가 처음 로그인하면 고객 프로필을 채웁니다.

선택적으로 [!DNL Add Users] 페이지에서 하이퍼링크된 역할 이름을 클릭할 수 있습니다. 사용자를 역할에 할당하거나 역할에서 사용자 할당을 취소할 수 있는 [!DNL Role Membership] 페이지가 열립니다.

[역할 구성원 자격 구성](../c-about-settings-menu/c-about-users-menu.md#task_DAC596AAFFCE4EF0BE68CEEF7E365414)을 참조하십시오.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**계정 사용자를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL Add Users]**&#x200B;를 클릭합니다.
1. [!DNL Add Users] 페이지의 [!DNL User's Email] 필드와 [!DNL User's Email (again)] 필드에 새 사용자의 전자 메일 주소를 입력합니다.
1. (선택 사항) 새 계정 사용자에게 계정 사용자를 제거하거나 계정 사용자 역할을 편집할 수 있는 권한을 부여하려면 **[!UICONTROL User Administrator]**&#x200B;을 선택합니다.
1. [!DNL Roles for this User] 테이블에서 새 계정 사용자에게 할당할 역할을 확인합니다.
1. 클릭 **[!UICONTROL Add User]**.

## 계정 {#task_4EAE1D018F384691A083AD51E5CE58DC}에 대해 존재하는 역할 보기

[!DNL View Roles] 페이지를 사용하여 현재 로그인한 계정에 대해 현재 존재하는 모든 역할을 표시할 수 있습니다.

계정에 대한 역할이 없는 경우 사용자 인터페이스에 이 문제가 표시됩니다. 역할 추가를 사용하여 역할을 만들고 추가할 수 있습니다.

[계정](../c-about-settings-menu/c-about-users-menu.md#task_E148D02275DE4F899BA79736A29895AB)에 새 역할 추가를 참조하십시오.

역할을 제거해도 역할을 할당받은 계정 사용자는 삭제되지 않습니다.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**계정에 대해 존재하는 역할을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL View Roles]**&#x200B;를 클릭합니다.
1. (선택 사항) 테이블의 [!DNL Remove?] 열 머리글에서 제거할 역할을 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 테이블의 [!DNL Role Name] 열 머리글에서 하이퍼링크된 역할 이름을 클릭합니다. 사용자를 역할에 할당하거나 역할에서 사용자 할당을 취소할 수 있는 [!DNL Role Membership] 페이지가 열립니다.

      [역할 구성원 자격 구성](../c-about-settings-menu/c-about-users-menu.md#task_DAC596AAFFCE4EF0BE68CEEF7E365414)을 참조하십시오.

   * 표의 [!DNL Edit] 열 머리글에서 연필 아이콘을 클릭합니다. [!DNL Edit Role] 페이지가 열리고 역할 이름 변경, 설명 변경 등이 가능합니다.

      [역할 편집](../c-about-settings-menu/c-about-users-menu.md#task_13875C2464034CE387285640412E1B59)을 참조하십시오.

## 역할 편집 {#task_13875C2464034CE387285640412E1B59}

기존 역할의 이름을 변경하고, 해당 설명을 변경하고, 역할 액세스 권한을 부여할 사용자 인터페이스의 영역만 선택할 수 있습니다.

[계정](../c-about-settings-menu/c-about-users-menu.md#task_E148D02275DE4F899BA79736A29895AB)에 새 역할 추가를 참조하십시오.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**역할을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL View Roles]**&#x200B;를 클릭합니다.
1. 표의 [!DNL Edit] 열 머리글에서 변경할 역할 옆에 있는 연필 아이콘을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 원하는 경우 [!DNL Role Name] 텍스트 필드에 새 이름을 입력합니다. *는 역할에 이 필드가 필수임을 나타냅니다.
   * 원하는 경우 [!DNL Description] 텍스트 필드에 역할에 대한 새 설명을 입력합니다.
   * 그룹 상자에서 역할에 액세스하거나 차단할 기능을 선택하거나 선택 취소합니다.

1. 클릭 **[!UICONTROL Save Changes]**.

## 계정 {#task_E148D02275DE4F899BA79736A29895AB}에 새 역할 추가

[!DNL Add Roles] 페이지를 사용하여 계정 사용자에게 권한을 보다 쉽고 빠르게 할당할 수 있습니다.

예를 들어 홍보 부서의 각 멤버에게 사이트 검색/머천다이징 작업에 대한 액세스 권한을 개별적으로 부여할 수 있습니다. 그러나 이러한 사용자를 &quot;PR&quot; 역할에 추가한 다음 해당 작업을 전체 역할에 할당하는 것이 더 효율적입니다.

각 역할 이름은 고유해야 합니다. 대시 `"-"`, 밑줄 `"_"` 및 마침표 `"."`를 비롯한 영숫자 문자와 공통 기호를 사용할 수 있습니다. 이름은 밑줄 또는 마침표로 시작할 수 없습니다.

테이블의 [!DNL Users in This Role] 열 헤더 아래에서, 선택적으로 사용자의 하이퍼링크된 이메일 주소를 클릭할 수 있습니다. 사용자를 역할에 할당하거나 역할에서 사용자 할당을 취소할 수 있는 특정 사용자에 대해 [!DNL Role Membership] 페이지가 열립니다.

[역할 구성원 자격 구성](../c-about-settings-menu/c-about-users-menu.md#task_DAC596AAFFCE4EF0BE68CEEF7E365414)을 참조하십시오.

테이블의 [!DNL Roles] 열 헤더 아래에서, 선택적으로 하이퍼링크된 역할 이름을 클릭할 수 있습니다. 선택한 역할에 사용자를 할당하거나 선택한 역할에서 사용자 할당을 취소할 수 있는 [!DNL Role Membership] 페이지가 열립니다.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**계정에 새 역할을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL Add Roles]**&#x200B;를 클릭합니다.
1. [!DNL Add Roles] 페이지의 [!DNL Role Name] 필드에 역할의 이름을 입력합니다.
1. (선택 사항) [!DNL Description] 필드에 역할을 적절히 설명하는 문장을 입력합니다.
1. 각 전자 메일 주소 왼쪽에 있는 상자를 선택하여 역할에 속한 사용자를 선택합니다.
1. 클릭 **[!UICONTROL Add Role]**.

## 역할 구성원 자격 구성 {#task_DAC596AAFFCE4EF0BE68CEEF7E365414}

[!DNL Role Membership] 페이지를 사용하여 역할에 사용자를 추가하거나 역할에서 사용자를 제거할 수 있습니다.

사용자별로 역할을 볼 때 개별 사용자 그룹 멤버십을 관리할 수도 있습니다.

[계정](../c-about-settings-menu/c-about-users-menu.md#task_E148D02275DE4F899BA79736A29895AB)에 새 역할 추가를 참조하십시오.

[계정](../c-about-settings-menu/c-about-users-menu.md#task_4EAE1D018F384691A083AD51E5CE58DC)에 대해 존재하는 역할 보기를 참조하십시오.

>[!NOTE]
>
>이 작업을 수행하려면 관리자 권한이 있는 사이트 검색/머천다이징 사용자여야 합니다.

**계정 사용자를 역할에 할당하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Users]** > **[!UICONTROL Role Membership]**&#x200B;를 클릭합니다.
1. [!DNL Role Membership] 페이지에서 다음 중 하나를 수행합니다.

   <table> 
      <thead class="chhead sthead"> 
      <th class="choptionhd"> <p>옵션 </p> </th> 
      <th class="chdeschd"> <p>단계 </p> </th> 
      </thead> 
      <tr class="chrow strow"> 
      <td class="choption"><strong>단일 역할에 하나 이상의 사용자를 추가하려면</strong></td> 
      <td class="chdesc stentry"> <p>
      <ul id="ul_59E7C36210804EF9B6A2706A5357A892"> 
      <li id="li_2A8D31C968B543EBA7948DD4EFA350AA"> <span class="uicontrol"> 역할 변경</span> 드롭다운 목록에서 사용자를 추가할 역할을 선택합니다. <p><span class="uicontrol"> 역할 변경</span> 드롭다운 목록이 표시되지 않으면 <span class="uicontrol"> GROUP별 사용자 보기</span>를 클릭합니다. </p> </li> 
      <li id="li_3A67F0DDBDBE4883A17300A3F088D71A"> (선택 사항) 표에서 <span class="uicontrol"> 역할 멤버만 표시</span> 테이블에 선택된 역할에 현재 할당된 계정 사용자만 테이블에 표시되도록 하십시오. </li> 
      <li id="li_4926A22D1ED94AC9972C2619A398A8C7"> 테이블의 확인란 열에서 선택한 역할에 할당할 계정 사용자를 하나 이상 선택합니다. <p>선택한 역할에서 제거하려는 계정 사용자를 하나 이상 선택 취소합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr class="chrow strow"> 
      <td class="choption"><strong>단일 사용자에게 하나 이상의 역할을 추가하려면</strong></td> 
      <td class="chdesc stentry"> <p> 
         <ul id="ul_B3F8E84B0ED94B2D83F0DB0C91F07DC7"> 
         <li id="li_67EE15F527384CCDB8171DB3D89F6819"> <span class="uicontrol"> 사용자 변경</span> 드롭다운 목록에서 하나 이상의 역할을 할당할 사용자를 선택합니다. <p><span class="uicontrol"> 사용자 변경</span> 드롭다운 목록이 표시되지 않으면 <span class="uicontrol"> 사용자별 역할 보기</span>를 클릭합니다. </p> </li> 
         <li id="li_7830E87D6924433DBBA03C953B9452A2"> (선택 사항) 표에서 <span class="uicontrol"> 이 사용자의 역할만 표시</span> 를 선택하여 선택된 계정 사용자에게 현재 할당된 역할만 테이블에 표시합니다. </li> 
         <li id="li_DE742B95BFC34BF4AE338B165B533FDF"> 테이블의 확인란 열에서 선택한 사용자에게 할당할 역할을 하나 이상 선택합니다. <p>선택한 사용자에서 제거할 역할을 하나 이상 선택 취소합니다. </p> </li> 
         </ul> </p> </td> 
      </tr> 
   </table>

1. **변경 내용 저장**&#x200B;을 클릭합니다.
