---
description: 고객이 실패한 검색을 시도했을 때 올바른 검색어에 대한 제안을 받을 수 있도록 사용자가 의도한 행동을 구성할 수 있습니다. 올바른 검색으로 이어지는 검색어에 대한 맞춤법과 입력 수정을 검색하여 제안 사항이 만들어집니다.
seo-description: 고객이 실패한 검색을 시도했을 때 올바른 검색어에 대한 제안을 받을 수 있도록 사용자가 의도한 행동을 구성할 수 있습니다. 올바른 검색으로 이어지는 검색어에 대한 맞춤법과 입력 수정을 검색하여 제안 사항이 만들어집니다.
seo-title: 무슨 말이야
solution: Target
title: 무슨 말이야
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# About Did You Mean{#about-did-you-mean}

고객이 실패한 검색을 시도했을 때 올바른 검색어에 대한 제안을 받을 수 있도록 사용자가 의도한 행동을 구성할 수 있습니다. 올바른 검색으로 이어지는 검색어에 대한 맞춤법과 입력 수정을 검색하여 제안 사항이 만들어집니다.

## 구성 {#task_B539D6A0043547EFB1CA19B67E762371}

고객의 쿼리가 검색 결과를 반환하지 않거나 최소한 반환하는 경우 검색 제안을 [!DNL site search/merchandising] 만드는 방법을 사용자 지정할 수 있습니다.

<!-- 

t_configuring_did_you_mean.xml

 -->

**구성을**

1. 제품 메뉴에서 **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**&#x200B;을 클릭합니다.
1. 페이지의 [ [!DNL Did You Mean] 제안에서 **다음 단어 제거** ] 텍스트 필드에 공백이나 줄로 구분된 단어를 입력하여 원하지 않는 제안을 필터링합니다.

   권장되는 대체 검색어로 표시되지 않는 검색 색인의 단어입니다. 정규 표현식을 사용하여 패턴과 일치하는 단어를 제외할 수 있습니다. 그렇지 않으면 정확한 단어만 제거됩니다.

1. 원하는 **추천** 옵션을 설정합니다.

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
      <td colname="col2"> <p>소프트웨어가 제안을 찾는 데 소요되는 시간을 조정합니다. 사용자가 한 문자로 실수를 하면 모든 알고리즘이 동일한 제안을 내놓습니다. 그 이유는 한 번의 편집만으로 작업 중인 제안에 도달하고 모든 알고리즘은 원본과 가까운 단어를 찾기 때문입니다. 하지만 원래 검색어가 인덱스의 기존 검색어와 유사하지 않으면 <b>Deep</b> 및 <b>Bad Spellers</b> 추천 알고리즘이 가능한 제안을 계속 검색합니다. 이 시나리오는 고객이 입력하기 어려운 적절한 이름을 시도하여 이름을 소리내는 경우에 유용합니다. 하지만 유사한 제안만 표시하려면 빠른 <b>알고리즘을 선택할 수</b> 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>표시할 제안 기본 수 </p> </td> 
      <td colname="col2"> <p>고객의 검색에서 결과가 반환되지 않을 때 표시할 용어 제안(0-20)의 수를 지정합니다. 기본값은 3입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 추천 단어 길이 </p> </td> 
      <td colname="col2"> <p>추천 단어 수에 대한 최소 문자 수를 지정하여 용어를 의미했습니까? </p> <p>예를 들어 값을 4로 설정하면 1, 2 또는 3자 길이의 단어가 소프트웨어에서 제안되지 않습니다. 0을 지정하면 용어 제안에서 단어가 제거되지 않습니다. 높은 값을 지정하면 일반적으로 용어 제안이 없습니다. 기본값은 3입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최소 인덱스 빈도 </p> </td> 
      <td colname="col2"> <p> 단어가 Did You Mean 사전에 포함되기 전에 색인에 표시되어야 하는 최소 횟수를 지정합니다. </p> <p>필드에 음수는 지정할 수 없습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과가 없을 경우 추천 단어 검색 </p> </td> 
      <td colname="col2"> <p>고객의 검색에서 결과가 없고 용어 제안(Did You Mean)이 하나 이상 있을 때 처음 제안된 용어를 자동으로 다시 검색합니다. </p> <p>프레젠테이션 템플릿에서 다음 태그를 사용하여 사이트 검색/머천다이징이 자동으로 다른 용어를 검색하고 있음을 나타낼 수 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>여기에서 다른 제안을 표시할 수도 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>낮은 결과로 제안 </p> </td> 
      <td colname="col2"> <p>고객이 10개 미만의 결과를 생성하는 용어를 검색하는 경우 검색 엔진은 100개 이상의 결과를 산출할 수 있는 제안이 있는지 확인합니다. 이 경우 다음 태그를 사용하여 사용자에게 결과가 있는 동안 다른 것을 검색하려고 했을 수 있음을 표시할 수 있습니다. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> 위의 시나리오에서 제안 수는 표시할 <span class="uicontrol"></span>제안 기본값 수에 지정된 값에 의해 제어됩니다. 낮은 임계값과 높은 임계값은 아래 옵션을 통해 구성할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>초기 결과가 </p> </td> 
      <td colname="col2"> <p>시스템에서 제안을 제공하기 시작할 때의 결과 수를 제어합니다. </p> <p>이 옵션은 결과가 <span class="uicontrol"></span>낮기 때문에 제안 만들기를 선택할 때만 나타납니다. </p> <p>기본값은 10입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>제안에서 이 이상의 결과를 생성해야 합니다. </p> </td> 
      <td colname="col2"> <p>기본 검색의 결과가 낮은 결과 수로 인해 수행된 제안을 결과 수로 필터링합니다. </p> <p>이 옵션은 결과가 <span class="uicontrol"></span>낮기 때문에 제안 만들기를 선택할 때만 나타납니다. </p> <p>기본값은 100입니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

