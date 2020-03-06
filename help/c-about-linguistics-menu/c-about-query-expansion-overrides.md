---
description: 검색 쿼리 결과 확장을 무시할 수 있습니다.
seo-description: 검색 쿼리 결과 확장을 무시할 수 있습니다.
seo-title: 쿼리 확장 무시 정보
solution: Target
title: 쿼리 확장 무시 정보
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 쿼리 확장 무시 정보{#about-query-expansion-overrides}

검색 쿼리 결과 확장을 무시할 수 있습니다.

## 쿼리 확장 재정의 사용 {#concept_6895B469B0E044299E93361BFA06B554}

쿼리 확장 재정의를 구성할 때 &quot;규칙&quot; 세트를 만듭니다. 각 규칙에는 기본적으로 &quot;검색 시 확장하지 마십시오&quot; `<this>` 라는 텍스트 단어나 구가 `<that>` 있고 텍스트 단어나 구문이나 `<this>` `<that>` 분류가 있습니다.

>[!NOTE]
>
>이 기능은 기본적으로 Search&amp;Promote에서 활성화되지 않습니다. 해당 기능을 활성화하려면 기술 지원 센터에 문의하십시오. 쿼리 확장 무시 기능이 활성화되면 사용자 인터페이스에서 &quot;설정&quot;해야 합니다.

**쿼리 확장 재정의 작동 방식**

[쿼리 확장 무시 추가] 페이지에서 텍스트 및 용어 값이 지정되면 코드는 특정 연결에 대해 작동합니다. 사전 또는 대체 Word 양식과 같은 분류 유형이 용어로 지정되면 확장 안 함 값은 지정된 분류로 생성된 양식으로 변환되지 않습니다.

예를 들어 다음과 같은 정의가 있다고 가정합니다.

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

대체 단어 양식을 통해 &quot;dog&#39;s&quot; 및 &quot;dogs&quot;를 포함하도록 확장되는 &quot;dogs&quot;에 대한 검색 쿼리에는 &quot;dogs&quot;가 포함되지 않습니다.

그러나 정의가 다음과 같은 경우:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

쿼리에는 &quot;dog&#39;s&quot; 또는 &quot;dogs&quot;(&quot;dog&quot;에 대한 대체 단어 형식)가 포함되어 있지 않습니다.

여러 용어, 여러 분류 또는 둘 다를 지정할 수 있습니다. 그러나 [모두]를 [유형]으로 선택하면 여러 용어 목록이 하나의 &quot;모두&quot; 항목으로 축소됩니다.

모든 규칙에서 텍스트 및 분류 항목이 혼합되어 있는 경우 사용자 인터페이스에서 텍스트 값을 먼저 표시하도록 재구성됩니다. 그러나 검색 시 평가 순서에 영향을 미치거나 암시하지는 않습니다.

텍스트 용어는 무의미한 참조를 제거하기 위해 확인됩니다. 즉, 용어를 확장 안 함 값과 비교하고 일치하는 항목이 있으면 용어를 제거합니다. 또한 텍스트나 분류와 같은 중복 용어 값이 제거됩니다.

이전 정의를 복제하는 확장 안 함 값으로 새 규칙을 추가하면 새 정의의 용어가 원본에 추가됩니다.

## 쿼리 확장 재정의 구성 {#task_A087354A509D4997BA275186C224160E}

Search&amp;Promote에서 쿼리 확장 재정의 정의 및 추가.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
이 기능은 기본적으로 Search&amp;Promote에서 활성화되지 않습니다. 해당 기능을 활성화하려면 기술 지원 센터에 문의하십시오. 쿼리 확장 무시 기능이 활성화되면 사용자 인터페이스에서 &quot;설정&quot;해야 합니다. 아래의 첫 번째 몇 단계는 그 방법을 요약해 놓은 것이다.

**쿼리 확장 재정의 구성**

1. Search&amp;Promote에서 설정 > **사용자** > **역할** 보기를 **클릭합니다**.
1. [역할 보기] 페이지의 테이블의 [작업] 열에서 **** [언어학] 메뉴의 [쿼리 확장 무시]에 액세스할 수 있는 역할의 오른쪽에 있는 편집을 클릭합니다.
1. 역할 편집 페이지에서 언어학 트리를 확장합니다.
1. 쿼리 **확장 무시를**&#x200B;확인한 다음 변경 내용 **저장을 클릭합니다**.
1. 언어학 **** > **쿼리 확장 무시를 클릭합니다**.
1. 쿼리 **확장 무시 추가를 클릭합니다**.
1. 쿼리 확장 무시 추가 페이지에서 원하는 옵션을 설정합니다.

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
      <td colname="col2"> <p>확장하지 않을 단어 또는 구문을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p>텍스트를 <b>선택하여</b> 특정 단어나 구문 연결을 지정합니다. 또는 분류를 선택하여 단어 또는 구문을 선택한 분류를 통해 변환되지 않도록 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>용어 </p> </td> 
      <td colname="col2"> <p>텍스트를 <b>유형으로 선택한</b> 경우에만 사용할 수 있습니다. 검색 확장에서 제외할 단어 또는 구문을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 </p> </td> 
      <td colname="col2"> <p> Click <b>+</b> or <b>-</b> to add or delete Terms, each, to the definition. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 완료되면 추가를 **클릭합니다**.

   질의 확장 대체 정의 페이지에서 추가한 정의를 편집하거나 삭제할 수 있습니다.
1. 추가 결과를 미리 보려면 파란색 상자에서 스테이지된 사이트 인덱스를 **다시** 생성하여 스테이지된 웹 사이트 인덱스를 신속하게 다시 만듭니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * [라이브] **를 클릭합니다**.

      라이브 [설정 보기를 참조하십시오.](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)

   * [ **라이브 푸시]를 클릭합니다**.

      스테이지 [설정 라이브 푸시를 참조하십시오.](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

