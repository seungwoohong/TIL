## ng serve

```
$ ng serve --disable-host-check
```
> Host check를 하지 않는다. 보안상 좋지 않다.

```
$ ng serve --host 0.0.0.0
```
> host 를 설정 할 수 있다. 0.0.0.0 은 모든 호스트가 접속 가능 하다

```
$ ng serve --pord
```
> production compile 를 한다. production compile option은 anuglar.json에서 가능하다.

```
$ ng serve --configuration=production
```
> angular.json에 설정 된 configurations의 키를 지정해준다. 