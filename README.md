# 주말DBMS

1.  Oracle Database 11gR2 Express Edition for Windows [[링크](https://www.notion.so/DBMS-be3a6e3d890b4129826224cb0a0918f7)]

1. SQL 질의어 : 컴퓨터에게 표 만들고 수정 관리 명령하는 언어
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
