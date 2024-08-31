---
layout: page
title: Résumé
subtitle: 스펀지 같은 개발자 신원균 입니다.
---

<span style="float: right; "><a href="{{ '/assets/resume.pdf' | prepend: site.baseurl }}"><strong>> Download as PDF</strong></a> </span>
<br>

## SKILLS

### <strong> Strong </strong><br/>
Java, Spring Framework, JPA, RDBMS
dart, JavaScript, HTML5, C#, C/C++<br/>
<br/>
### <strong> Knowledgeable </strong><br/>
MQ (Kafka, RabbitMQ) <br/>
Monitoring (Prometheus, Grafana, pinpoint, nGrinder, Datadog) <br/>
Frontend (Flutter,React.js,Vue.js) <br/>
OS (Linux, MacOS, Windows)
DevOps (docker, nginx, GithubActions, ArgoCD)
<br/>

---

## Work

어떤 상황들에서, 어떤 방식을 시도해서, 어떤 결과를 만들어냈다.
<h3> 삼성전자 </h4>
<span style="color:gray"> Tizen Application Developer </span> <span style="float: right; color:gray"> 2024.01 ~ 현재 </span>
<br/><br/>
<strong> Role </strong> <br/>
제품에 들어가는 LCD 애플리케이션 개발 담당
<br/><br/>
<strong> What I did </strong> <br/>
- 로그 분석을 통한 신규 팝업 생성
<br/>&emsp;
  <strong>Situation</strong> : x시점에서 단 한번만 발생하는 팝업을 생성해야 하는 상황, 과거 동일 요구사항이 있었지만 x시점에 단 한번만 실행되는 팝업을 만들 지 못함
<br/>&emsp;
  <strong>Solve</strong> : x시점에 특정 파일이 생성되어 flag 역할을 한다는 정보를 바탕으로 해당 파일을 생성하는 패킷이 어디에서든 존재할 것이라 추정하였고, 해당 파일을 찾기 위해 디버거를 통해 로그를 뒤졌고 x파일을 생성한 후 완료를 알리는 패킷이 전송된다는 사실을 확인 후 해당 패킷을 팝업의  flag로 사용
<br/>&emsp;
  <strong>Result</strong> : 기획서 및 사양서 수정 없이 개발 정상 진행
<br/><br/>
- 선행 개발 상품 LCD 개발 대응
    - 신규 기능 개발을 위해 마이컴 개발자 및 기획, 공용부 개발자와 협업
    - 일정 준수를 위해 해외 개발자들과 협업 및 개발 가이드 작성
<br/>&emsp;
    
- 해외 개발자들과 협업
    - 해외 개발자의 업무 투입을 위한 여러 영문 가이드 작성
    - 실시간으로 소통하며 협업 진행


<h3> AITStory </h3>
<span style="color:gray">Backend Developer </span> <span style="float: right; color:gray"> 2023.09 ~ 2023.12 (4개월)</span>
<br/><br/>
<strong> Role </strong> <br/>
T map의 전기차 충전 플랫폼 백엔드 개발 담당
<br/><br/>
<strong> What I did </strong> <br/>

- 기존 결제 대기 상태로 종료된 충전으로인해 발생하는 문제점 해결

  <strong>Situation</strong> : 충전 종료 요청이후 결제가 진행되다 결제 대기 상태에서 충전이 정상적으로 종료된 후 결제가 멈추는 현상 발생
<br/>&emsp;

  <strong>Solve</strong> : 결제 대기 상태로 바뀐 시점 ~ 이후 상태값이 바뀌는 시점 사이에서 발생할 수 있는 모든 종류의 오류를 순서대로 발생시키는 테스트 시나리오 작성, 그 후 실제 환경에서 발생할 수 있는 원인을 분석. 
