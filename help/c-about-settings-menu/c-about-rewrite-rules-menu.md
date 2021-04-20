---
description: 규칙 다시 작성 메뉴를 사용하여 크롤링 및 검색 URL 및 제목 규칙을 설정합니다.
solution: Target
subtopic: Rewrite Rules
title: 다시 작성 규칙 메뉴 정보
topic: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '10202'
ht-degree: 0%

---


# 다시 작성 규칙 메뉴 {#about-the-rewrite-rules-menu} 정보

규칙 다시 작성 메뉴를 사용하여 크롤링 및 검색 URL 및 제목 규칙을 설정합니다.

## 크롤링 목록 저장소 URL 규칙 정보 {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

URL 크롤링 규칙은 웹 내용 내에서 발생하는 URL을 다시 작성하는 방법을 지정합니다. 규칙 및 조건 수를 제한 없이 지정할 수 있으며 발생한 URL의 모든 부분을 조작할 수 있습니다.

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

크롤링 규칙은 웹 사이트를 방문하는 각 고객에 고유한 세션 ID와 같이 URL의 동적 부분을 재작성하는 데 가장 유용합니다. 다시 작성 규칙을 사용하여 검색 로봇에서 쿼리 매개 변수 등의 URL 부분을 숨길 수도 있습니다. 기본적으로 규칙은 지정되지 않으며 URL 재작성을 수행하지 않습니다.

웹 사이트가 크롤되면 포함된 컨텐츠 URL은 크롤할 추가 웹 페이지의 임시 목록에 저장됩니다. 이 목록에 URL을 추가하기 전에 스토어 다시 작성 규칙이 적용됩니다. 일반적으로 저장소 다시 작성 규칙은 URL에서 세션 ID를 제거하거나 크롤링을 위해 특정 세션 ID를 적용하는 데 사용됩니다. 검색 로봇이 목록에서 URL을 검색할 때 다시 쓰기 규칙을 사용하여 해당 URL의 부분을 다시 조작할 수 있습니다. 일반적으로 검색 규칙은 시간에 민감한 데이터를 URL에 다시 삽입하는 데 사용됩니다. 웹 사이트에서 페이지를 실제로 검색하는 데 사용되는 이 최종 URL입니다.

[크롤링 목록 검색 URL 규칙 검색 정보](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)를 참조하십시오.

일반적으로 저장소 URL 규칙만 사용합니다. URL 규칙 검색은 URL에 세션 ID와 같은 동적 데이터가 포함되어 있고 동적 데이터가 시간이 경과함에 따라 유효한 상태로 바뀌는 경우에만 필요합니다. 이 경우 [스토어 URL 규칙]을 사용하여 발견된 URL에서 데이터의 최신 상태를 가져옵니다. 그런 다음 검색 로봇이 페이지를 검색하려고 할 때 URL 규칙 검색을 사용하여 해당 데이터를 각 URL에 추가합니다.

각 규칙은 다시 작성 규칙(RewriteRule) 지시문과 하나 이상의 선택적 다시 작성 조건(RewriteCond)으로 지정됩니다. 규칙의 순서는 중요합니다. 규칙 세트는 규칙별로 규칙을 통해 반복됩니다. 규칙이 일치하면 해당 다시 작성 조건을 반복합니다. 크롤링 URL 규칙은 다음과 같은 방식으로 지정됩니다.

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

포함된 URL이 발견되면 검색 로봇은 URL을 각 크롤링 규칙의 패턴과 일치시킵니다. 패턴이 일치하면 다시 작성 엔진은 해당 RewriteCond 지시문을 찾습니다. 조건이 없는 경우 URL은 대체 문자열에서 생성된 새 값으로 대체되며 규칙 세트의 다음 규칙으로 계속됩니다. 조건이 있는 경우 나열된 순서대로 처리됩니다. 다시 작성 엔진은 조건 패턴(CondPattern)을 테스트 문자열(TestString)과 일치시킵니다. 두 일치 조건이 있으면 사용 가능한 조건이 없을 때까지 다음 조건이 처리됩니다. 모든 조건이 일치하는 경우 URL은 규칙에 지정된 대체로 대체됩니다. 조건이 충족되지 않으면 전체 조건 세트와 해당 규칙이 실패합니다.

## 다시 작성 규칙 지시문 정보 {#section_162122340BB34F12BB9A36DC9349092B}

