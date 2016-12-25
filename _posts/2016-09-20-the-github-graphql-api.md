---
layout: post
title: "[NewsLetter] The GitHub GraphQL API (+ 8건)" 
description: "REST API를 대체하면서 App과의 Interface를 보다 효과적으로 가져갈 수 있는 GraphQL API 소개"
tags: [GraphQL API, Web 도용, 자율주행, Web BLE, Obama, Traffic, Github, 회고, 기업문화, 맥킨지]
---

## 개발 관련

#### [The GitHub GraphQL API](http://githubengineering.com/the-github-graphql-api/){:target="_blank"}
{% include image.html path="post/github_graphql_api_sample.png" path-detail="post/github_graphql_api_sample.png" %}
* 최근에 Github가 REST API v4를 발표하면서, `GraphQL`을 동시에 지원하기로 발표했습니다.
* GraphQL은 업계에서 기존 REST API를 대체하는 기술로 떠오르는 규격입니다.
* 제가 생각하는 특징이자 장점은 아래와 같습니다. 
    * 응답 형식을 **Client에서 결정**합니다.
    * Client에서 필요한 데이터를 어떤 형식으로 조회할 것인지를 정의해서 요청하면 그에 따라서 데이터를 응답해 줍니다. 
    * 따라서 기존에 설계된 REST API의 결과가, 새로운 시나리오에 적합하지 않은 경우가 흔하게 발생하는데 기존에는 범용으로 설계된 REST API 몇 개를 조합해서 써야 했다면 GraphQL은 그럴 필요가 없습니다. 
    * 위에 특징이 시나리오 변경에 따른 REST API를 같이 수정하거나 변경 해야 하는 **관리 부담을 줄여주고 성능적으로도 유리**할 수 있습니다.
* 기존에 REST API를 제공하는 파트에서는 한번쯤 눈여겨보면 좋을 것 같습니다. 

#### [Dear Al-Jazeera: Why Steal Our Code?](https://www.scrollytelling.io/al-jazeera.html){:target="_blank"}
* Web 진영에서의 자주 겪는 웹페이지 도용 사건입니다. 
    * Web 기반 기술들의 특징상 소스를 노출되지 않게 방어하는 것이 현실적으로 불가능하며, 난독화 정도가 한계입니다.
* 기자가 작성한 기사를 두 군데의 언론사에 팔았는데, 도덕적인 문제는 차치하고서라도 페이지를 그대로 베껴서 이미지 등의 리소스를 베낀 서버에서 가져와서 서버의 Traffic 비용 부담까지 발생했습니다. 

### [구글의 자율주행테스트와 자율모드해제 보고서의 의미분석](http://www.digieco.co.kr/KTFront/report/report_issue_trend_view.action?board_seq=11111&board_id=issue_trend&sort_order=&kind=a01&list_page=&list_gubun=&searchtext=&etc1=386&etc2=){:target="_blank}
{% include image.html path="post/self_driving_car_test_result_by_ca.png" path-detail="post/self_driving_car_test_result_by_ca.png" %}
* 16페이지의 짧은 보고서인데 내용이 무척 흥미롭습니다. 
* 캘리포니아주 자동차국(DMV)은 보쉬, 델파이, 구글, 닛산, 메르세데스-벤츠, 테슬라, 폴크스바겐에 대해서 자율주행 테스트 결과를 보고하도록 했는데, 그 보고서 중에서 구글에 대한 내용입니다. (구글 이외의 회사들의 보고서는 내용이 부실하다고 합니다)
    * 전체 주행거리 중에 20% 가량이 자율주행실패(해제)로 메뉴얼 조작으로 전환 된다고 합니다. (완전 자율 주행을 위해서는 99.95% 이상의 신뢰도가 필요해서 현 수준은 무리)
    * 7년간 수집한 도로정보를 기반으로 매일 300만 마일을 가상 주행할 수 있는 시뮬레이터가 있다고 합니다. (기계학습 진행 중)

#### [The web is getting bluetooth](https://goo.gl/IKqwYF){:target="_blank"}
* Web Bluetooth기술이 많이 성숙해졌다는 내용입니다. 
* 아직은 여러 가지 이유로 (보안 / 기술적 한계) 제약이 많은 상황인데, 알아두면 좋을 것 같네요. 
* 아래는 현재의 한계 입니다.
    * BLE만 지원 (classic Bluetooth는 미지원)
    * Only Central, no Peripheral
    * One device at a time, no scanning
    * iOS 미지원

## 세미나 정보

#### [Tech Planet 2016  (2016.10.17 월요일)](http://techplanet.skplanet.com/agenda.html){:target="_blank"}
* SKP에서 주최하는 세미나 입니다. 
* 9/20일 오후 2시부터 등록이 가능하며, 비용은 단돈 1만원 입니다.


## 기타 읽을 거리

#### [베어 그릴스와 버락 오바마의 대화](https://sungmooncho.com/2016/09/10/bear-grylls-and-obama/){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/BViwzLUNXw8?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 오바마 대통령이 이야기해주는 ‘가족’의 의미
* 그리고 끈기(persistence)의 중요성을 배울 수 있습니다.

#### [한국기업의 조직건강도와 기업문화진단 보고서](https://t.co/LNViLDYIqF){:target="_blank"}
{% include image.html path="post/culture_of_korean_companies.png" path-detail="post/culture_of_korean_companies.png" %}
*  맥킨지 보고서 자료 입니다. (40페이지)
*  국내 100개 대기업 및 중견기업, 40,951을 대상으로 조사를 했는데, 경영진과 그 외, 연령별, 성별에 따른 `시각 차`가 크다는 내용입니다.
    * 예를 들어 리더쉽에 대한 평가는 경영진은 최상 수준으로, 일반직원~중간관리자는 최하 수준으로 인지
    * 야근/회의/회식/업무시지에 대해서 20/30대는 문제의식을 보이고, 50대는 긍정적으로 인식

#### [플레이탕스 해커톤 후기](http://lqez.github.io/blog/a-postmortem-of-the-platance-hackathon.html){:target="_blank"}
* 스마트 스터디에서 진행한 해커톤 후기 입니다. 
* 스마트 스터디라는 회사 자체의 문화나 업무 분위기가 무척 좋아 보이네요. 

#### The Simple Solution to Traffic
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/iHzzSao6ypE?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 교통 체증이 생기는 이유에 대해서 설명이 쉽고 명쾌합니다. 
* 요약하면 교차로(의 신호등)과 사람들간의 인지/반응 속도의 차이가 주요 원인인데, 흥미롭게도 이 두 가지 모두 자율주행을 적용하면 근본적으로 해결이 가능할 수 있어 보입니다. 
    * 교차로에 신호등이 심지어는 필요 없을 수 있다는 인식이 놀랍네요

## 신규 버전 및 출시 정보

#### [Code better with Reviews](https://github.com/universe-2016){:target="_blank"}
{% include image.html path="post/github_trello_like_ux.png" path-detail="post/github_trello_like_ux.png" %}
* Github에 Pull Request 리뷰 기능이 추가 되었고
* 칸반 형태로 프로젝트 관리 기능이 추가 되었습니다. (전 이게 마음에 드네요)
