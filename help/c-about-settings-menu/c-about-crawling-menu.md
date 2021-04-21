---
description: 크롤링 메뉴 세트 날짜와 URL 마스크, 암호, 컨텐츠 유형, 연결, 양식 정의 및 URL 시작 지점을 사용합니다.
solution: Target
subtopic: Crawling
title: 크롤링 메뉴 정보
topic-legacy: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
exl-id: 22dbbc30-bf1c-4d51-8fb0-708115ba844b
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '11011'
ht-degree: 0%

---

# 크롤링 메뉴 {#about-the-crawling-menu} 정보

크롤링 메뉴 세트 날짜와 URL 마스크, 암호, 컨텐츠 유형, 연결, 양식 정의 및 URL 시작 지점을 사용합니다.

## URL 시작 지점 정보 {#concept_5D857E3B5C124E85BC0B5AE77A509573}

대부분의 웹 사이트에는 고객이 처음으로 방문하는 하나의 기본 시작 지점 또는 홈 페이지가 있습니다. 이 기본 시작 지점은 검색 로봇이 색인 크롤링을 시작하는 URL 주소입니다. 그러나 웹 사이트에 도메인 또는 하위 도메인이 여러 개 있거나 사이트의 일부가 기본 시작 지점에서 연결되어 있지 않은 경우 URL 시작 지점을 사용하여 더 많은 시작 지점을 추가할 수 있습니다.

지정된 각 URL 시작 지점 아래의 모든 웹 사이트 페이지는 인덱싱됩니다. URL 시작 지점을 마스크와 결합하여 색인화할 웹 사이트의 특정 부분을 정확하게 제어할 수 있습니다. 고객이 URL 시작 지점 설정의 효과를 볼 수 있으려면 먼저 웹 사이트 인덱스를 다시 만들어야 합니다.

기본 시작 지점은 일반적으로 색인 및 검색할 웹 사이트의 URL입니다. 계정 설정에서 이 기본 진입점을 구성합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

기본 URL 시작 지점을 지정한 후에는 선택적으로 순서대로 크롤링할 추가 시작 지점을 지정할 수 있습니다. 대부분의 경우 기본 시작 지점 아래의 페이지에서 연결되지 않은 웹 페이지에 대한 추가 시작 지점을 지정합니다. 다음 예제와 같이 웹 사이트가 두 개 이상의 도메인에 걸쳐 있을 때 추가 시작 지점을 지정합니다.

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

아래 표에 하나 이상의 공백으로 구분된 키워드를 사용하여 각 진입점의 자격을 매길 수 있습니다. 이러한 키워드는 페이지의 인덱스 방식에 영향을 줍니다.

**중요**:주어진 키워드를 시작 포인트에서 분리하고 공백으로 구분해야 합니다.쉼표는 유효한 구분 기호가 아닙니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> 시작 지점 페이지에 있는 텍스트를 색인화하지 않고 페이지의 링크를 따르려면 
     시작 지점 뒤에 <code>
       noindex 
     </code>. </p> <p>다음 예제와 같이 키워드를 시작 지점에서 공백으로 구분합니다. </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>이 키워드는 
     <code>
       content="noindex" 
     </code>) 
     <code>
       &lt;head&gt; 
     </code>... 
     시작 지점 페이지의 <code>
       &lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> 시작 지점 페이지의 텍스트를 색인화하지만 페이지의 링크를 따라가지 않으려면 
     시작 지점 뒤에 <code>
       nofollow 
     </code>. </p> <p>다음 예제와 같이 키워드를 시작 지점에서 공백으로 구분합니다. </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>이 키워드는 
     <code>
       content="nofollow" 
     </code> 사이에 
     <code>
       &lt;head&gt; 
     </code>... 
     시작 지점 페이지의 <code>
       &lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>양식 </p> </td> 
   <td colname="col2"> <p> 시작 지점이 로그인 페이지인 경우, 
     <code>
       form 
     </code>은(는) 일반적으로 검색 로봇이 웹 사이트를 크롤하기 전에 로그인 양식을 제출하고 적절한 쿠키를 받을 수 있도록 사용됩니다. "form" 키워드를 사용할 때 시작 지점 페이지는 인덱싱되지 않고 검색 로봇은 시작 지점 페이지를 크롤링으로 표시하지 않습니다. 사용 
     검색 로봇이 페이지의 링크를 따라가지 못하게 하려면 <code>
       nofollow 
     </code>. </p> </td> 
  </tr> 
 </tbody> 
</table>

[콘텐츠 유형 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)도 참조하십시오.

[색인 커넥터 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)도 참조하십시오.

## 인덱싱할 URL 진입점을 여러 개 추가하는 중 {#task_2338A47387D74CFDAC4D4EF4A367ED45}

웹 사이트에 여러 도메인 또는 하위 도메인이 있고 해당 도메인을 크롤링하려는 경우 URL 진입점을 사용하여 URL을 더 추가할 수 있습니다.

웹 사이트의 기본 URL 시작 지점을 설정하려면 계정 설정을 사용합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

**인덱싱할 URL 진입점을 여러 개 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 클릭합니다.
1. [!DNL URL Entrypoints] 페이지의 [!DNL Entrypoints] 필드에 한 줄에 URL 주소를 입력합니다.
1. (선택 사항) **[!UICONTROL Add Index Connector Configurations]** 드롭다운 목록에서 색인화를 위한 시작 지점으로 추가할 색인 커넥터를 선택합니다.

   드롭다운 목록은 이전에 하나 이상의 색인 커넥터 정의를 추가한 경우에만 사용할 수 있습니다.

   ![](assets/url_entrypoints_index_connector.png)

   [색인 커넥터 정의](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886) 추가를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## URL 마스크 정보 {#concept_8039DFC53FF3410AA494D602F71BA164}

URL 마스크는 검색 로봇이 색인화하거나 색인화하지 않는 웹 사이트 문서를 결정하는 패턴입니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 작성하십시오.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

다음은 사용할 수 있는 두 가지 유형의 URL 마스크입니다.

* URL 마스크 포함
* URL 마스크 제외

URL 마스크 포함 - 검색 로봇이 마스크의 패턴과 일치하는 모든 문서를 색인화합니다.

URL 제외 마스크는 검색 로봇이 일치하는 문서를 색인화하도록 지시합니다.

검색 로봇이 링크에서 웹 사이트를 통해 이동하면서 URL을 찾아 해당 URL과 일치하는 마스크를 찾습니다. 첫 번째 검색은 색인에서 해당 URL을 포함할지 제외할지를 결정합니다. 발견된 URL과 일치하는 마스크가 없으면 해당 URL이 인덱스에서 삭제됩니다.

시작 지점 URL에 대한 URL 마스크를 자동으로 생성합니다. 이 동작을 통해 웹 사이트에서 발견된 모든 문서를 색인화할 수 있습니다. 또한 웹 사이트를 &quot;나가기&quot;하는 링크가 포함되어 있지 않습니다. 예를 들어 인덱스 페이지가 https://www.yahoo.com에 링크되는 경우 검색 로봇은 진입점 URL에 의해 자동으로 생성된 포함 마스크와 일치하지 않으므로 해당 URL을 색인화하지 않습니다.

지정하는 각 URL 마스크는 별도의 줄에 있어야 합니다.

마스크는 다음 중 하나를 지정할 수 있습니다.

* `https://www.mydomain.com/products.html`의 전체 경로입니다.
* `https://www.mydomain.com/products`의 부분 경로입니다.
* `https://www.mydomain.com/*.html`에서와 같이 와일드카드를 사용하는 URL.
* 정규 표현식(고급 사용자의 경우).

   마스크를 정규 표현식으로 만들려면 마스크 유형( `exclude` 또는 `include`)과 URL 마스크 사이에 `regexp` 키워드를 삽입합니다.

다음은 간단한 제외 URL 마스크 예입니다.

```
exclude https://www.mydomain.com/photos
```

이 예제는 제외 URL 마스크이므로 패턴과 일치하는 모든 문서는 색인화되지 않습니다. 패턴은 파일과 폴더 모두 일치하는 모든 항목과 일치하므로 제외 URL과 일치하는 `https://www.mydomain.com/photos.html` 및 `https://www.mydomain.com/photos/index.html` 모두 색인이 되지 않습니다. `/photos/` 폴더의 파일만 일치시키려면 URL 마스크에 다음 예제와 같이 후행 슬래시가 포함되어야 합니다.

```
exclude https://www.mydomain.com/photos/
```

다음 제외 마스크 예제에서는 와일드카드 사용 방법을 사용합니다. 검색 로봇에게 확장명이 &quot;.pdf&quot;인 파일을 간과하도록 지시합니다. 검색 로봇은 이러한 파일을 색인에 추가하지 않습니다.

```
exclude *.pdf
```

간단한 포함 URL 마스크는 다음과 같습니다.

```
include https://www.mydomain.com/news/
```

URL 진입점에서 일련의 링크를 통해 연결되거나 URL 진입점 자체로 사용되는 문서만 인덱싱됩니다. 포함 URL 마스크로 문서의 URL만 나열해도 연결되지 않은 문서에 색인이 적용되지 않습니다. 연결되지 않은 문서를 색인에 추가하려면 [URL 시작 지점] 기능을 사용할 수 있습니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

