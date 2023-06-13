https://www.youtube.com/watch?v=8aV5AxJrHDg
https://www.youtube.com/watch?v=sHK8uN5fBhs&list=PLrsbMazVPK_qhf3ahA_zRPlwBaGGhSu2P


COMMON TERMS
gitlab runner
CI/CD pipelines

```
runner / ubuntu
apt-get install curl
sudo curl -L --output /usr/local/bin/gitlab-runner https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-amd64
sudo chmod +x /usr/local/bin/gitlab-runner
sudo useradd --comment 'GitLab Runner' --create-home gitlab-runner --shell /bin/bash
sudo gitlab-runner install --user=gitlab-runner --working-directory=/home/gitlab-runner 
sudo gitlab-runner start
gitlab-runner --version
sudo gitlab-runner register --url https://gitlab.com/ --registration-token $REGISTRATION_TOKEN
shell
cd /home/gitlab-runner/
ls -al
rm .bash_logout
```
