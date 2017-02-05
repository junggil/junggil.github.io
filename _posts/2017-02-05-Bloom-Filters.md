---
layout: post
title: "[NewsLetter] Bloom Filters (+ 9건)"
description: "DynamoDB 에서부터 Postgresql, HBase and Bitcoin 까지 분산시스템에서 널리 사용되는 Bloom Filter에 대한 소개"
tags: [Bloom Filter, Python Ddjango, Gitlab Databse Incident, Testing with Postman, Zombie in Office, PyCon APAC 2017, Voice Fishing, TED Originals]
---

## 개발 관련 

#### Back-to-Basics Weekend Reading - Bloom Filters
{% include image.html path="post/bloom_filter.png" path-detail="post/bloom_filter.png" %}
* [Link](http://www.allthingsdistributed.com/2017/02/bloom-filters.html){:target="_blank"}
* Bloom Filter는 연산량이 증가보다 저장공간을 효율적으로 사용하는 것이 더 중요할 때 사용합니다. 
    * 서로다른 여러개의 해쉬함수를 사용하며, 전체 해쉬값의 대상 Bit가 모두 Set인 경우에는 대상이 존재할 가능성이 있습니다. 하지만 하나라도 Set이 되어있지 않으면 대상이 존재하지 않음을 보장합니다. 다시 말해, False positive가 가능하며 False negative는 없음을 보장하는 특징을 갖고 있습니다.
    * 복수개의 해쉬함수 계산이 필요하기 때문에 연산량이 증가합니다.
    * DynamoDB 에서부터 Postgresql, HBase and Bitcoin 까지 분산시스템에서 주로 사용된다고 합니다.

#### 장고, 현실은 시궁창
<div class="embed-responsive embed-responsive-16by9">
<iframe src="//www.slideshare.net/slideshow/embed_code/key/ArQAAo7xTT46n0" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/lqez/django-in-production" title="Django in Production" target="_blank">Django in Production</a> </strong> from <strong><a target="_blank" href="//www.slideshare.net/lqez">Hyun-woo Park</a></strong> </div>
</div>
* 스마트스터디의 5년에 걸친 프로덕션 경험 노하우 입니다.
* 제목과는 달리(?) Django를 프로덕션 수준으로 쓰기 위해서 필요한 기술컴포넌트와 전략에 대해서 재치있게 잘 다루고 있습니다.
    * 스마트스터디 기술자료도 믿고 볼만하죠.

#### GitLab.com Database Incident
* [Link](https://kyupokaws.wordpress.com/2017/02/02/2117-gitlab-com-database-incident%ED%95%9C%EA%B8%80%EB%B2%88%EC%97%AD/){:target="_blank"}
{% include image.html path="post/gitlab_database_incident.png" path-detail="post/gitlab_database_incident.png" %}
* 6시간 분량의 데이터베이스 데이터(code, issues, merge ... )를 날렸는데, 그 원인이 내부 개발자의 실수와도 관계까 있었습니다.
* Gitlab은 해당 문제를 대처하는 과정에서, 서비스에 문제가 발생했음을 `공개적`으로 공지를 하고 복구 과정을 Youtube로 생중계 하면서 오히려 좋은 평가를 받고 있는 상황입니다.
    * 문제를 발생시킨 직원은 해고되지 않았다고 하며, 
    * 생중계 과정에서 기술적인 조언을 받아들이고, 핵심적인 내용에 대한 좋은 조언을 한 개발자에게는 Job Offer도 있었다는 소문이 있었습니다. 

#### Testing your API with Postman
* [Link](http://equimper.github.io/2017/01/28/testing-your-api-with-postman/){:target="_blank"}
* Postman은 REST API 테스트를 위해서 정말 많은 사람들이 사용하는 툴입니다.
* Postman을 좀 더 유용하게 쓸 수 있도록, Collections / Tests / Runner 등에 대한 Tutorial을 제공합니다. 
    * 하나씩 따라서 한번 해보시길 권장합니다.

## 조직문화
#### 회사에 좀비가 살고 있어요
{% include image.html path="post/zombie_in_the_office.png" path-detail="post/zombie_in_the_office.png" %}
> 좀비의 목표는 정상적인 직원을 물어뜯어 좀비로 만드는 것 뿐이다. 좀비의 공격을 막아내며 업무까지 제대로 하기는 쉽지 않은 일이다. .."

* [Link](http://morethanair.com/archives/469){:target="_blank"}
* 업무 전문성을 포기한 대신 아부를 통해 권력을 갈구하는 좀비가 회사를 장악하는 과정을 설명합니다.
* 내용이 과장되거나 지나친 부분이 있지만, 읽어볼만 합니다.

#### [문유석 판사의 일상有感] 부장님들께 원래 드리려던 말씀
* [Link](http://v.media.daum.net/v/20170131010207649){:target="_blank"}
* "부장님들께 드리는 말"로 유명세를 탄 문유석 판사님의 후속 글입니다.
* 해당 글도 진솔하고 담담해서 읽어보면 좋습니다.
* 본문의 내용 중에서 일부를 아래 발췌해서 적습니다.
    * 자제함으로써 누군가를 행복하게 할 수도 있는 힘, 그건 권력이다.
    * 시대에 따라 옳고 그름이 다를 수 있다. 하지만 힘은 과거가 가지고 있고 시간은 미래로 흐른다. 과거가 미래에 양보하고 미래는 그런 과거를 존중하는 것, 이것이 발전 아닐까.

## 컨퍼런스 소식

#### PyCon APAC 2017 - Kuala Lumpur
* [Link](https://pycon.my/2016/08/17/pycon-apac-2017-in-kuala-lumpur/){:target="_blank"}
* 작년 서울에 이어서 이번에는 말레이시아의 Kuala Lumpur 에서 열립니다.
* Dates: Aug 26 (Sat) to Aug 27 (Sun) 2017 


## 기타 읽을 거리
#### "바로 이 목소리" 공개 현상수배
{% include image.html path="post/ml_voice_fishing.png" path-detail="post/ml_voice_fishing.png" %}
* [Link](http://s1332.fss.or.kr/fss/kr/promo/bodobbs_view.jsp?seqno=20204&no=9&s_title&s_kind&page=0){:target="_blank"}
* 정부가 주도적으로 한 일 중에서 무척 훌륭한 성과라고 생각합니다.
* 보이스피싱 사기범 목소리를 DB화 한 후 딥러닝으로 상습범을 분리하여 공개했습니다.
    * 목소리를 듣고 신원을 제보하면 1천만원의 포상금을 지급합니다.
    
#### 개발자가 아닌 개발자
* [Link](http://www.haruair.com/blog/3840?1){:target="_blank"}
* 짧지만 읽어볼만한 글입니다.
* 어떤식의 개발자도 개발자라고 할 수 있으며, 능력 및 연봉의 수준에 상관없이 발업권이 보장되어야 부당한 샇왕에 대한 개선이 될 수 있다고 이야기합니다.

#### [TED] 독창적인 사색가의 놀라운 습관들
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/5NcLS3mzPeE?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 성공이 아니라 도전 자체로 보상이 주어지면 위대한 성취를 이룰 수 있게 한다는 연구결과가 많이 있습니다.
* 즉, 실패를 대하는 태도가 성공의 비밀이라는 관점인데, 해당 영상도 이와 맥을 같이합니다.
    * 조직 심리학자 아담 그랜트는 "오리지널스(Originals)"에 대해 연구합니다
    * 오리지널스는 새로운 아이디어를 꿈꾸고 실제로 실현하고자 행동하는 사람들을 의미합니다. 
    * "가장 위대한 오리지널스는 가장 많이 실패해 본 사람입니다. 왜냐하면, 가장 많이 시도해 본 사람이기 때문입니다. 단 몇 개의 좋은 아이디어를 얻기 위해서는 수많은 나쁜 아이디어가 필요합니다." 
