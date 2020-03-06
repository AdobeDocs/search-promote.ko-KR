---
description: 고객이 검색 쿼리를 입력할 때 사용자가 정의한 구 주위에 따옴표를 입력할 필요가 없도록 웹 사이트에서 사용되는 일반 구문을 정의할 수 있습니다.
seo-description: 고객이 검색 쿼리를 입력할 때 사용자가 정의한 구 주위에 따옴표를 입력할 필요가 없도록 웹 사이트에서 사용되는 일반 구문을 정의할 수 있습니다.
seo-title: 일반 구문 정보
solution: Target
title: 일반 구문 정보
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: 8efa90ac2927b263b7d48ccbf25d4b0e917dac79

---


# 일반 구문 정보{#about-common-phrases}

고객이 검색 쿼리를 입력할 때 사용자가 정의한 구 주위에 따옴표를 입력할 필요가 없도록 웹 사이트에서 사용되는 일반 구문을 정의할 수 있습니다.

## 일반 구문 사용 {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>일반 구문 기능은 기본적으로 활성화되지 않으므로 사용자 인터페이스에 표시되지 않습니다. 이 기능을 사용하려면 기술 지원에 문의하십시오.

일반 구문은 고객의 검색 중에 인식되는 여러 단어로 된 구문의 모음입니다. 이 용어는 구문을 개별 단어 대신 결합된 단어 그룹으로 처리합니다. 고객이 웹 사이트에서 검색 쿼리를 입력하면 &quot;Pacific Ocean&quot;과 같은 큰 따옴표로 용어를 둘러싸서 구문을 식별할 수 있습니다. 그러나 일반 구문 그룹을 추가하면 고객이 검색 쿼리에서 일치하는 구문을 찾을 때 인용 부호 단계가 자동으로 수행됩니다.

예를 들어, 웹 사이트 고객이 다음 검색 쿼리를 입력한다고 가정합니다.

`hotels near the pacific ocean`

따옴표를 붙이지 않으면 고객의 검색 결과는 `pacific ocean`고객이 의도한 바가 아닌 세계 어느 곳에도 있는 호텔에 대한 결과를 얻게 됩니다.

하지만 &quot;태평양&quot;이라는 일반적인 구문을 추가하면 해당 검색 쿼리가 자동으로 다음 항목으로 변환됩니다.

`hotels near the "pacific ocean"`

공통 구문을 사용하면 고객이 단어 구문에 대한 인용 부호를 명시적으로 사용하지 못하도록 할 수 없습니다. 대신 정의된 구문이 검색 쿼리에서 발견되면 인용 부호가 추가됩니다.

이 검색 쿼리 확장은 백엔드 검색 CGI 매개 변수 `sp_q` 및 `sp_q_#`

백엔드 검색 CGI 매개 변수의 [](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)표 행 25, 26 및 32를 참조하십시오.

## 일반 구문 그룹 추가 {#task_35C84FABCD9042C5B48C5C788B752871}

공통 구문 그룹을 추가하여 검색 쿼리가 고객이 입력한 정확한 순서와 근접 순서로 모든 단어가 포함된 웹 페이지를 정확하게 반환할 수 있습니다.

일반 구문 그룹을 추가할 때 기본 일반 구문 그룹 페이지에서 찾기 기능을 사용할 수 있습니다. 찾기 기능을 사용하면 기존 구문을 검색하고 해당 구문이 속한 그룹을 확인할 수 있습니다.

