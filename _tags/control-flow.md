---
title: 제어 흐름
description: Liquid 템플릿 언어의 제어 흐름과 조건문 태그에 대한 개요
redirect_from: /tags/
---

제어 흐름 태그는 Liquid가 보여 주는 정보를 프로그래밍 로직을 사용하여 바꿀 수 있습니다.

## if

특정 조건이 `true`(참)일 경우에만 코드 블록을 실행합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% if product.title == "Awesome Shoes" %}
  These shoes are awesome!
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
These shoes are awesome!
```

## unless

`if`의 반대로서, 특정 조건이 **충족되지 않는** 경우에만 코드 블록을 실행합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% unless product.title == "Awesome Shoes" %}
  These shoes are not awesome.
{% endunless %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
These shoes are not awesome.
```

다음과 같이 작성하는 것과 동일합니다:

```liquid
{% raw %}
{% if product.title != "Awesome Shoes" %}
  These shoes are not awesome.
{% endif %}
{% endraw %}
```

## elsif / else

`if` 또는 `unless` 블록 내에 더 많은 조건문을 추가합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- If customer.name = "anonymous" -->
{% if customer.name == "kevin" %}
  Hey Kevin!
{% elsif customer.name == "anonymous" %}
  Hey Anonymous!
{% else %}
  Hi Stranger!
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Hey Anonymous!
```

## case/when

변수를 다른 값과 비교하는 switch문을 만듭니다. `case`로 switch문을 초기화, `when`로 값을 비교합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign handle = "cake" %}
{% case handle %}
  {% when "cake" %}
     This is a cake
  {% when "cookie" %}
     This is a cookie
  {% else %}
     This is not a cake nor a cookie
{% endcase %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
This is a cake
```
