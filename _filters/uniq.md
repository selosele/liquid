---
title: uniq
description: 배열에서 중복되는 항목을 제거하는 Liquid 필터
---

배열에서 중복되는 모든 요소를 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "ants, bugs, bees, bugs, ants" | split: ", " %}

{{ my_array | uniq | join: ", " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "ants, bugs, bees, bugs, ants" | split: ", " %}

{{ my_array | uniq | join: ", " }}
```
