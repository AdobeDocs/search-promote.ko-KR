---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 8.16.0 릴리스 노트(2014년 9월 18일)
solution: Target
title: Search&amp;Promote 8.16.0 릴리스 노트(2014년 9월 18일)
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.16.0 Release Notes (9/18/2014){#search-promote-release-notes}

## Search&amp;Promote 8.16.0 Release Notes (9/18/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## New features {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* 검색 안내 3(GS3)에서 검색 결과 캐싱 - 계정에서 사용할 수 있도록 이 사용자 정의 기능을 자동으로 설정하려면 Adobe 기술 계정 관리자에게 문의하십시오.
* 자주 변경되는 필드에 대한 수직 업데이트 - 이제 컨텐츠를 완전히 다시 색인화할 필요 없이 메타데이터 필드 세트에 대한 모든 값을 신속하게 업데이트할 수 있습니다.

   새 메타 태그 필드 [추가 및 수직 업데이트](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) 정보의 표에서 수직 업데이트 필드 옵션을 [참조하십시오](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   This feature can only be used on [!DNL Adobe Search&Promote] accounts that use Index Connector. 이 사용자 지정 기능을 계정에서 사용할 수 있도록 자동으로 설정하려면, Adobe 기술 계정 관리자에게 문의하십시오.

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* Corrected the Index Connector parsing of XML feeds that contained `?>` string.
* 최소 문서 개수 적용 시 색인 커넥터 SFTP 피드를 수정했습니다.
* 이제 Microsoft Excel로 보고서 내보내기에서 UTF8을 지원합니다.
* Guided Search: 패싯 컴파일이 지연되었습니다.
* 속성 로더: 수집 데이터에 중복 키가 있었습니다.
* 개별 규칙을 라이브로 적용할 때의 잘못된 비즈니스 규칙 실행 순서를 수정했습니다.
* 잘못된 패싯 실행 취소 링크가 Guided Search에 의해 생성되었습니다.
* 현재 실행 중인 색인 크롤의 진도와 상태를 확인할 수 있도록 해주는 새로운 원격 제어 작업을 추가했습니다(`sp_lines=N`).

   인덱싱을 [위한 원격 제어 정보를 참조하십시오](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* 색인 커넥터 증분 시 가져오기를 하면 정보가 삭제될 때 인증 정보를 보내야 합니다.
* The [!DNL Change Log] report now identifies the user who initiates a manual index operation.

   See [Viewing the Change Log](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* When you export a [!DNL Terms Report], you are no longer limited to 500 or less items in the report.

   용어 [보고서 보기 또는 Null 검색어 보고서 보기...를 참조하십시오.](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* The Index Connector **[!UICONTROL Strip HTML]** setting was always displaying as checked.
* Inconsistent search results were experienced with the **[!UICONTROL Common Phrases]** feature.
* 속성 이름 표시가 규칙 목록 요약에서 잘렸습니다.
* 개별 비즈니스 규칙을 라이브로 적용하면 모든 비즈니스 규칙이 라이브로 적용됩니다.

