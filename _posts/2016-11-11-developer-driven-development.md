---
layout: post
title: "[NewsLetter] Developer-Driven Development (+ 8건)"
description: "어떻게 시간 낭비없이, 코드가 엉망이 되지 않으면서, 원하지 않는 개발도 하지 않으면서 회사를 성장시킬 프로세스를 만들 수 있는가?"
tags: [DDD, 8Percent, 회고, Naming Rule, Mob Programming, Docker Swarm, Evangelist, 쿠팡]
---

## 개발 방법론

#### [Developer-Driven Development](https://medium.com/@isaaclyman/development-driven-development-75c01b2afca1#.g6j5lurn5){:target="_blank"}
* 글이 좀 길지만, 개발자 분들은 *정독*을 해보기를 적극 추천 합니다.
* 직접 읽는 느낌을 전달하지는 못하겠지만 시간이 없으신 분들을 위해서 간략히 요약을 해봅니다.
    * 해당 글은 다음 질문에 대한 대답 입니다. 
    * "어떻게 시간 낭비없이, 코드가 엉망이 되지 않으면서, 원하지 않는 개발도 하지 않으면서 회사를 성장시킬 프로세스를 만들 수 있는가?"
    * 개발자들이 적극적으로 `참여` (buy-in) 하도록 유도해야 더 생산성 있는 개발이 가능하며 (이를 위해서는 개발자들이 행복해야 하는데), 개발자의 행복은 Coke와 축구경기가 아니라 개발자 스스로 자랑스러울 만큼 잘 작성된 코드와 기능을 동료와 함께 만들어 나갈 때 만들어짐.
* 그럼 어떻게 개발해야 할까?
    1. `Code Review in reverse`
> 코드가 작성된 후가 아니라, 코드 작성 전에 코드 리뷰를 수행한다. 코드 리뷰는 개발 요구사항 (스토리)에 대한 담당자를 정하고, 담당자가 이후 실제 개발에서 필요할 것이 예상되는 라이브러리, 기술을 포함해서 step-by-step으로 어떻게 요구사항을 해결할지를 기술한다. 이 과정에서는 변수 이름, 클래스 정의, 인터페이스, 통신 방법, 캐싱 기술 등이 포함되며, 필요하다면 의사코드를 추가한다.
    2. `20% Time`
> 기술부채 (Tech. Dept)는 방치 될수록 점차 문제가 심각해 지면서, 최종적으로 개발자들의 의욕을 떨어뜨린다. 기술부채를 해결하기 위해서 개발자들은 전체 업무시간의 20%를 기술부채를 해결하기 위한 활동으로 - refactoring, load testing, researching, creating developer resources - 사용한다.
    3. `Story despecialization`
> 다음 요구사항 (스토리)를 처리할 준비가 된 개발자는, 기존업무 배경과 상관없이 순서대로 내용을 배정받는다. 이를 통해서 팀원이 불의의 사고 등으로 업무를 계속할 수 없는 경우에도 제품이 문제없이 동작하도록 한다.

#### [8퍼센트 CTO 1년 차 회고](https://brunch.co.kr/@leehosung/26){:target="_blank"}
{% include image.html path="post/8percent_regression.png" path-detail="post/8percent_regression.png" %}
* 이번 글은 관리자 분들은 정독을 해보기를 추천 합니다.
* 이와 같이 어떤 시도가 있었고, 어떤 부분을 느꼈는지에 대한 공유가 내부에서도 적극적으로 있으면 좋을 것 같습니다.

#### [오픈소스의 네이밍 특징들](https://brunch.co.kr/@goodvc78/12){:target="_blank"}
{% include image.html path="post/variable_name_statistics.png" path-detail="post/variable_name_statistics.png" %}
* 공통적으로 개발자가 가장 힘들어하는 일은 "이름 짓기" 라고 합니다. (49%)
* github의 JAVA 프로젝트 상위 20개에 대한 분석해서, 클래스/함수/변수에 따라서 각각 많이 쓰는 단어를 추출했습니다. 
* 해당 단어 조합으로 사용하면 이름 짓는 고민을 좀 덜 수 있을 것 같네요.

