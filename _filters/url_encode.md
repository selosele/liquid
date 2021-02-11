---
title: url_encode
description: 문자열에서 URL에 안전하지 않은 문자를 인코딩하는 Liquid 필터
---

문자열에서 URL에 안전하지 않은 모든 문자를 퍼센트 인코딩 문자로 변환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "john@liquid.com" | url_encode }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "john@liquid.com" | url_encode }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Tetsuro Takara" | url_encode }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Tetsuro Takara" | url_encode }}
```
