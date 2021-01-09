---
title: Liquid의 변종
description: Liquid의 여러 종류 및 사용 환경에 따라 Liquid가 어떻게 변할 수 있는지에 대한 개요
---

Liquid는 수많은 환경에서 사용되는 유동적이고 안전한 언어입니다. [Shopify](https://www.shopify.com){:target="_blank" rel="noopener noreferrer"} 상점에서 사용하기 위해 만들어졌고, [Jekyll](https://jekyllrb.com){:target="_blank" rel="noopener noreferrer"} 웹사이트에서도 광범위하게 사용됩니다. 시간이 흐르면서, Shopify와 Jekyll은 Liquid에 자신들만의 객체와 태그, 필터를 추가했습니다. 가장 인기 있는 버전은 **Liquid**, **Shopify Liquid**, **Jekyll Liquid** 입니다.

이 사이트는 베타 및 출시 후보를 포함하는 **Liquid** 최신 버전, 즉 Shopify와 Jekyll 버전이 아닌 Liquid를 문서화합니다. Liquid repository를 다운로드하거나 [gem](https://rubygems.org/gems/liquid){:target="_blank" rel="noopener noreferrer"}으로 설치하면, 선택한 Liquid 버전에 있는 모든 객체, 태그, 필터에 접근할 수 있습니다.

## Shopify

Shopify always uses the latest version of Liquid as a base, but Shopify adds a significant number of objects, tags, and filters to Liquid for use in merchants' stores. These include objects representing store, product, and customer information, and filters for displaying store data and manipulating storefront assets like product images.

Shopify's version of Liquid is documented in the [Shopify Help Center](https://help.shopify.com/themes/liquid). If you want to try out Shopify's version of Liquid, you can create a development store through the [Shopify Partner Dashboard](https://help.shopify.com/en/partners/dashboard/development-stores).

## Jekyll

[Jekyll](https://jekyllrb.com) is a static site generator, a command-line tool that creates websites by merging templates with content files. Jekyll uses Liquid as its template language, and adds a few objects, tags, and filters. These include objects representing content pages, tags for including snippets of content in others, and filters for manipulating strings and URLs.

Jekyll also powers [GitHub Pages](https://pages.github.com/), a web hosting service that lets you push a Jekyll installation to a GitHub repository and have the resulting website published. This website is built using GitHub Pages.

Jekyll might not be using the latest version of Liquid. This means that the tags and filters listed on this site may not work in Jekyll. Often the Jekyll project will wait for a stable release of Liquid rather than using a beta or release candidate version. To see what version of Liquid Jekyll is using, check the **runtime dependencies** section of [Jekyll's gem page](https://rubygems.org/gems/jekyll).

Jekyll's version of Liquid is documented in the [Liquid section of Jekyll's documentation](https://jekyllrb.com/docs/liquid/). If you want to try out Jekyll's version of Liquid, you can clone the Jekyll project or install Jekyll as a gem and test Liquid on a static site.
