---
title: split
description: 구분자를 사용하여 문자열을 배열로 분할하는 Liquid 필터
---

인수를 구분자로 사용하여 문자열을 배열로 나눕니다. 일반적으로 쉼표로 구분된 항목을 문자열에서 배열로 변환하는 데 사용됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
```
