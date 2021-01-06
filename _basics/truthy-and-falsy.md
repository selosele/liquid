---
title: 참과 거짓
description: Liquid 템플릿 언어의 boolean 로직에 대한 개요
---

프로그래밍에서, 조건부로 `true`를 반환하는 모든 것을 **참**이라고 부르고, `false`를 반환하는 모든 것을 **거짓**이라고 부릅니다. 모든 객체 자료형은 참과 거짓으로 설명될 수 있습니다.

- [참](#참)
- [거짓](#거짓)
- [요약](#요약)

## 참

Liquid에서 `nil`과 `false`를 제외한 모든 값은 참입니다.

아래 예시에서, "Tobi"라는 문자열은 boolean이 아니지만 해당 조건에서는 참입니다.

```liquid
{% raw %}
{% assign tobi = "Tobi" %}

{% if tobi %}
  이 조건은 언제나 true입니다.
{% endif %}
{% endraw %}
```

[문자열]({{ "/basics/types/#문자열" | prepend: site.baseurl }})은 비어 있어도 참입니다. 다음 예시에서는 `settings.fp_heading`이 비어 있으면 빈 HTML 태그가 생성됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% if settings.fp_heading %}
  <h1>{{ settings.fp_heading }}</h1>
{% endif %}
{% endraw %}
```

<p class="code-label">출력</p>
```html
<h1></h1>
```

## 거짓

Liquid에서 거짓 값은 [`nil`]({{ "/basics/types/#nil" | prepend: site.baseurl }})과 [`false`]({{ "/basics/types/#boolean" | prepend: site.baseurl }})입니다.

## 요약

다음 표에는 Liquid의 참과 거짓에 대해 요약이 되어 있습니다.

|           |  참   | 거짓  |
| --------- | :---: | :---: |
| true      |   •   |       |
| false     |       |   •   |
| nil       |       |   •   |
| 문자열    |   •   |       |
| 빈 문자열 |   •   |       |
| 0         |   •   |       |
| 정수      |   •   |       |
| 실수      |   •   |       |
| 배열      |   •   |       |
| 빈 배열   |   •   |       |
| page      |   •   |       |
| EmptyDrop |   •   |       |
