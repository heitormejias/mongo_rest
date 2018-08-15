# Mongo Example App

## Docker

-- rodar o MongoDB
docker run -d --name mongodb -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=root -v ./mongodb:/data/db mongo:xenial

-- rodar o Admin
docker run -d --rm --name admin-mongo --link mongodb:mongodb -p 1234:1234 adicom/admin-mongo
-- url de conexao no admin
mongodb://root:root@mongodb:27017