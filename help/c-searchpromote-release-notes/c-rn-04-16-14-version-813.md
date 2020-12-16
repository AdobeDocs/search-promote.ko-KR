---
description: 'null'
seo-description: 'null'
seo-title: Search&Amp;Promote 8.13.0 릴리스 노트(04/16/2014)
solution: Target
title: Search&Amp;Promote 8.13.0 릴리스 노트(04/16/2014)
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 57%

---


# Search &amp; Promote 8.13.0 릴리스 노트(04/16/2014){#search-promote-release-notes}

| 새로운 기능 및 향상된 기능 | 설명 |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 전체 테이블 일치 지원이 되는 다이내믹 패싯 | 일부 고객은 다이내믹 패싯을 통해 선택하고 표시하고자 하는 &quot;SKU 수준&quot; 속성이 많습니다. 예를 들어, 이제는 원할 경우 각각의 다이내믹 패싯 필드를 정적 계정 구성에서 최대 하나의 테이블 이름과 연결할 수 있습니다. 이렇게 연결된 테이블 관계는 검색에 관련된 다이내믹 패싯 필드에 대해 검색 시 적용할 수 있습니다. [동적 팩트 정보](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)를 참조하십시오. |

**수정 사항**

* `<search-description>` 대신 `<search-display-field>` 태그를 사용하도록 데이터 보기 설명 필드를 변경했습니다.
* 기본 키를 두 개 이상의 필드에 대한 연결로 만들기 위해 색인 커넥터에 기능을 추가했습니다.
* AttributeLoader-Regen-Enabled 스크립트 `attributeloader-regen.pl`을 변경하여 값을 HTML로 인코딩하지 않도록 했습니다.
* &quot;범위 검색&quot; 쿼리에 대해 색인 작성 시와 검색 시의 공백 처리를 일치시켰습니다.
* 다이내믹 패싯이 활성화되어 있을 때 비즈니스 규칙을 추가하면 때로 오류가 발생했습니다.

   [비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

* Javascript 오류로 인해 **설정** > **SPIN** > **IndexConnector**&#x200B;에서 정의를 추가하거나 편집할 수 없었습니다.
* 비즈니스 규칙을 저장한 후에는 비즈니스 규칙 생성 중에 시간을 선택하면 GMT 표준 시간대로 기본 설정되는 것으로 나타났습니다. 저장한 후에는 계정의 표준 시간대가 적용되는 것으로 나타났습니다.

   [비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

* 스테이징 서버에서 비즈니스 규칙이 제대로 정렬되지 않았습니다.

   [비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

* 검색 실적 보고는 이메일 배달을 위해 보고서를 예약하는 기능을 제공하는 향상된 기능입니다.
* 비즈니스 규칙 수정 일정은 일광 절약 시간으로 자동으로 변경되었습니다.

   [비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

* 많은 수의 동적 패싯 필드가 정의된 경우, 사용자는 코어 검색 응답 시간이 느려졌습니다.
* 잘못된 범위 색인 오류가 발생했습니다.
* 북미가 아닌 지역에 있는 데이터 센터의 Dynamic Media Classic 액세스가 손상되었습니다.
* SPIN XPath 유효성 검증 기능에서 오류가 아닌 항목을 오류로 반환했습니다.

* SPIN 활성화/비활성화 작업 후에 사용자가 구성원 센터 로그인 페이지로 리디렉션되었습니다.

