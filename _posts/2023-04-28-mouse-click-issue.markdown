---
layout: post
title: Mouse click issue
image: Apps-Mouse-icon.png
date: 2023-04-28 12:30:00 +9:00
tags: [computer, issue]
categories: computer issue
---

최근에 갑자기 마우스 포인터는 움직이는데 클릭이 되지 않는 이슈가 꽤 자주 발생하였다. 검색해 보아도 정확한 이유와 확실한 해결방법을 찾을 수 없어 이것저것 만져보다가 임시방편으로 해결할 수 있는 방법을 찾게 되어 글을 작성하게 되었다. 증상은 다음과 같다.
1. 가장 최신의 창에서만 클릭이 가능하다.
2. 윈도우하단 고정바의 클릭이 먹통이 된다.
3. 모든 창의 닫힘버튼 등의 조작되지 않는다.

사용하는 마우스의 물리적인 문제가 아니다. 왜냐하면 연결해보았던 모든 마우스에서 발생하였고, 노트북 터치패드도 같은 문제가 발생하였기 때문이다.

***

#### temporary solution

나의 컴퓨터에서만 해결되는 방법인지는 잘 모르겠으나, 다음과 같은 동작을 순서대로 하게되면 마우스의 동작이 정상적으로 복구된다.
1. Win(윈도우키) + R키를 누르고 'regegit' 입력 후 확인

    ![]({{site.baseurl}}/images/2023-04-28-mouse-click-issue/1_cmdregedit입력.png)


2. 사용자 계정 커트롤 UAC창이 뜨면 화살표 버튼으로 '예' 쪽으로 커서를 옮기고 Enter키 누르기

    ![]({{site.baseurl}}/images/2023-04-28-mouse-click-issue/2_사용자계정컨트롤UAC창.png)


3. 레지스트리 편집기가 실행되면 마우스 클릭동작이 가능해짐

    ![]({{site.baseurl}}/images/2023-04-28-mouse-click-issue/3_레지스트리편집기.png)


아직 근본적인 해결방법은 모르겠으나 위와 같은 임시 방법으로 해당 이슈를 해결하고 있다.
