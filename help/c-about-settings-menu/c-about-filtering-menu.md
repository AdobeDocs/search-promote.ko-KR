---
description: '[필터링] 메뉴를 사용하여 웹 문서를 인덱싱하기 전에 웹 문서의 내용을 변경하는 스크립트를 사용합니다.'
seo-description: '[필터링] 메뉴를 사용하여 웹 문서를 인덱싱하기 전에 웹 문서의 내용을 변경하는 스크립트를 사용합니다.'
seo-title: 필터링 메뉴 정보
solution: Target
subtopic: Filtering
title: 필터링 메뉴 정보
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '4026'
ht-degree: 1%

---


# 필터링 메뉴 {#about-the-filtering-menu} 정보

[필터링] 메뉴를 사용하여 웹 문서를 인덱싱하기 전에 웹 문서의 내용을 변경하는 스크립트를 사용합니다.

## 스크립트 필터링 정보 {#concept_E56B73D625854AB2A899EF2D56CFCB47}

웹 문서를 인덱싱하기 전에 [!DNL Filtering Script]을 사용하여 웹 문서의 내용을 변경할 수 있습니다.

HTML 태그를 삽입하고, 관련 없는 컨텐츠를 제거할 수 있으며, 문서의 URL, MIME 유형 및 기존 컨텐츠를 기반으로 새로운 HTML 메타데이터를 만들 수도 있습니다. 필터링 스크립트는 강력한 문자열 처리와 정규식 일치를 유연하게 제공하는 Perl 스크립트입니다. 초기화 스크립트, 종료 스크립트, URL 마스크 스크립트 및 테스트 URL이 있는 필터링 스크립트를 사용합니다.

필터링 스크립트는 웹 사이트에서 문서를 읽을 때마다 실행됩니다. 이 스크립트는 표준 필터로 실행되며 즉, STDIN에서 데이터를 읽고, 해당 데이터를 어떤 방식으로 변환하고 결과를 STDOUT에 씁니다. 필터링 스크립트를 사용하여 필터링 스크립트에서 인덱스 로그로 상태 메시지를 인쇄할 수 있습니다. 메시지를 STDERR로 인쇄하거나 `_search_debug_log()` 하위 루틴을 통해 인쇄할 수 있습니다.

스테이지 필터링 스크립트 페이지의 **[!UICONTROL Expert (diff)]** 모드에서 사용할 수 있는 일부 GNU 비교 옵션에는 다음이 포함됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU 비교 옵션 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> 공백 크기의 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> 빈 줄을 삽입하거나 삭제하는 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트 출력 형식을 사용하여 3줄의 컨텍스트를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수) 행을 표시하거나, 줄이 지정되지 않으면 3개의 컨텍스트 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> 대/소문자를 구분하지 않습니다.대소문자 등가 것으로 간주합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> 출력 결과를 에드 스크립트와 유사하지만 파일에 나타나는 순서대로 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> RCS 형식 디폴트를 출력합니다.각 명령이 영향을 받는 줄 수를 지정한다는 점을 제외하고 <span class="codeph"> -f </span>와 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 세 줄의 컨텍스트를 표시하는 통합 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수)을 표시하거나, 행이 지정되지 않으면 3개의 출력 형식을 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이러한 스크립트에서 로컬 변수, 전역 변수 또는 둘 다를 사용할 수 있습니다. 모든 전역 변수는 네임스페이스 &quot;main:::&quot;로 앞에 표시됩니다. 필터링 스크립트가 시작되면 해당 환경에 다음과 같은 표준 파일 핸들이 포함됩니다.

* STDIN - 없음(읽을 때 즉시 EOF 반환)
* STDOUT - 대체 HTML(데이터가 STDOUT에 인쇄되는 경우 원본 문서 대신 사용됩니다)
* STDERR - STDERR로 인쇄되는 데이터는 오류 메시지가 색인 로그에 인쇄됩니다.

또한 다음 예와 같이 `_search_debug_log()` 하위 루틴을 사용하여 인덱스 로그에 사용자 정의 메시지를 작성할 수 있습니다.

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

이러한 메시지는 `DEBUG` 단어와 함께 서문으로 표시되며 오류로 기록되지 않습니다.

