---
layout: post
title: "[NewsLetter] 일 년에 한 개의 사이드 프로젝트 (+ 21건)"
description: "개인프로젝트를 진행을 위한 Tip과 성공 사례들 중심으로"
tags: [개인프로젝트, Jarvis, HTTP/2, Leap Second, Amazon Go, 오픈소스 참여, 권력 중독, 리더쉽, SIRU Cafe, 자율주행, 드론배송, 김어준]
---

## 개발 관련

#### [일 년에 한 개의 사이드 프로젝트](https://medium.com/ui-ux-post-translator/%EC%9D%BC-%EB%85%84%EC%97%90-%ED%95%9C-%EA%B0%9C%EC%9D%98-%EC%82%AC%EC%9D%B4%EB%93%9C-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EB%B2%88%EC%97%AD-75e55b224626#.t1n2khc3d){:target="_blank"}
{% include image.html path="post/done_is_better_than_perfect.png" path-detail="post/done_is_better_than_perfect.png" %}
* 끝까지 `완료` 할 수 있는 프로젝트를 위한 지혜를 얻을 수 있습니다.
* 개인 프로젝트를 하면서 어려움을 겪는 주요 이유는
    * 선택의 모순 : 선택에 대한 고민이 일정 지연을 가져오고, 반복되면 프로젝트 진행이 어려워짐
    * 마감일의 부재 : 스스로에게 동기부여를 하기 위해서도 데드라인의 중요한 의미를 갖음
* 저의 2017년에 계획하는 개인 프로젝트 목록입니다.
    * ~~github + jekyll로 blog 운영하기~~ (완료. 지금 보고 있는 페이지 입니다)
    * Slack Bot 운영 (JIRA연동 알림, 혹은 Server에 미반영 수정사항 알림)
    * AWS IoT Button + Echo 연동 시나리오 발굴 및 PoC
    * 오픈소스 참여 (가능한 python)

#### Mark Zuckerberg reveals AI assistant, Jarvis
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/ZGLPxEv_EWo?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* Mark Zuckerberg가 개인 프로젝트 결과를 공개했습니다.
* Amazon Echo / Google Home과 같이 Voice 기반의 IoT 제어를 포함하는 비서 시스템으로
    * 100시간의 개발시간이 소요되었다고 하며, 
    * 개인프로젝트의 규모와 모건 프리먼의 목소리가 인상적입니다.
    * 특허 출원중인 관련 구조도는 아래와 같습니다. 
{% include image.html path="post/Jarvis.jpg" path-detail="documentation/sample-image@2x.jpg" alt="Sample image" %}

#### [Look Before You Leap – December 31, 2016 Leap Second on AWS](https://aws.amazon.com/ko/blogs/aws/look-before-you-leap-december-31-2016-leap-second-on-aws/){:target="_blank"}
* 세슘 원자시계와 실제 시간의 보정을 위해서 윤초 1초가 삽입될 예정입니다. 
* 2016년 12월 31일 23:59:59가 2번 발생하는 형식으로 보정이 되는 것이 일반적인 해법인데 AWS에서의 대응방법을 소개합니다.
    * EC2 (Amazon Linux): 자동으로 윤초가 적용됩니다. 관리할 필요 없음. 
    * EC2 (Amazon Linux 외): AWS에서 제공하는 NTP 서버 (Amazon Adjusted Time Server)로 시간 동기화 설정 필요.
    * RDS: 12월 31일 23:59:59가 2번 발생하도록 자동으로 보정
    * PaaS (AWS IoT, Lambda, API Gateway, DynamoDB): 자동으로 보정될 것으로 예상하지만 `확인 필요`


#### [나만 모르고 있던 HTTP/2](http://www.popit.kr/%EB%82%98%EB%A7%8C-%EB%AA%A8%EB%A5%B4%EA%B3%A0-%EC%9E%88%EB%8D%98-http2/){:target="_blank"}
* HTTP/1.1과의 하위호환성을 유지하면서, 3 가지 개선을 이룸
    1. Multiplexed Streams : 1개의 Connection으로 비동기 요청 전송 가능
    2. Server Push : Client가 요청하기 전에 서버에서 HTML 문서 구조를 분석해서 필요한 리소스를 전달
    3. Header Compression: Huffman Encoding을 적용하여 전송 사이즈를 최소화
