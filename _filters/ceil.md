---
title: ceil
description: 가장 가까운 정수로 반올림한 수치값을 반환하는 Liquid 필터
---

숫자를 가장 가까운 정수로 반올림합니다. Liquid는 필터가 적용되기 전의 숫자를 변환하려 합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 1.2 | ceil }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 1.2 | ceil }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 2.0 | ceil }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 2.0 | ceil }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | ceil }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 183.357 | ceil }}
```

입력된 값이 문자열이어도 적용됩니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "3.5" | ceil }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "3.5" | ceil }}
```
