---
title: sort_natural
description: 대/소문자를 구분하지 않는 순서로 배열을 정렬하는 Liquid 필터
---

대/소문자를 구분하지 않는 순서로 배열의 항목을 정렬합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort_natural | join: ", " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort_natural | join: ", " }}
```

선택적으로 사용 가능한 인수는 정렬에 사용할 배열 항목의 속성을 지정합니다.

```liquid
{% raw %}
{% assign products_by_company = collection.products | sort_natural: "company" %}
{% for product in products_by_company %}
  <h4>{{ product.title }}</h4>
{% endfor %}
{% endraw %}
```
