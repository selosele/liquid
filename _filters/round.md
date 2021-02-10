---
title: round
description: 가장 가까운 정수로 반올림하는 Liquid 필터
---

숫자를 가장 가까운 정수로 반올림하거나 숫자가 인수로 전달된 경우 해당 소수 자릿수로 반올림합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 1.2 | round }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 1.2 | round }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 2.7 | round }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 2.7 | round }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | round: 2 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 183.357 | round: 2 }}
```
