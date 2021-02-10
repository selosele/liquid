---
title: last
description: 배열의 마지막 항목을 반환하는 Liquid 필터
---

배열의 마지막 항목을 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | split: " " | last }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | split: " " | last }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.last }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.last }}
```

태그 내부에서 필터를 사용하려면 `last`를 점 표기법과 함께 사용합니다:

```liquid
{% raw %}
{% if my_array.last == "tiger" %}
  There goes a tiger!
{% endif %}
{% endraw %}
```
