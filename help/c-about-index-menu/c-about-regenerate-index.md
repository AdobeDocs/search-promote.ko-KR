---
description: 사이트를 다시 크롤링하지 않고도 색인 재생성을 사용하여 웹 사이트의 인덱스를 업데이트할 수 있습니다.
solution: Target
subtopic: Regenerate Index
title: 색인 재생성 정보
topic: 색인, 사이트 검색 및 머천다이징
uuid: 9d1f1d88-0453-4422-a625-a348febbf224
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# 인덱스 다시 생성 정보{#about-regenerate-index}

[!DNL Regenerate Index]을 사용하여 사이트를 다시 크롤링하지 않고도 웹 사이트의 인덱스를 업데이트할 수 있습니다.

## 인덱스 다시 생성 사용 {#concept_6CBE6B8D18EF47D293091CBA542245FA}

다음 계정 옵션을 변경할 때마다 이 옵션을 사용할 수 있습니다.

* 단어 및 언어
* 제외된 단어
* 동의어
* 메타데이터 필드를 삭제할 때 필드 이름, 데이터 유형, 날짜 형식, 정렬 순서, 최소 또는 최대 등급 값, 기본 등급 값, 목록 유형 또는 목록 구분 기호를 변경할 때 메타데이터 설정이 사용됩니다.

업데이트된 계정 옵션 정보는 새 사이트 인덱스를 생성하는 데 사용됩니다. 재생성 기능을 사용하면 사이트 인덱스를 빠르고 효율적으로 변경할 수 있습니다.

기본적으로 새 웹 사이트 컨텐츠 또는 변경된 웹 사이트 컨텐츠는 색인에 포함되지 않습니다. 이러한 컨텐츠를 포함하려면 전체 또는 증분 인덱스를 실행합니다.

라이브 또는 스테이징된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).[

라이브 또는 스테이지된 웹 사이트의 증분 인덱스 실행 참조: [](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## 라이브 또는 스테이지된 웹 사이트 {#task_B28DE40C0E9A475ABCBCBC4FF993AACD}의 인덱스 다시 생성

[!DNL Regenerate Index]을(를) 사용하여 사이트를 다시 로드할 필요 없이 웹 사이트의 인덱스를 업데이트할 수 있습니다.

**라이브 또는 스테이지된 웹 사이트의 인덱스를 다시 생성하려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Regenerate]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Regenerate]**.

1. [!DNL Regenerate] 페이지에서 **[!UICONTROL Regenerate Index Now]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL Live Regenerate]**&#x200B;을(를) 실행하도록 선택한 경우 **[!UICONTROL View Last Crawl]**&#x200B;을 클릭하여 마지막으로 수행된 라이브 인덱스 재생성에 대한 성능 통계를 검토합니다.

   * 인덱스를 다시 생성하는 동안 **[!UICONTROL Stop Regenerate Now]**&#x200B;을 클릭하여 색인 재생성 프로세스를 중지합니다.
   * 인덱스를 다시 생성하는 동안 **[!UICONTROL Restart Regenerate Now]**&#x200B;을 클릭하여 색인 재생성 프로세스를 처음부터 다시 시작합니다.
   * 스테이지된 재생성 후 색인 오류가 발생하면 **[!UICONTROL View Errors]**&#x200B;을 클릭하여 연관된 로그를 확인합니다.

## 라이브 또는 스테이지된 웹 사이트 {#task_61CE8F9E7BF84BA89A8D482B2106BB15}의 다시 생성된 색인 로그 보기

실시간 색인 재생성 또는 스테이지된 인덱스 재생성 작업이 완료되면 연관된 로그를 보고 발생한 오류를 해결할 수 있습니다.

로그를 내보내거나 저장할 수 없습니다. 그러나 새 색인이 발생할 때까지 로그는 계속 볼 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 재생성된 색인 로그를 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Log]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Log]**.

1. 로그 페이지의 맨 위 또는 아래에서 다음 중 하나를 수행합니다.

   * 탐색 옵션 **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** 또는 **[!UICONTROL Go to line]**&#x200B;을 사용하여 로그를 통해 이동합니다.

   * 표시 옵션 **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** 또는 **[!UICONTROL Show]**&#x200B;을 사용하여 표시되는 내용을 세밀하게 수정할 수 있습니다.

