# myweb
Custom Web Server Setting for Oracle Ampere A1(aarm64)

it need setup for docker and docker-compose

You go first give execute permission for "./createfolder.sh" ex) "chmod +x ./createfolder.sh"

then execute it.

it make folder for container.

Next, you run "sudo docker build -t myphp:1.0 ./"

(myphp is a optional name I made. you can naming for you want. but If it is changed, you should be modify docker-compose.yml)



When this is done, a custom php image that supports wordpress is created.

finally execute "sudo docker-compose up -d"

created container list:

myphp(custom build)

nginx

mariadb

phpmyadmin

redis

h5ai(this is small web file server. this is small web file server. This is not necessary for service. if you want, can delete it. if you want, can delete it)


it run with npm(nginx proxy manager).

so, containters are no ports are defined.

if you need, modify "docker-compose.yml"




###########################################################################







도커로 만든 커스텀 웹서버 세팅 입니다.
Oracle Ampere A1(aarm64)에서 테스팅 되었습니다.

docker와 docker-compose가 설치된 환경이 필요합니다.

먼저, ./createfolder.sh 에 실행권한을 주고 실행 시키세요. 컨테이너를 위한 폴더 구성을 생성 합니다.

그 후, "sudo docker build -t myphp:1.0 ./" 명령어를 사용하여 WordPress에 맞는 php 이미지를 빌드하세요.

myphp라는 이름 외에 다른 이름을 써도 되지만, 원할경우 바꿀수도 있습니다. 대신 그 경우 docker-compose.yml를 수정해야됩니다.

이미지가 생성 되었다면, "sudo docker-compose up -d" 명령어를 실행하면 도커가 컨테이너를 로드합니다.


컨테이너 리스트:

myphp(커스텀 php 빌드)

nginx

mariadb

phpmyadmin

redis

h5ai(작은 웹 파일 서버 입니다. 서비스에 필요는 없으니 원한다면 지워도 됩니다.)




이 프로젝트는 nginx proxy manager 위에서 구동된다는 가정으로 빌드가 되어 있습니다. 

당신이 필요할 경우, 포트값을 직접 선언해야될 수 있습니다.

그럴 경우 "docker-compose.yml"을 수정하여 ports를 추가해야됩니다.