다음은 필터링의 예입니다. 웹 페이지 `<title>` 필드는 회사 이름으로 시작하는 경우가 많습니다. 이 정보는 사이트 탐색 목적으로 유용하지만 검색 시 관련이 없습니다. 모든 MegaCorp 웹 페이지의 제목이 다음과 같은 공통 문자열로 시작하는 경우:

```
<title>MegaCorp -- meaningful title 
here</title>
```

각 문서 제목 시작 부분에서 &quot; `MegaCorp --`&quot;을 제거하고 필터링 스크립트로 처리된 각 문서를 계산해야 합니다. 이렇게 하려면 다음 스크립트를 사용할 수 있습니다.

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## 전역 변수 {#global-variables}

필터링 스크립트에서 다음 변수를 사용할 수 있습니다.

| 변수 | 설명 |
|--- |--- |
| `$main::search_crawl_type` | `$main::search_crawl_type` 값은 진행 중인 인덱스 작업의 유형을 나타냅니다.  사용되지 않는 양식:`$main::ws_crawl_type` 인덱스 작업 및 관련 값은 다음과 같습니다. <ul><li>전체 인덱스:수동 - `manual`</li><li>전체 인덱스:예약됨 - `auto`</li><li>전체 인덱스:원격 제어 - `CGI`</li><li>증분 색인:수동 - `manual-incremental`</li><li>증분 색인:예약됨 - `auto-incremental` </li><li>증분 색인:원격 제어 - `CGI-incremental`</li><li>스크립트 색인:수동 - `manual-indexlist.txt` </li><li>스크립트 색인:예약됨 - `auto-indexlist.txt`</li><li>스크립트 색인:원격 제어 - `CGI-indexlist.txt`</li><li>다시 생성 - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | 이 값은 현재 인덱스 작업에 대해 &quot;인덱스 캐시 지우기&quot; 인덱싱 옵션을 요청했는지 여부를 나타냅니다. &quot;인덱스 캐시 지우기&quot;가 요청되면 `$main::search_clear_cache` 값은 &quot; `1`&quot;입니다.  사용되지 않는 형식: `$main::ws_clear_cache` |
| `$main::search_fields` | 이 값에는 계정에 정의된 메타데이터 필드의 탭으로 구분된 목록이 포함되어 있습니다. 기본적으로 이 값은 다음과 같습니다.   `url title desc keys target body alt date charset language` 사용되지 않는 양식:`$main::ws_fields` |
| `$main::search_collections` | 이 값에는 계정에 정의된 컬렉션의 탭으로 구분된 목록이 포함되어 있습니다.  사용되지 않는 형식: `$main::ws_collections` |
| `$main::search_url` | 값은 문서의 정규화된 URL입니다.  사용되지 않는 형식: `$main::ws_url` |
| `$main::search_content_type` | 이 값은 http-equiv 메타 태그에서 가져온 문서의 컨텐츠 유형입니다. 일반적인 값은 &quot;text/html;charset=iso-8859-1&quot;  사용되지 않는 형식: `$main::ws_content_type` |
| `$main::search_content_class` | 값은 내용 유형 필드에서 파생된 문서의 내용 클래스입니다.  사용되지 않는 형식: `$main::ws_content_class` |
| `$main::search_syntax_check` | 이 값은 &quot;구문 확인&quot; 단추의 사용을 반영합니다. 클릭하면 값이 1(1);그렇지 않으면 값이 0(영)입니다.  사용되지 않는 형식: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | 웹 서버에서 제공하는 경우 이 값에는 문서의 마지막 수정 날짜의 Epoch 표현(1970년 1월 1일 이후 시간)이 포함됩니다.  Perl localtime() 라이브러리 호출을 사용하여 이 값의 형식을 지정할 수 있습니다. |

### 빠른 팁 {#section_89A5C16911744AF98E232DF608C6A1F5}

* 모든 전역 변수는 네임스페이스 &quot;main::&quot; 앞에 표시됩니다.`$main::doc_count = 0;`
* 모든 로컬 변수는 &quot;my&quot;로 선언됩니다.`my $i = 0;`
* 서브루틴은 초기화 스크립트에 정의됩니다. 다음과 같은 명시적 &quot;main::&quot; 네임스페이스가 필요하지 않습니다.`sub my_sub {` `...`

   `}`

