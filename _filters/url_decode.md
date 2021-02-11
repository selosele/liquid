---
title: url_decode
description: 문자열에서 퍼센트 인코딩된 문자를 해독하는 Liquid 필터
---

URL로 인코딩된 문자열이나 [url_encode]({{ "/filters/url_encode/" | prepend: site.baseurl }})에 의해 인코딩된 문자열을 해독합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "%27Stop%21%27+said+Fred" | url_decode }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "%27Stop%21%27+said+Fred" | url_decode }}
```