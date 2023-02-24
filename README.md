# multicontainer_docker_tutorial

To setup a multi-containers docker to host a frontend server running on Angular 11, a Node.js backend server and a NGINX reversed proxy server.

# Test Local
Make sure you have docker installed on your local machine.

Run command:

cd multicontainer_docker_tutorial
docker-compose up --build 


docker pull my-sql
docker pull nginx
docker pull node:12.7-alpine
docker pull node:12.13-alpine
docker pull adminer
docker tag nginx 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/nginx:latest
docker tag node:12.13-alpine 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/node:12.13-alpine
docker tag node:12.7-alpine 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/node:12.7-alpine
docker tag adminer 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/adminer:latest
aws ecr get-login-password --region ap-northeast-1 | docker login --username AWS --password-stdin 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com
docker push 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/nginx:latest
docker push 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/node:12.7-alpine
docker push 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/node:12.13-alpine
docker push 074155581761.dkr.ecr.ap-northeast-1.amazonaws.com/adminer:latest


check the username that were used to clone the git
git remote -v
git config --get remote.origin.url

git config user.name "leehin"
git config user.email "diamdiam@gmail.com"
asdf