---
title: Raw
description: Liquid 템플릿 언어의 raw 태그에 대한 개요
---

Raw는 태그 처리를 임시로 비활성화합니다. 충돌이 있는 문법을 사용하는 콘텐츠(예: Mustache, Handlebars)를 생성하는 데 유용합니다.

<p class="code-label">Input</p>
<pre class="highlight">
<code>{% raw %}
&#123;&#37; raw &#37;&#125;
  In Handlebars, {{ this }} will be HTML-escaped, but
  {{{ that }}} will not.
&#123;&#37; endraw &#37;&#125;
{% endraw %}</code>
</pre>

<p class="code-label">Output</p>
```text
{% raw %}In Handlebars, {{ this }} will be HTML-escaped, but {{{ that }}} will not.{% endraw %}
```
