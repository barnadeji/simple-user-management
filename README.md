1. Pull MongoDB docker image
docker pull mongodb/mongodb-community-server:latest
docker run --name mongodb -p 27017:27017 -d mongodb/mongodb-community-server:latest
2. Run application
docker pull bdeji91/bdeji:12
docker run -p 3000:3000 --env ENVIRONMENT=production bdeji91/bdeji:12