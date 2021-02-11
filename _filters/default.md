---
title: default
description: 값이 존재하지 않을 때의 폴백 케이스를 명시하는 Liquid 필터
---

값이 존재하지 않을 때의 폴백 케이스를 지정합니다. `default`는 좌측 값이 `nil`, `false` 또는 비어 있을 경우 표출됩니다.

다음 예시에서 `product_price`가 정의되지 않았고 기본값이 사용되었습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
2.99
```

다음 예시에서는 `product_price`이 정의되었고 기본값이 사용되지 않았습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign product_price = 4.99 %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
4.99
```

다음 예시에서는 `product_price`이 비어 있고 기본값이 사용되었습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign product_price = "" %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
2.99
```