* 파일을 변경하기 전에 `$main::search_content_type`을 테스트합니다. 테스트를 수행하면 SWF 파일 또는 PDF 파일과 같이 바이너리 파일을 함부로 변경하지 않아도 됩니다.

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`은 서버에서 제공하는 전체 내용 유형 헤더입니다. &quot;text/html&quot;과 같은 간단한 MIME 유형을 포함할 수도 있습니다. 또는 MIME 형식을 포함할 수 있으며 그 뒤에 &quot;text/html;&quot;과 같은 문서의 문자 집합 인코딩과 같은 다른 정보가 올 수 있습니다.charset=iso-8859-1&quot;
* HTML이 아닌 문서의 각 유형에 대해 `$main::search_content_type`은(는) 다양한 값을 사용할 수 있습니다. 스크립트에서 각 값에 대한 테스트는 번거롭게 됩니다. 예를 들어 일부 Word 문서에는 &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; 또는 &quot;application/x-msword&quot;의 컨텐츠 유형 값이 있습니다. 이러한 경우 `$main::search_content_class`은(는) 다음 값을 사용할 수 있습니다.

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* 이 예제에서 &quot;word&quot;에 대해 `$main::search_content_class`을 테스트하는 것은 가능한 3개의 내용 유형 값 중 하나와 일치합니다.
* 필터링 스크립트에서 STDOUT에 아무 것도 인쇄되지 않으면 문서가 다운로드된 것과 동일하게 사용됩니다. 즉, 문서의 아무 내용도 변경할 필요가 없으면 해당 문서의 STDIN을 STDOUT에 복사할 필요가 없습니다.
* 문서에서 모든 텍스트를 제거하려면 유효한 STDOUT 파일을 인쇄합니다. 예를 들어 HTML 문서에서 모든 텍스트를 완전히 제거하려면 다음을 수행합니다.`print "<html></html>";`

## 필터링 스크립트 {#task_0AB84FD1133F47F9AA069A79BEA13A22} 추가

필터링 스크립트는 웹 사이트에서 다운로드한 각 문서에 대해 실행되는 Perl 스크립트입니다.

초기화 스크립트, 종료 스크립트 및 URL 마스크 스크립트와 함께 필터링 스크립트를 사용합니다.

필터링 스크립트의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 작성해야 합니다.

스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)

**필터링 스크립트를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Filtering Script] 페이지의 [!DNL Test URL] 필드에 웹 사이트에 있는 문서의 URL을 입력합니다.

   원시 HTML 텍스트의 변경 사항을 보려면 테스트 옵션을 클릭합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL 테스트 필드 </p> </td> 
      <td colname="col2"> <p>웹 사이트에서 문서의 URL을 입력할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트 </p> </td> 
      <td colname="col2"> <p>필터링 스크립트 및 URL 마스크에 대해 URL을 테스트합니다. </p> <p>테스트 URL 문서가 다운로드되며, 이 문서는 필터링 스크립트에 대한 STDIN 입력으로 사용됩니다. 그런 다음 초기화, 필터링 및 종료 스크립트가 실행됩니다. 필터링 스크립트에서 STDOUT 출력이 있으면 해당 출력이 새 브라우저 창에 표시됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>테스트만 </p> </td> 
      <td colname="col2"> <p>스크립트 작업만 테스트합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>미리 보기 </p> </td> 
      <td colname="col2"> <p>페이지를 볼 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>전체 시각적 요소 </p> </td> 
      <td colname="col2"> <p>문서의 전과 후 테이블 전체 보기를 생성합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>짧은 시각적 요소 </p> </td> 
      <td colname="col2"> <p>전과 후 보기 사이의 차이만 표시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>전문가(비교) </p> </td> 
      <td colname="col2"> <p>제공된 명령줄 옵션을 사용하여 파일을 비교하는 데 사용되는 GNU diff 명령의 원시 출력을 표시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>스크립트 필터링 </p> </td> 
      <td colname="col2"> <p>제공된 필드에 필터링 스크립트를 붙여넣을 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>변경 내용 저장 </p> </td> 
      <td colname="col2"> <p>필터링 스크립트를 저장합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>구문 확인 </p> </td> 
      <td colname="col2"> <p>초기화, 필터링 및 종료 스크립트를 실행하여 스크립트에 대한 빠른 구문 검사를 수행할 수 있습니다. 스크립트를 업데이트하거나 저장하지 않습니다. </p> <p>모든 Perl 컴파일러 오류 및 경고와 모든 STDERR 출력이 인쇄됩니다. </p> <p>스크립트가 고객에게 표시되기 전에 사이트 색인을 다시 구성해야 합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **GNU diff 명령줄 옵션**

   스테이지 필터링 스크립트 페이지의 **[!UICONTROL Expert (diff)]** 모드에서 사용할 수 있는 일부 GNU 비교 옵션에는 다음이 포함됩니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>GNU diff 명령줄 옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> 공백 크기의 변경 사항을 무시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> 빈 줄을 삽입하거나 삭제하는 변경 사항을 무시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> 컨텍스트 출력 형식을 사용하여 3줄의 컨텍스트를 표시합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C 선  </span> </p> </td> 
      <td colname="col2"> <p> 컨텍스트의 선(정수) 행을 표시하거나, 줄이 지정되지 않으면 3개의 컨텍스트 출력 형식을 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> 대/소문자를 구분하지 않습니다.대소문자 등가 것으로 간주합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> 출력 결과를 에드 스크립트와 유사하지만 파일에 나타나는 순서대로 변경합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> RCS 형식 디폴트를 출력합니다.각 명령이 영향을 받는 줄 수를 지정한다는 점을 제외하고 <span class="codeph"> -f </span>와 같습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> 세 줄의 컨텍스트를 표시하는 통합 출력 형식을 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U 선  </span> </p> </td> 
      <td colname="col2"> <p> 컨텍스트의 선(정수)을 표시하거나, 행이 지정되지 않으면 3개의 출력 형식을 사용합니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 필터링 스크립트 및 URL 마스크에 대해 테스트하려면 **[!UICONTROL Test]**&#x200B;을 클릭합니다.

   **[!UICONTROL Test]**&#x200B;을 클릭해도 필터링 스크립트가 업데이트되고 저장되지 않습니다.
1. [!DNL Filtering Script] 필드에 스크립트를 붙여 넣습니다.
1. (선택 사항) 필터링, 초기화 및 종료 스크립트를 실행하여 스크립트에 대한 빠른 구문 검사를 수행하려면 **[!UICONTROL Check Syntax]**&#x200B;을 클릭합니다.

   **[!UICONTROL Check Syntax]** 은 스크립트를 업데이트 및 저장하지 않습니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Filtering Script] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 초기화 스크립트 정보 {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

웹 문서를 인덱싱하기 전에 [!DNL Initialization Script]을 사용하여 웹 문서의 내용을 변경할 수 있습니다.

HTML 태그를 삽입하고, 관련 없는 컨텐츠를 제거할 수 있으며, 문서의 URL, MIME 유형 및 기존 컨텐츠를 기반으로 새로운 HTML 메타데이터를 만들 수도 있습니다. 초기화 스크립트는 강력한 문자열 처리와 정규 표현식 일치의 유연성을 제공하는 Perl 스크립트입니다. 필터링 스크립트, 종료 스크립트, URL 마스크 스크립트 및 테스트 URL과 함께 초기화 스크립트를 사용합니다.

초기화 스크립트는 색인화가 시작되기 전에 한 번 실행됩니다. 이 스크립트를 사용하여 필터링 스크립트에서 사용하는 전역 변수 및 하위 루틴을 초기화합니다. 초기화 스크립트를 사용하여 필터링 스크립트에서 인덱스 로그로 상태 메시지를 인쇄할 수 있습니다. 메시지를 STDERR로 인쇄하거나 `_search_debug_log()` 하위 루틴을 통해 인쇄합니다.

스테이지 초기화 스크립트 페이지의 **[!UICONTROL Expert (diff)]** 모드에서 사용할 수 있는 일부 GNU 비교 옵션에는 다음이 포함됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU 비교 옵션 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> 공백 크기의 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> 빈 줄을 삽입하거나 삭제하는 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트 출력 형식을 사용하여 3줄의 컨텍스트를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수) 행을 표시하거나, 줄이 지정되지 않으면 3개의 컨텍스트 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> 대/소문자를 구분하지 않습니다.대소문자 등가 것으로 간주합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> 출력 결과를 에드 스크립트와 유사하지만 파일에 나타나는 순서대로 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> RCS 형식 디폴트를 출력합니다.각 명령이 영향을 받는 줄 수를 지정한다는 점을 제외하고 <span class="codeph"> -f </span>와 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 세 줄의 컨텍스트를 표시하는 통합 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수)을 표시하거나, 행이 지정되지 않으면 3개의 출력 형식을 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이러한 스크립트에서 로컬 변수, 전역 변수 또는 둘 다를 사용할 수 있습니다. 모든 전역 변수는 네임스페이스 &quot;main:::&quot;로 앞에 표시됩니다. 초기화 스크립트가 시작되면 해당 환경에 다음과 같은 표준 파일 핸들이 포함됩니다.

* STDIN - 없음(읽을 때 즉시 EOF 반환)
* STDOUT - 없음(데이터가 STDOUT에 인쇄되는 경우 무시됩니다.)
* STDERR - STDERR로 인쇄되는 데이터는 오류 메시지가 색인 로그에 인쇄됩니다.

또한 다음 예와 같이 `_search_debug_log()` 하위 루틴을 사용하여 인덱스 로그에 사용자 정의 메시지를 작성할 수 있습니다.

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

이러한 메시지는 `DEBUG` 단어와 함께 서문으로 표시되며 오류로 기록되지 않습니다.

초기화 스크립트의 예는 다음과 같습니다.

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

[전역 변수](#global-variables)를 참조하십시오.

### 빠른 팁 {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* 모든 전역 변수는 네임스페이스 &quot;main::&quot; 앞에 표시됩니다.`$main::doc_count = 0;`
* 모든 로컬 변수는 &quot;my&quot;로 선언됩니다.`my $i = 0;`
* 서브루틴은 초기화 스크립트에 정의됩니다. 다음과 같은 명시적 &quot;main::&quot; 네임스페이스가 필요하지 않습니다.`sub my_sub {` `...`

   `}`

* 파일을 변경하기 전에 `$main::search_content_type`을 테스트합니다. 테스트를 수행하면 SWF 파일 또는 PDF 파일과 같이 바이너리 파일을 함부로 변경하지 않아도 됩니다.

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`은 서버에서 제공하는 전체 내용 유형 헤더입니다. &quot;text/html&quot;과 같은 간단한 MIME 유형을 포함할 수도 있습니다. 또는 MIME 형식을 포함할 수 있으며 그 뒤에 &quot;text/html;&quot;과 같은 문서의 문자 집합 인코딩과 같은 다른 정보가 올 수 있습니다.charset=iso-8859-1&quot;
* HTML이 아닌 문서의 각 유형에 대해 `$main::search_content_type`은(는) 다양한 값을 사용할 수 있습니다. 스크립트에서 각 값에 대한 테스트는 번거롭게 됩니다. 예를 들어 일부 Word 문서에는 &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; 또는 &quot;application/x-msword&quot;의 컨텐츠 유형 값이 있습니다. 이러한 경우 `$main::search_content_class`은(는) 다음 값을 사용할 수 있습니다.

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * 텍스트

