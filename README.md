# FastAPI with Vue.js

Build the images and spin up the containers:

```sh
docker-compose up -d --build
```

Apply the migrations:

```sh
docker-compose exec backend aerich upgrade
```

Made changes to the models, you can run the following commands to update the database:
```shell
docker-compose exec backend aerich migrate

docker-compose exec backend aerich upgrade
```

Backend:
[http://localhost:5000](http://localhost:5000)

[http://localhost:5000/docs](http://localhost:5000/docs)

Frontend:
[http://localhost:8080](http://localhost:8080) 