<br/>&emsp;&emsp;&emsp; 한 유저가 동시에 2건의 충전을 종료시키는 경우 결제 플랫폼에서 오류가 발생하게 되지만 해당 결제의 결과는 메세징 큐를 통해 비동기로 전송되고 해당 큐의 리스너에서 결제의 결과를 저장
<br/>&emsp;&emsp;&emsp; 따라서 결제 요청의 실패를 충전건에 반영하지 못하고 있었고, 충전 종료 요청에 대한 오류 또한 통합하여 제공하였기에 오류의 원인도 트래킹이 되지 않음
<br/>&emsp;&emsp;&emsp; 해당 요청에 대해서 동시성이 문제였기에 Retry 옵션을 추가하였고, 동시 재요청을 방지하기 위해 jitter를 추가
<br/>&emsp;

    <strong>Result</strong> : retry 추가 및 오류 상세화 이후 해당 현상이 발생하지 않게 됨.
<br/>&emsp;&emsp;&emsp; 또한, 정산 불일치의 주된 원인이 해당 현상이였기에, 수작업으로 결제 취소 후 재결제 하던 정산 과정을 90% 가량 감소시킴.
<br/><br/>


- 특정 api에서 발생하던 응답 지연 현상 해결

  <strong>Situation</strong> : X에 관한 정보를 사용하는 api의 응답속도가 다른 api들에 비해 눈에 띄게 느림
  <br/>&emsp;

  <strong>Solve</strong> : 해당 api의 응답속도가 느려진 시점을 모니터링 도구를 통해 파악하고 해당 시점의 코드와 현재 코드를 비교
  <br/>&emsp;&emsp;&emsp; 기존 db에서 조회하던 X를 타 서비스에서 제공받은 것으로 대체했다는 변경점 확인
  <br/>&emsp;&emsp;&emsp; 이 과정에서 필터에 걸러지는 데이터 또한 우선적으로 X에 관한 정보를 가지고 있는 방식이라는 것을 확인했고, 해당 데이터들이 필터링이 끝난 후 X에 대한 정보를 포함하게끔 변경
  <br/>&emsp;

  <strong>Result</strong> : api의 응답속도가 P50(중간값)기준  461ms -> 59.5ms 로 약 675%의 성능 향상
  <br/><br/>

- 쿠폰 코드 추가 프로세스 단축
  <br/>&emsp;

  <strong>Situation</strong> : 신규 쿠폰 코드 추가 시 쿠폰 유효성 검증 및 db에 추가하는 과정에 드는 시간이 많이 소요 됨
  <br/>&emsp;

  <strong>Solve</strong> : 수식에 맞게 쿠폰 코드를 만들어내는 기능과 admin api를 통해 관리자가 api 호출로 간단하게 원하는 수 만큼의 쿠폰을 추가한다면 기존의 방식에 비해 소요 시간을 많이 단축 시킬 수 있다고 생각
  <br/>&emsp;&emsp;&emsp; 쿠폰의 유효성을 검증하는 방식으로 
    1. DB의 쿠폰 코드들을 페이징을 통해 조회하여 만들어진 쿠폰 코드들 중 중복된 값을 제거한 후 다시 추가하는 방식
    2. 기존에 사용했던 쿠폰 코드들이 담겨있는 엑셀 파일을 통해 쿠폰 코드의 유효성을 체크하는 방식
    3. DB의 유니크 키 예외를 통해 중복을 걸러 유효성을 체크하는 방식
  <br/>&emsp; 위 3가지 방식을 떠올렸고 각 방식을 비교해본 결과 1000개의 신규 쿠폰 추가 기준으로 1의 방식은 평균 2분 10초, 2의 방식은 평균 1분 50초, 3의 방식은 1분 53초의 시간이 소요됨
<br/>&emsp;
    2의 방식이 제일 빠르지만 파일에 쿠폰 코드를 지속적으로 추가해야 하고, PRD환경에 이러한 파일을 올려야 하기에 유지 보수성이 매우 떨어진다고 생각하였고 1,3의 방법의 경우에도 2분에 가까운 시간은 효율적이진 않다고 생각.
<br/><br/>
  저장에 걸리는 시간이 주요한 원인이였기에 이를 줄이기 위해 저장 과정 자체를 병렬로 쓰레드를 펼쳐서 하는 방법 고안
