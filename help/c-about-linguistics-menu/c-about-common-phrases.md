---
description: 고객이 검색 쿼리를 입력할 때 사용자가 정의한 구 주위에 따옴표를 입력할 필요가 없도록 웹 사이트에서 사용되는 일반 구문을 정의할 수 있습니다.
solution: Target
title: 일반 구문 정보
topic: 언어학,사이트 검색 및 상품 판매
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---


# 일반 구문 정보{#about-common-phrases}

고객이 검색 쿼리를 입력할 때 사용자가 정의한 구 주위에 따옴표를 입력할 필요가 없도록 웹 사이트에서 사용되는 일반 구문을 정의할 수 있습니다.

## 일반 구문 사용 {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>일반 구문 기능은 기본적으로 활성화되지 않으므로 사용자 인터페이스에 표시되지 않습니다. 이 기능을 사용하려면 기술 지원에 문의하십시오.

일반 구문은 고객이 검색하는 동안 인식되는 여러 단어로 된 구문의 모음입니다. 이 용어는 구문을 개별 단어 대신 결합된 단어 그룹으로 처리합니다. 고객이 웹 사이트에서 검색 쿼리를 입력하면 &quot;태평양&quot;과 같은 큰 따옴표를 사용하여 용어를 둘러싸서 구문을 식별할 수 있습니다. 그러나 일반 구문 그룹을 추가할 때 검색 쿼리에서 일치하는 구문을 찾을 때 인용 부호 단계가 자동으로 수행됩니다.

예를 들어 웹 사이트에 대한 고객이 다음 검색 쿼리를 입력한다고 가정합니다.

`hotels near the pacific ocean`

`pacific ocean`에 따옴표를 추가하지 않은 경우 고객의 검색 결과는 세계 어느 해양 호텔에서도 고객이 의도한 바가 아닌 결과를 반환합니다.

그러나 일반적인 구문 &quot;태평양&quot;을 추가하면 검색 쿼리가 자동으로 다음 항목으로 변환됩니다.

`hotels near the "pacific ocean"`

일반 구문 사용은 고객이 단어 구문에 대한 인용 부호를 명시적으로 사용하는 것을 배제하지 않습니다. 대신 검색 쿼리에서 정의된 구문이 발견되면 간단히 인용 부호를 추가합니다.

이 검색 쿼리 확장은 백엔드 검색 CGI 매개 변수 `sp_q` 및 `sp_q_#`,

[백엔드 검색 CGI 매개 변수](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)의 표 행 25, 26 및 32를 참조하십시오.

## 일반 구문 그룹 {#task_35C84FABCD9042C5B48C5C788B752871} 추가

공통 구문 그룹을 추가하여 검색 쿼리가 고객이 입력한 정확한 순서와 근접 위치에 모든 단어가 포함된 웹 페이지를 정확하게 반환하도록 할 수 있습니다.

일반 구문 그룹을 추가할 때 기본 일반 구문 그룹 페이지에서 찾기 기능을 사용할 수 있습니다. 찾기 기능을 사용하면 기존 구문을 검색하고 해당 구문이 상주하는 그룹을 확인할 수 있습니다.

[구문](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E)에 특정 단어가 포함된 그룹 찾기를 참조하십시오.

