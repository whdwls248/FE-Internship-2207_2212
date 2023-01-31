## 회사명 : 볼트마이크로 (주)
## 인턴 기간 : 2022.07.01~2022.12.31
## 개발팀 : 프론트엔드 개발팀
  
## 참여 프로젝트
* ### [통합 로그인 페이지 제작](#cameriFi-login)
> 실제 서비스 페이지 : https://login.camerafi.com/?callbackUrl=https%3A%2F%2Fstudio.camerafi.com%2Fko%2Fdashboard
* ### [스튜디오 스코어보드 페이지 제작](#cameriFi-scoreboard)
> 실제 서비스 페이지 :  https://studio.camerafi.com/ko/match-list

------

* 회사 업무 계정 설정
  * Jira
  * Confluence
  * Github

------

# CameriFi Scoreboard
* #### html, css를 이용한 다양한 스코어보드 제작 및 스코어보드 컨트롤 페이지 제작
* #### Vanilla JS를 통한 스코어보드와 컨트롤 페이지 연동 테스팅
  * 축구 스코어보드 & 컨트롤
![html 스코어보드 1](https://user-images.githubusercontent.com/90994001/212021341-70ca7eed-1794-4cc8-90ca-a5721eb82983.png)
![컨트롤 1](https://user-images.githubusercontent.com/90994001/212021367-b39ebea6-6485-4cff-a04a-cf259e8e30c9.png)
  * 야구 스코어보드 & 컨트롤
![html 스코어보드 2](https://user-images.githubusercontent.com/90994001/212021345-c334cd48-c15d-4000-9157-e1eea89916f0.png)
![컨트롤 2](https://user-images.githubusercontent.com/90994001/212021370-d07256bc-403c-4200-a006-4fdcc20a620e.png)
  * 테니스 스코어보드 & 컨트롤
![html 스코어보드 3](https://user-images.githubusercontent.com/90994001/212021347-e1d9ea06-ba36-431b-a7ab-e4159de63fe5.png)
![html 스코어보드 4](https://user-images.githubusercontent.com/90994001/212021349-e3b8e975-4bb2-42ae-95af-8d4e59eaffb9.png)
![테니스 컨트롤](https://user-images.githubusercontent.com/90994001/212021374-80bd8e32-1c96-49cf-b5c8-a9d22415628c.png)
  * 미식축구 스코어보드 & 컨트롤
![html 스코어보드 5](https://user-images.githubusercontent.com/90994001/212021353-bfd5e336-a365-43a3-a98b-c99d28d654ad.png)
![미식축구 컨트롤](https://user-images.githubusercontent.com/90994001/212021364-5e397779-1289-4578-8d3d-beaf0da5a6d7.png)
  * 골프 스코어보드 & 컨트롤
![html 스코어보드 6](https://user-images.githubusercontent.com/90994001/212021358-ec7e78a9-2d40-4a71-8b23-a9a6d50f7ef7.png)
![골프 컨트롤](https://user-images.githubusercontent.com/90994001/212021361-6ee224dc-1d48-45b8-8c04-4a14637c7a48.png)
> 스코어보드 페이지와 컨트롤 페이지간의 데이터 연동에는 Broadcast Channel API를 사용

### 스코어보드 통합 과정 realtime DB 구조 설계
#### 스코어보드의 경기 데이터 DB 저장 및 연결 작업을 위한 realtime DB 구조 설계
 * 현재 추가 완료된 스코어보드에 대한 DB 구조 설계
 * 설계된 DB 구조들을 통합하기 위한 회의 및 공통 데이터 추출 및 구조 정리 작업
 * 설계된 DB 구조들의 기초 코드화 작업 진행
#### node.js와 firebase를 이용한 경기 데이터 저장
> control 페이지에서 조작된 데이터가 realtime DB에 전달되면 메인 페이지에서 realtime DB에 접근하여 자신이 해당되는 key값의 value를 가져오는 방식
 * Common 스코어보드 firebase realtime DB 연결
![common_DB](https://user-images.githubusercontent.com/90994001/213390193-7b470428-770c-44b6-90b2-e20ced54b2f2.png)
 * Tennis 스코어보드 firebase realtime DB 연결
![image](https://user-images.githubusercontent.com/90994001/213390259-a63c5004-cdb9-4096-8a4f-4422b7bf83e5.png)
> 팀별 이미지 파일의 경우 firebase storage에 업로드 후 생성된 링크 사용
 * 팀별 이미지 업로드
![image](https://user-images.githubusercontent.com/90994001/213390298-57962211-3737-4bad-bc6b-db4b8a2ef9bb.png)

#### 기존 프로젝트와 스코어보드 통합과정에서 스코어보드를 React로 포팅
 * React로 포팅된 기존 스코어보드 미리보기 화면
 ![리액트 포팅](https://user-images.githubusercontent.com/90994001/213615720-d3288c47-ad36-4689-9a57-fe6974e59f8a.png)
 * React로 포팅한 스코어보드와 realtime DB 연결
 
### 스코어보드 페이지 제작 및 컨텐츠 추가
> UI 제작에는 MUI를 사용하였고 프로젝트 언어는 Typescript 사용

#### 컨트롤 페이지 타이머 기능 추가
![image](https://user-images.githubusercontent.com/90994001/213616034-53cb3fa0-475a-4723-b779-874cb80344f2.png)

#### 컨트롤 페이지 스코어보드 보이기/숨기기 기능 추가
![보이기 숨기기](https://user-images.githubusercontent.com/90994001/213616975-d8b90535-65b3-48d5-8bdb-cb6fa035365d.png)
![보이기 숨기기2](https://user-images.githubusercontent.com/90994001/213616977-935b051a-d55c-4e51-8929-9aca9ddfe723.png)

#### 각 종목별 컨트롤 페이지 생성
 * 미식축구
![미식축구 컨트롤](https://user-images.githubusercontent.com/90994001/213616972-518ff93c-0202-465a-82d3-c4145ceab3de.png)
 * 테니스
![테니스 컨트롤](https://user-images.githubusercontent.com/90994001/213616979-cbaa267a-5df5-40b5-a186-d5de9a987f0a.png)

### 경기 상세 페이지 조회수 & 좋아요 기능 추가
 * 조회수
 > 파이어베이스의 firestore의 각 경기 matchID 안에 조회수 저장 데이터 추가
 * 좋아요
 > 파이어베이스의 firestore의 각 경기 matchID 안에 해당 경기에 좋아요를 누른 사용자들의 uid를 저장
![좋아요 뷰](https://user-images.githubusercontent.com/90994001/213619099-b4c84c52-1833-48e2-bee4-194b5af250bf.png)

### 선수 목록 페이지 컨텐츠 추가
> 선수 소개 오버레이와 선수 명단을 확인할 수 있는 페이지 제작

#### 선수 목록 페이지 레이아웃 작업
* 경기 상세 페이지에서 선수 명단 페이지 이동버튼 추가
* URL, 미리보기, 선수 목록 탭, 테마 탭으로 구성
* 선수 목록 탭엔 선수 정보 데이터를 가져와 보여줌
![image](https://user-images.githubusercontent.com/90994001/215698183-77676687-532c-4718-b9c6-58f8e3740aaa.png)

#### 선수 명단 소개 테마 제작 및 테마 탭 연결
* 선수 명단 소개 테마3 제작
![image](https://user-images.githubusercontent.com/90994001/215701374-868100bc-2d81-4578-83e3-5bdf0fe2fab2.png)
* 테마 탭 구현 및 테마 연결
  * DB구조 변경 및 DB, RDB 불러오기 수정
  * Firestore에 Overlay 썸네일 폴더를 만들고 테마 썸네일 저장 및 
![image](https://user-images.githubusercontent.com/90994001/215701117-725c5708-5831-4393-99f9-7eab726033ff.png)

### 스코어보드 공유 기능 추가
#### 스코어보드 공유 버튼 추가 및 기능 구현
* 데스크탑 환경에서 공유 버튼 클릭 시 클립보드에 복사
![image](https://user-images.githubusercontent.com/90994001/215706607-9709ec2c-7789-4fde-ba4d-5df8732996e9.png)
* 모바일 환경에서의 공유 기능
> Web Share API 사용
![image](https://user-images.githubusercontent.com/90994001/215706761-3645d945-df46-4eb8-825f-b7a4a7f1ac20.png)
#### 스코어보드 공유 페이지 메타 태그 작업
* matchData의 undefine 방지를 위하여 next.js의 Serversideprops에서 matchData를 가져온 후 경기 상세 페이지 컴포넌트의 props로 넘겨줌
* matchData의 경기 사진과 경기 명을 meta 태그로 넘겨줌
![메타태그](https://user-images.githubusercontent.com/90994001/215708190-4d09e1ab-d157-4ea1-8d31-5a4ecd4f216a.png)

### 각 종목별 프로 컨트롤러 추가
> 데스크탑과 모바일 환경에 따라 다른 반응형 UI 적용
* 축구
![축구 프로 컨트롤](https://user-images.githubusercontent.com/90994001/215709952-14dab1f8-c39c-4a54-9d9b-390f88842884.png)
* 테니스
![테니스 프로 컨트롤](https://user-images.githubusercontent.com/90994001/215710064-5932259b-929b-4dec-9a8d-27b179947d67.png)
* 미식축구
![미식축구 프로 컨트롤](https://user-images.githubusercontent.com/90994001/215710035-0526571e-1388-4f64-bbed-44a1c609ea06.png)
* 야구
![야구 프로 컨트롤](https://user-images.githubusercontent.com/90994001/215710470-a426eb52-8fcb-4832-857d-25cfeeebf4e2.png)

### 선수 명단 & 컨트롤 페이지 병합
> controlMatch와 platerList 컴포넌트를 하나의 공용 컴포넌트로 합치는 작업
![image](https://user-images.githubusercontent.com/90994001/215710635-e865b13c-08cd-4395-b080-153360d37785.png)

### figma로 디자인된 유저 프로필 페이지 UI 구현
![image](https://user-images.githubusercontent.com/90994001/215711489-54edb527-6409-4915-9957-28a0f72f573c.png)

### 유저 프로필 페이지 기능 구현
#### 유저 프로필 정보 가져오기
* 프로필 페이지의 주인의 uid를 동적으로 가져오는 동적 페이지
* uid를 사용하는 API를 통하여 해당 사용자의 닉네임, 국가 정보 및 경기 데이터를 가져옴 
![프로필 페이지](https://user-images.githubusercontent.com/90994001/215711843-45393405-afc1-420f-b7d9-54b39da2271d.png)

#### 유저 팔로우 기능 구현
* 팔로우 버튼 토글링
* API를 활용하여 팔로우, 팔로잉 uid 데이터베이스와 연결 및 팔로우, 팔로우 취소 기능 구현
![팔로우](https://user-images.githubusercontent.com/90994001/215712333-49bd0279-561d-4c11-b8ef-27fd7bc41b8e.png)
![image](https://user-images.githubusercontent.com/90994001/215712134-5cbdca77-4397-42a9-9f32-6a6368dcf4d6.png)

------

# CameriFi-login

## CameraFi Studio, CameraFi ShopiFi, CameraFi Live에서 각각 따로 운영되고 있던 로그인 페이지들을 하나의 통합 로그인 페이지로 변경

### figma로 디자인된 통합 로그인 페이지 UI를 구현
#### 사용 기기의 화면 비율에 따른 반응형 웹페이지 구현
> UI작업엔 bootstrap과 mdl 사용
  * 제작한 통합 로그인 페이지
  ![통합로그인](https://user-images.githubusercontent.com/90994001/215431504-85b22aea-61ce-46e5-a138-0369f5f975fe.png)
  * 제작한 이메일 로그인 페이지
  ![이메일 로그인](https://user-images.githubusercontent.com/90994001/215431492-51919fac-bf40-4189-a584-ff1b7e7f78af.png)
  * 제작한 회원가입 페이지
  ![회원가입](https://user-images.githubusercontent.com/90994001/215431507-45ca3020-1162-4def-8976-8b446a3d1b1f.png)
  * 각 페이지별 모바일 버전
  ![모바일 UI](https://user-images.githubusercontent.com/90994001/215679160-440ae5d8-d751-4600-8fcc-c55f5a119e52.png)
  
### 통합 로그인 및 회원가입 기능 구현 및 에러 메시지 구현
> 로그인 및 회원가입엔 Firebase Auth의 API 활용 
![image](https://user-images.githubusercontent.com/90994001/215679853-8725b65a-415c-44cd-ac98-bdd76747b9fe.png)
![image](https://user-images.githubusercontent.com/90994001/215679910-59f9b3d7-c726-4c0e-a9ce-b52a9390fe6b.png)

### 회원가입 완료 페이지 제작
> 이메일 회원가입 시 가입 완료 페이지에 가입한 이메일 주소와 token 값을 callbackURL로 전달
* 소셜 서비스로 최초 로그인 시 소셜 회원가입 완료 페이지
* ![image](https://user-images.githubusercontent.com/90994001/215708689-e34a5042-21ad-4b8b-b467-b6536650330a.png)
* 이메일 회원가입 완료 시 이메일 회원가입 완료 페이지
![image](https://user-images.githubusercontent.com/90994001/215708701-65fc90b9-f483-43a0-92b0-a0fb325af2a8.png)







