---
description: 전체 인덱스를 사용하여 스테이징 또는 라이브 웹 사이트의 모든 페이지를 색인화할 수 있습니다. 색인화를 통해 고객이 원하는 것 또는 검색을 수행할 때 필요한 내용을 보다 손쉽게 찾을 수 있습니다.
solution: Target
subtopic: Full Index
title: 전체 색인 정보
topic-legacy: Index,Site search and merchandising
uuid: dce1eafd-5aea-4945-8305-8f9e7dc392df
exl-id: cb702bd6-8702-469b-8ce9-0368ccdd55d9
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---

# 전체 인덱스 정보{#about-full-index}

전체 인덱스를 사용하여 스테이징 또는 라이브 웹 사이트의 모든 페이지를 색인화할 수 있습니다. 색인화를 통해 고객이 원하는 것 또는 검색을 수행할 때 필요한 내용을 보다 손쉽게 찾을 수 있습니다.

## 전체 인덱스 사용 {#concept_C69BD21863FD4856B49326F35DB570D3}

전체 인덱스를 생성할 때 색인 작성 프로세스 동안 시작 시간, 경과 시간 및 오류와 같은 상태 정보가 표시됩니다. 마지막 인덱스의 상태에 대한 정보도 표시됩니다.

색인 재생이 필요한 계정 설정을 변경한 경우 상태가 &quot;다시 생성&quot;으로 표시될 수 있습니다. 재생성하는 동안 계정 설정이 업데이트된 사이트 인덱스를 만들기 위해 적용됩니다.

언제든지 색인 작성 프로세스를 중지하거나 다시 시작할 수 있습니다.

새 색인은 라이브 웹 사이트에 대해 작성되지만 고객은 마지막 색인을 사용하여 사이트를 계속 검색할 수 있습니다. 마지막 인덱스의 상태에 대한 정보도 표시됩니다.

## 라이브 웹 사이트 {#task_6760F3256D004A228B38968DF15421F0}에 대한 전체 인덱스 일정 설정

웹 사이트를 크롤링할 시간 및 일을 지정하고 인덱스를 업데이트할 수 있습니다.

선택한 시간은 계정 설정에 구성된 시간대에 따라 로컬입니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

웹 서버는 종종 밤에 유지 보수를 위해 아래로 내려갈 예정이다. 예약된 색인 시간 동안 서버가 다운된 경우 색인 지정 프로세스가 실패합니다. 웹 서버를 사용할 수 있는 시간을 선택해야 합니다.

색인 일정은 라이브 색인에만 적용됩니다.스테이지된 색인은 예약할 수 없습니다.

**라이브 웹 사이트에 대한 전체 색인 일정을 설정하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Schedule]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Time]** 드롭다운 목록에서 전체 인덱싱을 시작할 시간을 선택합니다.
1. 전체 색인화를 실행할 일 이상을 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.

## 라이브 또는 스테이지된 웹 사이트의 전체 인덱스 실행 {#task_F7FE04D8A1654A7787FCCA31B45EB42D}

전체 인덱스를 사용하여 스테이징 또는 라이브 웹 사이트의 모든 페이지를 색인화할 수 있습니다. 색인화를 통해 고객이 원하는 것 또는 검색을 수행할 때 필요한 내용을 보다 손쉽게 찾을 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 전체 인덱스를 실행하려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Index]**.

1. 원하는 인덱싱 옵션을 설정합니다.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>옵션 </p> </th> 
    <th colname="col2" class="entry"> <p>설명 </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>인덱스 캐시 지우기 </p> </td> 
    <td colname="col2"> <p>인덱스 캐시에서 모든 문서를 제거합니다. </p> <p>이 옵션을 선택하면 모든 웹 사이트 페이지가 서버에서 다운로드됩니다. 이 설정을 선택하고 비활성화하면 전체 인덱스가 수행될 때마다 계정이 캐시를 지우도록 설정됩니다. 또는 이전에 변경한 일부 계정 설정은 이제 전체 색인이 필요합니다. </p> <p>이 옵션을 선택 해제하면 웹 서버에서 페이지가 더 이상 존재하지 않는다고 말할 때까지 모든 인덱스 페이지가 인덱스에 유지됩니다. 이 상황은 해당 페이지에 대한 링크가 제거되더라도 적용됩니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>보류 중 다시 생성 </p> </td> 
    <td colname="col2"> <p>색인 내용을 상당히 변경하는 계정 설정을 변경한 경우 을 선택합니다. 다음과 같은 사항을 변경하는 것이 실질적으로 포함됩니다. 
    <ul id="ul_4EB8FF692FEB47BBB9A64D61299380D1"> 
    <li id="li_7CF8D286512F4210BEA3DB9F0EFA097A">동의어 </li> 
    <li id="li_8178ABC342BB4365B3927E20433756E3">컬렉션 </li> 
    <li id="li_57C8BD06BFA64AFAA2C9EF2CC59520EF">메타데이터 </li> 
    <li id="li_C4B6A7DA023B4A43991D03EC592170C9">제외된 단어 </li> 
    <li id="li_9E0AD4B6DDC24A5A8FB5C2C1CCD5348A">계정 언어 </li> 
    <li id="li_338F107547DF48AAA0EF90F4AD8664A5">등급 </li> 
    <li id="li_7F49B86D94974E79AAD381A64A1400F2">대소문자를 구분하는 검색 전환 </li> 
    <li id="li_E8FE6EE240A840AC826ADF4294AAC6F6">발음 부호 지원 전환 </li> 
    <li id="li_51763D482DCB4ED0972966F492B8C0F2">숫자 색인 전환 중 </li> 
    </ul> </p> <p>다른 크롤이 실행되기 전에 모든 색인 데이터를 통해 빠른 전달을 수행하여 새 계정 설정을 따르게 합니다. </p> <p>이 옵션은 스테이지 웹 사이트의 전체 인덱스를 수행하는 경우에만 사용할 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>모든 페이지 카운트 </p> </td> 
    <td colname="col2"> <p>계정 페이지 제한에 도달해도 웹 사이트 페이지 크롤링을 계속할 수 있습니다. </p> <p>추가 페이지는 색인에 추가되지 않지만 웹 사이트의 총 문서 수를 확인할 수 있습니다. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Full Index Now]**.
1. (선택 사항) 색인 오류가 발생하면 **[!UICONTROL View Errors]**&#x200B;을 클릭하여 연결된 로그를 봅니다.

## 라이브 또는 스테이지된 웹 사이트 {#task_02E5E944C56B4EB19CC1FF321F3221B8}의 전체 인덱스 로그 보기

실시간 전체 인덱스 또는 스테이지된 전체 인덱스가 완료되면 연결된 로그를 보고 발생한 오류를 해결할 수 있습니다.

로그를 내보내거나 저장할 수 없습니다. 로그는 새 색인이 발생할 때까지 볼 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 전체 색인 로그를 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Log]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Log]**.

1. 로그 페이지의 맨 위 또는 아래에서 다음 중 하나를 수행합니다.

   * 탐색 옵션 **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** 또는 **[!UICONTROL Go to line]**&#x200B;을 사용하여 로그를 통해 이동합니다.

   * 표시 옵션 **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** 또는 **[!UICONTROL Show]**&#x200B;을 사용하여 표시되는 내용을 세밀하게 수정할 수 있습니다.
