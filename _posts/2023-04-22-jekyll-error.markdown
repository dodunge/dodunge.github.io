---
layout: post
title: marshal data too short (ArgumentError) 에러 해결 방법
image: github_pages_logo.jpg
date: 2023-04-22 22:38:08 +9:00
tags: [blog, study]
categories: githubPage
---

internal:marshal:34:in `load': marshal data too short (ArgumentError) 에러는 마샬링(marshaling)된 데이터가 손상되었을 때 발생하는 에러이다. 이러한 에러는 jekyll을 비롯한 다양한 ruby 어플리케이션에서 발생할 수 있다. 먼저 에러를 발생시키는 원인을 파악하고, 적절한 대처방법 찾아보았다. 에러 발생시의 모습은 다음과 같다.

***

#### Error Image

![에러 발생시의 화면]({{site.baseurl}}/images/2023-04-22-jekyll-error/jekyll_error.jpg)

해당 에러는 Ruby 객체를 마샬링해서 저장하고 다시 읽을 때 데이터가 손상되어서 발생하는 경우가 있다고 한다. 이러한 경우, 먼저 .jekyll-cache 폴더와 _site 폴더를 삭제하고 다시 bundle exec jekyll serve 명령어로 Jekyll을 실행해 보면 된다. 재실행시에 정상작동하는 것을 볼 수 있다.

***

#### Resolved Results Image

![해결된 결과 화면1]({{site.baseurl}}/images/2023-04-22-jekyll-error/Delete jekyll-cache and _site.jpg)


![해결된 결과 화면2]({{site.baseurl}}/images/2023-04-22-jekyll-error/정상동작.png)


다음처럼 marshal data too short (ArgumentError) 에러없이 정상동작되는 것을 확인할 수 있다.

***