* 이 예제에서 &quot;word&quot;에 대해 `$main::search_content_class`을 테스트하는 것은 가능한 3개의 내용 유형 값 중 하나와 일치합니다.
* 필터링 스크립트에서 STDOUT에 아무 것도 인쇄되지 않으면 문서가 다운로드된 것과 동일하게 사용됩니다. 즉, 문서의 아무 내용도 변경할 필요가 없으면 해당 문서의 STDIN을 STDOUT에 복사할 필요가 없습니다.
* 문서에서 모든 텍스트를 제거하려면 유효한 STDOUT 파일을 인쇄합니다. 예를 들어 HTML 문서에서 모든 텍스트를 완전히 제거하려면 다음을 수행합니다.`print "<html></html>";`

## 초기화 스크립트 추가 중 {#task_5A03B8D0C46E4674B7CE88203515803B}

초기화 스크립트는 문서를 인덱싱하기 전에 한 번 실행되는 Perl 스크립트입니다.

필터링 스크립트, 종료 스크립트 및 URL 마스크 스크립트와 함께 초기화 스크립트를 사용합니다.

초기화 스크립트의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 구축해야 합니다.

스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)

**초기화 스크립트를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Initialization Script] 페이지의 [!DNL Test URL] 필드에 웹 사이트에 있는 문서의 URL을 입력합니다.

   원시 HTML 텍스트의 변경 사항을 보려면 테스트 옵션을 클릭합니다.

   **필터링 스크립트 추가** 아래의 필터링 옵션 테이블을 참조하십시오.

   필터링 스크립트 및 URL 마스크에 대해 테스트하려면 **[!UICONTROL Test]**&#x200B;을 클릭합니다.

   **[!UICONTROL Test]**&#x200B;을 클릭해도 초기화 스크립트가 업데이트되고 저장되지 않습니다.
