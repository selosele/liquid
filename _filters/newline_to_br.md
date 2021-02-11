---
title: newline_to_br
description: 문자열의 줄 바꿈을 HTML <br /> 태그로 변환하는 Liquid 필터
---

문자열의 모든 줄 바꿈(`\n`)을 HTML 줄 바꿈 `<br />` 태그로 변환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
{% endraw %}
```

<p class="code-label">출력</p>
```html
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
```
