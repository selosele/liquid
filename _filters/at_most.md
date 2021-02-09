---
title: at_most
description: 숫자의 최대값을 제한하는 Liquid 필터
---

숫자의 최대값을 제한합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | at_most: 5 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
4
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | at_most: 3 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
3
```
