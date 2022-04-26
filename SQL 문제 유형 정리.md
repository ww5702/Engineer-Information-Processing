### SQL 인덱스 작성
```
student 테이블의 name 속성에 idx_name 이름의 인덱스를 생성하시오
```
CREATE INDEX idx_name ON student(name);   

### 튜플 삭제
```
학생 테이블에서 이름이 민수인 튜플을 삭제
```
DELETE FROM 학생 WHERE 이름 = '민수'   

### 튜플 수정
```
(  ) 테이블명 (  ) 컬럼 = 값 WHERE 점수 >= 90;
```
UPDATE 테이블명 SET 컬럼 = 값 WHERE 점수 >= 90;   

### 테이블에 컬럼 추가
```
학생 테이블에 주소라는 속성의 크기 20의 컬럼을 추가하는 결과를 작성
```
ALTER TABLE 학생 ADD 주소 VARCHAR(20);

### 테이블에 인덱스(정보) 추가
```
학생 테이블의 구조를 이미 제공했다고 가정
```
INSERT INTO 학생 VALUES(12345678,'홍길동',3,'경영학개론');   

### 테이블 기본 CREATE
```
이름은 NULL 이 나올수없다.
학번은 기본키이다.
전공은 외래키이다.
학과코드가 변경되면 전공 값도 같은 값으로 변경한다.
```
Not Null   
Primary   
Foreign     
References   

### SQL 결과 도출
```
결과 테이블
학과    학과별튜플수
전기      1
컴퓨터     2
전자        2

AS 사용할것, WHERE 쓰지말것, GROUP BY 사용할것 
```
SELECT 학과, COUNT(학과) AS '학과별튜플수'   
FROM 학생   
GROUP BY 학과;   

### JOIN 문법
```
SELECT ... FROM 학생정보 a JOIN 학과정보 b (   ) a.학과 = b.(   ) 
```
ON   
학과   

### 내림차순
```
성이 이씨 인 사람을 학년을 기준으로 내림차순 출력
SELET ... FROM ... WHERE 이름 LIKE ( 1 ) ORDER BY ( 2 )   
```
'이%'   
학년 DESC   
