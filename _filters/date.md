---
title: date
description: 날짜를 출력, 구성하는 Liquid 필터
---

타임스탬프를 다른 날짜 형식으로 변환합니다. 구문의 형식은 [`strftime`](http://strftime.net){:target="_blank"}와 동일하며 Ruby의 [`Time.parse`](https://ruby-doc.org/stdlib/libdoc/time/rdoc/Time.html#method-c-parse)와 동일한 형식을 사용합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ article.published_at | date: "%a, %b %d, %y" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
Fri, Jul 17, 15
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ article.published_at | date: "%Y" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
2015
```

문자열이 올바른 날짜 형식으로 구성되어 있으면 `date`가 작동합니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "March 14, 2016" | date: "%b %d, %y" }}
{% endraw %}
```

<p class="code-label">출력</p>
```text
{{ "March 14, 2016" | date: "%b %d, %y" }}
```

현재 시간을 가져오려면 `"now"` (또는 `"today"`)를 `date`에 전달하십시오:

<p class="code-label">입력</p>
```liquid
{% raw %}
This page was last updated at {{ "now" | date: "%Y-%m-%d %H:%M" }}.
{% endraw %}
```

<p class="code-label">출력</p>
```text
This page was last updated at {{ "now" | date: "%Y-%m-%d %H:%M" }}.
```

출력 값은 페이지가 캐시 또는 정적 사이트 생성으로 인해 사용자에게 보여질 때의 시간이 아니라 템플릿에서 페이지가 마지막으로 생성된 시간입니다.