# 차트 다운 받기

**레포 세팅**
```
helm repo add jenkins https://charts.jenkins.io
helm repo update
```

**레포 확인**
```java
helm search repo jenkins
```

NAME            CHART VERSION APP VERSION DESCRIPTION  
jenkins/jenkins `5.8.90`        2.516.3    Jenkins - Build great things at any scale!…

**차트 다운**
```
helm pull jenkins/jenkins --version 5.8.90 --destination /Users/elsboo/Downloads/
```

# 전체 매니페스트 확인하기
```yaml
helm template jenkins \
--namespace jenkins-beta \
-f jenkins/values.yaml \
--debug >> template.txt
```
