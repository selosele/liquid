---
title: escape
description: 문자열에서 안전하지 않은 글자를 이스케이핑하는 Liquid 필터
---

문자열을 이스케이프 시퀀스로 대체(예를 들어 URL에서 문자열이 사용될 수 있게)하여 이스케이핑합니다. 이스케이핑할 문자열이 없으면 처리되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Have you read 'James & the Giant Peach'?" | escape }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Have you read 'James & the Giant Peach'?" | escape }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Tetsuro Takara" | escape }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Tetsuro Takara" | escape }}
```
