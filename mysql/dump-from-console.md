### 쉘에서 mysql dump 하기

* 특정 스키마 모든 테이블 dump 하기
```
mysqldump -u root -p myschema mytable
```

* 특정 파일 이름으로 저장하기
```
mysqldump -u root -p myschema > myschema_dump.sql
mysqldump -u root -p myschema mytable > mytable_dump.sql
```

* 모든 스키마 dump 하기
```
mysqldump -u root -p --all-databases > allmyschema_dump.sql
```

* DB 복구 하기
```
mysqldump -u root -p myschema < myschema_dump.sql
```