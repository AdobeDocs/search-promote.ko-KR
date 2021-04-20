---
description: Search&amp;Promote에 대한 FAQ 보기
solution: Target
title: FAQ
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '8648'
ht-degree: 0%

---


# FAQ{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

웹 사이트에서 SWF 파일의 인덱싱 및 검색 지원에 대해 설명하는 FAQ 페이지입니다.

다음은 SWF 파일에 대한 일반적인 질문입니다.

* [SWF 파일은 언제 크롤링 및 인덱싱됩니까?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [SWF를 인덱싱하려면 어떻게 해야 합니까?..](#section_0A6A52CC70D4495BBE14D91906318F95)
* [SWF 파일은 어떻게 인식됩니까?](#section_B36C0536AB544F509601DC6A11A8E656)
* [SWF 파일은 어떻게 인덱싱됩니까?](#section_36856058A4B54FA5ABF921344F50410C)
* [SWF 파일은 페이지로 카운트됩니까?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [개별 SWF 파일의 인덱싱을 방지하려면 어떻게 해야 합니까?](#section_E38AD37989EF410B97AF5125057BFD22)
* [SWF 파일이 ...에서 인덱싱되지 않도록 하려면 어떻게 해야 합니까?](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [웹 사이트에서 중국어, 일본어 또는 한국어 SWF 파일을 검색할 수 없는 이유는 무엇입니까?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## SWF 파일은 언제 크롤링 및 인덱싱됩니까?{#section_01BB5259140D4D5FB04CCB7A1A63DE99}

SWF 파일은 다음 예제와 같이 HTML 페이지의 embed 또는 object 태그에 포함된 경우 크롤되고 인덱싱됩니다.

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

파일 URL을 시작 지점으로 나열하는 경우 SWF 파일도 인식됩니다.

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

## SWF 파일을 색인화하려면 어떻게 해야 합니까?{#section_0A6A52CC70D4495BBE14D91906318F95}

SWF 파일을 크롤링하고 인덱싱하려면 내용 유형 **[!UICONTROL Adobe Flash Movies]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택합니다.

Flash 파일이 HTML 문서의 `<embed>` 태그 또는 `<object>` 태그에서 참조되는 한 텍스트는 인덱싱되며 파일에 나열된 모든 URL이 크롤됩니다.

파일이 `<embed>` 태그 또는 `<object>` 태그에서 참조되지 않으면 HTML 문서의 `<a href=...>` 태그 또는 URL 진입점으로 SWF 파일을 나열할 수 있습니다.

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

## SWF 파일은 어떻게 인식됩니까?{#section_B36C0536AB544F509601DC6A11A8E656}

SWF 파일은 다음 MIME 유형으로 식별됩니다.

`application/x-shockwave-flash`

파일 확장명이 .swf인 경우 SWF 파일은 `application/octet-stream`&quot; 또는 `text/plain` MIME 유형으로도 인식됩니다.

구성되지 않은 서버는 SWF 파일에 다른 MIME 형식을 사용할 수 있습니다. SWF 파일의 크롤링 및 색인 작성에 문제가 있는 경우 서버 구성을 확인하십시오.

## SWF 파일은 어떻게 인덱싱됩니까?{#section_36856058A4B54FA5ABF921344F50410C}

SWF 파일에 포함된 텍스트는 포함하는 HTML 페이지의 `<body>` 텍스트인 것처럼 인덱싱됩니다. 검색 결과가 포함된 SWF 파일에 포함된 텍스트를 찾으면 결과는 SWF 파일이 아닌 포함하는 HTML 페이지로 연결됩니다. 이렇게 하면 SWF 파일이 올바른 컨텍스트에 표시됩니다.

SWF 파일에 URL이 &quot;동영상 로드&quot; 액션인 경우 참조된 SWF 파일의 텍스트는 포함하는 HTML 페이지의 일부로 색인화됩니다.

SWF 파일에 &quot;URL 가져오기&quot; 동작으로 URL이 포함되어 있는 경우 HTML `<a href=...>` 참조가 크롤링 및 나중에 인덱싱되는 것처럼 나중에 URL이 크롤링 및 인덱싱됩니다.

SWF 파일이 URL 시작 지점으로 나열되는 경우 SWF 파일 텍스트는 단일 페이지로 인덱싱됩니다. 진입점 SWF에서 텍스트를 찾는 검색 결과는 포함하는 HTML 페이지가 아니라 동영상으로 바로 링크됩니다.

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

## SWF 파일은 페이지로 카운트됩니까?{#section_0158D6DE70BC40D78E2374787B9F58AB}

아니오. SWF 파일은 바깥쪽 HTML 페이지의 일부로 간주됩니다. SWF 파일에 포함된 모든 &quot;동영상 로드&quot; URL도 포함하는 HTML 페이지의 일부로 간주됩니다. 따라서 HTML 페이지에서 참조되는 SWF 파일은 계정 페이지 합계에 대해 &quot;페이지&quot;로 계산되지 않습니다.

SWF 파일이 URL 시작 지점으로 나열되는 경우 해당 SWF 파일과 해당 SWF 파일에 나열된 모든 &quot;동영상 로드&quot; URL은 계정의 페이지 합계에 대해 하나의 &quot;페이지&quot;로 카운트됩니다.

## 개별 SWF 파일의 인덱싱을 방지하려면 어떻게 해야 합니까?{#section_E38AD37989EF410B97AF5125057BFD22}

SWF 파일의 인덱싱을 방지하기 위해 로봇 메타 태그( `<meta name="ROBOTS" content="NOINDEX">`) 또는 `<noindex>` 태그를 포함하는 HTML 문서에 추가할 수 있습니다. 즉, `<embed>` 또는 `<object>` 태그가 포함된 문서입니다.

robots 메타 태그( `<meta name="ROBOTS" content="NOFOLLOW">`)를 사용하여 SWF 파일에 포함된 다음 URL을 방지할 수도 있습니다. 다음 HTML 문서가 비활성화된 경우, SWF 파일에 &quot;URL 가져오기&quot; 작업으로 나열된 URL이 표시되지 않습니다.

## 웹 사이트에서 SWF 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?{#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

SWF 색인을 비활성화하려면 **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) 내용 유형을 선택 취소합니다.

또한 [!DNL URL Masks]을 사용하여 SWF 파일의 색인을 비활성화할 수도 있습니다.

색인 부분에 [URL 마스크 추가...의 인덱스 부분이 아닌 URL 마스크를 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

SWF 색인을 비활성화하려면 다음 URL 마스크 중 하나를 입력합니다.

* `exclude *.swf` (정규 표현식을 사용하지 않는 경우)
* `exclude regexp ^.*\.swf$` (정규 표현식을 사용하는 경우)

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 SWF 파일을 검색할 수 없는 이유는 무엇입니까?{#section_EE1A3A705AE74148BD195A0CE513A5C4}

사이트 검색/머천다이징은 Adobe Flash으로 만든 SWF 파일에서 UTF-8을 가져옵니다. UTF-8에는 언어 표시가 없습니다. 내용 유형 **[!UICONTROL Adobe Flash Movies]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 SWF 파일에서 사용되는 언어를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

이전 SWF 파일에서도 문자 세트를 지정하지 않습니다. SWF 내용 유형 **[!UICONTROL Adobe Flash Movies]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 SWF 파일에 사용되는 문자 세트를 지정해야 합니다.

## 일반 검색 {#reference_E2C675162789452A9B99C6633B12CBEF}

사이트 검색/머천다이징을 통해 웹 사이트를 방문하는 고객이 원하는 것을 찾는 방법을 설명하는 FAQ 페이지입니다.

일반 검색과 관련된 일반적인 질문은 다음과 같습니다.

* [사이트를 사용하려면 소프트웨어를 설치해야 합니까?..](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [내 사이트가 페이지 제한을 초과하면 어떻게 됩니까?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [주마다 이메일 주소를 변경하는 방법은 무엇입니까?](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [사이트 검색/머천다이징에서 내 고객 정보는 얼마나 안전합니까?](#section_5484CB954167412BB7F0480CB0C504B8)
* [고객 정보의 개인 정보는 어떻게 됩니까?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [검색에 내 배너 광고를 표시할 수 있습니까?](#section_611EB8B32C16418386CB7DC7FB6954B8)

검색 기능에 대한 일반적인 질문은 다음과 같습니다.

* [사이트에 대한 검색 결과를 사용자 정의할 수 있습니까?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [고객이 무엇을 찾고 있는지..](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [인덱싱되고 검색할 컨텐츠 유형(PDF, 텍스트, Flash, MP3 및 Microsoft Office)을 어떻게 제어할 수 있습니까?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [ASP, JSP, PHP, CFM 또는 Perl 기반 내용을 통해 동적으로 생성된 웹 페이지가 지원됩니까?](#section_E279F004F1C542A2B9773B832E7B013F)
* [동의어를 사용하여 검색 결과를 향상시키는 방법은 무엇입니까?..](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [검색 결과 순서를 제어할 수 있습니까?](#section_C6361048502745779D9749A842C4C370)
* [검색 결과 페이지의 언어를 변경할 수 있습니까?](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Adobe에 사이트를 두 개 이상 저장할 수 있습니까?](#section_AFA8825182094660A71EEC84B8329D6D)
* [두 개 이상의 도메인을 검색할 수 있습니까?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [...할 수 있도록 사이트를 개별 섹션으로 나눌 수 있습니다.](#section_52153A9DE9F9493B967A70583848B2A4)
* [웹 사이트의 일부를 ...에서 제외하려면 어떻게 해야 합니까?](#section_D452EDE153654EF398F4A87780C6D43B)
* [지원되는 문자 집합은 무엇입니까?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [웹 사이트를 변경하거나 업데이트하면 어떻게 됩니까?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [사이트를 자동으로 색인화할 수 있습니까?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [나는 내 웹사이트에서 비밀번호를 쓴다. 여전히 사이트 검색/머천다이징을 사용할 수 있습니까?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [https의 크롤링 및 색인 지정 또는...을 지원합니까?](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [사이트 검색/머천다이징은 내 웹 사이트의 robots.txt 파일을 승인합니까?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [웹 사이트의 특정 부분은 자주 업데이트되어야 하므로...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [스크립트나 프로그램을 사용하여 증분 작업을 시작할 수 있습니까?](#section_0B6BB039557A42AA876D35D748E17DD0)

## 사이트 검색/머천다이징을 사용하려면 소프트웨어를 설치해야 합니까?{#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

아니오. 이는 사이트 검색/머천다이징의 주요 장점입니다. 엔진은 전문적인 애플리케이션으로 호스팅 및 전적으로 고성능 서버에서 유지 관리됩니다. 따라서 소프트웨어를 다른 검색 솔루션보다 쉽게 사용할 수 있습니다. 웹 사이트에 있는 고객이 검색을 입력할 수 있도록 작은 양의 HTML 코드를 페이지에 추가하는 것이 유일한 방법입니다. 사이트 검색/머천다이징은 나머지 모든 작업을 처리합니다.

## 내 사이트가 페이지 제한을 초과하면 어떻게 됩니까?{#section_ECA5FA01032D4322BABA4E2C7FE498C1}

Adobe는 방문자가 중단 없이 웹 사이트를 검색할 수 있도록 검색 기능을 지속적으로 제공하고 있습니다. 웹 사이트가 페이지 제한을 초과하는지 확인하려면 전체 인덱스 상태 또는 라이브 로그를 검토하십시오.

[전체 인덱스 정보](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3)를 참조하십시오.

라이브 또는 스테이징의 전체 인덱스 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).[

## 주별 보고서가 전송되는 이메일 주소는 어떻게 변경합니까?{#section_AE27F63DD13F425B940C8E7D9ED5C614}

주별 보고서는 각 활성 계정의 소유자에게 전송됩니다. **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**&#x200B;를 클릭하여 이메일 주소를 변경할 수 있습니다. 활성 검색 계정이 두 개 이상 있으면 모든 뉴스레터가 새 주소로 전송됩니다.

[개인 사용자 정보 구성](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)을 참조하십시오.

## 사이트 검색/머천다이징에서 내 고객 정보는 얼마나 안전합니까?{#section_5484CB954167412BB7F0480CB0C504B8}

사이트 검색/머천다이징은 안전하고 빠르고 안정적이며 사용이 간편합니다. Adobe 제품을 사용하도록 쿠키(원하는 경우에도 사용)를 강제하지 않으며, 암호와 같은 민감한 정보는 나중에 브라우저에서 검색할 수 있는 URL 링크에 절대 삽입되지 않습니다.

## 고객 정보의 개인 정보는 어떻게 됩니까?{#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobe은 고객과 방문자의 프라이버시를 존중하기 위해 노력한다. Adobe [개인 정보 보호 센터](https://www.adobe.com/privacy.html)를 참조하십시오.

## 검색 결과 페이지에 고유한 배너 광고를 표시할 수 있습니까?{#section_611EB8B32C16418386CB7DC7FB6954B8}

예. 검색 결과의 모양과 컨텐츠를 제어합니다. 웹 사이트에 대한 검색 결과 템플릿 내에서 LinkExchange 또는 SmartClicks와 같은 고유한 배너 교환 네트워크에 대한 링크를 만들 수 있습니다. 방문자가 만든 모든 히트는 배너 교환 계정에 올바르게 크레딧이 됩니다.

## 사이트에 대한 검색 결과를 사용자 정의할 수 있습니까?{#section_A64B3A621B794DF78D35ED06D9C43D0B}

예. 이것은 사이트 검색/머천다이징의 유일한 기능입니다. 고급 템플릿 기술과 HTML에 대한 간단한 지식을 통해 검색 결과가 어떻게 나타나는지 정확하게 제어할 수 있습니다.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)를 참조하십시오.

자체 서버와 사이트 검색/머천다이징 서버 간의 전환이 완벽하고 고객에게 보이지 않습니다. HTML을 모르거나 사용자 정의 템플릿을 만들 시간이 없는 경우 Adobe의 사내 전문 웹 개발자 팀에서 만든 매력적이고 사용하기 쉬운 템플릿을 선택할 수 있습니다.

## 사이트에서 고객이 검색하는 항목을 확인할 수 있습니까?{#section_73709E1B0E82478DA7B4D15B6C845F33}

예. 지난 2개월 동안 웹 사이트에서 방문자가 검색하는 검색 통계를 유지합니다. 제품 메뉴의 보고서 아래에서 언제든지 이러한 통계를 검토할 수 있습니다. 검색 보고서는 웹 사이트에서 방문자가 찾고 있는 항목과 관련된 중요한 정보를 제공합니다. 이 정보를 사용하여 디자인을 개선하거나 사이트 검색/머천다이징 엔진을 조정하여 방문자에게 보다 나은 서비스를 제공할 수 있습니다.

## 인덱싱되고 검색할 컨텐츠 유형(PDF, 텍스트, Flash, MP3 및 Microsoft Office)을 어떻게 제어할 수 있습니까?{#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

PDF 문서, 일반 텍스트 문서, Flash 동영상, MP3 파일 또는 Microsoft Office 문서에서 발견되는 텍스트의 인덱싱 및 검색을 활성화하거나 비활성화하도록 계정을 쉽게 구성할 수 있습니다.

이러한 설정은 [!DNL Staged Content Types] 페이지에서 제어됩니다.

[콘텐트 유형 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)를 참조하십시오.

## ASP, JSP, PHP, CFM 또는 Perl 기반 내용을 통해 동적으로 생성된 웹 페이지가 지원됩니까?{#section_E279F004F1C542A2B9773B832E7B013F}

정적 또는 동적으로 생성된 HTML 웹 페이지는 데이터베이스 또는 다른 백엔드 프로세스를 비롯한 인덱싱됩니다. 브라우저에서 보는 HTML 코드는 인덱싱되어 있으므로 이러한 백엔드 아키텍처로 인해 HTML 페이지가 표시되는 한 웹 사이트에서 사이트 검색/머천다이징을 사용할 수 있습니다.

검색 로봇은 [!DNL Account Settings]에 지정된 웹 사이트 주소의 첫 번째 페이지에서 시작하여 페이지 간 링크를 따라 웹 사이트를 탐색합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

검색 로봇이 웹 사이트의 모든 페이지를 탐색하고 인덱싱할 때 검색 엔진을 사용하여 사이트를 검색할 수 있습니다. 즉, 동적으로 생성된 문서가 다른 페이지의 링크와 함께 웹 사이트에 취합되는 경우에도 검색 로봇이 동적 컨텐츠를 크롤하여 색인화할 수 있습니다.

웹 사이트 컨텐츠가 크롤링 및 인덱싱된 후에 웹 사이트로 연결되는 고객은 인덱싱된 컨텐츠 내에서 정보를 검색할 수 있습니다.

## 동의어를 사용하여 내 사이트의 검색 결과를 개선할 수 있는 방법은 무엇입니까?{#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

방문자가 검색 쿼리와 관련된 페이지를 찾도록 할 때 유의어를 사용할 수 있습니다.

예를 들어 사이트에서 판매할 제품의 가격 목록이 포함된 페이지가 있다고 가정합니다. 그러나 사이트 검색/머천다이징에서 제공하는 검색 보고서를 검토한 후 고객은 검색에서 &quot;비용&quot;, &quot;비용&quot;, &quot;비용&quot; 또는 &quot;비용&quot;이라는 단어를 찾고 있음을 알게 됩니다. 이러한 단어는 검색 결과에 가격 목록 페이지를 표시하지 않습니다. [!DNL Dictionaries]의 [!DNL Add Synonyms] 기능을 사용하면 이러한 단어가 모두 동의어임을 지정할 수 있으며 고객은 사용하는 검색어에 상관없이 가격 목록을 찾을 수 있습니다.

[사전 정보](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034)를 참조하십시오.

## 검색 결과의 순서를 제어할 수 있습니까?{#section_C6361048502745779D9749A842C4C370}

예. 고급 관련 인터페이스를 사용하여 특정 검색 쿼리에 대해 반환되는 페이지를 제어할 수 있습니다. 이 기능은 특정 단어를 쿼리할 때 특정 페이지가 표시되도록 하려는 경우에 유용합니다.

[새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)를 참조하십시오.

## 검색 결과 페이지의 언어를 변경할 수 있습니까?{#section_6EE41DA8241247D48BBEB061A50599C5}

예. 사이트 검색/머천다이징 템플릿은 원하는 언어를 사용하고 웹 사이트의 모양과 일치하는 결과 페이지를 구성할 때 유연합니다.

템플릿은 검색 결과를 표시하도록 정의된 텍스트, 표준 HTML 태그 및 특수 태그의 조합으로 구성됩니다. 고객이 검색을 수행하면 검색 로봇은 템플릿을 읽고 표준 HTML 태그를 사용하여 텍스트를 출력하며 특수 템플릿 태그를 기준으로 결과 링크를 삽입합니다.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)를 참조하십시오.

결과 언어를 변경하려면 템플릿에 나타나는 영어 텍스트를 편집할 수 있습니다.

[프레젠테이션 또는 전송 템플릿 편집](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)을 참조하십시오.

## Adobe 고객 로그인 시 사이트를 두 개 이상 저장할 수 있습니까?{#section_AFA8825182094660A71EEC84B8329D6D}

예. 단일 Adobe 고객 로그인을 사용하여 여러 웹 사이트에 대해 다른 검색 엔진을 관리할 수 있습니다. &quot;계정&quot;에서 계정을 선택하고 관리합니다.

[다른 계정을 선택하여 ](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26)을(를) 참조하십시오.

## 두 개 이상의 도메인을 검색할 수 있습니까?{#section_BFBB0E9861D942F095B56CF0A8F16596}

예. [!DNL URL Entrypoints]을 사용하여 두 개 이상의 도메인에 대한 액세스를 구성할 수 있습니다. 소유하는 추가 도메인에 대한 URL 진입점을 제공합니다. 소유하지 않은 도메인을 색인화할 수 있는 권한이 있어야 합니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

## 고객이 이러한 영역을 개별적으로 또는 전체 사이트를 검색할 수 있도록 사이트를 개별 섹션으로 나눌 수 있습니까?{#section_52153A9DE9F9493B967A70583848B2A4}

예. &quot;컬렉션&quot; 기능은 고객이 웹 사이트의 특정 영역을 검색하여 원하는 내용을 빠르게 찾을 수 있도록 해줍니다.

[컬렉션 정보](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127)를 참조하십시오.

예를 들어 고객은 제품 판매 정보와 관련된 URL 컬렉션 또는 지원 서비스와 관련된 URL 컬렉션을 검색할 수 있습니다. 고객이 컬렉션의 드롭다운 목록 또는 확인란 그룹을 볼 수 있도록 컬렉션을 설정할 수 있습니다.

## 웹 사이트의 일부를 검색되지 않도록 제외하려면 어떻게 해야 합니까?{#section_D452EDE153654EF398F4A87780C6D43B}

예. URL 마스크를 지정하여 색인화에서 포함하거나 제외할 웹 사이트 페이지를 결정합니다. URL 마스크는 웹 사이트 페이지가 검색 결과에 표시되는지 여부를 결정합니다.

[URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

[URL 마스크 정보 스크립트](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)를 참조하십시오.

개별 웹 페이지의 일부가 검색되지 않도록 하려면 페이지의 일부분을 색인화에서 제외할 수 있습니다. 텍스트를 `<noindex>` 및 `</noindex>` 태그로 둘러싸십시오. 이 방법은 검색에서 탐색 텍스트를 제외하려는 경우에 유용합니다.

## 지원되는 문자 집합은 무엇입니까?{#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

웹 페이지는 일반적으로 다음과 유사한 메타 태그가 있는 문자 집합을 지정합니다.

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

사이트 검색/머천다이징 엔진은 오늘날 인터넷에서 사용 중인 모든 일반적인 문자 집합을 사용하여 웹 페이지를 올바르게 인덱싱합니다. 지원되는 문자 집합 중 일부는 다음과 같습니다.

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>아랍어(ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>중국어(번체)Big5) </p> </td> 
   <td colname="col3"> <p>일본어(Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>아랍어(Windows-1256) </p> </td> 
   <td colname="col2"> <p>중국어(번체)EUC-TW) </p> </td> 
   <td colname="col3"> <p>러시아어(KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>발트어(ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>키릴 자모(ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>남유럽(ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>발트어(Windows-1257) </p> </td> 
   <td colname="col2"> <p>키릴 자모(Windows-1251) </p> </td> 
   <td colname="col3"> <p>터키어(ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중부 유럽(ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>그리스어(ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>터키어(Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중부 유럽(Windows-1250) </p> </td> 
   <td colname="col2"> <p>그리스어(Windows-1253) </p> </td> 
   <td colname="col3"> <p>유니코드(UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어(ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>히브리어(ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII(us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어(ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>히브리어(Windows-1255) </p> </td> 
   <td colname="col3"> <p>서유럽어(ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어 간체EUC-CN) </p> </td> 
   <td colname="col2"> <p>일본어(EUC-JP) </p> </td> 
   <td colname="col3"> <p>서유럽어(ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어 간체GB2312) </p> </td> 
   <td colname="col2"> <p>일본어(ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>서유럽어(Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어 간체GBK) </p> </td> 
   <td colname="col2"> <p>일본어(ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>서유럽어(x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>중국어 간체HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>일본어(ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

기술 지원에 문의하여 위에 나열되지 않은 문자 집합에 대해 질문하십시오.

## 웹 사이트를 변경하거나 업데이트하면 어떻게 됩니까?{#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

웹 사이트의 컨텐츠를 변경한 후 전체 인덱스나 증분 인덱스를 수행할 수 있습니다. 사이트 검색/머천다이징 다운로드 및 변경된 웹 사이트 컨텐츠를 색인화합니다. 색인화가 완료되면 고객이 새 컨텐츠를 검색할 수 있습니다. 특정 시간에 특정 날짜에 사이트의 자동 색인 지정을 예약할 수도 있습니다.

라이브 또는 스테이징된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).[

라이브 또는 스테이징된 웹 사이트의 증분 인덱스 실행 중...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).[

라이브 웹 사이트](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)에 대한 전체 인덱스 일정 설정을 참조하십시오.[

라이브 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)에 대한 증분 인덱스 일정 설정을 참조하십시오.[

## 사이트를 자동으로 색인화할 수 있습니까?{#section_9C7D41636238488691ECDFEE4D4E5103}

예. 매일 사이트의 자동 색인을 예약할 수 있습니다.

매일 자동 색인 작성 외에도 사이트에서 빈번하게 변경되는 부분을 증분적으로 색인화할 수 있습니다. 자동 색인이 예약되어 있는 일 수의 경우 색인이 발생하는 시간을 제어할 수 있습니다. 또한 원할 때마다 언제든지 수동으로 사이트 인덱스를 시작할 수 있습니다.

라이브 웹 사이트](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)에 대한 전체 인덱스 일정 설정을 참조하십시오.[

라이브 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)에 대한 증분 인덱스 일정 설정을 참조하십시오.[

## 나는 내 웹사이트에서 비밀번호를 쓴다. 사이트 검색/머천다이징을 계속 사용할 수 있습니까?{#section_4618EB5B66704640B5502D1B5CB4B32E}

HTTP 기본 인증을 사용하여 웹 사이트의 특정 부분을 암호로 보호하는 경우 사이트 검색/머천다이징에서 사이트를 색인화하는 데 사용할 영역 및 암호를 지정할 수 있습니다.

필요한 웹 사이트 영역에 액세스하기 위한 암호 추가...를 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).[

## https 또는 보안 서버 컨텐츠의 크롤링 및 인덱싱 기능을 지원합니까?{#section_D5BB8B8FBEA4405583E86B4AEC37151B}

예. 보안 서버(https)에서 컨텐츠를 크롤링하고 인덱싱할 수 있습니다.

## 사이트 검색/머천다이징은 내 웹 사이트의 robots.txt 파일을 승인합니까?{#section_73BBF6FE93C64C109F45CBC2FA394DB2}

예. 로봇 제외 프로토콜은 준수합니다. 검색 로봇은 웹 사이트에 있는 robots.txt 파일을 검사합니다. robots.txt 파일에서 모든 로봇을 검색하여 사이트를 검색할 수 없는 경우 사이트 검색/머천다이징 로봇도 제외됩니다. 사이트 검색/머천다이징 로봇만 사이트를 탐색하도록 하려면 robots.txt 파일의 내용을 다음 항목으로 설정합니다.

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

웹 로봇과 로봇 제외 프로토콜에 대한 자세한 내용은 다음 링크를 참조하십시오.

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## 고객이 가장 정확한 검색 결과를 얻을 수 있도록 웹 사이트의 특정 부분을 자주 업데이트해야 합니다. 증분 색인 지정 기능이 이 문제에 도움이 됩니까?{#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

예. 이 시나리오는 사이트 검색/머천다이징을 용이하게 하기 위해 증분 색인 지정 기능을 만든 것입니다. 증분 인덱싱의 주요 이점은 회사가 웹 사이트의 일부를 동적으로 변경할 수 있는 인덱스를 자주 만들 수 있다는 것입니다. 이러한 기능을 통해 &quot;분&quot; 단위로 검색 결과를 표시할 수 있습니다.

라이브 또는 스테이징된 웹 사이트의 증분 인덱스 실행 중...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).[

라이브 웹 사이트](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)에 대한 증분 인덱스 일정 설정을 참조하십시오.[

## 제품 카탈로그 또는 인벤토리 관리 시스템과 같은 백엔드 데이터베이스에서 동적으로 생성된 웹 페이지가 지원됩니까?{#section_26896C556483457E879785E751583B16}

데이터베이스에서 작성한 페이지 또는 다른 백엔드 프로세스를 비롯한 정적 또는 동적으로 생성된 HTML 웹 페이지는 인덱싱됩니다. 브라우저에 의해 표시되는 HTML 코드는 인덱싱되므로 백엔드 데이터베이스 정보가 HTML 페이지에 도달하는 한 웹 사이트에서 사이트 검색/머천다이징을 사용할 수 있습니다.

검색 로봇은 [!DNL Account Settings]에 지정된 웹 사이트 주소의 첫 번째 페이지에서 시작하여 페이지 간 링크를 따라 웹 사이트를 탐색합니다.

[계정 설정 구성](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)을 참조하십시오.

검색 로봇이 웹 사이트의 모든 페이지를 탐색하고 인덱싱할 때 검색 엔진을 사용하여 사이트를 검색할 수 있습니다. 즉, 동적으로 생성된 문서가 다른 페이지의 링크와 함께 웹 사이트에 취합되는 경우에도 검색 로봇이 동적 데이터베이스 컨텐츠를 크롤하여 색인화할 수 있습니다.

웹 사이트 컨텐츠가 크롤링 및 인덱싱된 후에 웹 사이트로 연결되는 고객은 인덱싱된 컨텐츠 내에서 정보를 검색할 수 있습니다.

전체 컨텐츠 검색을 쉽게 활성화하거나 보다 좁은 주제 기반 검색을 제목, 메타 설명 또는 메타 키워드 문서 태그 또는 세 가지 모두 정보로 제한할 수 있습니다. 메타데이터 정의를 사용하여 실제 검색 결과에 제품 이미지와 같은 사용자 정의 표시 필드를 만들 수도 있습니다.

[새 메타 태그 필드 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)를 참조하십시오.

## 스크립트나 프로그램을 사용하여 사이트의 증분 색인을 시작할 수 있습니까?{#section_0B6BB039557A42AA876D35D748E17DD0}

예. 스크립트나 프로그램을 사용하여 웹 사이트의 증분 인덱스를 시작할 수 있을 뿐만 아니라 컨텐츠가 변경되거나 업데이트될 때마다 서버에 ping을 수행하여 사이트를 색인화할 수 있습니다.

[스크립팅된 인덱스 정보](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)를 참조하십시오.

## 기능 구현 {#reference_2D0C4A80B8D64051BA9694D562DCE663}

[!DNL Search&Promote]의 다양한 기능 구현에 대해 설명하는 FAQ 페이지입니다.

다음은 웹 사이트의 [!DNL Search&Promote]에 있는 기능 구현과 관련된 일반적인 질문입니다.

* [비즈니스 규칙이 실행되지 않는 이유는 무엇입니까?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [색인 예약, 색인 시작 오류 및 스테이지된 색인 시작 문제가 발생하는 이유는 무엇입니까?](#section_E05758193DF5436784B0145839989F75)
* [색인 크기 제한이 허용된 경계를 초과합니다. 이 문제는 왜 발생하며 어떻게 수정합니까?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## 비즈니스 규칙이 실행되지 않는 이유는 무엇입니까?{#section_7FEB60383D8A4B11A60DFF9067274699}

배너가 표시될 때 비즈니스 규칙을 구성하거나 결과가 어떻게 나타나는지 그리고 어떤 순서로 표시되는지를 결정할 수 있도록 도와줍니다. 패싯에서 항목의 위치와 주어진 검색에 사용되는 템플릿을 구성할 수도 있습니다.
프레젠테이션 템플릿에서 실행되는 순서를 변경하려면 비즈니스 규칙의 순서를 변경합니다. 비즈니스 규칙은 정의된 순서대로 실행됩니다.즉, 규칙의 주문 번호가 높을수록 나중에 프로세스에서 실행되어 이전 규칙보다 우선합니다. 비즈니스 규칙 페이지의 테이블의 순서 열에 새 숫자를 입력하여 규칙을 다시 정렬합니다.

[비즈니스 규칙 정보](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD)를 참조하십시오.

## 색인 예약, 색인 시작 오류 및 스테이지된 색인 시작 문제가 발생하는 이유는 무엇입니까?{#section_E05758193DF5436784B0145839989F75}

인덱스를 생성할 때 전체 또는 증분 색인이든 색인 크롤링 상태 정보가 실시간으로 표시됩니다. 예를 들어 색인 작성 프로세스 중에 발생한 시작 시간, 경과 시간 및 오류를 볼 수 있습니다. 마지막 인덱스의 상태에 대한 정보도 표시됩니다. 이 정보를 사용하여 발생하는 색인 오류 문제를 해결합니다.

인덱스를 예약하려면 라이브 웹 사이트](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) 및 [라이브 웹 사이트에 대한 증분 인덱스 일정 설정](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)을 참조하십시오.[

스테이지된 인덱스를 시작하려면 라이브 또는 스테이지된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.라이브 또는 스테이징 웹 사이트의 증분 색인 실행 중...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).[](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D)[

## 색인 크기 제한이 허용된 경계를 초과합니다. 이러한 문제가 발생하는 이유는 무엇이며 이를 어떻게 해결해야 합니까?{#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

웹 사이트는 추가되고 있는 더 많은 문서와 웹 페이지를 &quot;검색&quot;하는 시간이 지남에 따라 확장되는 경향이 있습니다. 귀하의 계정이 색인 크기 제한을 초과할 수 있습니다. 이러한 경우 **[!UICONTROL URL Mask]** 사용을 고려할 수 있습니다. 이 기능은 색인을 원하지 않거나 포함하지 않아도 되는 색인 크롤링 문서의 문서 및 웹 페이지를 숨겨 인덱스 크기를 줄입니다. 색인 크기 제한이 계정에서 더 크게 설정되도록 하려면 기술 지원에 문의하는 방법도 있습니다.

[URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

어떻게 해야 할지 잘 모르는 경우 기술 지원에 문의해야 합니다. 색인 크기에 영향을 주는 다른 변수가 많이 있을 수 있으며, 조정되면 계정 과금에 영향을 줄 수 있습니다.

## 국제 {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

중국어(간체 및 번체), 일본어 및 한국어와 같은 멀티바이트 아시아 언어 등 19개 이상의 언어에 대한 인덱싱 및 검색 지원을 설명하는 FAQ 페이지입니다.

언어 및 문자 집합에 대한 일반적인 질문은 다음과 같습니다.

* [검색 쿼리의 문자 집합 인코딩을 제어하는 것...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [인코딩이...의 인코딩과 일치하는 페이지만 검색됩니다.](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [검색 결과 페이지에 사용되는 인코딩은 무엇입니까?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [유니코드, UTF-8, 인코딩 페이지에서 사이트 검색/머천다이징을 사용할 수 있습니까?](#section_130997CB08934A13A5261D85CF88040C)
* [웹 사이트에서 중국어, 일본어 또는 한국어 PDF 파일을 검색할 수 없는 이유는 무엇입니까?](#section_539AFF482F814D28B5929F683D2F2175)
* [웹 사이트에서 중국어, 일본어 또는 한국어 SWF 파일을 검색할 수 없는 이유는 무엇입니까?](#section_9C0849528AFF4C10AA97A2C912992638)
* [웹 사이트에서 중국어, 일본어 또는 한국어 Microsoft Office 파일을 검색할 수 없는 이유는 무엇입니까?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [웹 사이트에서 중국어, 일본어 또는 한국어 MP3 파일을 검색할 수 없는 이유는 무엇입니까?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [...을 얻기 위해 특별한 일을 해야 하나요?](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Netscape 4.7 이하 버전의 경우 중국어, 일본어 또는 한국어 글꼴은 어떻게 검색 결과에 표시됩니까?](#section_DF42567063304F918D406AC76529DFB7)

## 검색 쿼리의 문자 집합 인코딩은 어떤 컨트롤을 사용합니까?{#section_DF2E8570AFC2480FA199FD26C941A22F}

검색 계정의 &quot;웹 양식&quot; 섹션에는 검색 기능을 웹 사이트에 추가하는 데 사용하는 샘플 검색 양식이 포함되어 있습니다. 이 검색 양식 코드를 보면 다음과 유사한 라인을 찾을 수 있습니다.

`<input type=hidden name="sp_f" value="iso-8859-1">`

이 코드 행은 들어오는 쿼리가 서유럽 언어에 대한 일반적인 인코딩인 iso-8859-1로 인코딩되었음을 검색 엔진에 알립니다. 제품 메뉴로 이동하고 **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**&#x200B;를 클릭하여 이 설정을 변경할 수 있습니다. [!DNL Personal Information] 페이지의 **[!UICONTROL Character Encoding]** 드롭다운 목록에서 새 인코딩을 선택합니다.

[개인 사용자 정보 구성](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)을 참조하십시오.

검색 양식의 `sp_f` 행을 편집하여 웹 페이지의 인코딩 값을 수동으로 변경할 수도 있습니다. 검색 양식의 `sp_f` 값은 표시되는 페이지의 문자 집합 인코딩과 일치해야 합니다.

## 검색 쿼리의 인코딩과 일치하는 인코딩을 검색하는 페이지만 검색됩니까?{#section_9E544F3DB7DE41618DC1BC8224B32C5A}

기본적으로 아니요. 웹 사이트 페이지가 문자 집합 인코딩을 올바르게 식별하면 페이지가 여러 인코딩을 사용하는 경우에도 검색 쿼리 인코딩과 페이지 인코딩 간에 필요한 전환이 이루어집니다.

## 검색 결과 페이지에 사용되는 인코딩은 무엇입니까?{#section_DA68670F35D54EAABF7DBB010F4409BF}

계정의 문자 집합 인코딩은 결과 템플릿에 대한 기본 인코딩을 결정합니다.

[개인 사용자 정보 구성](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)을 참조하십시오.

HTML 템플릿에서 문자 세트를 지정하는 방법에 대해 자세히 알아볼 수 있습니다.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)를 참조하십시오.

## 유니코드, UTF-8, 인코딩 페이지에서 사이트 검색/머천다이징을 사용할 수 있습니까?{#section_130997CB08934A13A5261D85CF88040C}

예. 그러나 UTF-8과 같은 유니코드 문자 집합은 페이지가 쓰는 언어를 결정하는 데 필요한 정보를 충분히 제공하지 않습니다. 이러한 페이지를 올바로 검색하려면 언어를 지정해야 합니다. 문서 언어를 결정하기 위해 정보는 다음 순서로 처리됩니다.

* 서버에 의해 문서에 대한 컨텐츠 언어 HTTP 헤더가 제공됩니다.
* 문서의 `<HEAD>` 섹션에 있는 META 요소(예: `META HTTP-EQUIV="Content-Language" Content="ja_JP"`).

* `<HTML>` 태그의 LANG 속성(예: `<HTML LANG="ja_JP">`).

서버가 컨텐츠 언어 HTTP 헤더를 전달하도록 구성되어 있지 않고, 문서에 언어 META 요소 및 `<HTML>` 태그의 언어 속성이 모두 포함되어 있지 않은 경우, 메타데이터 주입을 사용하여 적절한 언어를 지정할 수 있습니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 PDF 파일을 검색할 수 없는 이유는 무엇입니까?{#section_539AFF482F814D28B5929F683D2F2175}

사이트 검색/머천다이징은 언어를 표시하지 않고 Adobe PDF 파일에서 UTF-8을 가져옵니다. **[!UICONTROL PDF Documents]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 PDF 파일에서 사용할 언어를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 SWF 파일을 검색할 수 없는 이유는 무엇입니까?{#section_9C0849528AFF4C10AA97A2C912992638}

사이트 검색/머천다이징은 언어를 표시하지 않고 Adobe Flash으로 만든 Adobe Flash 동영상 파일에서 UTF-8을 가져옵니다. 내용 유형 **[!UICONTROL Adobe Flash Movies]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 SWF 파일에 사용되는 언어를 지정해야 합니다.

Flash 버전 4 또는 이전 버전의 SWF 파일의 경우 파일에 있는 문자 집합이 지정되지 않습니다. 내용 유형 **[!UICONTROL Adobe Flash Movies]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 SWF 파일에 사용되는 문자 세트를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 Microsoft Office 파일을 검색할 수 없는 이유는 무엇입니까?{#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

사이트 검색/머천다이징은 언어를 표시하지 않고 Microsoft Office 파일(Microsoft Word, Microsoft Excel 및 Microsoft PowerPoint)에서 UTF-8을 가져옵니다. 내용 유형 **[!UICONTROL Microsoft Office Files]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 Microsoft Office 파일에서 사용되는 언어를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 MP3 파일을 검색할 수 없는 이유는 무엇입니까?{#section_DB6D60CF46F94125BF4E54AF3036DBFC}

내용 유형 **[!UICONTROL Text in MP3 Music Files]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택하는 경우 메타데이터 주입을 사용하여 MP3 파일을 인코딩하는 데 사용되는 문자 세트를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 웹 사이트의 .txt 파일을 올바로 색인화하려면 특별한 작업이 필요합니까?{#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

내용 유형 **[!UICONTROL Text Documents]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 .txt 파일을 인코딩하는 데 사용되는 문자 세트를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## Netscape 4.7 이하 버전의 경우 중국어, 일본어 또는 한국어 글꼴은 어떻게 검색 결과에 표시됩니까?{#section_DF42567063304F918D406AC76529DFB7}

계정에서 기본 템플릿, 바로 사용할 수 있는 템플릿 중 하나 또는 이러한 템플릿을 기반으로 하는 템플릿을 사용하는 경우 Arial 또는 Helvetica를 글꼴 면으로 지정하는 글꼴 태그가 계정에 포함될 수 있습니다. 예, `<font face="arial, helvetica" size="+1">`. Netscape 4.7 이하에서는 Arial 또는 Helvetica 글꼴 얼굴이 사용될 때 중국어, 일본어 또는 한국어 문자를 표시하지 않습니다. `face` 속성을 제거하거나 글꼴 얼굴을 중국어, 일본어 또는 한국어에 보다 적합한 글꼴로 바꿉니다.

## 낮은 페이지 수 {#reference_4344E3E3CB2948939860F8C078BD7773}

낮은 색인 페이지 수와 관련된 일반적인 문제를 설명하는 FAQ 페이지입니다.

색인 페이지 카운트의 낮은 색인화에 대한 일반적인 질문은 다음과 같습니다.

* [색인 로그를 검사했습니까?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [URL에 입력 실수가 있습니까?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [시작 지점 웹 페이지에 다른 페이지에 대한 링크가 있습니까?](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [웹 사이트의 다른 페이지에 대한 링크가 포함된 경우..](#section_EE34A67D60A844EBB0921C03544FF63E)
* [웹 페이지의 HTML 태그는](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [...에서 HTML 주석 태그를 잘못 구성했습니까?](#section_D1C39D79341845CB9C38579AABDF3A24)
* [웹 페이지에 다른 페이지의 링크가 포함되어 있습니까?..](#section_F8082759184049AAA8FA6342C1F84389)
* [URL에 가상 도메인 서비스를 사용하고 있습니까?..](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [웹 페이지에서 메타 새로 고침 태그를 사용합니까?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [웹 페이지에서 메타 로봇 태그를 사용합니까?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [웹 사이트에서 로봇 제외 파일을 사용합니까?](#section_BF7B663347814F58AD736066C86B7D25)

## 색인 로그를 검사했습니까?{#section_D6626536DC3D40DDA4A1224F1CB276BF}

색인 로그는 웹 사이트를 색인화할 때 사이트 검색/머천다이징 로봇이 수집하는 자세한 정보를 포함합니다. 로그에는 크롤링된 링크 및 발생한 오류 목록이 포함됩니다. 색인 로그를 검사하면 웹 사이트의 모든 페이지가 인덱싱되지 않은 이유를 확인할 수 있습니다.

라이브 또는 스테이징의 전체 인덱스 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).[

라이브 또는 스테이징의 증분 인덱스 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).[

## URL에 입력 실수가 있습니까?{#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

HTML 양식에 긴 URL을 입력하면 하나 이상의 타이포그래피 오류가 발생할 수 있습니다. URL에는 공백이 없어야 합니다. 또한 일부 웹 서버는 대소문자를 구분하는 방식으로 URL을 처리합니다.

제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 클릭합니다. [!DNL Staged URL Entrypoints] 페이지에서 다음을 확인합니다.

* URL에 인쇄 오류가 없습니다.
* URL의 문자는 모두 대소문자를 올바로 사용합니다.
* URL에 공백 문자가 없습니다.

URL 시작점을 테스트하려면 웹 브라우저에 URL을 복사하여 붙여 넣어 웹 사이트가 표시되는지 확인합니다. 나타나지 않는 경우 URL 경로에 오류가 없는지 다시 확인하십시오.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

## 시작 지점 웹 페이지에 웹 사이트의 다른 페이지에 대한 링크가 있습니까?{#section_1C2D6ED54E7249268B555D9DC33352B3}

사이트 검색/머천다이징 로봇은 고객처럼 웹 사이트를 탐색합니다.페이지를 연결하는 링크를 따릅니다. 검색 로봇이 사이트에서 다른 페이지를 찾고 색인화하려면 먼저 시작 지점 웹 페이지에 링크가 있어야 합니다.

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

## 웹 사이트의 다른 페이지에 대한 링크가 JavaScript에 포함되어 있습니까?{#section_EE34A67D60A844EBB0921C03544FF63E}

웹 사이트에서 JavaScript를 사용하여 다른 페이지에 연결하는 롤오버 작업 및 메뉴와 같은 정교한 탐색 기술을 사용할 수 있습니다. 하지만 사이트 검색/머천다이징 로봇은 JavaScript에 포함된 링크를 따라갈 수 없습니다.

이 문제를 해결하는 데 사용할 수 있는 한 가지 해결 방법은 JavaScript가 포함된 HTML의 다른 페이지에 숨겨진 링크를 배치하는 것입니다. 웹 사이트 고객이 이러한 링크를 볼 수 없지만 검색 로봇은 여전히 링크를 검색하고 탐색합니다. `</body>` 태그 바로 앞에 숨겨진 태그를 페이지 하단에 배치할 수 있습니다. 다음과 같이 표시됩니다.

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

또 다른 해결 방법은 웹 사이트에 있는 추가 페이지의 URL을 크롤링 및 색인을 위한 시작 지점으로 나열하는 것입니다. 다음과 같이 URL을 `https://`으로 시작합니다.

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

인덱싱할 URL 시작 지점 [여러 개 추가](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45)를 참조하십시오.

## 웹 페이지의 HTML 태그가 잘못된 시퀀스에 있습니까?{#section_F31A2F5D2C284AC084158A5BD763DC5D}

HTML 사양을 사용하려면 `<html>`, `<head>` 및 `<body>` 태그가 HTML 문서의 특정 시퀀스를 따라야 합니다. 모든 웹 페이지의 태그에는 다음 시퀀스가 있어야 합니다.

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

HTML 태그가 올바른 순서로 표시되지 않으면 사이트 검색/머천다이징 로봇이 웹 페이지를 제대로 구문 분석하고 색인화할 수 없습니다. 다음은 올바른 시퀀스에 있지 않은 태그의 예입니다.

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

이 경우 `<html>`, `<head>` 및 `<body>` 태그를 웹 페이지의 올바른 시퀀스에 배치합니다.

## 웹 페이지에서 HTML 주석 태그 형식이 잘못 지정되었습니까?{#section_D1C39D79341845CB9C38579AABDF3A24}

웹 페이지에서 잘못된 HTML 주석을 주의 깊게 검토하고 수정해야 합니다.

HTML 사양을 사용하려면 HTML 주석이 `<!--` 문자로 시작되고 `-->` 문자로 끝나야 합니다. 사이트 검색/머천다이징 로봇이 웹 페이지의 태그를 부적절하게 파싱하는 잘못된 형식의 주석을 쉽게 간과할 수 있습니다. 잘못된 형식의 주석을 사용하면 사이트 검색/머천다이징 로봇은 파싱해야 하는 다른 중요한 태그를 놓칠 수 있습니다. 웹 페이지에서 `<body>` 태그 바로 앞에 주석을 유의하십시오.

다음은 올바른 형식의 주석의 예입니다.

`<!-- This HTML comment is OK. -->`

다음은 부적절한 형식의 주석의 예입니다.

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## 웹 페이지에 다른 도메인의 페이지에 대한 링크가 포함되어 있습니까?{#section_F8082759184049AAA8FA6342C1F84389}

웹 사이트는 도메인 주소가 다른 웹 서버에 실제로 존재하는 페이지로 구성될 수 있습니다. 예를 들어 기본 웹 사이트 주소가 다음과 같은 경우:

`https://www.mydomain.com/`

웹 사이트에는 다음과 같은 다른 도메인의 페이지가 있을 수도 있습니다.

`https://www.otherdomain.com/`

기본적으로 사이트 검색/머천다이징 로봇은 기본 도메인이 아닌 도메인의 링크를 따라가지 않습니다. 그러나 검색 계정에 대한 추가 진입점을 설정하여 여러 도메인을 쉽게 색인화할 수 있습니다.

제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 클릭합니다. 사이트의 &quot;기본 웹 사이트 시작 지점&quot; URL을 추가합니다. 그런 다음 사이트 페이지를 포함하는 다른 모든 도메인에 추가 URL 진입점을 추가합니다. 예를 들어 기본 URL 시작 지점을 다음으로 설정합니다.

`https://www.mydomain.com/`

다음 사이트 URL 진입점을 추가합니다.

`https://www.otherdomain.com/`

## URL에 가상 도메인 서비스를 사용하고 있습니까?{#section_2861F09EA21A45E6B7E15F032739CDF3}

고객이 웹 사이트로 이동할 수 있도록 더 나은 URL을 제공하기 위해 가상 도메인 서비스(&quot;도메인 리디렉션 서비스&quot;라고도 함)를 사용할 수 있습니다. 예를 들어 웹 사이트의 실제 주소가 다음과 같다고 가정합니다.

`https://www.myispdomain.com/~myname/mywebpages/`

그러나 고객이 다음 주소로 사이트에 도달할 수 있도록 가상 도메인 서비스를 사용합니다.

`https://myname.adomain.com/`

또는 

`https://adomain.com/myname/`

기본적으로 사이트 검색/머천다이징 로봇은 기본 도메인이 아닌 도메인의 링크를 따라가지 않습니다. 그러나 검색 계정에 대한 추가 진입점을 설정하여 여러 도메인을 쉽게 색인화할 수 있습니다.

제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**&#x200B;를 클릭합니다. 사이트의 가상 도메인 이름에 &quot;기본 웹 사이트 URL 시작 지점&quot;을 추가합니다. 그런 다음 웹 사이트가 실제로 거주하고 있는 도메인에 진입점을 추가할 수 있습니다.

예를 들어 기본 URL 시작 지점을 다음과 같이 설정합니다.

`https://myname.adomain.com/`

그리고 다음 추가 웹 사이트 URL 시작 지점을 추가합니다.

`https://www.myispdomain.com/~myname/mywebpages/`

## 웹 페이지에서 메타 새로 고침 태그를 사용합니까?{#section_5A2F544C237C49B8B1A7FE0C45371C0D}

대부분의 웹 사이트에는 다음과 유사한 `<head>...</head>` 태그 사이에 메타 새로 고침 태그가 포함된 전면 페이지가 있습니다.

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

특정 상황에서 사이트 검색/머천다이징 로봇은 메타 새로 고침 URL을 따라 웹 사이트의 컨텐츠를 색인화할 수 없습니다. 이 문제는 추가 시작점을 설정하여 쉽게 해결할 수 있습니다.

제품 메뉴에서 **[!UICONTROL Settings]** > 크롤링 > **[!UICONTROL URL Entrypoints]**&#x200B;을 클릭합니다. 메타 새로 고침 태그의 URL에 다른 진입점을 추가합니다.

## 웹 페이지에서 메타 로봇 태그를 사용합니까?{#section_36275A33DDFE4620BABA948F8A63DBD2}

웹 페이지는 메타 로봇 태그를 사용하여 웹 사이트를 정기적으로 탐색하는 웹 로봇을 제어합니다. 메타 로봇 태그는 웹 페이지의 `<head>...</head>` 태그 사이에 나타나며 다음 태그와 비슷합니다.

`<meta name="robots" content="noindex, nofollow">`

사이트 검색/머천다이징 로봇은 자체 웹 로봇이므로 메타 로봇 태그의 지시를 따릅니다. 이러한 방식으로 다른 로봇을 제외함으로써 사이트 검색/머천다이징 로봇도 제외합니다.

웹 로봇과 로봇 제외 프로토콜에 대한 자세한 내용은 다음 링크를 참조하십시오.

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

웹 사이트에서 인덱싱할 웹 페이지에서 메타 로봇 태그를 제거하거나 수정합니다.

## 웹 사이트에서 로봇 제외 파일을 사용합니까?{#section_BF7B663347814F58AD736066C86B7D25}

웹 사이트에는 모든 또는 특정 로봇이 크롤링 시 제외됩니다. 웹 사이트에 robots.txt 파일이 있는지 확인하려면 다음과 같이 최상위 도메인 아래에서 확인합니다.

`https://www.yourdomain.com/robots.txt`

robots.txt 파일의 내용은 다음 텍스트와 유사합니다.

```
User-agent: * 
Disallow: /
```

사이트 검색/머천다이징 로봇은 자체 웹 로봇이므로 robots.txt 파일에서 지침을 따릅니다. 사이트 검색/머천다이징 로봇은 제외됩니다. 이 문제를 해결하려면 로봇 제외 파일(robots.txt)을 편집하여 다음과 같이 사이트 검색/머천다이징 로봇이 웹 사이트를 크롤링 및 색인화할 수 있도록 허용합니다.

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

웹 사이트에서 Microsoft® Office 파일의 인덱싱 및 검색 지원에 대해 설명하는 FAQ 페이지입니다.

다음은 Microsoft Office 파일에 대한 일반적인 질문입니다.

* [Microsoft Office 파일에서 색인화된 항목은 무엇입니까?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Microsoft Office 파일에서 색인되지 않는 항목...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [Microsoft Office 파일은 HTML 페이지와 다르게 색인화됩니다...](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Microsoft Office 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?..](#section_FEBA71274CD14CB99731ADF982087F4C)

## Microsoft Office 파일에서 색인화된 항목은 무엇입니까?{#section_8681DADFCFE24B7787B1FC08D431EE28}

Microsoft Word 파일, Microsoft Excel 파일 및 Microsoft PowerPoint 파일의 전체 내용은 인덱싱됩니다.

Microsoft Word 파일의 다음 부분은 인덱싱됩니다.

* Title
* 키워드
* 제목(설명)
* 텍스트 기반 컨텐츠
* 다른 문서에 대한 하이퍼링크

Microsoft Excel 파일의 다음 부분은 인덱싱됩니다.

* 제목
* 키워드
* 제목(설명)
* 셀의 텍스트
* 셀의 숫자 수식의 값

Microsoft PowerPoint 파일의 다음 부분은 인덱싱됩니다.

* 제목
* 키워드
* 제목(설명)
* 각 슬라이드의 텍스트

## Microsoft Office 파일에서 색인이 되지 않는 것은 무엇입니까?{#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Microsoft Office 파일에 포함된 그래픽 또는 포함된 그래픽에 포함된 모든 텍스트는 색인이 적용되지 않습니다. 사용자 지정 속성 정의는 메타데이터로 인덱싱되지 않습니다. PowerPoint 파일의 머리글 및 바닥글과 같은 특수 필드의 일부 텍스트도 색인이 되지 않습니다.

## Microsoft Office 파일은 HTML 페이지와 다르게 색인화됩니까?{#section_C104B44684F340549A6B9EB8F39EDDBB}

검색 로봇이 Microsoft Office 파일과 HTML 파일을 인덱싱하는 방식의 차이점은 각 HTML 파일은 개별 페이지이고 단일 Microsoft Office 파일은 수백 개의 페이지를 나타낼 수 있다는 것입니다. 이러한 이유로 각 페이지는 Microsoft Office 파일에서 검색 계정 아래에 별도의 페이지로 카운트됩니다.

## 웹 사이트에서 Microsoft Office 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?{#section_FEBA71274CD14CB99731ADF982087F4C}

검색 로봇이 Microsoft Office 파일을 크롤링하고 인덱싱하지 않으려면 **[!UICONTROL Microsoft Office Files]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**) 내용 유형을 선택 해제합니다.

[!DNL URL Masks]을 사용하여 Microsoft Office 파일의 색인을 비활성화할 수도 있습니다.

다음 URL 마스크를 입력합니다.

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>정규 표현식을 사용하지 않는 경우 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">제외 *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">exclude *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">제외 *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>정규 표현식을 사용하는 경우 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">regexp ^을(를) 제외합니다.*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">regexp ^을(를) 제외합니다.*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">regexp ^을(를) 제외합니다.*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

색인 부분에 [URL 마스크 추가...의 인덱스 부분이 아닌 URL 마스크를 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

웹 사이트에서 MP3 음악 파일의 인덱싱 및 검색 지원에 대해 설명하는 FAQ 페이지입니다.

다음은 MP3 파일과 관련된 일반적인 질문입니다.

* [MP3 파일은 언제 크롤링 및 인덱싱됩니까?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [기어가고 색인화하려면 어떻게 해야 하나요?](#section_3CD794446E3545379C14E9F222118665)
* [MP3 파일은 어떻게 인식됩니까?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [MP3 파일에서 색인화된 것은 무엇입니까?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [MP3 파일은 페이지로 카운트됩니까?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [개별 MP3 파일의 색인 작업을 방지하려면 어떻게 해야 합니까?](#section_C989DC1D3D3841B38F683A462195DC05)
* [MP3 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [사이트에서 중국어, 일본어 또는 한국어 MP3 파일을 검색할 수 없는 이유는 무엇입니까?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## MP3 파일은 언제 크롤링 및 인덱싱됩니까?{#section_538EA1682C9C47E3A62640BB25D84C36}

MP3 파일은 두 가지 방법 중 하나로 크롤링 및 색인화됩니다. 가장 일반적인 방법은 HTML 파일의 앵커 href 태그에 있는 것입니다.

`<a href="MP3-file-URL"></a>`

두 번째 방법은 MP3 파일의 URL을 URL 시작 지점으로 입력하는 것입니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

## 사이트에서 MP3 파일을 크롤링하고 색인화하려면 어떻게 해야 합니까?{#section_3CD794446E3545379C14E9F222118665}

계정에 대한 MP3 크롤링 및 인덱싱을 활성화하려면 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;를 클릭합니다. [!DNL Staged Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]**&#x200B;을 선택합니다.

[콘텐트 유형 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)를 참조하십시오.

## MP3 파일은 어떻게 인식됩니까?{#section_230E7336965A424F96C5CCF1D3C2D103}

MP3 파일은 &quot;audio/mpeg&quot;인 MIME 유형으로 인식됩니다.

## MP3 파일에서 색인화된 것은 무엇입니까?{#section_E99D252B27CA4946AED3FCD3ABD8779D}

MP3 파일은 선택적으로 소량의 텍스트 정보를 저장합니다. 이 정보에는 앨범 이름, 아티스트 이름, 노래 제목, 노래 장르, 출시 연도 및 댓글이 포함될 수 있습니다. 이 정보는 파일의 맨 끝에 TAG라는 이름으로 저장됩니다. TAG 정보가 포함된 MP3 파일은 다음 방법으로 인덱싱됩니다.

* 노래 제목은 HTML 페이지의 제목처럼 처리됩니다.
* 주석은 HTML 페이지에 대해 정의된 설명처럼 처리됩니다.
* 이 장르는 HTML 페이지에 대해 정의된 키워드로 취급됩니다.
* 아티스트 이름, 앨범 이름 및 릴리스 연도는 HTML 문서의 본문처럼 처리됩니다.

## MP3 파일은 페이지로 카운트됩니까?{#section_9910BEB6617D4D2090558CDF6C65D16B}

예. 웹 사이트에서 크롤링 및 인덱싱된 각 MP3 파일은 하나의 페이지로 카운트됩니다.

## 개별 MP3 파일의 색인화를 방지하려면 어떻게 합니까?{#section_C989DC1D3D3841B38F683A462195DC05}

MP3 파일에 연결된 앵커 태그를 `<nofollow>` 및 `</nofollow>` 태그로 둘러싸십시오. 검색 로봇은 이러한 태그 사이의 링크를 따라가지 않습니다.

또 다른 방법은 MP3 파일의 URL을 제외 마스크로 추가하는 것입니다.

[URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

[URL 마스크 정보 스크립트](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)를 참조하십시오.

## MP3 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?{#section_305D2B28D1124776B6DC0C62A17827C6}

계정에 대한 MP3 인덱싱을 제어하는 가장 쉬운 방법은 [!DNL Staged Content Types] 페이지에서 **[!UICONTROL Text in MP3 Music Files]**&#x200B;을 선택 취소하는 것입니다.

[크롤링 및 인덱스](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)할 컨텐트 유형 선택을 참조하십시오.

또한 URL 마스크 기능을 사용하여 파일 확장명에 의한 MP3 인덱싱을 비활성화할 수 있습니다. 이렇게 하려면 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다. 다음 마스크 중 하나를 입력합니다.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>계정... </p> </th> 
   <th colname="col2" class="entry"> <p>다음 URL 마스크를 입력합니다. </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>정규 표현식을 사용하지 않음 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclude *.mp3  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>정규 표현식 사용 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> regexp ^을(를) 제외합니다.*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

## 사이트에서 중국어, 일본어 또는 한국어 MP3 파일을 검색할 수 없는 이유는 무엇입니까?{#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

중국어, 일본어 또는 한국어 MP3 파일을 검색하려면 제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**&#x200B;을 클릭합니다. 그런 다음 **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**&#x200B;를 클릭하고 MP3 파일을 인코딩하는 데 사용할 문자 세트를 지정합니다.

[크롤링 및 인덱스](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8)할 컨텐트 유형 선택을 참조하십시오.

[주입 정보](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5)를 참조하십시오.

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

FAQ 페이지에서는 웹 사이트에서 PDF 파일의 인덱싱 및 검색 지원에 대해 설명합니다.

PDF 파일에 대한 일반적인 질문은 다음과 같습니다.

* [PDF 파일에서 색인이 되는 것은 무엇입니까?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [PDF 파일에서 색인화되지 않는 항목은 무엇입니까?](#section_A14B353AE503408896BACBBF3F748FA0)
* [색인화된 PDF 파일은 어떻게 카운트됩니까?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [검색 결과에 PDF 아이콘이 표시될 수 있습니까?](#section_829CE82CC3544502A13D27C4DB820189)
* [검색 결과 링크를 ...의 특정 페이지에 연결할 수 있습니까?](#section_A06E7F7017E6441E98209D288EE57BF6)
* [PDF 파일이 ...에서 색인화되지 않도록 하려면 어떻게 합니까?](#section_96671419A822486AAC654D8DAD819940)
* [웹 사이트에서 중국어, 일본어 또는 한국어 PDF 파일을 검색할 수 없는 이유는 무엇입니까?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## PDF 파일에서 색인이 되는 것은 무엇입니까?{#section_62BFCD7158B44F2BB3B1864224B50174}

PDF 파일의 전체 내용은 인덱싱됩니다. PDF 파일의 다음 부분은 인덱싱됩니다.

* 제목
* 키워드
* 제목(설명)
* 텍스트 기반 컨텐츠

## PDF 파일에서 색인화되지 않는 항목은 무엇입니까?{#section_A14B353AE503408896BACBBF3F748FA0}

PDF 목차, 파일 내의 그래픽 또는 포함된 그래픽에 포함된 모든 텍스트는 색인이 적용되지 않습니다.

## 색인화된 PDF 파일은 어떻게 카운트됩니까?{#section_C35DE36A65D649BD8FF314E9EFD990A6}

각 PDF 파일은 여러 페이지가 포함된 PDF를 포함하여 단일 문서로 계산됩니다.

## 검색 결과에 PDF 아이콘이 표시될 수 있습니까?{#section_829CE82CC3544502A13D27C4DB820189}

예. 템플릿 내의 `<search-if-link-extension>` 태그를 사용하여 검색 결과에 PDF 아이콘 또는 다른 그래픽 또는 텍스트를 포함하십시오.

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

PDF 아이콘은 검색 결과가 매우 클 수 있는 PDF 파일에 연결된다는 것을 고객이 알 수 있도록 도와줍니다. 파일 크기는 모뎀이나 모바일 장치를 통해 웹 사이트에 액세스하는 고객에게 문제가 될 수 있습니다.

## 검색 결과가 PDF 파일의 특정 페이지에 링크될 수 있습니까?{#section_A06E7F7017E6441E98209D288EE57BF6}

예. 고객은 스마트 링크 템플릿 태그( `<search-smart-link>...</search-smart-link>`)를 클릭하여 검색 결과가 포함된 첫 번째 PDF 페이지를 열 수 있습니다.

스마트 링크를 사용하려면 템플릿의 검색 결과 섹션에 있는 `<search-link>...</search-link>` 태그를 `<search-smart-link>...</search-smart-link>` 태그로 바꾸십시오. 고객은 스마트 링크 태그가 생성하는 링크를 클릭하면 검색 쿼리와 관련된 첫 번째 PDF 페이지로 이동합니다.

>[!NOTE]
>
>이 기능을 사용하려면 강조 표시 플러그인과 EWH(External Window Handler) 플러그인을 포함해야 하는 최신 버전의 Adobe Acrobat 또는 Adobe Acrobat Reader을 사용해야 합니다. 또한 웹 브라우저는 Netscape Navigator용 Adobe Acrobat 플러그인을 사용해야 합니다(이 Netscape Navigator 플러그인을 허용하는 모든 브라우저를 사용할 수 있음). Internet Explorer 4.0 이상용 Acrobat ActiveX 컨트롤을 사용해야 합니다.

[검색 템플릿 태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)를 참조하십시오.

## 웹 사이트에서 PDF 파일이 인덱싱되지 않도록 하려면 어떻게 해야 합니까?{#section_96671419A822486AAC654D8DAD819940}

검색 로봇이 PDF 파일을 크롤링하고 색인화하지 않도록 하려면 콘텐트 유형 **[!UICONTROL PDF Documents]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)의 선택을 취소합니다.

또한 [!DNL URL Masks]을 사용하여 PDF 색인을 비활성화할 수도 있습니다.

색인 부분에 [URL 마스크 추가...의 인덱스 부분이 아닌 URL 마스크를 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

PDF 색인을 비활성화하려면 다음 URL 마스크 중 하나를 입력합니다.

* `exclude *.pdf` (정규 표현식을 사용하지 않는 경우)
* `exclude regexp ^.*\.pdf$` (정규 표현식을 사용하는 경우)

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

## 웹 사이트에서 중국어, 일본어 또는 한국어 PDF 파일을 검색할 수 없는 이유는 무엇입니까?{#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

사이트 검색/머천다이징은 PDF 파일에서 언어를 표시하지 않고 UTF-8을 가져옵니다. 내용 유형 **[!UICONTROL PDF Documents]**( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**)을 선택한 경우 메타데이터 주입을 사용하여 PDF 파일에 사용되는 언어를 지정해야 합니다.

[필드 삽입 정의 추가](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)를 참조하십시오.

## 페이지 {#reference_48A748BC1ED14844ACAC2735C8388E8A}이(가) 너무 많습니다.

인덱서가 실제로 사용자가 보유한 페이지보다 많은 페이지를 계산했고 각 경우에 솔루션이 무엇인지 몇 가지 이유를 설명하는 FAQ 페이지입니다.

웹 사이트가 페이지 제한보다 낮다고 판단되지만 인덱서가 제한에 도달했다고 하는 경우 이러한 일반적인 질문과 답변을 검토하여 가능한 해결 방법을 찾아야 합니다.

* [다양한 색인 로그를 검토했습니까?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [CGI 프로그램이 웹 사이트에서 인덱싱되고 있습니까?](#section_86ED8A641B3841EC80153B4F107548FD)
* [서버에서 디렉터리 검색을 사용하도록 설정합니까?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [웹 사이트에 포럼이나 뉴스 그룹이 있습니까?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [웹 사이트에 PDF 또는 Microsoft Office 파일이 있습니까?..](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [여러 개의 URL 시작 지점이 있습니까?](#section_8C54AFD7DF56472A9364D516482B534C)
* [내부 바이트 또는 시간 제한(..)을 초과했습니다.](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## 다양한 색인 로그를 검토했습니까?{#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

색인 로그는 웹 사이트를 색인화할 때 사이트 검색/머천다이징 로봇이 수집한 자세한 정보를 포함합니다. 로그에는 크롤링된 모든 링크 및 발생한 오류 목록이 포함되어 있습니다. 색인 로그를 검사하면 색인화된 페이지를 확인할 때 시작할 수 있습니다.

라이브 또는 스테이징의 전체 인덱스 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).[

라이브 또는 스테이징의 증분 인덱스 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).[

라이브 또는...의 스크립트 증분 인덱스 로그 보기를 참조하십시오.](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).[

라이브 또는 스테이징의 재생성된 색인 로그 보기...를 참조하십시오.](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).[

라이브 또는 스테이징된 웹 사이트의 등급 다시 지정 색인 로그 보기](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D)를 참조하십시오.[

## CGI 프로그램이 웹 사이트에서 인덱싱되고 있습니까?{#section_86ED8A641B3841EC80153B4F107548FD}

CGI 프로그램은 때로 인덱서가 여러 &quot;조작&quot; URL을 크롤하도록 하는 URL 매개 변수를 사용합니다. 사이트 검색/머천다이징이 CGI 프로그램을 읽고 CGI 매개 변수가 포함된 URL을 따르는 경우 검색 색인에 유용하지 않은 여러 개의 페이지 크롤링과 인덱싱된 페이지가 있을 수 있습니다. 일반적인 CGI 매개 변수는 `?` 또는 `&` 문자가 있는 URL에 나타납니다.

URL 마스크 기능을 사용하여 CGI 프로그램이 인덱싱되지 않도록 마스크를 적용할 수 있습니다. URL 접두어를 마스크하거나 일반 표현식을 사용하여 CGI 스크립트를 마스크할 수 있습니다.

[URL 마스크 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)를 참조하십시오.

[URL 마스크 정보 스크립트](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)를 참조하십시오.

[정규 표현식](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A)을 참조하십시오.

## 서버에서 디렉터리 검색을 사용하도록 설정합니까?{#section_073C88EEE74F4CA0AD2C7145D4810B22}

웹 서버에 디렉토리 탐색을 사용할 수 있고 해당 디렉토리에 index.html 파일이 없는 경우 해당 디렉토리를 방문하면 해당 디렉토리에 있는 파일의 목록을 표시할 수 있습니다. 일반적으로 페이지 맨 위에는 **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]** 등을 클릭하여 목록을 다른 방법으로 정렬할 수 있는 링크가 있습니다. 일반적으로 이러한 URL은 사이트 검색/머천다이징 색인 로그에 `?M=A`과 같은 문자가 끝에 있는 URL로 표시됩니다. 사이트 검색/머천다이징 인덱서는 다음과 같이 링크되며, 이로 인해 여러 &quot;위조&quot; URL을 인덱싱할 수 있습니다.

일반적으로 잘 설계된 웹 사이트에는 모든 디렉토리에 인덱스 파일이 있거나 인덱스 파일이 없는 해당 디렉토리에 대해 디렉토리 검색이 비활성화되어 있습니다. 페이지를 변경하거나 서버측에서 디렉토리 목록을 비활성화할 수 없는 경우 이러한 &quot;가짜&quot; URL을 손쉽게 마스크를 적용할 수 있습니다.

이 작업을 수행하려면 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다. `?` 문자가 포함된 URL에 마스크를 추가합니다. 다음과 같은 정규 표현식 마스크를 입력하여 이 작업을 수행할 수 있습니다.

`exclude regexp ^.*\?.*$`

마스크를 만든 후 웹 사이트를 다시 색인화해야 합니다.

라이브 또는 스테이징된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).[

라이브 또는 스테이징된 웹 사이트의 증분 인덱스 실행 중...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).[

## 웹 사이트에 포럼이나 뉴스 그룹이 있습니까?{#section_8DCB94F0850A41B9B2EA885F779E2F84}

웹 사이트에서 포럼이나 뉴스 그룹이 크롤되는 경우 다른 표시 옵션 또는 정렬 옵션에 대해 URL을 팔로우할 수 있습니다. 이 비헤이비어는 동일한 페이지가 여러 번 인덱싱됨을 의미합니다.

일반적으로 포럼이나 뉴스 그룹에는 자체 검색 엔진이 있습니다. 이러한 경우 [!DNL URL Masks]을(를) 사용하여 사이트 검색/머천다이징에서 포럼을 숨길 수 있습니다.

제품 메뉴에서 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**&#x200B;를 클릭합니다. [!DNL Staged URL Masks] 페이지에서 URL을 제외 URL 마스크로 입력하여 포럼에 마스크를 적용합니다.

색인 부분에 [URL 마스크 추가...의 인덱스 부분이 아닌 URL 마스크를 참조하십시오.](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

마스크를 만든 후 웹 사이트의 색인을 다시 지정했는지 확인합니다.

라이브 또는 스테이징된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).[

라이브 또는 스테이징된 웹 사이트의 증분 인덱스 실행 중...을 참조하십시오.](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).[

## 웹 사이트에 PDF 또는 Microsoft Office 파일이 있습니까?{#section_455FC5438DF74E68AB9A31D359EAD4D9}

웹 사이트에 PDF 파일 또는 [!DNL Microsoft Office] 파일이 있는 경우 몇 개의 파일의 인덱스 크기만 많은 페이지를 카운트한다는 것을 알 수 있습니다. PDF 또는 Microsoft Office 파일의 각 페이지가 별도의 페이지로 계산되기 때문에 문서에 비해 색인이 많은 페이지가 있습니다.

제품 메뉴에서 **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**&#x200B;를 클릭합니다. [!DNL Full Index] 페이지에서 **[!UICONTROL Count All Pages]**&#x200B;을 선택한 다음 **[!UICONTROL Full Index Now]**&#x200B;를 클릭하여 총 페이지 수를 확인합니다. PDF 파일이나 Microsoft Office 파일을 인덱싱하지 않으려면 **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**&#x200B;에서 이 콘텐트 유형을 비활성화할 수 있습니다.

라이브 또는 스테이징된 웹 사이트의 전체 인덱스 실행...을 참조하십시오.](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).[

[콘텐트 유형 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)를 참조하십시오.

## 여러 개의 URL 시작 지점이 있습니까?{#section_8C54AFD7DF56472A9364D516482B534C}

사이트 검색/머천다이징 로봇은 지정된 URL 시작 지점에서 크롤링을 시작하고 특정 도메인의 모든 콘텐츠에 대한 모든 검색 링크를 따릅니다. 많은 URL 시작 지점을 지정한 경우 상당한 수의 페이지가 크롤될 수 있습니다.

추가 도메인의 시작 지점 문서 헤더에 있는 Robots Exclusion Protocol의 `nofollow` 태그를 다음과 같이 사용하십시오.

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

위의 코드는 사이트 검색/머천다이징 로봇에 페이지 컨텐츠를 색인화하도록 지시하지만 추가 페이지에 대한 링크를 따라가지 않도록 합니다.

웹 로봇과 로봇 제외 프로토콜에 대한 자세한 내용은 다음 링크를 참조하십시오.

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

추가 도메인의 페이지 소스에 대한 액세스 권한이 없는 경우 여러 URL 진입점을 제거할 수 있습니다. 이렇게 하면 색인 활동을 고객이 검색할 수 있게 하려는 컨텐츠가 있는 도메인에만 제한할 수 있습니다.

[URL 시작 지점 정보](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)를 참조하십시오.

## 사이트 검색/머천다이징의 내부 바이트 또는 시간 제한을 초과했습니다.{#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

계정이 &quot;전체 색인 상태&quot; 화면에서 한도에 도달했는지 확인하십시오. 상태 보고서에서 색인이 허용된 것보다 크거나 허용된 것보다 시간이 더 많이 걸렸다고 보고하는 경우 웹 사이트가 완전히 인덱싱되지 않습니다. 웹 사이트 페이지의 적절한 범위 및 카운트를 얻으려면 이 오류를 수정할 수 있습니다.

사이트 검색/머천다이징 서버를 보호하기 위해 바이트 및 시간에 대한 내부 제한이 있습니다. 크롤링된 파일이 매우 클 때 또는 사이트 검색/머천다이징이 도달하려고 하는 서버가 느려질 때만 이러한 제한에 도달했습니다.

시간 제한에 도달하는 경우 서버가 온라인 상태인지 확인하고 나중에 색인을 다시 시도하십시오. 바이트 제한에 도달하는 경우 인덱스 로그를 보고 크롤링된 파일을 확인합니다. 비정상적으로 크나요? 이러한 메시지 중 하나가 표시되면 기술 지원에 문의하십시오.
