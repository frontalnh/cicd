## Jenkins 설치하기

```sh
sudo yum update -y
# Jenkins 패키지 추가
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat/jenkins.repo &&
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key

# Install java, docker, git
sudo yum install -y java-1.8.0-openjdk jenkins git docker

# 자바 버전 8 로 설정
sudo alternatives --config java
sudo service jenkins start

# 초기 비밀번호 확인
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

# docker 그룹에 jenkins 추가
sudo usermod -aG docker jenkins
sudo service docker start
sudo chmod 666 /var/run/docker.sock
sudo -su jenkins
```

## 설치해야할 플러그인들

Docker Pipeline: 파이프라인에서 도커 명령어 사용하게 해줌
Pipeline: AWS Steps
Docker
