# Foregin Key Options
일단 옵션에 대해서 알아 보기전에 외래키가 무엇인지 다시 한번 되새겨 보자

 외래키는 디비의 참조 무결성을 보장하기 위해 사용되고
 외래키를 통해 관계가 형성된 테이블을 참조 할 수 있으며
 외래키를 통해 관계가 이루어진다고 볼 수 있다.

 주의 사항?
 * Foreign Key 로 설정할 두 테이블의 필드는 같은 데이터 형을 가지고 있어야 한다

 * 꼭 기본키가 아니여도 값이 유니크면 참조 가능하다
 * BLOB, TEXT는 Foreign Key로 설정이 불가능하다

## Options
### On Delete
* Casecade

    참조하고 있는 테이블에 데이터가 삭제 되면 자동 삭제
* Set null

    참조하고 있는 테이블에 데이터가 삭제 되면 해당 데이터는 null로 update
* Set default

    참조하고 있는 테이블에 데이터가 삭제 되면 해당 데이터는 default로 update
* Restrict

    자식 테이블에 데이터가 남아 있는 경우 부모 테이블의 데이터는 삭제 불가
<br>

### On Update
* Casecade

    참조하고 있는 테이블에 데이터가 수정 되면 자동 수정
* Set null

    참조하고 있는 테이블에 데이터가 수정 되면 해당 데이터는 null로 update
* Set default

    참조하고 있는 테이블에 데이터가 수정 되면 해당 데이터는 default로 update
* Restrict

    자식 테이블에 데이터가 남아 있는 경우 부모 테이블의 데이터는 수정 불가

<br><br>
모델링 할 때 주의 하면서 사용 해야겠다 흠..
<br><br><br><br><br>

출처: http://congi.tistory.com/entry/Foreign-Key-설정-방법-및-옵션-설명
