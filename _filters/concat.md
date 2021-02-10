---
title: concat
description: 배열을 합치는 Liquid 필터
---

다수의 배열을 하나로 연결(결합)합니다. 결과 배열에는 입력된 모든 배열 항목이 포함됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign fruits = "apples, oranges, peaches" | split: ", " %}
{% assign vegetables = "carrots, turnips, potatoes" | split: ", " %}

{% assign everything = fruits | concat: vegetables %}

{% for item in everything %}
- {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
- apples
- oranges
- peaches
- carrots
- turnips
- potatoes
```

`concat` 필터로 두 개 이상의 배열을 연결할 수도 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign furniture = "chairs, tables, shelves" | split: ", " %}

{% assign everything = fruits | concat: vegetables | concat: furniture %}

{% for item in everything %}
- {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
- apples
- oranges
- peaches
- carrots
- turnips
- potatoes
- chairs
- tables
- shelves
```
