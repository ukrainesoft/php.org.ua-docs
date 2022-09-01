---
navigation:
  - ref.pdo-odbc.html: « ODBC и DB2 (PDO)
  - ref.pdo-pgsql.html: PostgreSQL (PDO) »
  - index.html: PHP Manual
  - ref.pdo-odbc.html: ODBC и DB2 (PDO)
title: PDOODBC DSN
---
# PDOODBC DSN

(PECL PDOODBC >= 0.1.0)

PDOODBC DSN — З'єднання з базами даних ODBC або DB2

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDOODBC складається з наступних елементів:

Префікс DSN

**`odbc:`**. Якщо ви з'єднуєтеся з базою, вказаною в каталозі менеджера драйверів ODBC або каталозі DB2, ви можете додати ім'я цього каталогу в DSN.

DSN

Ім'я бази даних зазначено в каталозі менеджера драйверів ODBC або в каталозі DB2. Також ви можете вказати повний рядок з'єднання ODBC, як описано тут [» http://www.connectionstrings.com/](http://www.connectionstrings.com/)

`UID`

Ім'я користувача для з'єднання. Якщо ви вказуєте ім'я користувача у рядку DSN, PDO ігноруватиме ім'я, задане аргументом у конструкторі PDO.

`PWD`

Пароль користувача для з'єднання. Якщо ви вказуєте пароль користувача у рядку DSN, PDO ігноруватиме пароль, заданий аргументом у конструкторі PDO.

### Приклади

**Приклад #1 Приклад PDOODBC DSN (менеджер драйверів ODBC)**

У наступному прикладі показано використання PDOODBC DSN для з'єднання з базою даних, визначеною в каталозі ODBC як testdb:

```
odbc:testdb
```

**Приклад #2 Приклад використання PDOODBC DSN (некаталогізоване з'єднання IBM DB2)**

У наступному прикладі показано використання PDOODBC DSN для з'єднання з базою даних IBM DB2 на ім'я **`SAMPLE`**, використовуючи повний рядок ODBC DSN:

```
odbc:DRIVER={IBM DB2 ODBC DRIVER};HOSTNAME=localhost;PORT=50000;DATABASE=SAMPLE;PROTOCOL=TCPIP;UID=db2inst1;PWD=ibmdb2;
```

**Приклад #3 Приклад використання PDOODBC DSN (некаталогізоване з'єднання Microsoft Access)**

У наступному прикладі показано використання PDOODBC DSN для з'єднання з базою Microsoft Access, що зберігається в **`C:\db.mdb`**, використовуючи повний рядок ODBC DSN:

```
odbc:Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\\db.mdb;Uid=Admin
```
