---
title: escape_once
description: 문자열에서 안전하지 않은 글자를 한 번 이스케이핑하는 Liquid 필터
---

기존 이스케이핑된 엔티티를 변경하지 않고 문자열을 이스케이핑합니다. 이스케이핑할 문자열이 없으면 처리되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "1 < 2 & 3" | escape_once }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "1 < 2 & 3" | escape_once }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "1 &lt; 2 &amp; 3" | escape_once }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "1 &lt; 2 &amp; 3" | escape_once }}
```
