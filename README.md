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

초기 비밀번호로 로그인 하기

```sh
cat /var/lib/jenkins/secrets/initailAdminPassword
```
