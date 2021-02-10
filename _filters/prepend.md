---
title: prepend
description: 문자열의 시작 부분에 특정 문자열을 추가하는 Liquid 필터
---

문자열의 시작 부분에 특정 문자열을 추가합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
```

`prepend`는 변수와 함께 사용될 수도 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign url = "example.com" %}
{{ "/index.html" | prepend: url }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign url = "example.com" %}
{{ "/index.html" | prepend: url }}
```
