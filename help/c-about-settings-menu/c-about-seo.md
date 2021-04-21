---
description: SEO(검색 엔진 최적화) 메타 태그를 사용하여 페이지의 특정 요소를 조정하고 검색 엔진 배치를 개선할 수 있습니다.
solution: Target
subtopic: SEO
title: SEO 정보
topic-legacy: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
exl-id: 0045455b-cb86-4820-82fa-753475ab6ca6
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 1%

---

# SEO 정보{#about-seo}

SEO(검색 엔진 최적화) 메타 태그를 사용하여 페이지의 특정 요소를 조정하고 검색 엔진 배치를 개선할 수 있습니다.

## SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B} 사용

시작 텍스트 뒤에 단어 목록이 오는 각 요소를 정의할 수 있습니다. 단어 목록은 다음을 포함할 수 있습니다.

* 선택한 기간 동안(예: &quot;지난 달&quot;) 사이트에서 자주 사용되는 검색 구문은 사용자 지정 제외에 따라 다릅니다.
* 페이지에서 가져온 검색에서 하나 이상의 필드의 값 세트입니다.
* 목록에서 정의하는 정적 단어 및 구문

사람들이 SEO에 사용하는 가장 일반적인 페이지 요소는 페이지 제목과 &quot;keywords&quot; 및 &quot;description&quot; 메타 태그입니다. 이러한 3개의 페이지 요소에 대한 설정을 정의할 수 있습니다. 또한 3가지 유형의 각 페이지에 대해 다음 3가지 설정을 정의할 수 있습니다.검색 결과 페이지, 검색 페이지 및 항목 세부 사항 페이지.

SEO 설정을 저장하거나 미리 보면 `<search-include>` 템플릿 태그를 사용하여 다른 검색 템플릿에 포함할 수 있는 작은 검색(전송) 템플릿 세그먼트가 생성됩니다. 예를 들어 검색 결과 페이지 제목 필드를 다음과 같은 다른 템플릿에 포함할 수 있습니다.

```
<search-include file="seo/seo_search_title.tpl" />
```

SEO 필드에 대한 `<search-include>` 태그의 `file` 속성에 대해 가능한 9개의 값은 다음과 같습니다.

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

프레젠테이션 템플릿의 SEO 필드를 사용하려면 몇 가지 단계를 완료해야 합니다.

먼저 위에 설명된 대로 `<search-include>`을 사용하여 `<general>` 요소 내의 XML 검색 템플릿에 원하는 필드를 포함할 수 있습니다.

그런 다음 각 `<search-include>` 태그를 `<general-field>` 및 `</general-field>` 태그로 둘러싸서 다음 예제와 같이 `name` 속성에 필드 이름을 지정합니다.

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

그런 다음 프레젠테이션 템플릿에서 `<guided-general-field>` 태그를 사용하여 다음 예제와 같이 필요한 곳에 지정된 필드를 삽입할 수 있습니다.

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

`gsname` 속성을 사용하여 &quot;기본&quot; 검색을 지정합니다.

웹 페이지에서 사용할 수 있는 9개의 서로 다른 SEO 필드를 정의할 수 있습니다. 여기에는 다음이 포함됩니다.

* 검색 결과 페이지 - 제목, 설명 및 키워드
* 검색 페이지 - 제목, 설명 및 키워드
* 항목 세부 정보 페이지 - 제목, 설명 및 키워드

9개 필드는 모두 비슷한 설정으로 정의됩니다. 실제로 &quot;검색 결과 페이지&quot;의 &quot;제목&quot; 필드와 같은 9개 필드의 이름은 이러한 필드를 사용하는 방법에 대한 제안일 뿐입니다. 프레젠테이션 템플릿 및 검색 템플릿의 모든 컨텍스트에서 필드를 사용할 수 있습니다.

[템플릿 정보](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5)도 참조하십시오.

[프레젠테이션 템플릿 태그](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)도 참조하십시오.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)도 참조하십시오.

[검색 결과 단어 목록 구성](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4)을 참조하십시오.

## 검색 결과 단어 목록 구성 중 {#task_A459A3734EC04042BA52C81184251DD4}

페이지 제목, 설명 및 키워드에 포함된 검색 결과 단어 및 구문 목록을 구성할 수 있습니다.

