---
description: 단어 및 언어를 사용하여 검색어가 웹 페이지의 컨텐츠와 일치하는 방식을 결정할 수 있습니다.
solution: Target
title: 단어 및 언어 정보
topic: 언어학,사이트 검색 및 상품 판매
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---


# 단어 및 언어 정보{#about-words-language}

[!DNL Words & Language]을(를) 사용하여 검색어가 웹 페이지의 컨텐츠와 일치하는 방식을 결정할 수 있습니다.

## 단어 및 언어 사용 {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

사이트 방문자가 해당 설정을 변경하는 등 [!DNL Words & Language] 설정의 효과를 사용할 수 있으려면 먼저 사이트 인덱스를 다시 생성해야 합니다. 색인 작성과 달리 재생성하는 것은 웹 페이지 크롤링을 포함하지 않으며 단 몇 초만에 소요됩니다.

## 검색어가 웹 컨텐츠 {#task_351A9144A51F4B41923BDBACDEF3B616}과(와) 일치하는 방식 구성

단어 및 언어를 사용하여 사이트 검색/머천다이징이 검색어와 웹 페이지의 컨텐트에 일치하는 방법을 결정할 수 있습니다.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**검색어가 웹 컨텐츠와 일치하는 방식을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**&#x200B;을 클릭합니다.
1. [!DNL Words & Languages] 페이지에서 원하는 옵션을 설정합니다.

   <!-- 
   
   r_words_and_languages_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>대/소문자 구분 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않았습니다. </p> <p>대문자를 소문자와 구분할지 여부를 결정합니다. 예를 들어, "성공"을 선택하면 "성공"과 구분되고 검색 결과는 두 사람 간에 다를 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>발음 부호 민감도 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p> 발음 부호 문자가 포함된 단어가 없는 단어와 구분되는지 여부를 결정합니다. 예를 들어, "pagina"를 선택하면 "página"와 구별됩니다. 영어 이외의 언어를 사용하는 웹 사이트가 있는 경우 이 옵션을 선택 해제합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>숫자 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p>숫자가 포함된 단어를 인덱싱할지 여부를 결정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>아포스트로피 무시 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않았습니다. </p> <p>아포스트로피가 쿼리에서 제거됩니다. 예를 들어 "Tree's"를 검색하면 "Trees"에 대한 검색과 동일한 결과가 반환됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>하이픈 무시 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않았습니다. </p> <p>쿼리에서 하이픈이 제거됩니다. 예를 들어 "blue-bell"을 검색하면 "bluebell"을 검색하는 것과 동일한 결과가 반환됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부분 영숫자 일치 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않았습니다. </p> <p>이 옵션을 선택하면 토큰을 알파벳순으로 분할할 수 있으므로 자유 텍스트가 부품 또는 제품 토큰에서 일치할 수 있습니다. </p> <p>예를 들어 웹 사이트에서 하나 이상의 페이지의 본문 내용에 <span class="codeph"> 910XT </span>의 제품 식별자가 있다고 가정합니다. 이 옵션이 선택되어 있지 않은 <i>인 경우 <span class="keyword"> Adobe Search &amp; Promote </span>은 <span class="codeph"> 910XT </span>를 검색할 때 이 제품 식별자와 일치하는 항목을 찾습니다. </i> 또한 <span class="uicontrol"> 검색 Concat-Div-Enable </span>이 켜져 있으면 <span class="keyword"> Adobe Search &amp; Promote </span>도 <span class="codeph"> 910 XT </span>을 찾습니다. 그러나 <span class="codeph"> 910 </span> 또는 <span class="codeph"> XT </span>의 인스턴스는 찾을 수 없습니다. </p> <p><span class="uicontrol"> 부분 영숫자 일치 </span>를 선택하면 인덱서가 혼합된 영숫자 토큰을 여러 토큰으로 구분합니다. 예를 들어 <span class="codeph"> XYZ123 </span> 같은 제품 ID는 다음 3개의 토큰으로 인덱싱됩니다.<span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span> 및 <span class="codeph"> 123 </span>. 이러한 기능을 사용하면 이러한 변형이 있을 때 검색 시간 자유 텍스트를 일치시킬 수 있습니다. </p> <p>다른 예로 제품 식별자 <span class="codeph"> AB910XT </span>가 있다고 가정합니다. <span class="uicontrol"> 부분 영숫자 일치 </span> <i>를 선택하고</i>에 <span class="uicontrol"> Search Concat-Div-Enable </span>이 켜져 있으면 <span class="keyword"> Adobe Search &amp; Promote </span>은 <span class="codeph"> AB910XT </span>, &lt;a11 0/&gt; AB </span>, <span class="codeph"> 910 </span> 및 <span class="codeph"> XT </span>. <span class="codeph"> 그런 다음 사용자가 <span class="codeph"> 910XT </span>를 검색할 때 검색은 확장되어 <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span> 또는 <span class="codeph"> XT </span> 인스턴스도 찾습니다. </span></p> <p> <p>참고: <span class="uicontrol"> Search Concat-Div-Enable </span>은(는) 기본적으로 활성화되지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </p> <p> <p>참고: <span class="uicontrol"> 부분 영숫자 일치 </span>는 모든 인덱스 필드에 전체적으로 적용됩니다. 그러나 자유 텍스트 일치에만 영향을 줍니다.정확한 일치 또는 범위 일치에는 영향을 주지 않습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유사한 사운드 일치 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p>비슷하게 들리는 단어들은 "건강", "헬스"와 같이 일치합니다. 이 기능을 사용하면 단어를 잘못 입력해도 손쉽게 검색할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>대체 Word Forms </p> </td> 
      <td colname="col2"> <p>기본값은 <b>기본 대체 단어 Forms</b>입니다. </p> <p>Alternate Word Forms 드롭다운 목록에서 다음 옵션 중에서 선택할 수 있습니다. 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>없음</b> <p>색인 작성 중에는 형태나 대체 단어 양식이 적용되지 않습니다. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>기본 대체 단어 Forms</b> <p>인덱싱하는 동안 자동으로 형태소 분석이 수행됩니다. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>도메인 사전</b> <p>형태소 사전으로 설정한 모든 도메인 사전은 대체 단어 양식의 소스로 사용됩니다. </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> 사전 </a> 정보를 참조하십시오. </p> <p><a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> 사전 구성을 형태소 사전 </a>으로 참조하십시오. </p> </li> 
      </ul> </p> <p><span class="keyword"> Adobe Search &amp; Promote </span>에서 구문 분석이 활성화되어 있으면 구문 내에 대체 단어 양상도 발생한다는 점을 주의하십시오. </p> <p><a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Search &amp; Promote 8.15.0 릴리스 노트(6/19/2014) </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>언어 </p> </td> 
      <td colname="col2"> <p>기본값은 <b>영어(미국)</b>입니다. </p> <p>선택한 언어를 사용하면 선택한 부분에서 사용하는 규칙에 따라 날짜 및 숫자 값을 구문 분석합니다. </p> <p><span class="uicontrol"> 대체 단어 Forms </span>이 <span class="uicontrol"> 기본 대체 단어 Forms </span> 또는 <span class="uicontrol"> 도메인 사전 </span>으로 설정된 경우 선택한 언어에 대한 언어 규칙에 따라 단어 형식 및 단어 엔딩이 변경됩니다. </p> <p>기본적으로 언어 설정은 웹 사이트에서 읽은 페이지의 언어를 결정하는 데 사용되지 않습니다. 읽기 페이지의 언어는 해당 HTTP 헤더나 페이지 자체 내의 메타 태그에서 결정됩니다. 웹 사이트에는 여러 언어로 된 페이지가 포함될 수 있습니다. 각 페이지는 여기에서 선택한 언어에 관계없이 올바로 읽고 인덱싱됩니다. </p> <p>웹 사이트의 일부 페이지에 대해 UTF-8과 같은 유니코드 문자 집합 인코딩을 사용하는 경우 해당 각 페이지의 언어가 올바르게 지정되었는지 확인하십시오. 유니코드 문서에 적절한 HTTP 헤더 또는 메타태그가 없는 경우 <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 메타데이터 </span> &gt; <span class="uicontrol"> 주입 </span>을 사용하여 적절한 언어를 지정할 수 있습니다. </p> <p><span class="uicontrol"> 지정된 언어가 없는 문서에 적용하시겠습니까? </span> 을 클릭하여 명시적 설정이 없는 웹 사이트에서 읽은 페이지에 언어 설정을 사용합니다. 문서의 <i>일부</i>에만 언어 설정이 없을 때 이 설정을 사용합니다. 문서 <i>없음</i>에 언어 설정이 있거나 해당 문서 집합이 잘 알려진 관리 가능한 작은 목록인 경우 <span class="uicontrol"> 설정 </span> &gt; <span class="uicontrol"> 메타데이터 </span> &gt; <span class="uicontrol"> 주입 </span>을 사용하십시오. </p> <p><a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> 주입 정보 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>디컴파운더 사용? </p> </td> 
      <td colname="col2"> <p> <p>참고: 이 기능은 덴마크어 및 독일어에만 사용됩니다. 또한 이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. 이 옵션이 활성화되면 <b>디컴포저 사용?</b> 이 표의 앞부분에 설명된  <span class="uicontrol"> 언어  </span> 드롭다운 목록 <span class="uicontrol"> 에서  </span> 덴마크어 또 <span class="uicontrol"> 는 </span> 는 독일어를 선택한 경우에만 사용자 인터페이스에 옵션이나타납니다. </p> </p> <p><span class="uicontrol"> 디컴포저 사용을 선택하면 </span>이 서비스는 구성 요소 단어를 원래 복합 단어와 함께 인덱싱할 수 있도록 해주는 덴마크어 또는 독일어 복합 단어를 분해합니다. </p> <p>이 기능의 작동 방식을 보려면 텍스트 필드에 단어를 입력한 다음 <span class="uicontrol"> 테스트 </span>를 클릭합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Settings]**.
1. 변경 결과를 미리 보려면 **[!UICONTROL regenerate your staged site index]**&#x200B;을 클릭하여 스테이지된 웹 사이트 인덱스를 다시 작성합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

