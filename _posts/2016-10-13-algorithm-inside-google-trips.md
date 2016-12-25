---
layout: post
title: "[NewsLetter] Algorithm Inside Google Trips (+ 9건)" 
description: "Google Trips에 사용된 Eulerian Graph부터 TSP까지의 알고리즘과 응용을 설명"
tags: [TSP, Moral Machine, 디지털 노마드, OpenCV, Coding Interview, Molly-Guard, Physics, Incentive]
---

## 개발 관련

#### [The 280-Year-Old Algorithm Inside Google Trips](https://research.googleblog.com/2016/09/the-280-year-old-algorithm-inside.html){:target="_blank"}
{% include image.html path="post/algorithm_of_google_trips.png" path-detail="post/algorithm_of_google_trips.png" %}
* 얼마 전에 출시된 Google Trip에 사용된 알고리즘에 대한 소개 입니다. (Eulerian Graph 부터 TSP 까지)
* 이 글을 보면서 App에 대한 신뢰가 생겨서, 다음 여행에 Google Trips를 꼭 써보고 싶어지네요.
* 수학을 잘 모르는 저도 관심 있게 읽을 수 있게 친절하고 자세히 설명을 해 두었습니다.
    1. 지점들을 연결해서 그래프를 만들고
    2. MST를 구성 
    3. 한붓그리기가 가능하도록 edge가 홀수인 지점 간에 경로를 추가
    4. 여기에 구글에 수집된 정보를 포함해서 (어느 식당이 언제 사람이 많고, 어느 도로가 언제 막히는지) 경로를 최적화

#### [Moral Machine (인공지능용 윤리)](http://moralmachine.mit.edu/){:target="_blank"}
{% include image.html path="post/self_driving_ethics.png" path-detail="post/self_driving_ethics.png" %}
* MIT 미디어랩에서 만든 인공지능용 윤리. 소위 trolley problem이라도 부르는 인명피해를 피할 수 없는 상황에서 어떤 가치에 입각해 피해를 최소화해야 하는 지를 판단하는 테스트
* 총 13개의 상황에 대해서 2가지 상황 중에 선택을 해야 하는데, 선택을 하기가 쉽지 않습니다. 
    * 끝까지 진행하시면 스스로가 어떤 기준으로 윤리적인 판단을 하는지에 대해서 확인해 볼 수 있습니다. 
* 이와 별개로 자율주행에는 사고 시에 배상 및 책임 관련해서도 재미있는 주제라 찾아볼 만 합니다. (제조사가 책임을 어디까지 포함해야 하는지)

