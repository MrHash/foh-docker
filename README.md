# Docker Scripts

Build and share Docker images for Honeybee based development:
```shell
#login if required
docker login

docker build -t friendsofhoneybee/php:5.6-cli ./php/cli
docker build -t friendsofhoneybee/php:5.6-fpm ./php/fpm
docker build -t friendsofhoneybee/elasticsearch:2.4 ./elasticsearch
docker build -t friendsofhoneybee/rabbitmq:3.6-management ./rabbitmq

docker push friendsofhoneybee/php
docker push friendsofhoneybee/elasticsearch
docker push friendsofhoneybee/rabbitmq
```

Write a Docker Compose file to combine and link the images in your project...