**일반 구문 그룹을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지에서 **구문 그룹 추가**&#x200B;를 클릭합니다.
1. [!DNL Add Common Phrase Group] 페이지에서 원하는 옵션을 설정하고 그룹을 구성하는 모든 구문을 추가합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>그룹 이름 </p> </td> 
      <td colname="col2"> <p>필수. </p> <p>공통 구문 그룹의 고유한 이름입니다. </p> <p>나중에 일반 구문 그룹을 편집하는 경우 그룹 이름은 변경할 수 없습니다. 그룹 이름을 변경하려면 <span class="uicontrol"> 이름 바꾸기</span> 기능을 사용합니다. </p> <p><a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> 일반 구문 그룹 이름 바꾸기</a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>참고 </p> </td> 
      <td colname="col2"> <p>선택적. </p> <p>일반 구문 그룹과 관련된 정보를 추가합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구문 </p> </td> 
      <td colname="col2"> <p>필수. </p> <p>최대 5단어까지 구문을 지정할 수 있습니다. 최대 단어 설정을 조정하려면 기술 지원 팀에 문의하십시오. </p> <p>입력하는 각 구문은 공통 구문 그룹 내에서 고유해야 합니다. </p> <p>작업 열의 더하기(+) 및 빼기(-) 아이콘을 사용하여 입력한 구문을 추가하거나 구문을 삭제합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. **추가를 클릭합니다**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 일반 구문 테스트 {#task_A0C344E051CA45A9A0588242F9DA675D}

구문 그룹과 연관되도록 메타데이터 필드를 선택한 경우 특정 구문의 확장을 테스트할 수 있습니다.

구문 확장을 테스트할 때 구문 그룹과 연관된 메타데이터 필드에 대해 정확한 구문을 검색합니다. 그 구문은 주위에 인용 부호가 있는 것처럼 검색된다. 다른 모든 메타데이터 필드는 따옴표 없이 구문 내의 단어만 검색합니다. 예를 들어 구문 `audi TT`을 테스트했다고 가정합니다. 반환된 결과는 다음과 같이 나타날 수 있습니다.

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**일반 구문을 테스트하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지의 **테스트 구문에** 텍스트 필드가 포함된 테스트 구문에 테스트할 메타데이터 확장명을 포함하는 구문을 입력합니다.
1. 클릭 **[!UICONTROL Test]**.

   확장 결과가 텍스트 상자에 표시됩니다.
1. (선택 사항) 텍스트 상자의 오른쪽 아래 모서리를 드래그하여 표시 영역을 확장합니다.

## 구문 {#task_20714969274740A7BB4DC71E705EA15E}에 특정 단어가 들어 있는 그룹 찾기

[!DNL Find]을 사용하여 추가한 모든 기존 그룹 중에서 구문의 특정 단어를 검색할 수 있습니다.

[찾기]를 사용하면 다음과 같은 위치를 찾습니다.

* 모든 그룹 중에서 정확히 동일한 구문을 찾을 수 있는 곳입니다.
* 구문의 단어 순서와 구문의 근접성에 상관없이 모든 그룹 사이에 있는 모든 단어

[일반 구문 그룹 편집](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)을 참조하십시오.

**구문에 특정 단어가 들어 있는 그룹을 찾으려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지의 **[!UICONTROL Find groups with phrases that contain]** 텍스트 필드에 구문을 입력합니다.
1. 클릭 **[!UICONTROL Find]**.

   결과가 텍스트 상자에 표시됩니다.
1. (선택 사항) 다음 중 하나 이상을 수행합니다.

   * 텍스트 상자의 오른쪽 아래 모서리를 드래그하여 표시 영역을 확장합니다.
   * 결과 창에서 하이퍼링크된 구문을 클릭하여 연관된 그룹의 공통 구문 그룹 편집 페이지를 엽니다.

## 일반 구문 그룹 편집 {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

추가한 일반 구문 그룹의 기존 필드, 메모 및 구문을 편집할 수 있습니다. 그러나 그룹 이름을 편집하려면 [!DNL Rename] 기능을 사용해야 합니다.

[일반 구문 그룹 이름 바꾸기](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB)도 참조하십시오.

**일반 구문 그룹을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지에서 그룹 이름의 맨 오른쪽에 있는 **[!UICONTROL Edit]**&#x200B;을 클릭합니다.
1. [!DNL Edit Common Phrase Group] 페이지에서 원하는 옵션을 설정합니다.

   [공통 구문 그룹 추가](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871)의 옵션 표를 참조하십시오.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 일반 구문 그룹 이름 바꾸기 {#task_168E07C59C0F40989D43E7010EFF22EB}

기존 공통 구문 그룹의 이름을 변경할 수 있습니다. 그러나 일반 구문 그룹의 기존 필드, 메모 및 구문을 변경하려면 [!DNL Edit] 기능을 사용해야 합니다.

[일반 구문 그룹 편집](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)을 참조하십시오.

**일반 구문 그룹 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지에서 그룹 이름의 맨 오른쪽에 있는 **[!UICONTROL Rename]**&#x200B;을 클릭합니다.
1. [!DNL Rename Common Phrase Group] 페이지의 **[!UICONTROL Group Name]** 텍스트 필드에 그룹의 새 이름을 입력합니다.
1. **이름 바꾸기**&#x200B;를 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 일반 구문 그룹 {#task_4106D282A2ED4A27B09EE5A8CAAEDA36} 삭제

추가한 모든 일반 구문 그룹을 삭제할 수 있습니다. 실수로 그룹을 삭제하는 경우 [!DNL History]을 사용하여 그룹을 복원할 수 있습니다.

[작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

**일반 구문 그룹을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. [!DNL Common Phrases Groups] 페이지에서 그룹 이름의 맨 오른쪽에 있는 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. [!DNL Delete Common Phrase Group] 페이지에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

