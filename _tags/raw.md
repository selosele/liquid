---
title: Raw
description: Liquid 템플릿 언어의 raw 태그에 대한 개요
---

Raw는 태그 처리를 임시로 비활성화합니다. 충돌이 있는 문법을 사용하는 콘텐츠(예: Mustache, Handlebars)를 생성하는 데 유용합니다.

<p class="code-label">입력</p>
<pre class="highlight">
<code>{% raw %}
&#123;&#37; raw &#37;&#125;
  Handlebars에서 {{ 이것 }}은 HTML 이스케이핑 처리되지만 
  {{{ 이것 }}}은 처리되지 않습니다.
&#123;&#37; endraw &#37;&#125;
{% endraw %}</code>
</pre>

<p class="code-label">출력</p>
```text
{% raw %}Handlebars에서 {{ 이것 }}은 HTML 이스케이핑 처리되지만 {{{ 이것 }}}은 처리되지 않습니다.{% endraw %}
```
