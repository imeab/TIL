### ALTER: 테이블 구조 수정

| 목적 | 문법 |
|---|---|
| 컬럼 추가 | `ADD COLUMN 컬럼명 자료형 [제약조건];` |
| 컬럼 이름 변경 | `RENAME COLUMN 기존명 TO 새이름;` |
| 컬럼 삭제 | `DROP COLUMN 컬럼명;` |
| 타입 변경 (데이터 없음) | `ALTER COLUMN 컬럼명 TYPE 자료형;` |
| 타입 변경 (데이터 있음) | `ALTER COLUMN 컬럼명 TYPE 자료형 USING (컬럼명::자료형);` |
| 제약조건 설정 | `ALTER COLUMN 컬럼명 SET 제약조건 / DEFAULT 값;` |
| 제약조건 해제 | `ALTER COLUMN 컬럼명 DROP 제약조건;` |
| 기본키 추가 | `ADD CONSTRAINT 이름 PRIMARY KEY (컬럼명);` |
| 고유값 추가 | `ADD CONSTRAINT 이름 UNIQUE (컬럼명);` |
| 조건 검사 추가 | `ADD CONSTRAINT 이름 CHECK (조건식);` |
| 외래키 추가 | `ADD CONSTRAINT 이름 FOREIGN KEY (컬럼명) REFERENCES 참조테이블(컬럼명) [ON DELETE CASCADE/SET NULL];` |
| 제약조건 삭제 | `DROP CONSTRAINT 이름;` |

> 모든 문법 앞에 `ALTER TABLE 테이블명`이 붙음