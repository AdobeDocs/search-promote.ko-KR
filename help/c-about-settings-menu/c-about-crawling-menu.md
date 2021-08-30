---
description: 크롤링 메뉴 세트 날짜 및 URL 마스크, 암호, 콘텐츠 유형, 연결, 양식 정의 및 URL 진입점을 사용합니다.
solution: Target
subtopic: Crawling
title: 크롤링 메뉴 정보
topic-legacy: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
exl-id: 22dbbc30-bf1c-4d51-8fb0-708115ba844b
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '11015'
ht-degree: 0%

---

# 크롤링 메뉴 정보{#about-the-crawling-menu}

크롤링 메뉴 세트 날짜 및 URL 마스크, 암호, 콘텐츠 유형, 연결, 양식 정의 및 URL 진입점을 사용합니다.

## URL 시작 지점 정보 {#concept_5D857E3B5C124E85BC0B5AE77A509573}

대부분의 웹 사이트에는 고객이 처음에 방문하는 하나의 기본 시작 지점 또는 홈 페이지가 있습니다. 이 기본 진입점은 검색 로봇이 인덱스 크롤링을 시작하는 URL 주소입니다. 그러나 웹 사이트에 여러 도메인 또는 하위 도메인이 있거나 사이트의 일부가 기본 시작 지점에서 연결되어 있지 않은 경우 URL 시작 지점을 사용하여 시작 지점을 추가할 수 있습니다.

지정된 각 URL 시작 지점 아래의 모든 웹 사이트 페이지는 색인화됩니다. URL 시작 지점을 마스크와 결합하여 색인화할 웹 사이트의 부분을 정확하게 제어할 수 있습니다. 고객이 URL 진입점 설정의 효과를 볼 수 있으려면 먼저 웹 사이트 인덱스를 다시 만들어야 합니다.

기본 시작 지점은 일반적으로 색인화하고 검색할 웹 사이트의 URL입니다. 계정 설정에서 이 기본 진입점을 구성합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

기본 URL 진입점을 지정한 후에는 선택적으로 크롤링할 추가 진입점을 지정할 수 있습니다. 대부분의 경우 기본 시작 지점 아래의 페이지에서 연결되지 않은 웹 페이지에 대해 추가 시작 지점을 지정합니다. 다음 예와 같이 웹 사이트가 둘 이상의 도메인에 걸쳐 있을 때 추가 시작 지점을 지정하십시오.

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

아래 표에서 하나 이상의 공백으로 구분된 키워드로 각 진입점에 자격을 부여할 수 있습니다. 이러한 키워드는 페이지가 색인화되는 방식에 영향을 줍니다.

**중요**: 주어진 키워드를 진입점과 공백으로 구분해야 합니다. 쉼표는 유효한 구분 기호가 아닙니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>인덱스 없음 </p> </td> 
   <td colname="col2"> <p> 시작 지점 페이지에서 텍스트를 색인화하지 않지만 페이지의 링크를 따라가려면 를 추가합니다. 
     진입점 뒤에 <code>
       noindex 
     </code> 있습니다. </p> <p>다음 예제와 같이 키워드를 진입점과 구분하여 공백을 사용하십시오. </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>이 키워드는 
     <code>
       content="noindex" 
     </code>) 사이에 
     <code>
       &lt;head&gt; 
     </code>.. 
     시작 지점 페이지의 <code>
       &lt;/head&gt; 
     </code> 태그. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>팔로우 </p> </td> 
   <td colname="col2"> <p> 시작 지점 페이지에서 텍스트를 색인화하지만 페이지의 링크를 따라가지 않으려면 을 추가합니다. 
     진입점 뒤에 <code>
       nofollow 
     </code> 있습니다. </p> <p>다음 예제와 같이 키워드를 진입점과 구분하여 공백을 사용하십시오. </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>이 키워드는 
     다음 사이 
     <code>
       &lt;head&gt; 
     </code>.. 
     시작 지점 페이지의 <code>
       &lt;/head&gt; 
     </code> 태그입니다.<code>
       content="nofollow" 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>양식 </p> </td> 
   <td colname="col2"> <p> 진입점이 로그인 페이지이면 
     <code>
       form 
     </code> 은 일반적으로 검색 로봇이 웹 사이트를 크롤링하기 전에 로그인 양식을 제출하고 적절한 쿠키를 수신할 수 있도록 사용됩니다. "form" 키워드를 사용할 때 시작 지점 페이지가 인덱싱되지 않고 검색 로봇이 시작 지점 페이지를 크롤링으로 표시하지 않습니다. 사용 
     검색 로봇이 페이지의 링크를 따르지 않도록 하려면 <code>
       nofollow 
     </code> 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

[컨텐츠 유형 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)도 참조하십시오.

[인덱스 커넥터 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)도 참조하십시오.

## 인덱싱할 여러 URL 시작 지점 추가 {#task_2338A47387D74CFDAC4D4EF4A367ED45}

웹 사이트에 여러 도메인 또는 하위 도메인이 있고 크롤링하려는 경우 URL 진입점을 사용하여 URL을 더 추가할 수 있습니다.

웹 사이트의 주 URL 입력 지점을 설정하려면 계정 설정을 사용합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

