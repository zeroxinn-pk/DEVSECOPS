# USEFUL LINKS
> https://www.youtube.com/watch?v=8aV5AxJrHDg

> https://www.youtube.com/watch?v=sHK8uN5fBhs&list=PLrsbMazVPK_qhf3ahA_zRPlwBaGGhSu2P

> https://www.youtube.com/watch?v=KgddhbgdHEA

COMMON TERMS
gitlab runner
CI/CD pipelines

```
runner / ubuntu
apt-get install curl

download gitlab-runner binary 
sudo curl -L --output /usr/local/bin/gitlab-runner https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-amd64
sudo chmod +x /usr/local/bin/gitlab-runner

creating gitlab-runner user
sudo useradd --comment 'GitLab Runner' --create-home gitlab-runner --shell /bin/bash

run gitlab runner as service
sudo gitlab-runner install --user=gitlab-runner --working-directory=/home/gitlab-runner 

start gitlab-runner
sudo gitlab-runner start

test gitlab-runner
gitlab-runner --version

register the runner on gitlab 
sudo gitlab-runner register --url https://gitlab.com/ --registration-token $REGISTRATION_TOKEN
sudo gitlab-runner register --url https://gitlab.com/ --registration-token GR13489411kidr9_zkSkmLyz5kjVm
shell

cd /home/gitlab-runner/
ls -al
sudo rm .bash_logout

apt-get install git
```

pipeline
```
stages:
 - build
 - test
 - integration
 - prod

job_build:
 stage: build
 script:
  - echo "This is a build stage"

jon_test:
 stage: test
 script:
  - echo "This is a test stage"

job_integration:
 stage: integration
 script:
  - echo "This is an integration stage"

job_prod:
 stage: prod
 script:
  - echo "This is a deploy stage"
```
