---
layout: page
title: Résumé
subtitle: 노력의 가치를 아는 개발자 신원균 입니다
---

<span style="float: right; "><a href="{{ '/assets/resume.pdf' | prepend: site.baseurl }}"><strong>> Download as PDF</strong></a> </span>
<br>

### SKILLS

<strong>Back-End</strong><br/>
Java, Spring Boot, Websocket, Node.js<br/>
<strong>Front-End</strong><br/>
Flutter,React.js,Vue.js, HTML5, Javascript<br/>
<strong>Server</strong><br/>
Tomcat, Nginx<br/>
<strong>DevOps</strong><br/>
AWS(EC2,RDS,S3,CodeDeploy)<br/>
<strong>DB</strong><br/>
PostgreSQL, MySQL, MSSQL, H2<br/>
<strong>OS</strong><br/>
MacOS, Linux,Windows<br/>
<strong>Tools</strong><br/>
IntelliJ, Postman, MySQL workbench,VS code, pgAdmin4, Android Studio<br/>
<strong>Collaborations, Document</strong><br/>
Git, Github, Notion, Slack, Google Workspace, MS office<br/><br/><br/>

### PROJECTS

**디너서비스 웹** - 팀 프로젝트 2인 <span style="float: right; ">2022.11 ~ 2022.11</span>  
고객이 원하는 음식을 고객이 원하는 때에 배달하는 서비스를 구축하라는 비즈니스 요구사항을 바탕으로 만들어진 프로젝트 입니다. 주어진 비즈니스 요구 사항을 바탕으로 분석,설계 산출물을 만들고 이를 바탕으로 실제 웹을 구축하였습니다. 해당 서비스는 고객을 위한 주문 인터페이스가 존재하고, 관리자의 조리 및 배달 그리고 재고 관리를 위한 인터페이스가 존재합니다. 재고는 DB를 구축하여 관리하였고 이를 바탕으로 품절 관리를 하였습니다. 해당 프로젝트에서 프론트엔드의 경우 페어 프로그래밍을 통해 만들었으며, 백엔드와 DB구축 및 관리는 제가 전부 구현하였습니다. 사용한 기술의 경우 프론트 엔드는 React, 백엔드는 Node.js를 사용하였고 DB는 MySQL을 사용하였습니다.
<br/><br/>
자세한 프로젝트 내용은 <a href="https://github.com/sok5188/Mr_Daebak">미스터대박</a> 깃허브의 프로젝트 pdf를 참고 해 주시면 감사하겠습니다.

<br/><br/>

**음악맞추기** - 개인 프로젝트 <span style="float: right; "> 2023.01 ~ 2023.02</span>  
이 프로젝트를 진행하게 된 계기는, 제가 좋아하는 스타크래프트 유즈맵인 음악 맞추기 맵을 플레이 하다 느낀 불편함 때문이었습니다.
워낙 많이 하다보니, 다양한 맵이 필요했고 원하는 장르 또한 부족하다고 느꼈고 직접 유즈맵을 만들기에는 너무 많은 시간이 필요하다는 것을 알게되었습니다.
때문에, 친구들과 함꼐 맵을 쉽게 만들고 플레이 할 수 있는 웹을 만들고 싶다는 생각이 들어 직접 만들어 보기로 결정했습니다.<br/>
위 프로젝트에서 사용한 기술의 경우, 1인 프로젝트다 보니 SSR방식을 택했고 프론트엔드에서는 Thymeleaf, Vue.js, javascript, HTML5을 사용했고, 백엔드의 경우 Spring Boot 3.0.1, Spring Security을 사용하였고, DB는 PostgreSQL을 사용하였습니다. 그리고, 소켓 통신을 통해 사용자 간 채팅을 가능하게 하였습니다. 배포는 EC2를 통해 하였고 RDS를 사용하여 원격으로 DB를 관리하였습니다.<br/><br/>
자세한 프로젝트 내용은 <a href="https://github.com/sok5188/GuessMusic">음악맞추기</a> 깃허브의 GuessMusic 프로젝트 pdf를 참고 해 주시면 감사하겠습니다.
<br/><br/><br/>

