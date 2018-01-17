## pm2

서버를 띄워야 하고 Node.js의 경우 서버가 크래시나면 재시작을 하기 위해서 워치독(watchdog) 류의 프로세스 관리자프로세스를 사용한다. 그 중 하나가 PM2이다.


### 설치

```
npm install(alias: i) pm2 -g
```

### 설치 확인
```
pm2 version(alias: v)
2.9.1
```

### 사용법
실행
```
pm2 start app.js --name <name>
```
실행 되고 있는 리스트 보기
```
pm2 list
```
리비전 정보 보기
```
pm2 show <id|name>
```
재시작 하기
```
pm2 restart <id | name | 'all'>
```
실행 종료
```
pm2 stop <id | 'all'>
```
app 삭제
```
pm2 delete <id | 'all'>
```


forever 와 비슷 하지만 보기에도 훨씬 깔끔하고 계속적으로 업데이트 되고 있다.

개인적으로는 pm2가 더 편하고 좋습니다.