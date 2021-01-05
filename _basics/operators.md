---
title: 연산자
description: 연산자를 사용하여 Liquid 템플릿 언어로 계산 수행 가능.
---

Liquid에는 많은 논리/비교 연산자가 있습니다.

## 기본적인 연산자

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

태그 내에 여러 개의 연산자를 사용할 수도 있습니다:

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
  이 product의 title에는 Pack이라는 단어가 포함되어 있습니다.
{% endif %}
{% endraw %}
```

문자열 배열 내에 특정 문자열이 있는지 검사할 수도 있습니다.

```liquid
{% raw %}
{% if product.tags contains "Hello" %}
  이 제품의 tags는 "Hello"라는 이름을 갖고 있습니다.
{% endif %}
{% endraw %}
```

오직 문자열만 찾습니다. 객체 배열 내에 특정 객체가 있는지 검사할 수는 없습니다.

## 연산자의 순서

태그 내에 하나보다 많은 `and` 또는 `or` 연산자가 포함된 경우, 연산자는 오른쪽에서 왼쪽 순서대로 검사됩니다. 소괄호로 순서를 변경할 수 없고, Liquid에서 유효하지 않은 기호인 소괄호가 포함된 코드는 작동하지 않습니다.

```liquid
{% raw %}
{% if true or false and false %}
  `and` 조건이 먼저 검사되었으므로 true로 평가됩니다.
{% endif %}
{% endraw %}
```

```liquid
{% raw %}
{% if true and false and false or true %}
  태그는 다음과 같이 검사되었으므로 false로 평가됩니다:

  true and (false and (false or true))
  true and (false and true)
  true and false
  false
{% endif %}
{% endraw %}
```
