# Apache Spark
Этот гайд предназначен для тех, кто хочет развернуть Apache Spark. Все действия выполнялись на ОС Windows 10/11, в остальных ОС установку можно выполнять через командную строку, а не графический интерфейс согласно официальной ([документации](https://spark.apache.org/)).

Необходимый стек для выполнения процедур: 
* Java Development Kit ([скачать](https://www.oracle.com/cis/java/technologies/downloads/));
* Apache Spark ([скачать]([https://www.oracle.com/cis/java/technologies/downloads/](https://spark.apache.org/)
* Python ([скачать](https://www.python.org/), можно взять самую новую версию проблем быть не должно - на момент написания гайда 3.12.3);
* Jupyter Notebook (проще всего получить, скачав [Anaconda](https://www.anaconda.com/), чуть сложнее - [Miniconda](https://docs.anaconda.com/free/miniconda/index.html);
* Hadoop и winutils.exe (см. ниже).

## 1. Установка Docker и Docker Compose
Все необходимое есть на сайте - они ставятся сразу вместе: [скачать](https://www.docker.com/products/docker-desktop/).
