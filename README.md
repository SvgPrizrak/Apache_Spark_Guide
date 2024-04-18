# Apache Spark
Этот гайд предназначен для тех, кто хочет развернуть Apache Spark. Все действия выполнялись на ОС Windows 10/11, в остальных ОС установку можно выполнять через командную строку, а не графический интерфейс согласно официальной [документации](https://spark.apache.org/).

Необходимый стек для выполнения процедур: 
* Java Development Kit ([скачать](https://www.oracle.com/cis/java/technologies/downloads/), я брал самую последнюю версию на момент написания гайда 22.0.1);
* Apache Spark ([скачать](https://spark.apache.org/), я брал самую последнюю версию на момент написания гайда 3.5.1);
* Python ([скачать](https://www.python.org/), можно взять самую новую версию проблем быть не должно - на момент написания гайда 3.12.3);
* Jupyter Notebook (проще всего получить, скачав [Anaconda](https://www.anaconda.com/), чуть сложнее - [Miniconda](https://docs.anaconda.com/free/miniconda/index.html));
* Hadoop и winutils.exe (см. ниже в гайде).

Перед установкой всех программ следует внимательно следить за их расположением на жестком диске, поскольку это потребуется для добавления директорий в `PATH`!!!

## 1. Установка Python, Java Development Kit (JDK) и Anaconda
Проще всего установить согласно инструкции, никаких проблем с установкой возникнуть не должно:
* в моем случае путь для Python - `C:\Users\Имя вашего пользователя\AppData\Local\Programs\Python\Python312\python.exe`;
* в моем случае путь для JDK - `C:\Program Files\Java\jdk-22`;
* путь для Anaconda на установку Spark не влияет, она нужна для запуска `Jupyter Notebook`.

## 2. Установка Apache Spark
Проще всего скачать архив с официального сайта (см. выше) и извлечь в какую-нибудь директорию Вашего компьютера, переименовать папку по необходимости (в моем случае: я переименовал название папки в `Apache Spark`, поэтому директория называется так: `C:\Program Files\Apache Spark`). Внутри директории множество папок и файлов - `bin`, `conf`, `data` и т.д.

## 3. Установка Apache Hadoop и winutils.exe
Из [репозитория](https://github.com/steveloughran/winutils/tree/master) скачать подходящую версию Hadoop (в нашем случае это папка `hadoop-3.0.0/bin`, он совместим со скачанной версией Spark). Внутри этой папки есть файл `winutils.exe`, от него работоспособность Spark зависит в первую очередь. Папку следует извлечь в какую-нибудь директорию Вашего компьютера, переименовать папку по необходимости (в моем случае: я переименовал название папки в `Apache Hadoop`, поэтому директория называется так: `C:\Program Files\Apache Hadoop`). Внутри директории должна быть только папка `bin`.

Внимание: существуют также сторонние [репозитории](https://github.com/cdarlint/winutils) с другими, более новыми версиями Hadoop, при выборе которых следует стоит быть очень осторожным, поскольку если Вы возьмете не ту версию Hadoop для Spark, то могут возникнуть конфликты (об этом чуть ниже).

## 4. Добавление в PATH
Далее следует зайти в `Мой компьютер` -> `Свойства` -> `Дополнительно` -> `Переменные среды` - для разных версий Windows методология может немного отличаться (например, в ОС Windows 11 может выскочить окно, в котором нужно выбрать пункт `Дополнительные параметры системы`), но в целом принцип нахождения аналогичен. 

Далее следует создать 4 переменных среды в верхнем окне переменных среды:
```python
HADOOP_HOME = путь до папки c Apache Hadoop (в моем случае - C:\Program Files\Apache Hadoop)
PYSPARK_HOME = путь до папки с Python (в моем случае - C:\Users\Имя вашего пользователя\AppData\Local\Programs\Python\Python312\python.exe)
JAVA_HOME = путь до папки с JDK (C:\Program Files\Java\jdk-22)
SPARK_HOME = путь до папки с Apache Spark (в моем случае - C:\Program Files\Apache Spark)
```

Кроме того, следует создать 3 дополнительных системных переменных в окне системных переменных, нажав на `Path` -> `Изменить` -> `Создать`:
```python
%HADOOP_HOME%\bin
%JAVA_HOME%\bin
%SPARK_HOME%\bin
```

## 5. Проверка работоспособности через Jupyter Notebook и командную строку
После всех манипуляций следует зайти в командую строку от имени администратора и проверить запуск Spark командой `spark-shell`
