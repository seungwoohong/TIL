## CRLF

Line ending 

CR(Carriage-Return, \r)과 LF(Line Feed, \n)을 사용하고 Unix 나 Mac OS 는 LF 만 사용한다.

warning: LF will be replaced by CRLF


윈도에서는 CRLF 를 사용하므로 저장소에서 가져올 때 LF 를 CRLF 로 변경하고 저장소로 보낼 때는 CRLF 를 LF 로 변경하도록 true 로 설정한다.
```
$ git config --global core.autocrlf true
```