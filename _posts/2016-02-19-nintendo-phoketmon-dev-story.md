---
layout: post
title: "[NewsLetter] 닌텐도 포켓몬 선물서버 개발기 (+ 4건)"
description: "한국인 개발자 중에서 재야에 숨은 능력자들의 개발 이야기를 공유 드립니다."
tags: [닌텐도, 개발기, LED 전광판, 스마트 미러, 중간 보고, 사내 프레임워크]
---

## 개발 관련

#### [닌텐도 포켓몬스터 선물서버 개발기](http://gall.dcinside.com/hit/13259){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/9oWYftUqVUM?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 대단한 열정과 노력입니다.
* 패킷캡쳐를 통해서 닌텐도의 내부 프로토콜을 분석하고, MITM (Man-In-The-Middle) 공격으로 RSA키를 위조합니다.
    * 평문통신 구간이 없이 꼼꼼하게 인증을 요구하는 닌텐도 역시 대단하지만
    * 그 모든 서버를 해독해서 결국 자체 선물서버를 구축합니다.

#### [버스 LED전광판 제작기](http://gall.dcinside.com/board/view/?id=hit&no=13251){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/inFyqopE8iA?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 풀스택 개발자이자, 1인 기업의 개발기 입니다.
    * H/W 설계, PCB 제작
    * 조립, 납땜, 프린팅
    * 펌웨어 개발
    * 안드로이드 앱개발
    * 마케팅, 판매
* 기존 솔루션의 불편한 점을 분석해서, 시장을 만드는 노력과 열정이 많은 자극을 줍니다.

#### [스마트 미러 제작기](http://blog.embian.com/120){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/hluRkE8JwHM?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* [외국 개발기](https://www.youtube.com/watch?v=PDIbhV8Nvq8){:target="_blank"}에 대한 한글화 버전입니다. 
* 회사 동료들간에 team project로 진행되었는데, 이런 문화가 부럽습니다.
* 라즈베리파이 대신에 태블릿과 노트북을 사용하였으며, 별도로 한글화에 맞춰 다음의 API 목록을 사용하였습니다.
    1. Youtube Data API 
    2. 서울시 지하철 도착정보 open API 
    3. Sound Cloud API  


## 기타 읽을 거리

#### [훌륭한습관 중간 보고](http://ohyecloudy.com/pnotes/archives/great-habit-interim-report/){:target="_blank"}
{% include image.html path="post/incremental_report.png" path-detail="post/incremental_report.png" %}
* 중간보고는 회사에서 꼭 필요한 습관이자 역량이라고 생각합니다. 
* 중간보고는 개인의 경쟁력 있는 강점이라는 것에도 적극 동의합니다. 
    * 아래는 글쓴이가 자기소개서에 포함하는 문장입니다.

> 중간보고를 잘합니다. 진행 중인 업무를 관리자가 쉽게 파악할 수 있어서 관리 비용이 낮습니다. 진행 상황 공유를 통해 피드백을 받을 수 있어 잘못된 방향으로 구현하는 일이 드뭅니다.


#### 오픈소스 내재화 관련 논의 소개
 * 오픈소스를 쓸 것인지 그걸 가져와서 프로젝트에 맞게 내제화를 할 것인지에 대해서, 최근에 논의가 있었고 양쪽 의견 모두 수용할 만한 포인트가 있어서 공유 드립니다. 
 1. [사내 프레임워크를 만들지 말자](https://blog.outsider.ne.kr/924){:target="_blank"}
 2. [내가 사내 프레임워크를 만드는 이유](http://blog.kivol.net/post/138455049723){:target="_blank"}

#### Console Weather Command
{% include image.html path="post/console_weather_command.png" path-detail="post/console_weather_command.png" %}
* 콘솔에서 아래 명령어를 직접 쳐보세요

```bash
curl -4 http://wttr.in/Seoul 
```