**인덱싱할 URL 입력 점을 여러 개 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 클릭합니다.
1. [!DNL URL Entrypoints] 페이지의 [!DNL Entrypoints] 필드에 줄당 하나의 URL 주소를 입력합니다.
1. (선택 사항) **[!UICONTROL Add Index Connector Configurations]** 드롭다운 목록에서 색인화를 위한 시작 지점으로 추가할 인덱스 커넥터를 선택합니다.

   드롭다운 목록은 이전에 하나 이상의 색인 커넥터 정의를 추가한 경우에만 사용할 수 있습니다.

   ![](assets/url_entrypoints_index_connector.png)

   [인덱스 커넥터 정의 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## URL 마스크 정보 {#concept_8039DFC53FF3410AA494D602F71BA164}

URL 마스크는 검색 로봇이 색인화하거나 색인화하지 않는 웹 사이트 문서를 결정하는 패턴입니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

다음은 사용할 수 있는 두 가지 종류의 URL 마스크입니다.

* URL 마스크 포함
* URL 마스크 제외

URL 포함 마스크는 검색 로봇에 마스크 패턴과 일치하는 문서를 색인화하도록 지시합니다.

제외 URL 마스크는 검색 로봇에 일치하는 문서를 색인화하도록 지시합니다.

검색 로봇이 링크에서 웹 사이트를 통해 이동할 때 URL이 나타나고 해당 URL과 일치하는 마스크를 찾습니다. 첫 번째 일치에서는 색인에서 해당 URL을 포함할지 또는 제외할지를 결정합니다. 발견된 URL과 일치하는 마스크가 없으면 해당 URL이 인덱스에서 무시됩니다.

포함 - 시작 지점 URL에 대한 URL 마스크가 자동으로 생성됩니다. 이 동작을 사용하면 웹 사이트에서 발생한 모든 문서가 색인화됩니다. 또한 웹 사이트를 &quot;나가기&quot;하는 링크가 있으면 편리하게 해당 링크가 사라집니다. 예를 들어, 인덱싱된 페이지가 https://www.yahoo.com으로 링크되는 경우 검색 로봇은 해당 URL이 진입점 URL에 의해 자동으로 생성된 포함 마스크와 일치하지 않으므로 해당 URL을 색인화하지 않습니다.

지정하는 각 URL 마스크는 별도의 줄에 있어야 합니다.

마스크는 다음 중 하나를 지정할 수 있습니다.

* `https://www.mydomain.com/products.html`의 전체 경로입니다.
* `https://www.mydomain.com/products`의 부분 경로입니다.
* `https://www.mydomain.com/*.html`에 있는 대로 와일드카드를 사용하는 URL입니다.
* 정규 표현식(고급 사용자).

   마스크를 정규식으로 만들려면 마스크 유형( `exclude` 또는 `include`)과 URL 마스크 사이에 `regexp` 키워드를 삽입합니다.

다음은 간단한 제외 URL 마스크 예입니다.

```
exclude https://www.mydomain.com/photos
```

이 예제는 제외 URL 마스크이므로 패턴과 일치하는 문서는 색인화되지 않습니다. 패턴은 파일과 폴더 모두 일치하는 항목을 발견하므로 제외 URL과 일치하는 `https://www.mydomain.com/photos.html` 및 `https://www.mydomain.com/photos/index.html`이 인덱싱되지 않습니다. `/photos/` 폴더의 파일만 일치시키려면 다음 예제와 같이 URL 마스크에 후행 슬래시가 포함되어야 합니다.

```
exclude https://www.mydomain.com/photos/
```

다음 제외 마스크 예제에서는 와일드카드 를 사용합니다. 검색 로봇에 &quot;.pdf&quot; 확장자가 있는 파일을 간과하도록 알려줍니다. 검색 로봇은 이러한 파일을 인덱스에 추가하지 않습니다.

```
exclude *.pdf
```

간단한 포함 URL 마스크는 다음과 같습니다.

```
include https://www.mydomain.com/news/
```

URL 진입점의 일련의 링크 또는 URL 진입점으로 사용되는 문서만 인덱싱됩니다. 포함 URL 마스크로 문서의 URL을 단독으로 나열하는 것은 연결되지 않은 문서를 색인화하지 않습니다. 인덱스에 연결되지 않은 문서를 추가하려면 URL 시작 지점 기능을 사용할 수 있습니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

마스크 포함 및 제외 마스크가 함께 작동할 수 있습니다. 제외 URL 마스크를 만들고 포함 URL 마스크가 있는 제외된 페이지를 하나 이상 포함하여 웹 사이트의 많은 부분을 색인화에서 제외할 수 있습니다. 예를 들어, 시작 지점 URL이 다음과 같다고 가정합니다.

```
https://www.mydomain.com/photos/
```

검색 로봇은 `/photos/summer/`, `/photos/spring/` 및 `/photos/fall/` 아래의 모든 페이지를 크롤링하고 인덱싱합니다(`photos` 폴더의 각 디렉터리에 있는 하나 이상의 페이지에 대한 링크가 있다고 가정). 이 동작은 링크 경로를 사용하여 검색 로봇이 `/summer/`, `/spring/` 및 `/fall/`에서 문서를 찾을 수 있게 하고, 폴더 및 폴더 URL은 시작 지점 URL에서 자동으로 생성된 포함 마스크와 일치하기 때문에 발생합니다.

다음 예와 같이 제외 URL 마스크가 있는 `/fall/` 폴더의 모든 페이지를 제외하도록 선택할 수 있습니다.

```
exclude https://www.mydomain.com/photos/fall/
```

또는 다음 URL 마스크가 있는 인덱스의 일부로 `/photos/fall/redleaves4.html`만 선택적으로 포함할 수 있습니다.

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

위의 두 마스크 예가 의도한 대로 작동하려면 다음과 같이 포함 마스크가 먼저 나열됩니다.

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

검색 로봇이 나열된 순서로 방향을 따르기 때문에 검색 로봇은 먼저 `/photos/fall/redleaves4.html`을 포함시킨 다음 `/fall` 폴더에 있는 나머지 파일을 제외합니다.

지침을 다음과 같이 반대로 지정한 경우:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

그러면 마스크에 `/photos/fall/redleaves4.html`이 포함된다고 지정되더라도 포함되지 않습니다.

맨 먼저 나타나는 URL 마스크가 마스크 설정에서 나중에 나타나는 URL 마스크보다 항상 우선합니다. 또한 검색 로봇이 포함 URL 마스크와 제외 URL 마스크와 일치하는 페이지를 발견하는 경우 먼저 나열된 마스크가 우선합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

## URL 마스크에서 키워드 사용 정보 {#section_7609A7A6D79B482ABCA8900886541AAB}

일치하는 페이지가 색인화되는 방식에 영향을 주는 하나 이상의 공백으로 구분된 키워드로 각 포함 마스크에 자격을 부여할 수 있습니다.

마스크와 키워드 사이의 구분자로 쉼표를 사용할 수 없습니다. 공백만 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>인덱스 없음 </p> </td> 
   <td colname="col2"> <p> URL 마스크와 일치하는 페이지의 텍스트를 색인화하지 않고 일치하는 페이지 링크를 따르려면 를 추가합니다. 
     포함 URL 마스크 뒤에 <code>
       noindex 
     </code> 있습니다. 다음 예제와 같이 키워드를 마스크와 공백으로 구분해야 합니다. </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>위의 예에서는 검색 로봇이 
     <code>
       .swf 
     </code> 확장명을 사용하지만 해당 파일에 포함된 모든 텍스트의 색인화를 사용하지 않습니다. </p> <p>다음 
     <code>
       noindex 
     </code> 키워드는 
     다음 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그.<code>
       content="noindex" 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>팔로우 </p> </td> 
   <td colname="col2"> <p> URL 마스크와 일치하는 페이지의 텍스트를 색인화하지만 일치하는 페이지의 링크를 따르지 않으려면 를 추가합니다. 
     포함 URL 마스크 뒤에 <code>
       nofollow 
     </code> 있습니다. 다음 예제와 같이 키워드를 마스크와 공백으로 구분해야 합니다. </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>다음 
     <code>
       nofollow 
     </code> 키워드는 
     다음 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그.<code>
       content="nofollow" 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>포함 및 제외 마스크에 모두 사용됩니다. </p> <p>앞에 URL 마스크가 있으면 
     <code>
       regexp 
     </code>은 정규 표현식으로 처리됩니다. 검색 로봇이 제외 정규 표현식 URL 마스크와 일치하는 문서를 발견하면 해당 문서가 인덱싱되지 않습니다. 검색 로봇이 포함 정규 표현식 URL 마스크와 일치하는 문서를 발견하면 해당 문서가 인덱스화됩니다. 예를 들어 다음 URL 마스크가 있다고 가정해 보겠습니다. </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>검색 로봇은 다음과 같은 일치하는 파일을 제외합니다 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>다음의 정규 표현식 URL 마스크를 제외하는 경우: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>검색 로봇은 다음과 같은 CGI 매개 변수가 포함된 URL을 포함하지 않습니다 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code> </p> <p>정규 표현식 URL 마스크가 포함된 경우: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>검색 로봇은 ".swf" 확장자가 있는 파일의 모든 링크를 따릅니다. 다음 
     <code>
       noindex 
     </code> 키워드도 일치하는 파일의 텍스트가 색인화되지 않도록 지정합니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 웹 사이트의 일부를 색인화하거나 색인화하지 않도록 URL 마스크 추가 {#task_E1AFC17C746048B8843013D979E082C1}

[!DNL URL Masks] 을 사용하여 크롤링과 인덱싱할 웹 사이트의 일부를 정의할 수 있습니다.

[테스트 URL 마스크] 필드를 사용하여 색인화한 후 문서가 포함되었는지 여부를 테스트합니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**웹 사이트의 일부를 색인화하거나 색인화하지 않도록 URL 마스크를 추가합니다**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL URL Masks] 페이지의 **[!UICONTROL Test URL Masks]** 필드에서 웹 사이트의 테스트 URL 마스크를 입력한 다음 **[!UICONTROL Test]** 를 클릭합니다.
1. [!DNL URL Masks] 필드에 `include`(크롤링과 인덱싱할 웹 사이트를 추가하려면)를 입력하거나, `exclude`(웹 사이트가 크롤링과 인덱싱되지 않도록 차단하려면)를 입력한 다음 URL 마스크 주소를 입력합니다.

   줄당 하나의 URL 마스크 주소를 입력합니다. 예:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 날짜 마스크 정보 {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

날짜 마스크를 사용하여 파일의 나이에 따라 검색 결과에서 파일을 포함하거나 제외할 수 있습니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

사용할 수 있는 날짜 마스크는 다음과 같이 두 가지입니다.

* 날짜 마스크 포함(&quot;include-days&quot; 및 &quot;include-date&quot;)

   날짜 마스크 인덱스 파일을 지정한 날짜 또는 그 이전 날짜로 포함합니다.
* 날짜 마스크 제외(&quot;exclude-days&quot; 및 &quot;exclude-date&quot;)

   제외 날짜 마스크 인덱스 파일은 지정된 날짜 또는 이전 날짜입니다.

기본적으로 파일 날짜는 메타 태그 정보로 결정됩니다. 메타 태그를 찾을 수 없으면 검색 로봇이 파일을 다운로드할 때 서버에서 수신한 HTTP 헤더에서 파일 날짜가 결정됩니다.

지정하는 각 날짜 마스크는 별도의 줄에 있어야 합니다.

마스크는 다음 중 하나를 지정할 수 있습니다.

* `https://www.mydomain.com/products.html`에 있는 전체 경로
* `https://www.mydomain.com/products`에 있는 부분 경로
* 와일드카드 `https://www.mydomain.com/*.html`를 사용하는 URL
* 정규 표현식입니다. 마스크를 정규식으로 만들려면 URL 앞에 키워드 `regexp`을 삽입합니다.

날짜 마스크 포함 및 제외 모두 다음 두 방법 중 하나로 날짜를 지정할 수 있습니다. 마스크는 일치하는 파일이 지정된 날짜 또는 그 이전에 만들어진 경우에만 적용됩니다.

1. 일 수. 예를 들어 날짜 마스크가 다음과 같다고 가정합니다.

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   지정된 일 수가 다시 계산됩니다. 파일이 도착 날짜 또는 그 이전에 날짜인 경우 마스크가 적용됩니다.

1. YYYY-MM-DD 형식을 사용하는 실제 날짜입니다. 예를 들어 날짜 마스크가 다음과 같다고 가정합니다.

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   일치하는 문서가 지정된 날짜 또는 그 이전 날짜인 경우 날짜 마스크가 적용됩니다.

다음은 간단한 제외 날짜 마스크 예입니다.

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

이 마스크는 제외 날짜 마스크이므로 패턴과 일치하는 파일은 색인화되지 않고 90일 이상 오래됩니다. 문서를 제외하면 텍스트가 색인화되지 않고 해당 파일의 링크가 표시되지 않습니다. 이 파일은 사실상 무시됩니다. 이 예에서는 파일과 폴더가 모두 지정된 URL 패턴과 일치할 수 있습니다. `https://www.mydomain.com/docs/archive.html` 및 `https://www.mydomain.com/docs/archive/index.html` 모두 패턴과 일치하며 90일 이상 경과한 경우에는 색인화되지 않습니다. `/docs/archive/` 폴더의 파일만 일치시키려면 날짜 마스크에 다음과 같이 후행 슬래시가 포함되어야 합니다.

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

날짜 마스크는 와일드카드와 함께 사용할 수도 있습니다. 다음 제외 마스크는 검색 로봇에 날짜 또는 2011-02-15 이전에 업데이트된 &quot;.pdf&quot; 확장자가 있는 파일을 간과하도록 알려줍니다. 검색 로봇이 인덱스에 일치하는 파일을 추가하지 않습니다.

```
exclude-date 2011-02-15 *.pdf
```

날짜 마스크 포함 모습은 유사하며 일치하는 파일만 색인에 추가됩니다. 다음 포함 날짜 마스크 예는 검색 로봇에 웹 사이트의 `/docs/archive/manual/` 영역에 있는 0일 또는 그 이전의 모든 파일에서 텍스트를 색인화하도록 지시합니다.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

마스크 포함 및 제외 마스크가 함께 작동할 수 있습니다. 예를 들어 제외 날짜 마스크를 만들고 포함 URL 마스크가 있는 제외된 페이지를 하나 이상 포함하여 웹 사이트의 많은 부분을 색인화에서 제외할 수 있습니다. 시작 지점 URL이 다음과 같은 경우

```
https://www.mydomain.com/archive/
```

검색 로봇은 `/archive/summer/`, `/archive/spring/` 및 `/archive/fall/` 아래의 모든 페이지를 크롤링하고 인덱싱합니다(`archive` 폴더의 각 폴더에 있는 하나 이상의 페이지에 대한 링크가 있다고 가정). 이 동작은 링크 경로를 사용하여 검색 로봇이 `/summer/`, `/spring/` 및 `/fall/` 폴더의 파일을 &quot;찾기&quot;할 수 있고 폴더 URL이 시작 지점 URL에서 자동으로 생성된 포함 마스크와 일치하기 때문에 발생합니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

다음과 같이 제외 날짜 마스크가 있는 `/fall/` 폴더에서 90일이 넘는 모든 페이지를 제외하도록 선택할 수 있습니다.

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

다음 날짜 마스크가 있는 인덱스의 일부로 `/archive/fall/index.html`(파일이 얼마나 오래되었는지 여부에 관계없이, 0일 또는 그 이전 파일이 일치하는지)만 선택적으로 포함할 수 있습니다.

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

위의 두 개의 마스크 예가 의도한 대로 작동하려면 다음과 같이 포함 마스크를 먼저 나열해야 합니다.

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

검색 로봇은 지정된 순서대로 방향을 따르므로 검색 로봇은 먼저 `/archive/fall/index.html`을 포함하고 `/fall` 폴더의 나머지 파일들은 제외합니다.

지침을 다음과 같이 반대로 지정한 경우:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

그러면 마스크에 `/archive/fall/index.html`이(가) 포함되도록 지정되더라도 포함되지 않습니다. 맨 먼저 나타나는 날짜 마스크가 마스크 설정에서 나중에 나타날 수 있는 날짜 마스크보다 항상 우선합니다. 또한 검색 로봇이 포함 날짜 마스크와 제외 날짜 마스크와 일치하는 페이지를 발견하는 경우 먼저 나열된 마스크가 우선합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

## 날짜 마스크에서 키워드 사용 정보 {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

일치하는 페이지가 색인화되는 방식에 영향을 주는 하나 이상의 공백으로 구분된 키워드로 각 포함 마스크에 자격을 부여할 수 있습니다.

마스크와 키워드 사이의 구분자로 쉼표를 사용할 수 없습니다. 공백만 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키워드 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>인덱스 없음 </p> </td> 
   <td colname="col2"> <p> 포함 마스크로 지정한 날짜 이전 또는 날짜가 있는 페이지에서 텍스트를 색인화하지 않으려면 을 추가합니다. 
     다음과 같이 포함 날짜 마스크 후 <code>
       noindex 
     </code>: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>마스크에서 키워드를 공백으로 구분해야 합니다. </p> <p>위의 예에서는 검색 로봇이 10일 이상 버전의 ".swf" 확장자를 사용하는 파일의 모든 링크를 따르도록 지정합니다. 그러나 해당 파일에 포함된 모든 텍스트의 색인화를 비활성화합니다. </p> <p>이전 파일의 텍스트가 색인화되지 않았지만 해당 파일의 모든 링크를 따르도록 할 수 있습니다. 이 경우 제외 날짜 마스크를 사용하는 대신 "noindex" 키워드와 함께 포함 날짜 마스크를 사용하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>팔로우 </p> </td> 
   <td colname="col2"> <p> 포함 마스크에 의해 지정된 날짜 이전 또는 날짜에 날짜가 지정된 페이지의 텍스트를 색인화하려면 일치하는 페이지의 링크를 따라가지 않으려면 을 추가합니다. 
     다음과 같이 포함 날짜 마스크 후 <code>
       nofollow 
     </code>: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>마스크에서 키워드를 공백으로 구분해야 합니다. </p> <p>다음 
     <code>
       nofollow 
     </code> 키워드는 
     다음 사이 
     일치하는 페이지의 <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> 태그입니다.<code>
       content="nofollow" 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>포함 및 제외 마스크에 모두 사용됩니다. </p> <p>일반적으로 검색 로봇은 날짜 마스크를 확인하기 전에 모든 파일을 다운로드하여 구문 분석합니다. 이 동작은 일부 파일 유형이 파일 자체 내에 날짜를 지정할 수 있기 때문에 발생합니다. 예를 들어 HTML 문서에는 파일의 날짜를 설정하는 메타 태그가 포함될 수 있습니다. </p> <p>날짜를 기준으로 많은 파일을 제외하려고 하며 서버에 불필요한 로드를 추가하지 않으려면 
     날짜 마스크의 URL 뒤에 <code>
       server-date 
     </code> 있습니다. </p> <p>이 키워드는 검색 로봇이 각 파일을 구문 분석하는 대신 서버에서 반환되는 파일의 날짜를 신뢰하도록 지시합니다. 예를 들어, 다음 제외 날짜 마스크는 HTTP 헤더에서 서버가 반환한 날짜에 따라 문서가 90일 이상인 경우 URL과 일치하는 페이지를 무시합니다. </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> 서버에서 반환한 날짜가 90일 이상인 경우 
     <code>
       server-date 
     </code> 에서는 제외된 문서를 서버에서 다운로드하지 않도록 지정합니다. 따라서 문서에 대한 인덱싱 시간이 빨라지고 서버에 부하가 줄어듭니다. If 
     <code>
       server-date 
     </code>이 지정되지 않은 경우 검색 로봇은 HTTP 헤더에서 서버에서 반환한 날짜를 무시합니다. 대신 각 파일을 다운로드하여 날짜가 지정되었는지 확인합니다. 파일에 날짜가 지정되지 않은 경우 검색 로봇은 서버에서 반환한 날짜를 사용합니다. </p> <p>를 사용하지 마십시오 
     파일에 서버 날짜를 재정의하는 명령이 포함된 경우 <code>
       server-date 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> 포함 및 제외 마스크에 모두 를 사용합니다. </p> <p>앞에 오는 모든 날짜 마스크 
     <code>
       regexp 
     </code>은 정규 표현식으로 처리됩니다. </p> <p>검색 로봇이 제외 정규 표현식 날짜 마스크와 일치하는 파일을 발견하면 해당 파일을 색인화하지 않습니다. </p> <p>검색 로봇이 포함 정규 표현식 날짜 마스크와 일치하는 파일을 발견하면 해당 문서를 인덱싱합니다. </p> <p>예를 들어 다음과 같은 날짜 마스크가 있다고 가정합니다. </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>마스크는 검색 로봇에 180일 이상의 일치하는 파일을 제외하도록 지시합니다. 즉, URL에 "archive"라는 단어가 포함된 파일입니다. </p> <p><a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> 정규 표현식 </a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 웹 사이트의 일부 색인에 날짜 마스크 추가 {#task_0010543C55F648D2B5DEFEFAD60FAF04}

날짜 마스크를 사용하여 파일의 나이에 따라 고객 검색 결과에서 파일을 포함하거나 제외할 수 있습니다.

**[!UICONTROL Test Date]** 및 **[!UICONTROL Test URL]** 필드를 사용하여 색인화 후 파일이 포함되어 있는지 여부를 테스트합니다.

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**웹 사이트의 일부를 색인화하거나 색인화하지 않도록 날짜 마스크를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Date Masks] 페이지의 **[!UICONTROL Test Date]** 필드에 YYYY-MM-DD(예: `2011-07-25`) 형식의 날짜를 입력합니다. **[!UICONTROL Test URL]** 필드에서 웹 사이트의 URL 마스크를 입력한 다음 **[!UICONTROL Test]** 를 클릭합니다.
1. [!DNL Date Masks] 필드에 줄당 하나의 날짜 마스크 주소를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 암호 정보 {#concept_3EDBD731725D46B891F834D4472774DC}

HTTP 기본 인증을 통해 보호되는 웹 사이트의 부분에 액세스하려면 하나 이상의 암호를 추가할 수 있습니다.

고객이 암호 설정의 효과를 보려면 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

[!DNL Passwords] 페이지에서 각 암호를 한 줄에 입력합니다. 다음 예와 같이 암호는 URL 또는 영역, 사용자 이름 및 암호로 구성됩니다.

```
https://www.mydomain.com/ myname mypassword
```

위와 같이 URL 경로를 사용하는 대신 영역을 지정할 수도 있습니다.

사용할 올바른 영역을 결정하려면 브라우저로 암호로 보호된 웹 페이지를 열고 &quot;네트워크 암호 입력&quot; 대화 상자를 봅니다.

![](assets/realms.gif)

이 경우 영역 이름은 &quot;내 사이트 영역&quot;입니다.

위의 영역 이름을 사용하면 암호는 다음과 같을 수 있습니다.

```
My Site Realm myusername mypassword
```

웹 사이트에 여러 영역이 있는 경우 다음 예와 같이 개별 라인에 각 영역에 대한 사용자 이름과 암호를 입력하여 여러 암호를 생성할 수 있습니다.

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

암호 목록이 다음과 유사하도록 URL 또는 영역을 포함하는 암호를 혼합할 수 있습니다.

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

위의 목록에서 서버의 인증 요청과 일치하는 영역 또는 URL을 포함하는 첫 번째 암호가 사용됩니다. `https://www.mysite.com/path1/path2/index.html`의 파일이 `Realm3`에 있더라도, 예를 들어, `name2` 및 `password2`는 URL로 정의된 암호가 영역에 정의된 암호 위에 나열되므로 사용됩니다.

## 인증이 필요한 웹 사이트 영역에 액세스하기 위한 암호 추가 {#task_DED19D476FF04B48BB6456D5ECB8628A}

암호를 사용하여 크롤링 및 인덱싱 목적으로 웹 사이트의 암호로 보호된 영역에 액세스할 수 있습니다.

암호가 추가되어 고객에게 표시되기 전에 사이트 인덱스를 다시 만들어야 합니다

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**인증이 필요한 웹 사이트 영역에 액세스하기 위한 암호를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**&#x200B;를 클릭합니다.
1. [!DNL Passwords] 페이지의 **[!UICONTROL Passwords]** 필드에 영역 또는 URL, 연관된 사용자 이름 및 암호를 공백으로 구분하여 입력합니다.

   영역 비밀번호 및 개별 줄에 있는 URL 비밀번호의 예:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   행당 하나의 암호만 추가합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 컨텐츠 유형 정보 {#concept_6FEA1355C0374500B4C53090C34A8A07}

[!DNL Content Types] 을 사용하여 이 계정에 대해 크롤링하고 인덱싱할 파일 유형을 선택할 수 있습니다.

크롤링 및 색인화하도록 선택할 수 있는 콘텐츠 형식에는 PDF 문서, 텍스트 문서, Adobe Flash 동영상, Word, Excel, Powerpoint 등의 Microsoft Office 응용 프로그램의 파일, MP3 파일의 텍스트가 포함됩니다. 선택한 콘텐츠 유형 내에 있는 텍스트는 웹 사이트의 다른 모든 텍스트와 함께 검색됩니다.

고객에게 콘텐츠 유형 설정의 효과를 표시하려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

## MP3 음악 파일 인덱싱 정보 {#section_AD2E28BEEE3E46629E2B05C34A963673}

[!DNL Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]** 옵션을 선택하면 MP3 파일이 두 가지 방법 중 하나로 크롤링되고 인덱싱됩니다. 가장 일반적인 방법은 다음과 같이 HTML 파일의 앵커 href 태그에서 가져온 것입니다.

```
<a href="MP3-file-URL"></a>
```

두 번째 방법은 MP3 파일의 URL을 URL 진입점으로 입력하는 것입니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

MP3 파일은 해당 MIME 유형 &quot;audio/mpeg&quot;로 인식됩니다.

MP3 음악 파일 크기는 보통 적은 양의 텍스트만 포함되지만 매우 클 수 있습니다. 예를 들어 MP3 파일은 필요에 따라 앨범 이름, 아티스트 이름, 노래 제목, 노래 장르, 릴리스 연도 및 댓글과 같은 항목을 저장할 수 있습니다. 이 정보는 파일의 맨 끝에 TAG라고 하는 위치에 저장됩니다. TAG 정보가 포함된 MP3 파일은 다음과 같은 방법으로 인덱싱됩니다.

* 노래 제목은 HTML 페이지의 제목과 같습니다.
* 주석은 HTML 페이지에 대해 정의된 설명처럼 처리됩니다.
* 이 장르는 HTML 페이지에 대해 정의된 키워드로 처리됩니다.
* 아티스트 이름, 앨범 이름 및 릴리스 연도는 HTML 페이지의 본문처럼 처리됩니다.

웹 사이트에서 크롤링되고 인덱싱된 각 MP3 파일은 한 페이지로 계산됩니다.

웹 사이트에 많은 대용량 MP3 파일이 포함되어 있는 경우 계정의 인덱싱 바이트 제한을 초과할 수 있습니다. 이런 경우 [!DNL Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]** 을 선택 해제하여 웹 사이트에서 모든 MP3 파일이 색인화되는 것을 방지할 수 있습니다.

웹 사이트에서 특정 MP3 파일의 색인화를 방지하려면 다음 중 하나를 수행할 수 있습니다.

* MP3 파일에 연결된 앵커 태그를 `<nofollow>` 및 `</nofollow>` 태그로 묶습니다. 검색 로봇은 이러한 태그 사이의 링크를 따르지 않습니다.

* MP3 파일의 URL을 제외 마스크로 추가합니다.

   [URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

## 크롤링 및 색인화할 컨텐츠 유형 선택 {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

[!DNL Content Types] 을 사용하여 이 계정에 대해 크롤링하고 인덱싱할 파일 유형을 선택할 수 있습니다.

크롤링 및 색인화하도록 선택할 수 있는 콘텐츠 형식에는 PDF 문서, 텍스트 문서, Adobe Flash 동영상, Word, Excel, Powerpoint 등의 Microsoft Office 응용 프로그램의 파일, MP3 파일의 텍스트가 포함됩니다. 선택한 콘텐츠 유형 내에 있는 텍스트는 웹 사이트의 다른 모든 텍스트와 함께 검색됩니다.

고객에게 콘텐츠 유형 설정의 효과를 표시하려면 먼저 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

중국어, 일본어 또는 한국어 MP3 파일을 크롤링하고 색인화하려면 아래 단계를 완료하십시오. 그런 다음 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;에서 MP3 파일을 인코딩하는 데 사용할 문자 세트를 지정합니다.

[주입 정보](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)를 참조하십시오.

**크롤링 및 색인화할 컨텐츠 유형을 선택하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;를 클릭합니다.
1. [!DNL Content Types] 페이지에서 웹 사이트에서 크롤링하고 인덱싱할 파일 유형을 확인합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 연결 정보 {#concept_E2F3B7E7521147479E5948A94BB3A40B}

연결 을 사용하여 검색 로봇이 웹 사이트를 색인화하는 데 사용하는 최대 10개의 HTTP 연결을 추가할 수 있습니다.

연결 수를 늘리면 크롤링과 색인을 완료하는 데 걸리는 시간이 크게 줄어들 수 있습니다. 그러나 각 추가 연결은 서버의 로드를 증가시킵니다.

## 색인 속도를 높이기 위해 연결 추가 {#task_3E9B83E43C1842A19066355A15C4A6FB}

Connections를 사용하여 Crawler가 사용하는 동시 HTTP 연결 수를 증가시켜 웹 사이트를 색인화하는 데 걸리는 시간을 줄일 수 있습니다. 최대 10개의 연결을 추가할 수 있습니다.

각 추가 연결은 서버에 배치된 로드를 증가시킵니다.

**연결을 추가하여 인덱싱 속도를 높이려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**&#x200B;를 클릭합니다.
1. [!DNL Parallel Indexing Connections] 페이지의 **[!UICONTROL Number of Connections]** 필드에 추가할 연결 수(1-10)를 입력합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 양식 제출 정보 {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

양식 제출 을 사용하여 웹 사이트에서 양식을 인식하고 처리할 수 있습니다.

웹 사이트의 크롤링 및 색인 지정 중에 발생한 각 양식은 추가한 양식 정의와 비교됩니다. 양식이 양식 정의와 일치하는 경우 양식을 색인 지정 용도로 제출합니다. 양식이 두 개 이상의 정의와 일치하는 경우, 일치하는 각 정의에 대해 양식이 한 번 제출됩니다.

## 웹 사이트에서 양식을 인덱싱하기 위한 양식 정의 추가 {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

[!DNL Form Submission] 을 사용하여 색인화를 위해 웹 사이트에서 인식되는 양식을 처리할 수 있습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**웹 사이트에서 양식을 인덱싱하기 위한 양식 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 **[!UICONTROL Add New Form]** 을 클릭합니다.
1. [!DNL Add Form Definition] 페이지에서 [!DNL Form Recognition] 및 [!DNL Form Submission] 옵션을 설정합니다.

   [!DNL Form Definition] 페이지의 [!DNL Form Recognition] 섹션에 있는 다섯 가지 옵션은 처리할 수 있는 웹 페이지에서 양식을 식별하는 데 사용됩니다.

   [!DNL Form Submission] 섹션의 세 가지 옵션은 웹 서버에 양식과 함께 제출되는 매개 변수와 값을 지정하는 데 사용됩니다.

   라인당 한 개의 인식 또는 제출 매개변수를 입력합니다. 각 매개 변수에는 이름과 값이 포함되어야 합니다.

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
      <td colname="col2"> <p>양식이 포함된 웹 페이지 또는 페이지를 식별합니다. 단일 페이지에 나타나는 양식을 식별하려면 다음 예와 같이 해당 페이지의 URL을 입력합니다. </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>여러 페이지에 나타나는 양식을 식별하려면 와일드카드를 사용하여 페이지를 설명하는 URL 마스크를 지정합니다. 예를 들어 <code> https://www.mydomain.com/register/ </code> 아래의 ASP 페이지에서 발생하는 양식을 식별하려면 다음을 지정합니다. </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>정규 표현식을 사용하여 여러 페이지를 식별할 수도 있습니다. 을(를) 지정하기만 하면 됩니다 
      다음 예제와 같이 URL 마스크 앞에 <code>
        regexp 
      </code> 키워드를 추가합니다. </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 URL 마스크 </p> </td> 
      <td colname="col2"> <p>의 작업 속성을 식별합니다 
      <code>
        &lt;form&gt; 
      </code> 태그. </p> <p>페이지 URL 마스크와 마찬가지로 작업 URL 마스크는 단일 URL, 와일드카드가 있는 URL 또는 정규 표현식의 형태를 취할 수 있습니다. </p> <p>URL 마스크는 다음 중 하나일 수 있습니다. 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> 다음과 같은 전체 경로: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> 다음과 같은 부분 경로: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> 다음과 같이 와일드카드 를 사용하는 URL입니다. <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> 다음과 같은 정규 표현식입니다. <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>URL 마스크나 작업 URL 마스크로 식별되는 페이지의 텍스트를 색인화하지 않으려는 경우, 또는 해당 페이지에서 링크가 따르지 않게 하려면 
      <code>
        noindex 
      </code> 및 
      <code>
        nofollow 
      </code> 키워드. URL 마스크 또는 진입점을 사용하여 마스크에 이러한 키워드를 추가할 수 있습니다. </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> URL 진입점 정보 </a>를 참조하십시오. </p> <p><a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> URL 마스크 정보 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>양식 이름 마스크 </p> </td> 
      <td colname="col2"> <p>다음 경우에 양식 식별 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그에 이름 특성이 있습니다. </p> <p>단순 이름( 
      <code>
        login_form 
      </code>), 와일드카드( 
      <code>
        form* 
      </code>) 또는 정규 표현식( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>일반적으로 양식에는 이름 속성이 없으므로 이 필드를 비워 둘 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>양식 ID 마스크 </p> </td> 
      <td colname="col2"> <p>다음 경우에 양식 식별 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그에 id 속성이 포함되어 있습니다. </p> <p>단순 이름( 
      <code>
        login_form 
      </code>), 와일드카드( 
      <code>
        form* 
      </code>) 또는 정규 표현식( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>일반적으로 양식에는 이름 속성이 없으므로 이 필드를 비워 둘 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>명명된 매개 변수 또는 특정 값이 있는 명명된 매개 변수를 포함하거나 포함하지 않는 양식을 식별합니다. </p> <p>예를 들어, rick_brough@mydomain.com으로 사전에 설정된 전자 메일 매개 변수인 password 매개 변수가 포함된 양식을 식별하려면 다음 매개 변수 설정을 한 줄에 하나씩 지정합니다. </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>양식 제출</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>작업 URL 무시 </p> </td> 
      <td colname="col2"> <p>양식 제출의 대상이 양식의 작업 특성에 지정된 내용과 다른 시기를 지정합니다. </p> <p>예를 들어 양식에 있는 값과 다른 URL 값을 구성하는 JavaScript 함수를 통해 양식을 제출할 때 이 옵션을 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>무시 메서드 </p> </td> 
      <td colname="col2"> <p>양식 제출의 대상이 양식의 작업 속성에 사용되는 내용과 다를 때와 JavaScript 제출 시 메서드가 변경된 시점을 지정합니다. </p> <p>모든 양식 매개 변수의 기본값( 
      <code>
        &lt;input&gt; 
      </code> 태그(숨김 필드 포함), 
      <code>
        &lt;option&gt; 
      </code> 
      <code>
        &lt;select&gt; 
      </code> 태그와 사이에 있는 기본 텍스트 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> 태그)를 웹 페이지에서 읽을 수 있습니다. 그러나 <span class="uicontrol"> 매개 변수 </span> 필드의 <span class="wintitle"> 양식 제출 </span> 섹션에 나열된 모든 매개 변수는 양식 기본값으로 대체됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>양식 제출 매개 변수에 접두사를 추가할 수 있습니다 
      <code>
        not 
      </code> 키워드. </p> <p>매개 변수에 접두사를 추가할 때 
      <code>
        not 
      </code> 양식 제출의 일부로 제출되지 않습니다. 이 동작은 선택을 해제해야 하는 확인란을 선택하는 데 유용합니다. </p> <p>예를 들어 다음 매개 변수를 제출한다고 가정합니다. </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> 값이 있는 이메일 매개 변수 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> 값이 있는 암호 매개 변수 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> mycheckbox 매개 변수는 선택 취소됨으로 표시됩니다. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>기타 모두 
      <code>
        &lt;form&gt; 
      </code> 매개 변수를 기본값으로 </p> </li> 
      </ul> </p> <p>양식 제출 매개 변수는 다음과 같습니다. </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>의 메서드 속성입니다. 
      웹 페이지의 <code>
        &lt;form&gt; 
      </code> 태그는 GET 메서드 또는 POST 방법을 사용하여 데이터가 서버에 전송되는지 결정하는 데 사용됩니다. </p> <p>만약 
      <code>
        &lt;form&gt; 
      </code> 태그에 메서드 속성이 포함되어 있지 않고 GET 메서드를 사용하여 양식이 제출됩니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 양식 정의 편집 {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

웹 사이트의 양식이 변경되었거나 정의를 변경해야 하는 경우 기존 양식 정의를 편집할 수 있습니다.

[!DNL Form Submission] 페이지에는 양식 정의에 변경한 내용을 되돌리는 [!DNL History] 기능이 없습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**양식 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 업데이트할 양식 정의 오른쪽에 있는 **[!UICONTROL Edit]** 를 클릭합니다.
1. [!DNL Edit Form Definition] 페이지에서 [!DNL Form Recognition] 및 [!DNL Form Submission] 옵션을 설정합니다.

   웹 사이트에서 양식을 색인화하려면 [양식 정의 추가 아래의 옵션 표를 참조하십시오](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 양식 정의 삭제 {#task_C350FC0CDE344F2786215D544C048B5E}

웹 사이트에 양식이 더 이상 존재하지 않거나 특정 양식을 더 이상 처리하고 색인화하지 않으려는 경우 기존 양식 정의를 삭제할 수 있습니다.

[!DNL Form Submission] 페이지에는 양식 정의에 변경한 내용을 되돌리는 [!DNL History] 기능이 없습니다.

변경 내용이 고객에게 표시되도록 사이트 인덱스를 다시 만들어야 합니다.

[준비된 웹 사이트의 증분 색인 구성](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)을 참조하십시오.

**양식 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**&#x200B;를 클릭합니다.
1. [!DNL Form Submission] 페이지에서 제거할 양식 정의 오른쪽에 있는 **[!UICONTROL Delete]** 를 클릭합니다.

   삭제할 올바른 양식 정의를 선택해야 합니다. 다음 단계에서 **[!UICONTROL Delete]** 을 클릭해도 삭제 확인 대화 상자가 없습니다.
1. [!DNL Delete Form Definition] 페이지에서 **[!UICONTROL Delete]** 을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 색인 커넥터 정보 {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

XML 페이지 또는 모든 종류의 피드를 인덱싱하기 위해 추가 입력 소스를 정의하려면 [!DNL Index Connector] 을 사용합니다.

데이터 피드 입력 소스를 사용하여 웹 사이트에서 일반적으로 검색되는 것과 다른 양식에 저장된 컨텐츠에 액세스할 수 있는 크롤링 방법 중 하나를 사용합니다. 크롤링되고 직접 인덱싱된 각 문서는 웹 사이트의 콘텐츠 페이지에 해당합니다. 그러나 데이터 피드는 XML 문서 또는 쉼표로 구분된 텍스트 파일에서 가져오며 색인화할 컨텐츠 정보를 포함합니다.

XML 데이터 소스는 개별 문서에 해당하는 정보를 포함하는 XML 표준 또는 레코드로 구성됩니다. 이러한 개별 문서가 인덱스에 추가됩니다. 텍스트 데이터 피드에는 개별 문서에 해당하는 개별 새 행으로 구분된 레코드가 포함되어 있습니다. 이러한 개별 문서도 인덱스에 추가됩니다. 어느 경우든 인덱스 커넥터 구성은 피드를 해석하는 방법을 설명합니다. 각 구성은 파일이 상주하는 위치와 서버가 파일에 액세스하는 방법에 대해 설명합니다. 이 구성에서는 &quot;매핑&quot; 정보도 설명합니다. 즉, 각 레코드의 항목을 사용하여 결과 인덱스의 메타데이터 필드를 채우는 방법입니다.

[!DNL Staged Index Connector Definitions] 페이지에 인덱스 커넥터 정의를 추가한 후 이름 또는 유형 값에 대해 *를 제외한 모든 구성 설정을 변경할 수 있습니다.*

[!DNL Index Connector] 페이지에는 다음 정보가 표시됩니다.

* 구성하고 추가한 정의된 인덱스 커넥터의 이름입니다.
* 추가한 각 커넥터에 대해 다음 데이터 소스 유형 중 하나:

   * **텍스트**  - 단순 &quot;플랫&quot; 파일, 쉼표로 구분, 탭으로 구분 또는 기타 일관되게 구분된 형식.
   * **피드**  - XML 피드.
   * **XML**  - XML 문서의 컬렉션입니다.

* 다음 크롤링 및 인덱싱에 대해 커넥터를 사용할지 여부를 지정합니다.
* 데이터 소스의 주소입니다.

[색인 커넥터 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)를 참조하십시오

## 색인 커넥터의 텍스트 및 피드 구성에 대해 색인 프로세스가 작동하는 방식 {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p><span class="uicontrol"> 텍스트 </span>의 경우, 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며, 쉼표 또는 탭과 같은 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p><span class="uicontrol"> 피드 </span>의 경우 각 문서의 데이터는 다음 형식의 정규 표현식 패턴을 사용하여 추출됩니다. </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p><span class="wintitle"> 인덱스 커넥터 추가 </span> 페이지에서 <span class="uicontrol"> 매핑 </span>을 사용하여 캐시에 저장된 데이터 사본을 생성한 다음 Crawler에 대한 링크 목록을 만듭니다. 데이터는 로컬 캐시에 저장되고 구성된 필드로 채워집니다. </p> <p>구문 분석된 데이터는 로컬 캐시에 기록됩니다. </p> <p>이 캐시는 나중에 읽어 Crawler에 필요한 간단한 HTML 문서를 만듭니다. 예: </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p><span class="codeph"> &lt;title&gt; </span> 요소는 제목 메타데이터 필드에 매핑이 있을 때만 생성됩니다. 마찬가지로 <span class="codeph"> &lt;body&gt; </span> 요소는 본문 메타데이터 필드에 매핑이 존재하는 경우에만 생성됩니다. </p> <p> <b>중요</b>: 사전 정의된 URL 메타 태그에 값 지정을 지원하지 않습니다. </p> <p>다른 모든 매핑의 경우, 원본 문서에서 찾은 데이터가 있는 각 필드에 대해 <span class="codeph"> &lt;meta&gt; </span> 태그가 생성됩니다. </p> <p>각 문서의 필드가 캐시에 추가됩니다. 캐시에 기록되는 각 문서에 대해 다음 예와 같이 링크가 생성됩니다. </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>구성의 매핑에는 기본 키로 식별되는 필드가 하나 있어야 합니다. 이 매핑은 캐시에서 데이터를 가져올 때 사용되는 키를 형성합니다. </p> <p>Crawler는 URL <span class="codeph"> 인덱스를 인식합니다. </span> 스키마 접두사로, 로컬에서 캐시한 데이터에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>캐시된 문서 세트를 크롤링합니다. </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 인덱스: </span> 링크는 Crawler의 보류 목록에 추가되고 일반 크롤링 시퀀스에서 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>각 문서를 처리합니다. </p> </td> 
   <td colname="col3"> <p>각 링크의 키 값은 캐시의 항목에 해당하므로 각 링크를 크롤링하면 캐시에서 해당 문서의 데이터를 가져옵니다. 그런 다음 "assembled"를 HTML 이미지로 만들어 처리되고 인덱스에 추가합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 인덱스 커넥터의 XML 구성에 대해 색인 프로세스가 작동하는 방식 {#section_7F1551EA51854C5C99F284CE260526EB}

XML 구성에 대한 색인 지정 프로세스는 다음과 같은 사소한 변경 사항 및 예외가 있는 텍스트 및 피드 구성 프로세스와 유사합니다.

XML 크롤링용 문서는 이미 개별 파일로 분리되어 있으므로 위의 테이블의 1단계와 2단계는 직접 적용되지 않습니다. **[!UICONTROL Host Address]** 페이지의 **[!UICONTROL File Path]** 필드에 URL을 지정하면 일반 HTML 문서로 다운로드하여 처리됩니다. [!DNL Index Connector Add] 다운로드 문서에는 처리된 XML 문서를 가리키는 `<a href="{url}"...` 링크의 컬렉션이 포함되어 있습니다. 이러한 링크는 다음 양식으로 변환됩니다.

```
<a href="index:<ic_config_name>?url="{url}">
```

예를 들어 Adobe 설정에서 다음 링크를 반환한 경우:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

위의 표에서 3단계는 적용되지 않으며 4단계는 크롤링 및 색인 지정 시 완료됩니다.

또는 크롤링 프로세스를 통해 자연스럽게 발견된 다른 문서와 XML 문서를 혼합할 수 있습니다. 이러한 경우 rewrite 규칙( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**)을 사용하여 XML 문서의 URL을 Index Connector로 보낼 수 있습니다.

[크롤링 목록 검색 URL 규칙 정보](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)를 참조하십시오.

예를 들어 다음과 같은 rewrite 규칙이 있다고 가정되어 있습니다.

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

이 규칙은 `.xml`으로 끝나는 URL을 색인 커넥터 링크로 변환합니다. Crawler는 `index:` URL 체계를 인식하고 다시 기록합니다. 다운로드 프로세스는 기본 Index Connector Apache 서버를 통해 리디렉션됩니다. 다운로드한 각 문서는 피드에 사용되는 것과 동일한 정규 표현식 패턴을 사용하여 검사됩니다. 그러나 이 경우 제조된 HTML 문서는 캐시에 저장되지 않습니다. 대신 인덱스 처리를 위해 Crawler에게 직접 전달됩니다.

## 여러 Index Connectors 구성 방법 {#section_C2B14C0F06354A57AEF6238FF3814E5D}

모든 계정에 대해 여러 색인 커넥터 구성을 정의할 수 있습니다. 다음 그림과 같이 **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]**&#x200B;의 드롭다운 목록에 구성이 자동으로 추가됩니다.

![](assets/url_entrypoints_index_connector.png)

드롭다운 목록에서 구성을 선택하면 URL 시작 지점 목록의 끝에 값이 추가됩니다.

>[!NOTE]
>
>비활성화된 인덱스 커넥터 구성이 드롭다운 목록에 추가되지만 선택할 수 없습니다. 동일한 Index Connector 구성을 두 번째로 선택하면 목록의 끝에 추가되고 이전 인스턴스가 삭제됩니다.

증분 크롤링에 대한 Index Connector 진입점을 지정하려면 다음 형식을 사용하여 항목을 추가할 수 있습니다.

```
index:<indexconnector_configuration_name>
```

Crawler는 Index Connectors 페이지에 있고 활성화되어 있는 경우 추가된 각 항목을 처리합니다.

참고: 각 문서의 URL은 색인 커넥터 구성 이름과 문서의 기본 키를 사용하여 작성되므로 증분 업데이트를 수행할 때 동일한 인덱스 커넥터 구성 이름을 사용해야 합니다. 이렇게 하면 [!DNL Adobe Search&Promote]이 이전에 인덱싱된 문서를 올바르게 업데이트할 수 있습니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)도 참조하십시오.

**인덱스 커넥터를 추가할 때 설정 맵 사용**

Index Connector를 추가할 때 선택적으로 기능 **[!UICONTROL Setup Maps]**&#x200B;을 사용하여 데이터 소스의 샘플을 다운로드할 수 있습니다. 색인화 적합성에 대해 데이터가 검토됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>인덱스 커넥터 유형을 선택한 경우.. </p> </th> 
   <th colname="col2" class="entry"> <p>맵 설정 기능... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>텍스트 </p> </td> 
   <td colname="col2"> <p>탭을 먼저 시도한 다음 세로 막대( <span class="codeph">)를 사용하여 구분 기호 값을 결정합니다 | </span>)와 마지막으로 쉼표( <span class="codeph"> , </span>)를 만듭니다. <span class="uicontrol"> 설정 맵 </span>을 클릭하기 전에 구분 기호 값을 이미 지정한 경우 해당 값이 대신 사용됩니다. </p> <p>가장 잘 맞는 구성표는 맵 필드에 적절한 태그 및 필드 값에 대한 추정이 입력됩니다. 또한 구문 분석된 데이터의 샘플링이 표시됩니다. 파일에 헤더 행이 포함되어 있음을 알고 있는 경우 첫 번째 행 <span class="uicontrol"> 헤더를 선택해야 합니다. </span> 설정 함수는 이 정보를 사용하여 결과 맵 항목을 더 잘 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>피드 </p> </td> 
   <td colname="col2"> <p>데이터 소스를 다운로드하고 간단한 XML 구문 분석을 수행합니다. </p> <p>결과 XPath 식별자는 맵 테이블의 태그 행에 표시되고 필드의 비슷한 값이 표시됩니다. 이러한 행은 사용 가능한 데이터만 식별하고 더 복잡한 XPath 정의를 생성하지 않습니다. 그러나 XML 데이터를 설명하고 Itemtag 값을 식별하므로 여전히 유용합니다. </p> <p> <p>참고:  설정 맵 함수는 전체 XML 소스를 다운로드하여 분석을 수행합니다. 파일이 큰 경우 이 작업이 시간 초과될 수 있습니다. </p> </p> <p>성공하면 이 함수는 사용 가능한 모든 XPath 항목을 식별하며, 이 중 많은 항목은 사용하지 않는 것입니다. 결과 맵 정의를 검토하고 필요하지 않거나 원하는 정의를 제거해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>기본 링크 목록이 아니라 대표 개별 문서의 URL을 다운로드합니다. 이 단일 문서는 피드에 사용되는 것과 동일한 메커니즘을 사용하여 구문 분석되며 결과가 표시됩니다. </p> <p><span class="uicontrol"> 추가 </span> 를 클릭하여 구성을 저장하기 전에 URL을 다시 기본 링크 목록 문서로 변경해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**중요**: 파일 파서가 전체 파일을 메모리로 읽으려고 하므로 큰 XML 데이터 집합에서 설정 맵 기능이 작동하지 않을 수 있습니다. 따라서 메모리 부족 상태를 경험할 수 있습니다. 하지만 인덱싱 시 동일한 문서를 처리하는 경우 메모리로 읽히지 않습니다. 대신 대용량 문서는 &quot;이동 중&quot;으로 처리되며 메모리로 완전히 읽지는 않습니다.

**인덱스 커넥터를 추가할 때 미리 보기 사용**

인덱스 커넥터를 추가할 때 필요에 따라 **[!UICONTROL Preview]** 기능을 사용하여 데이터를 저장하고 있는 것처럼 데이터의 유효성을 확인할 수 있습니다. 구성에 대해 테스트를 실행하지만 구성을 계정에 저장하지 않습니다. 테스트는 구성된 데이터 소스에 액세스합니다. 그러나 다운로드 캐시를 임시 위치에 씁니다. 인덱싱 Crawler가 사용하는 주 캐시 폴더와 충돌하지 않습니다.

미리 보기는 Acct:IndexConnector-Preview-Max-Documents에 의해 제어된 5개의 문서만 처리합니다. 미리 본 문서는 인덱싱 Crawler에 표시될 때 소스 형태로 표시됩니다. 이 디스플레이는 웹 브라우저의 &quot;소스 보기&quot; 기능과 비슷합니다. 표준 탐색 링크를 사용하여 미리 보기 세트에서 문서를 탐색할 수 있습니다.

이러한 문서는 직접 처리되고 캐시에 다운로드되지 않으므로 미리 보기에서 XML 구성을 지원하지 않습니다.

## 인덱스 커넥터 정의 추가 {#task_96779B651A654E1F871F55D6DBBC8886}

각 인덱스 커넥터 구성은 해당 소스에 대해 정의된 데이터 항목을 인덱스의 메타데이터 필드에 연결하는 데이터 소스 및 매핑을 정의합니다.

고객이 새 정의 및 활성화된 정의의 효과를 보려면 사이트 인덱스를 다시 만드십시오.

**인덱스 커넥터 정의를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Stage Index Connector Definitions] 페이지에서 **[!UICONTROL Add New Index Connector]** 을 클릭합니다.
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
      <td colname="col2"> <p>인덱스 커넥터 구성의 고유한 이름입니다. 영숫자를 사용할 수 있습니다. "_" 및 "-" 문자도 허용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>유형 </p> </td> 
      <td colname="col2"> <p>데이터의 소스. 선택하는 데이터 소스 유형은 <span class="wintitle"> 인덱스 커넥터 추가 </span> 페이지에서 사용할 수 있는 결과 옵션에 영향을 줍니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> 텍스트 </span> <p>단순 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 기타 일관되게 구분된 형식. 각 줄바꿈 구분 텍스트 행은 개별 문서에 해당하며 지정된 구분 기호를 사용하여 구문 분석됩니다. </p> <p>각 값 또는 열을 열 번호가 참조하는 메타데이터 필드에 1부터 매핑할 수 있습니다. </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> 피드 </span> <p>여러 "행" 정보를 포함하는 기본 XML 문서를 다운로드합니다. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>링크가 포함된 기본 XML 문서 다운로드( 
      <code>
        &lt;a&gt; 
      </code>)을 개별 XML 문서에 추가합니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형: 텍스트</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>: 비활성화된 인덱스 커넥터 구성이 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터가 있는 서버 호스트의 주소를 지정합니다. </p> <p>원하는 경우 다음 예와 같이 데이터 소스 문서에 대한 전체 URI(Uniform Resource Identifier) 경로를 지정할 수 있습니다. </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>또는  </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>URI는 호스트 주소, 파일 경로, 프로토콜 및 선택적으로 사용자 이름 및 암호 필드에 적합한 항목으로 분류됩니다. </p> <p>데이터 소스 파일이 있는 호스트 시스템의 IP 주소 또는 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>단순 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 다른 일관적으로 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>증분 파일 경로 </p> </td> 
      <td colname="col2"> <p>단순 플랫 텍스트 파일, 쉼표로 구분, 탭으로 구분 또는 다른 일관적으로 구분된 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정되면 증분 색인 작업 중에 다운로드 및 처리됩니다. 지정된 파일이 없으면 파일 경로(File Path) 아래에 나열된 파일이 대신 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>수직 파일 경로 </p> </td> 
      <td colname="col2"> <p>세로 업데이트 중에 사용할 단순 플랫 텍스트 파일, 쉼표로 구분된 파일, 탭으로 구분된 파일 또는 세로로 구분된 다른 형식 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 세로 업데이트 작업 중에 다운로드 및 처리됩니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 삭제 </p> </td> 
      <td colname="col2"> <p>행당 단일 문서 식별자 값을 포함하는 단순 플랫 텍스트 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정되면 증분 색인 작업 중에 다운로드 및 처리됩니다. 이 파일에 있는 값은 이전에 인덱싱된 문서를 제거하기 위해 "삭제" 요청을 구성하는 데 사용됩니다. 이 파일의 값은 <span class="uicontrol"> 기본 키 </span> 로 식별되는 열의 전체 또는 증분 파일 경로 파일에 있는 값에 해당해야 합니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용할 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTP 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTPS 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>시간 초과 </p> </td> 
      <td colname="col2"> <p>FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 시간 제한(초)을 지정합니다. 이 값은 30에서 300 사이여야 합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다시 시도 </p> </td> 
      <td colname="col2"> <p>실패한 FTP, SFTP, HTTP 또는 HTTPS 연결에 대한 최대 다시 시도 횟수를 지정합니다. 이 값은 0에서 10 사이여야 합니다. </p> <p>값이 0이면 다시 시도되지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>인코딩 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일에 사용되는 문자 인코딩 시스템을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구분 기호 </p> </td> 
      <td colname="col2"> <p>지정된 데이터 소스 파일의 각 필드를 표시하는 데 사용할 문자를 지정합니다. </p> <p>쉼표 문자( <span class="codeph"> , </span>)는 구분 기호의 예입니다. 쉼표는 지정된 데이터 소스 파일에서 데이터 필드를 구분하는 데 도움이 되는 필드 구분 기호로 작동합니다. </p> <p><span class="uicontrol"> 탭을 선택하십시오. </span> 가로 탭 문자를 구분 기호로 사용하려면 다음을 수행하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 행의 머리글 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일의 첫 번째 행에 데이터가 아닌 머리글 정보만 포함함을 나타냅니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>색인화를 위한 최소 문서 수 </p> </td> 
      <td colname="col2"> <p>양수 값으로 설정하면 다운로드한 파일에 필요한 최소 레코드 수를 지정합니다. 받는 레코드가 적으면 인덱스 작업이 중단됩니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> <p> <b>참고</b>: 이 기능은 전체 인덱스 작업 동안에만 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정합니다. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> 열 </span> <p> 열 번호를 지정합니다. 첫 번째 열은 1(1)입니다. 각 열에 대한 새 맵 행을 추가하려면 <span class="wintitle"> 작업 </span> 아래에서 <span class="uicontrol"> + </span> 를 클릭합니다. </p> <p>데이터 소스의 각 열을 참조할 필요가 없습니다. 대신 값을 건너뛰도록 선택할 수 있습니다. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>가 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>필요한 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 필터링 스크립트 </span>에서 사용하는 컨텐츠를 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보 </a>를 참조하십시오. </p> <p>Index Connector가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 이 필드에는 <span class="wintitle"> 허용 목록 </span> 속성이 설정되어 있습니다. 이 경우 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서가 인덱스에 추가될 때 표시되는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 Index Connector 구성으로 표시된 모든 문서에서 고유해야 합니다. 발생한 모든 중복을 무시합니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용할 하나의 고유 값이 포함되어 있지 않지만 <i>에서 함께 가져오는 두 개 이상의 필드가 고유한 식별자를 형성할 수 있는 경우 여러 개의 <span class="uicontrol"> 열 </span> 값을 세로 막대("|")와 결합하여 <span class="uicontrol"> 기본 키 </span>를 정의할 수 있습니다.</i> </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> HTML을 분리하시겠습니까?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형: 피드</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>: 비활성화된 인덱스 커넥터 구성이 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일이 있는 호스트 시스템의 IP 주소 또는 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 정보의 "행"을 포함하는 기본 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>증분 파일 경로 </p> </td> 
      <td colname="col2"> <p>여러 정보의 "행"을 포함하는 증분 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정되면 증분 색인 작업 중에 다운로드 및 처리됩니다. 지정된 파일이 없으면 파일 경로(File Path) 아래에 나열된 파일이 대신 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>수직 파일 경로 </p> </td> 
      <td colname="col2"> <p>세로 업데이트 중에 사용할 정보의 여러 스파스 "행"을 포함하는 XML 문서의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정된 경우 세로 업데이트 작업 중에 다운로드 및 처리됩니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 삭제 </p> </td> 
      <td colname="col2"> <p>행당 단일 문서 식별자 값을 포함하는 단순 플랫 텍스트 파일의 경로를 지정합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> <p>이 파일이 지정되면 증분 색인 작업 중에 다운로드 및 처리됩니다. 이 파일에 있는 값은 이전에 인덱싱된 문서를 제거하기 위해 "삭제" 요청을 구성하는 데 사용됩니다. 이 파일의 값은 <span class="uicontrol"> 기본 키 </span> 로 식별되는 열의 전체 또는 증분 파일 경로 파일에 있는 값에 해당해야 합니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용할 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTP 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTPS 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> 파일 </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 개별 XML 라인을 식별하는 데 사용할 수 있는 XML 요소를 식별합니다. </p> <p>예를 들어, Adobe XML 문서의 다음 피드 조각에서 Itemtag 값은 <span class="codeph"> 레코드 </span>입니다. </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>양수 값으로 설정하면 다운로드한 파일에 필요한 최소 레코드 수를 지정합니다. 받는 레코드가 적으면 인덱스 작업이 중단됩니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> <p> <b>참고</b>: 이 기능은 전체 인덱스 작업 동안에만 사용됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>XPath 표현식을 사용하여 XML-요소-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> 태그 </span> <p>구문 분석된 XML 데이터의 XPath 표현을 지정합니다. 위의 Adobe XML 문서 예제 를 사용하여 Itemtag 옵션에서 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 <span class="codeph"> displayurl </span> 속성은 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 특성이 <span class="codeph"> 제목 </span>인 <span class="codeph"> 레코드 </span> 요소에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> 제목 </span>에 매핑됩니다. </span></p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph"> 레코드 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> desc </span>에 매핑됩니다.</span> </span></p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph"> 메타데이터 </span> 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 속성은 이름 특성이 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함되어 있으며 메타데이터 필드 <span class="codeph"> 본문 </span>에 매핑됩니다. </span></p> </li> 
      </ul> </p> <p>XPath는 상대적으로 복잡한 표기법입니다. 자세한 내용은 다음 위치에서 확인할 수 있습니다. </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> 을 참조하십시오. </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> 필드 </span> <p>생성된 각 <span class="codeph"> &lt;meta&gt; </span> 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>가 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>필요한 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 필터링 스크립트 </span>에서 사용하는 컨텐츠를 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보 </a>를 참조하십시오. </p> <p>Index Connector가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 이 필드에는 <span class="wintitle"> 허용 목록 </span> 속성이 설정되어 있습니다. 이 경우 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서가 인덱스에 추가될 때 표시되는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 Index Connector 구성으로 표시된 모든 문서에서 고유해야 합니다. 발생한 모든 중복을 무시합니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용할 하나의 고유 값이 포함되어 있지 않지만 <i>에서 함께 가져오는 두 개 이상의 필드가 고유한 식별자를 형성할 수 있는 경우 여러 개의 <span class="uicontrol"> 태그 </span> 정의를 세로 막대("|")와 결합하여 <span class="uicontrol"> 기본 키 </span>를 정의할 수 있습니다.</i> </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> HTML을 분리하시겠습니까?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> 삭제에 사용하시겠습니까?  </span> <p>증분 인덱스 작업 중에만 사용됩니다. 이 XPath 패턴과 일치하는 레코드는 삭제할 항목을 식별합니다. 이러한 각 레코드에 대한 <span class="uicontrol"> 기본 키 </span> 값은 파일 삭제 경로와 같이 "삭제" 요청을 구성하는 데 사용됩니다. </p> <p> <b>참고</b>: 이 기능은 기본적으로 활성화되어 있지 않습니다. 사용할 기능을 활성화하려면 기술 지원 팀에 문의하십시오. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>데이터 소스 유형: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>활성화됨 </p> </td> 
      <td colname="col2"> <p>크롤링과 색인을 위해 구성을 "켜기"로 설정합니다. 또는 구성을 "해제"하여 크롤링 및 색인화를 방지할 수 있습니다. </p> <p> <b>참고</b>: 비활성화된 인덱스 커넥터 구성이 진입점 목록에 있으면 무시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 주소 </p> </td> 
      <td colname="col2"> <p>데이터 소스 파일이 있는 호스트 시스템의 URL 주소를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>파일 경로 </p> </td> 
      <td colname="col2"> <p>링크가 포함된 기본 XML 문서의 경로를 지정합니다( 
      <code>
        &lt;a&gt; 
      </code>)을 개별 XML 문서에 추가합니다. </p> <p>경로는 호스트 주소의 루트에 상대적입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>프로토콜 </p> </td> 
      <td colname="col2"> <p>파일에 액세스하는 데 사용할 프로토콜을 지정합니다. 다음 중에서 선택할 수 있습니다. </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTP 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>필요한 경우 적절한 인증 자격 증명을 입력하여 HTTPS 서버에 액세스할 수 있습니다. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>FTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>SFTP 서버에 액세스하려면 적절한 인증 자격 증명을 입력해야 합니다. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> 파일 </li> 
      </ul> </p> <p> <b>참고</b>: 프로토콜 설정은 호스트 주소 및/또는 파일 경로 필드에 지정된 정보가 있는 경우에만 사용됩니다. 개별 XML 문서는 URL 사양에 따라 HTTP 또는 HTTPS를 사용하여 다운로드됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>지정한 데이터 소스 파일에서 "행"을 정의하는 XML 요소를 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>맵 </p> </td> 
      <td colname="col2"> <p>열 번호를 사용하여 열-메타데이터 매핑을 지정할 수 있습니다. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> 태그 </span> <p>구문 분석된 XML 데이터의 XPath 표현을 지정합니다. 위의 예제 Adobe XML 문서를 사용하여 Itemtag 옵션에서 다음 구문을 사용하여 매핑할 수 있습니다. </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>위의 구문은 다음과 같이 해석됩니다. </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p><span class="codeph"> 레코드 </span> 요소의 <span class="codeph"> displayurl </span> 속성은 메타데이터 필드 <span class="codeph"> page-url </span>에 매핑됩니다. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>이름 특성이 <span class="codeph"> 제목 </span>인 <span class="codeph"> 레코드 </span> 요소에 포함된 <span class="codeph"> 메타데이터 </span> 요소 내에 포함된 <span class="codeph"> 메타 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> 제목 </span>에 매핑됩니다. </span></p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p><span class="codeph"> 레코드 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함된 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 특성은 메타데이터 필드 <span class="codeph"> desc </span>에 매핑됩니다.</span> </span></p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p><span class="codeph"> 메타데이터 </span> 요소 내에 포함되어 있는 <span class="codeph"> 메타데이터 </span> 요소의 </span> 컨텐츠 <span class="codeph"> 속성은 이름 특성이 <span class="codeph"> description </span>인 <span class="codeph"> 레코드 </span> 요소 내에 포함되어 있으며 메타데이터 필드 <span class="codeph"> 본문 </span>에 매핑됩니다. </span></p> </li> 
      </ul> </p> <p>XPath는 상대적으로 복잡한 표기법입니다. 자세한 내용은 다음 위치에서 확인할 수 있습니다. </p> <p><a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> 을 참조하십시오. </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> 필드 </span> <p>생성된 각 &lt;meta&gt; 태그에 사용되는 이름 속성 값을 정의합니다. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> 메타데이터? </span> <p><span class="uicontrol"> 필드 </span>가 현재 계정에 대해 정의된 메타데이터 필드를 선택할 수 있는 드롭다운 목록이 됩니다. </p> <p>필요한 경우 <span class="uicontrol"> 필드 </span> 값은 정의되지 않은 메타데이터 필드일 수 있습니다. 정의되지 않은 메타데이터 필드는 <span class="wintitle"> 필터링 스크립트 </span>에서 사용하는 컨텐츠를 만드는 데 유용합니다. </p> <p><a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> 스크립트 필터링 정보 </a>를 참조하십시오. </p> <p>Index Connector가 맵 필드에서 여러 히트가 있는 XML 문서를 처리할 때 여러 값이 캐시된 결과 문서의 단일 값으로 연결됩니다. 기본적으로 이러한 값은 쉼표 구분 기호를 사용하여 결합됩니다. 그러나 해당 <span class="wintitle"> 필드 </span> 값이 정의된 메타데이터 필드라고 가정합니다. 또한 이 필드에는 <span class="wintitle"> 허용 목록 </span> 속성이 설정되어 있습니다. 이 경우 정의된 첫 번째 구분 기호인 필드의 목록 구분 기호 값이 연결에서 사용됩니다. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> 기본 키?  </span> <p>하나의 맵 정의만 기본 키로 식별됩니다. 이 필드는 이 문서가 인덱스에 추가될 때 표시되는 고유한 참조가 됩니다. 이 값은 색인의 문서 URL에 사용됩니다. </p> <p><span class="uicontrol"> 기본 키 </span> 값은 Index Connector 구성으로 표시된 모든 문서에서 고유해야 합니다. 발생한 모든 중복을 무시합니다. 소스 문서에 <span class="uicontrol"> 기본 키 </span>로 사용할 하나의 고유 값이 포함되어 있지 않지만 <i>에서 함께 가져오는 두 개 이상의 필드가 고유한 식별자를 형성할 수 있는 경우 여러 개의 <span class="uicontrol"> 태그 </span> 정의를 세로 막대("|")와 결합하여 <span class="uicontrol"> 기본 키 </span>를 정의할 수 있습니다.</i> </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> HTML을 분리하시겠습니까?  </span> <p>이 옵션을 선택하면 이 필드의 데이터에 있는 모든 HTML 태그가 제거됩니다. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> 작업 </span> <p>맵에 행을 추가하거나 맵에서 행을 제거할 수 있습니다. 행 순서는 중요하지 않습니다. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) **[!UICONTROL Setup Maps]** 을 클릭하여 데이터 소스의 샘플을 다운로드합니다. 색인화 적합성에 대해 데이터가 검토됩니다. 이 기능은 텍스트 및 피드 유형에만 사용할 수 있습니다.
1. (선택 사항) **[!UICONTROL Preview]** 을 클릭하여 구성의 실제 작업을 테스트합니다. 이 기능은 텍스트 및 피드 유형에만 사용할 수 있습니다.
1. **[!UICONTROL Add]** 을 클릭하여 [!DNL Index Connector Definitions] 페이지와 [!DNL URL Entrypoints] 페이지의 [!DNL Index Connector Configurations] 드롭다운 목록에 구성을 추가합니다.

   [URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.
1. [!DNL Index Connector Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]** 을 클릭합니다.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 인덱스 커넥터 정의 편집 {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

정의한 기존 색인 커넥터를 편집할 수 있습니다.

>[!NOTE]
>
>인덱스 커넥터 이름 또는 [!DNL Type] 드롭다운 목록에서 유형 등의 일부 옵션을 변경할 수 없습니다.

**인덱스 커넥터 정의를 편집하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 제목 아래에서 설정을 변경할 Index Connector 정의 이름에 대해 **[!UICONTROL Edit]** 를 클릭합니다.
1. [!DNL Index Connector Edit] 페이지에서 원하는 옵션을 설정합니다.

   [인덱스 커넥터 정의 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)에서 옵션 표를 참조하십시오.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 **[!UICONTROL rebuild your staged site index]** 을 클릭합니다.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 인덱스 커넥터 정의 설정 보기 {#task_D0B71A7426E54247BDB3468EC576D871}

기존 인덱스 커넥터 정의에 대한 구성 설정을 검토할 수 있습니다.

인덱스 커넥터 정의가 [!DNL Index Connector Definitions] 페이지에 추가되면 해당 유형 설정을 변경할 수 없습니다. 대신 정의를 삭제한 다음 새 정의를 추가해야 합니다.

**인덱스 커넥터 정의 설정을 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 제목 아래에서 설정을 검토하거나 편집할 색인 커넥터 정의 이름을 **[!UICONTROL Edit]**&#x200B;로 클릭합니다.

## 인덱스 커넥터 정의 복사 {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

기존 인덱스 커넥터 정의를 복사하여 작성하려는 새 인덱스 커넥터의 기준으로 사용할 수 있습니다.

인덱스 커넥터 정의를 복사할 때 기본적으로 복사된 정의가 비활성화됩니다. 정의를 활성화하거나 &quot;켜기&quot;하려면 [!DNL Index Connector Edit] 페이지에서 해당 정의를 편집하고 **[!UICONTROL Enable]** 를 선택해야 합니다.

[인덱스 커넥터 정의 편집](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)을 참조하십시오.

**인덱스 커넥터 정의를 복사하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 제목 아래에서 설정을 복제할 인덱스 커넥터 정의 이름을 **[!UICONTROL Copy]**&#x200B;로 클릭합니다.
1. [!DNL Index Connector Copy] 페이지에서 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Copy]**.
1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 인덱스 커넥터 정의 이름 바꾸기 {#task_5132118FC21B47D99881E0ED425225D7}

기존 인덱스 커넥터 정의의 이름을 변경할 수 있습니다.

정의 이름을 바꾼 후 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 선택합니다. 새 정의 이름이 [!DNL URL Entrypoints] 페이지의 드롭다운 목록에 반영되도록 합니다.

색인화할 URL 진입점을 여러 개 추가하는 [을 참조하십시오](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**인덱스 커넥터 정의 이름을 변경하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector] 페이지의 [!DNL Actions] 열 머리글에서 변경할 Index Connector 정의 이름에 대해 **[!UICONTROL Rename]** 를 클릭합니다.
1. [!DNL Index Connector Rename] 페이지의 [!DNL Name] 필드에 정의의 새 이름을 입력합니다.
1. 클릭 **[!UICONTROL Rename]**.
1. 클릭 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. 이전 Index Connector 이름이 목록에 있으면 해당 이름을 제거하고 새로 이름을 바꾼 항목을 추가합니다.

   색인화할 URL 진입점을 여러 개 추가하는 [을 참조하십시오](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (선택 사항) [!DNL Index Connector Definitions] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]** 을 클릭하여 변경한 내용을 되돌립니다.

      [기록 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시를 참조하십시오](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## 인덱스 커넥터 정의 삭제 {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

더 이상 필요하거나 사용하지 않는 기존 인덱스 커넥터 정의를 삭제할 수 있습니다.

**인덱스 커넥터 정의를 삭제하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**&#x200B;를 클릭합니다.
1. [!DNL Index Connector Definitions] 페이지의 [!DNL Actions] 열 머리글에서 제거할 Index Connector 정의 이름에 대해 **[!UICONTROL Delete]** 를 클릭합니다.
1. [!DNL Index Connector Delete] 페이지에서 **[!UICONTROL Delete]** 을 클릭합니다.