RewriteRule 지시문에는 다음과 같은 양식이 있습니다.

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` 현재 URL에 적용되는 POSIX 정규 표현식이 될 수 있습니다. &quot;현재 URL&quot;은 이전 규칙이 이미 URL과 일치하고 변경되었을 수 있으므로 요청된 원래 URL과 다를 수 있습니다.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

&quot;not&quot; 문자(&#39;!&#39;)는 사용할 수 없습니다. 를 클릭하여 패턴에 접두사를 붙입니다. &quot;not&quot; 문자는 현재 URL이 이 패턴과 일치하지 않는 경우에만 패턴을 무효화할 수 있습니다. &quot;not&quot; 문자는 네거티브 패턴과 일치시키는 것이 낫거나 최종 기본 규칙으로 사용할 수 있습니다.

>[!NOTE]
>
>&quot;not&quot; 문자와 그룹화된 와일드카드를 모두 패턴에 사용할 수 없습니다. 또한 대체 문자열에 $N이 들어 있을 때는 무효화된 패턴을 사용할 수 없습니다.

괄호를 사용하여 패턴에서 역참조를 만들 수 있습니다. 이 역참조는 대체 및 CondPattern에서 참조할 수 있습니다.

**대체** URL은 다음을 포함하는 대체 문자열로 대체됩니다.

일반 텍스트:전달된 텍스트는 변경되지 않고 그대로 유지됩니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음은 두 가지 유형의 역참조입니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RewriteCond** Backreferences마지막으로 일치한 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0) 형식을 사용합니다.  &lt;>

변수:NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열입니다. 환경 변수 설정에 대한 자세한 내용은 `*[E]*` 플래그를 참조하십시오.

함수:${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 *key*&#x200B;의 모든 문자를 인코딩합니다.
* &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않았습니다.공백은 &#39;+&#39;로 번역되며 다른 모든 문자는 %xx URL 인코딩된 동등한 문자로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL 인코딩 문자가 다시 단일 문자로 변환됩니다.

>[!NOTE]
>
>특별한 대체 문자열이 있습니다.`'-'` 즉, &quot;대체 없음&quot;을 의미합니다. `'-'` 문자열은 종종 C(체인) 플래그와 함께 사용되므로 대체가 발생하기 전에 여러 패턴에 URL을 일치시킬 수 있습니다.

**플래그**

(선택 사항) 대괄호 `[]`로 플래그를 묶습니다. 여러 개의 플래그가 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>마지막 규칙. </p> <p>재작성 프로세스를 중단하고 추가 재작성 규칙을 적용하지 않습니다. 현재 URL에 대한 추가 처리를 방지하려면 이 플래그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>다음 라운드. </p> <p> 원래 URL이 아닌 마지막 재작성 규칙의 URL을 사용하여 재작성 프로세스를 다시 실행합니다(첫 번째 재작성 규칙으로 다시 시작). 마감일을 만들지 않도록 주의해라! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>다음 규칙과 연계됩니다. </p> <p>현재 규칙을 다음 규칙에 연결(다음 규칙에 연결할 수도 있음 등). 규칙이 일치하면 대체 프로세스가 평소대로 계속됩니다. 규칙이 일치하지 않으면 후속 연쇄 규칙을 모두 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p> 패턴이 현재 URL에 대해 일치할 때 패턴은 대/소문자를 구분하지 않습니다(즉, 'A-Z'와 'a-z' 사이에는 아무런 차이가 없습니다). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '건너뛰기|S=num' </p> </td> 
   <td colname="col2"> <p>다음 규칙 또는 규칙을 건너뛰십시오. </p> <p> 현재 규칙이 일치하면 이 플래그는 규칙 세트의 다음 num 규칙을 생략하도록 다시 작성 엔진을 강제 적용합니다. 이 플래그를 사용하여 의사 if-then-else 구문을 만듭니다. then 절의 마지막 규칙은 skip=N이 되며 여기서 N은 else-절의 규칙 수입니다. </p> <p> <p>참고: 이 플래그는 'chain|C' 플래그와 같지 않습니다.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>환경 변수를 설정합니다. </p> <p>값 VAL에 설정된 환경 변수 "VAR"를 만듭니다. 여기서 VAL은 확장되는 정규 표현식 역참조, $N 및 %N을 포함할 수 있습니다. 이 플래그를 두 번 이상 사용하여 여러 변수를 설정할 수 있습니다. 이 변수는 %{VAR}을(를) 통해 다음 RewriteCond 패턴에서 나중에 참조되지 않을 수 있습니다. </p> <p>이 플래그를 사용하여 URL의 정보를 제거하고 기억하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>저장소 다시 작성 규칙 및 다시 작성 규칙 검색은 변수 값을 공유합니다. 이러한 비헤이비어로 인해 포함된 URL이 발견되어 저장될 때 변수를 시간 구분 세션 id 값으로 설정할 수 있습니다. 임시 저장소 목록에서 다음 URL을 검색할 때 해당 페이지를 검색하기 전에 최신 세션 ID 값을 추가할 수 있습니다.

**함수가 있는 RewriteRule의 예**

`"www.mydomain.com"` 및 `"www.MyDomain.com"` 문자열을 다르게 처리하는 대/소문자를 구분하는 서버가 있다고 가정합니다. 서버가 올바르게 작동하려면 일부 문서에 `"www.MyDomain.com."`을(를) 참조하는 링크가 포함되어 있더라도 도메인이 항상 `"www.mydomain.com"`인지 확인하십시오. 이렇게 하려면 다음 규칙을 사용할 수 있습니다.

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

이 다시 작성 규칙은 `tolower` 함수를 사용하여 URL의 도메인 부분을 다시 작성하여 다음과 같이 항상 소문자가 되도록 합니다.

1. 패턴 `(^https://([^/]*)(.*)$)`에는 URL의 `https://`와 첫 번째 `/` 사이의 모든 문자와 일치하는 역참조 `([^/]*)`이 있습니다. 패턴에는 URL의 나머지 모든 문자와 일치하는 두 번째 역참조 `(.*)`도 포함되어 있습니다.

1. 대체 `(https://${tolower:$1}$2)`은 URL의 나머지 부분 `(https://${tolower:$1} $2)`이(가) 그대로 남아 있는 첫 번째 역참조 `tolower` 함수를 사용하여 URL을 다시 작성하도록 검색 엔진에 지시합니다.`(https:// ${tolower:$1}$2)`

따라서 `https://www.MyDomain.com/INTRO/index.Html` 형식의 URL이 `https://www.mydomain.com/INTRO/index.Html`(으)로 다시 작성됩니다.

## RewriteCond 지시문 정보 {#section_CD5A19B2D3204F73B645411931FC34A1}

RewriteCond 지시문은 규칙 조건을 정의합니다. RewriteCond가 RewriteRule 앞에 있으면 해당 패턴이 현재 제목과 일치하고 추가 조건이 적용되는 경우에만 규칙이 사용됩니다. 다시 작성 조건은 다음 양식을 사용합니다.

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` 은 다음 구문을 포함할 수 있는 문자열입니다.

일반 텍스트:전달된 텍스트는 변경되지 않고 그대로 유지됩니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음은 두 가지 유형의 역참조입니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** Backreferences마지막으로 일치한 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0) 형식을 사용합니다.&lt;>

변수:이 변수는 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열일 수 있습니다. 변수 설정에 대한 자세한 내용은 RewriteRule *`[E]`* 플래그를 참조하십시오.

함수:${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 키의 모든 문자를 인코딩합니다. &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않고 남아 있고, 공백은 &#39;+&#39;로 변환되며 다른 모든 문자가 `%xx` URL 인코딩된 상응하는 것으로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 `%xx` URL은 문자를 다시 단일 문자로 인코딩합니다.

**일부** 추가가 있는 표준 확장 일반 표현식을 ContextPatterns로 변환합니다. 패턴 문자열 앞에 `!` 문자(느낌표)를 붙여 일치하지 않는 패턴을 지정할 수 있습니다. 실제 정규 표현식 문자열 대신 다음 특수 변형 중 하나를 사용할 수 있습니다.

>[!NOTE]
>
>이러한 모든 테스트에 느낌표(&#39;!&#39;)를 접두사로 지정할 수도 있습니다. 그들의 의미를 무효화하다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘가 필요 없음 </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern보다 사전적으로 작으면 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>보다 탁월하게 </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern보다 사전적으로 큰 경우 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘 동일함. </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern과 사전적으로 같으면 true입니다. 즉, 두 문자열은 정확하게 동일합니다(문자별로 문자). CondPattern이 ""(2개의 따옴표)일 경우 TestString을 빈 문자열로 비교합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**플래그**
(선택 사항) 대괄호로 플래그를 묶습니다 `[]`. 여러 개의 플래그가 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p> 아니요. </p> <p>이 플래그는 테스트를 대/소문자를 구분하지 않도록 합니다. 즉, 확장된 TestString과 CondPattern에서 'A-Z'와 'a-z'는 모두 아무런 차이가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>또는 다음 조건. </p> <p>이 플래그를 사용하여 규칙 조건을 암시적 AND 대신 로컬 OR과 결합합니다. 이 플래그를 사용하지 않으면 콘드/규칙을 여러 번 작성해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

일부 웹 페이지는 방문자가 처음으로 사이트에 도착할 때 &quot;sessionid&quot; CGI 변수를 할당합니다. 이 변수는 방문자를 식별하는 데 사용되며, 방문자가 사이트를 탐색할 때 변수가 전달됩니다. 검색 로봇은 사이트의 방문자 모양이므로 &quot;sessionid&quot; 번호가 할당됩니다. 검색 로봇은 두 번째 사이트 페이지가 새 값을 할당하려고 해도 이 단일 &quot;sessionid&quot; 값을 유지합니다. 이를 위해서는 두 개의 다시 작성 규칙이 필요합니다.

첫 번째 규칙은 세션 id 변수를 식별하고 저장하는 데 사용됩니다.

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule은 E-flag `([E=sessionid:$1])`을 사용하여 세션 CGI 매개 변수의 현재 값을 변수 `sessionid`에 할당합니다. `$1`은 RewriteRule의 패턴 `([^&#]+)`에서 첫 번째 괄호 집합 사이에 포함된 첫 번째 역참조를 참조합니다.

정규 표현식 `^&#]+`은 단어 `sessionid`과 다음 `**&**or**#**` 문자 사이의 URL 부분을 찾습니다. 이 RewriteRule은 세션 ID 변수의 초기 값을 만드는 데만 사용되므로 다시 작성되지 않습니다. 규칙의 대체 필드가 `-`으로 설정되어 다시 작성할 필요가 없음을 나타냅니다.

RewriteCond는 변수 `sessionid`( `%{sessionid}`)를 조사합니다. 단일 문자(!+), RewriteRule이 일치합니다.

이 규칙을 사용하여 URL은 `https://www.domain.com/home/?sessionid=1234&function=start`으로 읽히고 `1234` 값을 `sessionid` 변수에 할당합니다.

두 번째 규칙은 다음 RewriteRule 패턴과 일치하는 모든 URL을 다시 작성하는 데 사용됩니다.

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule 패턴에는 다음 두 가지 역참조가 포함되어 있습니다.`(.+)` 및 `(.*)`. 첫 번째 역참조는 `sessionid` 앞의 모든 문자와 일치합니다. 두 번째 역참조는 `&` 또는 `#` 종료 후 모든 문자와 일치합니다.

대체 패턴은 첫 번째 역참조를 사용하여 URL을 다시 쓰고, 그 다음에 첫 번째 규칙 `%{sessionid}`에 의해 정의된 세션 ID 변수의 값을 뒤에 두 번째 역참조를 사용하여 다시 기록합니다.`($1sessionid=%{sessionid} $2)`

이 RewriteRule에 RewriteCond가 포함되어 있지 않습니다. 따라서 RewriteRule *Pattern*&#x200B;과 일치하는 모든 URL에 대해 다시 작성합니다. 따라서 sessionid 변수( `%{sessionid}`)의 값이 `1234`이면 `https://www.domain.com/products/?sessionid=5678&function=buy` 형식의 URL이 `https://www.domain.com/products/?sessionid=1234&function=buy`으로 다시 작성됩니다.

## 감사의 말 {#section_B17088EF38244496BC1DDD4ECF75EB5B}

다시 작성 엔진 소프트웨어는 Apache Group에서 Apache HTTP 서버 프로젝트(https://www.apache.org/)에 사용하기 위해 개발했습니다.

## 크롤링 목록 저장소 URL 규칙 {#task_22DD40DF95584B12BE8E6ECFBF579BCD} 추가

크롤링 목록 저장소 URL 규칙을 추가하여 웹 콘텐츠 내에서 발생하는 URL이 어떻게 재작성되는지 지정할 수 있습니다. 규칙 및 조건 수를 제한 없이 지정할 수 있으며 발생한 URL의 모든 부분을 조작할 수 있습니다.

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**크롤링 목록 저장소 URL 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Store URL Rules]**&#x200B;를 클릭합니다.
1. [!DNL Crawl List Store URL Rules] 필드에 원하는 규칙을 입력합니다.

   &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.
1. (선택 사항) [!DNL Crawl List Store URL Rules] 페이지의 [!DNL Test Crawl List Store URL Rules] 필드에 테스트할 크롤링 규칙이 있는 테스트 URL을 입력한 다음 **테스트**&#x200B;를 클릭합니다.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL Crawl List Store URL Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 크롤링 목록 검색 URL 규칙 {#concept_EC8E2E48B99A458D8567B526C9827CBA}

URL 크롤링 규칙은 웹 콘텐츠 내에서 발생하는 URL을 어떻게 다시 작성하는지를 지정합니다. 규칙 및 조건 수를 제한 없이 지정할 수 있으며 발생한 URL의 모든 부분을 조작할 수 있습니다.

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

규칙이 고객에게 미치는 영향을 보려면 먼저 사이트 색인을 다시 작성해야 합니다.

크롤링 규칙은 웹 사이트를 방문하는 각 고객에 고유한 세션 ID와 같이 URL의 동적 부분을 재작성하는 데 가장 유용합니다. 다시 작성 규칙을 사용하여 검색 로봇에서 쿼리 매개 변수 등의 URL 부분을 숨길 수도 있습니다. 기본적으로 규칙은 지정되지 않으며 URL 재작성을 수행하지 않습니다.

웹 사이트가 크롤되면 포함된 컨텐츠 URL은 크롤할 추가 웹 페이지의 임시 목록에 저장됩니다. 검색 로봇이 목록에서 URL을 검색할 때 다시 쓰기 규칙 검색을 사용하여 해당 URL의 부분을 조작합니다. 일반적으로 검색 규칙은 시간 구분 데이터를 URL에 삽입하는 데 사용됩니다. 웹 사이트에서 페이지를 실제로 검색하는 데 사용되는 이 최종 URL입니다.

다시 작성 규칙 검색은 URL에 세션 ID와 같은 동적 데이터가 포함되어 있고 동적 데이터가 시간이 경과하여 유효한 상태로 변경되는 경우에만 필요합니다. 이 경우 [다시 작성 규칙 저장]을 사용하여 발견된 URL에서 데이터의 최신 상태를 가져옵니다. 그런 다음 다시 작성 규칙 검색을 사용하여 검색 로봇이 페이지를 검색할 때 각 URL에 해당 데이터를 추가합니다.

각 규칙은 다시 작성 규칙(RewriteRule) 지시문과 하나 이상의 선택적 다시 작성 조건(RewriteCond)으로 지정됩니다. 규칙의 순서는 중요합니다. 규칙 세트는 규칙별로 규칙을 통해 반복됩니다. 규칙이 일치하면 해당 다시 작성 조건을 반복합니다. 크롤링 URL 규칙은 다음과 같은 방식으로 지정됩니다.

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

포함된 URL이 발견되면 검색 로봇은 URL을 각 크롤링 규칙의 패턴과 일치시킵니다. 패턴이 일치하면 다시 작성 엔진은 해당 RewriteCond 지시문을 찾습니다. 조건이 없는 경우 URL은 대체 문자열에서 생성된 새 값으로 대체되며 규칙 세트의 다음 규칙으로 계속됩니다. 조건이 있는 경우 나열된 순서대로 처리됩니다. 다시 작성 엔진은 조건 패턴(CondPattern)을 테스트 문자열(TestString)과 일치시킵니다. 두 일치 조건이 있으면 사용 가능한 조건이 없을 때까지 다음 조건이 처리됩니다. 모든 조건이 일치하는 경우 URL은 규칙에 지정된 대체로 대체됩니다. 조건이 충족되지 않으면 전체 조건 세트와 해당 규칙이 실패합니다.

## 다시 작성 규칙 지시문 정보 {#section_32B24B29627946398AFBC5F869A610CB}

RewriteRule 지시문에는 다음과 같은 양식이 있습니다.

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` 현재 URL에 적용되는 POSIX 정규 표현식이 될 수 있습니다. &quot;현재 URL&quot;은 이전 규칙이 이미 URL과 일치하고 변경되었을 수 있으므로 요청된 원래 URL과 다를 수 있습니다.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

&quot;not&quot; 문자(&#39;!&#39;)는 사용할 수 없습니다. 를 클릭하여 패턴에 접두사를 붙입니다. &quot;not&quot; 문자는 현재 URL이 이 패턴과 일치하지 않는 경우에만 패턴을 무효화할 수 있습니다. &quot;not&quot; 문자는 네거티브 패턴과 일치시키는 것이 낫거나 최종 기본 규칙으로 사용할 수 있습니다.

>[!NOTE]
>
>&quot;not&quot; 문자와 그룹화된 와일드카드를 모두 패턴에 사용할 수 없습니다. 또한 대체 문자열에 $N이 들어 있을 때는 무효화된 패턴을 사용할 수 없습니다.

괄호를 사용하여 패턴에서 역참조를 만들 수 있습니다. 이 역참조는 대체 및 CondPattern에서 참조할 수 있습니다.

**대체** URL은 다음을 포함하는 대체 문자열로 대체됩니다.

일반 텍스트:전달된 텍스트는 변경되지 않고 그대로 유지됩니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음은 두 가지 유형의 역참조입니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** RewriteCond Backreferences** 마지막 일치 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0 &lt;= N &lt;= 9) 형식을 사용합니다.

변수:NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열입니다. 환경 변수 설정에 대한 자세한 내용은 *[E]* 플래그를 참조하십시오.

함수:${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 *key*&#x200B;의 모든 문자를 인코딩합니다.
* &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않았습니다.공백은 &#39;+&#39;로 번역되며 다른 모든 문자는 %xx URL 인코딩된 동등한 문자로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL 인코딩 문자가 다시 단일 문자로 변환됩니다.

>[!NOTE]
>
>특별한 대체 문자열이 있습니다.&#39;-&#39;는 &quot;대체 금지&quot;를 의미합니다. &#39;-&#39; 문자열은 종종 C(체인) 플래그와 함께 사용되므로 대체가 발생하기 전에 여러 패턴에 URL을 일치시킬 수 있습니다.

**플래그**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>마지막 규칙. </p> <p>재작성 프로세스를 중단하고 추가 재작성 규칙을 적용하지 않습니다. 현재 URL에 대한 추가 처리를 방지하려면 이 플래그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>다음 라운드. </p> <p> 원래 URL이 아닌 마지막 재작성 규칙의 URL을 사용하여 재작성 프로세스를 다시 실행합니다(첫 번째 재작성 규칙으로 다시 시작). 마감일을 만들지 않도록 주의해라. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>다음 규칙과 연계됩니다. </p> <p>현재 규칙을 다음 규칙에 연결(다음 규칙에 연결할 수도 있음 등). 규칙이 일치하면 대체 프로세스가 평소대로 계속됩니다. 규칙이 일치하지 않으면 후속 연쇄 규칙을 모두 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p> 패턴이 현재 URL에 대해 일치할 때 패턴은 대/소문자를 구분하지 않습니다(즉, 'A-Z'와 'a-z' 사이에는 아무런 차이가 없습니다). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '건너뛰기|S=num' </p> </td> 
   <td colname="col2"> <p>다음 규칙 또는 규칙을 건너뛰십시오. </p> <p> 현재 규칙이 일치하면 이 플래그는 규칙 세트의 다음 num 규칙을 생략하도록 다시 작성 엔진을 강제 적용합니다. 이 플래그를 사용하여 의사 if-then-else 구문을 만듭니다. then 절의 마지막 규칙은 skip=N이 되며 여기서 N은 else-절의 규칙 수입니다. </p> <p> <p>참고: 이 플래그는 'chain|C' 플래그와 같지 않습니다.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>환경 변수를 설정합니다. </p> <p>값 VAL에 설정된 환경 변수 "VAR"를 만듭니다. 여기서 VAL은 확장되는 정규 표현식 역참조, $N 및 %N을 포함할 수 있습니다. 이 플래그를 두 번 이상 사용하여 여러 변수를 설정할 수 있습니다. 이 변수는 %{VAR}을(를) 통해 다음 RewriteCond 패턴에서 나중에 참조되지 않을 수 있습니다. </p> <p>이 플래그를 사용하여 URL의 정보를 제거하고 기억하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>저장소 다시 작성 규칙 및 다시 작성 규칙 검색은 변수 값을 공유합니다. 이러한 비헤이비어로 인해 포함된 URL이 발견되어 저장될 때 변수를 시간 구분 세션 id 값으로 설정할 수 있습니다. 임시 저장소 목록에서 다음 URL을 검색할 때 해당 페이지를 검색하기 전에 최신 세션 ID 값을 추가할 수 있습니다.

**함수가 있는 RewriteRule의 예**

&quot;www.mydomain.com&quot; 및 &quot;www.MyDomain.com&quot; 문자열을 다르게 처리하는 대/소문자 구분 서버가 있다고 가정해 보십시오. 서버가 올바르게 작동하려면 일부 문서에 &quot;www.MyDomain.com&quot;을 참조하는 링크가 포함되어 있더라도 도메인이 항상 &quot;www.mydomain.com&quot;이어야 합니다. 이렇게 하려면 다음 규칙을 사용할 수 있습니다.

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

이 다시 작성 규칙은 `tolower` 함수를 사용하여 URL의 도메인 부분을 다시 작성하여 다음과 같이 항상 소문자가 되도록 합니다.

1. 패턴 `(^https://([^/]*)(.*)$)`에는 URL의 `https://`와 첫 번째 `/` 사이의 모든 문자와 일치하는 역참조 ** `([^/]*)`**가 포함되어 있습니다. 패턴에는 URL의 나머지 모든 문자와 일치하는 두 번째 역참조 `(.*)`도 포함되어 있습니다.
1. 대체 `(https://${tolower:$1}$2)`은 URL의 나머지 부분 `(https://${tolower:$1} $2)`이(가) 그대로 남아 있는 첫 번째 역참조 `tolower` 함수를 사용하여 URL을 다시 작성하도록 검색 엔진에 지시합니다.`(https:// ${tolower:$1}$2)`

따라서 `https://www.MyDomain.com/INTRO/index.Html` 형식의 URL이 `https://www.mydomain.com/INTRO/index.Html`(으)로 다시 작성됩니다.

## RewriteCond 지시문 정보 {#section_ADD642A24B68452CB98294A0BD687EC3}

RewriteCond 지시문은 규칙 조건을 정의합니다. RewriteCond가 RewriteRule 앞에 있으면 해당 패턴이 현재 제목과 일치하고 추가 조건이 적용되는 경우에만 규칙이 사용됩니다. 다시 작성 조건은 다음 양식을 사용합니다.

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` 은 다음 구문을 포함할 수 있는 문자열입니다.

일반 텍스트:전달된 텍스트는 변경되지 않고 그대로 유지됩니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음은 두 가지 유형의 역참조입니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** Backreferences마지막으로 일치한 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0) 형식을 사용합니다.&lt;>

변수:이 변수는 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열일 수 있습니다. 변수 설정에 대한 자세한 내용은 RewriteRule *`[E]`* 플래그를 참조하십시오.

함수:${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 키의 모든 문자를 인코딩합니다. &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않고 그대로 남아 있고, 공백은 &#39;+&#39;로 변환되며 다른 모든 문자는 %xx URL 인코딩된 상응하는 것으로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL은 문자를 다시 단일 문자로 인코딩합니다.

**일부** 추가가 있는 표준 확장 일반 표현식을 ContextPatterns로 변환합니다. 패턴 문자열에 &#39;!&#39; 접두사를 추가할 수 있습니다. 문자(느낌표)를 사용하여 일치하지 않는 패턴을 지정합니다. 실제 정규 표현식 문자열 대신 다음 특수 변형 중 하나를 사용할 수 있습니다.

>[!NOTE]
>
>이러한 모든 테스트에 느낌표(&#39;!&#39;)를 접두사로 지정할 수도 있습니다. 그들의 의미를 무효화하다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘가 필요 없음 </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern보다 사전적으로 작으면 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>보다 탁월하게 </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern보다 사전적으로 큰 경우 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘 동일함. </p> <p> CondPattern을 일반 문자열로 취급하고 TestString과 사전적으로 비교합니다. TestString이 CondPattern과 사전적으로 같으면 true입니다. 즉, 두 문자열은 정확하게 동일합니다(문자별로 문자). CondPattern이 ""(2개의 따옴표)일 경우 TestString을 빈 문자열로 비교합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**플래그**
(선택 사항) 대괄호로 플래그를 묶습니다 `[]`. 여러 개의 플래그가 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p> 아니요. </p> <p>이 플래그는 테스트를 대/소문자를 구분하지 않도록 합니다. 즉, 확장된 TestString과 CondPattern에서 'A-Z'와 'a-z'는 모두 아무런 차이가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>또는 다음 조건. </p> <p>이 플래그를 사용하여 규칙 조건을 암시적 AND 대신 로컬 OR과 결합합니다. 이 플래그를 사용하지 않으면 콘드/규칙을 여러 번 작성해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

일부 웹 페이지는 방문자가 처음으로 사이트에 도착할 때 &quot;sessionid&quot; CGI 변수를 할당합니다. 이 변수는 방문자를 식별하는 데 사용되며, 방문자가 사이트를 탐색할 때 변수가 전달됩니다. 검색 로봇은 사이트의 방문자 모양이므로 &quot;sessionid&quot; 번호가 할당됩니다. 검색 로봇은 두 번째 사이트 페이지에서 새 값을 할당하려고 해도 이 단일 &quot;sessionid&quot; 값을 유지합니다. 이를 위해서는 두 개의 다시 작성 규칙이 필요합니다.

첫 번째 규칙은 세션 id 변수를 식별하고 저장하는 데 사용됩니다.

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

RewriteRule은 E-flag `([E=sessionid:$1])`을 사용하여 세션 CGI 매개 변수의 현재 값을 변수 `sessionid`에 할당합니다. `$1`은 RewriteRule의 패턴 `([^&#]+)`에서 첫 번째 괄호 집합 사이에 포함된 첫 번째 역참조를 참조합니다.

정규 표현식 `^&#]+`은 단어 `sessionid`과 next**&amp;**또는**#**character 사이의 URL의 부분을 찾습니다. 이 RewriteRule은 세션 ID 변수의 초기 값을 만드는 데만 사용되므로 다시 작성되지 않습니다. 규칙의 대체 필드가 `-`으로 설정되어 다시 작성할 필요가 없음을 나타냅니다.

RewriteCond는 변수 `sessionid`( `%{sessionid}`)를 조사합니다. 단일 문자(!+), RewriteRule이 일치합니다.

이 규칙을 사용하여 URL은 `https://www.domain.com/home/?sessionid=1234&function=start`으로 읽히고 `1234` 값을 `sessionid` 변수에 할당합니다.

두 번째 규칙은 다음 RewriteRule 패턴과 일치하는 모든 URL을 다시 작성하는 데 사용됩니다.

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

RewriteRule 패턴에는 다음 두 가지 역참조가 포함되어 있습니다.`(.+)` 및 `(.*)`. 첫 번째 역참조는 `sessionid` 앞의 모든 문자와 일치합니다. 두 번째 역참조는 `&` 또는 `#` 종료 후 모든 문자와 일치합니다.

대체 패턴은 첫 번째 역참조를 사용하여 URL을 다시 쓰고, 그 다음에 첫 번째 규칙 `%{sessionid}`에 의해 정의된 세션 ID 변수의 값을 뒤에 두 번째 역참조를 사용하여 다시 기록합니다.`($1sessionid=%{sessionid} $2)`

이 RewriteRule에 RewriteCond가 포함되어 있지 않습니다. 따라서 RewriteRule *Pattern*&#x200B;과 일치하는 모든 URL에 대해 다시 작성합니다. 따라서 sessionid 변수( `%{sessionid}`)의 값이 `1234`이면 `https://www.domain.com/products/?sessionid=5678&function=buy` 형식의 URL이 `https://www.domain.com/products/?sessionid=1234&function=buy`으로 다시 작성됩니다.

## 감사의 말 {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

다시 작성 엔진 소프트웨어는 Apache Group에서 Apache HTTP 서버 프로젝트(https://www.apache.org/)에 사용하기 위해 개발했습니다.

## 크롤링 목록 검색 URL 규칙 {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A} 추가

크롤링 목록 검색 URL 규칙을 추가하여 웹 컨텐츠 내에서 발생한 URL이 어떻게 재작성되는지 지정할 수 있습니다. 다시 작성 규칙 검색은 URL에 세션 ID와 같은 동적 데이터가 포함되어 있고 동적 데이터가 시간이 경과하여 유효한 상태로 변경되는 경우에만 필요합니다.

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**크롤링 목록을 추가하려면 URL 규칙 검색**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**&#x200B;를 클릭합니다.
1. [!DNL Crawl List Retrieve URL Rules] 필드에 원하는 규칙을 입력합니다.

   &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.
1. (선택 사항) [!DNL Crawl List Retrieve URL Rules] 페이지의 [!DNL Test Crawl List Retrieve URL Rules] 필드에 테스트할 크롤링 규칙이 있는 테스트 URL을 입력한 다음 **테스트**&#x200B;를 클릭합니다.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL Crawl List Retrieve URL Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 크롤링 제목 규칙 {#concept_BD3A576987DA4D93A998B0B9CDDC3C79} 정보

크롤링 제목 규칙은 검색 색인에 저장하기 전에 웹 콘텐츠 내에서 발생하는 제목이 어떻게 다시 작성되는지 지정합니다.

<!-- 

c_about_crawl_title_rules.xml

 -->

예를 들어 다시 작성 규칙을 사용하여 조직 이름과 같은 제목의 일부를 제거할 수 있습니다. 웹 사이트가 크롤되면 발생한 제목이 임시 버퍼에 저장됩니다. 그러나 이 버퍼에 제목을 추가하기 전에 제목 규칙이 해당 버퍼에 적용됩니다. 기본적으로 사이트 검색/머천다이징에는 크롤링 제목 규칙이 없으며 제목을 수정하지 않습니다.

규칙이 고객에게 미치는 영향을 보기 전에 사이트 색인을 다시 작성하십시오.

기록 기능을 사용하여 제목 규칙 크롤링 변경 사항을 신속하게 되돌릴 수 있습니다.

규칙은 다음 두 가지 주요 요소로 구성됩니다.RewriteRule 및 선택적 RewriteCode를 반환합니다. 규칙 및 조건 수를 제한 없이 지정할 수 있습니다. 규칙 세트는 규칙별로 반복되므로 이러한 규칙의 순서가 중요합니다. 규칙이 일치하면 해당 다시 작성 조건을 모두 반복합니다(선택 사항). 크롤링 URL 규칙은 다음과 같은 방식으로 지정됩니다.

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

제목이 발견되면 검색 로봇은 각 크롤링 규칙의 패턴과 제목을 일치시킵니다. 패턴이 일치하면 다시 작성 엔진은 해당 RewriteCond 지시문을 찾습니다. 조건이 없는 경우 URL은 대체 문자열에서 생성된 새 값으로 대체되며 규칙 세트의 다음 규칙으로 계속됩니다. 조건이 있는 경우 나열된 순서대로 처리됩니다. 다시 작성 엔진은 조건 패턴(CondPattern)을 테스트 문자열(TestString)과 일치시킵니다. 두 일치 조건이 있으면 사용 가능한 조건이 없을 때까지 다음 조건이 처리됩니다. 모든 조건이 일치하는 경우 URL은 규칙에 지정된 대체로 대체됩니다. 조건이 충족되지 않으면 전체 조건 세트와 해당 규칙이 실패합니다.

텍스트 상자에 URL 규칙 크롤링을 입력한 다음 변경 내용 저장을 클릭합니다. &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다. 검색 규칙을 테스트하려면 &quot;다시 작성 규칙 테스트&quot; 텍스트 상자에 테스트 URL을 입력한 다음 테스트를 클릭합니다.

## RewriteRule 지시문 {#section_669445C505754E838E14029D6583D9B6}

각 RewriteRule 지시문은 재작성 규칙 하나를 정의합니다. 규칙은 나열된 순서대로 적용됩니다. 다시 작성 규칙은 다음 양식을 사용합니다.

```
RewriteRule Pattern Substitution [Flags]
```

**패턴** 은 현재 제목에 적용되는 POSIX 일반 표현식입니다. &quot;현재 제목&quot;은 이전 규칙이 이미 일치하고 변경되었으므로 원래 제목과 다릅니다.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

&quot;not&quot; 문자(&#39;!&#39;)를 사용할 수 있습니다. 를 클릭하여 패턴에 접두사를 붙입니다. &quot;not&quot; 문자는 현재 제목이 패턴과 일치하지 않는 경우에만 패턴을 무효화할 수 있습니다. &quot;not&quot; 문자는 네거티브 패턴과 일치시키는 것이 낫거나 최종 기본 규칙으로 사용할 수 있습니다. 참고:&quot;not&quot; 문자와 그룹화된 와일드카드를 모두 패턴에 사용할 수 없습니다. 또한 대체 문자열에 $N이 들어 있을 때는 무효화된 패턴을 사용할 수 없습니다.

괄호를 사용하여 대체 및 CondPattern에서 참조할 수 있는 역참조를 만들 수 있습니다.

**대체** 제목대체 문자열로 대체됩니다. 문자열에는 다음이 포함될 수 있습니다.

일반 텍스트 - 변경되지 않고 전달되는 텍스트입니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음은 두 가지 유형의 역참조입니다.

* 다시 작성 규칙 배경 참조

   이러한 일치 백참조는 해당 RewriteRule 패턴에 있고 $N(0 &lt;= N &lt;= 9) 형태를 사용합니다. 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* 다시 쓰기 컨텍스트 배경 참조

   마지막으로 일치한 RewriteCond Pattern에 있는 이러한 일치 백참조와 %N(0 &lt;= N &lt;= 9) 형식을 사용합니다.

변수 이 변수들은 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수의 이름에 대한 문자열일 수 있습니다. 환경 변수 설정에 대한 자세한 내용은 `[E]` 플래그를 참조하십시오.

함수 ${NAME_OF_FUNCTION 형식의 함수입니다.key} 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.

>[!NOTE]
>
>특별한 대체 문자열이 있습니다.&#39;-&#39;는 &quot;대체 금지&quot;를 의미합니다. &#39;-&#39; 문자열은 종종 C(체인) 플래그에 유용하므로 대체가 발생하기 전에 제목을 여러 패턴에 일치시킬 수 있습니다.

**플래그** (선택 사항)

플래그는 대괄호 `[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>마지막 규칙. </p> <p> 다시 작성 프로세스를 중지하고 추가 재작성 규칙을 적용하지 않습니다. 현재 제목에 대한 추가 처리를 방지하려면 이 플래그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>다음 라운드. </p> <p> 원래 제목이 아니라 마지막 재작성 규칙의 제목을 사용하여 재작성 프로세스를 다시 실행합니다(첫 번째 재작성 규칙으로 다시 시작). 막다른 고리를 만들지 않도록 주의해라. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>다음 규칙과 연계됩니다. </p> <p>현재 규칙을 다음 규칙에 연결(다음 규칙에 연결할 수도 있음 등). 규칙이 일치하면 대체 프로세스가 평소대로 계속됩니다. 규칙이 일치하지 않으면 후속 연쇄 규칙을 모두 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p>패턴이 현재 제목과 일치할 때 패턴은 대/소문자를 구분하지 않습니다(즉, 'A-Z'와 'a-z' 사이에는 아무런 차이가 없습니다). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '건너뛰기|S=num' </p> </td> 
   <td colname="col2"> <p>다음 규칙 또는 규칙을 건너뜁니다. </p> <p> 현재 규칙이 일치하면 이 플래그는 규칙 세트의 다음 num 규칙을 생략하도록 다시 작성 엔진을 강제 적용합니다. 의사 if-then-else 구문을 만들려면 이 구문을 사용합니다. then 절의 마지막 규칙은 skip=N이 되며 여기서 N은 else-절의 규칙 수입니다. (참고:'chain|C' 플래그와 같지 않습니다!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>환경 변수를 설정합니다. </p> <p> 값 VAL에 설정된 환경 변수 "VAR"를 만듭니다. 여기서 VAL은 확장되는 정규 표현식 역참조, $N 및 %N을 포함할 수 있습니다. 이 플래그를 두 번 이상 사용하여 여러 변수를 설정할 수 있습니다. 이 변수는 나중에 %{VAR}을(를) 통해 다음 RewriteCond 패턴에서 참조할 수 있습니다. 이 플래그를 사용하여 제목에서 정보를 제거하고 기억하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCond 지시문(선택 사항) {#section_D664B71DE3884E0790531804C49A3222}

RewriteCond 지시문은 규칙 조건을 정의합니다. RewriteCond가 RewriteRule 앞에 있으면 해당 패턴이 현재 제목과 일치하고 추가 조건이 적용되는 경우에만 규칙이 사용됩니다.

다시 작성 조건 지시문은 다음 양식을 사용합니다.

```
RewriteCond TestString CondPattern [Flags] 
```

**** TestStrings는 다음 구문을 포함할 수 있는 문자열입니다.

일반 텍스트 - 변경되지 않고 전달되는 텍스트입니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음과 같은 두 가지 유형의 역참조가 있습니다.

* RewriteRule Backreferences 해당 RewriteRule 패턴에 있는 이러한 일치 백참조를 사용하고 $N(0 &lt;= N &lt;= 9) 양식을 사용합니다. 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RewriteCond 역참조 마지막 일치 RewriteCondPattern에서 이러한 일치 역참조를 사용하여 %N(0 &lt;= N &lt;= 9) 양식을 만듭니다.

변수 이 변수들은 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수의 이름에 대한 문자열일 수 있습니다. 환경 변수 설정에 대한 자세한 내용은 `[E]` 플래그를 참조하십시오.

함수 ${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 키의 모든 문자를 인코딩합니다.
* &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않고 그대로 남아 있고, 공백은 &#39;+&#39;로 변환되며 다른 모든 문자는 %xx URL 인코딩된 상응하는 것으로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL 인코딩 문자가 다시 단일 문자로 변환됩니다.

**일부** 추가가 있는 표준 확장 일반 표현식을 ContextPatterns로 변환합니다. 패턴 문자열에 &#39;!&#39; 접두사를 추가할 수 있습니다. 문자(느낌표)를 사용하여 일치하지 않는 패턴을 지정합니다. 실제 정규 표현식 문자열 대신 다음 특수 변형 중 하나를 사용할 수 있습니다.

>[!NOTE]
>
>이러한 모든 테스트에 느낌표(&#39;!&#39;)를 접두사로 지정할 수 있습니다. 그들의 의미를 무효화하다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘력이 부족합니다. </p> <p><i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 작으면 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>보다 사전적으로 탁월합니다. </p> <p><i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 큰 경우 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> 사전적으로 동등합니다. </p> <p><i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>과(와) 완전히 같은 경우 즉, 두 문자열이 정확히 동일한(문자별) 경우 true입니다. <i>CondPattern</i>이 ""(두 개의 따옴표)일 경우 이 값은 <i>TestString</i>을 빈 문자열에 비교합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**플래그** (선택 사항)

플래그는 대괄호 `[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p> 테스트를 민감하지 않게 합니다. 즉, 확장된 <i>TestString</i>과 <i>CondPattern에서 'A-Z'와 'a-z'는 모두 아무런 차이가 없습니다.</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> 또는 다음 조건. </p> <p>이 플래그를 사용하여 규칙 조건을 암시적 AND 대신 로컬 OR과 결합합니다. 이 플래그를 사용하지 않으면 콘드/규칙을 여러 번 작성해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

표준 제목 형식의 회사 웹 사이트가 있다고 가정합니다.&quot;내 회사&quot; 뒤에 하이픈(&quot;내 회사 - 환영&quot; 또는 &quot;내 회사 - 뉴스&quot; 등의 페이지 관련 설명)이 옵니다. 사이트를 인덱싱할 때 제목에서 &quot;내 회사 -&quot;를 제거하고 전체 제목을 대문자로 변환하려는 경우

다음 다시 작성 규칙은 함수 터퍼를 사용하여 제목의 설명형 부분만 대문자로 다시 작성합니다.

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

규칙의 패턴 `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))`에는 &quot;내 회사-&quot; 다음에 나오는 제목 내용과 일치하는 역참조 `(.*)`이 포함되어 있습니다. ( )가 있는 패턴의 일부를 둘러싸면 대체에 의해 참조할 수 있는 역참조가 만들어집니다. 이 예제에서 대체(${toupper:**$1**})는 터치 함수를 사용하여 역참조(**$1**)를 다시 씁니다.

따라서 &quot;My Company - Welcome&quot; 형식의 제목은 &quot;WELCOME&quot;으로 다시 작성됩니다.

**감사의 말**

다시 작성 엔진 소프트웨어는 Apache Group에서 Apache HTTP 서버 프로젝트(https://www.apache.org/)에 사용하기 위해 개발했습니다.

## 크롤링 제목 규칙 추가 중 {#task_272BB4C603BA4C9ABDBEEB398798B101}

크롤링 제목 규칙을 추가하여 웹 콘텐츠 내에서 발견된 제목이 검색 인덱스에 저장되기 전에 어떻게 재작성되는지 지정할 수 있습니다.

<!-- 

t_adding_crawl_title_rules.xml

 -->

**크롤링 제목 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl Title Rules]**&#x200B;를 클릭합니다.
1. [!DNL Crawl Title Rules] 필드에 원하는 규칙을 입력합니다.

   &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.
1. (선택 사항) [!DNL Crawl Title Rules] 페이지의 [!DNL Test Crawl Title Rules] 필드에 테스트할 검색 규칙의 테스트 URL을 입력한 다음 **테스트**&#x200B;를 클릭합니다.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL Crawl Title Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 검색 URL 규칙 정보 {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

URL 검색 규칙은 웹 사이트 검색 결과의 URL이 표시되는 방식을 지정합니다. 규칙은 전체 URL에서 작동합니다. 세션 ID 정보가 자주 저장되는 쿼리 인수 등 URL의 모든 부분을 조작할 수 있습니다.

<!-- 

c_about_search_url_rules.xml

 -->

일반적으로 검색 URL 규칙은 URL에 세션 ID를 삽입하는 데 사용됩니다. 그러나 검색 URL 규칙을 사용하여 결과와 함께 표시되는 도메인 이름을 변경할 수도 있습니다. 기본적으로 규칙은 지정되지 않으며 URL 수정이 수행되지 않습니다.

검색 URL 규칙은 다음 두 가지 기본 요소로 구성될 수 있습니다.RewriteRule 및 선택적 RewriteCode를 반환합니다. 검색 결과의 일부로 URL이 포함되면 규칙을 조작하는 데 사용됩니다. 검색 URL 규칙 및 조건을 무제한으로 지정할 수 있습니다. 규칙 세트는 규칙별로 반복되므로 이러한 규칙의 순서가 중요합니다. 규칙이 일치하면 소프트웨어는 해당하는 다시 작성 조건을 모두 반복합니다(선택 사항). 크롤링 URL 규칙은 다음과 같은 방식으로 지정됩니다.

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

URL을 처리할 때 사이트 검색/머천다이징은 이를 각 검색 규칙의 패턴과 일치시킵니다. 일치가 실패할 경우 다시 작성 엔진은 규칙 처리를 즉시 중지하고 세트에서 다음 규칙을 계속 진행합니다. 패턴이 일치하면 다시 작성 엔진은 해당 RewriteCond 지침을 찾습니다. 조건이 없으면 URL은 새 값으로 대체됩니다. 이 값은 대체 문자열에서 생성되며 규칙 세트의 다음 규칙으로 계속됩니다. 조건이 있는 경우 이러한 조건이 나열되는 순서는 처리 방법입니다. 다시 작성 엔진은 조건 패턴(CondPattern)을 테스트 문자열(TestString)과 일치시킵니다. 두 일치 조건이 있으면 사용 가능한 조건이 없을 때까지 다음 조건이 처리됩니다. 모든 조건이 일치하는 경우 URL은 규칙에 지정된 대체로 대체됩니다. 조건이 충족되지 않으면 전체 조건 세트와 해당 규칙이 실패합니다.

## RewriteRule 지시문 정보 {#section_A3473B5B90B74DA1970213113A90591E}

다시 작성 규칙은 다음 양식을 사용합니다.

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**패턴** 은 현재 URL에 적용되는 POSIX 일반 표현식입니다. &quot;현재 URL&quot;은 이전 규칙이 이미 일치하여 변경되었을 수 있으므로 원래 URL과 다를 수 있습니다.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

&quot;not&quot; 문자(&#39;!&#39;)를 사용할 수 있습니다. 를 클릭하여 패턴에 접두사를 붙입니다. &quot;not&quot; 문자를 사용하면 패턴을 무효화할 수 있습니다. 즉, 현재 URL이 패턴과 일치하지 않는 경우에만 적용됩니다. 네거티브 패턴과 일치시키는 것이 좋거나 최종 기본 규칙으로 &quot;not&quot; 문자를 사용할 수 있습니다. &quot;not&quot; 문자와 그룹화된 와일드카드를 모두 패턴에 사용할 수 없습니다. 또한 대체 문자열에 $N이 들어 있을 때는 무효화된 패턴을 사용할 수 없습니다.

괄호를 사용하여 대체 및 CondPattern에서 참조할 수 있는 역참조를 만들 수 있습니다.

**대체** URL은 다음을 포함할 수 있는 대체 문자열로 완전히 대체됩니다.

일반 텍스트 - 변경되지 않고 통과하는 텍스트입니다.

백참조패턴 또는 CondPattern의 그룹화된 부품(괄호 안)에 대한 액세스를 제공합니다. 다음과 같은 두 가지 유형의 역참조가 있습니다.

RewriteRule Backreferences 해당 RewriteRule 패턴에 있는 이러한 일치 백참조를 사용하고 $N(0 &lt;= N &lt;= 9) 양식을 사용합니다. 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RewriteCond Backreferences - 마지막으로 일치한 RewriteCondPattern에서 이러한 일치 역참조를 사용하여 %N(0 &lt;= N &lt;= 9) 양식을 만듭니다.

함수:${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 *key*&#x200B;의 모든 문자를 인코딩합니다.
* &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않았습니다.공백은 &#39;+&#39;;(으)로 변환됩니다.다른 모든 문자는 %xx URL 인코딩된 동등한 문자로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL 인코딩 문자가 다시 단일 문자로 변환됩니다.

>[!NOTE]
>
>특별한 대체 문자열이 있습니다.&#39;-&#39;는 &quot;대체 금지&quot;를 의미합니다. &#39;-&#39; 문자열은 종종 C(체인) 플래그와 함께 유용합니다. 대체가 발생하기 전에 URL을 여러 패턴과 일치시킬 수 있습니다.

**플래그** (선택 사항)

플래그는 대괄호 `[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>마지막 규칙. </p> <p> 재작성 프로세스를 중지하고 추가 재작성 규칙을 적용하지 않습니다. 현재 URL에 대한 추가 처리를 방지하려면 이 플래그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p> 다음 라운드. </p> <p>마지막 재작성 규칙의 URL(원본 URL이 아님)을 사용하여 재작성 프로세스를 다시 실행합니다(첫 번째 재작성 규칙으로 다시 시작). 죽은 루프를 만들지 않도록 주의하세요! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> 다음 규칙과 연계됩니다. </p> <p>이 플래그는 현재 규칙을 다음 규칙에 연결할 수 있고, 이 규칙을 다음 규칙에 연결할 수도 있습니다. 규칙이 일치하면 대체 프로세스가 평소대로 계속됩니다. 규칙이 일치하지 않으면 후속 연쇄 규칙을 모두 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p>이 플래그는 패턴 대/소문자를 구분하지 않습니다. 즉, 패턴이 현재 URL에 대해 일치하면 'A-Z'와 'a-z'는 아무런 차이가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '건너뛰기|S=num' </p> </td> 
   <td colname="col2"> <p>다음 규칙 또는 규칙을 건너뜁니다. </p> <p> 현재 규칙이 일치하면 이 플래그는 규칙 세트의 다음 num 규칙을 생략하도록 다시 작성 엔진을 강제 적용합니다. 의사 if-then-else 구문을 만들려면 이 구문을 사용합니다. then 절의 마지막 규칙은 skip=N이 되며 여기서 N은 else-절의 규칙 수입니다. (참고:'chain|C' 플래그와 같지 않습니다!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>환경 변수를 설정합니다. </p> <p> 이 플래그는 VAL 값으로 설정된 환경 변수 "VAR"를 만듭니다. VAL에는 확장되는 정규 표현식 역참조, $N 및 %N이 포함될 수 있습니다. 이 플래그를 두 번 이상 사용하여 여러 변수를 설정할 수 있습니다. 이 변수는 %{VAR}을(를) 통해 다음 RewriteCond 패턴에서 나중에 참조되지 않을 수 있습니다. 이 플래그를 사용하여 URL의 정보를 제거하고 기억하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

저장소 다시 작성 규칙 및 다시 작성 규칙 검색은 변수 값을 공유합니다. 이로 인해 포함된 URL이 발견되어 저장될 때 변수를 시간 구분 세션 id 값으로 설정할 수 있습니다. 임시 저장소 목록에서 다음 URL을 검색할 때 해당 페이지를 검색하기 전에 최신 세션 ID 값을 추가할 수 있습니다.

**예**

대/소문자를 구분하는 서버가 있다고 가정합니다. 문자열 &quot;www.mydomain.com&quot; 및 &quot;www.MyDomain.com&quot;을 다르게 처리합니다. 서버가 올바르게 작동하도록 하려면 &quot;www.MyDomain.com&quot;을 참조하는 링크가 일부 문서에 포함되어 있더라도 도메인이 항상 &quot;www.mydomain.com&quot;이어야 합니다. 이렇게 하려면 다음 규칙을 사용할 수 있습니다.

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

이 다시 작성 규칙은 &quot;trolower&quot; 함수를 사용하여 URL의 도메인 부분을 다시 작성하여 항상 소문자가 되도록 합니다.

1. 패턴 `(^https://([^/]*)(.*)$)`에는 URL의 &quot;https://&quot;과 첫 번째 &quot;/&quot; 사이의 모든 문자와 일치하는 역참조 **`([^/]*)`**&#x200B;이 포함되어 있습니다. 패턴에는 두 번째 역참조 **()도 포함되어 있습니다.*)** URL의 나머지 모든 문자와 일치하는 모든 문자를 찾습니다.

1. 대체 `(https://${tolower:$1}$2)`은 첫 번째 역참조 `(https://**${tolower:$1**}$2)`에 **Tolower** 함수를 사용하여 URL을 다시 작성하도록 검색 엔진에 지시하며 나머지 URL은 그대로 남습니다 `(https://${tolower:$1}*$2*)`.

따라서 `https://www.MyDomain.com/INTRO/index.Html` 형식의 URL이 `https://www.mydomain.com/INTRO/index.Html`(으)로 다시 작성되었습니다.

**RewriteCond 지시문** (선택 사항)

RewriteCond 지시문은 규칙 조건을 정의합니다. RewriteCond가 RewriteRule 앞에 있으면 해당 패턴이 현재 제목과 일치하고 추가 조건이 적용되는 경우에만 규칙이 사용됩니다.

다시 작성 조건 지시문은 다음 양식을 사용합니다.

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

** TestStrings는 다음 구문을 포함할 수 있는 문자열입니다.

일반 텍스트:전달된 텍스트는 변경되지 않고 그대로 유지됩니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음과 같은 두 가지 유형의 역참조가 있습니다.

* ** RewriteRule Backreferences** 해당 RewriteRule 패턴에 있는 이러한 일치 백참조와 $N(0 &lt;= N &lt;= 9) 형식을 사용합니다. 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** Backreferences마지막으로 일치한 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0) 형식을 사용합니다.  &lt;>

변수 이 변수들은 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수의 이름에 대한 문자열일 수 있습니다. 변수 설정에 대한 자세한 내용은 RewriteRule *`[E]`* 플래그를 참조하십시오.

>[!NOTE]
>
>다시 작성 규칙은 일반적으로 변수를 사용합니다. 현재 URL의 모든 CGI 매개 변수는 자동으로 변수로 만들어집니다. 예를 들어 검색 URL `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"`은(는) 자동으로 4개의 변수를 제공하며 이 변수는 다시 작성 규칙에서 참조할 수 있습니다. 이 예제에서 한 변수는 &quot;session&quot;이고 그 값은 &quot;1234&quot;이고 다른 변수는 &quot;id&quot;라고 하며, 그 값은 &quot;5678&quot;입니다. 다른 두 변수는 `sp_a` 및 `sp_q`입니다. 모든 필요한 변수를 웹 페이지의 검색 양식에서 숨김 필드로 전달해야 합니다. 이 예에서는 검색을 수행하는 웹 사이트 사용자를 식별하는 &quot;session&quot; 및 &quot;id&quot; 값을 전달해야 합니다. 검색 양식에 숨김 필드를 전달하려면 `<input type=hidden name="session" value="1234">` 같은 태그를 사용합니다.

함수 ${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 *key*&#x200B;의 모든 문자를 인코딩합니다. &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않고 그대로 남아 있고, 공백은 &#39;+&#39;로 변환되며 다른 모든 문자는 %xx URL 인코딩된 상응하는 것으로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL은 문자를 다시 단일 문자로 인코딩합니다.

**일부** 추가가 있는 표준 확장 일반 표현식을 ContextPatterns로 변환합니다. 패턴 문자열에 &#39;!&#39; 접두사를 추가할 수 있습니다. 문자(느낌표)를 사용하여 일치하지 않는 패턴을 지정합니다. 실제 정규 표현식 문자열 대신 다음 특수 변형 중 하나를 사용할 수 있습니다.

느낌표(&#39;!&#39;)를 사용하여 이러한 모든 테스트에 접두사를 지정할 수 있습니다. 그들의 의미를 무효화하다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘력이 부족합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 작으면 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>보다 사전적으로 탁월합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 큰 경우 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>사전적으로 동등합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>과(와) 사전적으로 같으면 true입니다. 즉, 두 문자열은 정확하게 동일합니다(문자별 문자). <i>CondPattern</i>이 ""(두 개의 따옴표)일 경우 이 값은 <i>TestString</i>을 빈 문자열에 비교합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**플래그** (선택 사항)

플래그는 대괄호 `[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

&#39;nocase|NC&#39;(대/소문자 없음):이렇게 하면 테스트 대/소문자를 구분하지 않습니다. 즉, 확장된 *TestString*&#x200B;과 *CondPattern*&#x200B;에서 &#39;A-Z&#39;와 &#39;a-z&#39;는 모두 아무런 차이가 없습니다.

&#39;ornext|OR&#39;(또는 다음 조건):규칙 조건을 암시적 AND 대신 로컬 OR과 결합하는 데 사용합니다. 이 플래그가 없으면 컨텍스트/규칙을 여러 번 작성해야 합니다.

**예**

일부 웹 페이지는 고객이 처음으로 사이트에 도착할 때 &quot;sessionid&quot; CGI 변수를 할당합니다. 이 변수는 고객을 식별하는 데 사용되며, 고객이 사이트를 탐색할 때 변수가 전달됩니다. 검색 로봇은 고객의 모습과 비슷하므로 &quot;sessionid&quot; 번호가 할당됩니다. 검색 로봇은 두 번째 사이트 페이지에서 새 값을 할당하려고 해도 이 단일 &quot;sessionid&quot; 값을 유지합니다. 이를 위해 다음 다시 작성 규칙이 필요합니다.

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

RewriteRule 패턴에는 다음 두 가지 역참조가 포함되어 있습니다.(.)+) 및 (.*)를 참조하십시오. 첫 번째 역참조는 &quot;sessionid=&quot; 앞에 있는 모든 문자와 일치합니다. 두 번째 역참조는 세션 id의 종료 &#39;&amp;&#39; 또는 &#39;#&#39; 뒤에 오는 모든 문자와 일치합니다.

대체 패턴은 첫 번째 역참조를 사용하여 URL을 다시 쓰고, 그 다음에 &quot;sessionid=&quot; 문자열을 반환하고, URL에서 CGI 매개 변수로 전달된 세션 ID 변수의 값을 뒤에 두 번째 역참조를 사용하여 다시 기록합니다.`($1sessionid=%{sessionid}$2)`.

**RewriteCond**&#x200B;은 변수 세션 id `(%{sessionid})`를 조사합니다. 하나 이상의 문자(.)가 포함된 경우+), RewriteRule이 일치합니다.

따라서 검색 쿼리가 `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`인 경우 검색 로봇이 사이트를 크롤하여 링크를 저장할 때 발생한 &quot;sessionid&quot; 값 대신 &quot;sessionid&quot; 값이 &quot;5678&quot;되도록 모든 검색 결과 URL이 다시 작성됩니다.

**감사의 말**

다시 작성 엔진 소프트웨어는 Apache Group에서 Apache HTTP 서버 프로젝트(https://www.apache.org/)에 사용하기 위해 개발했습니다.

## 검색 URL 규칙 {#task_50C77D1B53804AEEB20896F74265BD6F} 추가

검색 URL 규칙을 추가하여 웹 사이트 검색 결과의 URL이 표시되는 방식을 지정할 수 있습니다. 규칙은 전체 URL에서 작동합니다. 세션 ID 정보가 자주 보관되는 쿼리 인수를 비롯하여 URL의 모든 부분을 조작할 수 있습니다.

<!-- 

t_adding_search_url_rules.xml

 -->

**검색 URL 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search URL Rules]**&#x200B;를 클릭합니다.
1. [!DNL Search URL Rules] 필드에 원하는 규칙을 입력합니다.

   &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.
1. (선택 사항) [!DNL Search URL Rules] 페이지의 [!DNL Test Search URL Rules] 필드에 테스트할 크롤링 규칙이 있는 테스트 URL을 입력한 다음 **테스트**&#x200B;를 클릭합니다.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL Search URL Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 검색 제목 규칙 정보 {#concept_C72D20F8DFF64EDE809AF4B72797E858}

검색 제목 규칙은 웹 사이트 검색 결과의 제목이 표시되는 방식을 지정합니다. 제목의 모든 부분은 조작될 수 있습니다.

<!-- 

c_about_search_title_rules.xml

 -->

예를 들어 다시 작성 규칙을 사용하여 조직 이름과 같이 제목의 일부를 제거할 수 있습니다. 기본적으로 사이트 검색/머천다이징에는 제목 규칙이 없으며 제목을 수정하지 않습니다.

제목 규칙은 다음 두 가지 기본 요소로 구성할 수 있습니다.다시 작성 규칙 및 선택적 다시 쓰기 컨텍스트 규칙 및 조건 수를 제한 없이 지정할 수 있습니다. 규칙 세트는 규칙별로 반복되므로 이러한 규칙의 순서가 중요합니다. 규칙이 일치하면 소프트웨어는 해당하는 다시 작성 조건을 모두 반복합니다(선택 사항). 검색 제목 규칙은 다음과 같은 방식으로 지정됩니다.

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

제목이 발견되면 사이트 검색/머천다이징이 각 크롤링 규칙의 패턴과 일치시킵니다. 패턴이 일치하면 다시 작성 엔진은 해당 RewriteCond 지시문을 찾습니다. 조건이 없는 경우 제목은 대체 문자열에서 생성된 새 값으로 대체되고 규칙 세트의 다음 규칙으로 계속됩니다. 조건이 있는 경우 나열된 순서대로 처리됩니다. 다시 작성 엔진은 조건 패턴(CondPattern)을 테스트 문자열(TestString)과 일치시킵니다. 두 일치 조건이 있으면 사용 가능한 조건이 없을 때까지 다음 조건이 처리됩니다. 모든 조건이 일치하는 경우 URL은 규칙에 지정된 대체로 대체됩니다. 조건이 충족되지 않으면 전체 조건 세트와 해당 규칙이 실패합니다.

## 다시 작성 규칙 지시문 {#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

각 RewriteRule 지시문은 재작성 규칙 하나를 정의합니다. 규칙은 나열된 순서대로 적용됩니다. 다시 작성 규칙은 다음 양식을 사용합니다.

```
RewriteRule Pattern Substitution [Flags]
```

**패턴** 현재 제목에 적용되는 POSIX 정규 표현식입니다. &quot;현재 제목&quot;은 이전 규칙이 이미 일치하여 변경되었을 수 있으므로 원래 제목과 다를 수 있습니다.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

&quot;not&quot; 문자(&#39;!&#39;)를 사용할 수 있습니다. 를 클릭하여 패턴에 접두사를 붙입니다. &quot;not&quot; 문자를 사용하면 패턴을 무효화할 수 있습니다. 즉, 현재 제목이 패턴과 일치하지 않는 경우에만 true입니다. &quot;not&quot; 문자는 네거티브 패턴과 일치시키는 것이 낫거나 최종 기본 규칙으로 사용할 수 있습니다. 참고:&quot;not&quot; 문자와 그룹화된 와일드카드를 모두 패턴에 사용할 수 없습니다. 또한 대체 문자열에 $N이 들어 있을 때는 무효화된 패턴을 사용할 수 없습니다.

괄호를 사용하여 대체 및 CondPattern에서 참조할 수 있는 역참조를 만들 수 있습니다.

**대체** 제목이 다음 내용을 포함할 수 있는 대체 문자열로 완전히 대체됩니다.

일반 텍스트 - 변경되지 않고 전달되는 텍스트입니다.

**역참조** Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 대한 액세스를 제공합니다. 다음은 두 가지 유형의 역참조입니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** RewriteCond Backreferences** 마지막 일치 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0 &lt;= N &lt;= 9) 형식을 사용합니다.

**변수** 이 변수들은 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열일 수 있습니다. 환경 변수 설정에 대한 자세한 내용은 [E] 플래그를 참조하십시오. 검색 결과를 생성한 검색 양식에서 변수를 정의할 수도 있습니다.

**함수** 이 함수는 ${NAME_OF_FUNCTION 형식의 함수입니다.key} 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.

특별한 대체 문자열이 있습니다.&#39;-&#39;는 &quot;대체 금지&quot;를 의미합니다. &#39;-&#39; 문자열은 종종 C(체인) 플래그와 함께 유용하므로 대체가 발생하기 전에 제목을 여러 패턴에 일치시킬 수 있습니다.

**플래그** (선택 사항)

플래그는 대괄호 `[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> 마지막 규칙. </p> <p> 재작성 프로세스를 중지하고 추가 재작성 규칙을 적용하지 않습니다. 현재 제목에 대한 추가 처리를 방지하려면 이 플래그를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>다음 라운드. </p> <p> 마지막 재작성 규칙의 제목을 사용하여(원래 제목이 아니라) 재작성 프로세스를 다시 실행합니다(첫 번째 재작성 규칙으로 다시 시작). 막다른 고리를 만들지 않도록 주의해라. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>다음 규칙과 연계됩니다. </p> <p> 이 플래그는 현재 규칙을 다음 규칙에 연결(다음 규칙에 연결할 수도 있음)합니다. 규칙이 일치하면 대체 프로세스가 평소대로 계속됩니다. 규칙이 일치하지 않으면 후속 연쇄 규칙을 모두 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nopcase|NC' </p> </td> 
   <td colname="col2"> <p> 아니요. </p> <p> 이 플래그는 패턴 대/소문자를 구분하지 않습니다. 즉, 패턴이 현재 제목과 일치하면 'A-Z'와 'a-z'는 아무런 차이가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '건너뛰기|S=num' </p> </td> 
   <td colname="col2"> <p> 다음 규칙 또는 규칙을 건너뜁니다. </p> <p> 현재 규칙이 일치하면 이 플래그는 규칙 세트의 다음 num 규칙을 생략하도록 다시 작성 엔진을 강제 적용합니다. 의사 if-then-else 구문을 만들려면 이 구문을 사용합니다. then 절의 마지막 규칙은 skip=N이 되며 여기서 N은 else-절의 규칙 수입니다. ('chain|C' 플래그와 동일하지 않습니다!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>환경 변수를 설정합니다. </p> <p> 이 플래그는 VAL 값에 환경 변수 "VAR"를 만듭니다. 여기서 VAL에는 정규 표현식 역참조, $N 및 %N이 포함될 수 있으며 이 값은 확장됩니다. 이 플래그를 두 번 이상 사용하여 여러 변수를 설정할 수 있습니다. 이 변수는 나중에 %{VAR}을(를) 통해 다음 RewriteCond 패턴에서 참조할 수 있습니다. 이 플래그를 사용하여 제목에서 정보를 제거하고 기억하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## RewriteCond 지시문(선택 사항) {#section_9D72B2AB454849A7B681BC39C506AAA3}

RewriteCond 지시문은 규칙 조건을 정의합니다. RewriteCond가 RewriteRule 앞에 있으면 해당 패턴이 현재 제목과 일치하고 추가 조건이 적용되는 경우에만 규칙이 사용됩니다.

다시 작성 조건 지시문은 다음 양식을 사용합니다.

```
RewriteCond TestString CondPattern [Flags]
```

**** TestStrings는 다음 구문을 포함할 수 있는 문자열입니다.

일반 텍스트 - 변경되지 않고 전달되는 텍스트입니다.

역참조를 사용하면 Pattern 또는 CondPattern의 그룹화된 부품(괄호 안)에 액세스할 수 있습니다. 다음과 같은 두 가지 유형의 역참조가 있습니다.

* **RewriteRule** Backreferences해당 RewriteRule 패턴에 있는 이 일치 역참조를 사용하고 $N(0) 형식을 사용합니다.  &lt;> 예, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** Backreferences마지막으로 일치한 RewriteCondPattern에 있는 이러한 일치 백참조와 %N(0) 형식을 사용합니다.  &lt;>

**변수** 이 변수들은 %{NAME_OF_VARIABLE} 형식의 변수입니다. 여기서 NAME_OF_VARIABLE은 정의된 변수 이름의 문자열일 수 있습니다. 환경 변수 설정에 대한 자세한 내용은 `[E]` 플래그를 참조하십시오. 검색 결과를 생성한 검색 양식에서 변수를 정의할 수도 있습니다.

**함수** 이 함수는 ${NAME_OF_FUNCTION:key} 형식의 함수입니다. 여기서 NAME_OF_FUNCTION은 다음과 같습니다.

* Tolower는 *key*&#x200B;소문자에서 모든 문자를 만듭니다.
* toupper는 *key*&#x200B;의 모든 문자를 대문자로 만듭니다.
* escape URL은 *key*&#x200B;의 모든 문자를 인코딩합니다.
* &#39;a&#39;..&#39;z&#39;, &#39;A&#39;.&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; 및 &#39;_&#39;는 변경되지 않고 그대로 남아 있고, 공백은 &#39;+&#39;로 변환되며 다른 모든 문자는 %xx URL 인코딩된 상응하는 것으로 변환됩니다.
* escape를 취소하면 &#39;+&#39;가 다시 공백으로 변환되고 모든 %xx URL 인코딩 문자가 다시 단일 문자로 변환됩니다.

특별한 대체 문자열이 있습니다.&#39;-&#39;는 &quot;대체 금지&quot;를 의미합니다. &#39;-&#39; 문자열은 종종 C(chain) 플래그와 함께 유용하므로 대체가 발생하기 전에 여러 패턴에 URL을 일치시킬 수 있습니다.

**CondPattern** 일부 추가 항목이 있는 표준 확장 일반 표현식입니다. 패턴 문자열에 &#39;!&#39; 접두사를 추가할 수 있습니다. 문자(느낌표)를 사용하여 일치하지 않는 패턴을 지정합니다. 실제 정규 표현식 문자열 대신 다음 특수 변형 중 하나를 사용할 수 있습니다.

이러한 모든 테스트는 느낌표(&#39;!&#39;)로 접두사를 추가할 수도 있습니다. 그들의 의미를 무효화하다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CondPattern 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>어휘력이 부족합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 작으면 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> 보다 사전적으로 탁월합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>보다 사전적으로 큰 경우 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>사전적으로 동등합니다. </p> <p> <i>CondPattern</i>을 일반 문자열로 취급하여 <i>TestString</i>과 사전적으로 비교합니다. <i>TestString</i>이 <i>CondPattern</i>과(와) 사전적으로 같으면 true입니다. 즉, 두 문자열은 정확하게 동일합니다(문자별 문자). <i>CondPattern</i>이 ""(두 개의 따옴표)일 경우 이 값은 <i>TestString</i>을 빈 문자열에 비교합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**플래그** (선택 사항)

플래그는 대괄호`[]`로 묶이고 여러 개의 플래그는 쉼표로 구분됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>플래그 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC'(대/소문자 없음) </p> </td> 
   <td colname="col2"> <p>테스트를 민감하지 않게 합니다. 즉, 확장된 <i>TestString</i>과 <i>CondPattern</i>에서 'A-Z'와 'a-z'는 모두 아무런 차이가 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR'(또는 다음 조건) </p> </td> 
   <td colname="col2"> <p> 규칙 조건을 암시적 AND 대신 로컬 OR과 결합하는 데 사용합니다. 이 플래그가 없으면 컨텍스트/규칙을 여러 번 작성해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section_E7454FFE169E459AABD9D033651939CB}

표준 제목 형식의 회사 웹 사이트가 있다고 가정합니다.&quot;내 회사&quot; 뒤에 하이픈(&quot;내 회사 - 환영&quot; 또는 &quot;내 회사 - 뉴스&quot; 등의 페이지 관련 설명)이 옵니다. 제목에서 &quot;내 회사 -&quot;를 제거하고 사이트를 인덱싱할 때 전체 제목을 대문자로 변환하려는 경우

다음 다시 작성 규칙은 함수 터퍼를 사용하여 제목의 설명형 부분만 대문자로 다시 작성합니다.

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

규칙의 패턴 `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))`에는 &quot;내 회사-&quot; 다음에 나오는 제목 내용과 일치하는 역참조 **`(.*)`**&#x200B;이 포함되어 있습니다. ( )가 있는 패턴의 일부를 둘러싸면 대체에 의해 참조할 수 있는 역참조가 만들어집니다. 이 예제에서 대체(${toupper:**$1**})는 터치 함수를 사용하여 역참조(**$1**)를 다시 씁니다.

따라서 &quot;My Company - Welcome&quot; 형식의 제목은 &quot;WELCOME&quot;으로 다시 작성됩니다.

**감사의 말**

다시 작성 엔진 소프트웨어는 Apache Group에서 Apache HTTP 서버 프로젝트(https://www.apache.org/)에 사용하기 위해 개발했습니다.

## 검색 제목 규칙 추가 중 {#task_155CECB74BE3444384EDBBD04F41515E}

검색 제목 규칙을 추가하여 웹 사이트 검색 결과의 제목을 표시하는 방법을 지정할 수 있습니다. 제목 일부를 조작할 수 있습니다.

<!-- 

t_adding_search_title_rules.xml

 -->

**검색 제목 규칙을 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search Title Rules]**&#x200B;를 클릭합니다.
1. [!DNL Search Title Rules] 필드에 원하는 규칙을 입력합니다.

   &#39;#&#39;(해시) 문자로 시작하는 빈 줄과 주석 줄이 허용됩니다.
1. (선택 사항) [!DNL Search Title Rules] 페이지의 [!DNL Test Search Title Rules] 필드에 테스트 제목을 입력한 다음 **테스트**&#x200B;를 클릭합니다.
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL Search Title Rules] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

