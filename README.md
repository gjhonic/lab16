# Laboratory work №16

**Install Projects**

```bash
git clone git@github.com:gjhonic/lab16.git
```

**Install Docker**

```bash
sudo pacman -S docker
sudo pacman -S docker-compose
```

**launch**

```bash
# Start docker (not work in windows wsl)
sudo systemctl start docker

#if you use windows wsl then need command
sudo service docker start

cd lab16

make upd
```

**Test**

```bash
$ curl http://127.0.0.1/v1/todos/list
>  (id: 0, message: wake up, description: you need wake up man)
(id: 1, message: to eat, description: You have to eat so as not to die)
(id: 2, message: go to bed, description: to wake up you have to fall asleep)
```

**Other command**
```bash

#Войти в контейнер (в бд например)
sudo docker exec -it lab16_postgres_1 bash 

#Зайти в бд под пользователем rust
psql -Urust -hlocalhost -dlab16

#Остановить контейнер (с бд например)
sudo docker stop lab16_postgres_1

#Удалить контейнер (с бд например)
sudo docker rm lab16_postgres_1

```