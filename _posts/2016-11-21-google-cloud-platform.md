---
layout: post
title: "[NewsLetter] Google Cloud Platform 특집 (+ 13건)"
description: "GPU 인스턴스와, AWS RI (Reserved Instance)와의 요금제 비교 중심으로"
tags: [NewsLetter, GCP, AWS, RI, Microsoft, Slack, Clean-Architecture, TED]
---

## Cloud 관련

#### [Google Cloud is 50% cheaper than AWS](https://thehftguy.wordpress.com/2016/11/18/google-cloud-is-50-cheaper-than-aws){:target="_blank"}
{% include image.html path="post/relative_costs_summary.png" path-detail="post/relative_costs_summary.png" %}
* 무척 흥미롭게 읽은 기사 입니다
* 네트워크 / CPU / 메모리가 중요한 모든 경우에 대해서 `Google Cloud가 더 비용이 저렴`하다고 합니다.
    * 주의할 부분은 이 글은 EC2만을 대상으로 하기 때문에, Database / Cache / PaaS 등에 대한 비교는 별도로 필요합니다.
* AWS에서는 EC2 인스턴스에 대한 사용량을 미리 선구매 하는 Reserved Instance(RI)를 사용해서 비용을 줄일 수 있는데, 필자는 `RI를 사용을 가급적 하지 말 것`을 권장 합니다. 
    * 첫 번째 이유는 사용량에 대한 예측이 정확하기를 보장하기가 무척 어렵다는 것이고
    * 두 번째 이유는 Google Cloud에서 제공하는 Sustained use discounts 제도는, 사용량을 보장할 필요 없이 한 달에 25% 이상을 사용하면 자동으로 전체 요금에서 최대 30%까지 할인되기 때문에 비용 적인 측면에서도 RI보다 유리하다는 주장입니다. (설득력 있네요)

