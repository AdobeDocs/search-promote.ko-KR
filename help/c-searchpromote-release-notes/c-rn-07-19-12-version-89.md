---
description: Search&amp;Promote 8.9 릴리스 노트.
solution: Target
title: Search&amp;Promote 8.9 릴리스 노트(07/19/2012)
topic: 릴리스 노트,사이트 검색 및 머천다이징
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 65%

---


# Search &amp; Promote 8.9 릴리스 노트(07/19/2012){#search-promote-release-notes}

**새로운 기능**

* 메타데이터 관리 개선 - 고객 피드에서 동적 메타데이터 정의

   스키마를 만들어 고객이 제공한 메타데이터 정의를 기준으로 Search&amp;Promote 계정으로 동적으로 다시 구성하십시오.
* 색인화 성능 개선 - 색인 로더

   색인 로더는 XML 컨텐트를 직접 Search&amp;Promote 색인에 가져오는 새로운 방법입니다. 이것은 표준 XML 피드 파일을 빨리 가져오도록 설계된 기존 Index Connector 기능의 하위 세트입니다.

**수정 사항 및 개선 사항**

* 비즈니스 규칙별 정렬 옵션 변경에 대한 지원 기능을 추가했습니다.
* 도움말 시스템 `<search-description>` 태그는 설명에 대한 메타 태그에 내용이 비어 있을 때 대신 본문을 표시합니다.
* 결과 기준 작업 방법으로 추가된 결과에 해당하는 표 히트를 추적하는 기능을 추가했습니다.
* POST를 통한 쿼리 매개 변수 제출에 대한 지원 기능을 추가했습니다
* 크롤링할 때 일부 경우에는 최종 mirror_account 작업을 건너뛸 수 있습니다.
* Adobe Analytics URL에는 URL 키에서 CGI 인수를 유사하게 스트립하는 데 필요한 Adobe Analytics 조회를 수행하는 Search &amp; Promote 코드와 CGI 인수가 없습니다.
* 다시 작성 규칙이 활성으로 푸시된 후 사용자 인터페이스에서 간헐적으로 사라졌습니다.
* 사용자가 의미했는지 설정을 사용하여 결과가 불량하여 제안을 하도록 설정한 Search &amp; Promote 계정에는 간헐적인 결과가 있을 수 있습니다.
* 다시 작성 규칙 테스트 출력에 줄 바꿈이 없습니다.
* URL 규칙 검색 페이지와 목록 저장소 URL 규칙 크롤링 페이지가 잘못된 내역 페이지를 가리켰습니다.
* 일부 배너에서 편집을 클릭해도 편집 페이지가 표시되지 않습니다.
* 때때로 업데이트 코드 등급을 다시 매기는 작업이 이례적으로 느릴 수 있습니다.
* 단면화 이름이 대소문자를 혼합해서 사용한 경우 단면화 항목 제거 또는 푸시가 작동하지 않았습니다.

