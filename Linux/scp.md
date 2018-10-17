# SCP
> 원격서버에 파일을 안전하게 전송할 수 있는 명령어로 Secure CoPy의 약자이다. ssh 와 동일하게 port는 22번을 사용한다.

## 명령어
`scp [옵션] [파일] [계정@서버주소]:저장경로`

ex)
```
$ scp test.txt testuser@123.123.123.80:/home/testuser/
```
> 현 위치의 test.txt를 123.123.123.80 서버의 /home/testuser/ 위치에 복사한다.

<br />

`scp [옵션] [파일] [계정@서버주소]:저장경로`

```
$ scp testuser@123.123.123.80:/var/www/test.txt /var/www/
```

> 123.123.123.80 서버의 /var/www/ 위치에 있는 test.txt를 현재 서버 /var/www/ 위치에 복사한다.

<br />

**폴더 복사**

`-r 옵션을 사용하면 된다.`
```
$ scp -r testuser@123.123.123.80:/var/www/html /var/www/
```
> 123.123.123.80 서버의 /var/www/html 폴더를 현재 서버 /var/www/ 위치에 복사한다.
