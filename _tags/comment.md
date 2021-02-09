---
title: 주석
description: Liquid 템플릿 언어의 주석 태그에 대한 개요
---

렌더링되지 않은 코드를 Liquid 템플릿 내에 그대로 둘 수 있습니다. `comment` 블록의 여는 부분과 닫는 부분 내부에 포함된 텍스트는 출력되지 않으며, 내부에 포함된 어느 Liquid 코드도 실행되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
무엇이든 {% comment %} 태그 {% endcomment %} 내에 둘 수 있고,
주석으로 변합니다.
{% endraw %}
```

<p class="code-label">출력</p>
```liquid
무엇이든 {% comment %} 태그 {% endcomment %} 내에 둘 수 있고,
주석으로 변합니다.
```
