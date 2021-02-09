---
title: at_least
description: 숫자의 최소값을 제한하는 Liquid 필터
---

숫자의 최소값을 제한합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | at_least: 5 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
5
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | at_least: 3 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
4
```