구문의 [특정 단어가 들어 있는 그룹 찾기를 참조하십시오](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**일반 구문 그룹을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지에서 구문 그룹 [!DNL Common Phrases Groups] 추가를 클릭합니다 ****.
1. 페이지에서 원하는 옵션을 설정하고 그룹을 구성하는 모든 구문을 추가합니다. [!DNL Add Common Phrase Group]

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
      <td colname="col2"> <p>필수. </p> <p>일반 구문 그룹의 고유한 이름입니다. </p> <p>나중에 일반 구문 그룹을 편집하는 경우 그룹 이름은 변경할 수 없습니다. 그룹 이름을 변경하려면 이름 변경 <span class="uicontrol"> 기능을 사용합니다</span> . </p> <p>일반 <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> 구문 그룹 이름 변경을 참조하십시오</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>참고 </p> </td> 
      <td colname="col2"> <p>선택적. </p> <p>일반 구문 그룹과 관련된 정보를 추가합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구문 </p> </td> 
      <td colname="col2"> <p>필수. </p> <p>최대 5개의 단어까지 구문을 지정할 수 있습니다. 최대 단어 설정을 조정하려면 기술 지원에 문의하십시오. </p> <p>입력하는 각 구문은 모든 일반 구문 그룹 내에서 고유해야 합니다. </p> <p>작업 열의 더하기(+) 및 빼기(-) 아이콘을 사용하여 입력한 구문을 추가하거나 구문을 삭제합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. **추가를 클릭합니다**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 일반 구문 테스트 {#task_A0C344E051CA45A9A0588242F9DA675D}

구문 그룹과 연결할 메타데이터 필드를 선택한 경우 특정 구문의 확장을 테스트할 수 있습니다.

구문의 확장을 테스트할 때 구문 그룹과 연관된 메타데이터 필드에 대해 정확한 구문을 검색합니다. 그 구문은 주위에 따옴표가 있는 것처럼 검색됩니다. 다른 모든 메타데이터 필드는 따옴표 없이 구문 내의 단어만 검색합니다. 예를 들어 구문을 테스트했다고 `audi TT`가정합니다. 반환된 결과는 다음과 같이 나타날 수 있습니다.

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**일반 구문을 테스트하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지의 텍스트 [!DNL Common Phrases Groups] 필드가 포함된 **테스트 구문에서 테스트할 메타데이터 확장명을 포함하는** 구문을 입력합니다.
1. 클릭 **[!UICONTROL Test]**.

   확장 결과가 텍스트 상자에 표시됩니다.
1. (선택 사항) 텍스트 상자의 오른쪽 아래 모서리를 드래그하여 표시 영역을 확장합니다.

## 구문에 특정 단어가 들어 있는 검색 그룹 {#task_20714969274740A7BB4DC71E705EA15E}

를 [!DNL Find] 사용하여 추가한 모든 기존 그룹 중에서 구문의 특정 단어를 검색할 수 있습니다.

[찾기]를 사용하면 다음 항목이 제거됩니다.

* 모든 그룹에서 정확히 동일한 구문을 찾을 수 있습니다.
* 구문의 단어 순서와 근접성에 관계없이 모든 그룹 사이에 있는 단어 중 하나라도 있습니다.

일반 [구문 그룹 편집을 참조하십시오](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61).

**구문에 특정 단어가 들어 있는 그룹을 찾으려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Common Phrases Groups] 텍스트 **[!UICONTROL Find groups with phrases that contain]** 필드에 구문을 입력합니다.
1. 클릭 **[!UICONTROL Find]**.

   텍스트 상자에 결과가 표시됩니다.
1. (선택 사항) 다음 중 하나 이상을 수행합니다.

   * 텍스트 상자의 오른쪽 아래 모서리를 드래그하여 표시 영역을 확장합니다.
   * 결과 창에서 하이퍼링크 구문을 클릭하여 연관된 그룹의 공통 구문 그룹 편집 페이지를 엽니다.

## 일반 구문 그룹 편집 {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

추가한 일반 구문 그룹의 기존 필드, 메모 및 구문을 편집할 수 있습니다. 하지만 그룹 이름을 편집하려면 해당 [!DNL Rename] 기능을 사용해야 합니다.

일반 [구문 그룹 이름 바꾸기를 참조하십시오](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB).

**일반 구문 그룹을 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지에서 그룹 이름의 맨 오른쪽에 [!DNL Common Phrases Groups] **[!UICONTROL Edit]** 있는 곳을 클릭합니다.
1. 페이지에서 원하는 옵션을 [!DNL Edit Common Phrase Group] 설정합니다.

   일반 구문 그룹 추가 아래의 [옵션 표를 참조하십시오](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871).
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 일반 구문 그룹 이름 바꾸기 {#task_168E07C59C0F40989D43E7010EFF22EB}

기존 일반 구문 그룹의 이름을 변경할 수 있습니다. 그러나 일반 구문 그룹의 기존 필드, 메모 및 구문을 변경하려는 경우 이 [!DNL Edit] 기능을 사용해야 합니다.

일반 [구문 그룹 편집을 참조하십시오](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) .

**일반 구문 그룹 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지에서 그룹 이름의 맨 오른쪽에 [!DNL Common Phrases Groups] **[!UICONTROL Rename]** 있는 곳을 클릭합니다.
1. 페이지의 [!DNL Rename Common Phrase Group] 텍스트 **[!UICONTROL Group Name]** 필드에 그룹의 새 이름을 입력합니다.
1. 이름 **변경을 클릭합니다**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 일반 구문 그룹 삭제 {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

추가한 모든 일반 구문 그룹을 삭제할 수 있습니다. 실수로 그룹을 삭제한 경우 그룹을 복원하는 [!DNL History] 데 사용할 수 있습니다.

작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

**일반 구문 그룹을 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**&#x200B;을 클릭합니다.
1. 페이지에서 그룹 이름의 맨 오른쪽에 [!DNL Common Phrases Groups] **[!UICONTROL Delete]** 있는 곳을 클릭합니다.
1. 페이지에서 [!DNL Delete Common Phrase Group] 을 클릭합니다 **[!UICONTROL Delete]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

