## 회사명 : 볼트마이크로 (주)
## 인턴 기간 : 2022.07.01~2022.12.31
## 개발팀 : 프론트엔드 개발팀

* 회사 업무 계정 설정
  * Jira
  * Confluence
  * Github
  
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









  
