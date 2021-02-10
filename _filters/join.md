---
title: join
description: 문자열 배열을 단일 문자열과 연결하는 Liquid 필터
---

인수를 구분자로 사용하여 배열의 항목을 단일 문자열과 연결합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
```
