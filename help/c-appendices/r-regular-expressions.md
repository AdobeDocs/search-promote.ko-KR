---
description: 정규 표현식 구성의 구문 및 규칙에 대한 재교육.
seo-description: 정규 표현식 구성의 구문 및 규칙에 대한 재교육.
seo-title: 정규 표현식
solution: Target
title: 정규 표현식
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 1%

---


# 정규 표현식{#regular-expressions}

정규 표현식 구성의 구문 및 규칙에 대한 재교육.

스테이지된 웹 사이트[의 증분 색인 구성을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)

**일반 표현식 구문**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>텍스트</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>모든 단일 문자 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [chars] </p> </td> 
   <td colname="col3"> <p> 문자 클래스:문자 중 하나 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^chars] </p> </td> 
   <td colname="col3"> <p>문자 클래스:문자 없음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> 대체 요소:text1 또는 text2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>한정 기호</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 이전 텍스트의 0 또는 1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 이전 텍스트 중 0 또는 N(N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>이전 텍스트 중 1 또는 N(N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>그룹</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (text) </p> </td> 
   <td colname="col3"> <p> 텍스트 그룹화 - 대체 요소의 테두리를 설정하거나 N이 있는 RewriteRule의 RHS에서 Nth 그룹이 사용되는 부분을 참조하도록 하기 위해) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>앵커</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> 선 앵커를 시작합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> 줄 끝 앵커. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>이스케이프</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>특정 문자를 escape합니다. 예를 들어 "" 문자를 지정합니다.[]()" 등. </p> </td> 
  </tr> 
 </tbody> 
</table>

**정규 표현식 규칙**

* 아래 설명된 특수 문자 중 하나가 아닌 일반 문자는 자신과 일치하는 한 문자 정규 표현식입니다.
* 백슬래시(\) 뒤에 특수 문자가 오는 것은 특수 문자 자체와 일치하는 1문자 정규 표현식입니다. 특수 문자는 다음과 같습니다.

   * `.` (마침표,  `*` (별표),  `?` (물음표),  `+` (더하기 기호),  `[` (왼쪽 대괄호),  `|` (세로 파이프) 및  `\` (백슬래시)는 대괄호 안에 나타나는 경우를 제외하고는 항상 특수 문자입니다.
   * `^` (삽입 기호 또는 곡절)는 일반 표현식의 시작 부분이나 대괄호 쌍의 왼쪽 바로 뒤에 오는 경우 특별합니다.
   * `$` (달러 기호)는 정규 표현식의 끝 부분에서 특별합니다.
   * `.` (period)는 새 행을 제외한 보조 코드 세트 문자를 포함하여 모든 문자와 일치하는 한 문자 정규 표현식입니다.
   * `[ ]`(왼쪽 및 오른쪽 대괄호)에 있는 비어 있지 않은 문자 문자열은 해당 문자열에서 보조 코드 세트 문자를 포함하여 하나의 문자와 일치하는 한 문자 정규 표현식입니다.

      그러나 문자열의 첫 번째 문자가 `^`(곡절)인 경우 한 문자 정규 표현식은 새 행 및 문자열의 나머지 문자를 제외하고, 보조 코드 세트 문자를 포함한 모든 문자를 찾습니다.

      `^`은 문자열에서 처음 발생하는 경우에만 이 특별한 의미를 갖습니다. `-`(빼기 기호)을 사용하여 보조 코드 세트 문자를 포함하여 연속된 문자 범위를 표시할 수 있습니다. 예를 들어 [0-9]은 [0123456789]과 같습니다.

      범위를 지정하는 문자는 동일한 코드 세트에서 와야 합니다. 문자가 다른 코드 세트에서 가져온 경우 범위를 지정하는 문자 중 하나가 일치합니다. `-`은(가) 처음 `^` 이후에) 또는 문자열의 마지막에 발생하는 경우 이 특수 의미를 잃게 됩니다(있는 경우). `]`(오른쪽 대괄호)은 문자열 내의 첫 번째 문자인 경우 초기 `^` 이후에 해당 문자열을 종료하지 않습니다. 예를 들어 `[]a-f]`은 `]`(오른쪽 대괄호) 또는 a~f의 ASCII 문자 중 하나를 찾습니다. 위에 특수 문자로 나열된 4개의 문자는 이러한 문자열 내에서 자신을 나타냅니다.

**한 문자 정규 표현식에서 일반 표현식을 구성하는 규칙**

다음 규칙을 사용하여 한 문자 정규 표현식에서 정규 표현식을 구성할 수 있습니다.

* 한 문자 정규 표현식은 한 문자 정규 표현식과 일치하는 모든 항목을 일치하는 정규 표현식입니다.
* 한 문자 정규 표현식 뒤에 `*`(별표)이 오는 일반 표현식은 0개 이상의 1자 정규 표현식과 일치하는 정규 표현식으로, 이 표현식은 보조 코드 집합 문자일 수 있습니다. 선택할 수 있는 경우 일치를 허용하는 가장 긴 왼쪽 문자열이 선택됩니다.
* 한 문자 정규 표현식 뒤에 `?`(물음표)이 오는 일반 표현식은 0이나 한 문자 정규 표현식의 1개 항목과 일치하는 정규 표현식입니다. 이 표현식은 보조 코드 집합 문자일 수 있습니다. 선택할 수 있는 경우 일치를 허용하는 가장 긴 왼쪽 문자열이 선택됩니다.
* 한 문자 정규 표현식 뒤에 `+`(더하기 기호)가 오는 일반 표현식은 한 문자 이상의 정규 표현식과 일치하며, 이 표현식은 보조 코드 집합 문자일 수 있습니다. 선택할 수 있는 경우 일치를 허용하는 가장 긴 왼쪽 문자열이 선택됩니다.
* 한 문자 정규 표현식 뒤에 `{m}`, `{m,}` 또는 `{m,n}`가 오는 일반 표현식은 한 문자 정규 표현식의 발생 범위와 일치하는 정규 표현식입니다. m 및 n의 값은 256보다 작은 음수가 아닌 정수여야 합니다.`{m}`은(는) 정확히 m회 발생 횟수와 일치합니다.`{m,}` 최소 m회 일치`{m,n}`는 m과 n의 포함 사이의 모든 일치 항목을 찾습니다. 선택 사항이 있을 때마다 정규 표현식은 가능한 한 많은 일치 항목을 찾습니다.
* 정규 표현식의 연결은 정규 표현식의 각 구성 요소와 일치하는 문자열의 연결과 일치하는 정규 표현식입니다.
* 문자 시퀀스( 및 ) 사이에 포함된 일반 표현식은 사용되지 않은 일반 표현식과 일치하는 모든 정규식입니다.
* 정규 표현식 뒤에 `|`(세로 파이프), 정규식은 첫 번째 정규 표현식(세로 파이프 앞)이나 두 번째 정규 표현식(세로 파이프 뒤)을 일치하는 정규 표현식입니다.

또한 정규 표현식을 행의 초기 세그먼트나 최종 세그먼트나 둘 다에 일치되도록 제한할 수 있습니다.

* 정규 표현식 시작 시 `^`(곡절)은 라인의 초기 세그먼트와 일치하도록 해당 정규 표현식을 제한합니다.
* 전체 정규 표현식 끝에 있는 `$`(달러 기호)는 해당 정규 표현식이 라인의 최종 세그먼트와 일치하도록 제한합니다.
* ^regular expression$ 생성에서는 정규 표현식을 전체 행과 일치하도록 제한합니다.

복잡한 대괄호로 묶은 일반 표현식 대신 사용할 수 있는 사전 정의된 문자 클래스 이름이 있습니다. 예를 들어 한 자리 정규 표현식 [0-9] 또는 문자 클래스 1자 정규 표현식 [[:digit:]]으로 숫자를 나타낼 수 있습니다.

사전 정의된 문자 클래스와 그 의미는 다음과 같습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>문자 클래스 </p> </th> 
   <th colname="col2" class="entry"> <p>의미 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> 알파벳 문자 또는 숫자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>알파벳 문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:blank:]] </p> </td> 
   <td colname="col2"> <p>공백이나 탭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> 제어 코드인쇄되지 않는 문자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:digit:]] </p> </td> 
   <td colname="col2"> <p>숫자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:graph:]] </p> </td> 
   <td colname="col2"> <p> 공간을 제외한 모든 인쇄 문자 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lower:]] </p> </td> 
   <td colname="col2"> <p>소문자 알파벳순 문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:print:]] </p> </td> 
   <td colname="col2"> <p> 공백을 포함한 모든 인쇄 문자 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:gest:]] </p> </td> 
   <td colname="col2"> <p> 구두점. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:공백:]] </p> </td> 
   <td colname="col2"> <p> 공백, 탭 또는 줄 끝과 같은 공백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:위쪽:]] </p> </td> 
   <td colname="col2"> <p> 대문자 알파벳순 문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xdigit:]] </p> </td> 
   <td colname="col2"> <p> 16진수, 대문자 또는 소문자로 구성됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

두 개의 특수 문자 클래스 이름은 단어 시작 및 끝 부분의 null 공백과 일치합니다. 즉, 실제 문자와 일치하지 않습니다. 단어는 영문자, 숫자 또는 밑줄(_)의 시퀀스로 간주됩니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>문자 클래스 </p> </th> 
   <th colname="col2" class="entry"> <p>의미 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> 단어 시작 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>단어 끝 </p> </td> 
  </tr> 
 </tbody> 
</table>

