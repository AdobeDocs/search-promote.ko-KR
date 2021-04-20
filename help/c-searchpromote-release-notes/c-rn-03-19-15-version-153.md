---
description: Search&amp;Promote 15.3.1 릴리스 노트.
solution: Target
title: Search&Amp;Promote 15.3.1 릴리스 노트(03/24/2015)
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---


# Search &amp; Promote 15.3.1 릴리스 노트(03/24/2015){#search-promote-release-notes}

## 새로운 기능 및 향상된 기능 {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 제품 모델 번호 검색 - 선택적으로 토큰을 알파벳순으로 전환하여 분할할 수 있는 새로운 언어학 설정을 추가했습니다. 이 기능을 사용하면 부품 또는 제품 스타일 토큰에 대해 보다 유연한 자유 텍스트 일치를 사용할 수 있습니다.

   [웹 컨텐츠와 검색어가 일치하는 방법 구성의 **[!UICONTROL Partial Alphanumeric Matching]**&#x200B;을 참조하십시오.](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* 데이터 보기 결과를 내보내는 기능이 추가되었습니다.

   [데이터 보기 정보](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)를 참조하십시오.

* 동적으로 생성된 범위 속성에 대한 범위 속성 자동 패싯 값 버켓 기능.

   Adobe Systems에서는 이 작업을 수행하려면 현재 범위 값을 식별하는 내용을 제공해야 합니다. 예를 들어 10인 경우 &quot;$10에서 $20 사이&quot; 범위의 문자열을 생성합니다. 또는 Adobe Systems에서 스크립트 필터링을 사용해야 합니다. `Type=Number` 필드에 대해서만 메타데이터 필드 정의에 새 속성을 추가했습니다. 새 옵션은 숫자 필드를 `Type=Text` 필드와 연결하고 범위 설명이 작성되는 방식을 설명하는 구성 정보를 지정합니다.

   [새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)를 참조하십시오.

## 수정 사항 {#section_22D1AFC99F394D569898828A0D3C419D}

* 패싯 레일 편집 대화 상자에는 단계 패싯이 포함되어야 합니다.
* 일본어 문자를 포함하는 검색에 대해 &quot;포함된&quot; 검색 모드에 대한 빈 코어 검색 결과.
* 이제 Word .docx 파일의 Tika 변환이 `title` 속성을 채웁니다.
* **[!UICONTROL Banner]** 관리자에서 잘못된 &quot;중복된 배너&quot; 메시지를 수정했습니다.
* [!DNL Dynamic Media Classic] 배너는 이제 프로토콜에 상관없이 지원됩니다.
* 계정에 대해 **[!UICONTROL Dynamic Facets]**&#x200B;이(가) 활성화된 경우에도 메타데이터 사용자 정의 필드를 편집할 때 때로 **[!UICONTROL Table Name]** 필드 속성이 숨겨졌습니다.
* **[!UICONTROL Recent Searches]** 더 이상 ASCII가 아닌 문자를 곱하기 인코딩하지 않습니다.
* 스크립트 필터링에 의존하지 않고 MDI 필드를 채울 수 있습니다.
* 제안의 인코딩이 잘못되었습니다.
* 이제 복잡한 비즈니스 규칙에서 &quot;다른 패싯 선택&quot; 트리거가 올바르게 작동합니다.

