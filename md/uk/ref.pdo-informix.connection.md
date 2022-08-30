З'єднання з базою даних Informix

-   [« Informix (PDO)](ref.pdo-informix.html)
    
-   [MySQL (PDO) »](ref.pdo-mysql.html)
    
-   [PHP Manual](index.md)
    
-   [Informix (PDO)](ref.pdo-informix.html)
    
-   З'єднання з базою даних Informix
    

# PDOINFORMIX DSN

(PECL PDOINFORMIX >= 0.1.0)

PDOINFORMIX DSN — З'єднання з базою даних Informix

### Опис

Рядок з'єднання (Data Source Name, DSN) PDOINFORMIX базується на рядку Informix ODBC DSN. Подробиці конфігурації Informix ODBC DSN читайте на сайті [» Informix Dynamic Server Information Center](http://publib.boulder.ibm.com/infocenter/idshelp/v10/index.jsp). Основні елементи PDOINFORMIX DSN:

Префікс DSN

**`informix:`**

DSN

DSN повинен бути або вказаний в odbc.ini або заданий повною [»рядком з'єднання](http://publib.boulder.ibm.com/infocenter/idshelp/v10/topic/com.ibm.odbc.doc/odbc66.htm#sii02998361)

### Приклади

**Приклад #1 Використання PDOINFORMIX DSN в odbc.ini**

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

У наступному прикладі здійснюється з'єднання з базою даних **`common_db`** з використанням рядка з'єднання.

```
$db = new PDO("informix:host=host.domain.com; service=9800;
    database=common_db; server=ids_server; protocol=onsoctcp;
    EnableScrollableCursors=1", "testuser", "tespass");
```