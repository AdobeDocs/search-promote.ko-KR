---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 15.3.1 릴리스 노트(2015년 3월 24일)
solution: Target
title: Search&amp;Promote 15.3.1 릴리스 노트(2015년 3월 24일)
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 15.3.1 Release Notes (03/24/2015){#search-promote-release-notes}

## 새로운 기능 및 향상된 기능 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 제품 모델 번호 검색 - 원할 경우 알파벳순 전환 시 토큰을 분할할 수 있는 새로운 언어학 설정이 추가되었습니다. 이 기능을 사용하면 부품 또는 제품 스타일 토큰에서 보다 유연한 자유 텍스트 일치를 사용할 수 있습니다.

   웹 **[!UICONTROL Partial Alphanumeric Matching]** 컨텐츠와 [검색어 일치 방법 구성에서 참조하십시오.](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* 데이터 보기 결과를 내보내는 기능이 추가되었습니다.

   데이터 [보기 정보를 참조하십시오](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

* 동적으로 생성된 범위를 참조하십시오.

   현재 Adobe Systems에서는 범위 값을 식별하는 컨텐츠를 제공해야 합니다. 예를 들어 10인 경우 범위 문자열 &quot;$10에서 $20 사이&quot;를 생성합니다. 또는 Adobe Systems에서 스크립트 필터링을 사용해야 합니다. 메타데이터 필드 정의에 필드 전용 새 속성을 `Type=Number` 추가했습니다. 새 옵션은 숫자 필드를 `Type=Text` 필드와 연결하고 범위 설명이 구성되는 방식을 설명하는 구성 정보를 지정합니다.

   새 [메타 태그 필드](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)추가를 참조하십시오.

## 수정 사항 {#section_22D1AFC99F394D569898828A0D3C419D}

* 패싯 레일 편집 대화 상자에는 스테이지된 패싯이 포함되어야 합니다.
* 일본어 문자가 포함된 검색에 대해 &quot;포함된&quot; 검색 모드에 대한 빈 코어 검색 결과.
* 이제 Word .docx 파일의 Tika 변환이 `title` 속성을 채웁니다.
* 관리자의 잘못된 &quot;중복 배너&quot; 메시지를 수정했습니다. **[!UICONTROL Banner]**
* [!DNL Dynamic Media Classic] 배너는 이제 프로토콜에 관계없이 사용할 수 있습니다.
* 경우에 따라 **[!UICONTROL Table Name]** **[!UICONTROL Dynamic Facets]** 필드 속성은 계정에 대해 활성화된 경우에도 메타데이터 사용자 정의 필드를 편집할 때 숨겨졌습니다.
* **[!UICONTROL Recent Searches]** 더 이상 비ASCII 문자를 곱하기 인코딩하지 않습니다.
* 스크립트 필터링을 사용하지 않고 MDI 필드를 채울 수 있습니다.
* 제안의 인코딩이 잘못되었습니다.
* 이제 복잡한 비즈니스 규칙에서 &quot;기타 패싯 선택&quot; 트리거가 올바르게 작동합니다.