#### [주니어 개발자의 기술 블로그 운영 회고](http://www.popit.kr/%EC%A3%BC%EB%8B%88%EC%96%B4-%EA%B0%9C%EB%B0%9C%EC%9E%90%EC%9D%98-%EA%B8%B0%EC%88%A0-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EC%9A%B4%EC%98%81-%ED%9A%8C%EA%B3%A0/){:target="_blank"}
* github + Jekyll로 기술 블로그 운영하는 방법입니다. (이 블로그도 동일하게 만들어졌습니다)
* 설치형 Tistory에서 github으로 이전을 결심한 배경을 살펴볼만 합니다.
    * 역시나 개발자로서의 이력관리가 주된 목적 입니다.
    * 추가적으로는 Markdown 포맷은 범용적이기 때문에, 사내/사외 플랫폼에 동시에 작성내용을 게시 가능한 장점이 있습니다.

#### [Mob Rule?](http://www.davefarley.net/?p=275){:target="_blank"}
{% include image.html path="post/mob_rules.png" path-detail="post/mob_rules.png" %}
* Mob 프로그래밍에 대한 회고 입니다. 
* 굉장히 개발 방법론 Spectrum상에서 도입이 어려운 방법이라고 생각하지만, 그만큼 잘 도입할 경우에 Comm. 비용을 극적으로 낮출 수 있을 것 같다고 기대합니다.  (앞에서 소개한 despecialization이 적용된 경우에는 도입이 일부 가능할 것 같네요)
    * (장점) 팀 전체가 동일한 경험과 소통의 수준을 유지 가능
    * (장점) 개발속도와 완성도 측면에서 (다른 개발 방법론 보다) 유리할 수 있음.
    * (단점) 10명 이하의 작은 규모의 팀이 적당함.
    * (단점) Pair-Programming과 비교했을 때, 분위기를 해치는 사람이 내부에 있는 경우 해결이 어려움. 

#### [Deploy & scale your application on AWS with Docker Swarm](http://blog.alexellis.io/scale-docker-swarm-on-aws/){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/F5J8eQHlR2I?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* *EC2 생성시에 User Data 부분에 Script를 작성해서*, 인스턴스가 생성되면서 자동으로 Docker Swarm에 join 될 수 있도록 한 것이 주요 아이디어 입니다.
* Elastic하게 인프라를 생성하는 것은 AutoScale Group을 설정하거나, CloudFormation으로도 가능할 것 같지만, *전체 인프라에 작업을 배포하는 것은 Docker Swarm이 유리*한 부분이 있어 보입니다. 
* 10분짜리 동영상을 보셨으면, 원글은 읽지 않으셔도 됩니다.


## 기타 읽을 거리

#### [How you know – 번역과 생각](https://sangminpark.wordpress.com/2016/10/31/how-you-know-%EB%B2%88%EC%97%AD%EA%B3%BC-%EC%83%9D%EA%B0%81/){:target="_blank"}
* 최근 SNS가 널리 쓰이면서 긴 글을 읽거나 쓰는 경우가 많이 없어졌는데, 읽기와 생각의 중요성을 정리한 글입니다. 
* *글을 많이 읽고 자신의 생각을 글로 정리해보는 것이 필요*하다는 것에 동의합니다.


#### [한국 AWS 클라우드 에반젤리스트 활동](https://aws.amazon.com/ko/blogs/korea/cloud-evangelism-in-korea/){:target="_blank"}
> For the evangelist role, we’re more flexible with respect to what you’ve done in the past… What’s most important is that elusive combination of technical experience, great communication skills, and a `passion for helping developers`.

* 제가 최근의 개인적인 Role 모델로 삼고 있는 AWS의 윤석찬 SA님의 글입니다. 
* 에반젤리스트의 역할을 소개 하고 있는데, 기업마다 정의가 차이가 있으니 해당 정의는 AWS 기준으로 참고하시면 될 것 같습니다.
* 다음의 두 가지의 역할을 합니다.
    * 기술에 대한 이해와 전파
    * 열정을 갖고 내부 `개발자를 돕는` 역할


#### [삼성, LG직원 다 빼가는 쿠팡...인력시장 블랙홀](http://www.koreaherald.com/view.php?ud=20161103000860){:target="_blank"}
* 아시는 분은 많이 아시겠지만, 쿠팡으로 최근 코딩 전문가들이 많이 이직을 했죠. 
* 기사로도 나왔네요. 