#### GPU 타입의 인스턴스 관련 
* 최근 유행인 GPU 기반 인스턴스 지원에 대한 AWS / MS Azure / Google 관련 기사들 입니다.
    * 9/29일 [AWS Announcing New P2 Instance Type for Amazon EC2](https://aws.amazon.com/ko/blogs/aws/new-p2-instance-type-for-amazon-ec2-up-to-16-gpus/){:target="_blank"}
    * 11/15일 [Announcing GPUs for Google Cloud Platform](https://cloudplatform.googleblog.com/2016/11/announcing-GPUs-for-Google-Cloud-Platform.html){:target="_blank"}
    * 11/16일 [Google's cloud GPU undercuts, outperforms AWS, Microsoft](https://goo.gl/ZY922a){:target="_blank"}
    * 11/18일 [“클라우드 GPU 경쟁 본격화” 구글, 분 단위 요금체계와 신형 하드웨어로 차별화](http://www.itworld.co.kr/news/102137){:target="_blank"}
* 일단 아직까지 요금제 및 성능에서 `Google 이 판정`승 입니다.

#### [Google Cloud Next](https://cloudnext.withgoogle.com/?utm_source=twittersocial2017-cloud-na-event-next-userconf-paidsocial-twitter-owned&utm_content){:target="_blank"}
* March 8–10, 2017 샌프란시스코
* AWS re:invent에 대응되는 컨퍼런스로 보입니다. 
    * re:invent는 사실 내용이 많이 익숙해서 배울 부분이 적어 보이는데, 여기는 참석해 보고 싶네요.
* 11/17일부터 Registration이 open된 상태입니다.

## 조직문화 관련

#### [Why good leaders make you feel safe](http://www.ted.com/talks/simon_sinek_why_good_leaders_make_you_feel_safe){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://embed.ted.com/talks/simon_sinek_why_good_leaders_make_you_feel_safe" width="640" height="360" frameborder="0" scrolling="no" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
</div>
* TED 동영상 입니다. (한글자막 지원)
* 오늘의 강력 추천 동영상입니다. 많은 사람들이 꼭 보기를 추천합니다. 
* “왜 훌륭한 리더는 우리가 안전하다고 느끼도록 만드는가?”
    * 리더가 자신을 `희생`해야, 사람들이 따르게 되고, 따르는 사람들이 리더가 제시하는 방향으로 스스로를 헌신하고 희생함
    * 구성원이 헌신적으로 노력하는 이유는, 리더도 자신을 위해서 희생을 할 것이라는 것을 믿기 때문
    * 리더와 권위자 (조직에서의 Position으로 얻은)는 다름

#### [박승남의 畵潭 | 제가 이 일을 왜 해야 합니까?](http://www.ciokorea.com/news/31887){:target="_blank"}
{% include image.html path="post/leadership_and_ownership.png" path-detail="post/leadership_and_ownership.png" %}
* 책임감이 본인의 R&R에 충실한 것이라면, 오너십은 그 범위를 넘는 것을 의미함
* 구성원의 오너쉽을 기대한다면 먼저 리더쉽을 보여주어야 한다. 

#### [없는 것을 만들었다고 하지 마세요](https://brunch.co.kr/@jinhoyooephf/12){:target="_blank"}
* 어떻게 해야 좋은 팀을 만들 것인지에 대한 Anti-Example을 통해서 설명합니다.
    * 가능한 이른 단계에서 개발자들과 함께 (진실하게) 소통할 것. 
    * 그리고 그럴 수 있는 사람들만 채용 할 것

#### [내가 개발을 포기하지 않을 수 있었던 이유](https://dobest.io/never-give-up/){:target="_blank"}
* 글 자체는 가볍습니다. 
* 다른 사람 (그게 자신이 존경하는 상대라면 더욱 더)으로 부터의 긍정적인 리뷰를 받는 경험의 중요성을 강조합니다.
    * 방법론적인 부분은 의견이 일치하지 않네요 ( VI  / 손코딩 / API 암기 … )

## 개발 관련

#### [Slack으로 막일을 줄여요 ~ 막일을 줄이기 위한 유용한 팁](http://www.popit.kr/slack-tip/){:target="_blank"}
* Slack 사용에 대한 소소한 팁입니다. 
* 개인적으로는 파트 내부에서 Slack을 통해서 offline으로 회의하기 전에 사전 업무 커뮤니케이션을 하는 것을 권장하고 있습니다.
* 전체 팀으로 확장이 되면 더 좋겠지만 아마도 일하는 성향의 선호도에 따라서 메신저 사용을 원하지 않는 경우도 많을 것으로 생각합니다. 

#### [Clean architectures in Python: a step-by-step example](http://blog.thedigitalcatonline.com/blog/2016/11/14/clean-architectures-in-python-a-step-by-step-example/#.WC5R0LKLSiM){:traget="_blank"}
* Clean architecture의 python 버전입니다. 
* 내용을 자세히 보지를 못했는데, 가능하면 이해하고 내부 세미나를 할 예정입니다. 

#### [To Compress Or Not To Compress, That Was Uber's Question](http://highscalability.com/blog/2016/3/21/to-compress-or-not-to-compress-that-was-ubers-question.html){:target="_blank"}
{% include image.html path="post/total_encode_decode_time.png" path-detail="post/total_encode_decode_time.png" %}
* 결론부터 이야기 하면 JSON을 쓰지 말라는 것입니다.
    * 위에 그림은 Uber에서 테스트한 결과 입니다. 
    * 인코딩/디코딩에 대한 성능저하가 주된 이슈이고 
    * 가급적 바이너리 기반의 프로토콜을 쓸 것을 (특히 IoT라면 더더욱) 권장 합니다. 
* 영미권에서도 개를 안좋은 의미로 쓰나보네요. 본문에서 JSON을 개처럼 느리다 (dog slow) 라고 표현하네요.

#### [정규표현식 테스트 사이트](https://regex101.com/){:target="_blank"}
* 정규표현식에 대해서 테스트 해보기 좋은 사이트 소개 합니다. 
* 최근 UI가 리뉴얼이 되었고 언어별 (php, python, go, javascript) 지원도 일부 포함합니다. 


## 기타 읽을 거리

#### [Microsoft joins The Linux Foundation as a Platinum member](http://venturebeat.com/2016/11/16/microsoft-joins-the-linux-foundation-as-a-platinum-member/){:target="_blank"}
* MS의 최근 행보가 과감하고 과거의 폐쇄적이었던 것에 비해서 방향성도 무척 마음에 듭니다. 
* 참고로 플래티넘 회원은 연간 $500,000 비용을 내도록 되어있는데, 현재 10개의 회사가 있고 삼성이 여기 포함입니다.
    * 이와 상대적으로 LG는 2010년에 일반회원으로 가입을 했네요.

#### 계획과 현실의 차이
{% include image.html path="post/plan_and_reality.png" path-detail="post/plan_and_reality.png" %}

#### 2015 단국대학교 마이크로로봇 경연대회
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/IUUvdLSic10?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 마이크로 로봇이 정말 많이 발전했군요. 
* 한번 지나간 길에 대한 맵을 구성해서, 재탐색시에는 정말 빠른 속도로 목표물을 찾아갑니다. 
* 한번 심심할 때 보면 재밌습니다. 
    * 워크샵 같은 형식으로 팀 행사로 실제 해보면 어떨까 싶습니다.
