---
title: size
description: 문자열의 문자 수 또는 배열의 항목 수를 반환하는 Liquid 필터
---

문자열의 문자 수 또는 배열의 항목 수를 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | size }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | size }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.size }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.size }}
```

태그 내부에서 `size`를 사용하려면 점 표기법과 함께 사용합니다:

```liquid
{% raw %}
{% if site.pages.size > 10 %}
  This is a big website!
{% endif %}
{% endraw %}
```
