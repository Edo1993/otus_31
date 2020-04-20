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

Команда ```sudo docker-compose up -d``` в директории с файлом *docker-compose.yml* создаёт контейнеры кластера
