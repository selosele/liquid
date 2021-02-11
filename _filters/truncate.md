---
title: truncate
description: 지정된 숫자만큼 문자열을 줄이는 Liquid 필터
---

인수에 전달된 숫자만큼 문자열의 문자 수를 줄입니다. 지정된 문자 수가 문자열의 길이보다 작으면 생략 부호 (...)가 문자열에 추가되고 문자 수에 포함됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncate: 20 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncate: 20 }}
```

### 생략 부호 커스텀

`truncate`는 선택적으로 사용 가능한 두 번째 인수를 사용할 수 있으며, 해당 인수는 줄어든 문자열에 추가할 문자열 시퀀스를 지정합니다. 기본값은 생략 부호 (...)이지만 다른 시퀀스를 지정할 수 있습니다.

두 번째 인수의 길이는 첫 번째 인수에 의해 지정된 문자 수에 따라 계산됩니다. 예를 들어 문자를 정확히 10자로 줄이고 3자의 생략 부호를 사용하면 3자부터 줄어드는 것으로 계산되므로 `truncate`의 첫 번째 인수에 **13**을 사용합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncate: 25, ", and so on" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncate: 25, ", and so on" }}
```

### 생략 부호 미사용

첫 번째 인수의 지정된 문자 수로 줄이고 두 번째 인수에 빈 문자열을 전달해서 후행 문자를 표시하지 않게 할 수 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncate: 20, "" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncate: 20, "" }}
```
