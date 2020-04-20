# otus_31
# MySQL - бэкап, репликация, кластер

# Домашнее задание:

развернуть InnoDB кластер в docker
развернуть InnoDB кластер в docker
* в docker swarm

в качестве ДЗ принимает репозиторий с docker-compose
который по кнопке разворачивает кластер и выдает порт наружу

____________________________________________________________________________________________________________________________

Статьи, которые помогли :

1) [MySQL InnoDB Cluster – обзор кластера](https://sqlinfo.ru/articles/info/35.html)
2) [MySQL InnoDB Cluster Tutorial 1 - ссылка с занятия](https://sakthismysqlblog.wordpress.com/2019/12/27/mysql-innodb-cluster-tutorial-1-group-replication-mysql-shell/)
3) [Deploying MySQL using Docker-Compose](https://linuxhint.com/mysql_docker_compose/)
4) [Настройка Laravel, Nginx и MySQL с Docker Compose - для нубов в docker compose](https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose-ru)
5) [How To Install and Use Docker Compose on CentOS 7 - для нубов в docker compose(2)](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-centos-7)
6) [How To Install WordPress With Docker Compose - для нубов в docker compose(2)](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-with-docker-compose)
7) [21.4 Using MySQL Router with InnoDB Cluster - mysql доки](https://dev.mysql.com/doc/refman/8.0/en/mysql-innodb-cluster-using-router.html)

Итог:

Команда ```docker-compose up -d``` в директории с файлом *docker-compose.yml* создаёт контейнеры кластера

![Img_alt](https://github.com/Edo1993/otus_31/blob/master/pics/311.png)

Просмотр списка контейнеров ```docker ps -a```

![Img_alt](https://github.com/Edo1993/otus_31/blob/master/pics/312.png)

Из предыдущего вывода берём id контейнера ```router``` - командой 
```docker exec -it 339bf3b9a40a bash```
выполняем вход в контейнер.
Для удобства - установим *mysql-shell* в контейнере

```yum install mysql-shell -y```

Запускаем оболочку

```mysqlsh```

В оболочке подключаемся

```shell.connect('root@mysqlcluster_router_1:6446', 'pass123') ```

![Img_alt](https://github.com/Edo1993/otus_31/blob/master/pics/313.png)

Проверяем состояние кластера

```var cluster=dba.getCluster(); cluster.status()```

Получаем красивый ответ

```
        "status": "OK", 
        "statusText": "Cluster is ONLINE and can tolerate up to ONE failure." 
```

![Img_alt](https://github.com/Edo1993/otus_31/blob/master/pics/314.png)

