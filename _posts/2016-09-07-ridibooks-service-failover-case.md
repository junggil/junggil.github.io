---
layout: post
title: "[NewsLetter] 리디북스 서비스 장애 복구 후기 (+ 10 건)"
description: "리디북스의 데이터 센터 이중화 구성을 통한 고가용성 설계와, 장애 발생시에 대응 전략을 통한 교훈"
tags: [리디북스, 장애, IoT, ElasticSearch, Go Lang, Kakao, KEMI, AI, 세미나, UX]
---

## 개발 관련

#### [리디북스 서비스 장애 복구 후기](http://www.ridicorp.com/blog/2016/09/02/idc-outage/){:target="_blank"}
{% include image.html path="post/ridibooks_service_fail_recover_tips.png" path-detail="post/ridibooks_service_fail_recover_tips.png" %}
* Multi-AZ 구성의 중요성 
    * 리디북스는 AWS가 아니라 별도의 데이터 센터를 쓰고 있기 때문에, Multi-AZ를 위해서는 2개 이상의 데이터 센터로 이중화를 구성을 해야 하는 상황이 저희와 차이가 있습니다. 
* 장애 공지를 위한 별도 인프라 구성 
* **장애 발생 후에 대처**가 훌륭합니다.
    * 복구 완료 시점이 명확하지 않았기 때문에, 전체 구성에 대해서 즉시 Provisioning 결정

#### IoT 관련 논쟁
1. [IoT’s killer app is home security](https://techcrunch.com/2016/08/31/iots-killer-app-is-home-security/){:target="_blank"}
2. [IoT’s killer app is not home security](https://techcrunch.com/2016/09/03/iots-killer-app-is-not-home-security/){:target="_blank"}
    * 1번 기사에 대해서 반박이 2번 기사 입니다. 
    * 저는 2번 내용에 대해서 많이 공감을 하고, 현재 IoT 제품들이 보안 쪽에 포커싱을 하고 있지만 그 기반이 되는 Wifi / 전원 등을 차단하면 손쉽게 무력화가 가능하다는 점은 큰 단점이고 해결이 되어야 하는 부분이라고 생각합니다. 

> 2016.12월 기준으로 `AWS IoT Greengrass`가 출시되면서, 외부 네트워크가 차단된 상태에서도 IoT 기기의 동작성을 보장할 수 있도록 되었습니다. 

#### [Elasticsearch based Image Search using RGB Signatures](http://sujitpal.blogspot.kr/2016/05/elasticsearch-based-image-search-using.html){:target="_blank"}
* 텍스트 기반이 아니라 이미지를, RGB Signature를 뽑아서 가장 유사도 높은 이미지를 검색하도록 Elasticsearch를 적용한 사례입니다.
* 괜찮아 보이기는 한데, 왠지 Elasticsearch보다 더 적합한 도구가 있지 않을까 하는 생각이 드네요 (왠지 원래 목적과 다르게 변태같이 쓰는 기분이라서 .. )

#### Go 언어 관련 모음
1. [기술탐색 golang](https://andromedarabbit.net/wp/%EA%B8%B0%EC%88%A0-%ED%83%90%EC%83%89-golang/){:target="_blank"} (JAVA 개발자의 golang에 대한 전반적인 감상평 – 공감되는 부분이 있습니다.)
    * 쓸만한 웹프레임워크 및 ORM이 부족함
    * 그래서 비지니스 로직에 직접 적용하기 보다는 동시성이 필요한 내부 서비스에 우선 적용하는 것이 좋을 것 같다는 의견
2. [Program your next server in Go](https://talks.golang.org/2016/applicative.slide#1){:target="_blank"}
3. [Making concurrent HTTP requests in Go](http://blog.narenarya.in/concurrent-http-in-go.html){:target="_blank"}
    * 읽어볼만 하긴 한데, 끝에 python3와의 비교가 공정하지 않네요.  
    * go-coroutine을 썼으면 python3에서도 gevent or asyncio를 써야 공평한 조건이라고 봅니다.

#### [카카오의 전사 리소스 모니터링 시스템 - KEMI](http://tech.kakao.com/2016/08/25/kemi/){:target="_blank"}
{% include image.html path="post/kakao_kemi_status_monitoring_system.png" path-detail="post/kakao_kemi_status_monitoring_system.png" %}
* 카카오에서 로그 수집 / 모니터링을 위해서 어떤 기술 스택을 사용하고 있는지를 참고할 수 있습니다. 

#### [스탠포드 AI100 프로젝트의 첫번째 보고서 공개](https://ai100.stanford.edu/2016-report){:target="_blank"}
* AI에 대한 100년 범위의 백서 입니다. 
    * AI의 정의에서부터 시작하는 ... 
* 차량/운송을 포함해서 각 도메인 별 경향을 간단히 소개한 뒤, 2030년의 한 도시에서 AI가 일상 생활에 주는 변화와 영향에 대해서 기술하고 있다고 합니다.
* 영어와 분량의 압박으로 정독을 하지 못했는데, 관심 있는 분들 읽어 보시면 좋을 것 같습니다. 

## 세미나 정보

#### [서버리스 아키텍처 (API Gateway / Lambda 위주) 세미나](http://onoffmix.com/event/76932){:target="_blank"}
* 한국 아마존 사용자 그룹 정기 세미나 입니다.
* 저는 이런 소규모 세미나에 관심이 많고 참석을 하고 싶지만, 이런 류의 밋업들이 특징인 공통적인 세션 전/후반에 네트워킹 시간이 부담이라 아직 시도를 못해보았습니다. 
* 9/21일 (수) 18:30 ~ 21:00

## 기타 읽을 거리

#### [Google Coder Analyzes a Billion Files to Find a Winner in Tabs vs Spaces Debate](http://gizmodo.com/google-coder-analyzes-a-billion-files-to-find-a-winner-1786016648){:target="_blank"}
{% include image.html path="post/tab_vs_spaces_result.png" path-detail="post/tab_vs_spaces_result.png" %}
* Tab VS Space 에 대한 오랜 싸움의 1차 판정 결과, 승자는 space

#### [How many freshmen want to study computer science at the University of Washington (치솟는 CS의 인기)](http://www.geekwire.com/2014/uw-computer-science-majors/){:target="_blank"}
{% include image.html path="post/freshmencse.jpg" path-detail="post/freshmencse.jpg" %}
* 좋기도 하지만 걱정이 더 많이 되네요.

#### 천재성의 특징
{% include image.html path="post/characteristics_of_genius.png" path-detail="post/characteristics_of_genius.png" %}
* 천재들이 보이는 관심의 폭이 어마어마하다는 점에 대해서는 많이 공감합니다. 

#### [Floor Plan Light Switch](http://www.yankodesign.com/2011/03/02/know-your-switches/){:target="_blank"} 
{% include image.html path="post/floor_plan_switch.jpg" path-detail="post/floor_plan_switch.jpg" %}
* UX 의 성공적인 예라고 생각합니다. 
    * 기술적 관점으로는 현실 가능성이 낮아 보이지만
