# Промежуточная аттестация 4

Создайте Docker образ nginx или вашего flask приложения

Выложите в реестр docker hub (https://hub.docker.com/) созданный образ

Создайте аккаунт (docker id) в докер хабе

Имя образа должно соответствовать формату <ваш docker id>/<имя репозитория>:<тег> Если тег не определять, то будет присвоен тег latest.  Такое имя образа можно задать сразу при сборке либо переименовать командой docker tag

docker push <имя образа>

Запустите контейнер из образа

docker run -d -p <host port>:<container port> --name mycontainer <имя образа> (это если нужно прокидывать порты на хост. Если не нужно, то параметр -p можно не указывать)

Приложите вывод команды docker inspect <имя контейнера>
    

---

## Выполнение:
    
Образ выложен в DockerHub: https://hub.docker.com/repository/docker/troitsa/flaskapp
    
**Запуск контейнера:**
    
docker run -d -p 56733:5000 \
  --name=flaskapp \
  -v $PWD:/app flaskapp

