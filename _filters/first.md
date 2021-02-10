---
title: first
description: 배열의 첫 번째 항목을 반환하는 Liquid 필터
---

배열의 첫 번째 항목을 반환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | split: " " | first }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | split: " " | first }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.first }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.first }}
```

태그 내부에서 필터를 사용하려면 `first`를 점 표기법과 함께 사용합니다:

```liquid
{% raw %}
{% if my_array.first == "zebra" %}
  Here comes a zebra!
{% endif %}
{% endraw %}
```