1. [!DNL Initialization Script] 필드에 스크립트를 붙여 넣습니다.
1. (선택 사항) 필터링, 초기화 및 종료 스크립트를 실행하여 스크립트에 대한 빠른 구문 검사를 수행하려면 **[!UICONTROL Check Syntax]**&#x200B;을 클릭합니다.

   **[!UICONTROL Check Syntax]** 은 스크립트를 업데이트 및 저장하지 않습니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Initialization Script] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 종료 스크립트 정보 {#concept_AAD6B3B0E7124874AD0947096FC42F47}

웹 문서를 인덱싱하기 전에 [!DNL Termination Script]을 사용하여 웹 문서의 내용을 변경할 수 있습니다.

HTML 태그를 삽입하고, 관련 없는 컨텐츠를 제거할 수 있으며, 문서의 URL, MIME 유형 및 기존 컨텐츠를 기반으로 새로운 HTML 메타데이터를 만들 수도 있습니다. 초기화 스크립트는 강력한 문자열 처리와 정규 표현식 일치의 유연성을 제공하는 Perl 스크립트입니다. 초기화 스크립트, 필터링 스크립트, 종료 스크립트, URL 마스크 스크립트 및 테스트 URL과 함께 종료 스크립트를 사용합니다.

종료 스크립트는 모든 문서가 인덱싱된 후에 한 번 실행됩니다. 종료 스크립트를 사용하여 필터링 스크립트에서 인덱스 로그로 상태 메시지를 인쇄할 수 있습니다. 메시지를 STDERR로 인쇄하거나 `_search_debug_log()` 하위 루틴을 통해 인쇄합니다.

단계 종료 스크립트 페이지의 **[!UICONTROL Expert (diff)]** 모드에서 사용할 수 있는 일부 GNU 비교 명령줄 옵션에는 다음이 포함됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diff 명령줄 옵션 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> 공백 크기의 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> 빈 줄을 삽입하거나 삭제하는 변경 사항을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트 출력 형식을 사용하여 3줄의 컨텍스트를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수) 행을 표시하거나, 줄이 지정되지 않으면 3개의 컨텍스트 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> 대/소문자를 구분하지 않습니다.대소문자 등가 것으로 간주합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> 출력 결과를 에드 스크립트와 유사하지만 파일에 나타나는 순서대로 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> RCS 형식 디폴트를 출력합니다.각 명령이 영향을 받는 줄 수를 지정한다는 점을 제외하고 <span class="codeph"> -f </span>와 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> 세 줄의 컨텍스트를 표시하는 통합 출력 형식을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U 선  </span> </p> </td> 
   <td colname="col2"> <p> 컨텍스트의 선(정수)을 표시하거나, 행이 지정되지 않으면 3개의 출력 형식을 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이러한 스크립트에서 로컬 변수, 전역 변수 또는 둘 다를 사용할 수 있습니다. 모든 전역 변수는 네임스페이스 &quot;main:::&quot;로 앞에 표시됩니다. 종료 스크립트가 시작되면 해당 환경에 다음과 같은 표준 파일 핸들이 포함됩니다.

