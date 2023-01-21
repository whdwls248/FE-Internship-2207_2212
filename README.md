## 회사명 : 볼트마이크로 (주)
## 인턴 기간 : 2022.07.01~2022.12.31
## 개발팀 : 프론트엔드 개발팀
  
## 참여 프로젝트
* ### [통합 로그인 페이지 제작](#login-part)
* ### [스튜디오 스코어보드 페이지 제작](#cameriFi-scoreboard)

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

# Login Part
뭘봐!!!!!!!!!!!!!!!!!!!











  