<br/>  실제 테스트 결과, 1의 경우 11초 3의 경우 10초로 저장 속도가 대폭 줄어들게 됨 

    <strong>Result</strong> : 수작업 시 1000개의 쿠폰을 삽입하는데 걸리는 시간을 자동화하여 약 10분에서 -> 2분으로 줄임
<br/>&emsp;&emsp;&emsp; 또한, 병렬 저장을 통해 이를 추가적으로 개선시켜 2분 -> 10초로 단축시킬 수 있었음
<br/><br/>

- 사후 재결제 기능 개발

  <strong>Situation</strong> : 정산 시 발생하던 금액 차이로 인해 수동으로 실제 충전 사용량을 바탕으로 다시 결재를 하는 상황에서 이를 자동화하는 신규 프로세스 구축
    <br/> 충분한 검증 필요, 쿠폰 및 사용자의 충전 이용등 전반적인 서비스 사용에 영향을 주지 않아야 함
  <br/>&emsp;

  <strong>Solve</strong> : 결제 내역을 바탕으로 해당 건에 사용된 쿠폰을 찾아 복구 시킨 뒤 재결제 사용건에 강제로 연결시켜 쿠폰이 자동으로 사용되게끔 구현
    <br/>&emsp;&emsp;&emsp; 재결하는 동안 생기는 이용건을 활성화 세션의 숫자에 포함되지 않게 하기 위하여 재결제가 성공할때까지 delete 상태로 유지하고, 재결제 완료 이후 해당 내용을 모두 activate 시켜 실제 충전 세션에 영향을 주지 않게 구현
  <br/>&emsp;&emsp;&emsp; 한 유저가 동시에 2건의 충전을 종료시키는 경우 결제 플랫폼에서 오류가 발생하게 되지만 해당 결제의 결과는 메세징 큐를 통해 비동기로 전송되고 해당 큐의 리스너에서 결제의 결과를 저장
  <br/>&emsp;&emsp;&emsp; 가능한 모든 상황을 나누고, 재결제 로직에서 발생가능한 모든 오류를 정리하여 이를 테스트 케이스화 하고 메인 서버와 배치서버 모두에서 모든 시나리오에 대해 자동화 검증 수행
  <br/>&emsp;

  <strong>Result</strong> : 건당 1분 이상 걸리던 작업을 자동화 하여 불필요한 반복작업을 없앨 수 있게 되었고, 이를 통해 보다 강건한 서비스를 운영할 수 있게 됨
  <br/><br/>


### PROJECTS

<br/>

<h3>Gyunpang</h3> 개인 프로젝트 <span style="float: right; "> 2024.03 ~ </span>
<br/><br/>
<strong>프로젝트 구조</strong><br/>
<img src="/assets/img/Gyunpang_Architect.jpg" alt="프로젝트구조">
<strong>프로젝트 배경</strong><br/>
실제 서비스 도중 발생할 수 있는 여러 상황들을 만들어보고 이 상황 속에서도 강건하게 유지되는 시스템을 구축해보고자 시작한 프로젝트입니다.<br/>
인터넷 쇼핑이라는 도메인을 이용하여 선착순 쿠폰, 재고 처리 등 다량의 사용자가 접근하는 상황에서 발생하는 동시성 문제와 특가 이벤트와 같이 일시적으로 급격하게 증가하는 트래픽에 대처하는 방법을 익혀보는 것이 목적인 프로젝트입니다<br/>
<br/>

<strong>사용한 기술 스택</strong>
<br/><br/>
BE : Spring (MVC, WebFlux, JPA, Security, Cloud, Kafka) <br/>
Devops : nginx, docker <br/>
MQ : Kafka(Kraft) <br/>
Cloud : aws ec2, oracle cloud, google cloud platfrom <br/>
Cache : (Redis) <br/>
Monitoring : (Pinpoint) <br/>
<br/><br/>

<strong>구현한 내용</strong>
<br/>
추후 기능별 정리 후 업데이트 예정입니다. <a href="https://sirong-blog.tistory.com/category/Gyunpang"> 개인 블로그</a> 에서 현재 진행 상황을 확인하실 수 있습니다.
<br/>