**스포티파이 클론코딩** - 팀 프로젝트 5인<span style="float: right; "> 2023.03 ~2023.04 </span>  
이 프로젝트는 서울소재 대학생간 진행하는 프로그래밍 스터디인 Homebrew클럽에서 진행하는 사전준비 프로젝트로 약 한달간 스포티파이 웹 페이지를 참고하여 Homebrewtify라는 웹 애플리케이션을 만드는 것이 목적인 프로젝트 입니다. <br/>
해당 프로젝트는 프론트엔드 2명 백엔드 3명으로 이루어져 있고 그 중 저는 백엔드를 담당하고 있습니다.
<br/><br/>
위 프로젝트에서 저는, Spring Batch를 이용하여 spotify dataset (11만 4천곡)을 설계한 DB에 맞게 파싱하고 저장하는 작업을 했으며, 이 과정에서 3분 이상 걸리던 배치 작업을 중복 제거, 로직 개선, 자료구조 변경 등을 통해 45초 까지 줄였습니다. 또, 프로젝트에서 발생하는 예외를 잡는 controller advice를 만들어 예외를 핸들링 하였으며, 엔티티간의 지연로딩 및 관계 매핑을 하였습니다. 그리고, 팔로우 기능, 좋아요 기능, 내 라이브러리 기능, 플레이리스트 기능, 최근 재생목록 기능, 로그인 및 회원가입에 필요한 컨트롤러 및 서비스를 구현하였습니다. 프로젝트에 Spring Security를 적용하였고, 인증 방식은 JWT를 이용하였으며 AccessToken은 인증 헤더에 담아 클라이언트의 로컬 스토리지에 저장하였고 RefreshToken의 경우 httpOnly쿠키로 클라이언트에게 전달 후 DB에 저장하였습니다. <br/><br/>
프론트엔드 팀원들과 소통을 위해 프로젝트에 Swagger를 적용하였고, Slack 및 매주 진행하는 회의를 통해 협업을 하였습니다.<br/>
마찬가지로 백엔드 팀원들과도 Slack 및 매주 회의를 진행하며 협업을 진행하였습니다.
<br/><br/>
프로젝트에 대한 상세 코드는 <a href="https://github.com/HomebrewComputerClub/Team2_clone_BE">Homebrewtify_BE</a> 깃허브에서 확인 부탁드립니다.
<br/><br/><br/>

