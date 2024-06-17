This is a [Redis](https://redis.io) with [RabbitMQ](https://www.rabbitmq.com).

## Penggunaan Docker Redis

- download redis

      docker pull redis

- jalankanlah container

      docker run --name redis -p 6379:6379 -d redis

      penjelasan:
      --name: membuat nama container
      -p: memberikan port ke container
      -d: menjalankan container di background

- untuk mengakses dan berinterkasi dengan redis

      docker exec -it redis redis-cli

- cek image

      docker image ls
      atau menggunakan group
      docker image ls | grep nama => docker image ls | grep redis

- cek container

      docker container ls -a
      atau
      sudo docker container ls -a

- jalankanlah container yang Exited setelah laptop/pc/vps Restart

      docker start CONTAINER ID (sesuaikan dengan container id yang ada di device kalian)
      docker start 609a049e2293
      atau
      docker start NAMES (sesuaikan dengan nama container yang ada di device kalian)
      docker start redis


- stop

      docker stop redis

- hapus container

      docker rm redis

- inspect ke dalam container

      docker inspect redis

- list file

      ls -al

## Penggunaan Docker RabbitMQ

- download rabbitmq

      docker pull rabbitmq:management

- jalankanlah container

      docker run --name rabbitmq -p 5672:5672 -p 15672:15672 -d rabbitmq:management

      penjelasan:
      --name: membuat nama container
      -p: memberikan port ke container
      -d: menjalankan container di background

- cek image

      docker image ls
      atau menggunakan group
      docker image ls | grep nama => docker image ls | grep rabbitmq

- cek container

      docker container ls -a
      atau
      sudo docker container ls -a

- jalankanlah container yang Exited setelah laptop/pc/vps Restart

      docker start CONTAINER ID (sesuaikan dengan container id yang ada di device kalian)
      docker start 4f845f79aab9
      atau
      docker start NAMES (sesuaikan dengan nama container yang ada di device kalian)
      docker start rabbitmq

- stop

      docker stop rabbitmq

- hapus container

      docker rm rabbitmq

- inspect ke dalam container

      docker inspect rabbitmq

- list file

      ls -al

- masuk ke RabbitMQ

      http://localhost:15672

      username: guest
      password: guest

## Informasi

- Boilerplate ini saya buat untuk Redis + RabbitMQ