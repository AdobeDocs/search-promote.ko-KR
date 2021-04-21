---
description: 증분 색인을 사용하여 자주 변경되는 페이지의 컬렉션과 같이 라이브 또는 스테이징 웹 사이트의 "조각"을 색인화할 수 있습니다.
solution: Target
subtopic: Incremental Index
title: 증분 색인 정보
topic-legacy: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
exl-id: 41943f84-23f0-434c-8eef-a9075dd5c03d
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 1%

---

# 증분 인덱스 정보{#about-incremental-index}

증분 색인을 사용하여 자주 변경되는 페이지의 컬렉션과 같이 라이브 또는 스테이징 웹 사이트의 &quot;조각&quot;을 색인화할 수 있습니다.

## 증분 인덱스 사용 {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

증분 인덱스는 수행하는 데 단 몇 초 걸리고 전체 색인에 많은 시간이 걸릴 수 있는 대용량 웹 사이트에서 유용합니다.

증분 색인을 생성할 때 색인 작성 프로세스 동안 시작 시간, 경과 시간 및 오류와 같은 상태 정보가 표시됩니다. 마지막 인덱스의 상태에 대한 정보도 표시됩니다.

언제든지 증분 인덱싱 프로세스를 중지하거나 다시 시작할 수 있습니다.

라이브 웹 사이트에 대한 새로운 증분 색인 빌드가 작성되지만 고객은 마지막 증분 색인을 사용하여 사이트를 계속 검색할 수 있습니다.

## 단계 웹 사이트 {#task_46A367B0786C4C90BFFA5D3F95FD86C0}의 증분 색인 구성

웹 사이트 URL 및 URL 마스크를 지정하여 증분 색인에 포함할 웹 사이트 페이지를 구성할 수 있습니다.

