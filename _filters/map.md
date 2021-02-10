---
title: map
description: 객체에서 특정 속성을 추출한 값의 배열을 생성하는 Liquid 필터
---

객체에서 특정 속성을 추출한 값의 배열을 생성합니다.

다음 예시에서 `site.pages`라는 객체가 웹 사이트의 모든 메타데이터를 포함하고 있습니다. `assign`과 `map` 필터를 사용하여 `site.pages` 객체 모든 항목의 `category` 속성값만 포함하는 변수를 생성합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign all_categories = site.pages | map: "category" %}

{% for item in all_categories %}
- {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
- business
- celebrities
- lifestyle
- sports
- technology
```
