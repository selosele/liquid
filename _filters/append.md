---
title: append
description: 문자열에 다른 문자열을 덧붙이는 Liquid 필터
---

두 개의 문자열을 연결시키고, 그 값을 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "/my/fancy/url" | append: ".html" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "/my/fancy/url" | append: ".html" }}
```

`append`는 변수와 함께 사용할 수도 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
```
