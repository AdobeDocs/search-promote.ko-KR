---
description: 단어 및 언어를 사용하여 검색어가 웹 페이지의 컨텐츠와 일치하는 방식을 결정할 수 있습니다.
seo-description: 단어 및 언어를 사용하여 검색어가 웹 페이지의 컨텐츠와 일치하는 방식을 결정할 수 있습니다.
seo-title: 단어 및 언어 정보
solution: Target
title: 단어 및 언어 정보
topic: Linguistics,Site search and merchandising
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 단어 및 언어 정보{#about-words-language}

를 [!DNL Words & Language] 사용하여 검색어가 웹 페이지의 컨텐츠와 일치하는 방식을 결정할 수 있습니다.

## 단어 및 언어 사용 {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

사이트 방문자가 설정을 변경하는 등 [!DNL Words & Language] 설정의 효과를 사용할 수 있으려면 먼저 사이트 인덱스를 다시 생성해야 합니다. 색인 작성과 달리 재생성에는 웹 페이지 크롤링 작업이 포함되지 않으며 단 몇 초만 소요됩니다.

## 검색 용어가 웹 컨텐츠와 일치하는 방식 구성 {#task_351A9144A51F4B41923BDBACDEF3B616}

단어 및 언어를 사용하여 사이트 검색/머천다이징이 검색어와 웹 페이지의 컨텐츠에 일치하는 방법을 결정할 수 있습니다.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**검색 용어가 웹 컨텐츠와 일치하는 방식을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**&#x200B;을 클릭합니다.
1. 페이지에서 원하는 옵션을 [!DNL Words & Languages] 설정합니다.

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
      <td colname="col2"> <p>기본적으로 선택되지 않습니다. </p> <p>대문자를 소문자와 구분할지 여부를 결정합니다. 예를 들어, "성공"을 선택하면 "성공"과 "성공"이 구분되고 검색 결과는 두 가지 사이에 다를 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>분음 구분 기호 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p> 분음 부호 문자가 포함된 단어가 없는 단어와 구분되는지 여부를 결정합니다. 예를 들어, 이 옵션을 선택하면 "pagina"는 "página"와 구별됩니다. 영어 이외의 언어를 사용하는 웹 사이트가 있는 경우 이 옵션을 선택 해제합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>숫자 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p>숫자가 들어 있는 단어를 인덱싱할지 여부를 결정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>아포스트로피 무시 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않습니다. </p> <p>아포스트로피가 쿼리에서 제거됩니다. 예를 들어 "Tree's"를 검색하면 "Trees"에 대한 검색과 동일한 결과가 반환됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>하이픈 무시 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않습니다. </p> <p>쿼리에서 하이픈이 제거됩니다. 예를 들어 "blue-bell"을 검색하면 "bluebell"에 대한 검색과 동일한 결과가 반환됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>부분 영숫자 일치 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택되지 않습니다. </p> <p>이 옵션을 선택하면 알파벳 순으로 전환으로 토큰을 분할할 수 있으므로 부분 또는 제품 토큰에서 자유 텍스트가 일치할 수 있습니다. </p> <p>예를 들어 웹 사이트에서 하나 이상의 페이지의 본문 컨텐츠에 <span class="codeph"> 910XT의 제품 식별자가 </span> 있다고 가정합니다. 이 옵션을 선택하지 <i>않으면</i> Adobe Search&amp;Promote <span class="keyword"> 는 910XT를 검색할 때 이 제품 식별자와 일치하는 항목을 </span> 찾습니다 <span class="codeph"> </span>. Search- <span class="uicontrol"> Concat-Div-Enable이 켜져 있는 경우 Adobe Search&amp;Promote </span> 는 <span class="keyword"> 910 XT도 찾을 수 </span> 있습니다 <span class="codeph"> </span>. 그러나 910 <span class="codeph"> 또는 XT의 인스턴스는 </span><span class="codeph"> 따로 찾을 수 </span> 없습니다. </p> <p>[부분 영숫자 <span class="uicontrol"> 일치]를 선택하면 인덱서는 이러한 혼합 영숫자 토큰을 </span>여러 토큰으로 구분합니다. 예를 들어 XYZ123과 같은 제품 <span class="codeph"> 식별자는 </span> 다음 세 개의 토큰으로 인덱싱됩니다.XYZ <span class="codeph"> 123 </span>, <span class="codeph"> XYZ </span>및 <span class="codeph"> 123 </span>. 이러한 기능을 사용하면 이러한 변형이 있을 때 검색 시간 자유 텍스트 일치를 수행할 수 있습니다. </p> <p>다른 예로 제품 식별자 AB910XT가 있다고 <span class="codeph"> 가정합니다 </span>. [Search At-Div-Matching]을 선택하고 <span class="uicontrol"> </span><i>[Search At-Div와</i> 일치하는 Search]를 선택하면 Adobe Search&amp;PromoteAdobe는 AB <span class="uicontrol"> 로 인덱스를 홍보합니다. AB 99 XT, AB, 9 CONCCT 1, XT </span> <span class="keyword"> </span> <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>0 및 XT로 변경합니다. 그런 다음 사용자가 <span class="codeph"> 910XT를 검색할 </span>때 검색이 확장되어 <span class="codeph"> 910XT, </span>910 <span class="codeph"> 또는 XT의 인스턴스가 </span>검색됩니다 <span class="codeph"> </span>. </p> <p> <p>참고: Search <span class="uicontrol"> Concat-Div-Enable </span> 은 기본적으로 활성화되지 않습니다. 해당 기능을 활성화하려면 기술 지원 센터에 문의하십시오. </p> </p> <p> <p>참고: 부분 <span class="uicontrol"> </span> 영숫자 일치는 모든 인덱스 필드에 전체적으로 적용됩니다. 그러나 자유 텍스트 일치에만 영향을 줍니다.정확한 일치 또는 범위 일치에는 영향을 주지 않습니다. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유사 일치 </p> </td> 
      <td colname="col2"> <p>기본적으로 선택됩니다. </p> <p>소리가 비슷한 단어는 "건강" 및 "helth"와 같이 일치합니다. 이 기능을 사용하면 단어 맞춤법이 잘못되더라도 손쉽게 검색할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>대체 Word 양식 </p> </td> 
      <td colname="col2"> <p>기본값은 <b>기본 대체 Word 양식입니다</b>. </p> <p>대체 Word 양식 드롭다운 목록에서 다음 옵션 중에서 선택할 수 있습니다. 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>없음</b> <p>색인 작성 중에는 형태나 대체 단어 양식이 적용되지 않습니다. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>기본 대체 Word 양식</b> <p>색인 작성 중에는 자동으로 형태소가 수행됩니다. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>도메인 사전</b> <p>형태소 사전에 설정한 모든 도메인 사전은 대체 단어 양식의 소스로 사용됩니다. </p> <p>사전 <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> 정보를 참조하십시오 </a>. </p> <p>사전 <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> 구성을 형태소 사전으로 </a>참조하십시오. </p> </li> 
      </ul> </p> <p>Adobe Search&amp;Promote에서 구문 분석이 활성화되어 <span class="keyword"> 있는 </span>경우 구문 내에서 대체 단어 양식도 발생합니다. </p> <p>Search&amp; <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Promote 8.15.0 릴리스 노트(2014년 6월 19일)를 </a>참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>언어 </p> </td> 
      <td colname="col2"> <p>기본값은 <b>영어(미국)입니다</b>. </p> <p>선택한 언어를 사용하면 선택한 부분에서 사용하는 규칙에 따라 날짜 및 숫자 값이 구문 분석됩니다. </p> <p>[ <span class="uicontrol"> 대체 단어 양식]을 [기본 대체 단어 양식] </span> 또는 [ <span class="uicontrol"> 도메인 사전]으로 설정하면 </span> <span class="uicontrol"> </span>선택한 언어의 언어적 규칙에 따라 단어 형태 및 단어 끝이 변경됩니다. </p> <p>기본적으로 언어 설정은 웹 사이트에서 읽은 페이지의 언어를 결정하는 데 사용되지 않습니다. 읽기 페이지의 언어는 해당 HTTP 헤더나 페이지 자체 내의 메타태그에서 결정됩니다. 웹 사이트에는 여러 언어로 된 페이지가 포함될 수 있습니다. 각 페이지는 여기에서 선택한 언어에 관계없이 올바로 읽고 인덱싱됩니다. </p> <p>웹 사이트의 일부 페이지에 대해 UTF-8과 같은 유니코드 문자 집합 인코딩을 사용하는 경우 해당 각 페이지의 언어가 올바르게 지정되었는지 확인하십시오. 유니코드 문서에 적절한 HTTP 헤더 또는 메타태그가 없는 경우 설정 &gt; 메타데이터 <span class="uicontrol"> &gt; </span> 주입을 <span class="uicontrol"> 사용하여 적절한 언어를 지정할 </span> <span class="uicontrol"> </span> 수 있습니다. </p> <p>지정된 <span class="uicontrol"> 언어가 없는 문서에 적용을 선택하십시오. </span> 를 클릭하여 명확한 설정이 없는 웹 사이트에서 읽은 페이지에 언어 설정을 사용합니다. 문서 <i>중 일부에만</i> 언어 설정이 없는 경우 이 설정을 사용합니다. 문서 <span class="uicontrol"> 설정이 </span> 없거나 해당 문서의 언어 설정이 잘 알려져 있고 편리하게 관리 가능한 작은 목록인 경우 설정 <span class="uicontrol"> &gt; </span> 메타데이터 <span class="uicontrol"> &gt; </span> <i></i> 주입을 사용합니다. </p> <p>주사 <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> 정보를 참조하십시오 </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>디컴파운더 사용? </p> </td> 
      <td colname="col2"> <p> <p>참고: 이 기능은 덴마크어 및 독일어에만 사용됩니다. 또한 이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 활성화하려면 기술 지원 센터에 문의하십시오. 활성화되면 디컴포저 <b>사용?</b> 이 표의 앞부분에 설명된 언어 <span class="uicontrol"> 드롭다운 목록에서 덴마크어 </span> 또는 <span class="uicontrol"> 독어를 선택한 경우에만 사용자 인터페이스에 </span> 옵션이 표시됩니다 <span class="uicontrol"> </span> . </p> </p> <p>디컴포저 사용을 <span class="uicontrol"> 선택하면 </span>를 사용하면 덴마크어 또는 독일어 복합 단어를 분해하여 원래 복합 단어와 함께 구성 요소 단어를 인덱싱할 수 있습니다. </p> <p>이 기능의 작동 방식을 확인하려면 텍스트 필드에 단어를 입력한 다음 테스트를 <span class="uicontrol"> 클릭합니다 </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Settings]**.
1. 변경 내용을 미리 보려면 스테이지된 웹 사이트 인덱스를 다시 **[!UICONTROL regenerate your staged site index]** 만들려면 을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

