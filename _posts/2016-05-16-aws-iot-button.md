---
layout: post
title: "[NewsLetter] AWS IoT Button 출시 (+ 3건)"
description: "AWS Dash가 DRS이외의 용도로 범용적으로 활동될 수 있도록 IoT Button라는 이름으로 출시됨."
tags: [AWS IoT Button, Lambda, Chirp, 하이퍼루프]
---

## 개발 관련

#### [AWS IoT Button](https://aws.amazon.com/iot/button/){:target="_blank"}
{% include image.html path="post/aws_iot_button.png" path-detail="post/aws_iot_button.png" %}
* AWS Dash가 범용적으로 확장되어서 `IoT Button` 이라는 이름으로 나왔습니다. 
* SINGLE / DOUBLE / LONG 입력에 대한 구분이 가능하며, Lambda를 연결해서 원하는 동작을 구현할 수 있습니다.  아래는 AWS IoT 설명 페이지의 사용 예시입니다. (요약: 생각하는건 다 할 수 있다)
* Wifi 연결을 지원하며 개당 가격은 $20 인데 Stock이 없어서 현재 주문은 불가능 합니다. 
    * [제품 링크](http://goo.gl/jtrf5d){:target="_blank"}
* 구매가 가능하면 AWS IoT Button으로 팀내에서 `Hackerthon`을 해봐도 좋을 것 같습니다.

> Netflix의 원격 제어, Papa John의 피자 주문 버튼, Philips Hue Light의 스위치, Airbnb 승객용 피드백 버튼으로 사용할 수 있습니다. 버튼 클릭으로 자동차의 잠금을 해제하거나 시동을 걸고, 택시를 부르고, 아내에게 전화하고, 차고 문을 열고, 사용 현황(기저귀, 아기의 수면)을 추적하거나, 가전제품을 원격으로 제어하도록 구성할 수 있습니다. 또한, "좋아요" 버튼, "모드" 버튼 또는 "비상 버튼"으로도 사용할 수 있습니다. Twitter, Facebook, Twilio, Slack과 같은 타사 서비스와 통합할 수 있을 뿐 아니라 여러분 회사의 애플리케이션 및 시스템과 통합하는 등 아직 AWS에서 생각하지 못한 다른 많은 사물과 통합할 수 있습니다.

#### 아마존과 google 
* Google -> Amazon 
    {% include image.html path="post/google_chirp_based_on_weave.png" path-detail="post/google_chirp_based_on_weave.png" %}
    * Google은 Amazon echo를 따라서 Brillo 기반의 홈 비서 처프 (Chirp)를 올해 중에 출시 예정
    * [관련기사- 아마존 에코에 대한 구글의 대항마 ‘처프 (Chirp)’](http://techneedle.com/archives/26595?utm_content=buffer1402f&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer){:target="_blank"}
* Amazon -> Google
    <div class="embed-responsive embed-responsive-16by9">
    <iframe src="https://www.youtube.com/embed/2Tgx7ACMjp4?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
    </div>
    * 아마존은 google의 youtube를 따라서 video direct를 선보였습니다.
    * 두 회사가 서로의 Business 영역으로 사업을 확장해 나가는 양상입니다.

#### 하이퍼루프 첫 시연 성공적
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/QCNJNmrViv8?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 많은 분들이 알고 계시겠지만 테슬라 모터스, SpaceX의 창업자 엘론 머스크의 구상 작품 입니다. 
    * SpaceX 바지선 재착륙 1차 2차 영상를 보면서도 느꼈지만, 엘론 머스크는 기술에 대한 `이미지메이킹`을 잘 하는 것 같네요.
* 위에 동영상의 주행실험에 따르면 1.1초 만에 시속 116마일 (187Km) 에 도달했다고 합니다. 

#### 화재시 행동 요령
{% include image.html path="post/in_case_of_file.png" path-detail="post/in_case_of_file.png" %}
* 다들 비상시에 행동 요령은 잘 알고 있을 것 같지만 다시 한번 공유 드립니다 (...)
