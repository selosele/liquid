---
title: modulo
description: 나눗셈 연산의 나머지 값을 반환하는 Liquid 필터
---

나눗셈 연산의 나머지 값을 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 3 | modulo: 2 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 3 | modulo: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 24 | modulo: 7 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 24 | modulo: 7 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | modulo: 12 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 183.357 | modulo: 12 }}
```
