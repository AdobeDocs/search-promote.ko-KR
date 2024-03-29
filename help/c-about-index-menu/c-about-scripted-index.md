---
description: 스크립트 색인을 사용하면 로그인할 필요 없이 증분 색인 옵션을 작성, 업데이트 및 유지 관리할 수 있습니다. 검색 로봇은 서버에 호스팅된 텍스트 파일의 지침을 읽습니다.
solution: Target
subtopic: Scripted Index
title: 스크립트 색인 정보
topic-legacy: Index,Site search and merchandising
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
exl-id: e1d14cd5-4885-4e3a-bc5f-fe0b6a4df15e
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1725'
ht-degree: 1%

---

# 스크립트 인덱스 정보{#about-scripted-index}

스크립트 색인을 사용하면 로그인할 필요 없이 증분 색인 옵션을 작성, 업데이트 및 유지 관리할 수 있습니다. 검색 로봇은 서버에 호스팅된 텍스트 파일의 지침을 읽습니다.

## 스크립트 인덱스 사용 {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## 스크립팅된 증분 색인 구성 정보 {#section_161D254065E143F3A39F3FC09C400090}

스크립트 색인을 사용하려면 [스크립팅된 증분 색인 구성] 페이지를 사용하여 서버에 있는 스크립트 파일(일반 텍스트 파일)에 대한 URL을 지정합니다. 예, `https://www.mysite.com/indexlist.txt`. 사이트가 변경될 때 수동으로 또는 자동으로 텍스트 파일에 명령 블록을 추가할 수 있습니다(뉴스 피드, 주식 시세 또는 기타 변경된 파일에서 정보가 도착할 때 트리거되는 스크립트를 사용하여).

스크립트 증분 색인이 시작되면 검색 로봇은 텍스트 파일을 읽고 해당 파일에 있는 새 명령을 실행합니다. 기본적으로 검색 로봇은 파일 날짜에 따라 결정되는 새 명령만 처리합니다. 스크립트 색인을 구성할 때 **[!UICONTROL Clear Date]**&#x200B;을 선택하지 않으면 검색 로봇은 가장 최근에 처리된 블록의 날짜 지정자를 &quot;기억&quot;합니다.

## 스크립트 파일 {#section_B312E40539F44C6583B4F9637D428E19} 정보

URL에서 지정하는 스크립트 파일은 서버에 있는 일반 텍스트 파일입니다. 라인 끝 시퀀스에 캐리지 리턴, 줄 피드 또는 둘 다를 사용할 수 있습니다. 빈 행에는 0 이상의 공백 문자가 있고 그 뒤에 행 끝 시퀀스가 옵니다. 모든 명령은 대소문자를 구분하지 않습니다.

텍스트 파일은 검색 로봇이 스크립팅된 증분 인덱스를 수행할 때 사용하는 정보를 설명하는 블록으로 구성됩니다.

블록은 날짜별로 정렬되며 가장 오래된 블록은 텍스트 파일 맨 위에, 가장 최근의 블록은 맨 아래에 있습니다. 각 블록은 단일 행 date-command 및 date-specifier 명령으로 시작하고 다음 블록 예제에서와 같이 빈 행 구분 문자로 끝납니다(몇 개의 명령 사이에 있음).