* 그런데 위의 사항들은 기본적으로 HTML 기반 Web 페이지를 전제로 하였기 때문에, 
    * REST API 서버에 대해서는 3번만이 의미가 있음 (HTTP/2의 효과가 상대적으로 `낮음`)
    * 관련 Stackoverflow 글 [Link](http://stackoverflow.com/questions/31692868/rest-api-with-http-2){:target:"_blank"}

#### Amazon Go 관련
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/NrmMk1Myrxc?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* Amazon Go에 사용된 기술과, 일자리 관련된 이슈를 같이 살펴보겠습니다.
    1. [아마존고(Amazon Go)는 어떤 기술이 적용되었나?](http://www.marketcast.co.kr/2158){:target="_blank"} : 컴퓨터비전, 딥러닝, 센서퓨전
    2. [무인점포 확산에 발 빼는 아마존](http://news.joins.com/article/20990309){:target="_blank"} : 노동계의 반발에 2,000개 점포 확산 계획을 취소
    3. [Amazon Go: We’re All Fucked](https://iot-for-all.com/amazon-go-were-all-f-cked-e6fb885f94c4#.p58dajqnn){:target="_blank"} : 무인화, 자동화가 전체 노동력의 47% 가량에 위협을 줄 것이라는 분석
* 역시나 일자리 및 소득이 걸린 민감한 사안이라 아마존 역시 조심스러운 상황으로 보입니다. 
    * 향후 기술 발전으로 일자리가 사라지는 경우에 대한 논의가 활발해 질 것 같습니다. 
    * 예: 기본 소득 – 노동 여부와 관계없이 사회 구성원들에게 균등하게 지급되는 소득

#### [오픈 소스에 참여하는 가장 쉬운 방법](https://emaren84.github.io/blog/archivers/the-easiest-way-to-get-into-open-source-kor){:target="_blank"}
{% include image.html path="post/easiest_participant_open_source_project.png" path-detail="post/easiest_participant_open_source_project.png" %}
* 문서로 프로젝트에 참여를 시작하라는 의견은 전적으로 동의합니다.
    * 문서화는 기존 프로젝트 인원에게도 꼭 필요한 부분이고, 
    * 신규 참여인원이 코드에 대한 테스트 및 개발환경 없이도 참여할 수 있으며,
    * 그 과정에서 전체 구조를 파악할 수 있다는 측면에서 도움이 된다고 생각합니다.
* 당장의 팀 내부의 프로젝트들도 이런 방법으로 오픈소스화 하여서, 내부 인원에게 `자유로운 참여`를 유도하면 좋을 것 같습니다.

## 개발 도구 관련 

#### [regexgen](https://github.com/devongovett/regexgen){:target="_blank"}
{% include image.html path="post/regexgen_sample.png" path-detail="post/regexgen_sample.png" %}
* 입력한 string들에 대응되는 정규표현식을 자동으로 생성해 줍니다.
* 개발과정에서 특정 패턴에 해당하는 정규표현식이 필요할때 사용하기 좋을 것 같습니다.

#### [sanic](https://github.com/channelcat/sanic){:target="_blank"}
{% include image.html path="post/benchmark_result_of_sanic.png" path-detail="post/benchmark_result_of_sanic.png" %}
* Python3.5+ 기반 Flask 기반의 고성능 웹서버입니다. 
    * 벤치마크 결과 Flask보다 8배 정도의 TPS를 보입니다.

#### [Python3.6 에서 바뀐점](http://raccoonyy.github.io/whats-new-in-python-3-6-korean/){:target="_blank"}
* Python3.6이 12월 23일에 정식출시되었습니다.
* 관련해서 새롭게 추가된 내용과, 바뀐 문법에 대해서 정리한 글입니다.
    * 저는 f 문자열 포매팅(PEP 498)와, 타입힌트(PEP 484)가 마음에 듭니다.

#### 무료 DB GUI Tool (SQL Client)
{% include image.html path="post/dbeaver_screen_shot.png" path-detail="post/dbeaver_screen_shot.png" %}
* Mac, Linux 에서 쓸만한 DB Tool - DBeaver
    * 속도와 안정성 면에서 MySQL Workbench보다 우수하다는 평입니다.
    * [WorkBench와 비교한 리뷰](http://lifeones.tistory.com/129){:target="_blank"}
    * [다운로드 링크](http://dbeaver.jkiss.org/){:target="_blank"}
* 보다 Mac의 UX에 근접한 가벼운 DB Tool - Sequel Pro
    * [다운로드 링크](https://sequelpro.com/download){:target="_blank"}

## 조직문화 관련

#### [왜 리더는 뱀에 물릴까?](https://brunch.co.kr/@unitasbrand/22){:target="_blank"}
* 리더가 경계해야 할 대상에 대해서 흐름을 놓치지 않고 긴 문장으로 풀어낸 명문 입니다.
* 그 중에서도 주로 `권력 중독`으로 변질된 리더쉽에 대한 글 입니다. 
* 권력 중독적인 리더쉽은 주변에도 부정적인 영향을 주며, 권력 중독된 리더는 결코 `변하지 않기 때문`에 피하는 거나 퇴사만이 해결책으로 제시합니다.
* 아래는 본문 내용 중에 발췌 합니다.
    * 권력을 가진 사람들은 자신이 독재자라고 생각하지 않는다, 그저 카리스마가 남들보다 강하다고 생각을 할 뿐이다. 
    * 권력에 중독이 되면 보편적인 상식과 기본적인 양심의 기능들이 마비된다. 
    * 권력 중독에 빠진 리더쉽은 바뀌지 않으며, 주변 팔로워들을 맹목적인 친위대로 변질시켜 버린다. 
    * 현대사회에서의 예스맨(Yes Man)은 개인적인 업무 성과보다는, 리더와의 관계를 통한 성과를 잘 내는 사람으로서 리더 지향적인 특징이 있다. 
    * 절대권력은 어떤이에게는 절대 특권을 주기 때문에, 절대 권력자가 비록 도덕적 기준에서 틀린 행동을 하더라도 묵인한다.
    * 뱀(추종자)은 다른 직원을 공격할때는 이빨에서 뿜어져 나오는 맹독을 사용하지만, 리더를 공격할 때는 이빨이 아니라 혀로 중독시킨다.
    * 리더 주변에는 조심할 사람, 매우 조심할 사람, 매우 매우 조심할 사람이 있다.
    * 이 중에는 리더의 뼈를 썪게 하고 조직을 썩게 만드는 사람이 있으며, 그런 사람의 출현은 리더가 스스로 만든다.

#### 리더로서의 성공의 기준
{% include image.html path="post/goal_of_leadership.jpg" path-detail="post/goal_of_leadership.jpg" %}
* 구성원은 자기 자신의 성장을 목표로,
* 리더는 구성원들을 성장시키는 것을 목표로 해야 한다.

#### [직장에서 윗년차가 되는 친구들에게](http://ppss.kr/archives/65565){:target="_blank"}
{% include image.html path="post/senior_and_junior.png" path-detail="post/senior_and_junior.png" %}
* 비단 병원에만 해당되는 사례가 아니라, 모든 조직에 적용될 수 있는 교훈이 담겨있습니다.
* 모든 사람이 한번씩 훑어 보면 좋을 것 같습니다.

> 누구나 곧 윗년차가 된다. 이 작은 지위는 군대놀이에 쓰일 수도 있고, 누군가를 끌어주는 데 쓰일 수도 있다. 피해자는 이 시스템 속에서 쉽게 다시 가해자가 될 수 있다.

## 기타 읽을 거리

#### [커피를 공짜로 팔아도 돈버는 카페](https://brunch.co.kr/@stayclassy/11){:target="_blank"}
{% include image.html path="post/siru_cafe_concept.png" path-detail="post/siru_cafe_concept.png" %}
* 카페의 비지니스 모델을 과감하게 바꾼 사례입니다.
* 흥미로운 사례로 읽어보는 것을 추천합니다. 아래는 기존 카페와의 차이점을 요약했습니다.
    * 학생들로 고객을 제한함.
    * 학생들이 카페를 다양한 목적으로 활용할 수 있도록 공간을 제공. 
    * 학생들의 유입을 위해 충전기, 회의실, 외부음식반입 허용, Wifi, 무료커피를 제공.
    * 그 과정에서 자연스럽게 채용을 원하는 기업을 홍보하는 모델.

#### [Truckers think automation won’t take their jobs for 40 years. Silicon Valley strongly disagrees.](http://qz.com/854117/truckers-think-automation-wont-take-their-jobs-for-40-years-silicon-valley-strongly-disagrees/){:target="_blank"}
{% include image.html path="post/trucker_most_common_job_in_us.png" path-detail="post/trucker_most_common_job_in_us.png" %}
* 40년 이내에는 직업이 위헙받지 않을 것이라는 Trucker들의 기대와는 달리, 
    * 실리콘밸리의 전문가들은 10년 이내에 자율주행 기술이 적용될 것이라고 확신합니다. 
* 자율주행 기술은 중산층을 구성하는 Trucker 1.7M명의 기존 일자리가 사라지게 만드는 것 뿐만 아니라 
    * $700B에 다다르는 관련 산업의 비용구조를 크게 바꿀 것이며,
    * 이것은 다음 대선과도 연관된다고 볼 수 있음.

#### [Amazon drivers say they are pushed to the limit as holiday deliveries reach a frenzy](http://www.latimes.com/business/la-fi-amazon-drivers-20161218-story.html){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/vNySOrI2Ny8?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 국내 택배기사들의 문제가 Amazon을 통해 미국에도 동일하게 적용되고 있고, Amazon과 택배기사간의 분쟁이 끊이지 않습니다.
    * 하루 260개의 배달을 하기위해 평균 2분마다 배송을 완료해야하고, 
    * 비용절감을 위한 재하청 구조(FedEx, UPS, 개인사업자등)로 구성됩니다. 
    * 발생하는 지연배송 claim은 고객에서 Amazon을 거쳐 배송업체로 넘어오고, 
    * 매주 집계된 claim 누적수가 높은 직원은 동료들 앞에서 공개적으로 모욕을 당합니다. 
    * 이러한 압박은 배달 중에 식사시간을 포기하기 만들고, 결국 기사들은 Amazon 택배수거함이 설치된 편의점(7-Eleven)에서 택배수거와 함께 핫도그로 식사를 대신하는 경우가 많다고 합니다. 
* 자율주행, 드론배송 등이 물류업체의 현실적인 필요성을 바탕으로 한다는 생각이 들게 만들었던 글입니다. 
    * 배송 관련 구조적인 문제를 근본적으로 해결하기 위해서라도 Amazon은 드론배송등의 배송 혁신에 투자가 필요한 상황으로 보입니다.
    * 위의 영상은, 최초 공식 드론배송을 현실화한 동영상입니다.

#### [알고리즘 문제 풀이 실력을 발전시키는 방법](https://www.acmicpc.net/blog/view/48?utm_content=buffer5d8f8&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer){:target="_blank"}
* 항상 이런 글들이 그렇듯이 특별한 방법이 없다가 결론입니다.
* 많은 시간을 쓰고, 친구들과 함께 하는 것이 유일한 방법인 것 같습니다.

#### [파이썬을 만난지 100일째](http://www.slideshare.net/ssuser971274/100-70226396){:target="_blank"}
* 자기개발을 위한 개인프로젝트 진행을 하고, 
* 해당 결과를 블로그로 기록하며 노력이 계속 될 수 있도록 알람을 통해서 자극을 유지하는 시도의 기록이 좋았습니다.
* 작은 것부터 완성을 이루는 자세가 훌륭하고 자극이 많이 되었습니다. 
    * Done is better than Perfect

#### '나는 언제 행복한 사람인지?' - 김어준
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/1zmnoElezRg?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
> "바보 같은 얘기처럼 들릴지 모르겠는데 사람들은 어떤 일을 하고 싶을 때 제일먼저 하는 게 뭔지 알아요?  다른 사람들한테 그 일이 얼마나 어려운지 설명하는 겁니다.  그 일이 실패했을 때 자기가 못난 사람이 안되려고 말입니다.  원래 워낙에 어렵고 힘든 일이기 때문에 내가 실패했어도 내가 못난 게 아니라는 이야기를 주변사람들한테 퍼트리는 걸 제일먼저 합니다. 열심히.  그런데 그러다 자기가 설득이 되요.  정말 어려운 일이구나.  그래서 주변에서 왜 아직 안하고 있냐 물어보면 화를 냅니다. 너는 그게 얼마나 어려운지 몰라서 그러는 거야.  자기가 자기한테 설득이 됩니다.  정말 어려운 일이구나.  마침내 안하게 되죠. 그 일은 너무 어려운 일이기 때문에 안 해도 되는 일, 어차피 못하는 일, 다들 실패하는 일이 돼서 그 일은 시도조차 하지 않고 그냥 끝나 버립니다."

## 짤방 관련

#### 개발자의 원죄
{% include image.html path="post/you_should_not_have_been_developer.jpg" path-detail="post/you_should_not_have_been_developer.jpg" %}

#### 프로그래밍을 배우는 과정
{% include image.html path="post/tring_to_learning_programming_language.jpg" path-detail="post/tring_to_learning_programming_language.jpg" %}

#### 다른사람과 대화를 할때의 주의점
{% include image.html path="post/when_you_say_other_people.jpg" path-detail="post/when_you_say_other_people.jpg" %}
