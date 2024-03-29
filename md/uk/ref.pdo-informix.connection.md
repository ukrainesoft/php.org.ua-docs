---
navigation:
  - ref.pdo-informix.md: « Informix (PDO)
  - ref.pdo-mysql.md: MySQL (PDO) »
  - index.md: PHP Manual
  - ref.pdo-informix.md: Informix (PDO)
title: PDO\_INFORMIX DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_INFORMIX DSN

(PECL PDO\_INFORMIX >= 0.1.0)

PDO\_INFORMIX DSN — З'єднання з базою даних Informix

### Опис

Рядок з'єднання (Data Source Name, DSN) PDO\_INFORMIX базується на рядку Informix ODBC DSN. Подробиці конфігурації Informix ODBC DSN читайте на сайті [» Informix Dynamic Server Information Center](http://publib.boulder.ibm.com/infocenter/idshelp/v10/index.jsp). Основні елементи PDO\_INFORMIX DSN:

Префікс DSN

**`informix:`**

DSN

DSN повинен бути або вказаний в odbc.ini або заданий повною [»рядком з'єднання](http://publib.boulder.ibm.com/infocenter/idshelp/v10/topic/com.ibm.odbc.doc/odbc66.htm#sii02998361)

### Приклади

**Приклад #1 Використання PDO\_INFORMIX DSN в odbc.ini**

Наступний приклад демонструє з'єднання з базою даних Informix визначеної як Infdrv33 odbc.ini:

```
$db = new PDO("informix:DSN=Infdrv33", "", "");
```

```
[ODBC Data Sources]
Infdrv33=INFORMIX 3.3 32-BIT

[Infdrv33]
Driver=/opt/informix/csdk_2.81.UC1G2/lib/cli/iclis09b.so
Description=INFORMIX 3.3 32-BIT
Database=common_db
LogonID=testuser
pwd=testpass
Servername=ids_server
DB_LOCALE=en_US.819
OPTIMIZEAUTOCOMMIT=1
ENABLESCROLLABLECURSORS=1
```

**Приклад #2 З'єднання з використанням повноцінного рядка з'єднання**

У наступному прикладі здійснюється з'єднання з базою даних \*\*`common_db`\*\*с использованием строки соединения.

```
$db = new PDO("informix:host=host.domain.com; service=9800;
    database=common_db; server=ids_server; protocol=onsoctcp;
    EnableScrollableCursors=1", "testuser", "tespass");
```
