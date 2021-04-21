---
description: '"날짜" 데이터 유형의 모든 필드를 구문 분석하여 색인화할 때 사용되는 날짜 형식을 정의할 수 있습니다.'
solution: Target
title: 날짜 형식
topic-legacy: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
exl-id: d3b4561b-6359-4b12-b0ff-40ca342a2faa
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 3%

---

# 날짜 형식{#date-formats}

&quot;날짜&quot; 데이터 유형의 모든 필드를 구문 분석하여 색인화할 때 사용되는 날짜 형식을 정의할 수 있습니다.

날짜 및 시간의 형식은 형식 문자열로 지정됩니다. 형식 문자열은 0개 이상의 변환 사양(전환 사양은 백분율 기호와 다른 문자로 구성됩니다)과 일반 문자로 구성됩니다. 각 날짜 필드에 대한 날짜 형식 문자열의 기본 목록이 제공됩니다.

이 목록을 완벽하게 제어할 수 있으며 사이트의 요구에 맞게 이 목록에 추가하거나 수정할 수 있습니다. 상위 형식 문자열이 우선 순위가 지정되고, 후속 형식 문자열은 지정된 메타데이터 태그의 내용을 구문 분석하면 오류가 발생하는 경우에만 사용됩니다.

예를 들어 다음 날짜 형식을 지정했다고 가정합니다.

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d, %Y %T %Z </p> <p>%A %B %d, %Y %T %Z </p> <p>%A %b %d, %Y %T %Z </p> <p>%a %B %d, %Y %T %Z </p> <p>%a %b %d, %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

첫 번째 형식 &quot;%B %d, %Y %T %Z&quot;은(는) 다음 &quot;2014년 9월 20일 13:12:00 PDT&quot;와 같은 날짜와 일치합니다. 이 형식 문자열로 메타데이터 태그 내용을 구문 분석할 수 없는 경우 사용 가능한 다음 형식 &quot;%b %d, %Y %T %Z&quot;을(를) 시도합니다. 이 형식은 다음과 같은 날짜와 일치합니다.&quot;2014년 9월 20일 3:12:00&quot; 메타데이터 태그 내용을 이 형식 문자열로 구문 분석할 수 없는 경우 사이트 검색/머천다이징이 작동하는 형식 문자열을 찾을 때까지 형식 문자열 목록으로 이동합니다.

다음 표에서는 사용 가능한 날짜 형식 문자열에 대해 설명합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 형식 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%A </p> </td> 
   <td colname="col2"> <p>"월요일"과 같이 전체 평일 이름의 전국적 표현으로 일치합니다. 국가 표현은 "단어 및 언어" 옵션의 "언어" 설정에서 결정됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> 약어가 처음 3자(예:"월" 국가 표현은 "단어 및 언어" 옵션의 "언어" 설정에서 결정됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> 월 이름의 전국적 표현(예:"6월" 국가 표현은 "단어 및 언어" 옵션의 "언어" 설정에서 결정됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> 약어가 처음 3자(예:"준" 국가 표현은 "단어 및 언어" 옵션의 "언어" 설정에서 결정됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> 는 "%m/%d/%y"과(와) 같습니다(예: )."06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> 월의 날짜를 십진수(01-31)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> 월의 날짜를 십진수(1-31)로 찾습니다.한 자리 앞에 빈 자리가 있음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> 시간(24시간)을 소수 자릿수로 일치(00-23) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> 약어가 처음 3자(예:"준"(%b과 동일) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> 시간(12시간)을 십진수(01-12)로 일치시킵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> 연도의 날짜를 십진수(001-366)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> 시간(24시간)을 십진수(0-23)로 일치시킵니다.한 자리 앞에 빈 자리가 있음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> 시간(12시간)을 십진수(1-12)로 일치시킵니다.한 자리 앞에 빈 자리가 있음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> 분을 소수점으로 일치(00-59) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> 월을 십진수로 일치(01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> "ante diem" 또는 "post meridiem"의 국가 표현(예:"PM." 국가 표현은 "단어 및 언어" 옵션의 "언어" 설정에서 결정됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> 는 "%H:%M"과(와) 같습니다(예:"13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> 는 "%I:%M:%S %p"과(와) 같습니다(예: )."01:23:45 PM" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> 둘째 숫자를 십진수로 일치(00-60) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> 는 "%H:%M:%S"과(와) 같습니다(예:"13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> 연도의 주 번호(주의 첫 날로 일요일)를 십진수(00-53)로 일치 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> 는 "%e-%b-%Y"와 같습니다(예: )."2001년 6월" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> 예를 들어, 세기가 있는 연도를 십진수로 일치시킵니다."2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> 세기가 없는 연도를 십진수(00-99)로 찾습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> 시간대 이름과 일치 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**기본 형식 문자열**

다음 기본 형식 문자열은 템플릿에 사용됩니다. 필요에 따라 이 목록에 추가하거나 편집할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>기본 형식 문자열 </p> </th> 
   <th colname="col2" class="entry"> <p>결과 예 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 13:12:00 GMT-7 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 13:12:00 GMT-7 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 일요일 13:12:00 GMT-7 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 일요일 13:12:00 GMT-7 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 13:12:00 GMT-7 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 1999년 9월 5일 13:12:00 GMT-7 </p> </td> 
  </tr> 
 </tbody> 
</table>
