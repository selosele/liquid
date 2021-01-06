---
title: 자료형
description: Liquid 템플릿 언어의 자료형에 대한 개요
---

Liquid의 객체는 다섯 가지 자료형 중 하나를 가질 수 있습니다.

- [문자열](#문자열)
- [숫자](#숫자)
- [Boolean](#boolean)
- [Nil](#nil)
- [배열](#배열)
  - [Accessing items in arrays](#accessing-items-in-arrays)
  - [Accessing specific items in arrays](#accessing-specific-items-in-arrays)
  - [Initializing arrays](#initializing-arrays)

[assign]({{ "/tags/variable/#assign" | prepend: site.baseurl }}) 또는 [capture]({{ "/tags/variable/#capture" | prepend: site.baseurl }}) 태그로 Liquid 변수를 선언할 수 있습니다.

## 문자열

Declare a string by wrapping a variable's value in single or double quotes:

```liquid
{% raw %}
{% assign my_string = "Hello World!" %}
{% endraw %}
```

## 숫자

Numbers include floats and integers:

```liquid
{% raw %}
{% assign my_int = 25 %}
{% assign my_float = 39.756 %}
{% endraw %}
```

## Boolean

Booleans are either `true` or `false`. No quotations are necessary when declaring a boolean:

```liquid
{% raw %}
{% assign foo = true %}
{% assign bar = false %}
{% endraw %}
```

## Nil

Nil is a special empty value that is returned when Liquid code has no results. It is **not** a string with the characters "nil".

Nil is [treated as false]({{ "/basics/truthy-and-falsy/#falsy" | prepend: site.baseurl }}) in the conditions of `if` blocks and other Liquid tags that check the truthfulness of a statement.

In the following example, if the user does not exist (that is, `user` returns `nil`), Liquid will not print the greeting:

```liquid
{% raw %}
{% if user %}
  Hello {{ user.name }}!
{% endif %}
{% endraw %}
```

Tags or outputs that return `nil` will not print anything to the page.

<p class="code-label">입력</p>
```liquid
{% raw %}
The current user is {{ user.name }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
The current user is
```

## 배열

Arrays hold lists of variables of any type.

### Accessing items in arrays

To access all the items in an array, you can loop through each item in the array using an [iteration tag]({{ "/tags/iteration/" | prepend: site.baseurl }}).

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if site.users = "Tobi", "Laura", "Tetsuro", "Adam" -->
{% for user in site.users %}
  {{ user }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Tobi Laura Tetsuro Adam
```

### Accessing specific items in arrays

You can use square bracket `[` `]` notation to access a specific item in an array. Array indexing starts at zero.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if site.users = "Tobi", "Laura", "Tetsuro", "Adam" -->
{{ site.users[0] }}
{{ site.users[1] }}
{{ site.users[3] }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Tobi
Laura
Adam
```

### Initializing arrays

You cannot initialize arrays using only Liquid.

You can, however, use the [split]({{ "/filters/split/" | prepend: site.baseurl }}) filter to break a string into an array of substrings.
