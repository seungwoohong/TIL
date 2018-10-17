### Develop log

## GCP  

### How to connect google cloud to filezilla on windows

1. puttygen으로 key 생성
2. Save private key
3. key text copy
3. gcp compute engine -> meta data -> ssh
4. Modify button click
5. 본인 계정에 키 저장
6. filezilla file -> site manager click
7. 사이트 설정
    - 프로토콜: SFTP
    - host: 해당 엔진 IP 입력 
    - 로그온: 키 파일
    - 사용자: 본인 계정
    - 키 파일: 생성된 ppk 파일 선택

8. 확인 및 연결
