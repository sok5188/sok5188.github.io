---
layout: page
title: Résumé
subtitle: 노력의 가치를 아는 개발자 신원균 입니다
---

<span style="float: right; "><a href="{{ '/assets/resume.pdf' | prepend: site.baseurl }}"><strong>> Download as PDF</strong></a> </span>
<br>

### SKILLS

<strong>Language</strong><br/>
Java, JavaScript, HTML5, C/C++<br/>
<strong>Back-End</strong><br/>
Spring Boot, Websocket(STOMP), Node.js<br/>
<strong>Front-End</strong><br/>
Flutter,React.js,Vue.js<br/>
<strong>Server</strong><br/>
Nginx<br/>
<strong>DevOps</strong><br/>
AWS(EC2,RDS,S3,CodeDeploy), GithubActions<br/>
<strong>DB</strong><br/>
PostgreSQL, MySQL, MSSQL, H2<br/>
<strong>OS</strong><br/>
MacOS, Linux,Windows<br/>
<strong>Tools</strong><br/>
IntelliJ, Postman, MySQL workbench,VS code, pgAdmin4, Android Studio<br/>
<strong>Collaborations, Document</strong><br/>
Git, Github, Notion, Slack, Google Workspace, MS office<br/><br/><br/>

### PROJECTS

