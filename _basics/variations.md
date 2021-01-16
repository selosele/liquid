---
title: Liquid의 변종
description: Liquid의 여러 종류 및 사용 환경에 따라 Liquid가 어떻게 변할 수 있는지에 대한 개요
---

Liquid는 수많은 환경에서 사용되는 유동적이고 안전한 언어입니다. [Shopify](https://www.shopify.com){:target="_blank"} 스토어에서 사용하기 위해 만들어졌고, [Jekyll](https://jekyllrb.com){:target="_blank"} 웹사이트에서도 광범위하게 사용됩니다. 시간이 흐르면서, Shopify와 Jekyll은 Liquid에 자신들만의 객체와 태그, 필터를 추가했습니다. 가장 인기 있는 버전은 **Liquid**, **Shopify Liquid**, **Jekyll Liquid** 입니다.

이 사이트는 베타 및 출시 후보를 포함하는 **Liquid** 최신 버전, 즉 Shopify와 Jekyll 버전이 아닌 Liquid를 문서화합니다. Liquid repository를 다운로드하거나 [gem](https://rubygems.org/gems/liquid){:target="_blank"}으로 설치하면, 선택한 Liquid 버전에 있는 모든 객체, 태그, 필터에 접근할 수 있습니다.

## Shopify

Shopify는 항상 Liquid 최신 버전을 기본으로 사용하지만, Liquid에 상당수의 객체, 태그, 필터를 추가해 스토어에서 사용할 수 있도록 합니다. 여기에는 스토어, 제품, 고객 정보를 표현하기 위한 객체와 스토어 데이터를 표시하고 제품 이미지와 같은 스토어 자산을 조작하기 위한 필터가 포함됩니다.

Liquid Shopify 버전은 [Shopify 도움말 센터](https://help.shopify.com/themes/liquid){:target="_blank"}에 문서화되어 있습니다. Liquid Shopify 버전을 사용해보고싶은 경우 [Shopify Partner Dashboard](https://help.shopify.com/en/partners/dashboard/development-stores){:target="_blank"}에서 개발 스토어를 생성할 수 있습니다.

## Jekyll

[Jekyll](https://jekyllrb.com){:target="_blank"}은 정적 사이트 생성기이자, 템플릿과 콘텐츠 파일을 병합하여 웹사이트를 만드는 명령줄 도구입니다. Jekyll은 Liquid를 템플릿 언어로 사용하며, 소수의 객체, 태그, 필터를 추가했습니다. 여기에는 콘텐츠 페이지를 표현하는 객체와 콘텐츠 스니펫을 인클루드하기 위한 태그, 문자열과 URL을 조작하기 위한 필터가 포함됩니다.

Jekyll also powers [GitHub Pages](https://pages.github.com/), a web hosting service that lets you push a Jekyll installation to a GitHub repository and have the resulting website published. This website is built using GitHub Pages.

Jekyll might not be using the latest version of Liquid. This means that the tags and filters listed on this site may not work in Jekyll. Often the Jekyll project will wait for a stable release of Liquid rather than using a beta or release candidate version. To see what version of Liquid Jekyll is using, check the **runtime dependencies** section of [Jekyll's gem page](https://rubygems.org/gems/jekyll).

Jekyll's version of Liquid is documented in the [Liquid section of Jekyll's documentation](https://jekyllrb.com/docs/liquid/). If you want to try out Jekyll's version of Liquid, you can clone the Jekyll project or install Jekyll as a gem and test Liquid on a static site.
