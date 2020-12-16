---
description: 웹 사이트가 변경될 때마다 검색 로봇이 Remote Control을 사용하여 인덱스를 실행하도록 요청하는 스크립트 또는 프로그램을 실행할 수 있습니다.
seo-description: 웹 사이트가 변경될 때마다 검색 로봇이 Remote Control을 사용하여 인덱스를 실행하도록 요청하는 스크립트 또는 프로그램을 실행할 수 있습니다.
seo-title: 색인화를 위한 원격 제어 정보
solution: Target
title: 색인화를 위한 원격 제어 정보
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 1%

---


# 색인화에 대한 원격 제어 정보{#about-remote-control-for-indexing}

웹 사이트가 변경될 때마다 검색 로봇이 Remote Control을 사용하여 인덱스를 실행하도록 요청하는 스크립트 또는 프로그램을 실행할 수 있습니다.

## {#concept_C79B322190E84106A434E5C6D4A4118F} 인덱싱을 위한 원격 제어 사용

원격 제어 인덱싱 요청은 일반적으로 서버에 있는 스크립트나 프로그램에서 옵니다.

로봇은 [!DNL Index] 메뉴에서 수동으로 시작한 것과 동일한 인덱싱 단계를 수행합니다. 원격 제어 요청을 제출하려면 필요한 암호 및 응답 문자열을 구성합니다.

## 원격 제어 요청을 수행하는 방법 {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

원격 제어 요청을 수행하려면 데이터 센터의 위치를 기반으로 다음 형식 예제를 사용합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 센터 위치 </p> </th> 
   <th colname="col2" class="entry"> <p>예 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>런던 </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>북미 </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>싱가포르 </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

또는 

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>문자열 및 값 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999  </span> </p> </td> 
   <td colname="col2"> <p> 계정 번호입니다. </p> <p><span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> 계정 설정</b> </span> 아래에서 계정 번호를 찾을 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>실행 중인 인덱스 크롤의 상태를 확인할 수 있습니다. </p> <p> <span class="codeph">  N </span> 은 양의 정수이거나  <span class="codeph"> 모두 </span>입니다. 이 값이 숫자 값이면 해당 인덱스 로그 파일의 마지막 <span class="codeph"> N </span> 줄이 JSON 응답에 포함됩니다. </p> <p>값이 모두 <span class="codeph">이면 전체 파일이 반환됩니다.</span> </p> <p>값이 <span class="codeph"> 0 </span>이면 로그 정보가 반환되지 않습니다. 이 값은 실행 중인 인덱스 상태 쿼리의 기본값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>실행할 다음 인덱싱 작업 중 하나를 지정할 수 있습니다. </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>검색 로봇은 웹 사이트의 전체 인덱스를 실행합니다. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> increment_index  </span> <p>검색 로봇은 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> &lt;a9/&gt; 구성</b></span> 아래에 설정된 구성을 사용하여 증분 인덱스를 실행합니다. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>검색 로봇은 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> &lt;a9/&gt; 구성</b></span> 아래에 설정된 구성을 사용하여 수직 업데이트를 실행합니다. </p> <p><a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 수직 업데이트 정보</a>를 참조하십시오. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>검색 로봇은 <span class="uicontrol"> <b>인덱스</b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> 구성</b></span> 아래에 지정된 텍스트 파일을 사용하여 증분 인덱스를 실행합니다. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>검색 로봇은 웹 사이트의 전체 스테이지 인덱스를 실행합니다. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> increation_staged_index  </span> <p>검색 로봇은 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> &lt;a9/&gt; 구성</b></span> 아래에 설정된 구성을 사용하여 증분 단계 인덱스를 실행합니다. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertised_index  </span> <p>검색 로봇은 <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> </b> </span> &gt; <span class="uicontrol"> <b> &lt;a9/&gt; 구성</b></span> 아래에 설정된 구성을 사용하여 수직 단계 업데이트를 실행합니다. </p> </li> 
     </ul> </p> <p>참고: 수직 업데이트를 사용하려면 Adobe 계정 담당자 또는 Adobe 지원 담당자가 귀하의 계정에서 사용하도록 설정해야 할 수 있습니다. </p> <p><a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> 수직 업데이트 </a> 정보를 참조하십시오. </p> <p>검색 로봇이 저장된 컨텐츠를 사용하려고 시도하도록 하려면 위의 <span class="codeph"> sp_operation </span> 값에 <span class="codeph"> _saved </span> 값을 추가할 수 있습니다. 예를 들어 다음을 지정할 수 있습니다. </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>또는  </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>또는 위의 <span class="codeph"> sp_operation </span> 값에 <span class="codeph"> _status </span>를 추가하여 현재 또는 가장 최근 작업에 대한 상태 보고서를 요청할 수 있습니다. 예를 들어 다음을 지정할 수 있습니다. </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>또는  </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>결과를 JSON 개체로 반환합니다. 연결된 로그 파일의 N 행을 포함하려면 <span class="codeph"> sp_lines=N </span>을 포함합니다. N이 음수이면 마지막 N 라인이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive  </span> </p> </td> 
   <td colname="col2"> <p> 스테이지된 색인을 원격으로 실시간으로 푸시할 수 있습니다. </p> <p>푸시 라이브 작업에 <span class="codeph"> _saved </span>을 추가하려는 시도는 무시됩니다. </p> <p><span class="codeph"> pushlive </span> 작업을 실행하면 OK, Priority 또는 Error 응답 텍스트 문자열이 서버로 반환됩니다. <span class="wintitle"> 원격 제어 </span> 페이지에서 이러한 응답 문자열을 지정합니다. </p> <p>색인</a>에 대한 <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> 원격 제어 구성을 참조하십시오. </a></p> <p>스테이지된 인덱스가 없을 때 라이브를 푸시하면 아무 것도 발생하지 않으며 OK 응답 문자열이 반환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx  </span> </p> </td> 
   <td colname="col2"> <p>원격 제어 암호입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

