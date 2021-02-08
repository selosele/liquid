---
title: Liquid의 변종
description: Liquid의 여러 종류 및 사용 환경에 따라 Liquid가 어떻게 변할 수 있는지에 대한 개요
---

Liquid는 수많은 환경에서 사용되는 유동적이고 안전한 언어입니다. [Shopify](https://www.shopify.com){:target="_blank"} 스토어에서 사용하기 위해 만들어졌고, [Jekyll](https://jekyllrb.com){:target="_blank"} 웹사이트에서도 광범위하게 사용됩니다. 시간이 흐르면서, Shopify와 Jekyll은 Liquid에 자신들만의 객체와 태그, 필터를 추가했습니다. 가장 인기 있는 버전은 **Liquid**, **Shopify Liquid**, **Jekyll Liquid** 입니다.

이 사이트는 베타 및 출시 후보를 포함하는 **Liquid** 최신 버전, 즉 Shopify와 Jekyll 버전이 아닌 Liquid를 문서화합니다. Liquid repository를 다운로드하거나 [gem](https://rubygems.org/gems/liquid){:target="_blank"}으로 설치하면 선택한 Liquid 버전에 있는 모든 객체, 태그, 필터에 접근할 수 있습니다.

## Shopify

Shopify는 항상 Liquid 최신 버전을 기본으로 사용하지만, Liquid에 상당수의 객체, 태그, 필터를 추가해 스토어에서 사용할 수 있도록 합니다. 여기에는 스토어, 제품, 고객 정보를 표현하기 위한 객체와 스토어 데이터를 표시하고 제품 이미지와 같은 스토어 자산을 조작하기 위한 필터가 포함됩니다.

Liquid Shopify 버전은 [Shopify 도움말 센터](https://help.shopify.com/themes/liquid){:target="_blank"}에 문서화되어 있습니다. Liquid Shopify 버전을 사용해보고싶은 경우 [Shopify Partner Dashboard](https://help.shopify.com/en/partners/dashboard/development-stores){:target="_blank"}에서 개발 스토어를 생성할 수 있습니다.

## Jekyll

[Jekyll](https://jekyllrb.com){:target="_blank"}은 정적 사이트 생성기이자, 템플릿과 콘텐츠 파일을 병합하여 웹사이트를 만드는 명령줄 도구입니다. Jekyll은 Liquid를 템플릿 언어로 사용하며, 소수의 객체, 태그, 필터를 추가했습니다. 여기에는 콘텐츠 페이지를 표현하는 객체와 재사용 가능한 콘텐츠를 인클루드하기 위한 태그, 문자열과 URL을 조작하기 위한 필터가 포함됩니다.

또한 Jekyll을 Github repository에 설치 및 push 후 결과를 웹 사이트에 게시해주는 웹 호스팅 서비스인 [GitHub Pages](https://pages.github.com/){:target="_blank"}를 지원합니다. 이 웹 사이트는 Github Pages를 사용하여 제작되었습니다.

Jekyll은 Liquid 최신 버전을 사용하지 않을 수 있으며, 이로 인해 이 사이트에 나열된 태그와 필터가 Jekyll에서 작동하지 않을 수 있습니다. 종종 Jekyll 프로젝트는 Liquid의 베타 또는 출시 후보 버전을 사용하는 대신 Liquid의 안정적인 출시 버전(stable release)을 기다릴 것입니다. Liquid Jekyll의 버전을 확인하려면 [Jekyll gem 페이지](https://rubygems.org/gems/jekyll){:target="_blank"}의 **runtime dependencies** 섹션을 확인하십시오.

Jekyll의 Liquid 버전은 [Jekyll 문서의 Liquid 섹션](https://jekyllrb.com/docs/liquid/){:target="_blank"}에 문서화되어 있습니다. Jekyll의 Liquid 버전을 사용하려면 Jekyll 프로젝트를 clone 하거나 Jekyll을 gem으로 설치 후 정적 사이트에서 Liquid를 테스트해 볼 수 있습니다.