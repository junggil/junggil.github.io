---
layout: post
title: "[NewsLetter] 견고한 서비스를 만들기 위한 팁 (+ 12건)"
description: "서비스 운영 및 인프라 관리에 대한 조언과, 배포 전략"
tags: [조직문화, 인사, 채용, 인프라, 운영, 배포, AWS IoT, Dash, 면접문제, Git, UI 디자인]
---

## 조직문화

#### [SW회사에는 왜 수평적인 조직문화가 필요한가](http://m.zdnet.co.kr/column_view.asp?artice_id=20161026091515#imadnews){:target="_blank"}
{% include image.html path="post/internal_marketing.png" path-detail="post/internal_marketing.png" %}
* `수평적인 조직`에 대한 해석이 핵심이라고 생각합니다.
    * 모든 직원이 평등하다는 의미가 아니라, 직급/나이/경력이 아닌 *전문성을 바탕으로 (자율적으로) 역할*을 할 수 있어야 한다는 뜻
* 아래 글과 같이 생각하면 *수평적인 조직을 이룰 수 있는 사람들만 채용*해야 합니다

#### [그렇다. 인사는 만사다](https://brunch.co.kr/@aaa/6?utm_content=bufferc5035&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/sF48Tr1CO9w?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 글 자체는 정리가 좀 덜 된 편입니다. 
    * 스크롤 훑으면서 읽어도 좋을 것 같네요.
* 하지만 공감 가는 문장이 좀 있네요.
    * *직장인에게 최고의 복지는 팀 동료*
    * 자율적이고 수평적인 문화를 유지하기 위해서는, 그렇게 어울릴 수 있는 사람을 뽑아야 한다. == 인사(채용)이 무엇보다 중요함


## 개발 관련

#### [견고한 서비스를 만들기 위한 팁](http://www.popit.kr/%EA%B2%AC%EA%B3%A0%ED%95%9C-%EC%84%9C%EB%B9%84%EC%8A%A4%EB%A5%BC-%EB%A7%8C%EB%93%A4%EA%B8%B0-%EC%9C%84%ED%95%9C-%ED%8C%81/){:target="_blank"}
{% include image.html path="post/deployment_strategy.png" path-detail="post/deployment_strategy.png" %}
* 서비스 운영 및 인프라 관리에 대한 훌륭한 통찰력이 포함 되어있습니다.
* 특히 배포 시간에 대한 기준이 저희의 상식 (업무시간 이후, 새벽)과는 많이 다르다는 것을 눈 여겨 볼만합니다.
* 내용을 요약하자면 (일부 공감 가지 않거나, 적용이 필요 없을 것 같은 내용은 제외 하였습니다)
    * 하나의 소스 트리로 여러 국가 서비스가 가능해야 함
    * 클라우드 서비스 적극 활용 (PaaS로 생각해도 무방할 것 같습니다)
    * 개발자는 운영 서버, 운영 DB에 접근하지 못함 (보안 측면도 있지만, 시스템의 안정성을 보장할 수 있음)
    * (운영 DB 접근을 못하는 것을 보완하기 위해서) 좋은 모니터링 체계 구축
    * 배포는 `근무 시간` 중에만

#### [AWS IoT 버튼을 이용한 출입문 벨 만들기!](http://woowabros.github.io/study/2016/10/28/woowahan_chime_bell.html){:target="_blank"}
{% include image.html path="post/amazon_dash_door_bell_poc.png" path-detail="post/amazon_dash_door_bell_poc.png" %}
* AWS IoT와 Lambda + LINE Message API를 사용해서 버튼을 누르면 메신저로 “문열어 주세요” 라고 입력이 되도록 만든 사례입니다.
* 이런 프로젝트를 진행을 하고, 사례를 공유하는 사내 분위기가 좋아 보입니다. 
    * 그리고 이런 기술 블로그를 외부에 공유하는 것 자체가 `회사에 대한 마케팅 효과`로 ROI가 무엇보다 크다라고 생각하구요.
    * 개인적으로 LG도 “사랑해요 LG”라는 감성에 호소하는 것 보다, 괜찮은 개발자를 유치하기 위해서는 이러한 기술 공유와 공개가 필요하다고 생각합니다.

#### [신입 사원 웹 개발자 필기 시험 문제](https://github.com/EBvi/dev-matrix/blob/master/dev-test.md){:target="_blank"}
* 최근 회사에 지원하는 SW직군 후보자들에 대한 면접을 보면서, 면접 질문을 어떻게 던져야 하나 고민을 했었는데 훌륭한 참고 사례라고 생각합니다. 
    * 기술적인 질문과 더불어 전반적으로 업무 센스와 영어 독해 능력, Linux 사용 경험 등을 묻는 것이 좋아 보입니다.
    * 예) alz로 압축을 하거나, hwp로 문서를 작성하여 외국에 전송하면 안 되는 이유를 설명하시오.

