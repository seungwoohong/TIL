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

# Date Type

## DATE
**DATE** 는 'YYYY-MM-DD' 형태의 데이터를 받아 들인다.
그래서 now()처럼 초단위로 데이터를 반환하는 함수로 값을 넣으려고 하는 경우, 에러가 발생하게 된다.

## DATETIME
**DATETIME**은 'YYYY-MM-DD HH:MM:SS' 와 같이 초단위 데이터를 받아 들인다. 위에서 말한 에러는 이 타입에서는 발생하지 않는다.

## TIMESTAMP 
**TIMESTAMP**는 UTC에 따라서 시간이 변경되며 1970-01-01 00:00:01부터 시간이 지원 된다. **TIMESTAMP**는 INSERT, UPDATE시 명시적으로 값을 지정하지 않을 경우나 해당 컬럼이 NULL일 경우 자동 업데이트를 해준다.

## TIME 
**TIME** 은 시간 정보를 나타낸다. 밤위는 "838:59:59" ~ "838:59:59" 'HH:MM:SS'형태를 데이터를 받는다.

## YEAR
**YEAR**은 년도에 대한 데이터를 2자리, 4자리로 값을 받는다.
명시적으로 지정해주지 않으면 기본으로 4자리 포맷이 된다.
4자리 포맷은 1901~2155, 0000년 까지 값을 가지고 2자리는 70~69값을 가진다. 70~00은 1970~2000을 의미하며 01~69는 2001~2069를 의미한다.