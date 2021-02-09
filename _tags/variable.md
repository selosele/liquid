---
title: 변수
description: Liquid 템플릿 언어에서 변수를 생성하는 태그에 대한 개요
---

변수 태그는 새 Liquid 변수를 생성합니다.

## assign

새 변수를 생성합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_variable = false %}
{% if my_variable != true %}
  이 표현은 유효하지 않습니다.
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
이 표현은 유효하지 않습니다.
```

변수에 문자열을 저장하려면 변수값을 따옴표 `"`로 감쌉니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign foo = "bar" %}
{{ foo }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
bar
```

## capture

여는 태그와 닫는 태그 내부의 문자열을 변수에 할당합니다. `capture`로 생성된 변수는 문자열입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% capture my_variable %}I am being captured.{% endcapture %}
{{ my_variable }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
I am being captured.
```

`capture`와 `assign`로 생성된 변수들을 사용하여 복잡한 문자열을 생성할 수 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign favorite_food = "pizza" %}
{% assign age = 35 %}

{% capture about_me %}
I am {{ age }} and my favorite food is {{ favorite_food }}.
{% endcapture %}

{{ about_me }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
I am 35 and my favourite food is pizza.
```

## increment

새 숫자 변수를 생성하고, 호출할 때마다 값을 증가시킵니다. 초기값은 0입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% increment my_counter %}
{% increment my_counter %}
{% increment my_counter %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
0
1
2
```

`increment` 태그로 생성된 변수는 `assign`, `capture` 태그로 생성된 변수는 독립적입니다.

다음 예제에서 `assign` 태그로 "var"라는 이름의 변수가 생성되었고, 그다음 같은 이름의 `increment` 태그가 여러 번 사용되었습니다. `increment` 태그는 `assign` 태그로 생성된 "var"라는 이름의 값에 영향을 미치지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign var = 10 %}
{% increment var %}
{% increment var %}
{% increment var %}
{{ var }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
0
1
2
10
```

## decrement

새 숫자 변수를 생성하고, 호출할 때마다 값을 감소시킵니다. 초기값은 -1입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% decrement variable %}
{% decrement variable %}
{% decrement variable %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
-1
-2
-3
```

[increment](#increment)처럼 `decrement` 태그 내부에 선언된 변수는 `assign`, `capture` 태그로 생성된 변수와 독립적입니다.