* STDIN - 없음(읽을 때 즉시 EOF 반환)
* STDOUT - 없음(데이터가 STDOUT에 인쇄되는 경우 무시됩니다.)
* STDERR - STDERR로 인쇄되는 데이터가 색인 로그에 오류로 인쇄됩니다.

또한 다음 예와 같이 `_search_debug_log()` 하위 루틴을 사용하여 인덱스 로그에 사용자 정의 메시지를 작성할 수 있습니다.

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

이러한 메시지는 `DEBUG` 단어와 함께 서문으로 표시되며 오류로 기록되지 않습니다.

필터링 스크립트에 의해 처리된 문서 수를 색인 로그에 오류 행으로 표시하려면 다음 종료 스크립트를 사용할 수 있습니다.

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

[전역 변수](#global-variables)를 참조하십시오.

### 빠른 팁 {#section_5790EA7ACAC046CBA01F759F88E2460F}

* 모든 전역 변수는 네임스페이스 &quot;main::&quot; 앞에 표시됩니다.`$main::doc_count = 0;`
* 모든 로컬 변수는 &quot;my&quot;로 선언됩니다.`my $i = 0;`
* 서브루틴은 초기화 스크립트에 정의됩니다. 다음과 같은 명시적 &quot;main::&quot; 네임스페이스가 필요하지 않습니다.`sub my_sub {` `...`

   `}`

* 파일을 변경하기 전에 `$main::search_content_type`을 테스트합니다. 테스트를 수행하면 SWF 파일 또는 PDF 파일과 같이 바이너리 파일을 함부로 변경하지 않아도 됩니다.

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type`은 서버에서 제공하는 전체 내용 유형 헤더입니다. &quot;text/html&quot;과 같은 간단한 MIME 유형을 포함할 수도 있습니다. 또는 MIME 형식을 포함할 수 있으며 그 뒤에 &quot;text/html;&quot;과 같은 문서의 문자 집합 인코딩과 같은 다른 정보가 올 수 있습니다.charset=iso-8859-1&quot;
* HTML이 아닌 문서의 각 유형에 대해 `$main::search_content_type`은(는) 다양한 값을 사용할 수 있습니다. 스크립트에서 각 값에 대한 테스트는 번거롭게 됩니다. 예를 들어 일부 Word 문서에는 &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; 또는 &quot;application/x-msword&quot;의 컨텐츠 유형 값이 있습니다. 이러한 경우 `$main::search_content_class`은(는) 다음 값을 사용할 수 있습니다.

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * 텍스트

* 이 예제에서 &quot;word&quot;에 대해 `$main::search_content_class`을 테스트하는 것은 가능한 3개의 내용 유형 값 중 하나와 일치합니다.
* 필터링 스크립트에서 STDOUT에 아무 것도 인쇄되지 않으면 문서가 다운로드된 것과 동일하게 사용됩니다. 즉, 문서의 아무 내용도 변경할 필요가 없으면 해당 문서의 STDIN을 STDOUT에 복사할 필요가 없습니다.
* 문서에서 모든 텍스트를 제거하려면 유효한 STDOUT 파일을 인쇄합니다. 예를 들어 HTML 문서에서 모든 텍스트를 완전히 제거하려면 다음을 수행합니다.`print "<html></html>";`

## 종료 스크립트 추가 {#task_F0CFB412871642CFBC88132889C5B6F9}

종료 스크립트는 모든 문서를 인덱싱한 후에 한 번 실행되는 Perl 스크립트입니다.

필터링 스크립트, 종료 스크립트 및 URL 마스크 스크립트와 함께 종료 스크립트를 사용합니다.

초기화 스크립트의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 구축해야 합니다.

스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)

**종료 스크립트를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL Termination Script] 페이지의 [!DNL Test URL] 필드에 웹 사이트에 있는 문서의 URL을 입력합니다.

   원시 HTML 텍스트의 변경 사항을 보려면 테스트 옵션을 클릭합니다.

   **필터링 스크립트 추가**&#x200B;에서 필터링 옵션 표를 참조하십시오.

   필터링 스크립트 및 URL 마스크에 대해 테스트하려면 **[!UICONTROL Test]**&#x200B;을 클릭합니다.

   **[!UICONTROL Test]**&#x200B;을 클릭해도 종료 스크립트가 업데이트되고 저장되지 않습니다.
1. [!DNL Termination Script] 필드에 스크립트를 붙여 넣습니다.
1. (선택 사항) 초기화, 필터링 및 종료 스크립트를 실행하여 스크립트에 대한 빠른 구문 검사를 수행하려면 **[!UICONTROL Check Syntax]**&#x200B;을 클릭합니다.

   **[!UICONTROL Check Syntax]** 은 스크립트를 업데이트 및 저장하지 않습니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Termination Script] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## URL 마스크 정보 스크립트 {#concept_384F32EA18F84853A7BA99A04009330B}

필터링하면 웹 문서의 내용을 인덱싱하기 전에 변경할 수 있습니다. HTML 태그를 삽입하고, 관련 없는 컨텐츠를 제거할 수 있으며, 문서의 URL, MIME 유형 및 기존 컨텐츠를 기반으로 새로운 HTML 메타데이터를 만들 수도 있습니다. URL 마스크 스크립트는 강력한 문자열 처리와 정규식 일치의 유연성을 제공하는 Perl 스크립트입니다.

웹 사이트의 특정 부분에만 있는 문서의 내용을 변경하려면 URL 마스크 포함, URL 마스크 제외 또는 둘 모두를 지정하여 적절한 페이지를 정의할 수 있습니다.

`"https://www.mysite.com/faqs/"` 아래의 문서만 변경하려면 다음 마스크 세트를 사용할 수 있습니다.

```
include https://www.mysite.com/faqs/ 
exclude *
```

다음 예에서처럼 URL 마스크 스크립트에서 정규 표현식을 사용할 수도 있습니다.

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

스크립팅된 URL 마스크는 [!DNL URL Masks] 필드에 입력한 순서대로 고려됩니다. 문서 URL이 마스크와 일치하면 해당 문서가 마스크 유형에 따라 포함되거나 제외됩니다. 문서의 URL이 URL 마스크와 일치하지 않는 경우 MIME 유형이 &quot;text/html&quot;인 경우에만 문서가 포함됩니다. 다른 모든 MIME 유형은 제외됩니다.

## URL 마스크 스크립트 추가 중 {#task_D18F2A496C1C45C997B5DA650AAF5D59}

URL에 마스크 포함 및 마스크를 제외하여 웹 사이트의 특정 부분에만 있는 문서의 컨텐츠를 변경할 수 있습니다.

URL 마스크 설정의 효과를 방문자에게 표시하려면 먼저 사이트 인덱스를 다시 작성하십시오.

**URL 마스크 스크립트를 추가하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다.
1. (선택 사항) [!DNL URL Masks] 페이지의 [!DNL Test URL] 필드에 웹 사이트에 있는 문서의 URL을 입력한 다음 **[!UICONTROL Test]**&#x200B;를 클릭하여 필터링 스크립트 및 마스크에 대해 URL을 테스트합니다.

   테스트 URL 문서가 다운로드되며, 이 문서는 필터링 스크립트에 대한 STDIN 입력으로 사용됩니다. 그런 다음 필터링, 초기화 및 종료 스크립트가 실행됩니다. 새 브라우저 창에 출력되는 필터링 스크립트의 STDOUT 출력이 있는 경우.

   **[!UICONTROL Test]**&#x200B;을 클릭해도 스크립트가 업데이트되고 저장되지 않습니다.
1. [!DNL URL Masks] 필드에 줄당 하나의 URL 마스크를 입력합니다.
1. (선택 사항) 필터링, 초기화 및 종료 스크립트를 실행하여 URL 마스크의 빠른 구문 검사를 수행하려면 **[!UICONTROL Check Syntax]**&#x200B;을 클릭합니다.

   **[!UICONTROL Check Syntax]** 은 스크립트를 업데이트 및 저장하지 않습니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL URL Masks] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 필터링의 콘텐트 유형 정보 {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

이 계정에 대해 필터링할 콘텐츠 유형을 선택할 수 있습니다.

선택한 콘텐츠 형식 내에 있는 텍스트는 HTML로 변환된 후 필터링 스크립트에 지정된 스크립트를 사용하여 처리됩니다.

[스크립트 필터링 정보](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)를 참조하십시오.

선택할 수 있는 컨텐츠 유형은 다음과 같습니다.

* PDF 문서
* 텍스트 문서
* Adobe Flash 동영상
* Microsoft Word 파일
* Microsoft Office 파일(OpenXML)
* Microsoft Excel 파일
* Microsoft Powerpoint 파일
* MP3 음악 파일의 텍스트

컨텐츠 유형 설정의 효과나 설정 변경 사항이 고객에게 표시되기 전에 사이트 인덱스를 다시 만들어야 합니다.

## 필터링된 내용 유형 선택 {#task_C46081FA425A43EC8FDE6EA4A52A170A}

스크립트 필터링에 지정된 스크립트에 전달할 내용 유형을 선택합니다.

[스크립트 필터링 정보](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47)를 참조하십시오.

**필터링된 컨텐츠 유형을 선택하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**&#x200B;를 클릭합니다.
1. [!DNL Content Types] 페이지에서 필터 스크립트에 전달할 내용 유형을 확인합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트[의 증분 인덱스 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)
1. (선택 사항) [!DNL Content Types] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.
