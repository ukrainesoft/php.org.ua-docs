---
navigation:
  - ref.pdo-ibm.md: « IBM (PDO)
  - ref.pdo-informix.md: Informix (PDO) »
  - index.md: PHP Manual
  - ref.pdo-ibm.md: IBM (PDO)
title: PDO\_IBM DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_IBM DSN

(PECL PDO\_IBM >= 0.9.0)

PDO\_IBM DSN — З'єднання з базою даних IBM

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO\_IBM базується на IBM CLI DSN. Головний компонент PDO\_IBM DSN:

Префікс DSN

Префикс DSN —\*\*`ibm:`\*\*

DSN

DSN може бути одним з наступного:

-   a) Налаштування джерела даних за допомогою db2cli.ini або odbc.ini
    
-   b) Каталогізоване ім'я бази даних. Т. е. псевдонім бази даних у каталозі клієнта DB2
    
-   c) Повноцінний рядок з'єднання:``DRIVER={IBM DB2 ODBC DRIVER};DATABASE=`database`;HOSTNAME=`hostname`;PORT=`port`;PROTOCOL=TCPIP;UID=`username`;PWD=`password`;``, де параметри означають таке:
    
    `database`
    
    Назва бази даних.
    
    `hostname`
    
    Ім'я хоста або IP-адреса сервера баз даних.
    
    `port`
    
    Порт TCP/IP, у якому слухає база.
    
    `username`
    
    Ім'я користувача.
    
    `password`
    
    Пароль користувача.
    

### Приклади

**Приклад #1 Приклад PDO\_IBM DSN із файлом db2cli.ini**

Наступний приклад демонструє PDO\_IBM DSN для з'єднання з базою DB2, зазначеною як DB2\_9 у db2cli.ini:

```
$db = new PDO("ibm:DSN=DB2_9", "", "");

[DB2_9]
Database=testdb
Protocol=tcpip
Hostname=11.22.33.444
Servicename=56789
```

**Приклад #2 Приклад PDO\_IBM DSN з рядком з'єднання**

Наступний приклад показує PDO\_IBM DSN для з'єднання з базою DB2 з ім'ям **`testdb`**, використовуючи синтаксис з'єднання DB2 CLI.

```
$db = new PDO("ibm:DRIVER={IBM DB2 ODBC DRIVER};DATABASE=testdb;" .
  "HOSTNAME=11.22.33.444;PORT=56789;PROTOCOL=TCPIP;", "testuser", "tespass");
```