<h3>공강구조대</h3> 팀 프로젝트 (3인) <span style="float: right; "> 2023.03 ~ 2023.06</span>
<br/>
현재 프로젝트의 코드는 <a href="https://github.com/orgs/EmptySaver/repositories">공강구조대</a> 깃허브에서 확인하실 수 있습니다.
<br/>
<b>현재는 비용 문제로 프로젝트의 운영을 지속할 수 없어 스토어 및 서버의 배포를 중단한 상태 입니다</b><br/>
프로젝트 시연 영상은 <a href="https://www.youtube.com/watch?v=LYtQgMJNOks"> 여기</a> 에서 확인하실 수 있고,
<br/>
프로젝트의 PPT는 <a href="https://github.com/EmptySaver/EmptySaverBE/blob/master/%E1%84%80%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A1%E1%86%BC%E1%84%80%E1%85%AE%20%E1%84%8E%E1%85%AC%E1%84%8C%E1%85%A9%E1%86%BC%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD.pptx">여기</a> 에서 다운받으실 수 있습니다.
<br/>
<strong>프로젝트 배경</strong><br/>
이 프로젝트는 졸업 설계 프로젝트이며, 팀원끼리 브레인스토밍을 한 결과, 시간표와 통학이라는 소재를 이용해
우리가 대학생활을 하며 필요했던 부분을 채워보자는 의견으로 좁혀졌습니다. 팀원들 모두 통학을 해본 경험이 있었고 통학하는 과정에서 공강시간이 크게 생기는 경우 다시 집으로 돌아가기에는 시간이 너무 무의미하게 사용되어 집으로 갈 수는 없지만 그렇다고 마땅히 할 일을 생각해내지 못하고 시간을 무의미하게 보낸 경우가 많았습니다. 이런 경험을 토대로, 공강시간에 할 수 있는 다양한 활동을 추천해주고 시간을 효율적으로 관리할 수 있게 하는 프로젝트를 진행해보자는 의견이 나와 진행하게 된 프로젝트 입니다.
<br/><br/>
<strong>담당한 부분</strong> : 프로젝트 기획 및 설계, 프론트 엔드, 백엔드
<br/><br/>
<strong>사용한 기술 스택</strong>
<br/>
교내 OPEN API를 통해 강의 정보를 받아오고, 프론트는 Flutter, 백엔드는 Spring Boot를 사용하였고, DB는 MySql을 사용했습니다. 또한, 서버는 EC2를 통해 배포 하였고, RDS를 사용하여 원격으로 DB를 관리하였습니다. 그리고, github actions와 AWS S3, AWS CodeDeploy를 이용하여 CI/CD를 구현하였습니다.<br/><br/>
<strong>구현한 내용</strong>
<br/>
해당 프로젝트에서 저는 배포와 관련된 부분 (CI,CD설정 및 AWS설정)을 담당하였고, 현재 <b>무중단 배포</b> 중에 있습니다. 또, 프로젝트의 <b>인증</b>을 <span style="font-style: italic ;"> JWT </span>를 이용하여 수행하였고 Filter에서 인증기능을 수행하였습니다. 그리고, 프론트엔드와 원활한 소통을 위해 서버에 <b>스웨거</b>를 적용하였습니다.<br/>
또, 다음의 SMTP서버를 이용하여 <b>이메일 인증 기능</b> 을 구현하였고, 이외의 로그인 및 회원가입등 사용자와 관련된 부분에 대한 기능 개발(엔티티 설계, 서비스 로직 및 API 설계 등)을 담당하였습니다. 그리고,<span style="font-style: italic ;"> Jsoup </span>을 이용하여 학교 비교과 페이지인 Uostory페이지의 정보들을 <b>크롤링</b>하여 DB에 저장하는 기능을 구현하였으며 이를 <b>Spring Scheduler</b>에 등록하여 매일 오전 5시에 수행되게끔 설정하였습니다. 그리고, <span style="font-style: italic ;"> FCM </span>(FireBase Cloud Messaging)을 사용하여 서버에서 Flutter 기기로 알림을 보내는 기능을 구현하였고, Flutter에서 이를 받아 처리하는 부분을 구현하였습니다. 이외에도, 친구관련 기능, 그룹관련 기능, 카테고리 관련 기능, 알림 관련 기능을 담당하여 개발을 하였습니다.<br/>
또한, 플러터를 이용하여 UI 개선작업 및 오류 메세지 핸들링, 화면 재배치등의 작업을 수행하였습니다.
<br/>
<strong> 협업 도구 </strong>
<br/>
팀원과의 소통은 Notion, Swagger, 카카오톡, Discord를 이용하여 필요시마다 적극적으로 소통을 하였습니다.<br/><br/>
<strong> 프로젝트 회고</strong>
,,,
<br/>
<hr/>
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<h3>스포티파이 클론코딩</h3> 팀 프로젝트 5인<span style="float: right; "> 2023.03 ~2023.04 </span>
<br/>
프로젝트에 대한 상세 코드는 <a href="https://github.com/HomebrewComputerClub/Team2_clone_BE">Homebrewtify_BE</a> 깃허브에서 확인 부탁드립니다.
<br/>
<strong>프로젝트 배경</strong><br/>
이 프로젝트는 서울소재 대학생간 진행하는 프로그래밍 동아리인 Homebrew클럽에서 진행한 프로젝트로 약 한달간 스포티파이 웹 페이지를 참고하여 Homebrewtify라는 음악 스트리밍 웹 애플리케이션을 만드는 것이 목적인 프로젝트 입니다. <br/>
해당 프로젝트는 프론트엔드 2명 백엔드 3명으로 이루어져 있고 그 중 저는 백엔드를 담당하고 있습니다.
<br/><br/>
<strong>담당한 부분</strong> : 프로젝트 요구사항 정리 및 ERD설계, 백엔드
<br/><br/>
<strong>사용한 기술 스택</strong>
<br/>
프론트는 React, 백엔드는 Spring Boot를 사용하였고, DB는 MySql을 사용했습니다. 또, Kaggle의 spotify dataset을 기반으로 음원 데이터베이스를 구성하였습니다.
<br/><br/>
<strong>구현한 내용</strong>
<br/>
위 프로젝트에서 저는, <span style="font-style: italic ;">Spring Batch</span>를 이용하여 spotify dataset (11만 4천곡)을 설계한 <b>DB에 맞게 파싱하고 저장</b>하는 작업을 했으며, 이 과정에서 <b>3분 이상</b> 걸리던 배치 작업을 중복 제거, 로직 개선, 자료구조 변경 등을 통해 <b>45초 까지</b> 줄였습니다. 또, 프로젝트에서 발생하는 예외를 잡는 controller advice를 만들어 <b>예외를 핸들링</b> 하였으며, 엔티티간의 지연로딩 및 관계 매핑을 하였습니다. 그리고, 팔로우 기능, 좋아요 기능, 내 라이브러리 기능, 플레이리스트 기능, 최근 재생목록 기능, 로그인 및 회원가입에 필요한 컨트롤러 및 서비스를 구현하였습니다. 프로젝트에 <span style="font-style: italic ;">Spring Security</span>를 적용하였고, 인증 방식은 JWT를 이용하였으며 AccessToken은 인증 헤더에 담아 클라이언트의 로컬 스토리지에 저장하였고 RefreshToken의 경우 httpOnly쿠키로 클라이언트에게 전달 후 DB에 저장하였습니다. <br/>
<strong> 협업 도구 </strong>
<br/>
프론트엔드 팀원들과 소통을 위해 프로젝트에 Swagger를 적용하였고, Slack 및 매주 진행하는 회의를 통해 협업을 하였습니다.<br/>
마찬가지로 백엔드 팀원들과도 Slack 및 매주 회의를 진행하며 협업을 진행하였습니다.
<br/>
<strong> 프로젝트 회고</strong>
,,,
<br/>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3>음악맞추기</h3> 개인 프로젝트 <span style="float: right; "> 2023.01 ~ 2023.02</span>  
<br/>
자세한 프로젝트 내용은 <a href="https://github.com/sok5188/GuessMusic">음악맞추기</a> 깃허브의 GuessMusic 프로젝트 pdf를 참고 해 주시면 감사하겠습니다.
<br/>
<strong>프로젝트 배경</strong><br/>
이 프로젝트를 진행하게 된 계기는, 제가 좋아하는 스타크래프트 유즈맵인 음악 맞추기 맵을 플레이 하다 느낀 불편함 때문이었습니다.
워낙 많이 하다보니, 다양한 맵이 필요했고 원하는 장르 또한 부족하다고 느꼈고 직접 유즈맵을 만들기에는 너무 많은 시간이 필요하다는 것을 알게되었습니다.
때문에, 친구들과 함꼐 맵을 쉽게 만들고 플레이 할 수 있는 웹을 만들고 싶다는 생각이 들어 직접 만들어 보기로 결정했습니다.<br/>
<strong>사용한 기술 스택</strong>
<br/>
위 프로젝트에서 사용한 기술의 경우, 1인 프로젝트다 보니 SSR방식을 택했고 프론트엔드에서는 Thymeleaf, Vue.js, javascript, HTML5을 사용했고, 백엔드의 경우 Spring Boot 3.0.1, Spring Security을 사용하였고, DB는 PostgreSQL을 사용하였습니다. 그리고, 소켓 통신을 통해 사용자 간 채팅을 가능하게 하였습니다. 배포는 EC2를 통해 하였고 RDS를 사용하여 원격으로 DB를 관리하였습니다.
<br/><br/>
<strong>구현한 내용</strong>
<br/>
사용자는 로컬 및 소셜 로그인을 통해 서비스에 들어올 수 있게 하였으며, 중복로그인 및 재로그인 시 세션count를 초기화 하여 항상 정상적으로 동작할 수 있게끔 하였으며
로그인 한 사용자는 만들어진 방에 참가하거나 직접 생성하여 방에 들어갈 수 있게 하였으며, 방에 접속한 경우 방장과 일반 참여자를 구분하여 화면을 다르게 표현하였습니다.
게임이 시작되면 각 사용자 별로 정답 점수를 표시하고 타이머를 이용하여 힌트를 표시하고 웹소캣을 통해 채팅 기능을 적용하여, 사용자간 대화 및 정답 입력이 가능하게 하였습니다.
정답을 맞춘 사용자가 나오게 되면 3초 동안 정답 공지 메세지를 출력하며 그 동안은 정답처리를 하지 않게끔 기능을 구현하였습니다.
로그인 시 관리자 계정으로 로그인 한 경우, 관리자 페이지로 이동이 가능하게 되며, 관리자 페이지에서 게임을 생성,수정,삭제할 수 있게끔 하였습니다.
또한, 페이징 처리를 통해 많은 양의 데이터를 불러오는데에 무리가 없게 하였습니다.
<br/>
<strong> 프로젝트 회고</strong>
,,,
<br/>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3> HomebrewChatting </h3> 팀 프로젝트 6인 <span style="float: right; "> 2023.05 ~ 2023.05</span>
<br/>
현재 프로젝트는 <a href="https://github.com/HomebrewComputerClub/Team2_Chatting_BE">HomebrewChattingBE</a> 에서 확인하실 수 있습니다.
<br/>
<strong>프로젝트 배경</strong><br/>
이 프로젝트는 서울소재 대학생간 진행하는 프로그래밍 스터디 Homebrew클럽에서 진행한 프로젝트로, 채팅기능 및 인증기능을 메인으로 하는 Homebrew동아리 홈페이지를 제작하는 프로젝트 입니다. <br/>
<strong>사용한 기술 스택</strong>
<br/>
React, Spring Boot를 통해 프론트엔드, 백엔드 개발을 진행하였으며 채팅을 위해 Websocket을 사용하였습니다. Github action, S3, CodeDeploy를 활용하여 프론트엔드 및 백엔드 CI/CD를 하였고, AWS certificate을 통해 HTTPS 인증을 진행하였고, 하나의 도메인에 프론트,백엔드 서버 모두를 돌리기 위해 Nginx를 이용하여 리버스 프록시를 적용하였습니다.<br/>
<strong>구현한 내용</strong>
<br/>
프로젝트에서 채팅 기능 및 CI/CD작업, Nginx관련 설정을 담당하였습니다.
프로젝트 초기 원활한 프로젝트 진행을 위해 AWS S3,CodeDeploy,Github Action을 이용하여 CI/CD작업을 우선적으로 수행하였습니다.
그 후, Stomp를 이용하여 프론트와 소켓 통신을 진행하였고, 웹 소캣 업그레이드를 위해 Nginx에 관련 설정을 하였고 이를 통해 클라이언트와 서버가 안전한 wss연결으로 채팅을 진행할 수 있게끔 하였습니다. 또, 채팅에 필요한 채팅 상태, 내용 및 DB 저장등 관련 API 및 로직들을 구현하였습니다. 
<br/>
<strong> 프로젝트 회고</strong>
,,,
<br/>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3>디너서비스 웹</h3> 팀 프로젝트 2인 <span style="float: right; ">2022.11 ~ 2022.11</span>
<br/>
자세한 프로젝트 내용은 <a href="https://github.com/sok5188/Mr_Daebak">미스터대박</a> 깃허브의 프로젝트 pdf를 참고 해 주시면 감사하겠습니다.
<br/>
<strong>프로젝트 배경</strong><br/>  
고객이 원하는 음식을 고객이 원하는 때에 배달하는 서비스를 구축하라는 비즈니스 요구사항을 바탕으로 만들어진 소프트웨어 공학 시간에 진행한 프로젝트 입니다. 
<br/>
<strong>사용한 기술 스택</strong>
React,Node.js를 이용하여 프론트,백엔드 개발을 진행하였습니다. DB는 MySQL을 사용하였습니다.
<br/>
<strong>구현한 내용</strong>
<br/>
주어진 비즈니스 요구 사항을 바탕으로 분석,설계 산출물을 만들고 이를 바탕으로 실제 웹을 구축하였습니다. 해당 서비스는 고객을 위한 주문 인터페이스가 존재하고, 관리자의 조리 및 배달 그리고 재고 관리를 위한 인터페이스가 존재합니다. 재고는 DB를 구축하여 관리하였고 이를 바탕으로 품절 관리를 하였습니다. 해당 프로젝트에서 프론트엔드의 경우 페어 프로그래밍을 통해 개발을 진행하였고, 백엔드는 제가 전적으로 담당하였습니다. 
<br/>
<strong> 프로젝트 회고</strong>
,,,
<br/>