검색은 적절한 HTTP 응답 형식으로 데이터를 반환합니다. 전체 응답은 HTTP 상태, HTTP 응답 헤더, 빈 행 및 응답 문자열로 구성됩니다.

예를 들어 다음과 같은 원격 제어 요청을 한다고 가정합니다.

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

다음은 서버의 응답입니다.

```
Status: 200 OK 
Content-type: text/plain 
OK
```

또는 다음과 같은 원격 제어 상태 요청을 수행한다고 가정합니다.

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

서버의 응답은 다음과 같을 수 있습니다.

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

이 인덱스 작업과 연관된 로그 목록의 처음 10줄을 상태와 함께 가져오려면 다음 쿼리가 사용됩니다.

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

서버의 응답:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

`offset` 값을 확인합니다. 이 값은 로그 파일에서 읽기가 중단된 파일 오프셋 위치를 식별합니다. 파일에서 *next* 열 줄을 읽으려면 서버에 전송된 요청에 `&sp_offset=672`를 포함시켜야 합니다.

`sp_offset`을 사용하면 로그 파일을 통해 효과적으로 페이지를 볼 수 있습니다.

상태와 함께 로그의 *마지막* 10줄을 가져오려면 수를 음수로 지정합니다. 예를 들어 다음과 같이 `-10` 값을 사용하여 `sp_lines=`을 지정합니다.

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

서버의 응답:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

이 작업이 파일 끝에 완료되었으며 읽을 줄이 더 이상 없으므로 여기에 반환되는 `offset` 값이 없습니다.

## {#task_57C296258404448DA7A5ADC9B7232391} 인덱싱을 위한 원격 제어 구성

웹 사이트가 변경될 때마다 Remote Control을 사용하여 서버에서 스크립트나 프로그램을 실행하여 검색 로봇이 인덱스를 실행하도록 요청할 수 있습니다.

**색인화를 위해 원격 컨트롤을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**&#x200B;을 클릭합니다.
1. [!DNL Remote Control] 페이지에서 각 구성 필드 옵션을 설정하여 서버에서 색인 요청을 자동으로 제출하여 웹 사이트를 색인화할 수 있습니다.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>옵션 </p> </th> 
    <th colname="col2" class="entry"> <p>설명 </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>원격 제어 암호 </p> </td> 
    <td colname="col2"> <p>원격 제어 암호를 지정합니다. </p> <p> 암호는 대/소문자를 구분하며 6자 이상이어야 하며 하나 이상의 문자를 포함해야 합니다. 하나 이상의 숫자를 포함하는 것이 좋습니다. </p> <p>사이트 검색/머천다이징 로그인 암호를 사용하지 마십시오. </p> <p>암호는 각 원격 제어 요청에 사용됩니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>확인 응답 문자열 </p> </td> 
    <td colname="col2"> <p>요청한 색인 작업이 성공적으로 시작되는 경우 OK 응답 텍스트 문자열을 지정할 수 있습니다. 이러한 경우 검색 로봇은 서버에 OK 응답 문자열을 반환합니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>우선 순위 응답 문자열 </p> </td> 
    <td colname="col2"> <p>원격 요청을 수행할 때 다른 인덱싱 작업이 진행 중인 경우 검색 로봇은 요청된 인덱스를 수행할 수 없습니다. 이 경우 Priority 응답 텍스트 문자열이 서버로 반환됩니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>오류 응답 문자열 </p> </td> 
    <td colname="col2"> <p>오류 응답 텍스트 문자열을 지정할 수 있습니다. 암호가 올바르지 않거나 다른 오류가 발생한 경우 이러한 경우 검색 로봇은 오류 응답 문자열을 다시 서버로 반환합니다. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
