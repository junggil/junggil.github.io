---
layout: post
title: "[NewsLetter] AWS re-Invent 2016 Summary"
description: "AWS re-Invent를 통해 신규로 소개된 AWS 서비스들에 대한 정리, MS Azure와의 비교"
tags: [AWS re-invent, Keynote, Andy Jassy, Werner Vogels, MS Azure, Cloud, Conference]
---

## AWS re:Invent 2016 총정리 
{% include image.html path="post/aws-reInvent-2016.png" path-detail="post/aws-reInvent-2016.png" %}
* 마인드맵 [Download (png, pdf, mindmap)](http://okky.kr/article/363825){:target="_blank"} 
* [AWS re:Invent 2016 총정리 - 윤석찬](https://aws.amazon.com/ko/blogs/korea/summary-of-aws-reinvent-2016/){:target="_blank"}
* [Azure 관점에서 본 AWS re:Invent 2016 관전기](http://anthonychu.ca/post/aws-reinvent-2016-announcements/){:target="_blank"}
    * Azure 진영에서는 PaaS/SaaS 측면에서는 AWS보다 Azure가 우위에 있다고 판단
    * Lambda (Azure Functions)만이 AWS가 우수하다고 생각하고, 나머지 분야에 대해서는 아직 Azure가 우수하며  AWS가 이번 발표로 많이 Azure와 근접한 것으로 평가

## 기조 연설 (Keynote Speech)

* `Andy Jassy`, `Werner Vogels`의 기조연설은 꼭 들어야 합니다.
    * James Hamilton은 Infra에 대해서 Deep하게 관심있는 분들을 제외하고는 추천하지 않습니다.

#### Andy Jassy, CEO (AWS)
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/8RrbUyw9uSg?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>

#### Werner Vogels, CTO (Amazon)
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/ZDScBNahsL4?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>

#### James Hamilton, VP and Distinguished Engineer (AWS)
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/AyOAjFNPAbA?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>


## AWS re:Invent 신규 서비스 출시 정보
{% include image.html path="post/aws_reinvent_new_services" path-detail="post/aws_reinvent_new_services" %}

#### [Amazon Athena](https://aws.amazon.com/ko/blogs/korea/amazon-athena-interactively-query-petabytes-of-data-in-seconds/){:target="_blank"}
* S3기반으로 동적 Query 지원
    * Redshift, EMR 연동 없이 좀더 쉽게 데이터 분석 및 처리가 가능할 듯
* 연관 서비스
* AWS Glue: S3, RDS를 소스로 하여 전처리(ETL)을 지원
* AWS Batch: S3를 기반으로 spot-instance를 활용하여 full scale 배치 작업을 지원
* Tokyo에서 바로 사용 가능

#### [Amazon Polly](https://aws.amazon.com/ko/blogs/korea/polly-text-to-speech-in-47-voices-and-24-languages/){:target="_blank"}
* 클라우드 기반의 TTS 엔진 
    * 24개 언어 47개 음성합성 지원, 번역은 미지원
* 동음 이의어, 약어, 숫자, 화폐단위, 날짜, 시간, 단위 등의 처리 지원
* SSML (Speech Synthesis Markup Language)를 사용하여 어구 강조, 악센트 처리 등의 디테일한 컨트롤 가능
* 한국어 미지원
* 북미 및 일부 유럽에서 사용 가능

#### [Amazon Lex](https://aws.amazon.com/ko/blogs/korea/amazon-lex-build-conversational-voice-text-interfaces/){:target="_blank"}
* ASR(자동 음성 인식) 및 NLU(자연어 이해) 엔진
* Slot이라는 개념이 있어서 특정의도에 꼭 필요한 항목을 대화형으로 채울 수 있도록 도와줌 
    * 예: 비행기 예약 – 날짜, 출발, 도착, 항공사가 슬롯으로 정의 되어있으면 사용자가 명시하지 않은 나머지 항목을 대화로 물어서 채움
* Business Logic 처리를 위해서 Lambda 실행 가능
* Lex + Polly로 Alexa와 유사한 대화형 음성 (+ 텍스트) 인터페이스 구성 가능
    * AVS기반으로 현재 검토 되고 있는 대화형 서비스들에 대해서 향후 방향을 검토해볼 필요가 있을 것 같습니다.
* Preview 상태로 버지니아 region에서만 Preview 신청한 사용자만 사용 가능

#### [AWS Greengrass](https://aws.amazon.com/ko/blogs/korea/aws-greengrass-ubiquitous-real-world-computing/){:target="_blank"}
* 설치형 AWS IoT 및 AWS Lambda 서비스
    * MQTT Broker / Security (Registry) / Lambda (python만 지원) / Shadow로 구성
    * Offline의 경우에도 동작성 보장과 반응 속도 향상이 가능
    * 원격에서 Device에 Logic 배포 가능 (Lambda Injection)
* GreenGrass Core (GGC)와 IoT Device SDK로 구성 (제약 조건 때문에 LGW, ZB 기반 Sensor등에 당장 적용은 어려울 것 같네요)
    * GGC: 128MB 이상의 메모리와 1GHz 이상의 x86 또는 ARM CPU 필요
    * IoT Device SDK: C++만 현재 지원 (IP 기반 네트워크에서만 사용가능, ZB, ZWave 미지원)
* Preview 서비스라 참여 신청한 고객만 제한적으로 사용 가능
