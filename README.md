1. Pull MongoDB docker image <br />
docker pull mongodb/mongodb-community-server:latest <br />
docker run --name mongodb -p 27017:27017 -d mongodb/mongodb-community-server:latest <br />
2. Run application <br />
docker pull bdeji91/bdeji:12 <br />
docker run -p 3000:3000 --env ENVIRONMENT=production bdeji91/bdeji:12