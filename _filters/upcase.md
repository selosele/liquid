---
title: upcase
description: 문자열을 대문자로 변환하는 Liquid 필터
---

문자열의 각 문자를 대문자로 만듭니다. 이미 모두 대문자인 문자열에는 영향을 미치지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Parker Moore" | upcase }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Parker Moore" | upcase }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "APPLE" | upcase }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "APPLE" | upcase }}
```
