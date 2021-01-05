---
title: 연산자
description: 연산자를 사용하여 Liquid 템플릿 언어로 계산을 수행할 수 있음.
---

Liquid는 많은 논리/비교 연산자를 갖고 있습니다.

## 기초 연산자

<table>
  <tbody>
    <tr>
      <td><code>==</code></td>
      <td>동등</td>
    </tr>
    <tr>
      <td><code>!=</code></td>
      <td>동등하지 않음</td>
    </tr>
    <tr>
      <td><code>&gt;</code></td>
      <td>초과</td>
    </tr>
    <tr>
      <td><code>&lt;</code></td>
      <td>미만</td>
    </tr>
    <tr>
      <td><code>&gt;=</code></td>
      <td>이상</td>
    </tr>
    <tr>
      <td><code>&lt;=</code></td>
      <td>이하</td>
    </tr>
    <tr>
      <td><code>or</code></td>
      <td>또는</td>
    </tr>
    <tr>
      <td><code>and</code></td>
      <td>그리고</td>
    </tr>
  </tbody>
</table>

예시:

```liquid
{% raw %}
{% if product.title == "Awesome Shoes" %}
  These shoes are awesome!
{% endif %}
{% endraw %}
```

태그 내에 다중 연산자를 사용할 수도 있습니다:

```liquid
{% raw %}
{% if product.type == "Shirt" or product.type == "Shoes" %}
  This is a shirt or a pair of shoes.
{% endif %}
{% endraw %}
```

## contains

`contains`은 문자열 내에 특정 문자열이 있는지 검사합니다.

```liquid
{% raw %}
{% if product.title contains "Pack" %}
  This product's title contains the word Pack.
{% endif %}
{% endraw %}
```

문자열 배열 내에 특정 문자열이 있는지 검사할 수도 있습니다.

```liquid
{% raw %}
{% if product.tags contains "Hello" %}
  This product has been tagged with "Hello".
{% endif %}
{% endraw %}
```

오직 문자열만 찾습니다. 위의 코드처럼 객체 배열 내에 특정 객체가 있는지 검사할 수는 없습니다.

## Order of operations

In tags with more than one `and` or `or` operator, operators are checked in order *from right to left*. You cannot change the order of operations using parentheses — parentheses are invalid characters in Liquid and will prevent your tags from working.

```liquid
{% raw %}
{% if true or false and false %}
  This evaluates to true, since the `and` condition is checked first.
{% endif %}
{% endraw %}
```

```liquid
{% raw %}
{% if true and false and false or true %}
  This evaluates to false, since the tags are checked like this:

  true and (false and (false or true))
  true and (false and true)
  true and false
  false
{% endif %}
{% endraw %}
```
