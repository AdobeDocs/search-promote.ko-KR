---
description: 검색 쿼리 결과 확장을 재정의할 수 있습니다.
solution: Target
title: 쿼리 확장 무시 정보
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 0%

---


# 쿼리 확장 재정의 정보{#about-query-expansion-overrides}

검색 쿼리 결과 확장을 재정의할 수 있습니다.

## 쿼리 확장 무시 사용 {#concept_6895B469B0E044299E93361BFA06B554}

쿼리 확장 재정의를 구성할 때 &quot;규칙&quot; 세트를 만듭니다. 각 규칙은 기본적으로 &quot;검색 시 `<this>`을(를) `<that>`으로 확장하지 마십시오&quot;(여기서 `<this>`는 간단한 텍스트 단어 또는 구문이고 `<that>`은 텍스트 단어 또는 구문 또는 분류입니다.)

>[!NOTE]
>
>이 기능은 기본적으로 Search &amp; Promote에서 활성화되지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. 쿼리 확장 재정의 기능이 활성화되면 사용자 인터페이스에서 &quot;설정&quot;해야 합니다.

**쿼리 확장 재정의 작동 방식**

[쿼리 확장 재정의 추가] 페이지에서 텍스트 및 용어 값이 지정된 경우 코드는 특정 쌍에 대해 작동합니다. 사전 또는 Alternate Word Forms과 같은 용어로 분류 유형을 지정하면 확장 안 함 값이 지정된 분류로 생성된 양식으로 변환되지 않습니다.

예를 들어 다음 정의가 있다고 가정합니다.

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

대체 단어 Forms을 통해 &quot;dog&#39;s&quot; 및 &quot;dogs&quot;를 포함하도록 확장되는 &quot;dog&quot;에 대한 검색 쿼리는 &quot;dogs&quot;를 포함하지 않습니다.

그러나 정의가 다음과 같은 경우:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

쿼리는 &quot;dog&#39;s&quot; 또는 &quot;dogs&quot;(&quot;dog&quot;의 경우 사용 가능한 대체 단어 Forms)을 포함하지 않습니다.

여러 용어, 여러 분류 또는 둘 다를 지정할 수 있습니다. 그러나 유형으로 모두를 선택하면 여러 용어 목록이 하나의 &quot;모두&quot; 항목으로 축소됩니다.

텍스트 및 분류 항목이 규칙에 혼합되면 사용자 인터페이스에서 텍스트 값을 먼저 표시하도록 다시 구성됩니다. 그러나 검색 시 평가 순서가 암시되거나 영향을 받지 않습니다.

텍스트 용어는 무의미한 참조를 제거하기 위해 확인됩니다. 즉, 용어 확장 안 함 값과 용어를 비교하고 일치하는 항목이 있으면 용어를 제거합니다. 또한 텍스트 또는 분류와 같은 중복 용어 값이 제거됩니다.

이전 정의를 복제하는 값을 확장하지 않음 값으로 새 규칙을 추가하는 경우 새 정의 용어가 원본에 추가됩니다.

## 쿼리 확장 재정의 구성 {#task_A087354A509D4997BA275186C224160E}

Search &amp; Promote에서 쿼리 확장 재정의 정의 및 추가

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
이 기능은 기본적으로 Search &amp; Promote에서 활성화되지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. 쿼리 확장 재정의 기능이 활성화되면 사용자 인터페이스에서 &quot;설정&quot;해야 합니다. 이 작업을 수행하는 방법에 대한 개요는 아래의 처음 몇 단계입니다.

**쿼리 확장 무시를 구성하려면**

1. Search &amp; Promote에서 **설정** > **사용자** > **역할 보기**&#x200B;를 클릭합니다.
1. 역할 보기 페이지의 테이블의 작업 열에서 언어 메뉴의 쿼리 확장 오버라이드에 대한 액세스 권한을 부여할 역할의 오른쪽에 있는 **편집**&#x200B;을 클릭합니다.
1. 역할 편집 페이지에서 언어학 트리를 확장합니다.
1. **쿼리 확장 재정의**&#x200B;를 선택한 다음 **변경 내용 저장**&#x200B;을 클릭합니다.
1. **언어학** > **쿼리 확장 재정의**&#x200B;를 클릭합니다.
1. **쿼리 확장 재정의 추가**&#x200B;를 클릭합니다.
1. 쿼리 확장 재정의 추가 페이지에서 원하는 옵션을 설정합니다.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
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
      <td colname="col1"> <p>확장 안 함 </p> </td> 
      <td colname="col2"> <p>확장하지 않을 단어 또는 구를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p><b>텍스트</b>를 선택하여 특정 단어 또는 구문 연결을 지정합니다. 또는 분류를 선택하여 선택한 분류를 통해 단어 또는 구문을 확장하지 않도록 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>용어 </p> </td> 
      <td colname="col2"> <p><b>텍스트</b>를 유형으로 선택한 경우에만 사용할 수 있습니다. 검색 확장에서 제외할 단어 또는 구를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 </p> </td> 
      <td colname="col2"> <p> 각각 정의에 용어를 추가하거나 삭제하려면 <b>+</b> 또는 <b>-</b>을 클릭합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 완료되면 **추가**&#x200B;를 클릭합니다.

   쿼리 확장 재정의 정의 페이지에서 추가한 정의를 편집하거나 삭제할 수 있습니다.
1. 추가 결과를 미리 보려면 파란색 상자에 있는 **스테이지된 사이트 인덱스**&#x200B;를 다시 생성하여 스테이지된 웹 사이트 인덱스를 신속하게 다시 작성합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **라이브**&#x200B;를 클릭합니다.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F) 참조

   * **라이브 푸시**&#x200B;를 클릭합니다.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

