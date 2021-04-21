---
description: 고객이 실패한 검색을 시도했을 때 올바른 검색어에 대한 제안을 받을 수 있도록 사용자가 의도한 행동을 구성할 수 있습니다. 유효한 검색어로 이어지는 검색어에 대한 맞춤법과 입력 수정을 통해 제안 사항이 생성됩니다.
solution: Target
title: 무슨 뜻입니까
topic-legacy: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
exl-id: c86da375-ac5f-442b-9975-6a4e1ba8a70d
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---

# {#about-did-you-mean} 정보를 의미했습니까?

고객이 실패한 검색을 시도했을 때 올바른 검색어에 대한 제안을 받을 수 있도록 사용자가 의도한 행동을 구성할 수 있습니다. 유효한 검색어로 이어지는 검색어에 대한 맞춤법과 입력 수정을 통해 제안 사항이 생성됩니다.

## {#task_B539D6A0043547EFB1CA19B67E762371}을(를) 구성하시겠습니까?

고객의 쿼리가 검색 결과를 반환하지 않거나 최소의 검색 결과를 반환할 때 [!DNL site search/merchandising]이 검색 제안을 하는 방법을 사용자 정의할 수 있습니다.

<!-- 

t_configuring_did_you_mean.xml

 -->

**다음을 구성하시겠습니까?**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**&#x200B;을 클릭합니다.
1. [!DNL Did You Mean] 페이지의 **추천 단어 제거** 텍스트 필드에 공백 또는 줄 구분 단어를 입력하여 원치 않는 제안을 필터링합니다.

   권장되는 대체 검색어로 표시되지 않는 검색 색인의 단어입니다. 일반 표현식을 사용하여 패턴과 일치하는 단어를 제외할 수 있습니다. 그렇지 않으면 정확한 단어만 제거됩니다.

1. 원하는 **Did You Mean** 옵션을 설정합니다.

   <!-- 
   
   r_did_you_mean_options.xml
   
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
      <td colname="col1"> <p>제안 알고리즘 </p> </td> 
      <td colname="col2"> <p>소프트웨어가 제안을 찾기까지 얼마나 걸리는지 조정합니다. 사용자가 한 문자 실수로 인해 모든 알고리즘에 동일한 제안이 표시됩니다. 이유는 작업 중인 제안에 도달하려면 한 번의 편집만 필요하며 모든 알고리즘은 원본과 가장 가까운 단어를 찾기 때문입니다. 하지만 원래 검색어가 인덱스의 기존 검색어와 유사하지 않으면 <b>Deep</b> 및 <b>잘못된 맞춤법 검사기</b> 추천 알고리즘이 계속 가능한 제안을 검색합니다. 이 시나리오는 고객이 입력하기 어려운 적절한 이름을 시도하여 이름을 소리낼 때 유용합니다. 그러나 유사한 제안만 표시하려는 경우 <b>빠른</b> 알고리즘을 선택할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>표시할 제안 기본 수 </p> </td> 
      <td colname="col2"> <p>고객의 검색에서 결과가 반환되지 않을 때 표시할 용어 제안(0-20)의 수를 지정합니다. 기본값은 3입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 추천 단어 길이 </p> </td> 
      <td colname="col2"> <p>제안된 단어에 대한 최소 문자 수를 지정하여 용어를 의미했습니까? </p> <p>예를 들어 값을 4로 설정하면 1, 2 또는 3자 길이의 단어가 소프트웨어에서 제안되지 않습니다. 0이라는 값을 지정하면 용어 제안에서 단어가 제거되지 않습니다. 높은 값을 지정하면 일반적으로 용어 제안 없이 결과가 표시됩니다. 기본값은 3입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 인덱스 빈도 </p> </td> 
      <td colname="col2"> <p> [의도한 단어] 사전에 포함되기 전에 색인에 단어가 나타나야 하는 최소 횟수를 지정합니다. </p> <p>필드에 음수는 지정할 수 없습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과가 없을 경우 추천 단어 검색 </p> </td> 
      <td colname="col2"> <p>고객의 검색에서 결과가 없고 하나 이상의 추천 단어 제안이 있을 때 제안된 첫 번째 용어를 자동으로 다시 검색합니다. </p> <p>프레젠테이션 템플릿에서 다음 태그를 사용하여 사이트 검색/머천다이징이 다른 용어를 자동으로 검색하고 있음을 나타낼 수 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>여기에서 다른 제안을 표시할 수도 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과가 낮아 추천 </p> </td> 
      <td colname="col2"> <p>고객이 10개 미만의 결과를 산출하는 용어를 검색하는 경우 검색 엔진은 100개 이상의 결과를 산출할 수 있는 제안이 있는지 확인합니다. 이 경우 다음 태그를 사용하여 사용자에게 결과가 있는 동안 다른 것을 검색하려고 할 수 있음을 표시할 수 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> 위 시나리오에서 제안 수는 <span class="uicontrol"></span>에 표시되는 제안 기본 개수에 지정된 값으로 제어됩니다. 낮은 임계값과 높은 임계값은 아래 옵션에 따라 구성할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>초기 결과가 </p> </td> 
      <td colname="col2"> <p>시스템에서 제안을 제공하기 시작할 때의 결과 수를 제어합니다. </p> <p>이 옵션은 <span class="uicontrol"> 결과가 낮기 때문에 제안 작업을 선택하는 경우에만 나타납니다</span>. </p> <p>기본값은 10입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>제안에서 이 이상의 결과를 생성해야 합니다. </p> </td> 
      <td colname="col2"> <p>기본 검색에서 결과 카운트로 결과가 낮아 수행된 제안을 필터링합니다. </p> <p>이 옵션은 <span class="uicontrol"> 결과가 낮기 때문에 제안 작업을 선택하는 경우에만 나타납니다</span>. </p> <p>기본값은 100입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.