마스크 포함 및 마스크 제외는 함께 사용할 수 있습니다. 제외 URL 마스크를 만들고 포함 URL 마스크가 있는 제외되는 페이지 중 하나 이상을 포함하여 웹 사이트의 큰 부분을 인덱스에서 제외할 수 있습니다. 예를 들어 시작 지점 URL이 다음과 같다고 가정해 보십시오.

```
https://www.mydomain.com/photos/
```

검색 로봇은 `/photos/summer/`, `/photos/spring/` 및 `/photos/fall/` 아래의 모든 페이지를 탐색하고 인덱싱합니다(`photos` 폴더의 각 디렉토리에 하나 이상의 페이지에 대한 링크가 있다고 가정함). 이 동작은 링크 경로를 통해 검색 로봇이 `/summer/`, `/spring/` 및 `/fall/`, 폴더 및 폴더 URL이 시작점 URL에 의해 자동으로 생성되는 포함 마스크와 일치하도록 합니다.

다음 예제와 같이 제외 URL 마스크가 있는 `/fall/` 폴더의 모든 페이지를 제외하도록 선택할 수 있습니다.

```
exclude https://www.mydomain.com/photos/fall/
```

또는 다음 URL 마스크가 있는 인덱스의 일부로 선택적으로 `/photos/fall/redleaves4.html`만 포함:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

위의 두 마스크 예제가 제대로 작동하려면 다음과 같이 포함 마스크가 먼저 나열됩니다.

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

검색 로봇은 나열된 순서대로 방향을 따르기 때문에 먼저 `/photos/fall/redleaves4.html`을 포함시킨 다음 `/fall` 폴더에 있는 나머지 파일을 제외합니다.

지침을 다음과 같이 정반대로 지정한 경우:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

그런 다음 마스크에 포함된 것으로 지정되더라도 `/photos/fall/redleaves4.html`은 포함되지 않습니다.

먼저 나타나는 URL 마스크는 마스크 설정 뒤에 나타나는 URL 마스크보다 항상 우선합니다. 또한 검색 로봇이 포함 URL 마스크와 제외 URL 마스크와 일치하는 페이지가 발견되면 먼저 나열된 마스크가 항상 우선합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

## URL 마스크가 {#section_7609A7A6D79B482ABCA8900886541AAB}인 키워드 사용 정보

일치하는 페이지가 인덱싱되는 방식에 영향을 주는 하나 이상의 공백으로 구분된 키워드로 각 포함 마스크를 평가할 수 있습니다.