<!-- <strong> 프로젝트 회고</strong> -->

<hr/>
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

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
프로젝트 구현에 주어진 시간 자체가 짧았고, 인원 또한 3명이였으며 심지어 프론트엔드가 1명인데 Flutter를 처음 사용해본 상태라 개발을 빠르게 해내지 못하였습니다.
프로젝트 자체가 활동하는 유저의 수가 어느정도 존재해야 신규 유입 사용자가 서비스를 100%활용할 수 있다는 한계점을 가지고 있는 프로젝트였다고 생각합니다.
이에 대한 대책으로 프로젝트에서 제공하는 빈 시간 찾기, 그룹 공지사항, 게시판,댓글 등을 통해 이미 존재하는 그룹인 동아리를 우선적으로 유저로 끌어드리려 하였습니다. 하지만, 개발 자체의 시간이 꽤 소요되었고 플레이스토어에는 업로드가 되어 있었으나, 앱스토어의 경우 개발자 등록비용이 10만원이고 해당 비용을 캡스톤 지원금으로 지불할 수 없다고 하여, 교내 중앙 동아리에 협조를 구하기 힘들었습니다. 때문에, 안드로이드 사용자를 대상으로만 테스트를 진행할 수 있었고 동아리 내에서 모든 동아리원이 저희 어플을 사용할 수 없었기에 유저수 유치에 실패하게 되었습니다.<br/>
또한, 개발 일정에 쫒겨 개발을 하다보니 테스트 코드를 제대로 작성하지 못한 상태로 Postman을 이용해 자체적으로 테스트만 진행하였습니다. 또, 트래픽 테스트 및 성능 모니터링도 다른 툴을 사용한 것이 아닌, 직접 ec2인스턴스에 들어가 로그를 보는 형식으로 진행하였습니다.<br/>
<br/>
그래서, 우선 Spring Actuator와 프로메테우스, 그라파나를 이용하여 모니터링 시스템을 구축하고, 핀포인트도 도입하여 서버의 성능을 실시간으로 모니터링할 환경을 구성하였습니다.
그 후, 부하 테스트를 수행하고 병목 지점을 찾아 성능 개선 작업을 수행하였고 동시성 문제를 고려하여 코드를 수정하였습니다.(V2)<br/>
자세한 내용은 <a href="https://sirong-blog.tistory.com/entry/%EB%B6%80%ED%95%98-%ED%85%8C%EC%8A%A4%ED%8A%B8-%ED%95%98%EA%B8%B0-1">블로그</a> 및 <a href="https://github.com/sok5188/EmptySaverBEV2">깃허브</a>를 참고 해주시면 감사하겠습니다.

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
데이터 셋 자체가 11만개 정도 되어 서버가 응답을 보내는데에 시간이 오래 소요될 것이라 예상했으나, 적당한 쿼리 수정 및 페이징 처리로도 충분히 빠른 응답을 내보낼 수 있었습니다.
JWT를 처음으로 공부하고 도입했던 프로젝트로, 스프링 동작 과정에 대해 좀 더 깊이 공부할 수 있게된 계기가 되었고 인증,인가 방식 공부에도 큰 도움이 된 프로젝트 였습니다.
다만, 프론트엔드에서 처리할 부분이 한달안에 하기에는 다소 많아 기간내에 완성을 하진 못하였습니다. 서버에서 스포티파이 open api를 통해 노래를 받아오고 프론트로 보내는 방식도 생각해보았으나, 보안적 이슈도 있었고 그렇게 되면 통신 비용이 너무 증가하게 될 것이라 판단하여 이 방식은 선택하지 않았습니다. 결국, 백엔드에서 구현한 내용은 모두 반영되었으나, 노래 자체를 API로 받아오는 부분 및 기타 프론트엔드 작동 오류 부분을 수정하지 못한 채 프로젝트를 마무리하게 되었습니다.<br/>
비록, 전체적으로 완성된 프로젝트는 아니였지만 Spring Batch, JWT등의 기술을 습득하게 되었고, 자료구조의 소중함을 다시금 깨닫게 해 준 프로젝트였습니다.
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
첫 개인프로젝트이자 아직 유일한 개인 프로젝트 입니다. 평소 친구들과 자주 했던 스타크래프트 유즈맵에서 시작한 프로젝트인지라 해당 유즈맵과 유사한점이 많다고 생각합니다. 다만, 스프링을 처음으로 학습한 상태로, 그것도 짧은 강의만 듣고 무작정 구글링을 해가며 진행했던 프로젝트 였습니다. 요청마다 응답의 속도가 조금씩 차이가나서 많은 곡을 재생하는 경우 어떤 브라우저에선 소리가 조금 밀리는 현상이 발견되었고 당시 여러 방법을 시도했으나 결국 고치지 못한 상태로 마무리 한 프로젝트 였습니다. 해당 프로젝트를 통해, 스프링을 통한 백엔드 설계, Thymeleaf 및 Vue.js를 이용하여 프론트엔드 설계를 경험해볼 수 있었고, OAuth및 SpringSecurity에 대해 처음 공부해볼 수 있었습니다. 특히, Spring Security의 경우 세션 로그인 방식에서 어떻게 이 로그인 정보를 유지할 수 있는 지에 대해 공부해볼 수 있는 기회가 되어 좋았습니다.
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
프로젝트 팀원 모두 과제 및 시험 때문에 활동을 많이 하지 못하여, 완성도면에서 많이 떨어지는 프로젝트라고 생각합니다. 프론트엔드를 담당한 팀원분을 포함해 일부 인원끼리 모여 급하게 백엔드 전반을 뒤집고 프로젝트를 진행하였고 그 결과, 기존 목표였던 소셜 로그인(JWT) 및 그룹 채팅 기능 완성에 실패하게 되었고, 로컬 로그인 및 1대1채팅 기능만 급하게 만든 상태로 프로젝트를 마무리하게 되었습니다.<br/>
채팅의 경우 1:1 채팅 및 그룹 채팅에 필요한 기능 및 API 구현은 모두 끝낸 상태로 프로젝트가 종료하였지만 바라던 만큼의 완성도에 도달하지 못했다는 아쉬움이 많이 남았지만 처음의 목표 수립과정에서 현실적인 수준의 목표를 설정하는 것 또한 중요한 일이라는 생각을 가질 수 있게 되었다고 생각합니다.
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
학교 수업에서 제시한 비즈니스 요구사항에 맞춘 프로젝트로 해당 프로젝트로 백엔드 개발에 조금 흥미를 가지게 되었고, 현재의 제가 될 수 있었다고 생각합니다.<br/>
지금 보면 너무나 단순한 기능만을 구현한 프로젝트이지만 그 당시엔 모든게 너무 새로웠고 HTTP가 뭔지도 CSR,SSR이 뭔지도 잘 몰랐던 터라 개발에 많은 어려움이 있었고, 같이 진행한 동기와 거의 매일 밤까지 코딩 공부를 했던 기억이 납니다. 하지만 이런 과정이 전혀 싫지 않았고 오히려 재미를 크게 느꼈던 기억으로 남아 있고 덕분에 더욱 개발에 흥미를 가지고 공부를 할 수 있게된 계기가 되었다고 생각합니다.
<br/>

<hr/>


## EDUCATION

#### 서울시립대학교 
<span style="color:ashy"> 컴퓨터과학부 </span> <span style="float: right; ">2018.03 ~ 2024.02</span> <br/>  

2022.9 ~ 2022.12 데이터 통신 조교 활동<br/>
2021.9 ~ 2021.12 교내 교양 수학 튜터 활동<br/>
2021.3 ~ 2021.6 학업 우수 장학 <br/>
<br/>

#### 삼성전자 dx 하계 S/W 알고리즘 특강
우수 수료자 선정, pro 등급 취득 <span style="float: right; ">2023.07 ~ 2023.08</span>

## LANGUAGE

TOEIC Speaking<span style="float: right; ">2023.09.16</span>  
**150 (IH)**

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
