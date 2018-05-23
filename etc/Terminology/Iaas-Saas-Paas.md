# IaaS, PaaS, SasS ?

이 용어들은 클라우드 서비스 유형을 말하는데 클라이언트에게 제공하는 서비스의 범위를 기준으로 나눈다.


## IaaS 란 ?
- Infrastructure as a Service의 약어이다.
- 서버 자원, IP, Network, Storage 인프라를 구축하기 위해서는 여러가지가 필요한데 이러한 것들을 가상의 환경에서 쉽고 편하게 이용 할 수 있도록 하고 H/W 확장성이 좋고 탄력적이다.
- example - AWS, Google Compute Engine

## PaaS 란 ?
- Platform as a Service의 약어이다.
- 서비스를 개발 할수 있는 안정적인 환경과 그 환경을을 이용하는 개발 할 수 있는 API를 제공한다.
- example - Google app Engine


## SaaS 란 ?
- Software as a Service의 약어이다.
- 클라우드 자체를 응용프로그램으로 제공하는 것을 SaaS라고 한다.
- example - mail service, google apps, G Suite

**ps.** 요즘 GCP에 대해서 공부 중 인데 그래서 그런지 더 명확 하게 느껴진다.

GCE(IaaS)는 내가 직접 가상 머신 내부의 환경을 꾸며야한다.

반면, App Engine은 "오로지 개발에만 집중해라" 하는 느낌을 준다.

## FaaS
- Function as a Service 약어이다
- PaaS 처럼 서버 시스템을 신경쓰지 않아도 된다는 점은 비슷 하지만
- 다른 점은 PaaS은 전체 어플리케이션을 배포 하여 24시간 계속 돌아가게 하여 실행 시키지만
- FaaS는 함수를 배포하며, 이벤트 발생 시만 실행 되었다가 작업을 마치면 종료 됩니다.