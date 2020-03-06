---
description: 스테이징을 사용하면 라이브 색인에 영향을 주지 않고 설정 및 구성 변경 사항을 테스트하고 미리 볼 수 있습니다.
seo-description: 스테이징을 사용하면 라이브 색인에 영향을 주지 않고 설정 및 구성 변경 사항을 테스트하고 미리 볼 수 있습니다.
seo-title: 스테이징 정보
solution: Target
title: 스테이징 정보
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 스테이징 정보{#about-staging}

스테이징을 사용하면 라이브 색인에 영향을 주지 않고 설정 및 구성 변경 사항을 테스트하고 미리 볼 수 있습니다.

## 스테이징 정보 {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

스테이징을 사용하면 라이브 색인에 영향을 주지 않고 설정 및 구성 변경 사항을 테스트하고 미리 볼 수 있습니다.

요소 [ID:context_A5783D07C72042EC8886F300FFF62C50을 참조하십시오](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

스테이징 옵션이 **[!UICONTROL Push All Live]** 있거나 **[!UICONTROL View Live Settings]** 해당 페이지의 모든 설정을 스테이징할 수 있는 모든 페이지입니다. 예외는 색인의 웹 페이지입니다. 이 영역의 페이지는 스테이지된 색인이나 라이브 색인에 대해 명시적으로 두 개의 인덱스를 독립적으로 직접 제어할 수 있습니다.

색인을 포함한 거의 모든 것을 스테이징할 수 있습니다. 일부 예외에는 스테이징과 라이브 환경에 동시에 영향을 주는 계정 특정 설정과 인덱싱 작업 예약이 포함됩니다. 기본적으로 스테이징할 수 있는 설정에 대한 변경 사항을 저장하면 자동으로 스테이징됩니다.

또는 **[!UICONTROL Push All Live]** **[!UICONTROL View Lives Settings]** 옵션이 활성화(흐리게 표시됨)되지 않은 경우 해당 페이지의 스테이지 설정이 라이브 설정과 동일함을 의미합니다.

스테이징된 항목의 경우 설정의 라이브 버전은 읽기 전용입니다.스테이지 설정을 라이브로 푸시하여 조작할 수 있습니다.

## 스테이지 페이지의 내역 정보 {#section_5BE780AFF26A450A9EFF4000DE53531B}

대부분의 준비 설정에는 페이지의 오른쪽 위 영역에 옵션이 [!DNL History] 있습니다. 클릭하면 **[!UICONTROL History]**&#x200B;최근에 열어 본 특정 단계 페이지에 대한 변경 사항을 되돌릴 수 있습니다.

또한 변경 로그를 통해 내역의 다른 보기를 볼 수도 있습니다. 변경 사항이 적용될 때마다 기본 데이터 파일의 백업 버전이 만들어집니다. 변경 로그에는 버전 번호, 변경 작업을 수행한 사용자의 전자 메일 주소 및 백업이 수행된 날짜가 표시되어 있습니다. 굵은 버전 값이 있는 항목은 현재 버전을 나타냅니다.

See [Viewing the Change Log](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## 스테이지 라이브 설정 관리 페이지 {#section_E72B8CAF516345A5B6B6783CF6E512EE}

지정된 페이지 내에서 바로 **[!UICONTROL Push All Live]** 및 **[!UICONTROL View Live Settings]** 옵션을 제공하는 것 외에도 **[!UICONTROL Manage Stage-Live Settings]** 페이지를 사용하여 동일한 작업을 수행할 수도 있습니다. 기본 제품 메뉴에서 사용할 수 있는 **[!UICONTROL Manage Stage-Live Settings]** 페이지는 현재 스테이징된 계정의 모든 설정을 보여주는 중앙 위치입니다. 모든 설정을 실시간으로 푸시하거나 선택한 설정만 라이브로 푸시하거나 설정을 삭제할 수 있습니다. 그러나 상호 의존성 문제가 발생하지 않도록 항상 모든 단계 항목을 라이브로 푸시하는 것이 좋습니다.

페이지의 설정은 카테고리로 그룹화됩니다. 각 카테고리를 확장하여 어떤 페이지의 설정이 준비되었는지 표시할 수 있습니다. 현재, 종속성은 스테이지 관리자 내에서 추적되지 않습니다. 따라서 색인을 제외하고 모든 내용을 한 번에 라이브하는 것이 좋습니다.

스테이지된 인덱스를 라이브로 푸시할 수 있습니다. 먼저 스테이지된 인덱스가 오래되었거나 손상되지 않았는지 확인하십시오. 실수로 스테이지된 인덱스를 라이브로 푸시하면 이전 라이브 인덱스를 롤백할 수 있습니다. 스테이지 인덱스를 라이브로 푸시하는 데에는 일반적으로 30초 미만이 소요됩니다.

## 스테이지 설정 또는 인덱스 테스트 {#section_6800E52D20854A779946EAB600801F12}

테스트 컨트롤을 지원하는 페이지에서 스테이지드 또는 라이브 설정에 대해 테스트할 수 있습니다. 단계 설정을 보면 스테이지된 설정이 테스트에 사용됩니다. 마찬가지로 라이브 설정을 볼 때 테스트에 라이브 설정이 사용됩니다. 템플릿 섹션에서 모든 테스트는 스테이지된 버전의 인덱스에 대해 수행됩니다. 스테이지된 인덱스를 검색하려면 CGI `sp_staged` 매개 변수를 1로 설정합니다. 이렇게 하면 스테이지된 인덱스를 사용할 것임을 나타냅니다. 스테이지된 인덱스가 없는 경우 라이브 인덱스가 검색되고 준비된 검색 시간 설정이 적절히 적용됩니다.

백엔드 [검색 CGI 매개 변수를](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)참조하십시오.

## 라이브 설정 보기 {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

모든 단계 페이지에서 설정의 라이브 버전을 검토할 수 있습니다.

<!-- 

t_viewing_live_settings.xml

 -->

옵션이 활성화(흐리게 표시됨)되지 않으면 해당 페이지에 대한 스테이지 설정과 라이브 설정이 이미 동기화되었음을 의미합니다. **[!UICONTROL View Live Settings]**

**라이브 설정을 보려면**

1. 스테이지된 설정이 있는 페이지에서 을 클릭하여 설정의 라이브 버전을 **[!UICONTROL View Live Settings]** 봅니다.
1. 원하는 경우 다음 중 하나를 수행합니다.

   * 단계 설정에 대해 선택한 현재 옵션을 **[!UICONTROL View]** 보려면 을 클릭합니다.
   * 설정을 편집하거나 삭제할 수 **[!UICONTROL View Stage Settings]** 있는 준비 설정으로 돌아가려면 을 클릭합니다.

## 스테이지 설정 라이브 푸시 {#task_44306783B4C0408AAA58B471DAF2D9A4}

모든 스테이지 페이지 보기 또는 중앙 **[!UICONTROL Manage Stage-Live Settings]** 페이지에서 설정을 실시간으로 푸시할 수 있습니다.

<!-- 

t_pushing_live_settings_live.xml

 -->

페이지에서 옵션이 활성화(흐리게 표시되지 않음)되면 스테이징된 설정이 있음을 의미합니다. **[!UICONTROL Push Live]** 또는 설정에 편집 내용이 있고 저장하면 설정이 스테이징이 됩니다. 이 옵션을 클릭하면 저장되지 않은 편집 내용이 준비 단계 영역에 저장됩니다. 보류 중인 편집이 없으면 페이지의 설정이 즉시 라이브로 푸시됩니다.

**스테이지 설정을 라이브로 푸시하려면**

1. 다음 중 하나를 수행하십시오.

   * &quot;스테이지&quot;가 보기로 선택된 모든 페이지에서 을 클릭합니다. **[!UICONTROL Push Live]**
   * 제품 메뉴에서 을 클릭합니다 **[!UICONTROL Staging]**. 페이지에서 **[!UICONTROL Manage Stage-Live Settings]** 다음 중 하나를 수행합니다.

   * 설정 트리를 사용하여 라이브로 푸시할 설정만 확인한 다음 을 클릭합니다 **[!UICONTROL Push Selected Live]**.
   * 클릭 **[!UICONTROL Push All Live]**.

## 중앙 위치에서 스테이지 라이브 설정 삭제 {#task_B72BEA9269704B1399600A9CA273369B}

삭제할 많은 설정이 있는 경우 **[!UICONTROL Manage Stage-Live Settings]** 페이지를 사용하여 중앙 위치에서 설정을 삭제할 수 있습니다.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**경고**:클릭하면 **[!UICONTROL Delete Selected]**&#x200B;선택한 모든 설정이 즉시 삭제됩니다.선택한 설정을 삭제할 것인지 확인하는 확인 대화 상자가 없습니다. 또한 페이지와 연결된 작업 내역 기능은 없습니다. 따라서 삭제 작업은 실행 취소할 수 없습니다.

**중앙 위치에서 스테이지 라이브 설정을 삭제하려면**

1. 제품 메뉴에서 을 클릭합니다 **[!UICONTROL Staging]**.
1. 페이지에서 **[!UICONTROL Manage Stage-Live Settings]** 설정 트리를 사용하여 삭제할 설정만 확인합니다.
1. 클릭 **[!UICONTROL Delete Selected]**.