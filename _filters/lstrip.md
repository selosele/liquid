---
title: lstrip
description: 문자열 좌측의 모든 공백을 제거하는 Liquid 필터
---

문자열 좌측의 모든 공백(tabs, spaces, 줄 바꿈)을 제거합니다. 단어 간 띄어쓰기에는 영향을 주지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "          So much room for activities!          " | lstrip }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "          So much room for activities!          " | lstrip }}
```
