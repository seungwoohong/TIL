# AMD, CommonJS

## Why ?
> script tag 이용해 여러 모듈을 import할때 중복 되는 변수들을 덮어써 버려서 ? 문제가 발생한다. 
> 
> 즉, A 와 B 라는 모듈을 import 했을 경우, 만약 두 모듈 다 나중에 import 된 B모듈이 A 모듈의 변수를 덮어쓰게 된다. 
> 
> 그렇기때문에 전역 변수에서도 문제가 발생 할 수 있다. 이런 문제를 해결 하기 위해 나온게 AMD이나 CommonJS다.

## AMD

> AMD 는 Asynchronous Module Definition의 약자로 비동기 모듈 정의를 뜻한다.

### example
먼저 AMD의 가장 대표적인 require.js를 import 한다.
```javascript
<script src="require.js"></script>
```
```javascript
define(['jquery', 'hong'], function($, h) {
  return {
    a: $,
    b: function() {
        consol.log(h);
    },
  }
});
```
> 첫 번째 인자는 모듈들의 목록을 배열 타입으로 전달 하고 두 번째 인자로는 콜백함수를 전달 하는데 인자로 모듈을 정의 할 파라메터를 정의한다.

```javascript
require(["package/myModule"], function(myModule) {
    myModule.b();
})
```
> 정의된 모듈을 로드 하는 방법은 위와 같이 require를 사용하여 로드 한다.

## CommonJS

```javascript
var lib = require( "package/lib" );

function foo(){
    lib.log( "hello world!" );
}

exports.foobar = foo;
```
> moudle.exports를 사용하여 module로 추출 된다. 

<br><br>

AMD 방식은 클라이언트 성향이 강하고 CommonJS는 서버사이드에서 많이 쓰인다.