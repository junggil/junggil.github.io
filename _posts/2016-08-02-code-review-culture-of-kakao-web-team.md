---
layout: post
title: "[NewsLetter] 카카오스토리 웹 팀의 코드리뷰 경험 (+ 3건)"
description: "어떤 기준으로 코드리뷰를 진행하는지에 대한 실졔 사례를 통해 배우는 교훈 - 가독성, 네이밍, 성능, 잠재적 버그에 대한 소통"
tags: [Code Review, Kakao, AWS Lambda, 한글코딩, ML, MooC]
---

## 개발 관련

#### [카카오스토리 웹 팀의 코드리뷰 경험](http://www.slideshare.net/OhgyunAhn/ss-61189141){:target="_blank}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="//www.slideshare.net/slideshow/embed_code/key/DGkWpEqIEwNRl" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/OhgyunAhn/ss-61189141" title="카카오스토리 웹팀의 코드리뷰 경험" target="_blank">카카오스토리 웹팀의 코드리뷰 경험</a> </strong> from <strong><a target="_blank" href="//www.slideshare.net/OhgyunAhn">Ohgyun Ahn</a></strong> </div>
</div>
* 108~117 페이지의 실제 code review 샘플이 재미있네요.
* 가독성, 네이밍, 성능, (잠재적) 버그 관련 해서도 적극적으로 **댓글로 리뷰**가 되는게 좋아 보여요
* 저희 파트의 개발 규모상 전원 동의로 merge를 진행해도 될 것 같은데, 그럼 Review를 적극적으로 해야 하는 스트레스가 있을 수 있어 보이는데 어떻게 생각하나요?

#### [AWS Lambda를 이용한 이미지 썸네일 생성 개발 후기](https://medium.com/n42-corp/aws-lambda%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-%EC%9D%B4%EB%AF%B8%EC%A7%80-%EC%8D%B8%EB%84%A4%EC%9D%BC-%EC%83%9D%EC%84%B1-%EA%B0%9C%EB%B0%9C-%ED%9B%84%EA%B8%B0-acc278d49980#.tx9uqx3bn){:target="_blank}
{% include image.html path="post/thumbnail_resize_using_lambda.png" path-detail="post/thumbnail_resize_using_lambda.png" %}
* Redis->토스트 클라우드->AWS Lambda로 최종 결정이 되기까지의 과정이 흥미롭습니다.
    * [토스트 클라우드](http://cloud.toast.com/){:target="_blank"}는 NHN 엔터의 클라우드 시장 진출을 위한 서비스입니다. (AWS에 비교될 수 있죠)
* 토스트 클라우드에 대해서는 처음부터 관심 있게 보고 있었는데, 처음보다 많이 좋아져서 이제는 PaaS 솔루션을 검토할 때 같이 고려를 해도 좋을 것 같네요.

#### [한글코딩.org 개발기 (실패기?)](https://medium.com/happyprogrammer-in-jeju/%ED%95%9C%EA%B8%80%EC%BD%94%EB%94%A9-org-%EA%B0%9C%EB%B0%9C%EA%B8%B0-%EC%8B%A4%ED%8C%A8%EA%B8%B0-f69bd4bc55c6#.he3t8hxev){:target="_blank"}
{% include image.html path="post/hangul_coding_sample.png" path-detail="post/hangul_coding_sample.png" %}
* 읽어보면 재미 있긴 한데, 한글 코딩은 익숙하지 않아서인지 저는 영어보다 가독성이 떨어진다고 생각하는 입장입니다. 

#### [Machine Learning Foundations: A Case Study Approach](https://www.coursera.org/learn/ml-foundations/){:target="_blank"}
{% include image.html path="post/hangul_ml_course_capture.png" path-detail="post/hangul_ml_course_capture.png" %}
* `한글 자막`이 지원되는 ML 과정입니다. 
* 공부해야지 하고 생각만하고, 영어 동영상 보면 잠드는 저같은 분들을 위해서 추천 드립니다. 
