---
title: truncatewords
description: 지정된 숫자만큼 단어를 줄이는 Liquid 필터
---

인수에 전달된 숫자만큼 문자열의 단어 수를 줄입니다. 지정된 단어 수가 문자열의 단어 수보다 작으면 생략 부호 (...)가 문자열에 추가됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncatewords: 3 }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncatewords: 3 }}
```

### 생략 부호 커스텀

`truncatewords`는 선택적으로 사용 가능한 두 번째 인수를 사용할 수 있으며, 해당 인수는 줄어든 문자열에 추가할 문자열 시퀀스를 지정합니다. 기본값은 생략 부호 (...)이지만 다른 시퀀스를 지정할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncatewords: 3, "--" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncatewords: 3, "--" }}
```

### 생략 부호 미사용

두 번째 인수에 빈 문자열을 전달해서 후행 문자를 표시하지 않게 할 수 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncatewords: 3, "" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "Ground control to Major Tom." | truncatewords: 3, "" }}
```
