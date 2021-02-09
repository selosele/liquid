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
  This statement is valid.
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
This statement is valid.
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

Captures the string inside of the opening and closing tags and assigns it to a variable. Variables created through `capture` are strings.

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

Using `capture`, you can create complex strings using other variables created with `assign`:

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

Creates a new number variable, and increases its value by one every time it is called. The initial value is 0.

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

Variables created through the `increment` tag are independent from variables created through `assign` or `capture`.

In the example below, a variable named "var" is created through `assign`. The `increment` tag is then used several times on a variable with the same name. Note that the `increment` tag does not affect the value of "var" that was created through `assign`.

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

Creates a new number variable, and decreases its value by one every time it is called. The initial value is -1.

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

Like [increment](#increment), variables declared inside `decrement` are independent from variables created through `assign` or `capture`.
