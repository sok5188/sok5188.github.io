---
layout: page
title: Résumé
subtitle: 스펀지 같은 개발자 신원균 입니다.
---

## SKILLS

### <strong> Strong </strong><br/>
Java, Spring Framework, JPA, RDBMS
<br/>
### <strong> Knowledgeable </strong><br/>

- Language ( dart, JavaScript, HTML5, C#, C/C++) <br/>
- MQ (Kafka, RabbitMQ) <br/>
- Monitoring (Prometheus, Grafana, pinpoint, nGrinder, Datadog) <br/>
- Frontend (Flutter,React.js,Vue.js, Nuget) <br/>
- OS (Linux, MacOS, Windows) <br/>
- DevOps (docker, nginx, GithubActions, ArgoCD)<br/>

---

## Work


<h3> 삼성전자 </h3>
<span style="color:gray"> Tizen Application Developer </span> <span style="float: right; color:gray"> 2024.01 ~ 현재 </span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
<div markdown="1">
<br/>
<strong> Role </strong> <br/>
제품에 들어가는 LCD 애플리케이션 개발 담당
<br/><br/>
<strong> What I did </strong> <br/>
- 로그 분석을 통한 신규 팝업 생성
<br/>&emsp;
  <strong>Situation</strong> : x 시점에서 단 한 번만 발생하는 팝업을 생성해야 하는 상황, 과거 동일 요구사항이 있었지만 단 한 번만 실행되는 팝업을 만들지 못함
<br/>&emsp;
  <strong>Solve</strong> : x 시점에 특정 파일이 생성되어 flag 역할을 한다는 정보를 바탕으로 해당 파일을 생성하는 패킷이 어디에서든 존재할 것이라 추정하였고, 해당 파일을 찾기 위해 디버거를 통해 로그를 뒤졌고 해당 파일을 생성한 후 완료를 알리는 패킷이 전송된다는 사실을 확인 후 해당 패킷을 팝업의  flag로 사용
<br/>&emsp;
  <strong>Result</strong> : 기획서 및 사양서 수정 없이 개발 정상 진행
<br/><br/>
- 선행 개발 상품 LCD 개발 대응
    - 여러 부서와의 협업을 통해 요구사항 정리, 구현 필요 항목 정리 등의 업무를 수행
    - 해외의 개발자들에게 필요한 구현 사항에 대해 영문으로 개발 가이드 문서를 작성하여 업무를 도왔으며 실시간으로 소통하며 개발을 진행하고, 코드 리뷰를 통해 개선 방향을 제시하며 협업

</div></details>

<h3> AITStory </h3>
<span style="color:gray">Backend Developer </span> <span style="float: right; color:gray"> 2023.09 ~ 2023.12 (4개월)</span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
<div markdown="1">
<br/>
<strong> Role </strong> <br/>
T map의 전기차 충전 플랫폼 백엔드 개발 담당
<br/><br/>
<strong> What I did </strong> <br/>

- 기존 결제 대기 상태로 종료된 충전으로 인해 발생하는 문제점 해결

  <strong>Situation</strong> : 충전 종료 요청 이후 결제가 진행되다 결제 대기 상태에서 충전이 정상적으로 종료된 후 결제가 멈추는 현상 발생
<br/>&emsp;

  <strong>Solve</strong> : 결제 대기 상태로 바뀐 시점 ~ 이후 상태 값이 바뀌는 시점 사이에서 발생할 수 있는 모든 종류의 오류를 순서대로 발생시키는 테스트 시나리오 작성, 그 후 실제 환경에서 발생할 수 있는 원인을 분석. 
<br/>&emsp;&emsp;&emsp; 한 유저가 동시에 2건의 충전을 종료시키는 경우 결제 플랫폼에서 오류가 발생하게 되지만 해당 결제의 결과는 메세징 큐를 통해 비동기로 전송되고 해당 큐의 리스너에서 결제의 결과를 저장
<br/>&emsp;&emsp;&emsp; 따라서 결제 요청의 실패를 충전 건에 반영하지 못하고 있었고, 충전 종료 요청에 대한 오류 또한 통합하여 제공하였기에 오류의 원인도 트래킹이 되지 않음
<br/>&emsp;&emsp;&emsp; 해당 요청에 대해서 동시성이 문제였기에 Retry 옵션을 추가하였고, 동시 재요청을 방지하기 위해 jitter를 추가
<br/>&emsp;

    <strong>Result</strong> : retry 추가 및 오류 상세화 이후 해당 현상이 발생하지 않게 됨.
<br/>&emsp;&emsp;&emsp; 또한, 정산 불일치의 주된 원인이 해당 현상이었기에, 수작업으로 결제 취소 후 재결제 하던 정산 과정을 90%가량 감소시킴.
<br/><br/>


- 특정 api에서 발생하던 응답 지연 현상 해결

  <strong>Situation</strong> : X에 관한 정보를 사용하는 api의 응답속도가 다른 api들에 비해 눈에 띄게 느림
  <br/>&emsp;

  <strong>Solve</strong> : 해당 api의 응답속도가 느려진 시점을 모니터링 도구를 통해 파악하고 해당 시점의 코드와 현재 코드를 비교
  <br/>&emsp;&emsp;&emsp; 기존 db에서 조회하던 X를 타 서비스에서 제공받은 것으로 대체했다는 변경 점 확인
  <br/>&emsp;&emsp;&emsp; 이 과정에서 필터에 걸러지는 데이터 또한 X에 관한 정보를 가지고 있는 방식이라는 것을 확인했고, 해당 데이터들이 필터링이 끝난 후 X에 대한 정보를 포함하게끔 변경
  <br/>&emsp;

  <strong>Result</strong> : api의 응답속도가 P50(중간값) 기준  461ms -> 59.5ms로 약 675%의 성능 향상
  <br/><br/>

- 쿠폰 코드 추가 프로세스 단축
  <br/>&emsp;

  <strong>Situation</strong> : 신규 쿠폰 코드 추가 시 쿠폰 유효성 검증 및 db에 추가하는 과정에 드는 시간이 많이 소요 됨
  <br/>&emsp;

  <strong>Solve</strong> : 수식에 맞게 쿠폰 코드를 만들어내는 기능과 admin api를 통해 관리자가 api 호출로 간단하게 원하는 수만큼의 쿠폰을 추가한다면 기존의 방식에 비해 소요 시간을 많이 단축할 수 있다고 생각
  <br/>&emsp;&emsp;&emsp; 쿠폰의 유효성을 검증하는 방식으로 
    1. DB의 쿠폰 코드들을 조회하여 만들어진 쿠폰 코드 중 중복된 값을 제거한 후 다시 추가하는 방식
    2. 기존에 사용했던 쿠폰 코드들이 담겨있는 엑셀 파일을 통해 쿠폰 코드의 유효성을 체크하는 방식
    3. DB의 유니크 키 예외를 통해 중복을 걸러 유효성을 체크하는 방식
  <br/>&emsp; 위 3가지 방식을 떠올렸고 각 방식을 비교해 본 결과 1000개의 신규 쿠폰 추가 기준으로 1의 방식은 평균 2분 10초, 2의 방식은 평균 1분 50초, 3의 방식은 1분 53초의 시간이 소요됨
<br/>&emsp;
    2의 방식이 제일 빠르지만 파일에 쿠폰 코드를 계속해서 추가해야 하고, PRD환경에 이러한 파일을 올려야 하기에 유지 보수성이 매우 떨어진다고 생각하였고 1,3의 방법의 경우에도 2분에 가까운 시간은 효율적이진 않다고 생각.
<br/><br/>
  저장에 걸리는 시간이 주요한 원인이었기에 이를 줄이기 위해 저장 과정 자체를 병렬로 쓰레드를 펼쳐서 하는 방법 고안
<br/>  실제 테스트 결과, 1의 경우 11초 3의 경우 10초로 저장 속도가 대폭 줄어들게 됨 

    <strong>Result</strong> : 수작업 시 1000개의 쿠폰을 삽입하는 데 걸리는 시간을 자동화하여 약 10분에서 -> 2분으로 줄임
<br/>&emsp;&emsp;&emsp; 또한, 병렬 저장을 통해 이를 추가로 개선해 2분 -> 10초로 단축할 수 있었음
<br/><br/>

- 사후 재결제 기능 개발

  <strong>Situation</strong> : 정산 시 발생하던 금액 차이로 인해 수동으로 실제 충전 사용량을 바탕으로 다시 결재하는 상황에서 이를 자동화하는 신규 프로세스 구축
    <br/> 충분한 검증 필요, 쿠폰 및 사용자의 충전 이용 등 전반적인 서비스 사용에 영향을 주지 않아야 함
  <br/>&emsp;

  <strong>Solve</strong> : 결제 내역을 바탕으로 해당 건에 사용된 쿠폰을 찾아 복구시킨 뒤 재결제 사용 건에 강제로 연결해 쿠폰이 자동으로 사용되게끔 구현
    <br/>&emsp;&emsp;&emsp; 재결제하는 동안 생기는 이용건을 활성화 세션의 숫자에 포함되지 않게 하기 위하여 재결제가 성공할 때까지 delete 상태로 유지하고, 재결제 완료 이후 해당 내용을 모두 activate 시켜 실제 충전 세션에 영향을 주지 않게 구현
  <br/>&emsp;&emsp;&emsp; 한 사용자가 동시에 2건의 충전을 종료시키는 경우 결제 플랫폼에서 오류가 발생하게 되지만 해당 결제의 결과는 메세징 큐를 통해 비동기로 전송되고 해당 큐의 리스너에서 결제의 결과를 저장
  <br/>&emsp;&emsp;&emsp; 가능한 모든 상황을 나누고, 재결제 로직에서 발생할 수 있는 모든 오류를 정리하여 이를 테스트 케이스화 하고 메인 서버와 배치 서버 모두에서 모든 시나리오에 대해 자동화 검증 수행
  <br/>&emsp;

  <strong>Result</strong> : 건당 1분 이상 걸리던 작업을 자동화하여 불필요한 반복 작업을 없앨 수 있게 되었고, 이를 통해 보다 강건한 서비스를 운영할 수 있게 됨
  <br/><br/>
</div></details>
---

## PROJECTS

<br/>

<h3> <a href="https://sirong-blog.tistory.com/category/Gyunpang"> Gyunpang </a> </h3>
 개인 프로젝트 <span style="float: right; "> 2024.03 ~ </span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
 <div markdown="1">
<br/><br/>
<strong>프로젝트 구조</strong><br/>
<img src="/assets/img/Gyunpang_Architect.jpg" alt="프로젝트구조">
<strong>프로젝트 소개</strong><br/>
실제 서비스 도중 발생할 수 있는 여러 상황들을 만들어보고 이 상황 속에서도 강건하게 유지되는 시스템을 구축해 보고자 시작한 프로젝트입니다.<br/>
인터넷 쇼핑이라는 도메인을 이용하여 선착순 쿠폰, 재고 처리 등 다량의 사용자가 접근하는 상황에서 발생하는 동시성 문제와 특가 이벤트와 같이 일시적으로 급격하게 증가하는 트래픽에 대처하는 방법을 익혀보는 것이 목적인 프로젝트입니다<br/>
<br/>

<strong> What I did </strong>
<br/>
- 도커 컴포즈를 통해 여러 대의 컨테이너를 무중단 배포
  <br/> <strong> Situation </strong> 
  <br/>프리티어 인스턴스 하나에 메인 백엔드 서버가 들어간 3개의 컨테이너를 띄우고 매 배포마다 blue/green 방식으로 컨테이너를 교체하려 함
  <br/> 그런데, 인스턴스의 성능 탓에 6개의 컨테이너를 잠깐이라도 유지하는 게 불가능함 
  <br/><br/>
  <strong> Solve </strong> 
  <br/> 기존 운영되는 color의 컨테이너의 스케일을 1로 줄인 후 새로운 컨테이너를 띄우는 방식 시도 -> 3대의 old 컨테이너가 모두 꺼지고 1개의 old 컨테이너가 다시 시작 됨
  <br/> 도커 이미지가 최신화 되어 다시 생성되는 것일 수 있다고 생각하여 도커 이미지를 pull 하기 전에 스케일을 1로 줄이는 방식 시도 -> 동일하게 1개의 컨테이너가 재시작 됨
  <br/> 해당 기능을 제공하는 옵션이 있을 것이라 추정하고, 공식 문서에 생성과 관련된 기능을 찾다 --no-recreate 옵션을 통해 컨테이너를 재생성 하지 않을 수 있다는 것을 확인, 해당 옵션 적용
  <br/>
  <br/> <strong> Result </strong> 
  <br/> 배포 -> old 컨테이너 1개로 rescale -> new 컨테이너 3개 up -> nginx 컬러 변경 및 reload -> old 컨테이너 down의 방식으로 무중단 배포 구현 완료
<br/><br/>

- 카프카 클러스터 구축
  <br/> <strong> Situation </strong> 
  <br/> 로그 메세지 및 이벤트 큐 관리를 위해 카프카를 사용하기로 했고, 인스턴스 성능 상 클러스터를 구축하여 사용하려고 함
  <br/> 그런데, 두 인스턴스 간 클러스터 연결이 잡히지 않음
  <br/><br/>
  <strong> Solve </strong> 
  <br/> 서로 간의 연결이 문제이기에 가장 먼저 포트가 열려있는지 확인해 보았으나 두 인스턴스 모두 서로에게 포트를 개방해 놓은 상태였다.
  <br/> 다음으로 서로 간 실제로 통신이 되는지 확인하기 위해 ping을 보내봤는데, node 1 -> node 2의 통신은 가능했지만 node2 -> node1의 핑이 오지 않았다. 이에 이상하다 싶어 확인해 보니 ec2 인스턴스의 경우 기본적으로 ICMP가 켜져 있지 않아 핑을 허용하지 않았고 이를 수정했다.
  <br/> 하지만 이를 변경한 후에도 연결은 서로 간 연결은 되지 않았고, KRaft 모드에서 클러스터 형성이 불안정한 것인가 싶어 로컬 환경에서 두 개의 카프카 노드를 띄워 확인해 보니 정상적으로 연결이 되었다.
  <br/> telnet을 통해 서로 간 포트 개방 여부를 확인하던 중 node 2의 카프카 포트가 열려있지 않은 걸 확인했다. 이에 다른 포트 80,443,8080 (node 2는 웹서버, 게이트웨이 역할을 한다)를 확인해 봤으나 다른 포트들은 모두 열려있었다.
  <br/> 두 인스턴스 간 차이를 생각해 보다 OS가 다르다는 사실을 알게 되었고 node 2의 경우 Ubuntu를 사용하고 있었고 ufw가 활성화 되어 있었으며 여기서 9092 포트는 허용해 놓지 않았기에 모든 요청이 block 되고 있었던 것이었다.
  <br/> ufw를 허용해 주고 다시 확인해 보니 정상적으로 연결되는 것을 알 수 있었다.
  <br/> <strong> Result </strong> 
  <br/> 비록, 아주 단순한 원인 때문에 발생했던 이슈였지만 인스턴스 간 통신에 대해서 조금 더 알아볼 수 있게 된 좋은 경험이었다.
<br/><br/>


<strong>사용한 기술 스택</strong>
<br/><br/>
BE : Spring (MVC, WebFlux, JPA, Security, Cloud, Kafka) <br/>
Devops : nginx, docker <br/>
MQ : Kafka(Kraft) <br/>
Cache : (Redis) <br/>
Monitoring : Pinpoint <br/>
<br/><br/>

</div>
</details>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3> <a href="https://github.com/orgs/EmptySaver/repositories"> 공강구조대 </a> </h3> 팀 프로젝트 (3인) <span style="float: right; "> 2023.03 ~ 2023.06 (3개월) </span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
<br/>
 <div markdown="1">
프로젝트 시연 영상은 <a href="https://www.youtube.com/watch?v=LYtQgMJNOks"> 여기</a> 에서 확인하실 수 있고,
<br/>
프로젝트의 PPT는 <a href="https://github.com/EmptySaver/EmptySaverBE/blob/master/%E1%84%80%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A1%E1%86%BC%E1%84%80%E1%85%AE%20%E1%84%8E%E1%85%AC%E1%84%8C%E1%85%A9%E1%86%BC%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD.pptx">여기</a> 에서 다운받으실 수 있습니다.
<br/>
<strong>프로젝트 소개</strong><br/>
시간표와 통학이라는 소재를 이용해 대학생활을 하며 아쉬웠던 점을 해결해보자는 아이디어로 시작한 프로젝트 입니다. 팀원들 모두 통학을 해본 경험이 있었고 통학하는 과정에서 공강시간이 크게 생기는 경우 다시 집으로 돌아가기에는 시간이 너무 무의미하게 사용되어 집으로 갈 수는 없지만 그렇다고 마땅히 할 일을 생각해내지 못하고 시간을 무의미하게 보낸 경우가 많았습니다. 이런 경험을 토대로, 공강시간에 할 수 있는 다양한 활동을 추천해주고 시간을 효율적으로 관리할 수 있게 도와주자는 취지로 프로젝트를 진행하게 되었습니다.
<br/><br/>
<strong>담당한 부분</strong> : Fullstack
<br/><br/>

<strong>What I did</strong>
<br/>
- CI/CD 파이프라인 구축
- JWT 및 이메일 인증 기능 구현
- 교내 페이지 및 영화 상영 정보 크롤링 기능 구현
  - 로그인 페이지와 크롤링 대상 페이지 간 도메인이 달라 로그인 유지 실패로 크롤링이 안되는 현상 발생
    - 실제 브라우저 상에선 로그인 후 해당 페이지로 잘 넘어가기에 이 과정에서 로그인을 유지하는 정보가 같이 넘어간다고 생각
    - 브라우저 내 개발자 도구를 이용하여 로그인부터 해당 페이지 접근까지의 모든 redirection 및 요청,응답의 header,body를 분석
    - 그 결과, 로그인 후 특정 티켓이 발급되고 해당 티켓을 바탕으로 세션에 로그인 인증을 부여하는 방식으로 동작하는 것을 확인
    - 크롤러 내부에서도 해당 티켓 값을 추출하여 크롤링 대상 페이지 접근하는 세션에 해당 값을 부여하여 인증 성공
- FCM을 통해 알림 전송 기능 구현
- 백엔드 서버 주요 기능 구현
- Flutter를 이용한 UI/UX 개선 작업


<strong>사용한 기술 스택</strong>
<br/>
BE : Spring (MVC, JPA, Security, Jsoup) <br/>
FE : Flutter <br/>
Alert : FCM <br/>
<br/>
</div></details>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3> <a href="https://github.com/sok5188/EmptySaverBEV2"> 공강구조대V2 </a> </h3> 개인 프로젝트 <span style="float: right; "> 2023.07 ~ 2023.08 (1개월)</span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
<div markdown="1">
<strong>프로젝트 소개</strong><br/>
기존 공강구조대 프로젝트를 끝낸 후 더 많은 사용자가 사용하는 환경에서 발생하는 문제들을 해결해 보고 싶다는 생각이 들어 진행한 프로젝트입니다.
<br/>


<strong>What I did</strong>
<br/>
- Spring Actuator 활성화 및 prometheus, grafana, pinpoint를 통한 모니터링 시스템 구축
- nGrinder를 통해 테스트 시나리오 작성 및 부하 테스트 수행
- Spring In Memory Cache 사용


<strong>사용한 기술 스택</strong>
<br/>
BE : Spring (MVC, JPA, Cache), nGrinder <br/>
Monitoring : prometheus, grafana, pinpoint <br/>

</div></details>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3> <a href="https://github.com/HomebrewComputerClub/Team2_Chatting_BE">HomebrewChatting</a> </h3> 팀 프로젝트 6인 <span style="float: right; "> 2023.05 ~ 2023.05</span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
 <div markdown="1">

<br/>
<strong>프로젝트 소개 </strong><br/>
이 프로젝트는 서울 소재 대학생 간 진행하는 프로그래밍 스터디 Homebrew 클럽에서 진행한 프로젝트로, 채팅 기능 및 인증 기능을 메인으로 하는 Homebrew 동아리 홈페이지를 제작하는 프로젝트입니다. <br/>

<strong>What I did</strong>
<br/>
- CI/CD 파이프라인 구축
- 웹서버(nginx) 설정
- 소켓 통신을 이용한 채팅 기능 구현
<br/>
<br/>

<strong> 프로젝트 회고</strong>
팀원 모두 과제 및 시험 때문에 활동을 많이 하지 못하여, 완성도가 많이 떨어지는 프로젝트라고 생각합니다. 프론트엔드를 담당한 팀원분을 포함해 일부 인원끼리 모여 급하게 백엔드 전반을 뒤집고 프로젝트를 진행하였고 그 결과, 기존 목표였던 소셜 로그인(JWT) 및 그룹 채팅 기능 완성에 실패하게 되었고, 로컬 로그인 및 1대1 채팅 기능만 급하게 만든 상태로 프로젝트를 마무리하게 되었습니다.<br/>
채팅의 경우 1:1 채팅 및 그룹 채팅에 필요한 기능 및 API 구현은 모두 끝낸 상태로 프로젝트가 끝나게 되었고, 바라던 만큼의 완성도에 도달하지 못했다는 아쉬움이 많이 남았지만, 처음의 목표 수립 과정에서 현실적인 수준의 목표를 설정하는 것 또한 중요한 일이라는 생각을 가질 수 있게 되었다고 생각합니다.

<strong>사용한 기술 스택</strong>
<br/>
BE : Spring (MVC, JPA, Security), Websocket <br/>
FE : React.js <br/>
Devops : AWS (EC2, S3, CodeDeploy), nginx
<br/>
</div></details>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<h3><a href="https://github.com/HomebrewComputerClub/Team2_clone_BE">Homebrewtify</a> </h3> 팀 프로젝트 5인<span style="float: right; "> 2023.03 ~2023.04 </span>
<details>
<summary> 
<strong> View Details</strong>
</summary>
<br/>
<div markdown="1">
<strong>프로젝트 소개</strong><br/>
이 프로젝트는 서울 소재 대학생 간 진행하는 프로그래밍 동아리인 Homebrew 클럽에서 진행한 프로젝트로 약 한 달간 스포티파이 웹 페이지를 참고하여 Homebrewtify라는 음악 스트리밍 웹 애플리케이션을 만드는 것이 목적인 프로젝트입니다. <br/>
<br/><br/>

<strong>What I did</strong>
<br/>
- Spring Batch를 이용하여 dataset insert 기능 구현
  - spotify dataset(11만 4천곡)의 중복 제거 및 데이터 정규화를 통해 삽입 과정을 3분 이상에서 45초로 줄였습니다.
- 메인 백엔드 기능 개발
  - 원활한 개발을 위해 swagger 도입
- JWT를 통한 사용자 인증 기능 구현
<br/>

<strong>사용한 기술 스택</strong>
<br/>
BE : Spring (MVC, JPA, Security, Batch)<br/>
FE : React.js <br/>
<br/>
</div></details>
<hr/>

<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->
<!-- -------------------------------------------프로젝트 구분선----------------------------------------------------- -->

<h3><a href= "https://github.com/sok5188/GuessMusic"> 음악맞추기 </a> </h3> 개인 프로젝트 <span style="float: right; "> 2023.01 ~ 2023.02</span>  

<details>
<summary> 
<strong> View Details</strong>
</summary>
 <div markdown="1">
<br/>

<strong>프로젝트 소개 </strong><br/>
이 프로젝트를 진행하게 된 계기는, 제가 좋아하는 스타크래프트 유즈맵인 음악 맞추기 맵을 플레이하다 느낀 불편함 때문이었습니다.
워낙 많이 하다 보니, 다양한 맵이 필요했고 원하는 장르 또한 부족하다고 느꼈고 직접 유즈맵을 만들기에는 너무 많은 시간이 필요하다는 것을 알게 되었습니다.
때문에, 친구들과 함께 맵을 쉽게 만들고 플레이할 수 있는 웹을 만들고 싶다는 생각이 들어 직접 만들어 보기로 결정했습니다.<br/>
<br/><br/>

<strong>What I did</strong>
<br/>
- 로컬 및 소셜 로그인 기능 구현
- 방장과 참여자 권한 구분 및 화면 분할
- 웹 소켓을 통한 채팅 기능 구현
- 어드민 페이지 구현
<br/><br/>

<strong> 프로젝트 회고</strong>
<br/>
첫 개인프로젝트이자 아직 유일한 개인 프로젝트입니다. 평소 친구들과 자주 했던 스타크래프트 유즈맵에서 시작한 프로젝트인지라 해당 유즈맵과 유사한 점이 많다고 생각합니다. 다만, 스프링을 처음으로 학습한 상태로, 그것도 짧은 강의만 듣고 무작정 구글링을 해가며 진행했던 프로젝트였습니다. 요청마다 응답의 속도가 조금씩 차이가 나서 많은 곡을 재생하는 경우 어떤 브라우저에선 소리가 조금 밀리는 현상이 발견되었고 당시 여러 방법을 시도했으나 결국 고치지 못한 상태로 마무리한 프로젝트였습니다. 해당 프로젝트를 통해, 스프링을 통한 백엔드 설계, Thymeleaf 및 Vue.js를 이용하여 프론트엔드 설계를 경험해 볼 수 있었고, OAuth및 Spring Security에 대해 처음 공부해 볼 수 있었습니다. 특히, Spring Security의 경우 세션 로그인 방식에서 어떻게 이 로그인 정보를 유지할 수 있는지에 관해 공부해 볼 수 있는 기회가 되어 좋았습니다.

<br/><br/>
<strong>사용한 기술 스택</strong>
<br/>
BE : Spring (MVC, JPA, Security)<br/>
FE : Thymeleaf, Vue.js 
<br/>
</div></details>
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