**단계 웹 사이트의 증분 인덱스를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Incremental Index Configuration]** 페이지에서 다양한 필드를 사용하여 색인화할 페이지를 지정합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>필드 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL 추가 또는 업데이트 </p> </td> 
      <td colname="col2"> <p>URL을 지정합니다. </p> <p>검색 로봇은 마지막으로 색인화한 이후 변경된 지정된 문서만 인덱싱합니다. </p> <p>또한 검색 로봇은 지정된 문서에 포함된 링크를 따르고 변경된 문서만 인덱싱합니다. </p> <p>이 필드는 다음 예제와 같이 마스크가 아닌 문서 URL만 포함해야 합니다. </p> <p> 
        <code>
          https://www.mydomain.com/products/new.html 
        </code> </p> <p>URL에 다음 키워드를 사용할 수 있습니다. </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <code>
            noindex 
          </code> <p>지정된 URL과 일치하는 페이지의 텍스트를 색인화하지 않고 페이지의 링크를 따르려면 
            다음 예와 같이 URL 뒤에 <code>
              noindex 
            </code> 있습니다. </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html noindex 
            </code> </p> <p>반드시 따로 
            공백이 있는 URL의 <code>
              noindex 
            </code>;쉼표는 유효한 구분 기호가 아닙니다. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <code>
            nofollow 
          </code> <p>지정된 URL과 일치하는 페이지의 텍스트를 색인화하지만 페이지의 링크를 따라가지 않으려면 
            다음 예와 같이 URL 뒤에 <code>
              nofollow 
            </code> 있습니다. </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html nofollow 
            </code> </p> <p> 반드시 따로 
            공백이 있는 URL의 <code>
              nofollow 
            </code>;쉼표는 유효한 구분 기호가 아닙니다. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL 마스크 찾기 및 업데이트 </p> </td> 
      <td colname="col2"> <p>전체 경로, 부분 경로 또는 와일드카드 또는 정규 표현식을 사용하는 경로 등 간단한 URL 마스크를 지정합니다. </p> <p>검색 로봇은 일치하는 모든 문서를 검색하고 마지막으로 색인화한 이후 변경된 문서만 인덱싱합니다. </p> <p>또한 검색 로봇은 일치하는 문서 내에 포함된 링크를 따르고 변경된 페이지만 인덱싱합니다. 예: </p> <p> 
      <code>
        https://www.mydomain.com/products/household/*.html 
      </code> </p> <p>다음 예제와 같이 정규 표현식을 사용할 수도 있습니다. </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </code> </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식</a>을 참조하십시오. </p> <p>키워드를 사용할 수도 있습니다 
      <code>
        nofollow 
      </code> 및 
      위의 <span class="uicontrol"> URL </span>을(를) 추가하거나 업데이트합니다.<code>
        noindex 
      </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL 마스크 포함 및 제외 </p> </td> 
      <td colname="col2"> <p>전체 경로, 부분 경로 또는 와일드카드 또는 정규 표현식을 사용하는 경로 등 간단한 URL 포함 또는 제외 마스크를 지정합니다. </p> <p>검색 로봇은 지정된 마스크 유형에 따라 문서를 찾아서 인덱싱하거나("include") 문서를 무시합니다("exclude"). </p> <p> 사이트를 색인화할 때 나타나는 순서대로 지침이 적용됩니다. 예를 들어 다음 마스크 목록을 참조하십시오. </p> <p> 
      <code>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </code> </p> <p> 
      <code>
        exclude https://www.mydomain.com/products/ 
      </code> </p> <p>페이지를 인덱싱합니다. 
      <code>
        lightbulbs1.html 
      </code> 및 
      <code>
        lightbulbs2.html 
      </code>. 하지만 제품 디렉토리 아래에 나열된 다른 페이지는 색인화하지 않습니다. </p> <p>먼저 나타나는 URL 마스크는 항상 목록에 나중에 나타나는 마스크보다 우선합니다. 또한 검색 로봇이 포함 마스크와 제외 마스크와 일치하는 문서가 발견되면 먼저 나열된 마스크가 우선합니다. </p> <p>키워드를 사용할 수도 있습니다 
      <code>
        nofollow 
      </code> 및 
      위의 <span class="uicontrol"> URL </span>을(를) 추가하거나 업데이트합니다.<code>
        noindex 
      </code> </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URL 마스크 정보</a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>날짜 마스크 포함 및 제외 </p> </td> 
      <td colname="col2"> <p>전체 경로, 부분 경로 또는 와일드카드 또는 정규 표현식을 사용하는 경로 등 간단하게 날짜 마스크를 포함하거나 제외할 수 있습니다. </p> <p>검색 로봇은 URL과 문서 날짜를 모두 기준으로 문서를 찾아 인덱싱하거나("include") 문서를 무시합니다("exclude"). </p> <p>다음과 같은 유형의 날짜 마스크를 사용할 수 있습니다. </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <code>
        include-days NNN 
      </code> <p>검색 로봇은 지정된 URL 마스크와 일치하고 NNN 일 이상인 모든 문서를 인덱싱합니다. </p> <p>다음 키워드 중 하나 이상이 있는 URL 마스크를 따를 수 있습니다. 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">server-date </li> 
        </ul> </p> <p>예를 들어 다음 마스크는 /archive/support 폴더에 있는 0일 이상의 모든 문서를 포함합니다. </p> <p> 
        <code>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </code> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <code>
        include-date YYYY-MM-DD 
      </code> <p>검색 로봇은 지정된 URL 마스크와 일치하고 YYYY-MM-DD 날짜보다 이전 또는 오래된 모든 문서를 인덱싱합니다. </p> <p>다음 키워드 중 하나 이상이 있는 URL 마스크를 따를 수 있습니다. </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> server-date </li> 
        </ul> </p> <p>다음 마스크 예제는 2011년 7월 25일 또는 그 이전에 날짜된 /archive/ 폴더에 있는 모든 문서를 포함합니다. </p> <p> 
        <code>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <code>
        exclude-days NNN 
      </code> <p>지정된 URL 마스크와 일치하고 NNN일 이상인 모든 문서의 인덱싱을 비활성화합니다. </p> <p>원할 경우, 키워드를 기준으로 URL 마스크를 따를 수 있습니다 
        <code>
          server-date 
        </code>. </p> <p>다음 마스크 예제에서는 90일 이상 된 모든 PDF 파일을 색인에서 제외합니다. </p> <p> 
        <code>
          exclude-days 90 *.pdf 
        </code> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <code>
        exclude-date YYYY-MM-DD 
      </code> <p>지정된 URL 마스크와 일치하고 YYYY-MM-DD 날짜보다 이전 또는 이전 날짜인 모든 문서의 인덱싱을 비활성화합니다. </p> <p>원할 경우, 키워드를 기준으로 URL 마스크를 따를 수 있습니다 
        <code>
          server-date 
        </code>. </p> <p>다음 마스크 예제에서는 2004년 4월 23일 또는 그 이전에 발급된 /archive/ 폴더에 있는 모든 문서를 제외합니다. </p> <p> 
        <code>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      </ul> </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> 날짜 마스크 정보</a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL 삭제 </p> </td> 
      <td colname="col2"> <p>URL을 지정합니다. </p> <p>검색 로봇은 검색 색인에서 지정된 문서를 찾아 삭제합니다. 지정한 페이지가 이미 검색 인덱스에 있는 경우 로봇은 다른 페이지를 추가하거나 업데이트하기 전에 페이지를 삭제합니다. </p> <p>이 필드에는 마스크가 아닌 문서 URL만 포함되어야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL 마스크 찾기 및 삭제 </p> </td> 
      <td colname="col2"> <p>전체 경로, 부분 경로 또는 와일드카드 또는 정규 표현식을 사용하는 단순 URL 마스크를 지정합니다. </p> <p>지정된 URL 마스크가 검색 인덱스의 페이지와 일치하는 경우 검색 로봇은 다른 페이지를 추가하거나 업데이트하기 전에 페이지를 삭제합니다. 예: </p> <p> 
      <code>
        https://www.mydomain.com/products/1998/household/* 
      </code> </p> <p>다음 예제와 같이 정규 표현식을 사용할 수도 있습니다. </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </code> </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식</a>을 참조하십시오. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 라이브 웹 사이트 {#task_2A46BA189ECC4317A9D5C6E99A336F33}에 대한 증분 색인 일정 설정

증분 색인 빈도와 증분 인덱스를 크롤링하고 업데이트하는 데 사용되는 기본 시간을 선택할 수 있습니다.

선택한 시간은 계정 설정에 구성된 시간대에 따라 로컬입니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

웹 서버는 종종 밤에 유지 보수를 위해 아래로 내려갈 예정이다. 예약된 색인 시간 동안 서버가 다운된 경우 색인 지정 프로세스가 실패합니다. 웹 서버를 사용할 수 있는 시간을 선택해야 합니다.

색인 일정은 라이브 색인에만 적용됩니다.스테이지된 색인은 예약할 수 없습니다.

**라이브 웹 사이트에 대한 증분 색인 일정을 설정하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Incremental Index Schedule]** 페이지의 **[!UICONTROL Incrementally Index]** 드롭다운 목록에서 시간 또는 분 단위로 인덱싱 빈도를 선택합니다.
1. **[!UICONTROL Base Time]** 드롭다운 목록에서 새 증분 인덱스를 재생성할 시작 시간을 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.

