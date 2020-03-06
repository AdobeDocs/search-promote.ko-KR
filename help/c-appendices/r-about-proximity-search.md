---
description: 근접 검색 기능을 사용하면 고유한 위치를 웹 사이트의 모든 페이지와 연결한 다음 해당 위치에서 근접(거리)하여 결과를 검색 및 정렬할 수 있습니다.
seo-description: 근접 검색 기능을 사용하면 고유한 위치를 웹 사이트의 모든 페이지와 연결한 다음 해당 위치에서 근접(거리)하여 결과를 검색 및 정렬할 수 있습니다.
seo-title: 근접 검색 정보
solution: Target
title: 근접 검색 정보
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# 근접 검색 정보{#about-proximity-search}

근접 검색 기능을 사용하면 고유한 위치를 웹 사이트의 모든 페이지와 연결한 다음 해당 위치에서 근접(거리)하여 결과를 검색 및 정렬할 수 있습니다.

예를 들어, 다음과 같은 미국 우편 번호 메타데이터가 있는 웹 사이트의 페이지를 채워왔다고 가정합니다.

```
<meta name="zipcode" content="84057">
```

그런 다음 ZIP 코드 메타데이터를 색인화하도록 계정을 구성합니다. > **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]**&#x200B;페이지에서 [!DNL Add Field] 다음 옵션을 설정합니다.

* 필드 이름: `zip`
* 메타 태그 이름: `zipcode`
* 데이터 유형: **[!UICONTROL Location]**
* 정렬: **[!UICONTROL Ascending]**
* 기본 단위: **[!UICONTROL Miles]**

사이트를 인덱싱한 후 다음 검색을 수행합니다.

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

결과 세트에는 우편번호 84057의 100마일 내에 있는 모든 문서가 들어 있으며, 이 우편번호로부터 거리를 오름차순으로 정렬됩니다.

미국 위치에 대한 전화 지역 코드를 사용할 수도 있습니다. 또는 위도/경도 쌍을 사용하여 사이트 메타데이터와 검색 기준의 위치를 지정할 수 있습니다. 위치 유형은 제공된 데이터의 양식에서 자동으로 결정됩니다.

세 자리 위치 값(&quot;DDD&quot;, 여기서 각 &quot;D&quot;는 0-9의 십진수 숫자를 나타냅니다)은 미국 전화 영역 코드로 처리됩니다.

5자리 또는 5개의 대시-4자리 위치 값(&quot;DDDD&quot; 또는 &quot;DDD-DDD&quot;)은 미국 우편 번호(ZIP)로 처리됩니다.

&quot;DD.DDD DDD DDD.DDD&quot;의 정확한 형식의 위치 값은 위도/경도 쌍으로 처리됩니다. 첫 번째 서명된 숫자 값은 위도, 두 번째 서명된 숫자 값은 경도를 나타냅니다.

**중요**:양수 위도 값, 양수 경도 값 또는 둘 다를 지정할 경우 URL의 &quot;+&quot; 문자를 인코딩해야 합니다 `%2b`. 그렇지 않으면 &quot;+&quot;는 공백으로 해석되며 값이 유효한 위치로 인식되지 않습니다. 예를 들어 위도 값 +49.2394와 경도 값 -123.1892가 있다고 가정합니다.&quot;+&quot;로 인코딩된 URL의 위치 부분은 다음과 같습니다.

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* 양수 위도 값은 적도의 북쪽을 나타냅니다.
* 음수 위도 값은 적도의 남쪽 도를 나타냅니다.
* 양의 경도 값은 Primean의 동쪽을 나타냅니다.
* 음수 경도 값은 Primean의 서쪽을 나타냅니다.

예를 들어 &quot;+48.8577+002.2950&quot; 값은 적도의 북쪽에서 48.8577도, 프랑스 파리에 있는 에펠탑의 정확한 위치인 Primeridian의 동쪽에서 2.295도를 나타냅니다. 숫자 기호와 각 자릿수는 선행 및 후행 0까지 필요합니다. 예를 들어 세 값 &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; 및 &quot;+48.8577+02.295&quot;는 위치가 아닙니다. 첫 번째 값에는 위도의 선행 기호가 없습니다. 두 번째 값에는 경도에 2개의 선행 0이 없습니다. 세 번째 값은 경도에 후행 0이 없습니다. 색인 로그에서 위치 관련 문제를 자세히 검사해야 합니다.

근거리에서 검색할 때 해당 검색에 대해 특수 &quot;근접 출력 필드&quot;가 만들어집니다. 이 필드는 검색 기준에 지정된 위치와 각 검색 결과와 연관된 위치 사이의 상대 거리로 채워집니다. 이 특수 필드의 이름은 &quot;_proximity&quot;가 끝에 추가된 검색 조건에 사용되는 위치 유형 필드에 사용됩니다.

위의 검색 예에서 결과는 &quot;zip_proximity&quot;의 오름차순으로 정렬됩니다. 즉, 지정된 ZIP 코드(84057)와 각 결과의 &quot;zip&quot; 필드 위치 사이의 거리입니다. 또한 이 특수 &quot;근접 출력 필드&quot;를 사용하여 검색 템플릿 태그를 사용하여 각 검색 결과의 상대 거리를 킬로미터 또는 마일 단위로 표시할 수 `<Search-Display-Field>` 있습니다.

템플릿 [태그](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)검색을 참조하십시오.

sp_s 옵션 없이 검색할 수도 있습니다. 이 경우 결과는 점수로 정렬됩니다(sp_s=0(기본값).점수는 sp_q_location[_#] 매개 변수를 통해 지정된 근접 검색 위치의 각 결과의 상대적 거리에 따라 영향을 받습니다. 근접성 검색에 적용되는 관련성 계산을 선택적으로 제어하기 위해 새로운 cgi 매개 변수 sp_q_max_related_distance[#] 가 추가되었습니다.

다음은 근접 연관성 검색 예입니다.

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

결과 세트에는 ZIP 코드 84057의 100마일 내에 있는 모든 문서가 포함되어 있으며 근접 연관성 점수의 영향을 받은 점수로 정렬된 제목 필드에 &quot;shirt&quot;라는 단어가 포함되어 있습니다. 근접 구성 요소에 대한 완벽한 연관성 점수는 0의 거리를 나타냅니다. 근접 구성 요소에 대한 최소 관련성 점수는 50마일 이내입니다.

CGI 매개 변수 검색 참조 항목에서 `sp_location`검토, `sp_location_#`, `sp_q_min``sp_q_min_#``sp_q_max``sp_q_max_#`, `sp_s` 검토및자세한 정보를 참조할 수 있습니다.

CGI [매개 변수](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890)검색을 참조하십시오.

새 [메타 태그 필드](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)추가를 참조하십시오.