HTTP 1.1 스타일을 사용할 때 10보다 낮은 모든 서수 날짜에 대해 행간 0이 필요합니다. 예를 들어 11월 6일은 11월 6일이 아니라 06일입니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>명령 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>date-command </p> </td> 
   <td colname="col2"> <p>각 블록의 첫 번째 행은 다음 두 날짜 명령 중 하나로 시작됩니다. </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> date  </span> <p>"date" 명령을 사용하여 날짜 지정자가 일, 날짜, 시간 및 시간대로 구성됨을 나타냅니다. </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> 초 </span> <p><span class="codeph">초 </span>을 사용하여 날짜 지정자가 epoch초 단위로 구성됨을 나타냅니다(예: 784111777). <span class="codeph">초 </span>을 사용할 때는 블록 간 초 수가 증가하는지 확인하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>date-specifier </p> </td> 
   <td colname="col2"> <p><span class="codeph"> date-specifier </span> 명령은 일반적으로 블록 정보를 파일에 추가한 시간(초 명령)과 서수 날짜 및 시간(날짜 명령) 또는 epoch 초(초 명령)을 기록합니다. 예: </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>HTTP 1.1 스타일을 사용할 때 10보다 낮은 모든 서수 날짜에 대해 행간 0이 필요합니다. 예를 들어 11월 6일은 11월 6일이 아니라 06일입니다. </p> <p>검색 로봇은 가장 최근에 처리된 블록의 날짜 지정자를 "기억"하며 "최신"으로 간주되는 정보만 인덱싱합니다. 검색 로봇에는 실시간 내용이 중요하지 않습니다. 대신 이전에 처리한 다른 시간과 관련된 시간이 중요한 시간입니다.) </p> <p>예를 들어 검색 로봇은 날짜 지정자가 10:00p.m인 블록을 읽은 후 색인 작업이 실행되는 시기에 관계없이 오후 10:00까지 기록하는 블록을 읽지 않습니다. 최악의 경우 날짜 지정자에 "2004" 대신 연도 "2040"을 잘못 입력할 수 있습니다. 이러한 경우 검색 로봇은 다음 인덱싱 작업 중에 2040 블록을 인덱싱한 다음 다른 정보 블록을 읽지 않습니다(2040년 이후 날짜 한 개가 없는 경우). 이러한 문제가 발생하면 텍스트 파일에서 이전에 처리된 모든 블록을 제거하고 <span class="uicontrol"> 날짜 지우기 </span>를 클릭한 다음 라이브로 푸시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주석 선 </p> </td> 
   <td colname="col2"> <p>"#" 문자로 주석 행을 시작합니다. </p> <p>각 주석 라인은 고유한 라인이어야 합니다.라인 끝 주석을 입력할 수 없습니다. </p> <p>주석 줄은 빈 행으로 간주되지 않습니다. 다음 예제와 같이 날짜 또는 초 명령 전이라도 블록의 어느 곳에나 표시될 수 있습니다. </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-command </p> </td> 
   <td colname="col2"> <p>각 텍스트 블록에는 원하는 만큼의 작업 명령이 포함될 수 있습니다. 다음 작업 명령 옵션은 표준 증분 인덱싱을 위한 옵션과 동일합니다. </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <code>
         add 
       </code> <p>URL과 함께 사용합니다. 검색 로봇은 마지막 인덱싱 작업 이후 변경된 지정된 URL만 인덱싱합니다. 또한 검색 로봇은 지정된 문서에 포함된 링크를 따르고 변경된 문서만 인덱싱합니다. </p> <p>URL을 
        <code>
          nofollow 
        </code> 또는 
        <code>
          noindex 
        </code> 키워드는 다음 예제와 같습니다. </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>URL 마스크와 함께 사용합니다. 검색 로봇은 지정된 URL 마스크와 일치하는 모든 문서를 찾아 업데이트합니다. </p> <p>URL을 
        <code>
          nofollow 
        </code> 또는 
        <code>
          noindex 
        </code> 키워드는 다음 예제와 같습니다. </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <code>
         include 
       </code> 또는 
       <code>
         exclude 
       </code> <p>URL 마스크와 함께 사용합니다. 검색 로봇은 지정된 마스크 유형에 따라 문서를 찾아서 인덱싱하거나("include") 문서를 무시합니다("exclude"). </p> <p>예: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p>또는  </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <code>
         include-date 
       </code> 또는 
       <code>
         exclude-date 
       </code> <p>URL 마스크와 함께 사용합니다. 검색 로봇은 URL과 문서 날짜를 모두 기준으로 문서를 찾아 인덱싱하거나("include") 문서를 무시합니다("exclude"). 다음 유형의 마스크를 사용할 수 있습니다. </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <code>
            include-days NNN 
          </code> <p>검색 로봇은 지정된 URL 마스크와 일치하고 NNN 일 이상인 모든 문서를 인덱싱합니다. </p> <p>키워드와 함께 URL 마스크를 따를 수 있습니다 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code> 및/또는 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> 검색 로봇은 지정된 URL 마스크와 일치하는 모든 문서를 인덱싱하고, YYYY-MM-DD 날짜보다 오래되거나 오래된 문서를 인덱싱합니다. 여기서 "YYYY"는 4자리 연도, "MM"은 1자리 또는 2자리 월(1-12)이고 "DD"는 1자리 또는 2자리 일(1-31)입니다. </p> <p>키워드와 함께 URL 마스크를 따를 수 있습니다 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code> 및/또는 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> 지정된 URL 마스크와 일치하고 NNN일 이상 오래된 모든 문서의 인덱싱을 비활성화합니다. </p> <p>키워드와 함께 URL 마스크를 따를 수 있습니다 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>지정된 URL 마스크와 일치하고 YYYY-MM-DD 날짜보다 이전 또는 이전 날짜인 모든 문서의 인덱싱을 비활성화합니다. </p> <p>키워드와 함께 URL 마스크를 따를 수 있습니다 
           <code>
             server-date 
           </code>. </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <code>
         delete 
       </code> <p>URL을 지정합니다. 검색 로봇은 URL로 식별되는 색인에서 문서를 제거합니다. </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <code>
         deletemask 
       </code> <p>검색 로봇은 지정된 URL 마스크와 일치하는 인덱스에서 문서를 제거합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)도 참조하십시오.