**검색 결과 단어 목록을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**&#x200B;를 클릭합니다.
1. [!DNL SEO Browse Pages Word List] 페이지의 각 [!DNL Title], [!DNL Description] 및 [!DNL Keywords] 그룹에서 원하는 옵션을 설정합니다.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>옵션 </p> </th> 
      <th colname="col2" class="entry"> <p>설명 </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>제목 | 설명 | 키워드 시작 </p> </td> 
      <td colname="col2"> <p>단어 목록 앞에 표시할 텍스트입니다. </p> <p>예를 들어 키워드 목록을 "브랜드"라는 단어로 시작할 수 있습니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다음 기간 동안 인기 검색어 포함 </p> </td> 
      <td colname="col2"> <p>검색이 포함된 기간입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>최대 검색 수 </p> </td> 
      <td colname="col2"> <p>포함된 최대 검색 수입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>필드 값 포함 </p> </td> 
      <td colname="col2"> <p>결과 단어 목록에 포함된 필드 값입니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>단어 및 구문 추가 </p> </td> 
      <td colname="col2"> <p>검색 결과 페이지 제목, 검색 페이지 제목 또는 항목 세부 사항 페이지 제목에 추가할 단어를 나열합니다. </p> <p>목록에 단어를 추가하려면 <b>편집</b>을 클릭합니다. </p> <p>한 줄에 단어나 구를 추가할 수 있습니다. 완료되면 <b>변경 내용 저장</b>을 클릭한 다음 페이지를 닫고 기본 SEO 페이지로 돌아갑니다. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>다음 단어 및 구문 제거(포함된 필드 값 제외) </p> </td> 
      <td colname="col2"> <p>검색 결과 페이지 제목, 검색 페이지 제목 또는 항목 세부 사항 페이지 제목에서 제거할 단어를 나열합니다. </p> <p><b>편집</b>을 클릭하여 제거 목록에 단어를 추가합니다. </p> <p>한 줄에 단어나 구를 추가할 수 있습니다. 완료되면 <b>변경 내용 저장</b>을 클릭한 다음 페이지를 닫고 기본 SEO 페이지로 돌아갑니다. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (선택 사항) 설정한 SEO 필드의 결과 값을 미리 보려면 **샘플 출력 미리 보기**&#x200B;를 클릭합니다.

   [구성한 SEO 메타 태그 미리 보기를 참조하십시오](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL SEO Search Results Word List] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 검색 페이지 단어 목록 구성 {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

페이지 제목, 설명 및 키워드에 포함된 검색 페이지 단어 및 구문 목록을 구성할 수 있습니다.

**검색 페이지 단어 목록을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**&#x200B;를 클릭합니다.
1. [!DNL SEO Browse Pages Word List] 페이지의 각 [!DNL Title], [!DNL Description] 및 [!DNL Keywords] 그룹에서 원하는 옵션을 설정합니다.

   [검색 결과 단어 목록 구성](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4) 아래의 옵션 표를 참조하십시오.
1. (선택 사항) 설정한 SEO 필드의 결과 값을 미리 보려면 **샘플 출력 미리 보기**&#x200B;를 클릭합니다.

   [구성한 SEO 메타 태그 미리 보기를 참조하십시오](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL SEO Browse Pages Word List] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## 항목 세부 정보 단어 목록 구성 {#task_761538C519B34164BE189F13C39B2495}

페이지 제목, 설명 및 키워드에 포함된 항목 세부 단어 및 구문 목록을 구성할 수 있습니다.

**항목 세부 정보 단어 목록을 구성하려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**&#x200B;를 클릭합니다.
1. [!DNL SEO Item Detail Word List] 페이지의 각 [!DNL Title], [!DNL Description] 및 [!DNL Keywords] 그룹에서 원하는 옵션을 설정합니다.

   [검색 결과 단어 목록 구성](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4) 아래의 옵션 표를 참조하십시오.
1. (선택 사항) 설정한 SEO 필드의 결과 값을 미리 보려면 **샘플 출력 미리 보기**&#x200B;를 클릭합니다.

   [구성한 SEO 메타 태그 미리 보기를 참조하십시오](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. **변경 내용 저장**&#x200B;을 클릭합니다.
1. (선택 사항) 결과를 미리 보려는 경우 스테이지된 사이트 인덱스를 다시 작성합니다.

   스테이지된 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)의 증분 인덱스 구성을 참조하십시오.[
1. (선택 사항) [!DNL SEO Item Detail Word List] 페이지에서 다음 중 하나를 수행합니다.

   * **[!UICONTROL History]**&#x200B;을 클릭하여 변경한 내용을 되돌립니다.

      [작업 내역 옵션 사용](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)을 참조하십시오.

   * 클릭 **[!UICONTROL Live]**.

      [라이브 설정 보기](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)를 참조하십시오.

   * 클릭 **[!UICONTROL Push Live]**.

      [스테이지 설정 라이브 푸시](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)를 참조하십시오.

## {#task_3F97949E193C4F92A104AD117FE49621}을(를) 구성한 SEO 메타 태그 미리 보기

SEO 필드의 결과 값을 미리 보고 사용할 위치에 삽입된 내용을 확인할 수 있습니다.

SEO 필드에는 포함된 필드 값이 포함될 수 있으므로 검색 결과는 지정한 검색 쿼리에 따라 달라질 수 있습니다.

**구성한 SEO 메타 태그를 미리 보려면**

1. 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**&#x200B;를 클릭합니다.
1. SEO 페이지에서 **샘플 출력 미리 보기**&#x200B;를 클릭합니다.
1. [!DNL SEO Preview] 페이지의 [!DNL Enter sample query] 필드에 검색할 쿼리 용어를 입력합니다.
1. **검색**&#x200B;을 클릭합니다.

   결과 제목, 설명 및 키워드 필드는 방금 입력한 검색 쿼리를 기반으로 페이지에 삽입되는 컨텐츠를 보여줍니다.
1. 기본 SEO 페이지로 돌아가려면 **닫기**&#x200B;를 클릭합니다.
