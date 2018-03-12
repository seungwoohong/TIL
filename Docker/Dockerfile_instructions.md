# Dockerfile's instructions

vscode에서 Dockerfile를 작성할때 docker플러그인을 설치하면 instruction마다 어떻게 사용하고 그에 대한 예시까지 보여준다. 너무 편하다.
거기다가 잘못 작성 했을 경우에 친절하게 왜 잘못 작성한건지 이유까지 설명해주며 고치라고 한다.

**FROM**

FROM은 Base 이미지를 지정해 주는데 주로 OS나 런타임 환경을 설정 하게 된다.
Base 이미지는 [DockerHub](https://hub.docker.com/)에서 쉽게 찾아 볼 수 있으며 원하는 버전의 alias를 지정 해주면 된다.
```
FROM ubuntu:14.04
FROM node:8
```

**RUN**

shell command를 해당 docker image에 실행시킬때 사용한다.
```
RUN npm install
```

**EXPOSE**

Docker container 외부에 노출 할 포트를 지정한다. port 80

