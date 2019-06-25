docker build -t moricom/ubuntu-ko-devtools .
docker push moricom/ubuntu-ko-devtools
docker pull moricom/ubuntu-ko-devtools

# Docker in Docker 
★ [Guro Office]\
docker run -itd -v /var/run/docker.sock:/var/run/docker.sock -v /usr/bin/docker:/usr/bin/docker --name devtools moricom/ubuntu-ko-devtools

[https://labs.play-with-docker.com]\
docker run -itd -v /var/run/docker.sock:/var/run/docker.sock -v /usr/local/bin/docker:/usr/bin/docker --name devtools moricom/ubuntu-ko-devtools
