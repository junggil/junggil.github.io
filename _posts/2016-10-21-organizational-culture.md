---
layout: post
title: "[NewsLetter] 조직문화 관련 특집 (+ 12건)"
description: "신뢰받는 리더가 되는 방법과, 직원들이 성과창출을 이루고 행복을 느끼게 하는 방법"
tags: [조직문화, 소통, 협력, Consistent Hashing, README Guide, SW Estimation, Kafka]
---

## 조직문화

#### [직원들이 변화를 거부하는 것은 당신의 말과 행동이 싫기 때문이다](http://ppss.kr/archives/91465?utm_content=buffere5a28){:target="_blank"}
> 리더인 당신이 신뢰할 수 있는 좋은 사람이라면, 그런 당신과 조직을 위한 올바른 변화와 혁신을 왜 거부하겠는가? 직원들을 변화로 이끄는 첫 번째 방법은 `신뢰받는 리더가 되는 것과 변화를 위한 환경을 만들어 주는 것`이다.

* 제목이 너무 자극적이지만 내용은 읽어볼만 합니다.
* 글에서 이야기하는 것은 두 가지 입니다.
    * 직원들을 움직이기 위해서는 신뢰받는 리더가 되어야 하고, 변화를 원하면 변화를 위한 환경을 마련해 줄 것
    * 성과창출과 직원행복은 동시적으로 추진 되어야 한다
* 위에 두 가지를 위해서는 `소통과 협력`이 가장 중요

#### [BE KIND](https://www.briangilham.com/blog/2016/10/10/be-kind){:target="_blank"}
* 주말에 회사에서 3시간 거리의 캠핑 장에 도착한 순간, 당신이 어제 고친 코드 때문에 장애가 발생했다는 것을 알게 된다면?
    * `돌발 상황을 대처하는 리더의 대응 방법`도 인상적이지만, (해당 기억을 평생 기억하고 되돌려주는 글쓴이의 모습도)
    * 이렇게 하기 위해서는 업무를 다른 사람이 Backup해줄 수 있도록, `조직 단위에서 2명 이상이 업무를 Cover할 수 있어야` 한다고 생각합니다. 
* 이 글을 읽으면서 또한 느낀 것은, ***장애 혹은 이슈의 원인이 명백한 상황**에서 무한한 포용은 현실적이지 않다고 생각합니다.
    * 그렇기 때문에 `채용이 무엇보다 중요`합니다. 
    * 조직에 Fit에 맞고, 스스로 문제의 원인을 찾아서 발전할 수 있는 직원들로 구성을 할 수 있다면 위에 사례처럼 반복적인 문제상황을 만들지 않더라도 상황이 개선될 수 있다고 생각합니다. 

#### [마윈에게 실명으로 항의하는 알리바바 직원들...중국 IT 기업의 수평적인 기업문화](http://biz.chosun.com/site/data/html_dir/2016/10/18/2016101802445.html){:target="_blank"}
* 소통을 위해서는 자신의 생각과 다른 의견에 대해서 `Top에서부터 받아들일 준비`가 되어있어야 한다고 생각합니다.

#### [개발자 불평 2.5만건 분석해보니](http://www.ciokorea.com/news/31461){:target="_blank"}
{% include image.html path="post/stress_of_developers.png" path-detail="post/stress_of_developers.png" %}
* 해외 사례라 국내 실정과 차이가 있다고 봅니다. 
* 개발자를 필요이상으로 관리/감독하는 것이 주요 불만 사항이고 (PM/상사/HR : 63.5%), 업무 자체에 대한 불만 (오류/버그: 10.5%)은 낮은 편이었습니다. 

#### [소통이 어려운 이유]
{% include image.html path="post/why_communication_is_so_hard.jpg" path-detail="post/why_communication_is_so_hard.jpg" %}
* 말을 많이 할수록 대화가 어렵다는 것을 느낍니다. 
* 느끼는 대화의 난이도는 *얼굴 보고 대화 <<<<<< 전화 << 메일 <<<<<< 메신저*

## 개발 관련

#### [Consistent Hashing 에 대한 기초](http://www.popit.kr/consistent-hashing/){:target="_blank"}
{% include image.html path="post/basic_of_consistent_hashing.png" path-detail="post/basic_of_consistent_hashing.png" %}
* (제가 본 것 중에) Consistent Hashing에 대해서 가장 쉽게 잘 설명된 자료 입니다. 
* 기존의 Hashing 기반의 Route/Load Balance는 서버가 사라지거나, 추가될 때의 re-balance 비용의 부담이 pain point 입니다. 
* 이를 해결하기 위한 방식이 Consistent Hashing입니다.
    * re-balance시에 추가/삭제된 서버 주변의 노드만 영향을 받습니다. (K개의 서버라고 하면 평균 N *1/K 정도)
    * 그런데 피지컬 서버 1개를 가상 서버로 확장해서 가상노드를(vnode) 사용한다면 N * 1/K의 노드에 대해서도 전체 서버로 분산해서 부하를 나눌 수 있습니다.  (자세한 내용은 위에 링크를 읽어보세요)
