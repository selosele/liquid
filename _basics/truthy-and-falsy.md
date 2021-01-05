---
title: 참과 거짓
description: Liquid 템플릿 언어의 불리언 로직에 대한 개요
---

프로그래밍에서, 조건부로 `true`를 반환하는 모든 것을 **참**이라고 부르고, `false`를 반환하는 모든 것을 **거짓**이라고 부릅니다. 모든 객체 유형은 참과 거짓으로 설명될 수 있습니다.

- [참](#참)
- [거짓](#거짓)
- [요약](#요약)

## 참

Liquid에서 `nil`과 `false`를 제외한 모든 값은 참입니다.

아래 예시에서, "Tobi"라는 문자열은 불리언이 아니지만 해당 조건에서는 참입니다.

```liquid
{% raw %}
{% assign tobi = "Tobi" %}

{% if tobi %}
  이 조건은 언제나 true입니다.
{% endif %}
{% endraw %}
```

[Strings]({{ "/basics/types/#string" | prepend: site.baseurl }}), even when empty, are truthy. The example below will result in empty HTML tags if `settings.fp_heading` is empty:

<p class="code-label">Input</p>
```liquid
{% raw %}
{% if settings.fp_heading %}
  <h1>{{ settings.fp_heading }}</h1>
{% endif %}
{% endraw %}
```

<p class="code-label">Output</p>
```html
<h1></h1>
```

## 거짓

The falsy values in Liquid are [`nil`]({{ "/basics/types/#nil" | prepend: site.baseurl }}) and [`false`]({{ "/basics/types/#boolean" | prepend: site.baseurl }}).

## 요약

The table below summarizes what is truthy or falsy in Liquid.

|               | truthy        | falsy         |
| ------------- |:-------------:|:-------------:|
| true          | •             |               |
| false         |               | •             |
| nil           |               | •             |
| string        | •             |               |
| empty string  | •             |               |
| 0             | •             |               |
| integer       | •             |               |
| float         | •             |               |
| array         | •             |               |
| empty array   | •             |               |
| page          | •             |               |
| EmptyDrop     | •             |               |
