---
title: plus
description: 한 숫자에 다른 숫자를 더하는 Liquid 필터
---

한 숫자에 다른 숫자를 더합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | plus: 2 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 4 | plus: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 16 | plus: 4 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 16 | plus: 4 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | plus: 12 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 183.357 | plus: 12 }}
```
