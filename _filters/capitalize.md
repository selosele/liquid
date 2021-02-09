---
title: capitalize
description: Liquid filter that capitalizes the first character of a string.
---

문자열의 첫 번째 문자를 대문자로 표기합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "title" | capitalize }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "title" | capitalize }}
```

`capitalize`는 문자열 첫 단어의 첫 번째 문자만 대문자로 표기합니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "my great title" | capitalize }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "my great title" | capitalize }}
```
