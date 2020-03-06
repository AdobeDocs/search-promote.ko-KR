---
description: 검색 메뉴를 사용하여 제외된 단어, 컬렉션, 제한 사항, 미리 보기 및 프레임을 설정합니다.
seo-description: 검색 메뉴를 사용하여 제외된 단어, 컬렉션, 제한 사항, 미리 보기 및 프레임을 설정합니다.
seo-title: 검색 메뉴 정보
solution: Target
subtopic: Searching
title: 검색 메뉴 정보
topic: Settings,Site search and merchandising
uuid: 072111fc-a32b-4acb-8337-cb21bcdb5542
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 검색 메뉴 정보{#about-the-searching-menu}

검색 메뉴를 사용하여 제외된 단어, 컬렉션, 제한 사항, 미리 보기 및 프레임을 설정합니다.

## 검색 정보 {#concept_207105CF26B1448F8A3D223787C56AB8}

검색을 사용하여 프레젠테이션 템플릿이 참조할 수 있는 명명된 검색을 정의하고 사용자 정의할 수 있습니다.

<!-- 

c_about_searches.xml

 -->

프레젠테이션 템플릿에서 검색 모듈 내에 정의된 명명된 검색을 참조할 수 있습니다. 이렇게 하면 지정된 템플릿 세트에 대해 수행되는 검색 유형을 쉽게 사용자 정의할 수 있습니다.

자주 사용하는 구문 및 일반 단어를 검색 결과에서 제외하려면 제외된 단어 [구성을 참조하십시오](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE).

웹 사이트의 검색 가능한 특정 영역을 정의하려면 컬렉션 [추가를 참조하십시오](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6).

검색 결과 링크의 대상 프레임을 지정하려면 양식과 [함께 프레임](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5)사용을 참조하십시오.

HTTP 레퍼러, IP 주소 또는 요청 체계(HTTP 또는 HTTPS)를 기반으로 검색을 제한하려면 미리 보기에서 [값 설정을 참조하십시오](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7).

## 검색 팁 {#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

보다 구체적인 검색 결과를 얻으려면 다음 검색 팁을 사용할 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>검색 팁 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>맞춤법 검사 </p> </td> 
   <td colname="col2"> <p>검색어의 맞춤법이 올바른지 확인하십시오. [ <span class="uicontrol"> 음성 일치]가 [언어] &gt; [단어 및 언어]에서 </span> 활성화되어 <span class="uicontrol"> 있는 경우 검색 엔진은 </span> <span class="uicontrol"> </span>검색어와 유사한 소리를 내는 단어를 찾습니다. 하지만 항상 검색어의 맞춤법을 올바로 지정하는 것이 가장 좋습니다. </p> <p>단어 <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> 및 언어 정보를 </a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>여러 단어 사용 </p> </td> 
   <td colname="col2"> <p>예: 
     <userinput>
       무료 제품 
     </userinput> </p> <p>여러 단어로 된 쿼리는 단일 단어 쿼리보다 더 정교한 결과를 반환합니다. </p> <p>예: 
     <userinput>
       무료 제품 
     </userinput> 단순히 
     <userinput>
       product 
     </userinput>. </p> <p>관련 결과가 일부 쿼리 용어가 포함되어 있지 않더라도 반환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>유사한 단어 사용 </p> </td> 
   <td colname="col2"> <p>예: 
     <userinput>
       안전한 개인 정보 보호 보안 
     </userinput> </p> <p>검색 쿼리에 사용할 수 있는 단어가 비슷할수록 검색 결과가 더 관련성이 높아집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>적절한 대문자 사용 </p> </td> 
   <td colname="col2"> <p>예: 
     <userinput>
       검색 템플릿 참조 
     </userinput> </p> <p>올바른 명사를 대문자로 변환 소문자 단어를 사용하는 경우 검색 엔진은 해당 단어의 모든 대/소문자를 일치시킵니다. </p> <p>예를 들어, 
     <userinput>
       검색 
     </userinput>를 입력하면 "search", "Search" 및 "SEARCH"라는 단어가 포함된 모든 문서가 검색됩니다. 그러나 
     <userinput>
       검색 
     </userinput>를 입력하면 대문자 단어만 포함된 문서가 검색됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>따옴표 사용 </p> </td> 
   <td colname="col2"> <p>예: 
     <userinput>
       "Adobe의 약속" 
     </userinput> </p> <p>인용 부호를 사용하여 "귀하에 대한 약속"과 같이 서로 인접하여 표시되어야 하는 단어를 찾습니다. 주변 따옴표가 없으면 검색 결과에는 "our", "purchase", "to" 및 "you"라는 단어가 포함되지만 반드시 이 순서에는 포함되지 않습니다. 대신 문서 내에서 단어가 어디에나, 어떤 순서로도 나타날 수 있습니다. </p> <p> 라디오 단추와 함께 <span class="uicontrol"> 모든 구문에 대해 고급 검색 양식을 사용할 경우, </span>모든 <span class="uicontrol"> 구문과 구문에 대해 </span>모두 사용할 <span class="uicontrol"> 경우, </span><span class="uicontrol"> </span> 선택한 구문은 따옴표만 사용할 수 있습니다. 모든 <span class="uicontrol"> 또는 </span> 구문을 선택한 경우 인용 부호가 무시됩니다 <span class="uicontrol"> </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+(더하기) 또는 -(빼기) 사용 </p> </td> 
   <td colname="col2"> <p>예: 
     <userinput>
       +"템플릿 언어" 
     </userinput> </p> <p>검색어 또는 구문이 검색 결과에 나타나야 함을 나타내려면 +를 사용합니다. </p> <p>검색 결과에서 검색어 또는 구문이 누락되어야 함을 표시하려면 을(를) 사용합니다. </p> <p>따옴표 안에 구문을 포함해야 합니다. 위의 예에서처럼 더하기 또는 빼기 기호 및 검색어 사이에 공백을 두지 마십시오. </p> <p> 라디오 단추와 함께 <span class="uicontrol"> 모든 구문에 대해 고급 검색 양식을 사용할 경우, </span>모든 <span class="uicontrol"> 구문과 구문에 대해 </span>모두 사용할 <span class="uicontrol"> 경우, </span><span class="uicontrol"> </span> 선택한 구문은 따옴표만 사용할 수 있습니다. 모든 <span class="uicontrol"> 또는 </span> 구문을 <span class="uicontrol"> </span> 선택한 경우 더하기 및 빼기 수정자가 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필드 검색 사용 </p> </td> 
   <td colname="col2"> <p>예: </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <userinput>
         제목:정보 
       </userinput> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <userinput>
         desc:"Our Team" 
       </userinput> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <userinput>
         키:로그인 
       </userinput> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <userinput>
         본문:보안 
       </userinput> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <userinput>
         alt:"join now" 
       </userinput> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <userinput>
         url:help 
       </userinput> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <userinput>
         target:Adobe 
       </userinput> </li> 
     </ul> </p> <p>필드 검색을 사용하면 문서의 특정 부분에 나타나는 단어에 대한 특정 검색을 만들 수 있습니다. </p> <p>본문 텍스트(body:), 제목 텍스트(title:), 대체 텍스트(alt:), 메타 설명(desc:), 메타 키 단어(keys:), URL(url:) 또는 메타 대상 키 단어(target:)에 대해 필드 검색을 수행할 수 있습니다. 필드 이름에 소문자를 사용하고 바로 다음에 콜론을 사용합니다. 콜론과 검색어 사이에 공백이 없습니다. </p> <p>필드 검색 뒤에는 단어나 구문만 표시됩니다. 구문은 따옴표에 포함되어야 합니다. </p> <p>필드 이름에 대한 목록 상자가 있는 고급 검색 양식을 사용하는 경우 선택한 단어나 구 앞에 필드 이름만 입력할 <span class="uicontrol"> 수 </span> 있습니다. 목록 상자에서 다른 고급 검색 양식 필드를 선택하면 특정 필드 이름이 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>와일드카드 사용 </p> </td> 
   <td colname="col2"> <p>예: </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <userinput>
         wh* 
       </userinput> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <userinput>
         "wh* are" 
       </userinput> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <userinput>
         415-*-* 
       </userinput> </li> 
     </ul> </p> <p>와일드카드 검색은 특정 요청에 대한 일치 항목 수를 확장합니다. * 문자는 와일드카드 문자로 사용됩니다. </p> <p>예를 들어 
     <userinput>
       wh* 
     </userinput> 단어 "what", "why", "when", "which" 및 "wh"로 시작하는 다른 단어를 찾습니다. *her*를 검색하면 단어 내에서 "here", "whether", "together", "gathering" 및 "her"가 포함된 다른 단어가 모두 검색됩니다. </p> <p>와일드카드를 + 및 - 수정자, 구문의 인용 부호 및 필드 검색 지정자와 결합할 수 있습니다. </p> <p>검색 
     <userinput>
       +wh* -se*ch 
     </userinput> "wh"로 시작하고 "se"로 시작하고 "ch"로 끝나는 단어를 포함하지 않는 단어가 있는 모든 페이지를 찾습니다. </p> <p>검색 
     <userinput>
       "wh* are" 
     </userinput> 에서는 "where are", "what are", "why are" 등의 구문을 찾습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 새 검색 정의 추가 {#task_98D3A168AB5D4F30A1ADB6E0D48AB648}

이 [!DNL GS Add Search] 패널을 사용하여 프레젠테이션 레이어에서 패싯, 탐색 표시, 페이지 탐색, 메뉴 및 최근 검색과 같은 검색 구성 요소에 대한 새 검색 정의를 구성하고 추가할 수 있습니다.

<!-- 

t_adding_a_new_definition.xml

 -->

새 검색 정의를 추가한 후 프레젠테이션 템플릿에서 참조하도록 하십시오.

템플릿 [정보를 참조하십시오](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**새 검색 정의를 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Searches] 을 클릭합니다 **[!UICONTROL Add New Search]**.
1. 페이지에서 원하는 옵션을 **[!UICONTROL GS Add Search]** 설정합니다.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   프레젠테이션 템플릿을 선택하는 처리 규칙이 이러한 옵션 중 일부를 재정의할 수 있습니다.

   새 [검색 정의](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) 추가 또는 [검색 정의](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)편집을 참조하십시오.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>검색 이름 </p> </td> 
      <td colname="col2"> <p>정의된 검색의 이름을 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>소스 </p> </td> 
      <td colname="col2"> <p>사용할 백엔드 검색을 선택할 수 있습니다. SiteSearch 또는 <span class="wintitle"> 머천다이징에서 선택할 </span> 수 <span class="wintitle"> 있습니다 </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>계정 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>검색할 사이트 검색/머천다이징 계정을 선택할 수 있습니다. 일반적으로 현재 사용 중인 계정에서 검색이 검색됩니다. 그러나 프레젠테이션 템플릿은 다른 계정에 대해 백엔드 검색을 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>서버 이름/IP </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 검색이 액세스해야 <span class="wintitle"> 하는 머천다이징 </span> 서버의 전체 이름을 <span class="wintitle"> 지정합니다 </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>서버 포트 </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 <span class="wintitle"> 서버 </span> 포트 번호를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>피라미드 </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 서버 내의 <span class="wintitle"> 피라미드를 </span> 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과 수 </p> </td> 
      <td colname="col2"> <p>반환할 검색 결과 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 페이지 결과 수(다른 경우) </p> </td> 
      <td colname="col2"> <p>첫 번째 페이지에서 반환되는 결과 수를 지정합니다. 다른 페이지와 다르게 만들어야 하는 경우 이 옵션을 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>열 수 </p> </td> 
      <td colname="col2"> <p>검색 결과가 분할되는 열의 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색 유형 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>다음 세 가지 검색 유형 중에서 선택할 수 있습니다. </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> 모두 </span> <p>쿼리 문자열에서 모든 단어가 포함된 문서를 검색합니다. </p> <p>검색어가 비활성화되고 해당 문자가 무시되기 전에 "+" 및 "-"를 사용하십시오. </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> 임의 </span> <p>"+" 및 "-" 단어 접두사를 사용할 수 있습니다. </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> 구문 </span> <p>쿼리 문자열은 따옴표로 묶은 구문으로 취급되고 모든 사용자 입력 따옴표는 무시됩니다. </p> <p>검색어가 비활성화되고 해당 문자가 무시되기 전에 "+" 및 "-"를 사용하십시오. </p> </li> 
        </ul> </p> <p> 쿼리의 각 단어가 잠재적으로 패싯 값을 선택하도록 하려면 기본 검색에서 항상 <span class="uicontrol"> 모두를 사용해야 합니다 </span>. </p> <p>검색 쿼리에서 + 및 - 수정자의 사용과 관련된 검색 팁을 검토할 수 있습니다. </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">검색 정보</a>를 참조하십시오 . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>컬렉션 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>검색할 색인 내의 컬렉션을 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>홍보 검색 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>지정한 결과 수에 따라 검색 결과에서 임의의 <span class="uicontrol"> 선택을 사용할 </span> 수 있습니다. </p> <p>Promosearch는 기존 개념입니다. 따라서 사이트 검색/머천다이징 내에서 새로운 배너 관리 시스템을 사용하는 것이 좋습니다. </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">배너 정보</a>를 참조하십시오 . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 매개 변수 적용 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택하고 Promote </span> 를 선택한 경우에만 사용할 <span class="uicontrol"> 수 있습니다 </span>. </p> <p>프로모션 검색에 선택한 패싯을 사용하여 판촉 행사 범위를 좁히도록 지정합니다. 대부분의 판촉 행사 계정은 이 옵션을 사용하지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>일치하는 판촉 행사가 없는 경우 기본 판촉 행사 제공 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택하고 Promote </span> 를 선택한 경우에만 사용할 <span class="uicontrol"> 수 있습니다 </span>. </p> <p>판촉 행사에 대한 초기 검색이 아무 것도 찾지 못할 경우 다른 판촉 행사 검색이 발생하도록 지정합니다. 판촉에 대한 두 번째 검색은 키워드를 삭제합니다. 대신 "is_default" 메타데이터 필드가 "yes"로 설정된 모든 프로모션을 찾습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색 강조 표시 </p> </td> 
      <td colname="col2"> <p>"영웅 영역"에서 강조 표시할 기본 검색에서 선택한 수의 결과를 가져옵니다. </p> <p>일반적으로 강조 표시 검색은 기본 검색과 유사한 검색 기준을 가지지만 특정 결과를 강조 표시하는 다른 등급 메커니즘이 있습니다. 소프트웨어는 기본 검색에서 중복 항목을 제거합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 검색 </p> </td> 
      <td colname="col2"> <p>이 옵션은 [검색 강조 표시]를 선택한 경우에만 사용할 <span class="uicontrol"> 수 </span>있습니다. </p> <p>결과를 강조 표시하는 결과가 있는 검색을 선택할 수 있습니다. 중복 항목은 이 검색에서 제거됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중복 제거 우선 순위 </p> </td> 
      <td colname="col2"> <p>이 옵션은 [검색 강조 표시]를 선택한 경우에만 사용할 <span class="uicontrol"> 수 </span>있습니다. </p> <p>여러 개의 강조 표시 검색을 사용할 수 있습니다. </p> <p>강조 표시 검색이 여러 개인 경우 중복 제거의 우선 순위를 지정해야 합니다. 여기서 "1"은 가장 높은 우선 순위입니다. </p> <p>예를 들어 두 개의 강조 표시 검색이 있다고 가정합니다.베스트 셀러와 신상품. 이론적으로 신제품일 가능성도 있다. 이 경우 새 제품 및 기본 검색에서 복제본을 제거할 수 있습니다. 따라서 베스트셀러의 우선 순위를 1로 설정하고 신제품의 우선 순위를 2로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>검색에 CGI 매개 변수를 추가할 수 있습니다. </p> <p>백엔드 <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> 검색 CGI 매개 변수를 참조하십시오 </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Add]**.
1. (선택 사항) [!DNL Searches] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 검색 정의 편집 {#task_AF1FFB1AEF874C13AB359C28F74BF461}

이 [!DNL Staged GS Edit Search] 패널을 사용하여 검색 안내 프레젠테이션 레이어에 대한 기존 검색 정의를 다시 구성할 수 있습니다.

<!-- 

t_editing_a_search_definition.xml

 -->

검색 정의를 편집한 후 프레젠테이션 템플릿에서 참조했는지 확인합니다.

템플릿 [정보를 참조하십시오](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**검색 정의를 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Searches] 표에서 변경하려는 정의의 **[!UICONTROL Edit]** 행에서 을 클릭합니다.
1. 페이지에서 원하는 옵션을 **[!UICONTROL GS Edit Search]** 설정합니다.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   프레젠테이션 템플릿을 선택하는 처리 규칙이 이러한 옵션 중 일부를 재정의할 수 있습니다.

   새 [검색 정의](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) 추가 또는 [검색 정의](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)편집을 참조하십시오.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>검색 이름 </p> </td> 
      <td colname="col2"> <p>정의된 검색의 이름을 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>소스 </p> </td> 
      <td colname="col2"> <p>사용할 백엔드 검색을 선택할 수 있습니다. SiteSearch 또는 <span class="wintitle"> 머천다이징에서 선택할 </span> 수 <span class="wintitle"> 있습니다 </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>계정 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>검색할 사이트 검색/머천다이징 계정을 선택할 수 있습니다. 일반적으로 현재 사용 중인 계정에서 검색이 검색됩니다. 그러나 프레젠테이션 템플릿은 다른 계정에 대해 백엔드 검색을 사용할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>서버 이름/IP </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 검색이 액세스해야 <span class="wintitle"> 하는 머천다이징 </span> 서버의 전체 이름을 <span class="wintitle"> 지정합니다 </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>서버 포트 </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 <span class="wintitle"> 서버 </span> 포트 번호를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>피라미드 </p> </td> 
      <td colname="col2"> <p>이 옵션은 머천다이징을 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>머천다이징 서버 내의 <span class="wintitle"> 피라미드를 </span> 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>결과 수 </p> </td> 
      <td colname="col2"> <p>반환할 검색 결과 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>첫 번째 페이지 결과 수(다른 경우) </p> </td> 
      <td colname="col2"> <p>첫 번째 페이지에서 반환되는 결과 수를 지정합니다. 다른 페이지와 다르게 만들어야 하는 경우 이 옵션을 사용합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>열 수 </p> </td> 
      <td colname="col2"> <p>검색 결과가 분할되는 열의 수를 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색 유형 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>다음 세 가지 검색 유형 중에서 선택할 수 있습니다. </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> 모두 </span> <p>쿼리 문자열에서 모든 단어가 포함된 문서를 검색합니다. </p> <p>검색어가 비활성화되고 해당 문자가 무시되기 전에 "+" 및 "-"를 사용하십시오. </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> 임의 </span> <p>"+" 및 "-" 단어 접두사를 사용할 수 있습니다. </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> 구문 </span> <p>쿼리 문자열은 따옴표로 묶은 구문으로 취급되고 모든 사용자 입력 따옴표는 무시됩니다. </p> <p>검색어가 비활성화되고 해당 문자가 무시되기 전에 "+" 및 "-"를 사용하십시오. </p> </li> 
        </ul> </p> <p> 쿼리의 각 단어가 잠재적으로 패싯 값을 선택하도록 하려면 기본 검색에서 항상 <span class="uicontrol"> 모두를 사용해야 합니다 </span>. </p> <p>검색 쿼리에서 + 및 - 수정자의 사용과 관련된 검색 팁을 검토할 수 있습니다. </p> <p><a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">검색 정보</a>를 참조하십시오 . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>컬렉션 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>검색할 색인 내의 컬렉션을 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>홍보 검색 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택한 경우에만 사용할 </span> 수 있습니다. </p> <p>지정한 결과 수에 따라 검색 결과에서 임의의 <span class="uicontrol"> 선택을 사용할 </span> 수 있습니다. </p> <p>Promosearch는 기존 개념입니다. 따라서 사이트 검색/머천다이징 내에서 새로운 배너 관리 시스템을 사용하는 것이 좋습니다. </p> <p><a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">배너 정보</a>를 참조하십시오 . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>패싯 매개 변수 적용 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택하고 Promote </span> 를 선택한 경우에만 사용할 <span class="uicontrol"> 수 있습니다 </span>. </p> <p>프로모션 검색에 선택한 패싯을 사용하여 판촉 행사 범위를 좁히도록 지정합니다. 대부분의 판촉 행사 계정은 이 옵션을 사용하지 않습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>일치하는 판촉 행사가 없는 경우 기본 판촉 행사 제공 </p> </td> 
      <td colname="col2"> <p>이 옵션은 Search&amp;Promote를 <span class="uicontrol"> 소스로 선택하고 Promote </span> 를 선택한 경우에만 사용할 <span class="uicontrol"> 수 있습니다 </span>. </p> <p>판촉 행사에 대한 초기 검색이 아무 것도 찾지 못할 경우 다른 판촉 행사 검색이 발생하도록 지정합니다. 판촉에 대한 두 번째 검색은 키워드를 삭제합니다. 대신 "is_default" 메타데이터 필드가 "yes"로 설정된 모든 프로모션을 찾습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>검색 강조 표시 </p> </td> 
      <td colname="col2"> <p>"영웅 영역"에서 강조 표시할 기본 검색에서 선택한 수의 결과를 가져옵니다. </p> <p>일반적으로 강조 표시 검색은 기본 검색과 유사한 검색 기준을 가지지만 특정 결과를 강조 표시하는 다른 등급 메커니즘이 있습니다. 소프트웨어는 기본 검색에서 중복 항목을 제거합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>기본 검색 </p> </td> 
      <td colname="col2"> <p>이 옵션은 [검색 강조 표시]를 선택한 경우에만 사용할 <span class="uicontrol"> 수 </span>있습니다. </p> <p>결과를 강조 표시하는 결과가 있는 검색을 선택할 수 있습니다. 중복 항목은 이 검색에서 제거됩니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>중복 제거 우선 순위 </p> </td> 
      <td colname="col2"> <p>이 옵션은 [검색 강조 표시]를 선택한 경우에만 사용할 <span class="uicontrol"> 수 </span>있습니다. </p> <p>여러 개의 강조 표시 검색을 사용할 수 있습니다. </p> <p>강조 표시 검색이 여러 개인 경우 중복 제거의 우선 순위를 지정해야 합니다. 여기서 "1"은 가장 높은 우선 순위입니다. </p> <p>예를 들어 두 개의 강조 표시 검색이 있다고 가정합니다.베스트 셀러와 신상품. 이론적으로 신제품일 가능성도 있다. 이 경우 새 제품 및 기본 검색에서 복제본을 제거할 수 있습니다. 따라서 베스트셀러의 우선 순위를 1로 설정하고 신제품의 우선 순위를 2로 설정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>검색에 CGI 매개 변수를 추가할 수 있습니다. </p> <p>백엔드 <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> 검색 CGI 매개 변수를 참조하십시오 </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) [!DNL Searches] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 검색 정의 삭제 {#task_1D8E991E4C4146B7A7311FAE5DAA3742}

더 이상 필요하거나 사용하지 않는 안내서 검색 정의를 삭제할 수 있습니다.

<!-- 

t_deleting_a_search_definition.xml

 -->

템플릿 [정보를 참조하십시오](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**검색 정의를 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Searches] 표에서 제거할 정의의 **[!UICONTROL Delete]** 행에서 을 클릭합니다.
1. 대화 [!DNL Confirmation] 상자에서 을 클릭합니다 **[!UICONTROL OK]**.
1. (선택 사항) [!DNL Searches] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 고정된 결과 키워드 관리자 정보 {#concept_0C5F152C029C485D8872C6795CBCD7C7}

검색 결과를 특정 위치에 수동으로 고정할 수 있습니다. 이러한 고정된 결과는 특정 검색 쿼리 또는 키워드와 연관됩니다. 를 [!DNL Pinned Result Keyword Manager] 사용하여 결과가 고정된 모든 키워드를 관리할 수 있습니다.

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## 따를 키워드 검색 규칙 {#section_ED67A24BE884468286F34FA5DFF826D7}

패널에 입력하는 검색 쿼리에는 다음 규칙이 있습니다.

* 쿼리에서 선행 및 후행 공백이 삭제됩니다.
* 다음과 같은 특수 검색 문자는 사용할 수 없습니다.

   * 별표(*)로 일치하는 와일드카드
   * 더하기 또는 빼기(+ 또는 -)를 사용할 때 필수 또는 필수-가 아니어야 합니다.
   * 콜론 문자(:)가 있는 필드 지정자가 없습니다.
   * 쉼표나 큰따옴표(, 또는 &quot;)가 없습니다.

* 쿼리에서 공백으로 구분된 여러 개의 용어 또는 단어가 허용됩니다.
* 대문자는 소문자로 변환됩니다.

검색어는 그대로 기억됩니다.동일한 결과를 얻으려면 동일한 검색어를 다시 사용해야 합니다.

고정된 결과는 대/소문자 구분을 지원하지 않습니다. 모든 키워드의 대문자가 소문자로 변환됩니다.

## 검색 결과 순서 변경 {#section_46FBE5279C7740A09D6DC9F54FE104AA}

패널이나 [!DNL Stage Add New Keyword] [!DNL Staged Edit Keyword] 패널에서 키워드를 검색할 때 검색 결과는 다음 인덱스 작업 후 발생할 수 있는 일을 반영합니다. 세 가지 다른 방법 중 하나를 사용하여 테이블에서 검색 결과의 순서를 변경할 수 있습니다.

첫 번째 방법은 **[!UICONTROL Pinned]** 확인란을 사용하는 것입니다. 이 확인란은 결과를 특정 위치에 고정하는 데 사용됩니다. 확인란을 선택하면 확인란 위의 모든 검색 결과도 고정됩니다. 이 기능을 사용하면 해당 확인란 위의 모든 결과가 특정 순서로 표시됩니다. 검색 결과의 고정을 해제하면 검색 결과가 현재 고정된 모든 결과 아래에 놓입니다.

두 번째 방법은 표에서 드래그 앤 드롭을 사용하는 것입니다. 드래그 앤 드롭으로 결과를 새 위치로 이동할 수 있습니다. 결과를 새 위치로 드래그하면 새 위치 위의 모든 결과가 핀으로 고정됩니다. 이 자동 핀으로 인해 나머지 결과가 최근에 드래그한 결과 위에 표시됩니다.

세 번째 방법은 &quot;#&quot; 열에 특정 위치를 입력하여 고정된 결과의 순서를 설정하는 것입니다. 드래그 앤 드롭과 달리 시뮬레이트된 검색 결과의 순서는 다음에 [!DNL Staged Edit Keyword] 패널을 열 때만 명확합니다. 현재 고정되지 않은 행의 주문 번호를 설정하면 여러 항목이 핀으로 고정됩니다. 현재 고정된 행의 주문 번호를 설정하면 현재 고정된 항목 내에서 해당 항목의 순서가 설정됩니다. 하지만 핀으로 고정된 항목의 수는 증가하지 않습니다.

검색 결과를 저장할 때 키워드 필드에 동일한 쿼리를 입력하여 결과를 다시 볼 수 있습니다.

## 고정된 검색 결과 정보 {#section_46780B7812F249F3B45503161C4FBDEE}

검색 결과는 관련성 점수로 순서가 정해집니다. 하지만 고정된 검색 결과는 관련 점수를 무시하고 미리 결정된 위치로 자연어 순서를 무시하려고 합니다. 결과가 상대적으로 있는 곳에 있도록 하여 그 위에 알려진 다른 검색 결과를 핀으로 묶어야 합니다.

패널에 표시되는 검색 결과는 다음 인덱스 다음에 표시되는 내용을 시뮬레이션합니다. 그러나 원본 문서의 변경 사항이나 멤버 센터의 특정 구성 변경 사항이 일치하지 않는 결과를 생성할 수 있습니다. 예를 들어 문서의 내용을 변경하는 작업은 색인 이후에나 알 수 있습니다.

핀 결과는 관련성을 무시하므로 색인 뒤에 유사하거나 동일한 순서로 나타납니다. 고정 해제된 결과는 색인 다음에 원래 위치로 돌아갑니다.고정 해제된 결과의 순서는 보장되지 않습니다.

## Adding a new keyword {#task_8CED128DADD34D0DAD2C64B64D0D6B06}

새 키워드와 고정된 결과를 추가할 수 있습니다.

<!-- 

t_adding_a_new_keyword.xml

 -->

새 키워드를 추가할 때 검색 결과의 순서를 변경하고 특정 위치에 고정할 수 있습니다.

**새 키워드를 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**&#x200B;을 클릭합니다.
1. 페이지에서 [!DNL Pinned Keyword Results Manager] 을 클릭합니다 **[!UICONTROL Add New Keyword]**.
1. 페이지의 [!DNL Add New Keyword] 필드에 **[!UICONTROL Keyword]** 검색 쿼리를 입력한 다음 을 클릭합니다 **[!UICONTROL Search Keyword]**.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   테이블 편집 단추를 사용하여 검색 결과 테이블을 보는 방법을 조정할 수 있습니다. 예를 들어 열 목록을 사용하여 특정 열을 표시하거나 숨길 수 있습니다. 드래그 앤 드롭을 사용하여 열의 순서를 다시 정렬할 수도 있습니다.

   다음 표에서는 테이블 편집기에 있는 열 속성에 대해 설명합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>열 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>주문 </p> </td> 
      <td colname="col2"> <p>열 모양의 숫자 순서를 지정합니다. 열을 드래그 앤 드롭하여 순서를 자동으로 업데이트할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 이름 </p> </td> 
      <td colname="col2"> <p>스테이지 새 키워드 추가 패널과 스테이지 편집 키워드 <span class="wintitle"> 패널의 </span> 시뮬레이션 검색 결과 <span class="wintitle"> 테이블에 표시되는 </span> 열 머리글의 이름을 <span class="wintitle"> </span> 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>포함 </p> </td> 
      <td colname="col2"> <p>이 확인란을 선택하면 고정된 결과 테이블에 열이 나타납니다. 상자가 비어 있거나 선택 해제되어 있으면 표에서 열이 사라집니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL을 이미지로 표시 </p> </td> 
      <td colname="col2"> <p>이 열에 할당된 메타 필드에 그래픽이나 그림에 대한 URL이 있으면 이 상자를 선택하면 HTML 이미지 태그가 배치되고 그림이 나타납니다. 사진 누락 또는 링크가 비어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 길이 </p> </td> 
      <td colname="col2"> <p>줄임표(...)로 잘리기 전에 표시할 텍스트의 최대 길이를 입력할 수 있습니다. URL을 이미지로 표시하도록 열이 설정된 경우 이 필드는 아무런 영향을 주지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) 다음 중 하나를 수행합니다.

   * 검색 결과의 순서를 변경합니다.
   * 을 **[!UICONTROL Edit Table]** 클릭하여 [!DNL Simulated Search Results] 표의 보기를 조정합니다. 완료되면 을 클릭하여 **[!UICONTROL Save Changes]** 패널로 [!DNL Add New Keyword] 돌아갑니다.

1. 클릭 **[!UICONTROL Save Search Results]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.
1. (선택 사항) [!DNL Pinned Results Keyword Manager] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 키워드 편집 {#task_30C550A7350B4394B5B43536368A84B1}

기존 키워드와 고정된 결과를 편집할 수 있습니다.

<!-- 

t_editing_a_keyword.xml

 -->

키워드를 편집할 때 검색 결과의 순서를 변경하고 특정 위치에 고정할 수 있습니다.

**키워드를 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Pinned Keyword Results Manager] 표에서 변경할 키워드의 **[!UICONTROL Edit]** 행에서 을 클릭합니다.
1. 페이지의 [!DNL Edit Keyword] 필드에 **[!UICONTROL Keyword]** 검색 쿼리를 입력한 다음 을 클릭합니다 **[!UICONTROL Search Keyword]**.

   키워드 검색에 대한 규칙을 따라야 합니다.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   테이블 편집 단추를 사용하여 검색 결과 테이블을 보는 방법을 조정할 수 있습니다. 예를 들어 열 목록을 사용하여 특정 열을 표시하거나 숨길 수 있습니다. 드래그 앤 드롭을 사용하여 열의 순서를 다시 정렬할 수도 있습니다.

   다음 표에서는 테이블 편집기에 있는 열 속성에 대해 설명합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>열 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>주문 </p> </td> 
      <td colname="col2"> <p>열 모양의 숫자 순서를 지정합니다. 열을 드래그 앤 드롭하여 순서를 자동으로 업데이트할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 이름 </p> </td> 
      <td colname="col2"> <p>스테이지 새 키워드 추가 패널과 스테이지 편집 키워드 <span class="wintitle"> 패널의 </span> 시뮬레이션 검색 결과 <span class="wintitle"> 테이블에 표시되는 </span> 열 머리글의 이름을 <span class="wintitle"> </span> 식별합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>포함 </p> </td> 
      <td colname="col2"> <p>이 확인란을 선택하면 고정된 결과 테이블에 열이 나타납니다. 상자가 비어 있거나 선택 해제되어 있으면 표에서 열이 사라집니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL을 이미지로 표시 </p> </td> 
      <td colname="col2"> <p>이 열에 할당된 메타 필드에 그래픽이나 그림에 대한 URL이 있으면 이 상자를 선택하면 HTML 이미지 태그가 배치되고 그림이 나타납니다. 사진 누락 또는 링크가 비어 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 길이 </p> </td> 
      <td colname="col2"> <p>줄임표(...)로 잘리기 전에 표시할 텍스트의 최대 길이를 입력할 수 있습니다. URL을 이미지로 표시하도록 열이 설정된 경우 이 필드는 아무런 영향을 주지 않습니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) 다음 중 하나를 수행합니다.

   * 검색 결과의 순서를 변경합니다.
   * 을 **[!UICONTROL Edit Table]** 클릭하여 [!DNL Simulated Search Results] 표의 보기를 조정합니다.

      새 [키워드](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06)추가를 참조하십시오.

      완료되면 을 클릭하여 **[!UICONTROL Save Changes]** 패널로 [!DNL Add New Keyword] 돌아갑니다.

1. 클릭 **[!UICONTROL Save Search Results]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.
1. (선택 사항) [!DNL Pinned Results Keyword Manager] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 키워드 삭제 {#task_F17D6357D6DD416495E6D4117899D81D}

더 이상 필요하거나 사용하지 않는 키워드를 삭제할 수 있습니다.

<!-- 

t_deleting_a_keyword.xml

 -->

새 키워드를 추가할 때 검색 결과의 순서를 변경하고 특정 위치에 고정할 수 있습니다.

**키워드를 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**&#x200B;을 클릭합니다.
1. 페이지의 표에서 제거할 키워드 [!DNL Pinned Keyword Results Manager] **[!UICONTROL Delete]** 행에서 을 클릭합니다.
1. 페이지에서 [!DNL Delete Keyword] 을 클릭합니다 **[!UICONTROL Delete]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.
1. (선택 사항) [!DNL Pinned Results Keyword Manager] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 컬렉션 정보 {#concept_62E42ACE53D54EEE9273433B86259127}

컬렉션을 사용하여 고객이 원하는 영역을 빠르게 찾을 수 있도록 고객이 웹 사이트의 특정 영역을 검색할 수 있도록 할 수 있습니다.

<!-- 

c_about_collections.xml

 -->

[검색 정보](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8)를 참조하십시오.

검색 [양식에서](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)컬렉션 사용을 참조하십시오.

예를 들어 고객은 제품 판매와 관련된 URL 컬렉션을 검색하거나 서비스를 지원할 수 있습니다. 고객이 지정한 컬렉션을 사용하려면 먼저 양식 검색 메뉴에서 검색 양식을 업데이트해야 합니다.

고객이 컬렉션 설정의 효과를 보기 전에 사이트 인덱스를 다시 작성하십시오.

선택적 **[!UICONTROL Test Collections]** 필드에 웹 사이트 URL 중 하나를 입력한 다음 을 클릭하여 컬렉션을 테스트할 수 **[!UICONTROL Test]**&#x200B;있습니다. 지정된 페이지가 속한 컬렉션이 반환됩니다.

각 컬렉션은 한 줄에 이름과 URL 마스크가 지정됩니다. URL 마스크는 다음과 같이 구성될 수 있습니다.

* 전체 경로(예: `https://www.mydomain.com/products.html`
* 부분 경로(예: `https://www.mydomain.com/products`
* 정규 표현

   마스크를 정규 표현식으로 만들려면 컬렉션 이름과 URL 마스크 `regexp` 사이에 키워드를 삽입합니다.

   정규 [표현식을 참조하십시오](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

컬렉션 필드의 각 줄에는 하나의 URL 마스크만 포함할 수 있습니다. 그러나 동일한 컬렉션 이름에 대해 여러 개의 URL 마스크를 여러 줄에 지정할 수 있습니다. 다음 예에는 4개의 서로 다른 컬렉션 이름과 5개의 URL 마스크가 포함되어 있습니다.

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

이 예에서는 이러한 컬렉션을 포함하도록 검색 양식을 업데이트한 후 고객이 정의된 각 컬렉션을 개별적으로 선택하고 검색할 수 있습니다. 이 `Support` 컬렉션에는 URL 마스크와 일치하는 파일이 포함되어 있으므로 이 컬렉션을 선택할 때 파일과 `www.yoursite.com/email_support/` 해당 파일을 모두 검색할 `www.yoursite.com/phone_support` 수 있습니다.

## 컬렉션 추가 {#task_07732D0F00104E59AD421297A704B2F6}

컬렉션을 추가하여 고객이 원하는 영역을 빠르게 찾을 수 있도록 웹 사이트의 특정 영역을 검색할 수 있습니다.

<!-- 

t_adding_collections.xml

 -->

URL 마스크의 결과가 고객에게 표시되도록 사이트 인덱스를 다시 구축해야 합니다.

스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.

**컬렉션을 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Collections]**&#x200B;을 클릭합니다.
1. 필드에 컬렉션 이름과 URL 마스크 주소를 [!DNL Collections] 한 줄에 하나씩 입력합니다.
1. (선택 사항) [!DNL Collections] 페이지의 **[!UICONTROL Test Collections]** 필드에 웹 사이트의 테스트 URL 마스크를 입력한 다음 을 클릭합니다 **[!UICONTROL Test]**.

   URL과 컬렉션의 이름을 보여주는 테스트 컬렉션 출력 창이 표시됩니다.
1. 컬렉션 추가를 마쳤으면 을 클릭합니다 **[!UICONTROL Save Changes]**.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 [웹 사이트의](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)증분 인덱스 구성을 참조하십시오.
1. (선택 사항) [!DNL Collections] 페이지에서 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 제한 정보 {#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

검색이 수행되기 전에 참조 URL 및 IP 주소를 검토하여 해당 위치에서 검색이 가능한지 확인합니다. 에서 지정한 [!DNL Restrictions] 내용에 따라 검색이 허용되는지 여부가 결정됩니다. 검색이 허용되지 않으면 일반 오류 페이지가 요청자에게 반환됩니다.

<!-- 

c_about_restrictions.xml

 -->

레퍼러 URL 마스크 또는 IP 주소 마스크로 제한 설정을 지정할 수 있습니다. 두 가지 유형의 제한 사항에는 검색을 허용하고 마스크를 제외하여 검색을 거부할 수 있는 마스크가 포함됩니다.

레퍼러 URL과 IP 주소 제한 기준을 모두 전달하는 경우 검색이 허용됩니다. 두 설정 중 어느 하나라도 검색을 허용하지 않으면 검색을 허용하는 다른 제한에 관계없이 검색이 실패합니다.

예를 들어, 검색 요청의 &quot;HTTP 레퍼러&quot; 필드가 &quot;exclude&quot; 레퍼러 URL 마스크와 일치하는 경우 요청 IP 주소가 &quot;include&quot; IP 주소 마스크와 일치하더라도 검색이 실패합니다. 레퍼러 URL 또는 IP 주소와 일치하는 마스크가 없는 경우 기본적으로 위치가 포함됩니다.

각 포함 마스크 또는 제외 마스크를 한 줄에 입력합니다.

## 레퍼러 URL 마스크 또는 IP 주소 마스크 제한 추가 {#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

제한 설정을 &quot;레퍼러 URL 마스크&quot; 또는 &quot;IP 주소 마스크&quot;로 지정할 수 있습니다. 두 가지 유형의 제한 사항에는 검색을 허용하고 마스크를 제외하여 검색을 거부할 수 있는 마스크가 포함됩니다. 레퍼러 URL과 IP 주소 제한 기준을 모두 전달하는 경우 검색이 허용됩니다.

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**레퍼러 URL 마스크 또는 IP 주소 마스크 제한을 추가하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**&#x200B;을 클릭합니다.
1. 페이지에서 원하는 제한 옵션을 [!DNL Restrictions] 설정합니다. 레퍼러 URL 마스크 주소, IP 주소 마스크 주소 또는 선택적으로 사이트 검색이 허용되지 않는 고객에게 표시되는 사용자 지정 웹 페이지의 URL 주소를 입력합니다.

   <!-- 
   
   r_restriction_options.xml
   
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
      <td colname="col1"> <p>레퍼러 URL 마스크 </p> </td> 
      <td colname="col2"> <p>HTTP 레퍼러 헤더의 레퍼러 URL을 읽습니다. 레퍼러 URL과 일치하는 첫 번째 마스크는 마스크가 포함 마스크인 경우 검색을 허용할지 여부를 결정합니다. 또는 마스크가 제외 마스크인 경우 검색을 허용하지 않을지 여부를 결정합니다. 레퍼러 URL과 일치하는 마스크가 없는 경우 해당 URL이 포함되고 검색이 허용됩니다. </p> <p> 검색 템플릿에 새 검색 양식이 포함되어 있거나 검색 템플릿에 "다음 10", "이전 10" 또는 "요약 숨기기"와 같은 링크가 포함될 수 있는 경우 검색 결과 템플릿을 "포함" 마스크로 나열합니다. 다음 예제와 같이 정규 표현식을 사용하는 것이 가장 쉽습니다. </p> <p> <span class="codeph"> regexp ^https?://[^/]*\.atomz\.com/ 포함*[?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>다음 예에는 5개의 서로 다른 레퍼러 URL 마스크가 포함되어 있습니다. </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>레퍼러 URL 마스크가 다음과 같은 경우: </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>IP 주소 마스크 </p> </td> 
      <td colname="col2"> <p>마스크가 포함 마스크인 경우 IP 주소와 일치하는 첫 번째 마스크가 검색을 허용할지 여부를 결정합니다. 또는 마스크가 제외 마스크인 경우 검색을 허용할지 여부를 결정합니다. 요청하는 IP 주소와 일치하는 마스크가 없는 경우 해당 IP 주소가 포함되고 검색이 허용됩니다. </p> <p>다음 예는 네 개의 서로 다른 IP 주소 마스크를 보여줍니다. </p> <p> <code> include&nbsp;64.128.192.* 
          include&nbsp;192.168. 
          include&nbsp;regexp&nbsp;^209\.42\.97\.[1-5]+ 
          exclude&nbsp;* </code> </p> <p>참조 IP 주소 마스크가 다음과 같은 경우: </p> <p> <code> 64.128.192.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          192.168.10.127&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          209.42.97.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          64.128.193.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          192.169.10.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          209.42.97.68&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>HTTPS를 사용하는 검색만 허용 </p> </td> 
      <td colname="col2"> <p>검색을 HTTPS로 제한합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>허용되지 않은 요청을 보내야 하는 URL </p> </td> 
      <td colname="col2"> <p> 제한된 사용자는 여기에 입력한 URL로 리디렉션됩니다. 이 옵션은 사이트를 검색할 수 없는 고객에게 표시할 사용자 지정 오류 페이지를 만들 수 있는 방법을 제공합니다. </p> <p>URL 파섹 </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 미리 보기 정보 {#concept_DF293FD3B02C467F8842C8C21D62F294}

설정한 쿼리 문자열 및 매개 변수는 소프트웨어에서 검색 양식을 테스트하거나 미리 볼 때마다 [!DNL Preview] 사용됩니다.

<!-- 

c_about_preview.xml

 -->

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

## 미리 보기에서 값 설정 {#task_CE267A0FF621474E80AB43B67B1C28D7}

설정한 미리 보기 값은 소프트웨어에서 검색 양식을 테스트하거나 미리 볼 때마다 사용됩니다.

<!-- 

t_setting_values_in_preview.xml

 -->

**미리 보기에서 값을 설정하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Preview]**&#x200B;을 클릭합니다.
1. 페이지에서 원하는 옵션을 [!DNL Preview] 설정합니다.

   <!-- 
   
   r_preview_options.xml
   
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
      <td colname="col1"> <p>쿼리 </p> </td> 
      <td colname="col2"> <p>기본적으로 쿼리 문자열은 <span class="codeph"> *로 설정되며, 일반적으로 결과가 </span>반환됩니다. 그러나 웹 사이트의 컨텐츠에 보다 구체적인 쿼리를 지정할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>매개 변수 </p> </td> 
      <td colname="col2"> <p>매개 변수는 이름과 값으로 설정됩니다. 필요한 만큼 추가 매개 변수를 지정할 수 있습니다. 예를 들어 <span class="codeph"> sp_q_1 </span> 및 <span class="codeph"> sp_x_1 </span> 매개 변수를 사용하여 추가 검색 기준을 지정할 수 있습니다. 매개 변수 값 <span class="codeph"> sp_q_1=windows&amp;sp_x_1=platform은 기본 쿼리 외에 검색된 페이지의 "platform" 메타 태그에서 "windows" 값을 찾는 미리 보기 검색을 </span> 만듭니다. </p> <p>백엔드 <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> 검색 CGI 매개 변수를 참조하십시오 </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>호스트 </p> </td> 
      <td colname="col2"> <p>웹 사이트에서 개인 도메인 레이블을 사용하는 경우 올바른 호스트 이름을 설정하여 검색 결과를 정확하게 미리 볼 수 있습니다. </p> <p>개인 도메인 레이블에 대한 자세한 내용은 고객 지원에 문의하십시오. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. 클릭 **[!UICONTROL Save Changes]**.
1. (선택 사항) 다음 중 하나를 수행합니다.

   * 아이콘을 **[!UICONTROL History]** 클릭하여 변경한 내용을 되돌립니다.

      작업 [내역 옵션](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)사용을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      라이브 [설정](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)보기를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      스테이지 [설정 라이브를](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)참조하십시오.

## 피드 정보 {#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

검색 색인은 웹 사이트의 큰 데이터베이스로 표시됩니다. 올바른 메타 태그의 정보가 충분히 수집되어 구성되거나 신디케이트된 정보가 데이터 피드에 포함됩니다. 이러한 데이터 피드를 타사 수신자와 같은 다른 서비스에 제출할 수 있습니다.

<!-- 

c_about_feeds.xml

 -->

웹 사이트가 크롤링 및 인덱스화된 후 자동 피드를 생성하여 타사 유기적 검색 엔진 및 쇼핑 엔진에 제출할 수 있습니다. 다음 스트림 피드를 만들 수 있습니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>피드 유형 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Recommendations </p> </td> 
   <td colname="col2"> <p>Recommendations 피드는 Adobe Recommendations를 통해 데이터 신디케이션 기능을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일반 피드 </p> </td> 
   <td colname="col2"> <p>일반 피드 유형으로 여러 피드를 구현할 수 있습니다. 사용자 지정 검색 쿼리는 웹 사이트의 색인에 대해 수행됩니다. 데이터는 검색 결과를 표시하기 위해 동일한 템플릿 언어를 사용하여 사용자 지정된 검색 템플릿을 통해 반환됩니다. 이러한 유형의 유연성은 특정 피드 유형뿐만 아니라 더 많은 업체에 피드를 제출할 수 있음을 의미합니다. </p> <p>다음 도움말 항목의 지침에 따라 전송(검색) 템플릿을 추가할 수 있습니다. </p> <p>새 <a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local"> 프레젠테이션 또는 전송 템플릿 파일 추가를 </a>참조하십시오. </p> <p> 템플릿을 추가한 후 검색 템플릿 태그를 사용하여 편집하여 포함할 검색 메타데이터 필드를 형식과 함께 정의합니다. </p> <p>프레젠테이션 <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> 또는 전송 템플릿 편집을 </a>참조하십시오. </p> <p>템플릿 <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> 태그 검색을 참조하십시오 </a>. </p> <p>전송 템플릿 파일의 이름을 기억하는지 확인하십시오. 피드의 기준을 지정할 때 이 이름을 사용하여 일반 피드를 템플릿에 바인딩합니다. </p> <p>이전에 다른 피드와 작업한 경우 피드 필드를 검색 메타데이터 필드에 매핑해야 합니다. 일반 피드에는 피드 만들기 <span class="uicontrol"></span> 마법사에서 이 특정 단계가 없습니다. 대신 템플릿은 메타데이터와 메타데이터의 형식을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Google Merchant </p> </td> 
   <td colname="col2"> <p>구글 머천트 센터는 사람들이 몇몇 구글 서비스를 통해 제품을 팔 수 있도록 해줍니다. 정기적으로 판매 가능한 제품 목록을 제출할 수 있는 데이터 신디케이션 구성 요소가 있습니다. </p> <p>Google Merchant Center는 타사 피드 공급업체와 마찬가지로 피드가 합법적이라고 판단하기 전에 충족해야 하는 특정 표준을 가지고 있습니다. 자세한 내용은 고객 담당자에게 문의하고 Google Merchant 설명서를 참조하십시오. 다음은 Google Merchant Center에서 피드의 유효성을 검사하는 동안 고려해야 하는 간략한 요약입니다. </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">각 제품에는 제품 페이지가 있습니다.전용 URL입니다. </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> 각 제품 변형은 피드에 별도의 항목을 가집니다. </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> 각 제품에는 이미지 URL이 있으며, 특히 서버에서 온 것이 좋습니다. 제품 변형에는 실제 변형을 보여주는 특정 이미지가 있습니다. 즉, 다른 신발 색상이 같은 이미지를 공유하지 않아야 합니다. </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> 각 제품에는 가용성, 조건, 설명, 카테고리 및 가격과 같은 특정 정보가 있습니다. </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">일반적으로 각 제품에는 ISBN, UPC, JAN 또는 EAN 등의 고유 식별자가 있습니다. </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">일반적으로 각 제품은 Google의 제품 분류법으로 분류됩니다. </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> 의류 제품에는 성별, 연령 그룹, 색상 및 크기와 같은 추가 필수 필드가 있습니다. </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> 세금 및 배송은 이 피드 내에서 Google Merchant Center 내에서 또는 제품별로 계정 설정으로 지정됩니다. </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> 사용자 정의 제품 및 특정 의류 제품은 일부 규칙에서 제외될 수 있지만, 사용 권한 및 면제에 대한 자세한 내용은 Google에 문의해야 합니다. </li> 
    </ul> <p>피드 유효성 검사를 제어하는 여러 가지 세부 사항이 있습니다. 피드 관리에 대한 자세한 내용은 Google Merchant 설명서를 참조하십시오. Google은 사양을 자주 변경하므로 설명서를 자주 확인하십시오. </p> <p>Google Merchant Center와 연관된 피드를 Google 제품 검색 피드라고 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Google 사이트 맵 </p> </td> 
   <td colname="col2"> <p>Google 사이트 맵에서는 Google이 웹 사이트를 크롤하는 방식에 영향을 줄 수 있는 방법을 제공합니다. 이 경우 사이트 맵인 신디케이트된 데이터 피드가 Google 사이트 맵에 주기적으로 제출됩니다. 사이트 맵에는 인터넷에 연결할 수 있는 URL이 포함되어 있으며 마지막 수정 날짜 또는 페이지 우선 순위와 같은 특정 정보가 각 URL과 연결될 수 있습니다. 이러한 정보를 Google에 제공하면 특정 페이지가 크롤링 및 인덱싱될 수 있는 빈도 및 빈도를 높일 수 있습니다. 경우에 따라 사이트 맵은 정상적인 상황에서 크롤러가 액세스할 수 없는 링크 목록을 광고하는 데 사용됩니다. </p> <p>피드 기능을 사용하여 Google 사이트 맵을 만들려면 고객 담당자에게 문의하십시오. Google은 Google 사이트 맵 서비스를 일반 사용자가 사용할 수 있도록 만들었고 Google 웹 마스터 도구 페이지에서 설명서를 제공합니다. </p> <p> <b>Google 사이트 맵 피드 만들기 요구 사항</b> </p> <p>Google 사이트 맵 피드를 만들려면 Google 사이트 맵이 이미 설정된 Google 웹 마스터 도구 계정이 있어야 합니다. Google 사이트 맵을 설정하려면 Google 웹 마스터 도구 설명서를 참조하십시오. </p> <p>또한 사이트 맵 파일이 어떻게 배달되는지 확인해야 합니다. 일반적으로 사이트 맵 파일은 도메인과 웹 사이트의 루트에서 가져옵니다. 간단한 모델은 FTP를 통해 서버에 파일을 전달하는 것입니다. 다른 솔루션은 사이트 맵 파일의 요청을 사이트 검색/머천다이징 컨텐츠 네트워크로 리디렉션하는 것입니다. 사이트 맵 피드 배달을 조정하고 설정하는 방법은 컨설팅 담당자에게 문의하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

자동 피드에 관심이 있는 경우 전문 서비스에 문의하여 지원을 받으십시오. 각 피드에는 데이터 품질 및 파일 전송에 대한 엄격한 요구 사항이 있습니다.

선택하는 피드 유형은 **[!UICONTROL Create Feed]** 마법사를 사용하여 필드를 만들 때 표시되는 옵션에 영향을 줍니다. 각 유형의 피드는 데이터 형식이 다릅니다. 피드 수신자가 피드를 거부하거나 부적절한 데이터를 고객에게 게시하지 않도록 적절한 데이터 형식을 따라야 합니다. 데이터 형식 외에도 공급업체는 일반적으로 데이터를 받는 데 가장 선호하는 방법을 하나 이상 갖습니다. 해당 피드에 대한 공급업체의 설명서를 참조하십시오.

피드 만들기의 문제점은 사이트 검색/머천다이징과 피드 간의 데이터와 일치하는 것입니다. 일반적으로 인덱스 크롤링 시 검색되는 데이터의 형식이 잘못되었거나 없습니다. 다음은 피드를 만들 때 찾을 내용에 집중할 수 있는 질문 목록입니다.

* 피드 수신자와 어떤 유형의 비즈니스 관계를 가지고 있습니까?
* 피드 수신자와 계정을 등록하고 만들어야 합니까?
* 공급업체와 관련하여 피드와 관련된 문제를 누가 모니터링하고 관리할 것입니까? 일반적으로 공급업체의 계정을 관리하는 것은 사용자의 책임입니다. 예를 들어 Google 사이트 맵은 WebMaster 계정과 사이트 맵의 상태를 모니터링할 사람이 필요합니다.
* 피드의 데이터 형식은 무엇입니까?
* 인덱스가 피드의 문자 인코딩과 일치합니까? 탭으로 구분된 데이터 포맷과 쉼표로 구분된 데이터 포맷은 데이터에서 탭 또는 쉼표를 사용할 때 문제가 됩니다.
* 데이터에는 탭이나 쉼표가 있을 때 어떤 것이 있습니까?
* 색인에 빈 데이터가 있는 페이지가 있습니까?
* 피드 수신자가 빈 데이터를 허용할 수 있습니까? 소프트웨어에서 데이터를 검색하는 방법에 대한 기준을 편집하여 빈 데이터를 해결할 수 있습니다.
* 피드 수신자가 원하는 대로 데이터 형식 라인업이 제공됩니까? 예를 들어, 일부 피드 수신자는 가격과 통화가 표시되는 방식에 따라 다릅니다.
* 공급업체가 허용할 수 있는 최대 개수의 항목이 있습니까? 검색 조건으로 결과를 제한하여 이 잠재적 문제를 해결할 수 있습니다.
* 공급업체가 피드를 어떻게 수신하려고 합니까? FTP 제출 및 HTTP 호스팅이 지원됩니다.

## 피드 만들기 {#task_63179C1FC359497483CD6CE13FD1C250}

하나 이상의 데이터 피드를 만들 수 있습니다.

<!-- 

t_creating_a_feed.xml

 -->

**피드를 만들려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 [!DNL Feeds] 드롭다운 목록에서 피드 유형을 **[!UICONTROL Create Feed]** 선택합니다.
1. 선택한 피드 유형에 따라 [!DNL Create Feed] 대화 상자에서 마법사의 각 패널에 식별된 옵션을 설정합니다.

   <!-- 
   
   r_feed_options.xml
   
   -->

   만들거나 편집하는 피드 유형에 따라 사용 가능한 옵션이 약간 다릅니다.

   **Adobe Recommendations**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>패널 </p> </th> 
      <th colname="col2" class="entry"> <p>마법사 패널 이름 </p> </th> 
      <th colname="col3" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>피드 이름 </p> </td> 
      <td colname="col3"> <p>피드의 이름을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>필드 맵 </p> </td> 
      <td colname="col3"> <p>공급업체별 피드 필드를 사이트 검색/머천다이징 메타데이터 필드에 매핑할 수 있습니다. 이 매핑 단계에서는 피드가 인덱스의 필드와 피드 데이터의 필드 간의 정보를 상호 연관시킬 수 있으므로 중요합니다. 일반 피드를 제외한 대부분의 경우 <span class="wintitle"> 상관 관계는 동적으로 생성된 검색 </span>템플릿에 저장됩니다. </p> <p>필드 맵 <span class="wintitle"> 테이블의 각 행은 </span> 필드 매핑을 나타냅니다. 테이블의 추가/제거 열에서 <span class="uicontrol"> +를 </span> 클릭하여 새 필드 매핑 행을 추가합니다.을 <span class="uicontrol"> - </span> 클릭하여 표에서 현재 선택된 필드 매핑 행을 삭제합니다. 피드 필드를 사이트 검색/머천다이징 메타데이터 필드에 연결하려면 해당 드롭다운 목록을 사용하여 원하는 필드를 선택합니다. </p> <p> <b>Adobe Recommendations에 대한 필드 매핑</b> </p> <p>권장 사항 데이터 피드는 CSV 파일이며 데이터 열은 쉼표로 구분됩니다. 필드 맵 테이블의 각 매핑의 표시 순서는 CSV 피드 파일에서 열의 순서를 결정하므로 중요합니다. 다음 순서로 매핑 행을 만듭니다. 각 행은 필수입니다. </p> <p> 
        <ol id="ol_49C739D04DD340168DC6C1F794544C35"> 
          <li id="li_A95D9C5A353746A3A0D38F200AC2EEA2"> ID </li> 
          <li id="li_044763D4C7054CEB948C94590735D74F"> 이름 </li> 
          <li id="li_832F07CA0E3F4E10A4AE30171F3E8541"> categoryId </li> 
          <li id="li_2A33FB42F7E942ED881BA1F478542C4D"> message </li> 
          <li id="li_A76E66B2366845B0B63ED5C200531ADD"> thumbnailUrl </li> 
          <li id="li_518CCD5E7E404521AB8199981BA86F76"> value </li> 
          <li id="li_14A0A8FCC2B34B758E1FBB98E3F2DFB2"> pageUrl </li> 
          <li id="li_36D22F1603394AF89E0C7ADB18AAAAB7"> inventory </li> 
          <li id="li_ABDB9C762BBC4F27B82FEA4425A8DDC4"> margin </li> 
        </ol> </p> <p> <b>고급 사용</b> </p> <p>위에서 설명한 바와 같이 처음 9개의 필수 피드 필드를 매핑한 후에는 사용자 정의 필드를 직접 만들 수 있습니다. 피드 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 해당 필드의 사용자 지정 태그 이름을 입력합니다. 이 사용자 정의 옵션은 피드에 특정 공급업체별 필드가 필요한 경우에 유용합니다. </p> <p> <p>참고: 권장 사항 피드 사양은 각 필드 이름에 "entity"가 접두사로 붙어야 한다고 명시하지만 이 경우에는 필요하지 않습니다. </p> </p> <p>사용자 지정 메타데이터 필드를 만들 수도 있습니다. 메타데이터 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 사용자 지정 메타데이터 필드 값을 입력합니다. 이 값은 미리 생성된 템플릿에 삽입되며 사용자 지정 검색 템플릿 태그를 주입하는 데에도 사용할 수 있습니다. </p> <p>템플릿 <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> 태그 검색을 참조하십시오 </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>검색 기준 </p> </td> 
      <td colname="col3"> <p>피드 파일이 생성되면 검색 쿼리를 사용하여 데이터를 필터링합니다. 이 패널에서 검색 쿼리에 사용되는 필터를 정의합니다. </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> 메타 필드 </span> <p>필터링할 메타데이터 필드를 정의합니다. </p> <p> <b>고급 사용</b> </p> <p>필터링 시스템은 표준 검색 쿼리이므로 드롭다운 <span class="uicontrol"> 목록에서 [무료 양식] </span> 을 선택하여 CGI 검색 매개 변수와 값을 입력할 수 있습니다. URL escape가 필요합니다. 검색 인수 <span class="codeph"> sp_q는 </span> 무시됩니다. 여러 개의 자유 형식 텍스트 상자를 만들 수 있습니다. 각 행 사이에 있는 인수는 자동으로 &amp; 로 구분됩니다. </p> <p>CGI <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> 매개 변수 검색을 참조하십시오 </a>. </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> 기준 </span> <p>필터 작업을 정의합니다. 드롭다운 목록에서 선택하는 필터 작업은 세 번째 열에 입력된 상수 값을 적용합니다. </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> 값 </span> <p>상수 값입니다. </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> 작업 </span> <p>새 필드 매핑 행을 추가하거나 현재 강조 표시된 행을 삭제합니다. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>파일 제출 </p> </td> 
      <td colname="col3"> <p>피드 파일 제출 일정을 구성하고 파일 업로드에 사용할 방법을 설정할 수 있습니다. </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> 예약 </span> <p>피드가 제출되는 최대 빈도를 설정합니다. 피드를 <span class="uicontrol"> 선택하지 </span> 않으면 피드가 꺼집니다. 다른 값은 피드가 다시 제출하기 전에 기다리는 기간을 정의합니다. 피드를 제출할 때의 결정은 각 색인에서 수행됩니다. 즉, 색인 끝에서 피드가 만료되었는지 확인하고 공급업체에서 업데이트하고 제출해야 하는지 확인합니다. 또한, 계정이 공급업체에게 과도하게 제출되지 않도록 하는 방법으로 사용됩니다. 일부 벤더에는 너무 자주 업로드되는 데이터 피드 소스에 대한 정책이 있습니다. 제출 빈도에 대한 데이터 피드 공급업체의 정책을 확인하십시오. 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> 업로드 방법 </span> <p>대부분의 피드는 두 가지 방법으로 파일을 배포합니다.FTP 및 호스팅 컨텐트 네트워크를 참조하십시오. </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol"> FTP </span> <p>사이트 검색/머천다이징 서버는 수동 FTP를 사용합니다. </p> <p>FTP는 파일을 다른 서버로 푸시하는 유일한 방법입니다. </p> <p> <span class="uicontrol"> FTP 서버 </span> - FTP 서버의 이름을 지정합니다. 프로토콜 또는 이전 "ftp://"을 포함하지 마십시오. </p> <p> <span class="uicontrol"> FTP 사용자 이름 </span> - FTP 계정의 이름을 지정합니다. </p> <p> <span class="uicontrol"> FTP 암호 </span> - FTP 계정의 암호를 지정합니다. </p> <p> <span class="uicontrol"> FTP 파일 이름 </span> - 전송할 파일의 이름을 지정합니다. 이 이름은 피드가 여러 파일을 생성하는 경우 템플릿으로서, 일반적으로 이름 끝에 있는 확장자 전에 숫자가 증가합니다. 예:basename.xml, basename1.xml, basename2.xml, ...., basename-Nth.xml </p> <p> <span class="uicontrol"> FTP 디렉토리 </span> - 특정 디렉토리 경로가 필요한 경우 여기에 입력합니다. 경로에 파일 이름을 포함하지 마십시오. </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> 호스팅 컨텐츠 네트워크 </span> <p>컨텐트 네트워크는 사이트 검색/머천다이징의 웹 서버에서 파일을 제공하는 수단입니다. 피드의 수신자는 HTTP 요청을 사용하여 웹 서버에서 피드를 가져옵니다. 이 설정을 위한 유일한 정보는 컨텐츠 네트워크 <span class="uicontrol"> 파일 </span>이름입니다. 파일 이름은 제공되는 파일의 기본 이름입니다. 파일 이름 확장자가 있는 파일 이름만 사용합니다. 피드에 따라 파일 이름은 피드가 다음 형식으로 여러 파일을 생성할 수 있는 여러 파일의 템플릿입니다.basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml </p> <p>기본 파일 이름을 입력하고 피드가 성공적으로 저장되면 마법사의 [확인] 패널에 컨텐트 네트워크 파일의 URL이 표시됩니다. 피드가 성공적으로 처리된 후에 URL이 활성화됩니다. 공급업체는 이 URL에서 피드 데이터를 가져올 수 있습니다. 여러 파일은 동일한 URL 경로를 사용합니다. 그러나 열거형 체계에 따라 파일 이름을 바꾸거나 변경해야 합니다. </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>확인 </p> </td> 
      <td colname="col3"> <p>확인 <span class="wintitle"> 패널에 </span> 도달하면 해당 시점에 피드가 저장됩니다. 하지만 실제 피드 파일은 나중에 저장할 수 있습니다. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> 데이터 보기 </span> <p>링크를 클릭하여 테이블 양식에 표시되는 데이터 보기를 통해 피드 출력을 확인할 수 있습니다. 데이터 보기는 선택되는 메타 필드와 마법사의 검색 기준 패널에서 지정된 검색 기준을 표시하여 문제를 해결하는 데 도움이 <span class="wintitle"> 될 수 </span> 있습니다. 데이터 보기는 동적으로 생성되므로 항상 사용할 수 있습니다. </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> 피드 파일 </span> <p>사이트 검색/머천다이징 서버가 피드 파일을 생성한 후 피드 파일 <span class="uicontrol"></span> 드롭다운 목록을 사용하여 서버의 파일을 볼 수 있습니다. 새 브라우저 탭 또는 새 브라우저 창이 피드의 컨텐츠와 함께 나타납니다. 이 방법은 서식 문제가 있는 피드를 해결하는 데 유용합니다. 최종 대상 또는 공급업체 자체에서 파일을 볼 수 없습니다. </p> <p> 피드가 새로운 경우 피드 파일을 생성할 때까지 드롭다운 목록이 비어 있습니다. </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> 컨텐트 네트워크 링크 </span> <p>마법사의 파일 제출 <span class="uicontrol"> 패널에서 </span> 업로드 방법으로 호스팅된 컨텐트 네트워크를 선택한 <span class="wintitle"> 경우 URL이 </span> 여기에 표시됩니다. 피드 파일을 아직 생성하지 않은 경우 피드가 성공적으로 생성될 때까지 URL이 유효하지 않습니다. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **일반 피드**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>패널 </p> </th> 
      <th colname="col2" class="entry"> <p>마법사 패널 이름 </p> </th> 
      <th colname="col3" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>피드 이름 </p> </td> 
      <td colname="col3"> <p>피드의 이름을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>검색 기준 </p> </td> 
      <td colname="col3"> <p>피드 파일이 생성되면 검색 쿼리를 사용하여 데이터를 필터링합니다. 이 패널에서 검색 쿼리에 사용되는 필터를 정의합니다. </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> 메타 필드 </span> <p>필터링할 메타데이터 필드를 정의합니다. </p> <p> <b>고급 사용</b> </p> <p>필터링 시스템은 표준 검색 쿼리이므로 드롭다운 <span class="uicontrol"> 목록에서 [무료 양식] </span> 을 선택하여 CGI 검색 매개 변수와 값을 입력할 수 있습니다. URL escape가 필요합니다. 검색 인수 <span class="codeph"> sp_q는 </span> 무시됩니다. 여러 개의 자유 형식 텍스트 상자를 만들 수 있습니다. 각 행 사이에 있는 인수는 자동으로 &amp; 로 구분됩니다. </p> <p>CGI <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> 매개 변수 검색을 참조하십시오 </a>. </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> 기준 </span> <p>필터 작업을 정의합니다. 드롭다운 목록에서 선택하는 필터 작업은 세 번째 열에 입력된 상수 값을 적용합니다. </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> 값 </span> <p>상수 값입니다. </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> 작업 </span> <p>새 필드 매핑 행을 추가하거나 현재 강조 표시된 행을 삭제합니다. </p> </li> 
        </ul> <p>일반 피드에 특수 CGI 매개 변수가 지정되어 있어야 합니다. 이 피드와 연관된 특수 템플릿을 바인딩하려면 <span class="codeph"> sp_t </span> 매개 변수를 정의합니다. 전송 템플릿 파일의 이름으로 <span class="codeph"> sp_t </span> 값을 설정합니다. 예를 들어 <span class="codeph"> super_feed.tpl이라는 전송 템플릿 파일을 추가한 </span>경우 사용자 지정 CGI 검색 매개 변수를 <span class="codeph"> sp_t=super_feed로 </span>만듭니다. 메타 필드 <span class="codeph"> 드롭다운 목록에서 자유 양식을 선택해야 </span> sp_t를 입력하는 텍스트 상자가 나타납니다 <span class="uicontrol"> </span> <span class="wintitle"> </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>파일 제출 </p> </td> 
      <td colname="col3"> <p>피드 파일 제출 일정을 구성하고 파일 업로드에 사용할 방법을 설정할 수 있습니다. </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> 예약 </span> <p>피드가 제출되는 최대 빈도를 설정합니다. 피드를 <span class="uicontrol"> 선택하지 </span> 않으면 피드가 꺼집니다. 다른 값은 피드가 다시 제출하기 전에 기다리는 기간을 정의합니다. 피드를 제출할 때의 결정은 각 색인에서 수행됩니다. 즉, 색인 끝에서 피드가 만료되었는지 확인하고 공급업체에서 업데이트하고 제출해야 하는지 확인합니다. 또한, 계정이 공급업체에게 과도하게 제출되지 않도록 하는 방법으로 사용됩니다. 일부 벤더에는 너무 자주 업로드되는 데이터 피드 소스에 대한 정책이 있습니다. 제출 빈도에 대한 피드 공급업체의 정책을 확인하십시오. 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> 업로드 방법 </span> <p>대부분의 피드는 두 가지 방법으로 파일을 배포합니다.FTP 및 호스팅 컨텐트 네트워크를 참조하십시오. </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol"> FTP </span> <p>사이트 검색/머천다이징 서버는 수동 FTP를 사용합니다. </p> <p>FTP는 파일을 다른 서버로 푸시하는 유일한 방법입니다. </p> <p> <span class="uicontrol"> FTP 서버 </span> - FTP 서버의 이름을 지정합니다. 프로토콜 또는 이전 "ftp://"을 포함하지 마십시오. </p> <p> <span class="uicontrol"> FTP 사용자 이름 </span> - FTP 계정의 이름을 지정합니다. </p> <p> <span class="uicontrol"> FTP 암호 </span> - FTP 계정의 암호를 지정합니다. </p> <p> <span class="uicontrol"> FTP 파일 이름 </span> - 전송할 파일의 이름을 지정합니다. 이 이름은 피드가 여러 파일을 생성하는 경우 템플릿으로서, 일반적으로 이름 끝에 있는 확장자 앞에 숫자가 증가합니다. 예:basename.xml, basename1.xml, basename2.xml, ...., basename-Nth.xml </p> <p> <span class="uicontrol"> FTP 디렉토리 </span> - 특정 디렉토리 경로가 필요한 경우 여기에 입력합니다. 경로에 파일 이름을 포함하지 마십시오. </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> 호스팅 컨텐츠 네트워크 </span> <p>호스팅 컨텐트 네트워크는 사이트 검색/머천다이징의 웹 서버에서 파일을 제공하는 수단입니다. 피드의 수신자는 HTTP 요청을 사용하여 웹 서버에서 피드를 가져옵니다. 이 설정을 위한 유일한 정보는 컨텐츠 네트워크 <span class="uicontrol"> 파일 </span>이름입니다. 파일 이름은 제공되는 파일의 기본 이름입니다. 파일 이름 확장자가 있는 파일 이름만 사용합니다. 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>기본 파일 이름을 입력하고 피드가 성공적으로 저장되면 마법사의 [확인] 패널에 컨텐트 네트워크 파일의 URL이 표시됩니다. 피드가 성공적으로 처리된 후에 URL이 활성화됩니다. 공급업체는 이 URL에서 피드 데이터를 가져올 수 있습니다. </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>탭을 유지하시겠습니까?</b> </p> <p>피드에서 탭 문자를 유지합니다. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>확인 </p> </td> 
      <td colname="col3"> <p>확인 <span class="wintitle"> 패널에 </span> 도달하면 해당 시점에 피드가 저장됩니다. 하지만 실제 피드 파일은 나중에 저장할 수 있습니다. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> 데이터 보기 </span> <p>링크를 클릭하여 테이블 양식에 표시되는 데이터 보기를 통해 피드 출력을 확인할 수 있습니다. 데이터 보기는 선택되는 메타 필드와 마법사의 검색 기준 패널에서 지정된 검색 기준을 표시하여 문제를 해결하는 데 도움이 <span class="wintitle"> 될 수 </span> 있습니다. 데이터 보기는 동적으로 생성되므로 항상 사용할 수 있습니다. </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> 피드 파일 </span> <p>사이트 검색/머천다이징 서버가 피드 파일을 생성한 후 피드 파일 <span class="uicontrol"></span> 드롭다운 목록을 사용하여 서버의 파일을 볼 수 있습니다. 새 브라우저 탭 또는 새 브라우저 창이 피드의 컨텐츠와 함께 나타납니다. 이 방법은 서식 문제가 있는 피드를 해결하는 데 유용합니다. 최종 대상 또는 공급업체 자체에서 파일을 볼 수 없습니다. </p> <p> 피드가 새로운 경우 피드 파일을 생성할 때까지 드롭다운 목록이 비어 있습니다. </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> 컨텐트 네트워크 링크 </span> <p>마법사의 파일 제출 <span class="uicontrol"> 패널에서 </span> 업로드 방법으로 호스팅된 컨텐트 네트워크를 선택한 <span class="wintitle"> 경우 URL이 </span> 여기에 표시됩니다. 피드 파일을 아직 생성하지 않은 경우 피드가 성공적으로 생성될 때까지 URL이 유효하지 않습니다. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Google Merchant Center**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>패널 </p> </th> 
      <th colname="col2" class="entry"> <p>마법사 패널 이름 </p> </th> 
      <th colname="col3" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>피드 이름 </p> </td> 
      <td colname="col3"> <p>피드의 이름을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>필드 맵 </p> </td> 
      <td colname="col3"> <p>공급업체별 피드 필드를 사이트 검색/머천다이징 메타데이터 필드에 매핑할 수 있습니다. 이 매핑 단계에서는 피드가 인덱스의 필드와 피드 데이터의 필드 간의 정보를 상호 연관시킬 수 있으므로 중요합니다. 일반 피드를 제외한 대부분의 경우 <span class="wintitle"> 상관 관계는 동적으로 생성된 검색 </span>템플릿에 저장됩니다. </p> <p>필드 맵 테이블의 각 행은 필드 매핑을 나타냅니다. 테이블의 <span class="wintitle"> 추가/제거 </span> 열에서 <span class="uicontrol"> </span> +를 클릭하여 새 필드 매핑 행을 추가합니다.을 <span class="uicontrol"> - </span> 클릭하여 표에서 현재 선택된 필드 매핑 행을 삭제합니다. 피드 필드를 사이트 검색/머천다이징 메타데이터 필드에 연결하려면 해당 드롭다운 목록을 사용하여 원하는 필드를 선택합니다. </p> <p> <b>고급 사용</b> </p> <p>사용자 정의 필드를 직접 만들 수 있습니다. 피드 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 해당 필드의 사용자 지정 태그 이름을 입력합니다. 이 사용자 정의 옵션은 피드에 특정 공급업체별 필드가 필요한 경우에 유용합니다. </p> <p>사용자 지정 메타데이터 필드를 만들 수도 있습니다. 메타데이터 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 사용자 지정 메타데이터 필드 값을 입력합니다. 이 값은 미리 생성된 템플릿에 삽입되며 사용자 지정 검색 템플릿 태그를 주입하는 데에도 사용할 수 있습니다. </p> <p>템플릿 <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> 태그 검색을 참조하십시오 </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>검색 기준 </p> </td> 
      <td colname="col3"> <p>피드 파일이 생성되면 검색 쿼리를 사용하여 데이터를 필터링합니다. 이 패널에서 검색 쿼리에 사용되는 필터를 정의합니다. </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> 메타 필드 </span> <p>필터링할 메타데이터 필드를 정의합니다. </p> <p> <b>고급 사용</b> </p> <p>필터링 시스템은 표준 검색 쿼리이므로 드롭다운 <span class="uicontrol"> 목록에서 [무료 양식] </span> 을 선택하여 CGI 검색 매개 변수와 값을 입력할 수 있습니다. URL escape가 필요합니다. 검색 인수 <span class="codeph"> sp_q는 </span> 무시됩니다. 여러 개의 자유 형식 텍스트 상자를 만들 수 있습니다. 각 행 사이에 있는 인수는 자동으로 &amp; 로 구분됩니다. </p> <p>CGI <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> 매개 변수 검색을 참조하십시오 </a>. </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> 기준 </span> <p>필터 작업을 정의합니다. 드롭다운 목록에서 선택하는 필터 작업은 세 번째 열에 입력된 상수 값을 적용합니다. </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> 값 </span> <p>상수 값입니다. </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> 작업 </span> <p>새 필드 매핑 행을 추가하거나 현재 강조 표시된 행을 삭제합니다. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>파일 제출 </p> </td> 
      <td colname="col3"> <p>피드 파일 제출 일정을 구성하고 파일 업로드에 사용할 방법을 설정할 수 있습니다. </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> 예약 </span> <p>피드가 제출되는 최대 빈도를 설정합니다. 피드를 <span class="uicontrol"> 선택하지 </span> 않으면 피드가 꺼집니다. 다른 값은 피드가 다시 제출하기 전에 기다리는 기간을 정의합니다. 피드를 제출할 때의 결정은 각 색인에서 수행됩니다. 즉, 색인 끝에서 피드가 만료되었는지 확인하고 공급업체에서 업데이트하고 제출해야 하는지 확인합니다. 또한, 계정이 공급업체에게 과도하게 제출되지 않도록 하는 방법으로 사용됩니다. 일부 벤더에는 너무 자주 업로드되는 데이터 피드 소스에 대한 정책이 있습니다. 제출 빈도에 대한 피드 공급업체의 정책을 확인하십시오. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> 업로드 방법 </span> <p>대부분의 피드는 두 가지 방법으로 파일을 배포합니다.FTP 및 호스팅 컨텐트 네트워크를 참조하십시오. </p> <p>데이터 피드 제출을 위한 권장 업로드 방법은 FTP <span class="uicontrol"> 입니다 </span>. Google Merchant Center는 이러한 목적으로 FTP 서버를 호스팅합니다. 이 Google 제품 검색 피드에 대해 별도의 Google FTP 계정을 설정하는 방법은 Google Merchant Center 도움말을 참조하십시오. </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol"> FTP </span> <p>사이트 검색/머천다이징 서버는 수동 FTP를 사용합니다. </p> <p>FTP는 파일을 다른 서버로 푸시하는 유일한 방법입니다. </p> <p> <span class="uicontrol"> FTP 서버 </span> - FTP 서버의 이름을 지정합니다. 이 경우 
            <userinput>
              uploads.google.com 
            </userinput>. 프로토콜 또는 이전 "ftp://"을 포함하지 마십시오. </p> <p> <span class="uicontrol"> FTP 사용자 이름 </span> - FTP 계정의 이름을 지정합니다. </p> <p> <span class="uicontrol"> FTP 암호 </span> - FTP 계정의 암호를 지정합니다. </p> <p> <span class="uicontrol"> FTP 파일 이름 </span> - 전송할 파일의 이름을 지정합니다. 이 이름은 피드가 여러 파일을 생성하는 경우 템플릿으로서, 일반적으로 이름 끝에 있는 확장자 앞에 숫자가 증가합니다. 예:basename.xml, basename1.xml, basename2.xml, ...., basename-Nth.xml </p> <p> <span class="uicontrol"> FTP 디렉토리 </span> - 특정 디렉토리 경로가 필요한 경우 여기에 입력합니다. 경로에 파일 이름을 포함하지 마십시오. </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> 호스팅 컨텐츠 네트워크 </span> <p>컨텐트 네트워크는 사이트 검색/머천다이징의 웹 서버에서 파일을 제공하는 수단입니다. 피드의 수신자는 HTTP 요청을 사용하여 웹 서버에서 피드를 가져옵니다. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>확인 </p> </td> 
      <td colname="col3"> <p>확인 <span class="wintitle"> 패널에 </span> 도달하면 해당 시점에 피드가 저장됩니다. 하지만 실제 피드 파일은 나중에 저장할 수 있습니다. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> 데이터 보기 </span> <p>링크를 클릭하여 테이블 양식에 표시되는 데이터 보기를 통해 피드 출력을 확인할 수 있습니다. 데이터 보기는 선택되는 메타 필드와 마법사의 검색 기준 패널에서 지정된 검색 기준을 표시하여 문제를 해결하는 데 도움이 <span class="wintitle"> 될 수 </span> 있습니다. 데이터 보기는 동적으로 생성되므로 항상 사용할 수 있습니다. </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> 피드 파일 </span> <p>사이트 검색/머천다이징 서버가 피드 파일을 생성한 후 피드 파일 <span class="uicontrol"></span> 드롭다운 목록을 사용하여 서버의 파일을 볼 수 있습니다. 새 브라우저 탭 또는 새 브라우저 창이 피드의 컨텐츠와 함께 나타납니다. 이 방법은 서식 문제가 있는 피드를 해결하는 데 유용합니다. 최종 대상 또는 공급업체 자체에서 파일을 볼 수 없습니다. </p> <p> 피드가 새로운 경우 피드 파일을 생성할 때까지 드롭다운 목록이 비어 있습니다. </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> 컨텐트 네트워크 링크 </span> <p>마법사의 파일 제출 <span class="uicontrol"> 패널에서 </span> 업로드 방법으로 호스팅된 컨텐트 네트워크를 선택한 <span class="wintitle"> 경우 URL이 </span> 여기에 표시됩니다. 피드 파일을 아직 생성하지 않은 경우 피드가 성공적으로 생성될 때까지 URL이 유효하지 않습니다. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Google 사이트 맵**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>패널 </p> </th> 
      <th colname="col2" class="entry"> <p>마법사 패널 이름 </p> </th> 
      <th colname="col3" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>피드 이름 </p> </td> 
      <td colname="col3"> <p>피드의 이름을 지정합니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>필드 맵 </p> </td> 
      <td colname="col3"> <p>공급업체별 피드 필드를 사이트 검색/머천다이징 메타데이터 필드에 매핑할 수 있습니다. 이 매핑 단계에서는 피드가 인덱스의 필드와 피드 데이터의 필드 간의 정보를 상호 연관시킬 수 있으므로 중요합니다. 일반 피드를 제외한 대부분의 경우 <span class="wintitle"> 상관 관계는 동적으로 생성된 검색 </span>템플릿에 저장됩니다. </p> <p>필드 맵 테이블의 각 행은 필드 매핑을 나타냅니다. 테이블의 추가/제거 열에서 <span class="uicontrol"> +를 </span> 클릭하여 새 필드 매핑 행을 추가합니다.을 <span class="uicontrol"> - </span> 클릭하여 표에서 현재 선택된 필드 매핑 행을 삭제합니다. 피드 필드를 메타데이터 필드에 연결하려면 해당 드롭다운 목록을 사용하여 원하는 필드를 선택합니다. </p> <p> <b>고급 사용</b> </p> <p>사용자 정의 필드를 직접 만들 수 있습니다. 피드 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 해당 필드의 사용자 지정 태그 이름을 입력합니다. 이 사용자 정의 옵션은 피드에 특정 공급업체별 필드가 필요한 경우에 유용합니다. </p> <p>사용자 지정 메타데이터 필드를 만들 수도 있습니다. 메타데이터 <span class="wintitle"> 필드 </span> 드롭다운 목록에서 사용자 지정을 <span class="uicontrol"> 클릭합니다 </span>. 연결된 텍스트 필드에 사용자 지정 메타데이터 필드 값을 입력합니다. 이 값은 미리 생성된 템플릿에 삽입되며 사용자 지정 검색 템플릿 태그를 주입하는 데에도 사용할 수 있습니다. </p> <p>템플릿 <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> 태그 검색을 참조하십시오 </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>검색 기준 </p> </td> 
      <td colname="col3"> <p>피드 파일이 생성되면 검색 쿼리를 사용하여 데이터를 필터링합니다. 이 패널에서 검색 쿼리에 사용되는 필터를 정의합니다. </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> 메타 필드 </span> <p>필터링할 메타데이터 필드를 정의합니다. </p> <p> <b>고급 사용</b> </p> <p>필터링 시스템은 표준 검색 쿼리이므로 드롭다운 <span class="uicontrol"> 목록에서 [무료 양식] </span> 을 선택하여 CGI 검색 매개 변수와 값을 입력할 수 있습니다. URL escape가 필요합니다. 검색 인수 <span class="codeph"> sp_q는 </span> 무시됩니다. 여러 개의 자유 형식 텍스트 상자를 만들 수 있습니다. 각 행 사이에 있는 인수는 자동으로 &amp; 로 구분됩니다. </p> <p>CGI <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> 매개 변수 검색을 참조하십시오 </a>. </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> 기준 </span> <p>필터 작업을 정의합니다. 드롭다운 목록에서 선택하는 필터 작업은 세 번째 열에 입력된 상수 값을 적용합니다. </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> 값 </span> <p>상수 값입니다. </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> 작업 </span> <p>새 필드 매핑 행을 추가하거나 현재 강조 표시된 행을 삭제합니다. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>파일 제출 </p> </td> 
      <td colname="col3"> <p>피드 파일 제출 일정을 구성하고 파일 업로드에 사용할 방법을 설정할 수 있습니다. </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> 예약 </span> <p>피드가 제출되는 최대 빈도를 설정합니다. 피드를 <span class="uicontrol"> 선택하지 </span> 않으면 피드가 꺼집니다. 다른 값은 피드가 다시 제출하기 전에 기다리는 기간을 정의합니다. 피드를 제출할 때의 결정은 각 색인에서 수행됩니다. 즉, 색인 끝에서 피드가 만료되었는지 확인하고 공급업체에서 업데이트하고 제출해야 하는지 확인합니다. 또한, 계정이 공급업체에게 과도하게 제출되지 않도록 하는 방법으로 사용됩니다. 일부 벤더에는 너무 자주 업로드되는 데이터 피드 소스에 대한 정책이 있습니다. 제출 빈도에 대한 피드 공급업체의 정책을 확인하십시오. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> 업로드 방법 </span> <p>대부분의 피드는 두 가지 방법으로 파일을 배포합니다.FTP 및 호스팅 컨텐트 네트워크를 참조하십시오. </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol"> FTP </span> <p>사이트 검색/머천다이징 서버는 수동 FTP를 사용합니다. </p> <p>FTP는 파일을 다른 서버로 푸시하는 유일한 방법입니다. </p> <p> <span class="uicontrol"> FTP 서버 </span> - FTP 서버의 이름을 지정합니다. 프로토콜 또는 이전 "ftp://"을 포함하지 마십시오. </p> <p> <span class="uicontrol"> FTP 사용자 이름 </span> - FTP 계정의 이름을 지정합니다. </p> <p> <span class="uicontrol"> FTP 암호 </span> - FTP 계정의 암호를 지정합니다. </p> <p> <span class="uicontrol"> FTP 파일 이름 </span> - 전송할 파일의 이름을 지정합니다. 이 이름은 피드가 여러 파일을 생성하는 경우 템플릿으로서, 일반적으로 이름 끝에 있는 확장자 전에 숫자가 증가합니다. 예:basename.xml, basename1.xml, basename2.xml, ...., basename-Nth.xml </p> <p> <span class="uicontrol"> FTP 디렉토리 </span> - 특정 디렉토리 경로가 필요한 경우 여기에 입력합니다. 경로에 파일 이름을 포함하지 마십시오. </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> 호스팅 컨텐츠 네트워크 </span> <p>컨텐트 네트워크는 사이트 검색/머천다이징의 웹 서버에서 파일을 제공하는 방법입니다. 피드의 수신자는 HTTP 요청을 사용하여 웹 서버에서 피드를 가져옵니다. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>업로드 방법 중 하나를 사용하려면 Google이 사이트 맵을 검색하는 데 사용하는 URL을 기본 사이트 맵 URL <span class="wintitle"></span> 필드에 지정해야 합니다. 사이트 맵 파일의 이름도 여기에서 결정됩니다. 사이트 맵이 큰 경우 여러 파일이 존재할 수 있으며 이름 지정 규칙은 파일 끝에 숫자 1로 시작하는 인덱스 번호를 첨부하는 것입니다. sitemap.xml, sitemap1.xml, <span class="codeph"> sitemap2.xml </span>등과 같이 첫 번째 파일 또는 인덱스 파일에 인덱스가 없습니다 <span class="codeph"> . </span><span class="codeph"> </span> .sitemap <span class="codeph"> 12.xml </span>. </p> <p>업로드 <span class="uicontrol"> 방법으로 호스트 컨텐트 네트워크를 선택한 </span> 경우 파일의 URL은 동일한 파일 이름을 가지지만 URL에는 호스팅 서비스의 경로와 호스트 이름이 있습니다. 따라서 사이트 맵에 대한 요청을 호스팅 컨텐츠 네트워크로 리디렉션합니다. 동일한 위치에서 파일을 가져올 수도 있습니다. </p> <p>피드 파일을 만들어 중간 대상에 제출하면 Google이 ping되어 사이트 맵 피드가 준비되었음을 알려줍니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>확인 </p> </td> 
      <td colname="col3"> <p>확인 <span class="wintitle"> 패널에 </span> 도달하면 해당 시점에 피드가 저장됩니다. 하지만 실제 피드 파일은 나중에 저장할 수 있습니다. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> 데이터 보기 </span> <p>링크를 클릭하여 테이블 양식에 표시되는 데이터 보기를 통해 피드 출력을 확인할 수 있습니다. 데이터 보기는 선택되는 메타 필드와 마법사의 검색 기준 패널에서 지정된 검색 기준을 표시하여 문제를 해결하는 데 도움이 <span class="wintitle"> 될 수 </span> 있습니다. 데이터 보기는 동적으로 생성되므로 항상 사용할 수 있습니다. </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> 피드 파일 </span> <p>피드 파일이 생성되면 피드 파일 <span class="uicontrol"> 드롭다운 </span> 목록을 사용하여 서버의 파일을 볼 수 있습니다. 새 브라우저 탭 또는 새 브라우저 창이 피드의 컨텐츠와 함께 나타납니다. 이 방법은 서식 문제가 있는 피드를 해결하는 데 유용합니다. 최종 대상 또는 공급업체 자체에서 파일을 볼 수 없습니다. </p> <p> 피드가 새로운 경우 피드 파일을 생성할 때까지 드롭다운 목록이 비어 있습니다. </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> 컨텐트 네트워크 링크 </span> <p>마법사의 파일 제출 <span class="uicontrol"> 패널에서 </span> 업로드 방법으로 호스팅된 컨텐트 네트워크를 선택한 <span class="wintitle"> 경우 URL이 </span> 여기에 표시됩니다. 피드 파일을 아직 생성하지 않은 경우 피드가 성공적으로 생성될 때까지 URL이 유효하지 않습니다. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. 마법사의 단계를 완료하면 을 **[!UICONTROL Close]**&#x200B;클릭합니다.

## 피드 편집 {#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

기존 피드의 구성을 편집할 수 있습니다.

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>피드를 편집할 때는 피드 유형을 변경할 수 없습니다. 피드 유형을 변경해야 하는 경우 기존 피드를 삭제한 다음 원하는 유형의 새 피드를 추가합니다.

피드 [삭제를](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269)참조하십시오.

**피드를 편집하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 다음 중 하나를 수행하십시오.

* 페이지의 표 [!DNL Feeds] 열에서 피드 이름 옆에 있는 드롭다운 목록을 클릭한 다음 을 [!DNL Name] **[!UICONTROL Edit feed]**&#x200B;클릭합니다.

* 페이지의 [!DNL Feeds] 열에서 [!DNL Name] 변경할 피드의 이름을 클릭합니다.

1. 피드의 마법사에서 마법사의 각 패널에 대해 원하는 옵션을 설정합니다.

   피드 ****&#x200B;추가 아래의 옵션 표를 참조하십시오.
1. 마법사의 끝에서 [!DNL Verification] 패널에서 을 클릭합니다 **[!UICONTROL Close]**.

## 피드 삭제 {#task_7E39A140E69D43C6B61FB42E81051269}

더 이상 필요하거나 사용하지 않는 피드를 삭제할 수 있습니다.

<!-- 

t_deleting_a_feed.xml

 -->

**피드를 삭제하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 화면의 [!DNL Feeds Menu] 열에서 제거할 피드 [!DNL Actions] **[!UICONTROL Delete]** 이름을 클릭합니다.
1. 대화 [!DNL Delete feed] 상자에서 을 클릭하여 삭제를 **[!UICONTROL Yes]** 확인합니다.

## 피드 파일 보기 {#task_1E413C7650DE466EA68925F72E086884}

피드 마법사의 마지막 패널에서 피드 데이터 보기를 빠르게 보거나 서버에서 현재 피드 파일을 다운로드할 수 있습니다. 이 기능은 피드 출력을 확인하고 검사하려는 경우 유용합니다.

<!-- 

t_viewing_feed_files.xml

 -->

**피드 파일을 보려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 표 [!DNL Feeds] 열에서 피드 이름 옆에 있는 드롭다운 목록을 클릭한 다음 을 [!DNL Name] **[!UICONTROL View Feed Files]**&#x200B;클릭합니다.
1. 피드 마법사의 [!DNL Verification] 패널에서 을 클릭합니다 **[!UICONTROL Show Data View]**.
1. 클릭 **[!UICONTROL Close]**.

## 파일 업로드 없이 피드 테스트 {#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

최종 대상에 파일을 업로드하지 않고도 피드를 테스트할 수 있습니다.

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**파일 업로드 없이 피드를 테스트하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 표 [!DNL Feeds] 열에서 피드 이름 옆에 있는 드롭다운 목록을 클릭한 다음 을 [!DNL Name] **[!UICONTROL Test Feed (No file upload)]**&#x200B;클릭합니다.
1. 페이지에서 [!DNL Feeds] 테스트 도중 및 다음 [!DNL Feed Status] 열이 업데이트됩니다.

## 피드 생성 및 업로드 {#task_C9A57827C7674035B62A22D310DDAA0C}

피드 마법사의 [!DNL File Submission] 패널에서 설정한 일정에 관계없이 피드 파일을 수동으로 생성하여 최종 대상에 제출할 수 있습니다.

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

피드 [만들기를](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250)참조하십시오.

**피드를 생성하고 업로드하려면**

1. 제품 메뉴에서 > **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**&#x200B;을 클릭합니다.
1. 페이지의 표 [!DNL Feeds] 열에서 피드 이름 옆에 있는 드롭다운 목록을 클릭한 다음 을 [!DNL Name] **[!UICONTROL Generate and Upload Feed]**&#x200B;클릭합니다.
1. 페이지에서 [!DNL Feeds] 데이터 피드 생성 및 업로드 도중 및 다음에 [!DNL Feed Status] 열이 업데이트됩니다.
