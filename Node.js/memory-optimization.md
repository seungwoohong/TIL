# Memory optimization

NodeJS 에서는 --max-old-space-size 플래그를 사용하면 메모리를 제한 할 수 있다.
```
$ node --max-old-space-size=512 index.js
```

이렇게 실행 시키면 메모리 사용을 512MB로 제한한다.

