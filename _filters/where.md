---
title: where
description: 배열에서 선택하는 Liquid 필터
---

특정 속성값을 가진 객체 또는 기본적으로 [참]({{ "/basics/truthy-and-falsy/#참" | prepend: site.baseurl }}) 값을 포함하는 배열을 생성합니다.

다음 예시에서 제품 목록이 있고 kitchen 제품을 별도로 표시하려 한다고 가정합니다. `where`를 사용하여 `"type"`이 `"kitchen"`인 제품만 포함하는 배열을 생성할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
All products:
{% for product in products %}
- {{ product.title }}
{% endfor %}

{% assign kitchen_products = products | where: "type", "kitchen" %}

Kitchen products:
{% for product in kitchen_products %}
- {{ product.title }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
All products:
- Vacuum
- Spatula
- Television
- Garlic press

Kitchen products:
- Spatula
- Garlic press
```

그 대신 제품 목록을 가지고 있고 구입 가능한 제품만 표시하려고 할 경우, `where`를 대상값이 없는 속성명과 함께 사용하여 `"available"` 값이 [참]({{ "/basics/truthy-and-falsy/#참" | prepend: site.baseurl }})인 모든 제품을 포함할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
All products:
{% for product in products %}
- {{ product.title }}
{% endfor %}

{% assign available_products = products | where: "available" %}

Available products:
{% for product in available_products %}
- {{ product.title }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
All products:
- Coffee mug
- Limited edition sneakers
- Boring sneakers

Available products:
- Coffee mug
- Boring sneakers
```

`where` 필터는 `first` 필터와 연결하면 배열에서 단일 객체를 찾는 데 사용될 수도 있습니다. 다음 예시에서 shirt를 별도로 표시하려 한다고 가정합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign new_shirt = products | where: "type", "shirt" | first %}

Featured product: {{ new_shirt.title }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Featured product: Hawaiian print sweater vest
```