<hr/>

<br/>

### EDUCATION

서울시립대학교 <span style="float: right; ">2018.03 ~ 2024.02</span>  
**컴퓨터과학부**  
2021.3 ~ 2021.6 학업 우수 장학 <br/>
2021.9 ~ 2021.12 교내 교양 수학 튜터 활동<br/>
2022.9 ~ 2022.12 데이터 통신 조교 활동<br/>
<br/>
<strong>수료 강의</strong> <br/>
자바 ORM 표준 JPA 프로그래밍 - 기본편 <span style="float: right; ">인프런, 김영한</span><br/>
실전! 스프링 부트와 JPA 활용2 - API 개발과 성능 최적화 <span style="float: right; ">인프런, 김영한</span><br/>
스프링 MVC 2편 - 백엔드 웹 개발 활용 기술 <span style="float: right; ">인프런, 김영한</span><br/>
스프링 핵심 원리 - 고급편 <span style="float: right; ">인프런, 김영한</span><br/>
스프링 부트 - 핵심 원리와 활용 <span style="float: right; ">인프런, 김영한</span><br/>

### LANGUAGE

TOEIC <span style="float: right; ">2022.07.24</span>  
**845**

<!-- ### EXPERIENCE

Title - **Comapany** <span style="float: right; ">Duration</span>
_Description Phasellus a tellus volutpat, ornare sapien et, lacinia erat. Suspendisse congue, enim vitae mattis pulvinar, eros lacus porttitor neque, eu sodales nibh metus nec arcu. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae;_
Technologies used

Title - **Comapany** <span style="float: right; ">Duration</span>
_Description Phasellus a tellus volutpat, ornare sapien et, lacinia erat. Suspendisse congue, enim vitae mattis pulvinar, eros lacus porttitor neque, eu sodales nibh metus nec arcu. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae;_
Technologies used

Title - **Comapany** <span style="float: right; ">Duration</span>
_Description Phasellus a tellus volutpat, ornare sapien et, lacinia erat. Suspendisse congue, enim vitae mattis pulvinar, eros lacus porttitor neque, eu sodales nibh metus nec arcu. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae;_
Technologies used -->

<!-- ### RECOGNITION & INTERESTS

- Etiam luctus ante quis est dictum faucibus.
- Etiam luctus ante quis est dictum faucibus.
- Etiam luctus ante quis est dictum faucibus.
- Etiam luctus ante quis est dictum faucibus.
- Etiam luctus ante quis est dictum faucibus.
- Etiam luctus ante quis est dictum faucibus. -->
