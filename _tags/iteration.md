---
title: 반복
description: Liquid 템플릿 언어의 반복 또는 &quot;루프&quot; 태그에 대한 개요
---

반복 태그는 코드 블록을 반복 실행합니다.

## for

코드 블록을 반복 실행합니다. `for`문 내부에서 사용할 수 있는 모든 속성 목록은 [forloop (object)](https://help.shopify.com/themes/liquid/objects/for-loops)에서 확인하십시오.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for product in collection.products %}
  {{ product.title }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
hat shirt pants
```

### else

반복문이 0의 길이를 가지고 있을 경우 실행할 `for`문의 폴백 케이스를 지정합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for product in collection.products %}
  {{ product.title }}
{% else %}
  The collection is empty.
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
The collection is empty.
```

### break

`break` 태그를 만나면 반복문 실행이 중지됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (1..5) %}
  {% if i == 4 %}
    {% break %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
1 2 3
```

### continue

`continue` 태그를 만나면 현재 반복문을 건너뜁니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (1..5) %}
  {% if i == 4 %}
    {% continue %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
1 2 3   5
```

## for (제한)

### limit

반복문 실행 횟수를 지정된 수치 만큼 제한합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array limit:2 %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
1 2
```

### offset

지정된 인덱스부터 반복문을 실행합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array offset:2 %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
3 4 5 6
```

### range

반복문 실행의 범위를 정의합니다. 숫자와 변수로 정의할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (3..5) %}
  {{ i }}
{% endfor %}

{% assign num = 4 %}
{% for i in (1..num) %}
  {{ i }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
3 4 5
1 2 3 4
```

### reversed

반복문의 순서를 뒤바꿉니다. 철자가 비슷한 `reverse` 필터와 다릅니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array reversed %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
6 5 4 3 2 1
```

## cycle

문자열 그룹을 순환한 후 인수에 전달된 순서대로 출력합니다. `cycle`이 호출될 때마다 다음 문자열 인수가 출력됩니다.

`cycle`은 [for](#for)문 내부에서 사용되어야 합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% cycle "one", "two", "three" %}
{% cycle "one", "two", "three" %}
{% cycle "one", "two", "three" %}
{% cycle "one", "two", "three" %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
one
two
three
one
```

`cycle`의 주용도:

- 테이블 행에 홀수/짝수 클래스를 적용할 때
- 행에 있는 마지막 상품 섬네일에 고유 클래스를 적용할 때

## cycle (제한)

하나의 템플릿에서 다수의 `cycle` 블록이 필요할 경우 `cycle`은 "cycle 그룹" 제한을 허용합니다. cycle 그룹에 제공된 이름이 없으면 동일한 제한을 가진 다수의 호출이 하나의 그룹으로 간주됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% cycle "first": "one", "two", "three" %}
{% cycle "second": "one", "two", "three" %}
{% cycle "second": "one", "two", "three" %}
{% cycle "first": "one", "two", "three" %}
{% endraw %}
```

<p class="code-label">출력</p>
```text
one
one
two
two
```

## tablerow

HTML 테이블을 생성합니다. HTML의 여는 태그 `<table>`와 닫는 태그 `</table>`로 감싸져야 합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<table>
{% tablerow product in collection.products %}
  {{ product.title }}
{% endtablerow %}
</table>
{% endraw %}
```

<p class="code-label">출력</p>
```html
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
    <td class="col3">
      Batman Poster
    </td>
    <td class="col4">
      Bullseye Shirt
    </td>
    <td class="col5">
      Another Classic Vinyl
    </td>
    <td class="col6">
      Awesome Jeans
    </td>
  </tr>
</table>
```

## tablerow (제한)

### cols

테이블의 열 수를 정의합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% tablerow product in collection.products cols:2 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

<p class="code-label">출력</p>
```html
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
  </tr>
  <tr class="row2">
    <td class="col1">
      Batman Poster
    </td>
    <td class="col2">
      Bullseye Shirt
    </td>
  </tr>
  <tr class="row3">
    <td class="col1">
      Another Classic Vinyl
    </td>
    <td class="col2">
      Awesome Jeans
    </td>
  </tr>
</table>
```

#### limit

특정 인덱스에서 tablerow 실행을 종료합니다.

```liquid
{% raw %}
{% tablerow product in collection.products cols:2 limit:3 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

### offset

특정 인덱스부터 tablerow를 실행합니다.

```liquid
{% raw %}
{% tablerow product in collection.products cols:2 offset:3 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

### range

반복문 실행의 범위를 정의합니다. 숫자와 변수로 정의할 수 있습니다.

```liquid
{% raw %}
<!--variable number example-->

{% assign num = 4 %}
<table>
{% tablerow i in (1..num) %}
  {{ i }}
{% endtablerow %}
</table>

<!--literal number example-->

<table>
{% tablerow i in (3..5) %}
  {{ i }}
{% endtablerow %}
</table>
{% endraw %}
```
