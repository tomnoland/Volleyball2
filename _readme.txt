Notes:

Sitebox


#####################################################################################

git clone --branch docker-phase-2 https://gitlab.com/rlamarca/sitebox-awesome.git app

git checkout -b tn_docker_nginx



cd /Volumes/Data/Projects/Sitebox3/app/docker/local_dev

cd /Volumes/Data/Projects/Sitebox3/app/docker/built_api_mongo

cd app/scripts && \
node pre-setup.js && \
cd ../..

cd /Volumes/Data/Projects/Sitebox3/app/docker/built_api_mongo
docker-compose up&

docker stop $(docker ps -aq) && docker rm $(docker ps -aq)

docker volume rm $(docker volume ls -q)


git pull https://gitlab.com/rlamarca/sitebox-awesome.git




Gitlab
thomasnoland
qx5gitlab




curl --header "Content-Type: application/json" \
  --request POST \
  --data '{"name": "MyTeam","siteName": "MySite","icon": "xxx","userId": "yyy"}' \
  https://sitebox-server.herokuapp.com/app/v1/team




heroku login

thomasnoland@gmail.com
!qx5heroku

YOUR_APP_NAME=sitebox-server
docker build -t registry.heroku.com/${YOUR_APP_NAME}/web .
docker push registry.heroku.com/${YOUR_APP_NAME}/web

docker build --pull --no-cache -t registry.heroku.com/${YOUR_APP_NAME}/web -f app/docker/Dockerfile_API .



docker login -u tom@noland.name --password-stdin
qx5docker

docker build -t sitebox-server -f Dockerfile_API
docker build -t sitebox-server -f app/docker/Dockerfile_API

docker-compose up --build server&

atom ~/.docker/config.json

Create sitebox-server in Heroku Dashboard

docker tag sitebox_server:1.0.0 registry.heroku.com/sitebox-server/web

heroku container:login

docker push registry.heroku.com/sitebox-server/web


heroku container:release web -a $YOUR_APP_NAME

heroku open -a sitebox-server

heroku create sitebox-server

heroku logs --tail -a sitebox-server

https://sitebox-server.herokuapp.com/app/v1

#####################################################################################

Put .env in api and client folders

Change localhost to mongo in keys_dev.js




docker stop $(docker ps -aq) && docker rm $(docker ps -aq)

docker volume rm $(docker volume ls -q)

rm -rf ./data/volumes/mongo_data
mkdir ./data/volumes/mongo_data

/usr/bin/open -a "/Applications/Google Chrome.app" ./index.html


#####################################################################################

git clone --branch development https://gitlab.com/rlamarca/sitebox-awesome.git app

cp ./data/env/.env ./app/packages/api
cp ./data/env/.env ./app/packages/client

cp ./keys_docker.js ./app/packages/api/config/keys_dev.js

cp -r ./docker ./app/


#####################################################################################

cd ./app/docker
docker-compose up&
cd ../..


#####################################################################################

docker-compose up mongo&
docker-compose up mongo-express&
docker-compose up server&
docker-compose up client&


#####################################################################################

docker rmi sitebox_server:1.0.0
docker rmi sitebox_client:1.0.0


#####################################################################################

