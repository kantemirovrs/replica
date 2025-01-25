# «Репликация и масштабирование. Часть 1»-Кантемиров Роман
#Задание1. На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.
#Решение 1.
#Основное отличие репликаций master-slave и master-master заключается в том что при асинхроной репликации (мастер-slave) запись изменений вреальном ремени происходит на одну ноду (master). На оставшиеся ноды (slave) запись ведется опосредовано с задержкой по времени, они участуют только на обработку пользовательских запросов на  чтения данных
# При синхроной master-master запись - ведётся на обе ноды. обе ноды участвуют в обработке пользовательских запросов как на чтение так и на запись данных. 
#
#Задание 2. Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции..
#Решение 2.
#Состояние сервера Master (docker:replication-master (46fb2f7c5233))
![z21.png](https://github.com/kantemirovrs/replica/blob/main/img/z21.png)
#Состояние сервера Slave (replication-slave (33da9cf9795b))
![z11.png](https://github.com/kantemirovrs/replica/blob/main/img/z11.png)
![z12.png](https://github.com/kantemirovrs/replica/blob/main/img/z12.png)
#
#Вывод текущего состояния БД на Master и добавление новой таблицы testDB 
#
![z31.png](https://github.com/kantemirovrs/replica/blob/main/img/z31.png)
#
#
#Вывод текущего состояния БД на Slave до и после добавления новой таблицы testDB на Master.  
# 
![z32.png](https://github.com/kantemirovrs/replica/blob/main/img/z32.png)

