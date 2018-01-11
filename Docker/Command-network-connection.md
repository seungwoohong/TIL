### docker container run 네트워크 연결하기

이미지를 run 할 경우 해당 컨테이너에 ***--network*** 옵션을 사용하여 네트워크를 설정 할 수 있다
```
$ docker container run --network=mynetwork myimage
```

또 해당 컨테이너에 ***--network-alias*** 을 이용하여 네트워크 별칭을 줄 수 있다.
```
$ docker container run --network=mynetwork --network-alias=mycon myimage
```

네트워크 연결 확인 방법은 ***inspect*** 옵션을 통해 확인 할 수 있다.
```
docker network inspect mynetwork
```