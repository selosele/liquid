---
title: abs
description: 숫자의 절대값을 반환하는 Liquid 필터
redirect_from: /filters/
---

숫자의 절대값을 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ -17 | abs }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ -17 | abs }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | abs }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 4 | abs }}
```

문자열에 숫자만 포함되어 있어도 작동합니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "-19.86" | abs }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "-19.86" | abs }}
```