#### [디지털 노마드 관련]
* 주거 및 식사를 위한 낮은 비용과 IT 인프라가 갖추어진 도시들이 노마드에 적합하다고 합니다.
* 그 중에서도 주변에 휴식을 위한 아름다운 자연을 갖추고 있는 발리가 좋아 보이네요.
* 저희 회사도 TDR/Task에 대해서 Challenge한 골을 주고 대신 디지털노마드로 작업공간을 자유롭게 지원해줄 수 있는 날이 올까요?
    1. 발리: [디지털노마드? 발리 한 달 살기(총 116만원)](https://brunch.co.kr/@lynnata/15){:target="_blank"}
    2. 발리: [나는 왜 디지털 노마드가 되었나](https://brunch.co.kr/@rabbitchoi/1){:target="_blank"}
    3. 방콕: [Neo Digital Nomad! (주)카닥의 디지탈 노마드 실험. 카닥 해외 전지훈련기](http://joonnoh.com/blog/5881){:target="_blank"}


#### [직원 3만명 넘는 회사에서 메일링 리스트 관리를 허술하게 하면 발생하는 일](https://www.reddit.com/r/talesfromtechsupport/comments/420oan/companywide_email_30000_employees_autoresponders/){:target="_blank"}
* 사건 요약
    1. 누군가가 전체 임직원이 등록된 메일링 주소로 메일을 보냄
    2. 휴가/부재중인 사람들이 등록한 자동회신 메일이 전체 메일로 발송됨
    3. 자동회신 메일에 대한 자동회신 메일이 발송됨 (반복)
    4. 인프라 장애 발생
    5. 인프라 담당자가 자동회신 처리가 되지 않도록 조치 후 재시작 
    6. 일부 자동회신 메일이 처리가 누락 ->  2번 이후 상황 재발생
* 전체 alias 메일에 대해서 접근권한이 필요하다는 교훈을 얻을 수 있습니다. 


#### [Bubble sheet multiple choice scanner and test grader using OMR, Python and OpenCV](http://www.pyimagesearch.com/2016/10/03/bubble-sheet-multiple-choice-scanner-and-test-grader-using-omr-python-and-opencv/){:target="_blank"}
{% include image.html path="post/opencv_poc_using_python.png" path-detail="post/opencv_poc_using_python.png" %}
* Python과 OpenCV를 사용하여 객관식 시험 자동 채점사례 입니다.
* IT에서 일반적인 기술도 다른 분야와 접목되면 유용한 경우를 만들 수 있어 보입니다.
* 그런데 시험지 사진을 찍고, 다음장으로 넘기는 부분에 대한 자동화도 고민이 필요할 것 같네요.

## 문제해결 및 코딩인터뷰 관련

#### [Cracking the Coding Interview](https://www.hackerrank.com/domains/tutorials/cracking-the-coding-interview){:target="_blank"}
* 믿고 쓰는(?) `hackerrank`에서 제공하는 코딩인뷰 관련 튜토리얼과 영상 입니다.  
* 굳이 코딩인터뷰를 준비할 필요가 없는 분들이라도, 가벼운 마음으로 영상을 보면서 문제를 풀어보면 재미 있습니다. 
* 자매품으로 [30 Days of Code Challenges](https://www.hackerrank.com/domains/tutorials/30-days-of-code){:target="_blank"}도 있습니다.

## 기타 읽을거리

#### [몰리 가드 (molly-guard)](https://en.wiktionary.org/wiki/molly-guard){:target="_blank"}
{% include image.html path="post/molly-guard.png" path-detail="post/molly-guard.png" %}
* 거대한-빨간-버튼을 덮는 플라스틱 커버를 '몰리 가드' 라고 부릅니다.
* 어원이 재미있습니다. 
> 한 프로그래머의 딸이 IBM 메인프레임의 버튼을 자꾸 누르려고 해서 커버를 달았는데 그 딸의 이름이 `몰리` 였다고 합니다.

#### Mythbusters - Soccer Ball Shot from Truck
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/BLuI118nhzc?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 50Mph 로 달리는 트럭에서, 진행방향과 반대 방향으로 50Mph로 공을 발사하면 어떻게 될까요?
* 저처럼 물리 이론에 대해서 직접 경험하기 전까지 신뢰하지 못하는(?) 분들은, 해당 동영상을 보면 느낌이 새롭습니다.

#### [업무일지 작성을 도와주는 스크린샷 자동 저장 앱](http://imays.blog.me/220825210221){:target="_blank"}
* 스스로의 하루 업무에 대해서 되돌아 볼 수 있게 해줍니다.
* 분단위로 어떤 일을 하면서 하루를 보냈는지 Tracking 할 수 있습니다. 
* WPPM (원단위 낭비제거)을 하던 시절이라면 필수 앱이었을 것 같네요

#### ["성과급 받은 직원이 더 열심히 일한다는 생각은 리더의 착각"](http://m.biz.chosun.com/svc/article.html?contid=2016100701594){:target="_blank"}
* 성과급이 효능이 없다라고 생각하지는 않지만, 금액에 비례하지는 않는다고 생각합니다. 
* 저는 현재의 인센티브 제도를 개선해서, (외국의 경우처럼) `근속년수에 비례`해서 `자사주`로 지급하는 것도 좋아 보입니다. 
    * 회사에서의 인력이탈 방지, 회사의 주식/가치를 올리기 위해서 적극적으로 참여하도록 유도
