---
description: 자동 완성 기능이 활성화된 검색 양식 및 자동 완성 사용 검색 양식의 일부로 포함된 autocomplete_data.js 파일의 생성을 제어하도록 다양한 자동 완료 영역을 구성할 수 있습니다.
solution: Target
subtopic: Auto-Complete
title: 자동 완성 정보
topic-legacy: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
exl-id: a1d08c0a-6c68-4da2-88d2-fe953d333536
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 1%

---

# 자동 완성 정보{#about-auto-complete}

자동 완성 기능이 활성화된 검색 양식 및 자동 완성 사용 검색 양식의 일부로 포함된 autocomplete_data.js 파일의 생성을 제어하도록 다양한 자동 완료 영역을 구성할 수 있습니다.

## 자동 완성 정보 {#concept_093A9CD754864BA79B456FE4BEB64578}

자동 완료 설정 페이지가 저장된 변경 사항이 있을 때마다 [!DNL autocomplete_data.js] 파일이 다시 생성되고 검색 컨텐츠 네트워크에 게시됩니다.

## 자동 완료 구성 {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

자동 완성 사용 검색 양식 및 파일의 생성을 제어하는 옵션을 구성하고 설정할 수 있습니다.

<!-- 

t_configuring_auto-complete.xml

 -->

자동 완성 구성 후에는 검토할 결과 HTML 소스를 볼 수 있습니다. HTML 소스는 웹 사이트의 페이지에 복사하여 붙여넣는 것입니다.

