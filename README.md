# Apache Spark
Этот гайд предназначен для тех, кто хочет развернуть Apache Spark. Все действия выполнялись на ОС Windows 10/11, в остальных ОС установку можно выполнять через командную строку, а не графический интерфейс согласно официальной ([документации](https://spark.apache.org/)).

Необходимый стек для выполнения процедур: 
* DBeaver ([скачать](https://dbeaver.io/), или иная СУБД, способная подключаться к PostgreSQL и ClickHouse);
* VSCode ([скачать](https://code.visualstudio.com/), я использовал его) / PyCharm ([скачать](https://www.jetbrains.com/ru-ru/pycharm/)) или любая другая IDE, работающая с Python;
* Python ([скачать](https://www.python.org/), можно взять самую новую версию проблем быть не должно - на момент написания гайда 3.12.3);
* Docker (см. ниже).

## 1. Установка Docker и Docker Compose
Все необходимое есть на сайте - они ставятся сразу вместе: [скачать](https://www.docker.com/products/docker-desktop/).
