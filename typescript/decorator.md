## Decorator in typescript

### ***what is decorator?***
decorator는 클래스가 도입되면서 주석과 메타 프로그래밍을 추가 할 수 있도록 도와주는 실험적인 기능이다.

### ***Kind of decorator***
* Class decorator
* method decorator
* property decorator
* parameter decorator

### ***Class Decorator***
클래스가 선언 되기전에 사용되며 생성자를 인자로 받아 클래스를 정의, 수정등을 할 수 있다.
```
function classDecorator (constructor: Function) {
    constructor.prototype.hello = function () {
        console.log('hello');
    }
}
```
### ***Methode Decorator***
메소드가 선언 되기전에 사용되며 클래스의 프로토타입, 메소드 이름, PropertyDescriptor을 받아 메소드를 수정, 관찰 등을 할 수 있다.
```
function editable(value:boolean) {
    return function (target: any, methodName: string, descriptor: PropertyDescriptor){
        descriptor.writeble = value;
    }
}
```
### ***Property Decorator***
Property가 선언 되기전에 사용되며 클래스의 프로토타입, Property 이름을 받아 Property를 수정, 관찰 등을 할 수 있다.
```
function (target: any, propertyKey: string) {
    return PropertyKey;
}
```
### ***Parameter Decorator***
Parameter가 선언 되기전에 사용되며 클래스의 프로토타입, 메소드 이름, Parameter의 index을 받아 Parameter를 수정, 관찰 등을 할 수 있다.
```
function (target: any, methodeName: string, index: number) {
    console.log(target);
    console.log(methodeName);
    console.log(index);
}
```

### how to use
```
@classDecorator

class Hello {

}
```

### PropertyDescriptor
<https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty>

위 링크 참조