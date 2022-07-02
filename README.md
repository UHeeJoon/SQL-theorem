# SQL-theorem
# 주말DBMS

1.  Oracle Database 11gR2 Express Edition for Windows [[링크](https://www.notion.so/DBMS-be3a6e3d890b4129826224cb0a0918f7)]
    *  설치 간 : system 계정명 패스워드(1234) 기억 

    1. 윈도우버튼  → cmd(명령프롬프트) 검색
    2. sqlplus
    3. 로그인 :  username : system    password : 설치할때 입력한 패스워드(1234)
        1. system 계정은 root 계정이기 때문에 모든권한을 가지고 있다… 
    4. 계정 만들기 
        1. 데이터베이스 내 모든 계정 확인 : select * from all_users;
        2. 계정 생성 : CREATE USER [ 계정명 ] identified by [패스워드];
            1.  : create user mydb identified by 1234      mydb 계정명으로 패스워드 1234 생성 
        3. 계정 권한 : grant [ 권한 이름 ]  to [ 계정명 ];
            1.  grant connect , resource , dba to mydb; 
        4. 계정 삭제 : drop user [ 계정명 ]  cascade;
    5. exit : cmd에서 db 나가기

2. SQL 질의어 : 컴퓨터에게 표 만들고 수정 관리 명령하는 언어
    1. DDL ( Data Definition L ) : 데이터 정의어
        1. CREATE : 데이터베이스 테이블/스키마 만들기 
        2. ALTER : 데이터베이스 테이블/스키마 수정 
        3. DROP : 데이터베이스 테이블/스키마 삭제
        4. RENAME : 데이터베이스 테이블/스키마 이름 변경 
        5. TRUNCATE : 데이터 모두 초기화 
    2. DML( Data Manipulation L ) 데이터 조작어   [ 테이블내 조작 ]
        1. SELECT : 데이터 검색
        2. INSERT : 데이터 행 추가 
        3. UPDATE : 데이터 수정 
        4. DELETE : 데이터 삭제 
    3. DCL ( Data Control L ) 데이터 제어어
        1. GRANT : 계정에 표 관리 권한 부여 ( ROLE ) 
        2. REVOKE : 계정에 권한 해제
    4. TCL  ( Transaction Control L ) : 트랙잭션 제어어
        1. COMMIT : 작성된 명령어 실행 
        2. ROLLBACK : 작성된 명령어 취소 
        3. SAVEPOINT : 작성된 명령어 이름 지정 

![image](https://user-images.githubusercontent.com/92840513/176982687-12aed22c-9d94-4c63-a5ad-fa63d175ed4f.png)

3. 관계형 데이터베이스 
    1. Table 테이블 = 표
        1. (레코드) : 행 = 가로 = 레코드 = 튜플
        2. (필드) : 열 = 세로 = 필드 = 속성
    
   ![image](https://user-images.githubusercontent.com/92840513/176982706-e59d9c83-bc32-417b-ad0b-ffa300252ae2.png)
    
    b. view 뷰  = 가상 테이블 
    
    데이터베이스 특징
    
    1. 동시 공유
    2. 실시간 접근성
    3. 지속적인 변화
    4. 데이터 논리적 독립성 [ 서로 다른 테이블끼리 독립성 ] 
    5. 내용에 의한 참조 [ 데이터 내용 으로 검색 가능 ]
    
    테이터베이스 정의 [ 가치가 있는 자료를 공동으로 소유하는 최대한 중복을 배제한 저장할수있는 자료들  ]
    
    1. 통합된 데이터 : 자료의 중복을 배제한 데이터 모임 
    2. 저장된 데이터 : 접근할수 있는 저장 매체에 저장된 자료 
    3. 운영 데이터 : 업무에 가치가 있는 자료 
    4. 공용 데이터 : 공동 소유하고 유지하는 자료 
    
    DB 설계  = 내가 컴퓨터 영구저장 → 공유 
    
    1. 테이블 이름 만든다.. [  Board ]
    2. 필드[제목] 만들기 [ 번호 , 제목 , 글쓴이  , 작성일 , 조회 , 추천 , 내용 ] 
    3. 문법으로 작성 
    
    CREATE TABLE BOARD(
    
    번호 숫자
    
    제목 문자
    
    글쓴이 문자
    
    작성일 날짜
    
    조회 숫자
    
    추천 숫자 
    
    내용 긴문자
    
    )


