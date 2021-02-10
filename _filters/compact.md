---
title: compact
description: 배열에서 nil 값을 제거하는 Liquid 필터
---

배열에서 모든 `nil` 값을 제거합니다.

다음 예시에서 `site.pages`는 웹 사이트의 콘텐츠 페이지 배열이며, 이러한 페이지 중 일부는 콘텐츠 카테고리를 명시하는 `category`라는 속성을 가지고 있습니다. 이러한 카테고리를 배열에 `map`하면, 일부 페이지가 `category` 속성을 가지고 있지 않을 경우 일부 배열 항목이 `nil`이 될 수 있습니다.

<p class="code-label">Input</p>
```liquid
{% raw %}
{% assign site_categories = site.pages | map: "category" %}

{% for category in site_categories %}
- {{ category }}
{% endfor %}
{% endraw %}
```

<p class="code-label">Output</p>
```text
- business
- celebrities
-
- lifestyle
- sports
-
- technology
```

`site_categories` 배열을 생성할 때 `compact`로 배열의 모든 `nil` 값을 제거할 수 있습니다.

<p class="code-label">Input</p>
```liquid
{% raw %}
{% assign site_categories = site.pages | map: "category" | compact %}

{% for category in site_categories %}
- {{ category }}
{% endfor %}
{% endraw %}
```

<p class="code-label">Output</p>
```text
- business
- celebrities
- lifestyle
- sports
- technology
```
