# DBClient ? 
----
* DBClient 는 SQL IDE Tool 입니다.
* 현재는 Mysql 및 Oracle 을 지원하고 추후 여러 DBMS 를 지원할 예정입니다. 
* Tode/Orange 와 유사한 인터페이스를 지원하며, WEB 베이스로 제작되어 있습니다.
* jar 다운로드 링크 :  https://github.com/MS-Song/InsidentAlert/raw/incidentAlertV1/incidentAlert/dbclient-1.0-SNAPSHOT.jar 

# 기능 요약
* 데이터베이스 등록 기능 
* 사용자 관리 및 로그인, 로그인 로그 기록
* 사용자별 데이터베이스 접근 권한 부여
* Database 의 Schema 정보 확인
* table, field, index, view, function 등의 정보 확인
* databas Query 실행
* PL/SQL 지원
* Bind Type 쿼리 자동 완성 ( :id, #{id}, ${id}, ? )
* 필드/테이블의 한글 코멘트로 검색 지원
* Query 의 필드 자동완성 지원
* 쿼리 저장 기능 및 재사용 기능 지원
* Table 기반의 Java Model, Hibernate Model 자동 완성 기능
* Table 기반의 Mybatis Insert/Update/Select/Result 자동 매팽 기능

# 구동 환경 
* SpringBoot 2.0 으로 기동되며 java8 이상에서 작동 합니다.  
* gradle 을 통한 빌드를 해야 하며, gradle Profile 을 통한 환경 변수 관리가 필요 합니다.
* profile 환경 변수로는 local, dev, production 등이 있으며 로그 레벨 및 DB 파일 위치등을 정의 합니다. 
* 관리자 계정 및 비밀번호는 root@test.com / 12345678 입니다 

----

# 실행 방법
### 일반적 실행 방법
* java -jar dbclient-1.0-SNAPSHOT.jar

### 파일로그와 함께 실행 방법
* java -Dlogging.file=/home/mkyong/app/logs/app.log -jar dbclient-1.0-SNAPSHOT.jar

### 파일로그와 함께 실행 방법
* java -Dlogging.file=/home/song7749/log/dbclient.log -jar dbclient-1.0-SNAPSHOT.jar

### 로그 레벨 변경 방법
* java -Dlogging.level.org.springframework=TRAC -jar dbclient-1.0-SNAPSHOT.jar
* java -jar dbclient-1.0-SNAPSHOT.jar --debug

# 향후 계획
* SpringBoot 2.0 으로 재 개발 중이며, 완료 후에는 jar 파일 형태로 제공할 계획 입니다. 

# screenshot
![DBClient Execute Image](https://raw.githubusercontent.com/MS-Song/dbclient/master/dbclient_example_image.png "dbClient Screenshot")