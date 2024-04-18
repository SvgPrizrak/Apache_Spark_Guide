# Apache Spark
Этот гайд предназначен для тех, кто хочет развернуть Apache Spark. Все действия выполнялись на ОС Windows 10/11, в остальных ОС установку можно выполнять через командную строку, а не графический интерфейс согласно официальной [документации](https://spark.apache.org/).

Необходимый стек для выполнения процедур: 
* Java Development Kit ([скачать](https://www.oracle.com/cis/java/technologies/downloads/), я брал самую последнюю версию на момент написания гайда 22.0.1);
* Apache Spark ([скачать](https://spark.apache.org/), я брал самую последнюю версию на момент написания гайда 3.5.1);
* Python ([скачать](https://www.python.org/), можно взять самую новую версию проблем быть не должно - на момент написания гайда 3.12.3);
* Jupyter Notebook (проще всего получить, скачав [Anaconda](https://www.anaconda.com/), чуть сложнее - [Miniconda](https://docs.anaconda.com/free/miniconda/index.html);
* Hadoop и winutils.exe (см. ниже в гайде).

Перед установкой всех программ следует внимательно следить за их расположением на жестком диске, поскольку это потребуется для добавления директорий в `Path`!!!

## 1. Установка Python и Java Development Kit (JDK)
Проще всего установить согласно инструкции, никаких проблем с установкой возникнуть не должно:
* в моем случае путь для Python - `C:\Users\Имя вашего пользователя\AppData\Local\Programs\Python\Python312\python.exe`;
* в моем случае путь для JDK - `C:\Program Files\Java\jdk-22`.

## 2. Установка Apache Spark
Проще всего скачать архив с официального сайта (см. выше) и извлечь в какую-нибудь директорию (в моем случае это корневая директория - `C:\Program Files\Apache Spark`).

## 3. Установка Apache Hadoop и winutils
Из [репозитория](https://github.com/steveloughran/winutils/tree/master)
