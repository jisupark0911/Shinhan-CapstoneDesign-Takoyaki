# 사용자 맞춤 IT 관련 정보 추천 시스템 (문어빵)
IT 관련 직종에 대해서 취업을 희망하는 사용자들에게 맞춤 정보를 제공해주는 서비스로
채용공고, 공모전, 대외활동에 대한 정보를 제공하고 서비스를 이용하는 사용자가 취업 정보를 확인하거나 즐겨찾기를 하는 등 서비스와 상호작용 할 경우, 
해당 행위를 기반으로 사용자에게 맞춤 정보를 추천해주는 웹 어플리케이션 입니다.  
<br>
주요 기술 스택으로는 JSP, Python, MySQL, AWS RDS를 사용하였습니다.

## 목차
1. [개발환경](#개발환경)
2. [프로젝트 기능](#프로젝트-기능)
   - 회원가입
   - 로그인/로그아웃
   - 채용공고, 공모전, 대외활동
   - 사용자 맞춤 추천
   - 자유게시판
3. [사용된 기술 스택](#사용된-기술-스택)
4. [시스템 아키텍처](#시스템-아키텍처)
5. [ERD](#ERD)
6. [담당한 부분](#담당한-부분)

## 개발환경
- Eclipse 
- Google Colab
- Visual Studio Code
- JDK 17
- mysql 8.0.36

## 프로젝트 기능
1. 회원가입
- 아이디와 비밀번호 등을 입력하여 회원가입을 할 수 있다.
- 이메일은 중복이 불가하다.
2. 로그인/로그아웃
- 로그인을 하지 않고 마이페이지 사용이 불가하다.
- 로그인을 하지 않고 공고 즐겨찾기 사용이 불가하다.
- 로그인을 하지 않고 채용공고, 공모전, 대외활동의 추천이 불가하다.
- 로그아웃 버튼을 누르면 로그아웃이 된다.
3. 채용공고, 공모전, 대외활동
- 채용공고는 지역별, 학력별, 기업별 카테고리로 검색이 가능하다.
- 공모전, 대외활동은 마감임박, 접수중, 접수예정 등의 카테고리를 선택가능하다.
- 검색을 통하여 키워드와 일치하는 채용공고, 공모전, 대외활동이 출력 가능하다.
- 사용자가 조회한 채용공고, 공모전, 대외활동은 콘텐츠 기반 추천 알고리즘에 사용된다.
4. 사용자 맞춤 추천
- 사용자가 조회한 채용공고, 공모전, 대외활동을 기반으로 사용자에게 콘텐츠 기반 추천 알고리즘을 사용하여 추천한다.
- 사용자가 즐겨찾기한 채용공고, 공모전, 대외활동에 대한 별점을 기반으로 선형 회귀 모델을 사용하여, 사용자가 별점을 높게 부여할 공고를 예측하고, 이를 높은 순으로 추천한다.
5. 자유게시판
- 자유게시판에서 글쓰기 버튼을 누르면 생성페이지로 이동하여 게시글을 작성 할 수 있다.
- 자유게시판에서 수정 버튼을 누르면 수정페이지로 이동하여 게시글을 수정 할 수 있다.
- 자유게시판에서 삭제 버튼을 누르면 게시글을 삭제 할 수 있다.

## 사용된 기술 스택
<div align="center">
  <a href="https://www.java.com/">
    <img src="https://img.shields.io/badge/Java-007396?style=flat&logo=java&logoColor=white" height="30" />
  </a>

  <a href="https://www.oracle.com/java/technologies/java-server-pages.html">
    <img src="https://img.shields.io/badge/JSP-007396?style=flat&logo=java&logoColor=white" height="30" />
  </a>

  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript">
    <img src="https://img.shields.io/badge/JavaScript-FFCA28?style=flat&logo=javascript&logoColor=black" height="30" />
  </a>

  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
    <img src="https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white" height="30" />
  </a>

  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS">
    <img src="https://img.shields.io/badge/CSS-1572B6?style=flat&logo=css3&logoColor=white" height="30" />
  </a>

  <a href="https://www.python.org/">
    <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" height="30" />
  </a>

  <a href="https://www.mysql.com/">
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white" height="30" />
  </a>

  <a href="https://aws.amazon.com/rds/">
    <img src="https://img.shields.io/badge/AWS_RDS-FF9900?style=flat&logo=amazon-aws&logoColor=white" height="30" />
  </a>
</div>

## 시스템 아키텍처
![image](https://github.com/user-attachments/assets/c4ca1ea9-18c0-433b-94e1-24c94e372667)
## ERD
![image](https://github.com/user-attachments/assets/c586d1da-4ad1-44c3-a8e9-f72b70e60fed)
## 담당한 부분
- 채용공고, 대외활동, 공모전 검색 및 카테고리 기능 구현
- 워크넷 Open api 구현
- 공모전, 대외활동 크롤링
- db 설계 및 워크넷 Open api, 공모전, 대외활동 크롤링 데이터 저장 코드 구현


