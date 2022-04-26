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

### 테이블에 컬럼 추가
```
학생 테이블에 주소라는 속성의 크기 20의 컬럼을 추가하는 결과를 작성
```
ALTER TABLE 학생 ADD 주소 VARCHAR(20);

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
