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

변수값을 작은 따옴표나 큰 따옴표로 감싸서 문자열을 선언할 수 있습니다.

```liquid
{% raw %}
{% assign my_string = "Hello World!" %}
{% endraw %}
```

## 숫자

숫자는 실수와 정수를 포함합니다.

```liquid
{% raw %}
{% assign my_int = 25 %}
{% assign my_float = 39.756 %}
{% endraw %}
```

## Boolean

Boolean은 `true` 또는 `false`입니다. boolean을 선언할 때 따옴표는 필요하지 않습니다.

```liquid
{% raw %}
{% assign foo = true %}
{% assign bar = false %}
{% endraw %}
```

## Nil

Nil은 Liquid 코드에 결과가 없을 때 반환되는 특수한 빈 값입니다. "nil"이라는 문자열이 **아닙니다**.

조건의 참을 검사하는 Liquid 태그와 `if`절 내에서 [false로 취급됩니다.]({{ "/basics/truthy-and-falsy/#거짓" | prepend: site.baseurl }})

다음 예시에서, user가 존재하지 않을 경우(즉, `user`가 `nil`을 반환) Liquid는 문자열을 출력하지 않습니다:

```liquid
{% raw %}
{% if user %}
  Hello {{ user.name }}!
{% endif %}
{% endraw %}
```

`nil`을 반환하는 태그나 결과는 페이지에 아무 것도 출력하지 않습니다.

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
