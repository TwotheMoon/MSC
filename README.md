# MSC - Muscle Challenge - JSP + 오라클 DB 로 제작한 포트폴리오
Make a health SNS site built using JSP, Oracle DB 

크로스 플랫폼을 생각하여 pc web 에서 보는 view와 휴대기기 에서 볼 수 있는 view를 css와 BootStrap 그리고 jQuery를 이용해 반응형으로 제작

<b>pc web view</b> - header, section, footer 3단 형식 

  - <b>header</b> : 로고, 회사소개, 회원가입, 스폰서, shop(결제 시스템x ) 메뉴바(nav는 header에 포함되어 jQuery를 이용해 오른쪽에서 메뉴버튼을 클릭할시 왼쪽으로 슬라이드로 나타난다.)
     - <b>로고</b>: 일러스트로 제작 (타이포그라피)
     - <b>회사소개</b> : 적재적소 이미지와 깔끔한 폰트로 제작, 본사 위치 다음 맵 api 이용
     - <b>회원가입</b> : 직접 입력 가입 or SNS 가입
     - <b>스폰서</b> : 여러 스포츠 제품 이미지 소개글
     - <b>shop</b> : 스폰서 광고 제품 판매 사이트 링크
     - <b>nav</b> : 로그인(로그인시 로그아웃 버튼 활성화, 유저 아이디표시), 회원가입, 문의사항, 회사소개, 스폰서, 스마트폰 화면전환(페이스북 참고) * position pixed

  - <b>section</b> : 2단구성
    - <b>section1</b> : 캐러셀을 이영해 이미지 슬라이드
    - <b>section2</b> : 본문내용 (M.S.C 기업 특징 등의 정보)  
  
  
  -<b>footer</b> : 유틸리티 링크(회사소개, 인재채용, 공지사항(게시판), 고객의소리(게시판), 이용약관, 개인정보처리방침), 사업자 정보(회사명, 사업자번호, 대표자, 연락처, 주소 등...)
  
  
  - <b>DB</b> : 회원정보, 광고제품, 고객문의, SNS 게시글 테이블( + 댓글 테이블 따로 구축)
    - <b>회원정보</b> Uid(PK), Upw, Uname, Ubirth, Ugender, Utel, Uemail, Uaddress, UbigThree
    - <b>광고제품</b> Pno, Pid, Pname, Pquantity Pprice, PDescription, Pcategory, Pactiovation, Pfilename(이미지)
    - <b>고객문의</b> Cid(FK), Cname, Ccontents
    - <b>SNS 게시글</b>   


<b>SNS web view</b>
  - <b>header</b> : 폰트어썸 아이콘을 이용 모든피드, 내피드, 설정(회원정보)
  - <b>section</b> : 게시글 출력(댓글 drop down)


<b>참고할 사이트</b>
  -Strava
  -Instagram or Facebook
  -FatSecreat


<b>참조할 외부 라이브러리 및 api</b>
  - Bootstrap (캐러셀 제작용) 기본 뷰는 한땀한땀 html css 로 직접 작업
  - ajax jQuery
  - fontawesome
  - 다음 맵 api
  - 유튜브 api (iframe 이용)
  - 카카오, 페이스북, 구글 로그인 api

<b>기술 구현 아이디어</b>
  - 부트스트랩을 이용한 캐러셀 (매번 이미지가 바뀌는 캐러셀)
  - sns 하트 누르면 하트색이 빨간색으로 바뀌고 숫자 카운트 (유저에따라 게시글 db 컬럼에 하트와 카운트 추가하여 조작)
  - 회원가입시 받는 3대 중량 데이터를 이용하여 회원정보에서 주간, 월간, 연간 3대 데이터 변동내용 출력 (웨어러블 기기나 기타 기기로 입력 받아으면 좋겠지만 현실적으로 구현 불가, 유저가 데이터 기록하는 식으로 표현 어플 "FatSecreat" 참고)
