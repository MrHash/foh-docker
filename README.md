# Docker Scripts

Build and share Docker images for Honeybee based development:
```shell
#login if required
docker login

docker build -t friendsofhonybee/nginx:1.11 ./nginx
docker build -t friendsofhoneybee/elasticserach:2.4 ./elasticsearch
docker build -t friendsofhoneybee/rabbitmq:3.6-management ./rabbitmq

docker push friendsofhoneybee/nginx
docker push friendsofhoneybee/elasticsearch
docker push friendsofhoneybee/rabbitmq
```

Write a Docker Compose file to combine and link the images in your project...