## 스크립트 파일 예 {#section_9F580F20E7214751B157A28B392BD64E}

다음 스크립트 파일 예제에서 검색 로봇은 date-specifiers가 가장 최근에 처리된 블록의 date-specifier 이후 날짜로 제공된 블록을 처리합니다. 이러한 경우 다음 인덱싱 작업이 발생합니다.

* 인덱스에서 `y2k-problems.html`을(를) 삭제합니다.
* `no-y2k-problems.html`을(를) 검색 색인에 추가하고 `no-y2k-problems.html`에 대한 링크를 팔로우하지 않습니다.

* 크롤링 중에 검색 인덱스에서 `housewares.htm` 및 `lightfixtures.htm`l과 일치하는 URL을 제외합니다.

* `www.mydomain.com` 아래에 다른 모든 디렉토리 및 문서를 포함합니다.
* `products` 및 `information` 디렉터리 내의 모든 문서를 업데이트하여 마지막 인덱싱 작업 이후 변경된 모든 하위 링크를 크롤링하고 인덱싱합니다.

* 크롤링 중에 1999년 1월 1일 이전 날짜인 경우 웹 사이트의 `archive` 섹션에서 URL을 제외합니다.
* 검색 인덱스에서 `housewares.html` 및 `lightfixtures.html`과(와) 일치하는 URL을 제외합니다.

* `help` 디렉터리에 있는 파일을 인덱싱하지만 해당 파일의 링크를 크롤링하거나 색인화하지 마십시오.
* `www.mydomain.com`에 대해 발생한 다른 파일을 크롤링하고 인덱싱합니다.

```
# Start of file. 
# Added by John Smith 
date Sat, 01 Jan 2004 16:05:53 PST 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/ 
delete https://www.mydomain.com/y2k-problems.html 
add https://www.mydomain.com/no-y2k-problems.html nofollow 
 
date Sun, 02 Jan 2004 20:19:08 PST 
# Added by the wire service updater 
exclude-date 1999-01-01 https://www.mydomain.com/archive server-date 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/help/ nofollow 
include https://www.mydomain.com/ 
# no add files, just update existing files 
# update all files in the "products" directory 
update https://www.mydomain.com/products/ 
# update all files in the "information" directory 
update regexp ^https://www\.mydomain\.com/information/.*$ 
# End of file.
```

## 스크립팅된 증분 인덱스 {#task_05AE040FE75E40FFAA5E10B6B6D4D255} 구성

로그인할 필요 없이 증분 인덱스를 작성하고 업데이트하며 유지 관리하는 스크립트를 지정할 수 있습니다. 검색 로봇은 서버에서 호스팅되는 텍스트 파일의 지침을 읽고 증분 인덱스를 수행합니다.