## 라이브 또는 스테이지된 웹 사이트 {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}의 증분 인덱스 실행

증분 색인을 사용하여 자주 변경되는 페이지의 컬렉션과 같이 라이브 또는 스테이징 웹 사이트의 &quot;조각&quot;을 색인화할 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 증분 인덱스를 실행하려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. 클릭 **[!UICONTROL Incremental Index Now]**.
1. (선택 사항) 색인 오류가 발생하면 **[!UICONTROL View Errors]**&#x200B;을 클릭하여 연결된 로그를 봅니다.

## 라이브 또는 스테이지된 웹 사이트 {#task_E668E1F1240C476DAA1CA783DC728232}의 증분 색인 로그 보기

실시간 증분 색인 또는 스테이지된 증분 인덱스가 완료되면 연결된 로그를 보고 발생한 오류를 해결할 수 있습니다.


로그를 내보내거나 저장할 수 없습니다. 로그는 새 색인이 발생할 때까지 볼 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 증분 색인 로그를 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. 로그 페이지의 맨 위 또는 아래에서 다음 중 하나를 수행합니다.

   * 탐색 옵션 **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** 또는 **[!UICONTROL Go to line]**&#x200B;을 사용하여 로그를 통해 이동합니다.

   * 표시 옵션 **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** 또는 **[!UICONTROL Show]**&#x200B;을 사용하여 표시되는 내용을 세밀하게 수정할 수 있습니다.
