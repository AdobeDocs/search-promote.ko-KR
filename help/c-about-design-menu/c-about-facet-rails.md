---
description: 패싯 레일을 사용하여 웹 페이지에서 패싯 그룹의 순서를 변경합니다.
seo-description: 패싯 레일을 사용하여 웹 페이지에서 패싯 그룹의 순서를 변경합니다.
seo-title: 패싯 레일 정보
solution: Target
subtopic: Navigation
title: 패싯 레일 정보
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# 패싯 레일 정보{#about-facet-rail}

패싯 레일을 사용하여 웹 페이지에서 패싯 그룹의 순서를 변경합니다.

## 패싯 레일 사용 {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

패싯은 속성 또는 특성이며, 일반적으로 검색 결과를 분류하는 방법입니다. 예를 들어 제조업체, 가격 및 색상은 패싯 그룹으로 간주될 수 있습니다. 각 패싯에는 여러 개의 제한 또는 값이 있을 수 있습니다. 예를 들어, 단면화로 색상이 있는 경우 &quot;단면값&quot;은 빨강, 주황색, 노랑, 녹색, 파랑, 남색 및 보라가 될 수 있습니다.

패싯 [정보를 참조하십시오](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

패싯 레일을 사용하여 웹 페이지에서 이러한 패싯 그룹의 순서를 변경합니다. 예를 들어 웹 페이지의 왼쪽에 검색 결과 섹션이 있다고 가정해 봅시다. 나열된 섹션, 위에서 아래로, 카테고리 패싯, 브랜드 패싯, 가격 패싯 및 가장 빈도가 높은 패싯. 패싯 레일을 사용하면 가장 빈도가 높은 패싯이 카테고리 패싯 위나 아래에 표시되도록 할 수 있습니다.

함께 순서를 바꾸려는 패싯 그룹은 패싯 레일 태그에 속합니다. 단면화는 하나의 단면화 레일에만 속할 수 있습니다. 패싯 레일은 프레젠테이션 템플릿 태그로 패싯의 단일 표현을 포함합니다. 이 레일에 속하는 모든 패싯은 해당 단일 패싯 표현을 공유합니다.

프레젠테이션 [템플릿 태그의](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) 템플릿 및 [패싯](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)정보를 참조하십시오.

## 패싯 레일 구성 {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

패싯 레일을 추가하여 프레젠테이션 레이어를 사용자 정의할 수 있습니다. 패싯 레일은 고객이 웹 페이지의 패싯 순서를 기반으로 검색 결과를 드릴다운할 수 있도록 하는 검색 안내 가이드를 제공합니다.

<!-- 

t_configuring_facet_rail.xml

-->

패싯 레일을 변경하면 내역 기능을 사용하여 되돌릴 수 있습니다.

**패싯 레일을 구성하려면**

1. 패싯 레일을 구성하려면 먼저 이미 패싯을 추가했고 해당 작업의 일부로 패싯 레일 이름을 지정했는지 확인하십시오.

   새 [패싯](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B)추가를 참조하십시오.
1. 제품 메뉴에서 > **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. 페이지에서 [!DNL Facet Rail] 패싯 레일에 포함할 패싯을 선택한 다음 드롭다운 목록에서 **[!UICONTROL Sort Facets Method]** 옵션을 설정합니다.

   <!-- 
   r_facet_rail_options.xml
   -->

   | 기능/옵션 | 설명 |
   |--- |--- |
   | Facet Rail 이름 | 패싯 레일의 이름을 식별합니다.  패싯을 추가할 때 패싯 레일의 이름을 만듭니다.  새 [패싯 추가를 참조하십시오.](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | 포함된 패싯 | 패싯 레일에 추가하기 위해 선택할 수 있는 가능한 패싯 목록입니다.  패싯을 사용하여 정렬하도록 선택한 `Custom`경우 여기에서 패싯을 선택하는 순서에 따라 `Custom Facet Order` 텍스트 상자에 패싯이 표시되는 순서가 결정됩니다. |
   | 패싯 정렬 방법 | 드롭다운 목록에서 다음 세 가지 옵션 중 하나를 선택합니다.<ul><li>`Alpha` 패싯은 구두점 문자를 포함하여 해당 이름에 따라 알파벳 순으로 정렬됩니다.</li><li>`Alpha (not case sensitive)` 패싯은 이름에 따라 알파벳순 문자의 대/소문자를 무시하고 구두점 문자를 포함하여 알파벳순으로 정렬됩니다. </li><li>`Alpha (alphanumeric only)` 패싯은 구두점 문자를 무시하고 이름에 따라 알파벳 순서로 정렬됩니다. </li><li>`Alpha (not case sensitive, alphanumeric only)` 패싯은 이름에 따라 알파벳 순서로 정렬되며, 알파벳 문자의 대/소문자를 무시하고, 구두점 문자는 무시됩니다. </li><li>`Count` 패싯은 카운트에 따라 정렬됩니다. </li><li>`Custom` 각 패싯의 정확한 이름을 입력하여 패싯의 순서를 정의할 수 있는 `Custom Facet Order` 텍스트 상자를 엽니다. 남아 있는 패싯 레이블은 `Custom Facet Order` 목록에서 제거됩니다.</li></ul> |
   | 사용자 지정 패싯 순서 | 이 옵션은 `Custom` 드롭다운 `Sort Facets Method` 목록에서 선택한 경우에만 사용할 수 있습니다.  패싯 이름을 라인당 하나 또는 모두 한 줄 및 쉼표로 구분하여 나열할 수 있습니다. 패싯 레이블이 정의된 경우 `Facets Included` 목록에 괄호로 묶여 표시됩니다.  패싯 레이블을 `Custom Facet Order` 텍스트 상자에 포함하지 마십시오.  목록에서 패싯을 선택하거나 선택 취소하면 `Facets Included` 텍스트 `Custom Facet Order` 상자가 자동으로 업데이트됩니다. |

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Facet Rail] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

1. 다음을 수행하여 프레젠테이션 템플릿을 편집합니다.

   * 프레젠테이션 템플릿에서 &quot;패싯 템플릿&quot;을 만듭니다.
   * &quot;패싯 템플릿&quot;을 `<guided-facet-rail>` 태그로 둘러싸십시오.

      프레젠테이션 템플릿 태그의 [패싯을](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)참조하십시오.

      예:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      이러한 태그는 프레젠테이션 템플릿의 섹션을 잘라 패싯 레일의 각 패싯에 대해 반복 가능한 패턴이 됩니다. 패싯 레일에 속하는 각 패싯은 이 조각 섹션을 사용하여 해당 출력을 평가합니다. 최종 프레젠테이션 템플릿에는 하나의 `<guided-facet-rail>` 태그만 표시될 수 있습니다.

      값이 검색 시 동적으로 결정되고 올바르게 대체되므로 다음 태그에서는 `gsname` `<guided-facet-rail>` 속성이 필요하지 않습니다.

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * 프레젠테이션 템플릿을 저장하고 실시간으로 푸시합니다.

      프레젠테이션 [또는 전송 템플릿](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)편집을 참조하십시오.
