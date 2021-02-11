---
title: slice
description: 문자열에서 지정된 위치에 있는 문자를 제거하는 Liquid 필터
---

첫 번째 인수에 전달된 지정 인덱스에서 시작하는 1개의 문자를 반환합니다. 선택적으로 사용 가능한 두 번째 인수는 반환될 문자의 길이를 지정합니다.

문자열의 인덱스는 0부터 번호가 매겨집니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 0 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Liquid" | slice: 0 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 2 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Liquid" | slice: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 2, 5 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Liquid" | slice: 2, 5 }}
```

첫 번째 인수가 음수일 경우 인덱스는 문자열의 끝부터 시작합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: -3, 2 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Liquid" | slice: -3, 2 }}
```
