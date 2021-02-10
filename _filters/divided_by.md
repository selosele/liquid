---
title: divided_by
description: 숫자를 다른 숫자로 나누는 Liquid 필터
---

숫자를 다른 숫자로 나눕니다.

약수가 정수일 경우 결과 값은 가장 가까운 정수(즉, [floor]({{ "/filters/floor/" | prepend: site.baseurl }}))로 반올림됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 16 | divided_by: 4 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 16 | divided_by: 4 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 5 | divided_by: 3 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 5 | divided_by: 3 }}
```

### 반올림 제어

`divided_by`는 약수와 동일한 유형의 결과를 냅니다 — 즉, 정수로 나누면 결과 값도 정수이고 실수(소수점)로 나누면 결과 값도 실수입니다.

다음 예시에서 약수는 정수입니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 20 | divided_by: 7 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 20 | divided_by: 7 }}
```

실수일 경우:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 20 | divided_by: 7.0 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ 20 | divided_by: 7.0 }}
```

### 변수 유형 변경

변수를 약수로 사용하고 싶은 경우, 실수로 변환하기 위해 `.0`를 추가할 수 없습니다. 이러한 경우 `times` 필터를 사용하여 실수로 변환된 변수 형태를 할당할 수 있습니다.

다음 예시에서 정수를 담고 있는 변수를 나누었고 결과 값은 정수입니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_integer = 7 %}
{{ 20 | divided_by: my_integer }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_integer = 7 %}
{{ 20 | divided_by: my_integer }}
```

실수를 얻기 위해 변수값에 `1.0`을 [곱한]({{ "/filters/times/" | prepend: site.baseurl }}) 다음 나누었습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_integer = 7 %}
{% assign my_float = my_integer | times: 1.0 %}
{{ 20 | divided_by: my_float }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{% assign my_integer = 7 %}
{% assign my_float = my_integer | times: 1.0 %}
{{ 20 | divided_by: my_float }}
```
