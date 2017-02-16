---
layout: post
title: "[NewsLetter] Google Cloud Spanner(+ 13건)"
description: "Globally Scalable한 SQL database 서비스 소개"
tags: [Google Cloud Spanner, Digitalocean L7, Spoqa flake8, TLS1.3, Extra Work, Evernote, Microsoft, Goldman, Durex, Volvo, Software Quality]
---

## 개발 관련 

#### Cloud Spanner
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/amcf6W2Xv6M?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* CAP 중에서 CP를 선택한 Global SQL 서비스
* 그런데 A를 99.999% 수준으로 끌어올려서, 사실상 CAP 전체를 보장한다 것이 중요한 항목입니다.
* Google 내부에서 2010년부터 7년째 사용중이며, 2012년도에 [논문](https://static.googleusercontent.com/media/research.google.com/ko//archive/spanner-osdi2012.pdf){:target="_blank"}을 공개했습니다.
* 이제 비용만 지불하면 Google과 동일한 Scale의 RDBMS를 사용 가능합니다.
* Spanner의 주요 특징은 아래와 같습니다.
	* Global Scale
    * Full Managed
    * High Available (99.999% -> Yearly Downtime 5m 15.6s)
    * Support SQL queries (ANSI 2011)
    * Support Transaction (ACID)
* References
	* [글로벌 분산 데이터베이스 Spanner](http://d2.naver.com/helloworld/216593){:target="_blank"}
	* [Introducing Cloud Spanner: a global database service for mission-critical applications](https://cloudplatform.googleblog.com/2017/02/introducing-Cloud-Spanner-a-global-database-service-for-mission-critical-applications.html<Paste>){:target="_blank"}
	* [Inside Cloud Spanner and the CAP Theorem](https://cloudplatform.googleblog.com/2017/02/inside-Cloud-Spanner-and-the-CAP-Theorem.html){:target="_blank"}

#### Load Balancers: Simplifying High Availability
{% include image.html path="post/digitalocean_l7_coming_soon.png" path-detail="post/digitalocean_l7_coming_soon.png" %}
* [Link](https://www.digitalocean.com/company/blog/load-balancers-simplifying-high-availability/){:target="_blank"}
* digitalocean에서 제공하는 관리형 L7 로드밸런서에 대한 소개 입니다. 
* digitalocean은 최근에 처음 알게되었는데, 이 회사의 움직임이나 결정방향이 마음에 듭니다. 
	* 현재 개발자 커뮤니티에서 무료 인증서로 인기있는 `Let's Encrypt`를 지원한다거나, 
	* Ruby, Go 기반의 Routing Algorithm 작성을 지원하는 등의 항목이 매력적입니다.
	* AWS에서도 digitalocean을 경계하였기 때문에, 동일한 비용 정책을 적용한 lightsail이라는 것을 작년 말에 발표했습니다.
* 참고로 AWS에도 ALB (Application Load Balancer)라고하는 L7을 제공하지만 TCP연결은 지원하지 않습니다.
	* 그외에 AWS Lambda를 연결해서 Routing Algorithm을 작성할 수있는 것등의 기능은 동일하구요.

#### flake8-import-order-spoqa
* [Link](https://spoqa.github.io/2017/02/12/flake8-import-order-spoqa.html){:target="_blank"}
* 한국 Python Community의 아이돌 `홍민희`님의 최신 글입니다.
* flake8이라는 Coding Style / Convention을 검사하는 오픈소스에, Spoqa에서 필요한 내용을 어떻게 요청해서 반영을 시켰는지에 대한 과정의 내용을, 담담하고 차분하게 설명하고 있습니다. 
* 오픈소스 커뮤니티에 대한 이해와 열정, 커뮤니케이션 방법이 모두 본받을만하고 훌륭하다고 생각합니다.

#### Introducing TLS 1.3
{% include image.html path="post/tls_13_handshake_changes.png" path-detail="post/tls_13_handshake_changes.png" %}
* [Link](https://blog.cloudflare.com/introducing-tls-1-3/){:target="_blank"}
* TLS 1.3부터 handshake 과정 간소화로 RTT가 단축된다고 합니다. 

#### Why is 80 characters the 'standard' limit for code width?
{% include image.html path="post/punch_card_line_limit_80.png" path-detail="post/punch_card_line_limit_80.png" %}
* [Link](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width){:target="_blank"}
* 대부분의 Style / Convention 을 검사하는 flake8 같은 도구에서 Line의 길이를 80자로 제한합니다.
* 그 근거가 Punch Card의 길이가 80글자였기 때문이라는 놀라운 내용입니다.

## 조직문화
#### 초과근무에 대해서 (The Clean Coder 내용 중)
{% include image.html path="post/the_clean_coder_extra_working_time.png" path-detail="post/the_clean_coder_extra_working_time.png" %}

#### 개발 프로세스가 개발 문화를 이기기 어려운 이유
* [Link](http://www.allofsoftware.net/2017/02/blog-post.html?m=1){:target="_blank"}
* 효율성 측면에서 프로세스보다 문화가 10배 이상의 효율을 내기 때문에, 프로세스로 업무를 강제하기 보다 자발적인 문화를 만들어야 한다는 내용입니다.
* 아래는 본문 내용중에 발췌 입니다.

> 프로세스는 복잡할수록 손해다. 문제만 없다면 프로세스가 없는 것이 제일 좋다. 문제가 있기 때문에 최소한의 제약을 가하는 것이다. 프로세스가 간단할수록 성숙도가 높다. 물론 주먹구구라서 프로세스가 없거나 간단한 회사는 예외다. 

#### 3 Effective Ways to Maintain High Energy Levels at Work for Software Engineers
{% include image.html path="post/effective_way_to_maintain_high_energy_level.png" path-detail="post/effective_way_to_maintain_high_energy_level.png" %}
* 육아와 직장을 병행하는 것이 시간과 체력적으로 어려운 부분이 있다는 것을 인정하고, 비용을 투자하고 생산성을 선택한다는 결정이 무척 인상적이었습니다.
* 짧고 내용이 잘 읽히는 편이라서, 영어지만 읽어볼 것을 권장합니다.
* 아래는 추가적으로 인상적인 구절을 붙여 넣습니다.

> One of the main evils of this profession is that in most companies workers are still measured by the time clock and not by performance.


#### Microsoft를 떠나며 Part 1/2
* [Link](https://brunch.co.kr/@stevenyoo/18){:target="_blank"}
* 새로운 배움이 계속될 수 있는지가, 회사를 선택하는 중요한 기준이 될 수 있다는 것을 보여줍니다.
* 현재 상태에 안주하지 않고 객관적인 시선으로 옮겨야 할 이유와, 머물러야할 이유를 정리하려고 하는 시도가 인상적입니다.
* 저도 새로운 자극과, 배움을 줄 수 있는 동료와 회사의 분위기가 중요하다고 생각합니다.

## 기타 읽을 거리
#### 에버노트가 3페타바이트의 데이터를 구글 클라우드로 옮긴 이유와 방법
* [Link](http://www.itworld.co.kr/news/103386#csidxf921e2c50cd0bffaac8172f84150cb9){:target="_blank"}
* 이와 같이 규모가 큰 Live 데이터를 이전하는 경우에는, 구글 측에서 직원을 파견해서 공동 작업을 한다는 부분이 인상적이네요.

#### As Goldman Embraces Automation, Even the Masters of the Universe Are Threatened
* [Link](https://www.technologyreview.com/s/603431/as-goldman-embraces-automation-even-the-masters-of-the-universe-are-threatened/){:target="_blank"}
* 골드만삭스에서 2000년 600명에 달했던 자산트레이더는 현재 2명만 남았고 그 자리는 200명의 컴퓨터 엔지니어들이 짜는 자동 트레이딩 프로그램으로 대체되었다는 기사입니다.
    * 알고리즘 및 AI로 기존 업무가 빠르게 대체 되고 있고, 
    * [The Robots Are Coming for Wall Street](https://www.nytimes.com/2016/02/28/magazine/the-robots-are-coming-for-wall-street.html?smid=pl-share){:target="_blank"} 연봉 35만~50만 달러를 받는 애널리스트가 40시간 걸릴 분석을 AI 프로그램인 Kensho는 단 몇 분만에 정확하게 결과물을 내놓는다는 작년 기사입니다.

#### Durex owners just bought a company that makes baby food
* [Link](https://twitter.com/i/moments/829980740817403904){:target="_blank"}
* 듀렉스가 166억 달러에 유아용 분유를 만드는 미드 존슨을 인수했습니다.
* 콘돔이 안 팔리면, 분유가 팔릴 것이라고 생각하면 훌륭한 전략이네요.

#### 볼보만 비껴가는 '스몰오버랩'... 꼼수일까, 노하우일까?
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/nnRIwQn9SA8?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* [Link](http://www.carmedia.co.kr/ftr/456211){:target="_blank"}
* 안전기준이 만들어지기 전부터 운전자의 안전을 고려했던, 볼보의 안전에대한 철학과 장인정신에 대한 집착을 옅볼수 있는 영상입니다.
* 다음 차는 볼보를 선택하고 싶어지게 만듭니다.
    
#### First Law of Software Quality
{% include image.html path="post/first_law_of_software_quality.png" path-detail="post/first_law_of_software_quality.png" %}
