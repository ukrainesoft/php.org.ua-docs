Встановлення

-   [« Вимоги](uodbc.requirements.md)
    
-   [Налаштування під час виконання »](odbc.configuration.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](uodbc.setup.md)
    
-   Встановлення
    

## Встановлення

**\-with-adabas=DIR**

Включити підтримку Adabas D. DIR - це каталог установки Adabas за промовчанням /usr/local.

**\-with-sapdb=DIR**

Увімкнути підтримку SAP DB. DIR - каталог установки SAP DB за промовчанням /usr/local.

**\-with-solid=DIR**

Увімкнути підтримку Solid. DIR – каталог установки Solid base, за умовчанням /usr/local/solid.

**\-with-ibm-db2=DIR**

Увімкнути підтримку IBM DB2. DIR - це каталог установки DB2 за промовчанням /home/db2inst1/sqllib.

**\-with-empress=DIR**

Увімкнути підтримку Empress. DIR - це каталог установки Empress, за промовчанням $EMPRESSPATH. Опція підтримується лише Empress версії 8.60 та вище.

**\-with-empress-bcs=DIR**

Включити підтримку `"Empress Local Access"`. DIR - це каталог установки Empress, за промовчанням $EMPRESSPATH. Опція підтримується лише Empress версії 8.60 та вище.

**\-with-birdstep=DIR**

Увімкнути підтримку Birdstep. DIR – це каталог установки Birdstep, за умовчанням /usr/local/birdstep.

**\-with-custom-odbc=DIR**

Включити певну підтримку ODBC. DIR - це каталог установки ODBC за промовчанням /usr/local. Переконайтеся, що ви визначили CUSTOMODBCLIBS і у вас є кілька odbc.h у ваших каталогах, що включаються. Наприклад, ви повинні визначити наступне для Sybase SQL Anywhere 5.5.00 в QNX перед запуском скрипту налаштування:

```
CPPFLAGS="-DODBC_QNX -DSQLANY_BUG"
   LDFLAGS=-lunix
   CUSTOM_ODBC_LIBS="-ldblib -lodbc".
```

**\-with-iodbc=DIR**

Увімкнути підтримку iODBC. DIR – це каталог установки iODBC, за умовчанням /usr/local.

**\-with-esoob=DIR**

Увімкнути підтримку Easysoft OOB. DIR - це каталог установки Easysoft OOB за промовчанням /usr/local/easysoft/oob/client.

**\-with-unixODBC=DIR**

Увімкнути підтримку unixODBC. DIR – це каталог установки unixODBC, за умовчанням /usr/local.

**\-with-openlink=DIR**

Увімкнути підтримку OpenLink ODBC. DIR - це каталог установки OpenLink за промовчанням /usr/local. Це те саме, що і iODBC.

**\-with-dbmaker=DIR**

Увімкнути підтримку DBMaker. DIR - це каталог установки DBMaker, за умовчанням це місце, де інстальовано останню версію DBMaker (наприклад, /home/dbmaker/3.6).

Користувачі Windows повинні увімкнути phpodbc.dll, щоб використати цей модуль.