쉼표는 마스크와 키워드 간의 구분 문자로 사용할 수 없습니다.공백만 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> URL 마스크와 일치하는 페이지의 텍스트를 색인화하지 않고 일치된 페이지 링크를 따르려면 
     포함 URL 마스크 뒤에 <code>
       noindex 
     </code>. 다음 예제와 같이 키워드를 마스크와 공백으로 구분해야 합니다. </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>위의 예제에서는 검색 로봇이 
     <code>
       .swf 
     </code> 확장명을 사용할 수 있지만 해당 파일에 포함된 모든 텍스트의 인덱싱을 사용할 수 없습니다. </p> <p>Adobe의 
     <code>
       noindex 
     </code> 키워드는 
     <code>
       content="noindex" 
     </code> 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> URL 마스크와 일치하는 페이지의 텍스트를 색인화하지만 일치된 페이지의 링크를 따라가지 않으려면 
     포함 URL 마스크 뒤에 <code>
       nofollow 
     </code>. 다음 예제와 같이 키워드를 마스크와 공백으로 구분해야 합니다. </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Adobe의 
     <code>
       nofollow 
     </code> 키워드는 
     <code>
       content="nofollow" 
     </code> 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>마스크 포함 및 제외에 모두 사용됩니다. </p> <p>URL 마스크 앞에 
     <code>
       regexp 
     </code>은(는) 정규 표현식으로 처리됩니다. 검색 로봇이 제외 정규 표현식 URL 마스크와 일치하는 문서가 발견되면 해당 문서는 색인이 적용되지 않습니다. 검색 로봇이 포함 정규 표현식 URL 마스크와 일치하는 문서를 발견하면 해당 문서가 인덱싱됩니다. 예를 들어 다음과 같은 URL 마스크가 있다고 가정합니다. </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>검색 로봇은 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>다음 제외 정규 표현식 URL 마스크가 있는 경우: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>검색 로봇은 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>정규 표현식 URL 마스크를 포함하는 경우: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>검색 로봇은 확장명이 ".swf"인 파일의 모든 링크를 따릅니다. Adobe의 
     <code>
       noindex 
     </code> 키워드는 일치하는 파일의 텍스트가 인덱싱되지 않도록 지정합니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 웹 사이트 {#task_E1AFC17C746048B8843013D979E082C1}의 인덱스 부분에 URL 마스크 추가

[!DNL URL Masks]을(를) 사용하여 웹 사이트의 어느 부분을 크롤링하거나 인덱싱하지 않으려는 것인지 정의할 수 있습니다.

[URL 마스크 테스트] 필드를 사용하여 문서가 색인 후에 포함되어 있는지 여부를 테스트합니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 작성하십시오.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**웹 사이트의 일부분을 색인화하거나 색인화하지 않도록 URL 마스크를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL URL Masks] 페이지의 **[!UICONTROL Test URL Masks]** 필드에 웹 사이트의 테스트 URL 마스크를 입력한 다음 **[!UICONTROL Test]**&#x200B;를 클릭합니다.
1. [!DNL URL Masks] 필드에 `include`(크롤링하고 인덱싱할 웹 사이트를 추가하려면) 또는 `exclude`(웹 사이트가 크롤링 및 인덱싱되지 않도록 차단하려면)를 입력한 다음 URL 마스크 주소를 입력합니다.

   한 줄에 하나의 URL 마스크 주소를 입력합니다. 예:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 날짜 마스크 정보 {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

[날짜 마스크]를 사용하여 파일 나이를 기준으로 검색 결과에서 파일을 포함하거나 제외할 수 있습니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 작성하십시오.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

다음은 사용할 수 있는 두 가지 날짜 마스크입니다.

* 날짜 마스크 포함(&quot;include-days&quot; 및 &quot;include-date&quot;)

   지정된 날짜 또는 그 이전에 날짜가 지정된 날짜 마스크 인덱스 파일을 포함합니다.
* 날짜 마스크 제외(&quot;제외 일&quot; 및 &quot;제외 날짜&quot;)

   지정된 날짜 또는 그 이전에 날짜가 지정된 날짜 마스크 인덱스 파일을 제외합니다.

기본적으로 파일 날짜는 메타 태그 정보로 결정됩니다. 메타 태그를 찾을 수 없으면 검색 로봇이 파일을 다운로드할 때 서버로부터 수신되는 HTTP 헤더에서 파일 날짜가 결정됩니다.

지정한 각 날짜 마스크는 별도의 줄에 있어야 합니다.

마스크는 다음 중 하나를 지정할 수 있습니다.

* `https://www.mydomain.com/products.html`의 전체 경로
* `https://www.mydomain.com/products`의 부분 경로
* 와일드카드 `https://www.mydomain.com/*.html`를 사용하는 URL
* 정규 표현식입니다. 마스크를 정규 표현식으로 만들려면 URL 앞에 `regexp` 키워드를 삽입합니다.

날짜 마스크 포함 및 제외 모두 다음 두 방법 중 하나로 날짜를 지정할 수 있습니다. 마스크는 지정된 날짜 전이나 이전에 일치하는 파일을 만든 경우에만 적용됩니다.

1. 일 수입니다. 예를 들어 날짜 마스크가 다음과 같다고 가정합니다.

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   지정된 일 수가 다시 계산됩니다. 파일이 도착 날짜 또는 그 전에 날짜가 지정되면 마스크가 적용됩니다.

1. YYYY-MM-DD 형식을 사용하는 실제 날짜입니다. 예를 들어 날짜 마스크가 다음과 같다고 가정합니다.

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   일치하는 문서의 날짜가 지정된 날짜 이전이면 날짜 마스크가 적용됩니다.

다음은 간단한 제외 날짜 마스크 예입니다.

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

이 마스크는 제외 날짜 마스크이므로 패턴과 일치하는 모든 파일은 색인화되지 않고 90일 이전 버전입니다. 문서를 제외하는 경우, 색인화된 텍스트가 없고 그 파일 뒤에 오는 링크가 없습니다. 파일이 효과적으로 무시됩니다. 이 예에서 파일과 폴더 모두 지정된 URL 패턴과 일치할 수 있습니다. `https://www.mydomain.com/docs/archive.html` 및 `https://www.mydomain.com/docs/archive/index.html` 모두 패턴과 일치하며 90일 이상이 되면 색인이 되지 않습니다. `/docs/archive/` 폴더의 파일만 일치시키려면 날짜 마스크에 다음과 같이 후행 슬래시가 포함되어야 합니다.

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

날짜 마스크는 와일드카드와 함께 사용할 수도 있습니다. 다음 제외 마스크는 검색 로봇에 날짜가 2011-02-15 이전 또는 그 날짜가 지정된 &quot;.pdf&quot; 확장자를 가진 파일을 간과하도록 지시합니다. 검색 로봇은 색인에 일치하는 파일을 추가하지 않습니다.

```
exclude-date 2011-02-15 *.pdf
```

날짜 마스크 포함(Include date mask looks)은 유사하며 일치하는 파일만 색인에 추가됩니다. 다음 날짜 마스크 포함 예제는 검색 로봇이 웹 사이트의 `/docs/archive/manual/` 영역에 있는 0일 또는 그 이전의 모든 파일에서 텍스트를 색인화하도록 합니다.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

마스크 포함 및 마스크 제외는 함께 사용할 수 있습니다. 예를 들어 제외 날짜 마스크를 만들고 포함 URL 마스크가 있는 제외된 페이지 중 하나 이상을 포함시켜 웹 사이트의 큰 부분을 인덱스에서 제외할 수 있습니다. 시작 지점 URL이 다음과 같은 경우:

```
https://www.mydomain.com/archive/
```

검색 로봇은 `/archive/summer/`, `/archive/spring/` 및 `/archive/fall/` 아래의 모든 페이지를 탐색하고 인덱싱합니다(`archive` 폴더의 각 폴더에 하나 이상의 페이지에 대한 링크가 있다고 가정함). 이 동작은 링크 경로를 통해 검색 로봇이 `/summer/`, `/spring/` 및 `/fall/` 폴더의 파일을 &quot;찾기&quot;할 수 있고 폴더 URL이 시작점 URL에 의해 자동으로 생성된 포함 마스크와 일치하기 때문에 발생합니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

다음과 같이 제외 날짜 마스크가 있는 `/fall/` 폴더에서 90일이 넘는 모든 페이지를 제외하도록 선택할 수 있습니다.

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

다음 날짜 마스크가 있는 인덱스의 일부로 `/archive/fall/index.html`(얼마나 오래되었는지 상관없이, 0일 이전 파일이 일치하는지 여부와 상관없이)만 선택적으로 포함할 수 있습니다.

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

위의 두 마스크 예제가 제대로 작동하려면 다음처럼 먼저 포함 마스크를 나열해야 합니다.

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

검색 로봇은 지정된 순서대로 방향을 따르기 때문에 먼저 `/archive/fall/index.html`을 포함시킨 다음 `/fall` 폴더에 있는 나머지 파일을 제외합니다.

지침을 다음과 같이 정반대로 지정한 경우:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

그런 다음 마스크에 `/archive/fall/index.html`이(가) 포함되도록 지정되더라도 은 포함되지 않습니다. 맨 처음 나타나는 날짜 마스크는 항상 마스크 설정에 나중에 나타날 수 있는 날짜 마스크보다 우선합니다. 또한 검색 로봇이 포함 날짜 마스크와 제외 날짜 마스크와 일치하는 페이지가 발견되면 먼저 나열된 마스크가 항상 우선합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

## 날짜 마스크가 있는 키워드 사용 정보 {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

일치하는 페이지가 인덱싱되는 방식에 영향을 주는 하나 이상의 공백으로 구분된 키워드로 각 포함 마스크를 평가할 수 있습니다.

쉼표는 마스크와 키워드 간의 구분 문자로 사용할 수 없습니다.공백만 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> 포함 마스크로 지정된 날짜 이전 또는 날짜가 지정된 페이지의 텍스트를 색인화하지 않으려면 
     다음과 같이 날짜 마스크 포함 후 <code>
       noindex 
     </code>: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>키워드가 마스크에서 공백으로 구분되도록 합니다. </p> <p>위의 예제에서는 검색 로봇이 10일 이전의 ".swf" 확장명을 가진 파일의 모든 링크를 따르도록 지정합니다. 그러나 이러한 파일에 포함된 모든 텍스트의 인덱싱을 비활성화합니다. </p> <p>이전 파일에 대한 텍스트가 색인이 되어 있지 않지만 해당 파일의 모든 링크를 따라가도록 할 수 있습니다. 이러한 경우 제외 날짜 마스크를 사용하는 대신 "noindex" 키워드와 함께 포함 날짜 마스크를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> 포함 마스크에 의해 지정된 날짜 이전 날짜 또는 날짜가 지정된 페이지의 텍스트를 색인화하고자 하지만 일치된 페이지의 링크를 따라가지 않으려면 
     다음과 같이 날짜 마스크 포함 후 <code>
       nofollow 
     </code>: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>키워드가 마스크에서 공백으로 구분되도록 합니다. </p> <p>Adobe의 
     <code>
       nofollow 
     </code> 키워드는 
     <code>
       content="nofollow" 
     </code> 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>마스크 포함 및 제외에 모두 사용됩니다. </p> <p>검색 로봇은 일반적으로 날짜 마스크를 확인하기 전에 모든 파일을 다운로드하고 파싱합니다. 이러한 동작은 일부 파일 유형이 파일 자체 내의 날짜를 지정할 수 있기 때문에 발생합니다. 예를 들어 HTML 문서에는 파일 날짜를 설정하는 메타 태그가 포함될 수 있습니다. </p> <p>날짜를 기준으로 많은 파일을 제외하고 서버에 불필요한 로드를 넣지 않으려면 
     날짜 마스크의 URL 뒤에 <code>
       server-date 
     </code>. </p> <p>이 키워드는 검색 로봇이 각 파일을 구문 분석하는 대신 서버에서 반환된 파일의 날짜를 신뢰하도록 합니다. 예를 들어 다음 제외 날짜 마스크는 HTTP 헤더에서 서버에서 반환한 날짜에 따라 문서가 90일 이상인 경우 URL과 일치하는 페이지를 무시합니다. </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> 서버에서 반환된 날짜가 90일 이상인 경우, 
     <code>
       server-date 
     </code>은 제외된 문서를 서버에서 다운로드할 수 없도록 지정합니다. 따라서 문서를 보다 빠르게 인덱싱하고 서버에 부담을 덜 수 있습니다. If 
     <code>
       server-date 
     </code>이(가) 지정되지 않은 경우 검색 로봇은 HTTP 헤더에서 서버에서 반환하는 날짜를 무시합니다. 대신 각 파일이 다운로드되고 검사되어 날짜가 지정되었는지 확인합니다. 파일에 지정된 날짜가 없으면 검색 로봇은 서버에서 반환한 날짜를 사용합니다. </p> <p>귀하는 
     파일에 서버 날짜를 재정의하는 명령이 포함된 경우 <code>
       server-date 
     </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 마스크 포함 및 제외 모두에 사용합니다. </p> <p>앞에 오는 모든 날짜 마스크 
     <code>
       regexp 
     </code>은(는) 정규 표현식으로 처리됩니다. </p> <p>검색 로봇이 제외 정규 표현식 날짜 마스크와 일치하는 파일을 발견하면 해당 파일을 색인화하지 않습니다. </p> <p>검색 로봇이 정규 표현식 날짜 마스크와 일치하는 파일을 발견하면 해당 문서를 인덱싱합니다. </p> <p>예를 들어 다음과 같은 날짜 마스크가 있다고 가정합니다. </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>마스크는 검색 로봇이 180일 이상의 일치하는 파일을 제외하도록 합니다. 즉, URL에 "archive"라는 단어가 포함된 파일입니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 웹 사이트 {#task_0010543C55F648D2B5DEFEFAD60FAF04}의 인덱스 부분에 날짜 마스크를 추가하거나 인덱스 부분을 포함하지 않음

[날짜 마스크]를 사용하여 파일의 연령을 기준으로 고객 검색 결과에서 파일을 포함하거나 제외할 수 있습니다.

**[!UICONTROL Test Date]** 및 **[!UICONTROL Test URL]** 필드를 사용하여 파일이 색인 후에 포함되어 있는지 여부를 테스트합니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 작성하십시오.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**웹 사이트의 일부를 색인화하거나 색인화하지 않고 날짜 마스크를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Date Masks] 페이지의 **[!UICONTROL Test Date]** 필드에 YYYY-MM-DD 형식(예: `2011-07-25`) 날짜를 입력합니다.**[!UICONTROL Test URL]** 필드에 웹 사이트의 URL 마스크를 입력한 다음 **[!UICONTROL Test]**&#x200B;를 클릭합니다.
1. [!DNL Date Masks] 필드에 줄당 하나의 날짜 마스크 주소를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 암호 {#concept_3EDBD731725D46B891F834D4472774DC} 정보

HTTP 기본 인증을 통해 보호되는 웹 사이트의 일부에 액세스하려면 암호를 하나 이상 추가할 수 있습니다.

고객이 암호 설정의 효과를 볼 수 있으려면 먼저 사이트 색인을 다시 구성해야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

[!DNL Passwords] 페이지에서 각 암호를 한 줄에 입력합니다. 암호는 다음 예제와 같이 URL 또는 영역, 사용자 이름 및 암호로 구성됩니다.

```
https://www.mydomain.com/ myname mypassword
```

위와 같이 URL 경로를 사용하는 대신 영역을 지정할 수도 있습니다.

사용할 올바른 영역을 결정하려면 브라우저에서 암호로 보호된 웹 페이지를 열고 &quot;네트워크 암호 입력&quot; 대화 상자를 확인합니다.

![](assets/realms.gif)

이 경우 영역 이름은 &quot;내 사이트 영역&quot;입니다.

위의 영역 이름을 사용하면 암호가 다음과 같이 표시될 수 있습니다.

```
My Site Realm myusername mypassword
```

웹 사이트에 여러 영역이 있는 경우 다음 예제와 같이 별도의 행에 각 영역에 대한 사용자 이름과 암호를 입력하여 여러 암호를 만들 수 있습니다.

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

URL 또는 영역을 포함하는 암호를 혼합하여 암호 목록이 다음과 같이 표시되도록 할 수 있습니다.

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

위의 목록에서 서버의 인증 요청과 일치하는 영역 또는 URL이 포함된 첫 번째 암호가 사용됩니다. `https://www.mysite.com/path1/path2/index.html`의 파일이 `Realm3`에 있더라도, 예를 들어 URL로 정의된 암호가 영역에 정의된 암호 위에 나열되기 때문에 `name2` 및 `password2`이(가) 사용됩니다.

## 인증 {#task_DED19D476FF04B48BB6456D5ECB8628A}이 필요한 웹 사이트 영역에 액세스하기 위한 암호 추가

암호를 사용하여 검색 및 색인 작업을 위해 웹 사이트의 암호로 보호된 영역에 액세스할 수 있습니다.

암호의 효과가 고객에게 추가되기 전에 사이트 색인을 다시 작성하십시오

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**인증이 필요한 웹 사이트 영역에 액세스하기 위한 암호를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**&#x200B;를 클릭합니다.
1. [!DNL Passwords] 페이지의 **[!UICONTROL Passwords]** 필드에 영역 또는 URL, 연관된 사용자 이름 및 암호를 공백으로 구분하여 입력합니다.

   영역 암호 및 개별 줄에 있는 URL 암호의 예:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   한 줄에 암호를 하나만 추가합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 콘텐트 유형 {#concept_6FEA1355C0374500B4C53090C34A8A07} 정보

[!DNL Content Types]을 사용하여 이 계정에 대해 크롤링하고 색인화할 파일 유형을 선택할 수 있습니다.

크롤링 및 색인화하도록 선택할 수 있는 컨텐츠 유형에는 PDF 문서, 텍스트 문서, Adobe Flash 동영상, Word, Excel 및 Powerpoint와 같은 Microsoft Office 애플리케이션의 파일 및 MP3 파일의 텍스트가 포함됩니다. 선택한 컨텐츠 유형 내에 있는 텍스트는 웹 사이트의 다른 모든 텍스트와 함께 검색됩니다.

고객이 컨텐츠 유형 설정의 효과를 볼 수 있으려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

## MP3 음악 파일 색인 만들기 정보 {#section_AD2E28BEEE3E46629E2B05C34A963673}

[!DNL Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]** 옵션을 선택하면 MP3 파일이 2가지 방법 중 하나로 크롤링 및 인덱싱됩니다. 가장 일반적인 방법은 다음과 같이 HTML 파일의 앵커 href 태그에서 가져온 것입니다.

```
<a href="MP3-file-URL"></a>
```

두 번째 방법은 MP3 파일의 URL을 URL 시작 지점으로 입력하는 것입니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

MP3 파일은 MIME 유형 &quot;audio/mpeg&quot;로 인식됩니다.

MP3 음악 파일 크기는 보통 적은 양의 텍스트만 포함되더라도 꽤 클 수 있습니다. 예를 들어 MP3 파일은 앨범 이름, 아티스트 이름, 노래 제목, 노래 장르, 릴리스 연도 및 주석과 같은 항목을 선택적으로 저장할 수 있습니다. 이 정보는 파일의 맨 끝에 TAG라는 이름으로 저장됩니다. 태그 정보가 포함된 MP3 파일은 다음과 같은 방식으로 인덱싱됩니다.

* 노래 제목은 HTML 페이지의 제목처럼 처리됩니다.
* 주석은 HTML 페이지에 대해 정의된 설명으로 처리됩니다.
* 이 장르는 HTML 페이지에 대해 정의된 키워드로 취급됩니다.
* 아티스트 이름, 앨범 이름 및 릴리스 연도는 HTML 페이지의 본문처럼 처리됩니다.

웹 사이트에서 크롤링 및 인덱싱된 각 MP3 파일은 하나의 페이지로 계산됩니다.

웹 사이트에 많은 MP3 파일이 포함되어 있는 경우 계정에 대한 색인 바이트 제한을 초과할 수 있습니다. 이러한 경우 [!DNL Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]**&#x200B;을 선택 해제하여 웹 사이트에 있는 모든 MP3 파일의 인덱싱을 방지할 수 있습니다.

웹 사이트에서 특정 MP3 파일의 색인화를 방지하려면 다음 중 하나를 수행할 수 있습니다.

* MP3 파일에 연결된 앵커 태그를 `<nofollow>` 및 `</nofollow>` 태그로 둘러싸십시오. 검색 로봇은 이러한 태그 사이의 링크를 따라가지 않습니다.

* MP3 파일의 URL을 제외 마스크로 추가합니다.

   [URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

## 크롤링 및 색인화할 내용 유형 선택{#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

[!DNL Content Types]을 사용하여 이 계정에 대해 크롤링하고 색인화할 파일 유형을 선택할 수 있습니다.

크롤링 및 색인화하도록 선택할 수 있는 컨텐츠 유형에는 PDF 문서, 텍스트 문서, Adobe Flash 동영상, Word, Excel 및 Powerpoint와 같은 Microsoft Office 애플리케이션의 파일 및 MP3 파일의 텍스트가 포함됩니다. 선택한 컨텐츠 유형 내에 있는 텍스트는 웹 사이트의 다른 모든 텍스트와 함께 검색됩니다.

고객이 컨텐츠 유형 설정의 효과를 볼 수 있으려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

중국어, 일본어 또는 한국어 MP3 파일을 크롤링 및 색인하려면 아래 단계를 완료하십시오. 그런 다음 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;에서 MP3 파일을 인코딩하는 데 사용할 문자 세트를 지정합니다.

[주입 정보](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)를 참조하십시오.

**크롤링 및 색인화할 컨텐츠 유형을 선택하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;를 클릭합니다.
1. [!DNL Content Types] 페이지에서 웹 사이트에서 크롤링하고 색인화할 파일 유형을 확인합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 연결 정보 {#concept_E2F3B7E7521147479E5948A94BB3A40B}

연결을 사용하여 검색 로봇이 웹 사이트를 색인화하는 데 사용하는 최대 10개의 HTTP 연결을 추가할 수 있습니다.

연결 수를 늘리면 크롤링 및 색인을 완료하는 데 소요되는 시간을 크게 줄일 수 있습니다. 그러나 각 추가 연결은 서버의 로드를 증가시킵니다.

## 색인 속도를 높이는 연결 추가 {#task_3E9B83E43C1842A19066355A15C4A6FB}

연결을 사용하여 Crawler가 사용하는 동시 HTTP 연결 수를 늘려 웹 사이트를 색인화하는 데 걸리는 시간을 줄일 수 있습니다. 최대 10개의 연결을 추가할 수 있습니다.

각 추가 연결은 서버에 배치된 로드를 증가시킵니다.

**색인 속도를 높이기 위해 연결을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**&#x200B;를 클릭합니다.
1. [!DNL Parallel Indexing Connections] 페이지의 **[!UICONTROL Number of Connections]** 필드에 추가할 연결 수(1-10)를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 양식 제출 정보 {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

양식 제출을 사용하면 웹 사이트에서 양식을 인식하고 처리할 수 있습니다.

웹 사이트의 크롤링 및 색인 작성 시 발견된 각 양식이 추가한 양식 정의와 비교됩니다. 양식이 양식 정의와 일치하면 색인화를 위해 양식이 제출됩니다. 양식이 두 개 이상의 정의와 일치하면 일치하는 각 정의에 대해 양식이 한 번 제출됩니다.

## 웹 사이트 {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}에서 양식을 인덱싱하기 위한 양식 정의 추가

[!DNL Form Submission]을 사용하여 색인 작업을 위해 웹 사이트에서 인식되는 양식을 처리할 수 있습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 작성해야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**웹 사이트에서 양식을 인덱싱하기 위한 양식 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 **[!UICONTROL Add New Form]**&#x200B;을 클릭합니다.
1. [!DNL Add Form Definition] 페이지에서 [!DNL Form Recognition] 및 [!DNL Form Submission] 옵션을 설정합니다.

   [!DNL Form Definition] 페이지의 [!DNL Form Recognition] 섹션에 있는 5가지 옵션은 처리할 수 있는 웹 페이지의 양식을 식별하는 데 사용됩니다.

   [!DNL Form Submission] 섹션의 3가지 옵션은 양식을 웹 서버에 제출할 매개 변수와 값을 지정하는 데 사용됩니다.

   한 줄에 하나의 인식 또는 제출 매개 변수를 입력합니다. 각 매개 변수에는 이름과 값이 포함되어야 합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>양식 인식</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>페이지 URL 마스크 </p> </td> 
      <td colname="col2"> <p>양식이 포함된 웹 페이지 또는 페이지를 식별합니다. 단일 페이지에 나타나는 양식을 식별하려면 다음 예제와 같이 해당 페이지의 URL을 입력합니다. </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>여러 페이지에 나타나는 양식을 식별하려면 와일드카드를 사용하여 페이지를 설명하는 URL 마스크를 지정합니다. 예를 들어 <code> https://www.mydomain.com/register/ </code> 아래의 ASP 페이지에서 발견된 양식을 식별하려면 다음을 지정합니다. </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>일반 표현식을 사용하여 여러 페이지를 식별할 수도 있습니다. JavaScript 파일에 
      다음 예제와 같이 URL 마스크 앞에 <code>
        regexp 
      </code> 키워드를 추가합니다. </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 URL 마스크 </p> </td> 
      <td colname="col2"> <p>의 작업 속성을 식별합니다. 
      <code>
        &lt;form&gt; 
      </code> 태그. </p> <p>페이지 URL 마스크와 마찬가지로 작업 URL 마스크는 단일 URL, 와일드카드가 있는 URL 또는 정규 표현식을 취할 수 있습니다. </p> <p>URL 마스크는 다음 중 하나일 수 있습니다. 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 다음과 같은 전체 경로:<code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 다음과 같은 부분 경로:<code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 다음과 같이 와일드카드를 사용하는 URL:<code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 다음과 같은 정규 표현식.<code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URL 마스크 또는 작업 URL 마스크로 식별되는 페이지의 텍스트를 색인화하지 않으려는 경우 또는 링크를 해당 페이지에서 따라가지 않으려면 
      <code>
        noindex 
      </code> 및 
      <code>
        nofollow 
      </code> 키워드. URL 마스크 또는 진입점을 사용하여 이러한 키워드를 마스크에 추가할 수 있습니다. </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> URL 시작 지점 </a>을 참조하십시오. </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URL 마스크 정보 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>양식 이름 마스크 </p> </td> 
      <td colname="col2"> <p>양식을 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그에는 name 특성이 있습니다. </p> <p>간단한 이름( 
      <code>
        login_form 
      </code>), 와일드카드( 
      <code>
        form* 
      </code>) 또는 정규식( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>일반적으로 양식에 이름 특성이 없으므로 이 필드를 비워 둘 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>양식 ID 마스크 </p> </td> 
      <td colname="col2"> <p>양식을 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그에는 id 특성이 있습니다. </p> <p>간단한 이름( 
      <code>
        login_form 
      </code>), 와일드카드( 
      <code>
        form* 
      </code>) 또는 정규식( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>일반적으로 양식에 이름 특성이 없으므로 이 필드를 비워 둘 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>이름이 지정된 매개 변수 또는 지정된 값이 있는 명명된 매개 변수를 포함하거나 포함하지 않는 양식을 식별합니다. </p> <p>예를 들어, rick_brough@mydomain.com에 사전 설정된 전자 메일 매개 변수(암호 매개 변수)를 포함하는 양식을 식별하려면 한 줄에 하나씩 다음 매개 변수 설정을 지정합니다. </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>양식 제출</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 URL 재정의 </p> </td> 
      <td colname="col2"> <p>양식 제출의 대상이 양식의 작업 속성에 지정된 내용과 다른 시점을 지정합니다. </p> <p>예를 들어 양식에서 찾은 URL 값과 다른 URL 값을 생성하는 JavaScript 함수를 통해 양식을 전송할 때 이 옵션을 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>메서드 재정의 </p> </td> 
      <td colname="col2"> <p>양식 제출의 대상이 양식의 action 속성에 사용되는 내용과 다른 시기와 JavaScript 제출을 통해 메서드를 변경한 시기를 지정합니다. </p> <p>모든 양식 매개 변수의 기본값( 
      <code>
        &lt;input&gt; 
      </code> 태그(숨김 필드 포함), 
      <code>
        &lt;option&gt; 
      </code> 
      <code>
        &lt;select&gt; 
      </code> 태그와 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> 태그)는 웹 페이지에서 읽습니다. 그러나 <span class="uicontrol"> 매개 변수 </span> 필드의 <span class="wintitle"> 양식 제출 </span> 섹션에 나열된 모든 매개 변수는 양식 기본값으로 대체됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>양식 제출 매개 변수에 
      <code>
        not 
      </code> 키워드. </p> <p>매개 변수에 
      <code>
        not 
      </code> 양식 제출의 일부로 제출되지 않습니다. 이 동작은 선택을 취소하여 전송해야 하는 확인란에 유용합니다. </p> <p>예를 들어 다음 매개 변수를 제출한다고 가정합니다. </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 값이 있는 전자 메일 매개 변수 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 값이 있는 password 매개 변수 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckbox 매개 변수는 선택 취소로 표시됩니다. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>기타 모두 
      <code>
        &lt;form&gt; 
      </code> 매개 변수를 기본값으로 지정 </p> </li> 
      </ul> </p> <p>양식 제출 매개 변수는 다음과 같습니다. </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>의 메서드 특성 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그는 GET 메서드 또는 POST 메서드를 사용하여 데이터가 서버로 전송되는지 결정하는 데 사용됩니다. </p> <p>JavaScript 파일 내의 
      <code>
        &lt;form&gt; 
      </code> 태그에 메서드 특성이 없습니다. 양식은 GET 메서드를 사용하여 제출됩니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 양식 정의 {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314} 편집

웹 사이트의 양식이 변경되었거나 정의를 변경해야 하는 경우 기존 양식 정의를 편집할 수 있습니다.

[!DNL Form Submission] 페이지에 양식 정의에 적용한 변경 내용을 되돌리기 위한 [!DNL History] 기능이 없습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 작성해야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**양식 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 업데이트할 양식 정의 오른쪽에 있는 **[!UICONTROL Edit]**&#x200B;을 클릭합니다.
1. [!DNL Edit Form Definition] 페이지에서 [!DNL Form Recognition] 및 [!DNL Form Submission] 옵션을 설정합니다.

   웹 사이트](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F)에서 양식을 인덱싱하기 위한 양식 정의 추가 아래의 옵션 표를 참조하십시오.[
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 양식 정의 {#task_C350FC0CDE344F2786215D544C048B5E} 삭제

양식이 웹 사이트에 더 이상 존재하지 않거나 특정 양식을 처리 및 색인화하지 않으려는 경우 기존 양식 정의를 삭제할 수 있습니다.

[!DNL Form Submission] 페이지에 양식 정의에 적용한 변경 내용을 되돌리기 위한 [!DNL History] 기능이 없습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 작성해야 합니다.

스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[

**양식 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 제거할 양식 정의 오른쪽에 있는 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.

   삭제할 올바른 양식 정의를 선택해야 합니다. 다음 단계에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭하면 삭제 확인 대화 상자가 없습니다.
1. [!DNL Delete Form Definition] 페이지에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 색인 커넥터 정보 {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

XML 페이지 또는 모든 종류의 피드를 인덱싱하기 위해 [!DNL Index Connector]을 사용하여 추가 입력 소스를 정의합니다.

데이터 피드 입력 소스를 사용하여 웹 사이트에서 일반적으로 검색된 내용과 다른 양식에 저장된 컨텐츠에 액세스할 수 있습니다. 이 방법은 사용 가능한 크롤링 메서드 중 하나를 사용합니다. 크롤링 및 직접 인덱싱된 각 문서는 웹 사이트의 컨텐츠 페이지에 해당합니다. 그러나 데이터 피드는 XML 문서 또는 쉼표 또는 탭으로 구분된 텍스트 파일에서 가져오며 색인화할 컨텐츠 정보를 포함합니다.

XML 데이터 소스는 개별 문서에 해당하는 정보를 포함하는 XML 표준 또는 레코드로 구성됩니다. 이러한 개별 문서는 색인에 추가됩니다. 텍스트 데이터 피드에는 개별 문서에 해당하는 새 라인으로 구분된 개별 레코드가 포함되어 있습니다. 이러한 개별 문서도 색인에 추가됩니다. 두 경우 모두 색인 커넥터 구성은 피드를 해석하는 방법을 설명합니다. 각 구성에서는 파일이 있는 위치와 서버가 파일에 액세스하는 방법을 설명합니다. 이 구성에서는 &quot;매핑&quot; 정보도 설명합니다. 즉, 각 레코드의 항목이 결과 인덱스의 메타데이터 필드를 채우는 데 사용되는 방법입니다.

[!DNL Staged Index Connector Definitions] 페이지에 색인 커넥터 정의를 추가하면 이름 또는 유형 값에 대해 *을 제외한 모든 구성 설정을 변경할 수 있습니다.*

[!DNL Index Connector] 페이지에는 다음 정보가 표시됩니다.

* 구성하고 추가한 정의된 색인 커넥터의 이름입니다.
* 추가한 각 커넥터에 대해 다음 데이터 소스 유형 중 하나:

   * **텍스트**  - 간단한 &quot;일반&quot; 파일, 쉼표로 구분된 파일, 탭으로 구분된 형식 또는 다른 일관되게 구분된 형식.
   * **피드**  - XML 피드.
   * **XML**  - XML 문서 모음.

* 커넥터가 다음 크롤링 및 색인 작업을 위해 활성화되었는지 여부입니다.
* 데이터 소스의 주소입니다.

[색인 커넥터 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84) 참조

## 색인 커넥터 {#section_E059A33D61EE4DB0972A37B8A35E9E16}의 텍스트 및 피드 구성에서 색인 작성 프로세스가 작동하는 방식

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>단계 </p> </th> 
   <th colname="col2" class="entry"> <p>프로세스 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드합니다. </p> </td> 
   <td colname="col3"> <p>텍스트 및 피드 구성의 경우 간단한 파일 다운로드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>다운로드한 데이터 소스를 개별 의사 문서로 분류합니다. </p> </td> 
   <td colname="col3"> <p><span class="uicontrol"> 텍스트 </span>의 경우 각 줄바꿈 구분 텍스트 줄은 개별 문서에 해당하며, 쉼표 또는 탭과 같은 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p><span class="uicontrol"> 피드 </span>의 경우 각 문서의 데이터는 다음 형식의 정규 표현식 패턴을 사용하여 추출됩니다. </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle"> 색인 커넥터 추가 </span> 페이지에서 <span class="uicontrol"> 매핑 </span>을(를) 사용하여 데이터의 캐시된 복사본을 만든 다음 크롤러에 대한 링크 목록을 만듭니다. 데이터는 로컬 캐시에 저장되고 구성된 필드로 채워집니다. </p> <p>파싱된 데이터는 로컬 캐시에 기록됩니다. </p> <p>이 캐시는 나중에 읽어서 Crawler가 필요한 간단한 HTML 문서를 만듭니다. 예: </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span> 요소는 제목 메타데이터 필드에 매핑이 있을 때만 생성됩니다. 마찬가지로 <span class="codeph"> &lt;body&gt; </span> 요소는 본문 메타데이터 필드에 매핑이 있을 때만 생성됩니다. </p> <p> <b>중요</b>:사전 정의된 URL 메타 태그에 값을 할당할 수는 없습니다. </p> <p>다른 모든 매핑의 경우, <span class="codeph"> &lt;meta&gt; </span> 태그가 원본 문서에서 찾은 데이터가 있는 각 필드에 대해 생성됩니다. </p> <p>각 문서에 대한 필드가 캐시에 추가됩니다. 캐시에 기록되는 각 문서에 대해 다음 예와 같이 링크가 생성됩니다. </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>구성의 매핑에는 기본 키로 식별되는 필드가 하나만 있어야 합니다. 이 매핑은 캐시에서 데이터를 가져올 때 사용되는 키를 형성합니다. </p> <p>크롤러는 URL <span class="codeph"> 인덱스를 인식합니다.</span> 스키마 접두어를 사용하여 로컬에 캐시된 데이터에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>캐시된 문서 집합을 크롤링합니다. </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 인덱스:</span> 링크는 Crawler의 보류 중인 목록에 추가되고 일반 크롤링 시퀀스에서 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>각 문서를 처리합니다. </p> </td> 
   <td colname="col3"> <p>각 링크의 키 값은 캐시에 있는 항목에 해당되므로 각 링크를 검색하면 캐시에서 해당 문서의 데이터를 가져옵니다. 그런 다음 HTML 이미지로 "어셈블됨"이 처리되어 색인에 추가됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 색인 커넥터 {#section_7F1551EA51854C5C99F284CE260526EB}의 XML 구성에서 색인 작성 프로세스가 작동하는 방식

XML 구성의 인덱싱 프로세스는 다음과 같은 사소한 변경 사항 및 예외 사항이 있는 텍스트 및 피드 구성 프로세스와 유사합니다.

XML 크롤에 대한 문서는 이미 개별 파일로 분리되어 있으므로 위 표의 1단계와 2단계는 직접 적용되지 않습니다. **[!UICONTROL Host Address]** 및 [!DNL Index Connector Add] 페이지의 **[!UICONTROL File Path]** 필드에 URL을 지정하면 이 URL이 다운로드되고 일반 HTML 문서로 처리됩니다. 다운로드 문서에는 처리된 XML 문서를 가리키는 `<a href="{url}"...` 링크의 컬렉션이 포함되어 있을 것으로 예상됩니다. 이러한 링크는 다음 양식으로 변환됩니다.

```
<a href="index:<ic_config_name>?url="{url}">
```

예를 들어 Adobe 설정이 다음 링크를 반환한 경우:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

위의 표에서 3단계는 적용되지 않으며 4단계는 크롤링 및 색인 작성 시 완료됩니다.

또는 크롤링 프로세스를 통해 자연스럽게 발견된 다른 문서와 XML 문서를 혼합할 수 있습니다. 이러한 경우 다시 작성 규칙( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**)을 사용하여 XML 문서의 URL을 변경하여 색인 커넥터에 연결할 수 있습니다.

[크롤링 목록 검색 URL 규칙 검색 정보](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)를 참조하십시오.

예를 들어 다음과 같은 다시 작성 규칙이 있다고 가정해 봅시다.

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

이 규칙은 `.xml`으로 끝나는 모든 URL을 색인 커넥터 링크로 변환합니다. crawler는 `index:` URL 스키마를 인식하고 다시 씁니다. 다운로드 프로세스는 기본 Index Connector Apache 서버를 통해 리디렉션됩니다. 다운로드된 각 문서는 피드에 사용되는 동일한 정규 표현식 패턴을 사용하여 검사됩니다. 그러나 이 경우 제작된 HTML 문서는 캐시에 저장되지 않습니다. 대신 색인 처리를 위해 크롤러에 직접 전달됩니다.

## 여러 색인 커넥터 구성 방법 {#section_C2B14C0F06354A57AEF6238FF3814E5D}

모든 계정에 대해 여러 색인 커넥터 구성을 정의할 수 있습니다. 다음 그림과 같이 **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]**&#x200B;의 드롭다운 목록에 구성이 자동으로 추가됩니다.

![](assets/url_entrypoints_index_connector.png)

드롭다운 목록에서 구성을 선택하면 URL 시작 지점 목록의 끝에 값이 추가됩니다.

>[!NOTE]
>
>비활성화된 색인 커넥터 구성이 드롭다운 목록에 추가되지만 선택할 수 없습니다. 동일한 색인 커넥터 구성을 두 번 선택하면 목록 끝에 해당 구성이 추가되고 이전 인스턴스가 삭제됩니다.

증분 크롤에 대한 색인 커넥터 진입점을 지정하려면 다음 형식을 사용하여 항목을 추가할 수 있습니다.

```
index:<indexconnector_configuration_name>
```

색인 커넥터 페이지에 있는 각 추가 항목이 발견되고 활성화된 경우 크롤러는 이를 처리합니다.

참고:각 문서의 URL은 색인 커넥터 구성 이름 및 문서의 기본 키를 사용하여 구성되므로 증분 업데이트를 수행할 때 동일한 색인 커넥터 구성 이름을 사용해야 합니다. 이렇게 하면 [!DNL Adobe Search&Promote]이(가) 이전에 인덱싱된 문서를 올바르게 업데이트할 수 있습니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)도 참조하십시오.

**색인 커넥터를 추가할 때 설정 맵 사용**

색인 커넥터를 추가할 때 **[!UICONTROL Setup Maps]** 기능을 사용하여 데이터 소스의 샘플을 다운로드할 수도 있습니다. 색인화 적합성에 대해 데이터가 검토됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>색인 커넥터 유형을 선택한 경우.. </p> </th> 
   <th colname="col2" class="entry"> <p>설정 맵 기능... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>텍스트 </p> </td> 
   <td colname="col2"> <p>탭을 먼저 시도한 다음 세로 막대( <span class="codeph">)를 사용하여 구분 기호 값을 결정합니다. | </span>) 및 마지막으로 쉼표( <span class="codeph"> , </span>). <span class="uicontrol"> 설정 맵 </span>을(를) 클릭하기 전에 구분 기호 값을 이미 지정한 경우 이 값이 대신 사용됩니다. </p> <p>최적의 구성표는 맵 필드에서 적절한 태그 및 필드 값을 추측으로 채웁니다. 또한 파싱된 데이터의 샘플링이 표시됩니다. 파일에 머리글 행이 포함되어 있다는 것을 알고 있는 경우 첫 번째 행 <span class="uicontrol"> 헤더에 반드시 </span> 머리글을 선택합니다. 설정 함수는 이 정보를 사용하여 결과 맵 항목을 더 잘 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>피드 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드하고 간단한 XML 파싱을 수행합니다. </p> <p>결과 XPath 식별자는 맵 테이블의 태그 행에 표시되며, 필드 값도 유사합니다. 이러한 행은 사용 가능한 데이터만 식별하고 더 복잡한 XPath 정의를 생성하지 않습니다. 그러나 XML 데이터를 설명하고 Itemtag 값을 식별하므로 여전히 유용합니다. </p> <p> <p>참고: 설정 맵 함수는 전체 XML 소스를 다운로드하여 분석을 수행합니다. 파일이 크면 이 작업이 시간 초과될 수 있습니다. </p> </p> <p>이 함수는 성공 시 사용할 수 없는 모든 XPath 항목을 식별합니다. 결과 맵 정의를 검토하고 필요 없거나 원하는 맵 정의를 제거해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>기본 링크 목록이 아니라 대표 개별 문서의 URL을 다운로드합니다. 이 단일 문서는 피드에 사용된 것과 동일한 메커니즘을 사용하여 구문 분석되고 결과가 표시됩니다. </p> <p><span class="uicontrol"> </span> 추가를 클릭하여 구성을 저장하려면 먼저 URL을 다시 기본 링크 목록 문서로 변경해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**중요**:파일 파서가 전체 파일을 메모리에 읽으려고 하므로 큰 XML 데이터 세트에서 설정 맵 기능을 사용할 수 없습니다. 결과적으로 메모리 부족 문제가 발생할 수 있습니다. 그러나 색인 작성 시 동일한 문서를 처리할 때 메모리에 읽을 수는 없습니다. 대신 대용량 문서는 &quot;이동 중&quot;에 처리되며 메모리에 처음부터 완전히 읽을 수는 없습니다.

**색인 커넥터를 추가할 때 미리 보기 사용**

색인 커넥터를 추가할 때 저장 중인 것처럼 **[!UICONTROL Preview]** 기능을 사용하여 데이터의 유효성을 검사할 수도 있습니다. 구성에 대해 테스트를 실행하지만 구성을 계정에 저장하지 않습니다. 테스트는 구성된 데이터 소스에 액세스합니다. 그러나 다운로드 캐시는 임시 위치에 씁니다.인덱싱 크롤러가 사용하는 기본 캐시 폴더와 충돌하지 않습니다.

미리 보기는 Acct:IndexConnector-Preview-Max-Documents에 의해 제어되는 5개의 문서 중 기본값인 5개만 처리합니다. 미리 본 문서는 인덱싱 크롤러에 제공되므로 소스 양식으로 표시됩니다. 이 표시는 웹 브라우저의 &quot;소스 보기&quot; 기능과 유사합니다. 표준 탐색 링크를 사용하여 미리 보기 세트에서 문서를 탐색할 수 있습니다.

이러한 문서는 직접 처리되고 캐시에 다운로드되지 않으므로 미리 보기는 XML 구성을 지원하지 않습니다.

## 색인 커넥터 정의 {#task_96779B651A654E1F871F55D6DBBC8886} 추가

각 색인 커넥터 구성은 데이터 소스 및 매핑을 정의하여 해당 소스에 대해 정의된 데이터 항목을 인덱스의 메타데이터 필드에 연결합니다.

새 정의 및 활성화된 정의의 효과가 고객에게 표시되기 전에 사이트 색인을 다시 작성하십시오.

**색인 커넥터 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Stage Index Connector Definitions] 페이지에서 **[!UICONTROL Add New Index Connector]**&#x200B;을 클릭합니다.
1. [!DNL Index Connector Add] 페이지에서 원하는 커넥터 옵션을 설정합니다. 사용 가능한 옵션은 선택한 **[!UICONTROL Type]**&#x200B;에 따라 다릅니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>이름 </p> </td> 
      <td colname="col2"> <p>색인 커넥터 구성의 고유한 이름입니다. 영숫자 문자를 사용할 수 있습니다. "_" 및 "-" 문자도 허용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p>데이터의 소스. 선택하는 데이터 소스 유형은 <span class="wintitle"> 색인 커넥터 추가 </span> 페이지에서 사용할 수 있는 결과 옵션에 영향을 줍니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> 텍스트 </span> <p>간단한 플랫 텍스트 파일, 쉼표로 구분된 형식, 탭으로 구분된 형식 또는 다른 일관되게 구분된 형식. 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p>열 번호에서 참조하는 각 값 또는 열을 1부터 메타데이터 필드에 매핑할 수 있습니다. </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> 피드 </span> <p>여러 개의 "행" 정보가 포함된 기본 XML 문서를 다운로드합니다. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>링크가 포함된 기본 XML 문서( 
      <code>
        &lt;a&gt; 
      </code>)을 개별 XML 문서에 연결합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형:텍스트</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>:비활성화된 색인 커넥터 구성은 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예제와 같이 데이터 소스 문서의 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>또는  </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다. </p> <p>데이터 소스 파일이 있는 호스트 시스템의 IP 주소 또는 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>간단한 플랫 텍스트 파일, 쉼표로 구분된 파일, 탭으로 구분 또는 다른 일관되게 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>증분 파일 경로 </p> </td> 
      <td colname="col2"> <p>간단한 플랫 텍스트 파일, 쉼표로 구분된 파일, 탭으로 구분 또는 다른 일관되게 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 증분 색인 작업 중에 다운로드 및 처리됩니다. 파일을 지정하지 않으면 파일 경로 아래에 나열된 파일이 대신 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>세로 파일 경로 </p> </td> 
      <td colname="col2"> <p>세로 업데이트 중에 사용할 간단한 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 다른 일관되게 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 세로 업데이트 작업 중에 다운로드 및 처리됩니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 삭제 </p> </td> 
      <td colname="col2"> <p>행당 단일 문서 식별자 값을 포함하는 간단한 플랫 텍스트 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 증분 색인 작업 중에 다운로드 및 처리됩니다. 이 파일에 있는 값은 이전에 인덱싱된 문서를 제거하기 위해 "삭제" 요청을 구성하는 데 사용됩니다. 이 파일의 값은 <span class="uicontrol"> 기본 키 </span>로 식별되는 열에서 전체 또는 증분 파일 경로 파일에 있는 값과 일치해야 합니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용되는 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>필요한 경우 HTTP 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>필요한 경우 HTTPS 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간 초과 </p> </td> 
      <td colname="col2"> <p>FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 시간 초과(초)를 지정합니다. 이 값은 30에서 300 사이여야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다시 시도 </p> </td> 
      <td colname="col2"> <p>실패한 FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 최대 재시도 횟수를 지정합니다. 이 값은 0에서 10 사이여야 합니다. </p> <p>값이 0(0)이면 다시 시도하지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>인코딩 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일에 사용되는 문자 인코딩 시스템을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구분 기호 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일의 각 필드를 지정하는 데 사용할 문자를 지정합니다. </p> <p>쉼표 문자( <span class="codeph"> , </span>)는 구분 기호의 예입니다. 쉼표는 지정된 데이터 소스 파일에서 데이터 필드를 구분하는 데 도움이 되는 필드 구분 기호로 사용됩니다. </p> <p><span class="uicontrol"> 탭을 선택하십시오. </span> 를 클릭하여 가로 탭 문자를 구분 기호로 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 행의 머리글 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일의 첫 번째 행에 데이터가 아닌 헤더 정보만 포함됨을 나타냅니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>색인화를 위한 최소 문서 수 </p> </td> 
      <td colname="col2"> <p>양수 값으로 설정된 경우 다운로드한 파일에 필요한 최소 레코드 수를 지정합니다. 받는 레코드 수가 적으면 색인 작업이 중단됩니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> <p> <b>참고</b>:이 기능은 전체 색인 작업 중에만 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정합니다. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 열 </span> <p> 열 번호를 지정합니다. 첫 번째 열은 1입니다. 각 열에 대한 새 맵 행을 추가하려면 <span class="wintitle"> 작업 </span> 아래에서 <span class="uicontrol"> + </span>을 클릭합니다. </p> <p>데이터 소스의 각 열을 참조할 필요가 없습니다. 대신 값을 건너뛰도록 선택할 수 있습니다. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>이(가) 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>원하는 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 스크립트 필터링 </span>에서 사용하는 내용을 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보를 참조하십시오 </a>. </p> <p>색인 커넥터가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 해당 필드에는 <span class="wintitle"> 허용 목록 </span> 특성이 설정되어 있습니다. 이 경우, 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서를 색인에 추가할 때 나타나는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 색인 커넥터 구성으로 표시된 모든 문서에서 고유해야 합니다. 발견된 모든 복본은 무시됩니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용하기 위한 단일 고유 값이 포함되어 있지 않지만 <i>이(가) 함께 취합한 두 개 이상의 필드가 고유 식별자에서</i>이 될 수 있는 경우, <span class="uicontrol"> 기본 키 </span> 열을 세로 막대("|")와 결합하여 <span class="uicontrol"> 기본 키 </span> 값을 정의할 수 있습니다. 값을 설정합니다. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML 제거?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형:피드</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>:비활성화된 색인 커넥터 구성은 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일이 있는 호스트 시스템의 IP 주소 또는 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 "행" 정보를 포함하는 기본 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>증분 파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 "행" 정보가 포함된 증분 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 증분 색인 작업 중에 다운로드 및 처리됩니다. 파일을 지정하지 않으면 파일 경로 아래에 나열된 파일이 대신 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>세로 파일 경로 </p> </td> 
      <td colname="col2"> <p>세로 업데이트 중에 사용할 여러 가지 정보의 스파스 "행"이 포함된 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 세로 업데이트 작업 중에 다운로드 및 처리됩니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 삭제 </p> </td> 
      <td colname="col2"> <p>행당 단일 문서 식별자 값을 포함하는 간단한 플랫 텍스트 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 증분 색인 작업 중에 다운로드 및 처리됩니다. 이 파일에 있는 값은 이전에 인덱싱된 문서를 제거하기 위해 "삭제" 요청을 구성하는 데 사용됩니다. 이 파일의 값은 <span class="uicontrol"> 기본 키 </span>로 식별되는 열에서 전체 또는 증분 파일 경로 파일에 있는 값과 일치해야 합니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용되는 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>필요한 경우 HTTP 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>필요한 경우 HTTPS 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 개별 XML 행을 식별하는 데 사용할 수 있는 XML 요소를 식별합니다. </p> <p>예를 들어 Adobe XML 문서의 다음 피드 조각에서 Itemtag 값은 <span class="codeph"> record </span>입니다. </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>색인화를 위한 최소 문서 수 </p> </td> 
      <td colname="col2"> <p>양수 값으로 설정된 경우 다운로드한 파일에 필요한 최소 레코드 수를 지정합니다. 받는 레코드 수가 적으면 색인 작업이 중단됩니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> <p> <b>참고</b>:이 기능은 전체 색인 작업 중에만 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>XPath 표현식을 사용하여 XML 요소-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> 태그 </span> <p>파싱된 XML 데이터의 XPath 표현을 지정합니다. 위의 Adobe XML 문서 예제를 사용하여 Itemtag 옵션 아래의 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 </span> 특성이 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다.<span class="codeph"> </span></p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 속성이 <span class="codeph"> title </span>인 </span> 레코드 <span class="codeph"> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 안에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 제목 </span> /&gt;. </span></p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 </span> 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> <span class="codeph">.</span> </span></span></p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 <span class="codeph"> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 본문 </span> /&gt;. </span></p> </li> 
      </ul> </p> <p>XPath는 비교적 복잡한 표기법입니다. 자세한 내용은 다음 위치에 있습니다. </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> 참조 </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> 필드 </span> <p>생성된 각 <span class="codeph"> &lt;meta&gt; </span> 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>이(가) 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>원하는 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 스크립트 필터링 </span>에서 사용하는 내용을 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보를 참조하십시오 </a>. </p> <p>색인 커넥터가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 해당 필드에는 <span class="wintitle"> 허용 목록 </span> 특성이 설정되어 있습니다. 이 경우, 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서를 색인에 추가할 때 나타나는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 색인 커넥터 구성으로 표시된 모든 문서에서 고유해야 합니다. 발견된 모든 복본은 무시됩니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용하기 위한 단일 고유 값이 포함되어 있지 않지만 <i>이(가) 함께 취합한 두 개 이상의 필드가 고유 식별자에서</i>할 수 있는 경우, <span class="uicontrol"> 기본 키 </span>를 여러 <span class="uicontrol"> 태그 </span> 정의와 세로 막대("|")를 결합하여 정의할 수 있습니다. 값을 설정합니다. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTML 제거?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 삭제에 사용하시겠습니까?  </span> <p>증분 색인 작업 중에 사용됩니다. 이 XPath 패턴과 일치하는 레코드를 사용하여 삭제할 항목을 식별합니다. 이러한 각 레코드에 대한 <span class="uicontrol"> 기본 키 </span> 값은 파일 삭제 경로와 같이 "삭제" 요청을 구성하는 데 사용됩니다. </p> <p> <b>참고</b>:이 기능은 기본적으로 활성화되어 있지 않습니다. 해당 기능을 사용하려면 기술 지원에 문의하십시오. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형:XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>:비활성화된 색인 커넥터 구성은 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일이 있는 호스트 시스템의 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>링크를 포함하는 기본 XML 문서의 경로를 지정합니다( 
      <code>
        &lt;a&gt; 
      </code>)을 개별 XML 문서에 연결합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용되는 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>필요한 경우 HTTP 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>필요한 경우 HTTPS 서버에 액세스하기 위해 적절한 인증 자격 증명을 입력할 수 있습니다. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> 파일 </li> 
      </ul> </p> <p> <b>참고</b>:프로토콜 설정은 호스트 주소 및/또는 파일 경로 필드에 지정된 정보가 있을 때만 사용됩니다. 개별 XML 문서는 URL 사양에 따라 HTTP 또는 HTTPS를 사용하여 다운로드됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 "행"을 정의하는 XML 요소를 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> 태그 </span> <p>파싱된 XML 데이터의 XPath 표현을 지정합니다. 위의 Adobe XML 문서 예제를 사용하여 Itemtag 옵션 아래에 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 </span> 특성이 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다.<span class="codeph"> </span></p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 속성이 <span class="codeph"> title </span>인 </span> 레코드 <span class="codeph"> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 안에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 제목 </span> /&gt;. </span></p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 </span> 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> <span class="codeph">.</span> </span></span></p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>이름 속성이 <span class="codeph"> description </span>인 </span> 레코드 <span class="codeph"> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 <span class="codeph"> 내용 </span> 특성이 메타데이터 필드 <span class="codeph"> 본문 </span> /&gt;. </span></p> </li> 
      </ul> </p> <p>XPath는 비교적 복잡한 표기법입니다. 자세한 내용은 다음 위치에 있습니다. </p> <p><a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> 참조 </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>이(가) 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>원하는 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 스크립트 필터링 </span>에서 사용하는 내용을 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보를 참조하십시오 </a>. </p> <p>색인 커넥터가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 해당 필드에는 <span class="wintitle"> 허용 목록 </span> 특성이 설정되어 있습니다. 이 경우, 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서를 색인에 추가할 때 나타나는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 색인 커넥터 구성으로 표시된 모든 문서에서 고유해야 합니다. 발견된 모든 복본은 무시됩니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용하기 위한 단일 고유 값이 포함되어 있지 않지만 <i>이(가) 함께 취합한 두 개 이상의 필드가 고유 식별자에서</i>할 수 있는 경우, <span class="uicontrol"> 기본 키 </span>를 여러 <span class="uicontrol"> 태그 </span> 정의와 세로 막대("|")를 결합하여 정의할 수 있습니다. 값을 설정합니다. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTML 제거?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) 데이터 소스의 샘플을 다운로드하려면 **[!UICONTROL Setup Maps]**&#x200B;을 클릭합니다. 색인화 적합성에 대해 데이터가 검토됩니다. 이 기능은 텍스트 및 피드 유형에만 사용할 수 있습니다.
1. (선택 사항) **[!UICONTROL Preview]**&#x200B;을 클릭하여 구성의 실제 작업을 테스트합니다. 이 기능은 텍스트 및 피드 유형에만 사용할 수 있습니다.
1. **[!UICONTROL Add]**&#x200B;을 클릭하여 [!DNL Index Connector Definitions] 페이지와 [!DNL URL Entrypoints] 페이지의 [!DNL Index Connector Configurations] 드롭다운 목록에 구성을 추가합니다.

   [URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.
1. [!DNL Index Connector Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]**&#x200B;을 클릭합니다.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 색인 커넥터 정의 {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9} 편집

정의한 기존 색인 커넥터를 편집할 수 있습니다.

>[!NOTE]
>
>색인 커넥터 이름 또는 [!DNL Type] 드롭다운 목록에서 유형 등의 일부 옵션을 변경할 수 없습니다.

**색인 커넥터 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 변경할 색인 커넥터 정의 이름을 보려면 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Edit] 페이지에서 원하는 옵션을 설정합니다.

   [색인 커넥터 정의 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)의 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]**&#x200B;을 클릭합니다.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 색인 커넥터 정의 {#task_D0B71A7426E54247BDB3468EC576D871} 설정 보기

기존 색인 커넥터 정의의 구성 설정을 검토할 수 있습니다.

색인 커넥터 정의를 [!DNL Index Connector Definitions] 페이지에 추가하면 해당 유형 설정을 변경할 수 없습니다. 대신 정의를 삭제한 다음 새로 추가해야 합니다.

**색인 커넥터 정의의 설정을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 검토하거나 편집할 색인 커넥터 정의 이름을 보려면 **[!UICONTROL Edit]**&#x200B;를 클릭합니다.

## 색인 커넥터 정의 {#task_3AD55DF07FC44A748D0EFDAB7B35699B} 복사

기존 색인 커넥터 정의를 복사하여 새로 만들 색인 커넥터에 대한 기초로 사용할 수 있습니다.

색인 커넥터 정의를 복사할 때 복사된 정의는 기본적으로 비활성화됩니다. 정의를 활성화 또는 &quot;켜기&quot;하려면 [!DNL Index Connector Edit] 페이지에서 해당 정의를 편집하고 **[!UICONTROL Enable]**&#x200B;를 선택합니다.

[색인 커넥터 정의 편집](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)을 참조하십시오.

**색인 커넥터 정의를 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 머리글 아래에서 설정을 복제할 색인 커넥터 정의 이름을 보려면 **[!UICONTROL Copy]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Copy] 페이지에서 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Copy]**.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 색인 커넥터 정의 이름 바꾸기 {#task_5132118FC21B47D99881E0ED425225D7}

기존 색인 커넥터 정의의 이름을 변경할 수 있습니다.

정의 이름을 바꾼 후 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 선택합니다. 새 정의 이름이 [!DNL URL Entrypoints] 페이지의 드롭다운 목록에 반영되도록 해야 합니다.

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

**색인 커넥터 정의 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 머리글 아래에서 변경할 색인 커넥터 정의 이름의 **[!UICONTROL Rename]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Rename] 페이지의 [!DNL Name] 필드에 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Rename]**.
1. 클릭 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. 이전 색인 커넥터 이름이 목록에 있으면 해당 이름을 제거하고 새로 이름이 변경된 항목을 추가합니다.

   인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오. 1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 색인 커넥터 정의 {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7} 삭제

더 이상 필요하거나 사용하지 않는 기존 색인 커넥터 정의를 삭제할 수 있습니다.

**색인 커넥터 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Definitions] 페이지의 [!DNL Actions] 열 머리글 아래에서 제거할 색인 커넥터 정의 이름의 **[!UICONTROL Delete]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Delete] 페이지에서 **[!UICONTROL Delete]**&#x200B;을 클릭합니다.
