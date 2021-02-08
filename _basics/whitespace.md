---
title: 공백 제어
description: Liquid 템플릿 언어의 코드 간 공백 제어에 대한 개요
---

Liquid 태그에 붙임표(hyphen) `{% raw %}{{-{% endraw %}`, `{% raw %}-}}{% endraw %}`, `{% raw %}{%-{% endraw %}`, and `{% raw %}-%}{% endraw %}`를 추가하여 렌더링된 태그의 왼쪽이나 오른쪽 공백을 제거할 수 있습니다.

일반적으로 텍스트를 표출하지 않더라도 렌더링된 HTML에서는 빈 줄이 표출됩니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_variable = "tomato" %}
{{ my_variable }}
{% endraw %}
```

렌더링된 템플릿의 "tomato" 직전에 빈 줄이 보일 겁니다.

<p class="code-label">출력</p>
```text
{% assign my_variable = "tomato" %}
{{ my_variable }}
```

붙임표를 `assign` 태그에 포함하여 렌더링된 템플릿에서 공백을 제거할 수 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{%- assign my_variable = "tomato" -%}
{{ my_variable }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
tomato
```

모든 공백의 표출을 원하지 않으면 모든 태그의 양쪽에 붙임표(`{% raw %}{%-{% endraw %}` and `{% raw %}-%}{% endraw %}`)를 추가합니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign username = "John G. Chalmers-Smith" %}
{% if username and username.size > 10 %}
  Wow, {{ username }}, you have a long name!
{% else %}
  Hello there!
{% endif %}
{% endraw %}
```

<p class="code-label">공백 제어 없는 출력</p>
```text
{% assign username = "John G. Chalmers-Smith" %}
{% if username and username.size > 10 %}
  Wow, {{ username }}, you have a long name!
{% else %}
  Hello there!
{% endif %}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{%- assign username = "John G. Chalmers-Smith" -%}
{%- if username and username.size > 10 -%}
  Wow, {{ username }}, you have a long name!
{%- else -%}
  Hello there!
{%- endif -%}
{% endraw %}
```

<p class="code-label">공백이 제거된 출력</p>
```text
Wow, John G. Chalmers-Smith, you have a long name!
```
