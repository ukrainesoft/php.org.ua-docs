З'єднання з базою даних IBM

-   [« IBM (PDO)](ref.pdo-ibm.html)
    
-   [Informix (PDO) »](ref.pdo-informix.html)
    
-   [PHP Manual](index.html)
    
-   [IBM (PDO)](ref.pdo-ibm.html)
    
-   З'єднання з базою даних IBM
    

# PDOIBM DSN

(PECL PDOIBM >= 0.9.0)

PDOIBM DSN — З'єднання з базою даних IBM

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDOIBM базується на IBM CLI DSN. Головний компонент PDOIBM DSN:

Префікс DSN

Префікс DSN - **`ibm:`**

DSN

DSN може бути одним з наступного:

-   a) Налаштування джерела даних за допомогою db2cli.ini або odbc.ini
    
-   b) Каталогізоване ім'я бази даних. Тобто. псевдонім бази даних у каталозі клієнта DB2
    
-   c) Повноцінний рядок з'єднання: ``DRIVER={IBM DB2 ODBC DRIVER};DATABASE=`database`;HOSTNAME=`hostname`;PORT=`port`;PROTOCOL=TCPIP;UID=`username`;PWD=`password`;``, де параметри означають таке:
    
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

**Приклад #1 Приклад PDOIBM DSN з використанням db2cli.ini**

Наступний приклад демонструє PDOIBM DSN для з'єднання з базою DB2, зазначеною як DB29 у db2cli.ini:

```
$db = new PDO("ibm:DSN=DB2_9", "", "");

[DB2_9]
Database=testdb
Protocol=tcpip
Hostname=11.22.33.444
Servicename=56789
```

**Приклад #2 Приклад PDOIBM DSN з використанням рядка з'єднання**

Наступний приклад демонструє PDOIBM DSN для з'єднання з базою DB2 з ім'ям **`testdb`** використовуючи синтаксис з'єднання DB2 CLI.

```
$db = new PDO("ibm:DRIVER={IBM DB2 ODBC DRIVER};DATABASE=testdb;" .
  "HOSTNAME=11.22.33.444;PORT=56789;PROTOCOL=TCPIP;", "testuser", "tespass");
```