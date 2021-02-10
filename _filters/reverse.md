---
title: reverse
description: 배열 또는 배열로 변환된 문자열을 반전시키는 Liquid 필터
---

배열의 항목 순서를 반전시킵니다. 문자열은 반전시킬 수 없습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
```

`reverse`로 문자열을 직접 반전시킬 수 없지만, 문자열을 배열로 분할하고 그 배열을 반전시킨 다음, 필터로 다시 연결할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
```