**스크립팅된 증분 인덱스를 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Configuration]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Scripted Incremental Index Configuration]** 페이지의 **[!UICONTROL Script File URL]**&#x200B;에서 서버에 있는 텍스트 파일 스크립트의 URL을 입력합니다.

   [스크립팅된 인덱스 정보](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)를 참조하십시오.
1. (선택 사항) 검색 로봇이 가장 최근에 처리된 블록의 날짜 지정자를 &quot;기억&quot;하지 못하게 하려면 **[!UICONTROL Clear Date]**&#x200B;을 선택합니다.

   기본적으로 검색 로봇은 파일의 날짜에 따라 결정되는 텍스트 파일에 있는 새로운 명령 블록만 처리합니다. 기본값을 원하지 않는 경우 **[!UICONTROL Clear Date]**&#x200B;을 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 라이브 웹 사이트 {#task_B3A87AC4AC784507859C23B9062BA11C}에 대해 스크립팅된 증분 색인 일정 설정

스크립팅된 증분 인덱싱을 하루 종일 일정한 간격으로 발생하도록 예약할 수 있습니다.

선택하는 기본 시간은 계정 설정에 구성된 시간대에 따라 로컬입니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

웹 서버는 종종 밤에 유지 보수를 위해 아래로 내려갈 예정이다. 예약된 색인 시간 동안 서버가 다운된 경우 색인 지정 프로세스가 실패합니다. 웹 서버를 사용할 수 있는 시간을 선택해야 합니다.

색인 일정은 라이브 색인에만 적용됩니다.스테이지된 증분 인덱스는 예약할 수 없습니다.

**라이브 웹 사이트에 대해 스크립팅된 증분 색인 일정을 설정하려면**

1. 제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Schedule]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Scripted Incremental Index Schedule]** 페이지의 **[!UICONTROL Read the Scripted Incrementally Indexing File]** 드롭다운 목록에서 스크립팅된 증분 인덱스 텍스트 파일을 실행할 빈도를 시간 또는 분 단위로 선택합니다.
1. **[!UICONTROL Base Time]** 드롭다운 목록에서 새로 스크립팅된 증분 인덱스를 다시 생성할 시작 시간을 선택합니다.
1. 클릭 **[!UICONTROL Save Changes]**.

## 라이브 또는 스테이지된 웹 사이트 {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}의 스크립트된 증분 인덱스 실행

스크립트 증분 색인을 사용하면 로그인할 필요 없이 라이브 또는 스테이징 웹 사이트의 &quot;부분&quot;을 인덱싱할 수 있습니다(예: 자주 변경된 페이지 컬렉션).

이 기능을 사용하려면 스크립팅된 증분 색인 텍스트 파일을 구성해야 합니다.

[스크립팅된 증분 인덱스 구성](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255)을 참조하십시오.

**라이브 또는 스테이지된 웹 사이트의 스크립트된 증분 인덱스를 실행하려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. 클릭 **[!UICONTROL Scripted Index Now]**.
1. (선택 사항) 색인 오류가 발생하면 **[!UICONTROL View Errors]**&#x200B;을 클릭하여 연결된 로그를 봅니다.

## 라이브 또는 스테이지된 웹 사이트 {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}의 스크립트된 증분 인덱스 로그 보기

실시간 전체 스크립트 색인 또는 스테이지된 전체 스크립트 인덱스가 완료되면 연결된 로그를 보고 발생한 오류를 해결할 수 있습니다.

로그를 내보내거나 저장할 수 없습니다. 그러나 새 색인이 발생할 때까지 로그는 계속 볼 수 있습니다.

**라이브 또는 스테이징 웹 사이트의 증분 색인 로그를 보려면**

1. 제품 메뉴에서 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * 클릭 **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. 로그 페이지의 맨 위 또는 아래에서 다음 중 하나를 수행합니다.

   * 탐색 옵션 **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** 또는 **[!UICONTROL Go to line]**&#x200B;을 사용하여 로그를 통해 이동합니다.

   * 표시 옵션 **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** 또는 **[!UICONTROL Show]**&#x200B;을 사용하여 표시되는 내용을 세밀하게 수정할 수 있습니다.
