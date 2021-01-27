## Jenkins 설치하기

```sh
yum update -y
# Jenkins 패키지 추가
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat/jenkins.repo &&
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key

# Install java, docker, git
sudo yum install -y java-1.8.0-openjdk jenkins git docker

# 자바 버전 8 로 설정
alternatives --config java
service jenkins start
```

## 설치해야할 플러그인들

AWS Global Configuration: Credential 에 AWS credential 등록하게 해줌
Docker Pipeline: 파이프라인에서 도커 명령어 사용하게 해줌
Pipeline: AWS Steps

초기 비밀번호로 로그인 하기

```sh
cat /var/lib/jenkins/secrets/initailAdminPassword
```