#### [Enabling required reviews for pull requests](https://help.github.com/articles/enabling-required-reviews-for-pull-requests/){:target="_blank"}
* Github의 기능 업데이트 내용입니다. (역시 Github 짱)
    * protected branch에 merge 되기 전에 반드시 review를 해야만 진행 가능하도록 설정 가능
* 파트 내부적으로도 Code Review를 활성화 하고, 가능한 Process 적으로 강제를 하려고 시도 중인데, Tool 적으로 지원이 되는 것은 무척 환영할 일이라고 봅니다. 

#### [git add -p 와 git commit -v 의 사용](https://blog.outsider.ne.kr/1247){:target="_blank"}
{% include image.html path="post/using_git_add_p.png" path-detail="post/using_git_add_p.png" %}
* 파일 단위가 아니라, 파일 내의 `변경사항 단위`로 Commit을 하면 장점이 많습니다.
    * 누구나 늦지 않았습니다. 
    * 저도 바로 이 글을 보기 전까지 git add –a를 썼던 잘못된 개발자입니다. 
    * 특히나 동일 파일을 여러 명이 서버에서 같이 수정하는 경우에는 더더욱 필수 입니다. 

#### [파이썬 생존 안내서](http://www.slideshare.net/sublee/ss-67589513){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="//www.slideshare.net/slideshow/embed_code/key/4pvoqooy8W7ETz" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/sublee/ss-67589513" title="파이썬 생존 안내서 (자막)" target="_blank">파이썬 생존 안내서 (자막)</a> </strong> von <strong><a target="_blank" href="//www.slideshare.net/sublee">흥섭 이</a></strong> </div>
</div>
* 파이썬에 관심이 있었는데 기회가 없었던 분들은, 꼭 보세요 두 번 보세요.
* 800페이지 가량인데 한페이지 한페이지가 속도감있게 넘어갑니다. 

#### [Obfuscated C Code Competition](http://faehnri.ch//have-fun/){:target="_blank"}
{% include image.html path="post/c_lang_obfuscate.png" path-detail="post/c_lang_obfuscate.png" %}
* C언어 난독화 코드를 이해할 수 있도록 도와주는 글 입니다.
* 가끔 [Code Golf](https://en.wikipedia.org/wiki/Code_golf){:target="_blank"} 등을 보면 이해할 수 없는 코드들을 마주하게 되는데, 해당 코드들을 읽는 방법을 배울 수 있습니다.

#### [모바일 UI 디자인 시 고려해야 할 가이드라인 모음](https://brunch.co.kr/@chulhochoiucj0/8){:target="_blank"}
* 개발자가 봐도 이해가 가능하고 납득할 수 있다는 것 자체가 너무 잘 정리된 글입니다. 
* 주변 UI 개발자들에게 공유해주고 싶은 내용이네요. 

## 기타 읽을 거리

#### [회의 시간에 똑똑해 보이는 법 9가지](https://sangminpark.blog/2016/10/25/%ED%9A%8C%EC%9D%98-%EC%8B%9C%EA%B0%84%EC%97%90-%EB%98%91%EB%98%91%ED%95%B4%EB%B3%B4%EC%9D%B4%EB%8A%94%EB%B2%95-9%EA%B0%80%EC%A7%80/){:target="_blank"}
{% include image.html path="post/discuss_mess_up.png" path-detail="post/discuss_mess_up.png" %}
* 가볍게 읽을 수 있는데, 해당 기법을 모두 몸에 익혔을 때의 효과는 실제로 엄청날 것 같습니다.
* 그런데 문제는 모든 참석자가 이렇다면… 끔직합니다.

#### [취업 면접에서 '질문 있으세요?' 시간에 꼭 물어봐야 할 질문은?](https://www.youtube.com/watch?v=Rcn_vD9RdEw){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/Rcn_vD9RdEw?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 4분짜리 동영상인데 흥미 진진합니다. 
* 특히 아래 질문을 통해서 면접관 우려를 파악해서, 즉시 자신감 있는 대안을 대답할 수 있다면 유용할 것 같네요.  (영상을 보면 어떻게 써먹는지가 나옵니다)

#### [Dynamic projection mapping onto deforming non-rigid surface](https://www.youtube.com/watch?v=-bh1MHuA5jU){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/bh1MHuA5jU?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 초당 1000회로 표면을 감지해서 프로젝션할 내용을 바꾸는 다이내믹 프로젝션 기술 데모 영상
    * 표면을 빠르게 움직이거나 늘여도 내용이 매우 자연스럽게 바뀌는데, 
    * 눈에 보이지 않는 마커가 새겨져 있다고 하네요 (그래도 대단함)

