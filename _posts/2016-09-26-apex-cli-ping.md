---
layout: post
title: "[NewsLetter] Apex, Cloud CLI Tool (+ 8건)" 
description: "Serverless 관리 개발 도구인 Apex CLI와 Cloud Monitoring Tool인 Apex Ping 소개"
tags: [Serverless, Apex cli, Apex ping, Amazon Echo, MSA, APNS, Problem Solving, Dev Writing]
---

## 개발 관련

#### Apex 소개
* Apex Ping: 특정 서비스가 정상인지 여부를 확인할 수 있는 `서비스 모니터링 툴`입니다. 한달동안 **무료**로 5개 API / 2개 알람을 등록할 수 있으니 써보는 것을 추천합니다. 
* Apex: Apex는 조직이름이면서 `Serverless 아키텍처`를 지원하는 CLI 툴 이름이기도 합니다.  Lambda 개발 및 배포는 Web으로 하는 것보다 간편하게 작업이 가능합니다. (그렇지만 API-Gateway외에 AWS IoT에 Lambda등에 트리거 걸기 위해서는 콘솔 접근이 필요합니다).  인프라 운영 업체(KINX)에서 IAM을 공유 받지 못해서 console 접근이 어려운 경우도 유용할 수 있습니다. 
* 참고자료
    * [Apex - AWS Lambda 관리도구 #1](https://blog.outsider.ne.kr/1241){:target="_blank"}
    * [Apex - AWS Lambda 관리도구 #2](https://blog.outsider.ne.kr/1242){:target="_blank"}
    * [Apex로 실제 Lambda 함수 작성하기](https://blog.outsider.ne.kr/1243){:target="_blank"}
    * [일일커밋 알림봇 개발기](https://mingrammer.com/dev-commit-alarm-bot){:target="_blank"}


#### [IFTTT + BT기반 마이크로 로봇을 통해 앱으로 현관문 제어하기](http://oooz.net/watch-dogs-2/){:target="_blank"}
{% include image.html path="post/poc_door_control_system.png" path-detail="post/poc_door_control_system.png" %}
* 가정집 현관문 (인터폰을 누르면 현관이 열리는)을 키 없이, 앱으로 제어하고 싶다는 생각에서 삽질(?)이 시작됩니다. 
    * 1편에서 [라즈베리 파이를 통해서 최초 솔루션](http://oooz.net/watch-dogs){:target="_blank"}을 찾지만, 외관이 흉칙 해서 실사용 되지 않다가 마이크로 로봇을 통해서 성공한 스토리 입니다. 
    * 사진은 1편의 결과물 vs 2편의 결과물
* onesound 님의 작품입니다. 
    * 이분은 만화가인데 만화만 잘 그리는게 아니라 개발쪽 영역에도 많은 관심을 보이고 실제로 동작하는 물건을 만들어 냅니다.
    * 개발자들도 생각에서 머무르지 않고 실제 구현까지 하기는 무척 어려운데 대단합니다. 

#### 아마존 에코 관련
* [아마존 에코 소유자, 아마존서 지출 늘었다](http://news.naver.com/main/read.nhn?mode=LSD&mid=shm&sid1=105&oid=092&aid=0002103313){:target="_blank"}
* [구매자 51%는 에코를 부엌에서 사용. 가장 많이 사용하는 기능은 타이머. 고객 87%가 만족](http://www.recode.net/2016/9/21/12997080/amazon-echo-survey-kitchen){:target="_blank"}

#### [마이크로서비스 아키텍처. 그것이 뭣이 중헌디?](http://www.popit.kr/%EB%A7%88%EC%9D%B4%ED%81%AC%EB%A1%9C%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98-%EA%B7%B8%EA%B2%83%EC%9D%B4-%EB%AD%A3%EC%9D%B4-%EC%A4%91%ED%97%8C%EB%94%94/){:target="_blank"}
{% include image.html path="post/sample_of_msa.png" path-detail="post/sample_of_msa.png" %}
* 서버리스 아키텍처 만큼 마이크로 아키텍처에 대한 언급을 많이 듣게 되는데요. 제가 봤던 자료 중에 가장 장/단점에 대해서 가장 정리가 잘 된 글이라고 생각합니다. 
* 서버구조의 차이뿐만 아니라 **클라이언트 관점을 포함**하고, `API Gateway`의 필요성에 대해서 설득력 있게 잘 정리 했습니다. 

#### [한국의 해커뉴스 데브뉴스](http://ow.ly/uSOx304pD2O){:target="_blank"}
* 말 글대로 Y Combination의 해커뉴스를 UI와 운영 방식까지 유사하게 한국에 도입한 사이트 입니다. 
* 아직은 글이 많지는 않고, Long run할 수 있을지는 모르겠지만 참고할 만 합니다. 

#### [애플 푸쉬서비스(APNs) 토큰 방식 인증 추가](https://code.iamseapy.com/archives/26){:target="_blank"}
* APNS 전송을 위한 서버 개발이 필요하신 분들은 눈 여겨 볼만 한 것 같습니다.
    * 기존의 불편한점은 인증서를 애플 개발자 사이트에서 다운로드 받아서 openssl로 한번 파일 변환해서 사용해야 했음
    * 더욱이 해당 인증서는 1년의 유효기간이 있어서 매년 갱신이 필요했음
    * Token은 openssl 변환이 필요 없으며 만료기간이 없음

## 기타 읽을 거리

#### [배송 파손 사고에 대한 문제해결 사례](https://twitter.com/jasongay/status/772556605548326912){:target="_blank"}
{% include image.html path="post/shipping_problem_solving_box_image.png" path-detail="post/shipping_problem_solving_box_image.png" %}
* VanMoof 에서 자전거 배송 파손 사고가 발생을 해결 하기 위해서 **박스에 TV 그림을 표시**
* 취급 주의 표시보다 효과가 확실해서 배송 사고가 극적으로 줄었다고 합니다.

#### VR을 위해 제작된 모든 방향으로 움직일 수 있는 트레드밀 Infinadeck V3 
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/seML5CQBzP8?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>

#### [개발자의 글쓰기](https://subokim.wordpress.com/2016/09/22/wt-of-dever/){:target="_blank"}
*  글 자체는 추천하지 않습니다. 
*  하지만 개발자에게 글쓰기 + 커뮤니케이션 역량은 개발 능력 이상으로 중요하다고 생각하고, 앞으로도 더 중요해 질 것이라고 생각해서 공유합니다. 
*  글 내용 중에 “천재를 제외하고 대부분의 사람들은 커뮤니케이션 스킬을 타고 나지 않습니다.” 라는 부분이 있는데, 저는 반대로 천재들은 더더욱 커뮤니케이션 스킬이 부족하기 때문에 더 많이 노력해야 한다고 봅니다.  (보통 천재들은 커뮤니케이션 스킬 부족을 인식하지 못하거나, 인식하더라도 그게 문제가 되지 않는 경우가 많은 것 같네요)
* 저는 그래서 글쓰기는 블로그 (SNS가 아니라) 쓰기가 좋아 보이고, 업무에서는 메일을 많이 쓰는 것도 도움이 된다고 생각합니다. (내용 요약 및 생각을 정리하는 용도로)
