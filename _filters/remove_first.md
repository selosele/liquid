---
title: remove_first
description: 문자열의 첫 번째 특정 문자열을 제거하는 Liquid 필터
---

문자열의 첫 번째 특정 문자열만 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
```
