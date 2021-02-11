---
title: strip_html
description: 문자열에서 HTML 태그를 제거하는 Liquid 필터
---

문자열에서 모든 HTML 태그를 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Have <em>you</em> read <strong>Ulysses</strong>?" | strip_html }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Have <em>you</em> read <strong>Ulysses</strong>?" | strip_html }}
```
