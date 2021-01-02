---
title: 소개
description: Liquid 템플릿 언어의 객체와 태그, 필터에 대한 개요
redirect_from: /basics/
---

Liquid 코드는 [**객체**](#객체)와 [**태그**](#태그), [**필터**](#필터)로 분류됩니다.

## 객체

**객체**는 페이지에서 내용을 표시할 위치를 Liquid에게 알려줍니다. 객체와 변수명은 이중 중괄호로 표시됩니다: `{% raw %}{{{% endraw %}` and `{% raw %}}}{% endraw %}`.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ page.title }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ page.title }}
```

위 코드에서, Liquid는 `Introduction`이라는 텍스트를 담고 있는 `page.title` 객체의 내용을 렌더링하였습니다. 

## 태그

**태그**는 로직과 템플릿의 제어 흐름을 생성하며, 중괄호와 퍼센트 기호로 표시됩니다: `{% raw %}{%{% endraw %}` and `{% raw %}%}{% endraw %}`.

마크업에 포함된 태그는 어떤 가시적인 텍스트도 생성하지 않습니다. Liquid 로직을 페이지에 표시하지 않고도 변수를 할당하거나 조건문/반복문을 만들 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% if user %}
  Hello {{ user.name }}!
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Hello Adam!
```

태그는 세 가지 유형으로 분류됩니다.

- [제어 흐름]({{ "/tags/control-flow/" | prepend: site.baseurl }})
- [반복문]({{ "/tags/iteration/" | prepend: site.baseurl }})
- [변수 할당]({{ "/tags/variable/" | prepend: site.baseurl }})

태그 유형에 대한 자세한 내용은 각 섹션에서 확인할 수 있습니다. 

## 필터

**필터**는 Liquid 객체의 출력 내용을 변경하며, 출력문 내부에서 `|` 기호로 구분됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "/my/fancy/url" | append: ".html" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "/my/fancy/url" | append: ".html" }}
```

하나의 출력문 내부에서 여러 필터가 사용될 수 있고, 왼쪽부터 오른쪽으로 적용됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "adam!" | capitalize | prepend: "Hello " }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "adam!" | capitalize | prepend: "Hello " }}
```
