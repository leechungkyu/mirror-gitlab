---
layout: post
title: Jenkins + git last committer E-mail 값 얻기
tags:
  - jenkins
  - git
  - svn
---

#### 1. 질문 그리고 과거 회상
***
> 사용자 별 svn 커밋 회수, 주/월 별 svn 전체 커밋 수 등 통계성 업무를 꽤 했었던 것 같다.<br>
고심 끝에 shell 파일 짜서 raw data 만들고, 다시 엑셀로 정리하며 뿌듯해 했었다.<br>
'미션' 이라고 하지 않는가. 아래 질문자도 스스로 문제 뒤에 따라오는 성취감을 느끼게 해주고 싶다.

![q1]({{ site.baseurl }}/images/q1.jpg)
질문을 읽고, 막 떠오른 답 2개를 던졌다.
1. 어려운 길 (아직 시도 안 해 봄)
2. 쉬운길 (이 포스팅 주제)

#### 2. '쉽게 가려면'의 족새
***
> 사실 해보지 않은 것에 대해새 쉽고/어렵고를 논하기 어렵다.<br>
무슨 근자감에서 '조금 쉽게 가려면' 이란 코멘트를 남겼을까. 왜 그랬니?<br>

#### 3. 구세주 EnvInject Plugin
***
> Jenkins 코어에서 제공하는 환경변수 중 ${GIT_COMMITER_EMAIL} 동작 안 하드라.

** Jenkins + git last commiter E-mail 값 얻는 방법 **

플러그인 한 개만 추가 설치하고, 별도의 프로그래밍 없이 Jenkins 기본 셋팅으로 아래 스크린샷 2개 따라하면 됨.

1. 플러그인 설치<br>
-EnvInject Plugin

2. Build<br>
-Execute shell<br>
-Inject environment variables

3. 빌드 후 조치<br>
-E-mail Notification

![a1]({{ site.baseurl }}/images/a1.jpg)
![a2]({{ site.baseurl }}/images/a2.jpg)

#### 4. 
***