* 해당 내용에 대해서는 별도 꼭지로 `팀 내부 세미나`를 해도 좋을 것 같네요. 

#### [json-data-generator 소개](http://www.popit.kr/json-data-generator/){:target="_blank"}
* 원글의 제목은 좀 이상하지만 (개발자는 막일 하는 사람이 아닙니다. 막일을 줄이기 위한 유용한 팁 1), 본문은 json-data-generator에 대한 소개 내용 입니다.
* json-data-generator는 JAVA기반 구현체이며 logger/kafka/HTTP Post 등의 전달 방식을 제공합니다.
    * Logger  – logs디렉토리 아래 log file 생성
    * File – 특정 디렉토리에 특정 file 확장자로 생성
    * HTTP POST – 특정 url로 POST방식으로 메시지 전송
    * Kafka – kafka broker로 특정 토픽에 대해서 메시지 전송


#### [README 작성 가이드](https://github.com/noffle/art-of-readme){:target="_blank"}
{% include image.html path="post/readme_job_list.png" path-detail="post/readme_job_list.png" %}
* README가 담고 있어야 하는 주요 내용은 위에 그림과 같습니다.
* 저는 보통 github 프로젝트를 볼 때 1차로 Star의 수를 보고, 2차로 README 파일의 완성도를 보게 됩니다.
* 파트 내부에서 관리되는 git 프로젝트들도 README에 정보가 거의 없는 경우가 많은데, README에 대한 작성을 신경써야 하겠습니다.


## 기타 읽을 거리

#### [Project delays: why good software estimates are impossible](http://chrismm.com/blog/project-delays-why-software-estimates){:target="_blank"}
* 어째서 과거와 비슷한 일을 하는데, 일정 예상이 실패하는 경우가 있는지?
    * 항상 프로젝트는 이전의 프로젝트와 사용하는 라이브러리/프레임워크/외부 API 등의 차이가 발생함
    * 해당 차이에서 예상하지 못한 상황이 발생할 확률이 5%라고 가정
    * 그럼 10개의 프로젝트가 진행되면 40% (1 - (1 - 0.05) ^ 10 = 0.40)의 확률로 일정에 오차가 발생
    * 프로젝트의 규모가 커질수록 오차가 증가함

#### [Google's "Director of Engineering" Hiring Test](http://www.gwan.com/blog/20160405.html){:target="_blank"}
* 구글 전화인터뷰에서 떨어진 것에 대한 회고.
    * 해당 글이 [reddit](https://www.reddit.com/r/programming/comments/57b1ye/googles_director_of_engineering_hiring_test/){:target="_blank"}에서 엄청난 화제가 되면서 blog가 폭파되었습니다. (현재는 복구됨)
    * 복구가 되면서 구글 채용담당자의 반박글이 댓글에 붙어있네요 (이것도 흥미롭습니다)
* 일방적인 글을 봤을 때는 채용담당자가 융통성이 없다고 생각했는데,
* 반박글을 보고 나니 지원자의 커뮤니케이션상의 문제도 있어 보이네요.  (역시 쌍방의 글을 다 봐야)

#### [SQL Server DB 메모리 사용률이 계속 높아요.. 메모리 사용률 98%의 오해](http://yoonsy.tistory.com/m/28){:target="_blank"}
* 한번 할당된 메모리는 사용 후에도 유지됨 (반납하지 않음)
* 사용률이 아니라 유휴 메모리의 절대량을 관리 필요

#### [자유시점 영상 생성 시스템](https://www.youtube.com/watch?v=fIz9hQ7-rUo){:target="_blank"}
<div class="embed-responsive embed-responsive-16by9">
<iframe src="https://www.youtube.com/embed/fIz9hQ7-rUo?modestbranding=1&autohide=1&showinfo=0&controls=0" frameborder="0" allowfullscreen></iframe>
</div>
* 위에 영상 꼭 보세요. 설명이 필요 없습니다. 
    * 카메라 기술이 발달하고 나니 FIFA/위닝 등의 카메라 시점이 현실(?)적이었다고 느껴지네요
* J리그와 캐논 주식회사가 지난 15일 사이타마 스타디움 2002에서 열린 J리그 결승전에 대한 공개된 실험 영상 입니다.

#### [How Kafka’s Storage Internals Work](https://medium.com/the-hoard/how-kafkas-storage-internals-work-3a29b02e026#.kc8va4lqd){:target="_blank"}
* 저도 아직 못 읽어봄 (메모를 위해 포함합니다)
* 혹시 블로그에 내용이 업데이트 되지 않았으면, 읽어보신분은 댓글로 의견 주시면 도움이 될 것 같습니다.

