# Docker
так как я использую виндоус то я не могу сделать это, но я сделал конспект и полностью прочитал конспект по лекии и посмотрел семинар, а эту работу я сделал используя иделаьное решение

## Создание контейнера
```Java
    docker run --rm -d
    > --name hw03_mariadb 
```
## Подключение к системе БД
```Java
    -v // далее надо указать путь к директории
```
## Создание и заполнение БД
```Java
    root@8aa4983aa90e:/# mariadb -u root -p // подключение как суперпользователь
    MariaDB [(none)]> create database hw03_test_base;
    MariaDB [mysql]> GRANT ALL PRIVILEGES ON  *.* to 'ordinary_user';
    root@8aa4983aa90e:/# mariadb -u ordinary_user -p // подключение как пользователь
    MariaDB [hw03_test_base]> create table tst_tbl01(col1 int, col2 varchar(20));
    MariaDB [hw03_test_base]> insert tst_tbl01(col1, col2) values(1, 'one'), (2, 'two'), (3, 'three');
    MariaDB [hw03_test_base]> create table tst_tbl02(col3 int, col4 varchar(20));
    MariaDB [hw03_test_base]> insert tst_tbl02(col3, col4) values(4, 'four'), (5, 'five'), (6, 'six'), (, );
```