검색 양식 미리 보기 를 참조하십시오.](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).[

[자동 완성 단어 목록 구성](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)을 참조하십시오.

[자동 완성 CSS 구성](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)을 참조하십시오.

**자동 완료를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**&#x200B;를 클릭합니다.
1. [!DNL Auto-Complete Setup] 페이지에서 원하는 옵션을 설정합니다.

   [검색 양식에서 표시되는 그대로 미리 보기...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>최대 제안 사항 </p> </td> 
      <td colname="col2"> <p>자동 완성 제안 목록에 표시할 최대 항목 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 입력 문자 </p> </td> 
      <td colname="col2"> <p>고객이 제안을 표시하기 전에 자동 완성 검색 양식에 입력해야 하는 문자 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최대 캐시 항목 수 </p> </td> 
      <td colname="col2"> <p>고객의 브라우저에서 캐싱하기 위해 이전에 요청한 자동 완료 제안 최대 수를 지정합니다. 일반적으로 이 설정은 기본값인 1000으로 두어야 합니다. </p> <p>이 옵션을 0으로 설정하여 브라우저 캐싱을 완전히 비활성화할 수 있지만 권장되지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>양식 이름 </p> </td> 
      <td colname="col2"> <p>자동 완성 사용 검색 양식의 "form" 태그의 "name" 속성을 지정합니다. 예: </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>여기서 <span class="filepath"> SiteSearch </span>는 양식 태그의 이름 속성입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Div 태그 ID </p> </td> 
      <td colname="col2"> <p>자동 완성 사용 검색 양식의 "div" 태그의 ID 속성을 지정합니다. 예: </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>여기서 <span class="filepath"> autocomplete </span>는 div 태그의 속성입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>입력 태그 ID </p> </td> 
      <td colname="col2"> <p>자동 완성 사용 검색 양식의 "입력" 태그의 ID 속성을 지정합니다. 예: </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>여기서 <span class="filepath"> q </span>은 입력 태그의 id 속성입니다. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>그림자 표시 </p> </td>
      <td colname="col2"> <p>자동 완성 제안 목록에 코스메틱 그림자 추가 </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>구 시작 시에만 일치 </p> </td>
      <td colname="col2"> <p>입력 텍스트 의 시작 부분과 일치하는 결과만 제안합니다. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>UTF-8 문자 집합 지원 </p> </td>
      <td colname="col2"> <p>ASCII가 아닌 문자를 용어에서 올바르게 처리합니다. </p> </td>
      </tr>
    </tbody> 
   </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 변경한 내용을 되돌리려면 **[!UICONTROL History]** 을 클릭합니다.

      [기록 옵션 사용](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 자동 완성 단어 목록 구성 {#task_1F8E0F346263443383F8CFD2C7AB35D4}

자동 완성 기능이 고객에게 제안으로 표시하는 단어 및 구 목록을 구성합니다.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

[자동 완료 구성](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)을 참조하십시오.

[자동 완성 CSS 구성](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)을 참조하십시오.

**자동 완성 단어 목록을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**&#x200B;를 클릭합니다.
1. [!DNL Auto-Complete Word List] 페이지에서 원하는 옵션을 설정합니다.

   검색 양식 미리 보기 를 참조하십시오.](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).[

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>인기 있는 검색 기간 </p> </td> 
      <td colname="col2"> <p> 고객의 최근 검색에서 단어와 구문을 포함할 기간을 제어합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> 최대 검색 수 </p> </td> 
      <td colname="col2"> <p>자동 완성 단어 목록에 포함할 검색한 단어 및 구문의 최대 개수를 제어합니다. 가장 인기 있는 상위 단어 및 구가 포함되어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 이름 </p> </td> 
      <td colname="col2"> <p>각 필드 이름은 인덱싱된 값을 포함할 하나의 필드의 이름을 정의합니다. 필드 이름을 추가하거나 제거하려면 + 및 - 을 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최대 값 수 </p> </td> 
      <td colname="col2"> <p>선택한 필드 이름에 허용되는 필드 값의 최대 개수를 정의합니다. 가장 많이 참조되는 최상위 값이 포함됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다음 단어 및 구 추가 </p> </td> 
      <td colname="col2"> <p> 자동 완성 단어 목록은 이 영역에 나열된 단어와 구로 채워집니다. </p> <p> 목록을 확인하거나 목록에 단어 및 구문을 추가하려면 <span class="uicontrol"> 편집 </span> 을 클릭합니다. 완료되면 <span class="uicontrol"> 변경 내용 저장 </span> 을 클릭합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>이 단어 및 구 제거 </p> </td> 
      <td colname="col2"> <p> 이 영역의 항목은 자동 완성 단어 목록에 표시되지 않습니다. </p> <p> 목록을 확인하거나 목록에 단어 및 구문을 추가하려면 <span class="uicontrol"> 편집 </span> 을 클릭합니다. 완료되면 <span class="uicontrol"> 변경 내용 저장 </span> 을 클릭합니다. </p> <p> 이 목록에서는 정규 표현식이 허용됩니다. 이 목록에서 정규 표현식을 지정하려면 <code>regexp</code> 행을 시작하고 그 뒤에 공백을 추가한 다음 정규 표현식을 입력합니다. 정규 표현식과 일치하는 단어 목록의 모든 줄이 제거됩니다. </p> <p> <b>중요</b>: 다른 애플리케이션에서 정규 표현식을 사용한 적이 있는 경우에만 정규 표현식을 사용해야 합니다. </p> <p><a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>대/소문자 무시 </p> </td> 
      <td colname="col2"> <p>자동 완성 단어 목록에서 알파벳 대문자/소문자만 다른 중복 항목이 제거됩니다. 모든 단어 목록 항목은 소문자로 강제 적용됩니다. </p> <p>자동 완료 제안을 "첫 번째 대문자로" 또는 "모두 대문자"로 표시하려면 를 추가합니다. 
        <code>
          text-transform : capitalize; 
        </code> 또는 
        <code>
          text-transform : uppercase; 
        </code> 결과 항목의 "/* 스타일 아래에 있는 자동 완료 CSS 컨텐츠에 대한 CSS 텍스트 속성. */" </p> <p><a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> 자동 완성 CSS </a> 구성을 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다시 색인에 대한 업데이트 </p> </td> 
      <td colname="col2"> <p>자동 완성 단어 목록은 성공적인 각 계정 다시 색인화된 후 자동으로 다시 생성됩니다. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 변경한 내용을 되돌리려면 **[!UICONTROL History]** 을 클릭합니다.
   * **[!UICONTROL Preview Word List]** 을 클릭하여 변경한 내용을 저장한 다음 자동 완료 제안 목록을 검토할 수 있는 [!DNL Auto-Complete Word List Preview] 페이지를 엽니다. 페이지 상단 근처에 있는 탐색 옵션을 사용하여 표시된 목록을 검토하고 세분화합니다. 완료되면 **[!UICONTROL Close]** 을 클릭하여 [!DNL Auto-Complete Word List] 페이지로 돌아갑니다.

      [기록 옵션 사용](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 자동 완성 CSS 구성 {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

자동 완성 CSS를 사용하여 사용할 자동 완성 계단식 스타일 시트를 구성합니다.

<!-- 

t_configuring_auto-complete_css.xml

 -->

자동 완성 CSS는 자동 완성 검색 양식의 일부로 포함된 [!DNL autocomplete_styles.css]의 콘텐츠를 제어합니다. 여기서 지정하는 CSS는 자동 완성 제안 목록의 시각적 프레젠테이션을 제어합니다. 가능한 시각적 프레젠테이션 아이디어의 예는 다음을 참조하십시오.

<!-- 404 DEAD LINK [https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html). -->

[자동 완성 단어 목록 구성](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

[자동 완료 구성](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

자동 완성 CSS 구성을 마치면 검색 양식을 미리 보고 지정한 CSS가 모양 및 레이아웃에서 허용되는지 확인할 수 있습니다.

검색 양식 미리 보기 를 참조하십시오.](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).[

**중요**: 사용자 지정 자동 완성 CSS를 적용하려면 HTML 코드에 나타나는 두 번째 줄에서 주석 태그를 제거해야 합니다. 그런 다음 검색 양식이 포함된 페이지의 헤드 섹션 내에서으로 동일한 줄을 이동합니다.

[검색 양식의 HTML 코드를 다음 위치에 복사..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**자동 완성 CSS를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**&#x200B;를 클릭합니다.
1. [!DNL Auto-Complete CSS] 텍스트 필드에서 자동 완성 제안 목록과 연결할 계단식 스타일 시트 정보를 붙여 넣거나 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 웹 사이트에 표시되는 검색 양식 미리 보기 {#task_437B35EFA5424603A08AF8E79E6B4714}

자동 완성 및 자동 완성 CSS의 구성에 따라 웹 사이트에 HTML 코드를 추가할 경우 검색 양식이 어떻게 표시되는지 미리 볼 수 있습니다.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

[자동 완료 구성](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)을 참조하십시오.

[자동 완성 CSS 구성](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)을 참조하십시오.

[검색 양식의 HTML 코드를 다음 위치에 복사..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

[검색 양식에서 컬렉션 사용](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)을 참조하십시오.

[양식](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)에 프레임 사용 을 참조하십시오.

[샘플 고급 검색 양식](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)을 참조하십시오.

[고급 검색 양식 HTML 코드](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)를 참조하십시오.

[고급 검색 양식 템플릿 코드](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)를 참조하십시오.

**웹 사이트에 표시되는 검색 양식을 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**&#x200B;를 클릭합니다.
1. (선택 사항) **[!UICONTROL HTML code]** 을 클릭하여 복사하여 웹 사이트의 페이지에 붙여넣는 HTML을 확인합니다.

## 검색 양식의 HTML 코드를 웹 사이트의 페이지에 복사 {#task_A3A01EA800F24C0AA33902387E0362C7}

자동 완성 및 자동 완성 CSS의 구성에 따라 웹 사이트에 HTML 코드를 추가할 경우 검색 양식이 어떻게 표시되는지 미리 볼 수 있습니다.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

[자동 완료 구성](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)을 참조하십시오.

[자동 완성 CSS 구성](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)을 참조하십시오.

[검색 양식의 HTML 코드를 다음 위치에 복사..](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

[검색 양식에서 컬렉션 사용](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)을 참조하십시오.

[양식](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)에 프레임 사용 을 참조하십시오.

[샘플 고급 검색 양식](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)을 참조하십시오.

[고급 검색 양식 HTML 코드](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)를 참조하십시오.

[고급 검색 양식 템플릿 코드](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)를 참조하십시오.

**검색 양식의 HTML 코드를 웹 사이트의 페이지에 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >양식 소스에서 `form name=` 값을 변경하지 마십시오.

1. (선택 사항) 다음 중 하나를 수행합니다.

   * 자동 완성 CSS를 구성하고 스타일을 검색 양식에 적용하려는 경우 HTML 코드에 나타나는 두 번째 줄에서 주석 태그를 제거합니다. 그런 다음 검색 양식이 포함된 페이지의 헤드 섹션 내에서으로 동일한 줄을 이동합니다.
   * 성능을 최대화하려면 HTML 코드 하단에 나열된 태그를 이동하여 검색 양식이 포함된 각 페이지의 본문 섹션 하단에 놓습니다.

1. 코드를 복사하여 검색 양식을 표시할 웹 사이트의 웹 페이지에 붙여넣습니다.