**공강구조대** - 팀 프로젝트 3인 <span style="float: right; "> 2023.03 ~ 2023.05(예정)</span>  
이 프로젝트는 졸업 설계 프로젝트이며, 팀원끼리 브레인스토밍을 한 결과, 시간표와 통학이라는 소재를 이용해
우리가 대학생활을 하며 필요했던 부분을 채워보자는 의견으로 좁혀졌습니다. 팀원들 모두 통학을 해본 경험이 있었고 통학하는 과정에서 공강시간이 크게 생기는 경우 다시 집으로 돌아가기에는 시간이 너무 무의미하게 사용되어 집으로 갈 수는 없지만 그렇다고 마땅히 할 일을 생각해내지 못하고 시간을 무의미하게 보낸 경우가 많았습니다. 이런 경험을 토대로, 공강시간에 할 수 있는 다양한 활동을 추천해주고 시간을 효율적으로 관리할 수 있게 하는 프로젝트를 진행해보자는 결론이 나왔고, 현재 프로젝트를 진행중에 있습니다.
<br/>
이 프로젝트에서 저는, 다른 팀원 한명과 함께 백엔드를 담당하였습니다.
<br/> 위 프로젝트에서 사용한 기술의 경우, 교내 OPEN API를 통해 강의 정보를 받아오고, 프론트는 Flutter, 백엔드는 Spring Boot를 사용하였고, DB는 MySql을 사용했습니다. 또한, 서버는 EC2를 통해 배포 하였고, RDS를 사용하여 원격으로 DB를 관리하였습니다. 그리고, github actions와 AWS S3, AWS CodeDeploy를 이용하여 CI/CD를 구현하였습니다.<br/><br/>
해당 프로젝트에서 저는 배포와 관련된 부분 (CI,CD설정 및 AWS설정)을 담당하였고, 현재 무중단 배포 중에 있습니다. 또, 프로젝트의 인증을 JWT를 이용하여 수행하였고 Filter에서 인증기능을 수행하였습니다. 그리고, 프론트엔드와 원활한 소통을 위해 서버에 스웨거를 적용하였습니다.
또, 다음의 SMTP서버를 이용하여 이메일 인증 기능을 구현하였고, 이외의 로그인 및 회원가입등 사용자와 관련된 부분에 대한 기능 개발(엔티티 설계, 서비스 로직 및 API 설계 등)을 담당하였습니다. 그리고,Jsoup을 이용하여 학교 비교과 페이지인 Uostory페이지의 정보들을 크롤링하여 DB에 저장하는 기능을 구현하였으며 이를 Spring Scheduler에 등록하여 매일 오전 5시에 수행되게끔 설정하였습니다. 그리고, FCM(FireBase Cloud Messaging)을 사용하여 서버에서 Flutter 기기로 알림을 보내는 기능을 구현하였고, Flutter에서 이를 받아 처리하는 부분을 구현하였습니다. 이외에도, 친구관련 기능, 그룹관련 기능, 카테고리 관련 기능, 알림 관련 기능을 담당하여 개발을 하였습니다.
<br/>
팀원과의 소통은 Notion, Swagger, 카카오톡, Discord를 이용하여 필요시마다 적극적으로 소통을 하였습니다.<br/>
현재, 백엔드개발은 95%이상 완료되었지만, 프론트엔드 개발이 부족하여 Flutter를 사용하여 구현이 덜 된 부분 및 미흡한 부분을 맡아 개발하고 있습니다.
<br/><br/>
현재 백엔드 프로젝트는 <a href="https://github.com/orgs/EmptySaver/repositories">공강구조대</a> 깃허브에서 진행중 입니다.
<br/><br/><br/>

**HomebrewChatting** - 팀 프로젝트 6인 <span style="float: right; "> 2023.05 ~ </span>
이 프로젝트는 서울소재 대학생간 진행하는 프로그래밍 스터디 Homebrew클럽에서 진행하는 프로젝트로, 채팅기능 및 인증기능을 메인으로 하는 Homebrew동아리 홈페이지를 제작하는 프로젝트 입니다. <br/>
해당 프로젝트는 프론트엔드 2명 백엔드 4명으로 진행하며 그 중 저는 백엔드를 담당하고 있습니다 <br/><br/>
프로젝트에서 담당할 분야인 채팅의 경우 1:1 채팅,1:N 채팅, 익명채팅 등의 채팅 기능을 생각하고 있으며 읽지 않은 알림 갯수 표시, 이전 대화기록 불러오기 등 여러 기능을 추가해볼 생각입니다. <br/>
위 프로젝트에서 저는, Github action, S3, CodeDeploy를 활용하여 프론트엔드 및 백엔드 CI/CD작업을 진행하였으며, 서버의 보안을 위해 Https를 적용하였습니다.<br/>
이후, 웹소캣을 이용하여 (sockJS) 소캣통신을 구현할 예정입니다.<br/>
현재 백엔드 프로젝트는 <a href="https://github.com/HomebrewComputerClub/Team2_Chatting_BE">HomebrewChattingBE</a> 깃허브에서 진행중 입니다.
<br/><br/><br/>

### EDUCATION

서울시립대학교 <span style="float: right; ">2018.03 ~ 2024.02</span>  
**컴퓨터과학부**  
2021.3 ~ 2021.6 학업 우수 장학 <br/>
2021.9 ~ 2021.12 교내 교양 수학 튜터 활동<br/>
2022.9 ~ 2022.12 데이터 통신 조교 활동<br/>

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
