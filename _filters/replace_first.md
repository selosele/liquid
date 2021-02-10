---
title: replace_first
description: 문자열의 첫 번째 특정 문자열을 대체하는 Liquid 필터
---

문자열에서 첫 번째 인수의 첫 번째 값만 두 번째 인수의 것으로 대체합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Take my protein pills and put my helmet on" | replace_first: "my", "your" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Take my protein pills and put my helmet on" | replace_first: "my", "your" }}
```
