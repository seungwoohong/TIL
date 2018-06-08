## Mysql - to_days();

to_days()는 주어진 날짜와 0000년 0월 0일 사이의 일 수를 숫자로 반환해 준다.
날짜 포맷의 Stirng형 타입과 정수 타입
두 가지 타입으로 파라미터 값을 줄 수 있다.

* Example
```
to_days('2010-01-10');
to_days(20100110);
```
```
select to_days('2010-01-10');
select to_days(20100110);
```

* Result

to_days('2010-01-10')|to_days(2010-01-10)
-|-
734147|734147
<br><br>

[reference](https://www.w3resource.com/mysql/date-and-time-functions/mysql-to_days-function.php)