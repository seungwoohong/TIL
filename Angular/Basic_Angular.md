#  Basic of Agnular

18.02.10

자료 - https://drive.google.com/open?id=1MRXMOo6QqniMQOFvf-zTcIAqi3zZkRkBmeYgP829rGU


### Angular 특징

* Google이 2014년 Angular 2가 발표되었으며 2016년 정식 버전인 Angular 2.0.0이 출시 되었다. 개발한 **SPA** 방식의 프론트앤드 자바스크립트 프레임워크

* Component 기반으로 개발 자체의 생산성을 높이고, 대규모 애플리케이션에 걸맞는 구조를 형성한다.

* Typescript 채택 - javascript E6로도 개발이 불가능 하지는 않지만 angular 개발 그룹에서 typescript 를 권장하고 있다.

* AoT Compile

### Components? of Angular

Components 라는 말이 적절한지는 모르겠지만 angular의 구성품들을 소개 하겠습니다.

* 컴포넌트 (Component)

    컴포넌트는 화면을 구성하는 뷰(View)를 생성하고 관리하는 것이 주된 역할이며 화면은 1개 이상의 컴포넌트를 조립하여 구성한다. 템플릿과 메타데이터, 컴포넌트 클래스로 구성되며 데이터 바인딩에 의해 연결된다.
    <br/><br/>

* 디렉티브 (Directive)

    애플리케이션 전역에서 사용할 수 있는 공통 관심사를 컴포넌트에서 분리하여 구현한 것으로 컴포넌트의 복잡도를 낮추고 가독성을 향상시킨다. 컴포넌트도 뷰를 생성하고 이벤트를 처리하는 등 DOM을 관리하기 때문에 큰 의미에서 디렉티브로 볼 수 있다. 구조 디렉티브(Structural directive)와 어트리뷰트 디렉티브(Attribute directive), 커스텀 디렉티브(Cunstom directive)로 구분할 수 있다.
    <br/><br/>
* 서비스 (Service)

    다양한 목적의 애플리케이션 공통 로직을 담당한다. 컴포넌트에서 애플리케이션 전역 관심사를 분리하기 위해 사용하며 의존성 주입(Dependency Injection)이 가능한 클래스로 작성된다.
    <br/><br/>

* 라우터(Router)

    컴포넌트를 교체하는 방법으로 뷰를 전환하여 화면 간 이동을 구현한다.
    <br/><br/>
* 모듈 (NgModule)

    기능적으로 관련된 구성요소(컴포넌트, 디렉티브, 파이프, 서비스)를 하나의 단위로 묶는 메커니즘을 말한다. 모듈은 관련이 있는 기능들이 응집된 기능 블록으로 애플리케이션을 구성하는 하나의 단위를 만든다. 모듈은 다른 모듈과 결합할 수 있으며 Angular는 여러 모듈들을 조합하여 애플리케이션을 구성한다. 컴포넌트, 디렉티브, 파이프, 서비스 등의 Angular의 구성요소는 모듈에 등록되어야 사용할 수 있다.
    <br/><br/>
* 파이프 (Pipe)

    다양한 목적의 애플리케이션 공통 로직을 담당한다. 컴포넌트에서 애플리케이션 전역 관심사를 분리하기 위해 사용하며 의존성 주입(Dependency Injection)이 가능한 클래스로 작성된다. angularjs의 필터와 비슷하다

    Reference - http://seungwoohong.tistory.com/3
### Angular CLI

* Angular CLI 설치
```
$ npm i -g @angular/cli
```
* Agnular CLI 설치 확인
```
$ ng -v
```
Reference - http://seungwoohong.tistory.com/10

### Structure of Angular
<img src="../docs/images/angular_structure.png" alt="Structure of Angular Project" style="width: 200px;"/>

