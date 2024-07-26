Session 2<br />
1. Pull MongoDB docker image <br />
docker pull mongodb/mongodb-community-server:latest <br />
docker run --name mongodb -p 27017:27017 -d mongodb/mongodb-community-server:latest <br />
2. Run application <br />
docker pull bdeji91/bdeji:12 <br />
docker run -p 3000:3000 --env ENVIRONMENT=production bdeji91/bdeji:12<br />
<br />
<br />
Session 3<br />
docker network create barni-practice<br />
<br />
docker run --name barni-api --network barni-practice --mount type=volume,source=apivolume,target=/home/bdeji/app -p 3000:3000 bdeji91/barni-api:1<br />
<br />
docker run --name barni-api-db --network barni-practice --mount source=db-config,target=/data/configdb --mount source=db-data,target=/data/db -p 27017:27017 bdeji91/barni-api-db:1