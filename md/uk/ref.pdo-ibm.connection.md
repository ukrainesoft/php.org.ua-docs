- [IBM (PDO)](ref.pdo-ibm.md)
- [Informix (PDO) »](ref.pdo-informix.md)

- [PHP Manual](index.md)
- [IBM (PDO)](ref.pdo-ibm.md)
- З'єднання з базою даних IBM

# PDO_IBM DSN

(PECL PDO_IBM \>= 0.9.0)

PDO_IBM DSN — З'єднання з базою даних IBM

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO_IBM базується на IBM
CLI DSN. Головний компонент PDO_IBM DSN:

Префікс DSN
Префікс DSN - **`ibm:`**.

DSN
DSN може бути одним з наступного:

- a\) Налаштування джерела даних за допомогою `db2cli.ini` або `odbc.ini`

b) Каталогізоване ім'я бази даних. Тобто. псевдонім бази даних
каталогу клієнта DB2

- c\) Повноцінний рядок з'єднання:
`DRIVER={IBM DB2 ODBC DRIVER};DATABASE=database`;HOSTNAME=`hostname`;PORT=`port`;PROTOCOL=TCPIP;UID=`username`;PWD=`password`;,
де параметри означають таке:

`database`
Назва бази даних.

`hostname`
Ім'я хоста або IP-адреса сервера бази даних.

`port`
Порт TCP/IP, у якому слухає база.

`username`
Ім'я користувача.

`password`
Пароль користувача.

### Приклади

**Приклад #1 Приклад PDO_IBM DSN з використанням `db2cli.ini`**

Наступний приклад демонструє PDO_IBM DSN для з'єднання з базою DB2
вказаної як DB2_9 в `db2cli.ini`:

$db = новий PDO("ibm:DSN=DB2_9", "", "");

[DB2_9]
Database=testdb
Protocol=tcpip
Hostname=11.22.33.444
Servicename=56789

**Приклад #2 Приклад PDO_IBM DSN за допомогою рядка з'єднання**

Наступний приклад демонструє PDO_IBM DSN для з'єднання з базою DB2
ім'ям **`testdb`** використовуючи синтаксис з'єднання DB2 CLI.

$db = новий PDO("ibm:DRIVER={IBM DB2 ODBC DRIVER};DATABASE=testdb;" ).
"HOSTNAME=11.22.33.444;PORT=56789;PROTOCOL=TCPIP;", "testuser", "tespass");
