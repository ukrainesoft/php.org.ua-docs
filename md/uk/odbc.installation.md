- [« Вимоги](uodbc.requirements.md)
- [Налаштування під час виконання »](odbc.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](uodbc.setup.md)
- Встановлення

## Установка

**--with-adabas[=DIR]**
Включити підтримку Adabas D. DIR - це каталог установки Adabas,
замовчуванням `/usr/local`.

**--with-sapdb[=DIR]**
Увімкнути підтримку SAP DB. DIR - каталог установки SAP DB, за замовчуванням
`/usr/local`.

**--with-solid[=DIR]**
Увімкнути підтримку Solid. DIR - каталог установки Solid base,
замовчуванням `/usr/local/solid`.

**--with-ibm-db2[=DIR]**
Увімкнути підтримку IBM DB2. DIR - це каталог установки DB2,
замовчуванням `/home/db2inst1/sqllib`.

**--with-empress[=DIR]**
Увімкнути підтримку Empress. DIR - це каталог установки Empress,
замовчуванням `$EMPRESSPATH`. Опція підтримується лише Empress версії
8.60 та вище.

**--with-empress-bcs[=DIR]**
Включити підтримку `Empress Local Access`. DIR – це каталог установки
Empress, за замовчуванням `$EMPRESSPATH`. Опція підтримується лише
Empress версії 8.60 та вище.

**--with-birdstep[=DIR]**
Увімкнути підтримку Birdstep. DIR - це каталог установки Birdstep, по
замовчуванням `/usr/local/birdstep`.

**--with-custom-odbc[=DIR]**
Включити певну підтримку ODBC. DIR – це каталог
установки ODBC, за замовчуванням `/usr/local`. Переконайтеся, що ви визначили
CUSTOM_ODBC_LIBS і у вас є кілька `odbc.h` у ваших включаються
каталогах. Наприклад, ви повинні визначити наступне для Sybase SQL
Anywhere 5.5.00 в QNX перед запуском скрипта налаштування:

CPPFLAGS="-DODBC_QNX -DSQLANY_BUG"
LDFLAGS=-lunix
CUSTOM_ODBC_LIBS="-ldblib-lodbc".

**--with-iodbc[=DIR]**
Увімкнути підтримку iODBC. DIR - це каталог установки iODBC,
замовчуванням `/usr/local`.

**--with-esoob[=DIR]**
Увімкнути підтримку Easysoft OOB. DIR – це каталог установки Easysoft
OOB, за замовчуванням `/usr/local/easysoft/oob/client`.

**--with-unixODBC[=DIR]**
Включити підтримку unixODBC. DIR - це каталог установки unixODBC,
замовчуванням `/usr/local`.

**--with-openlink[=DIR]**
Увімкнути підтримку OpenLink ODBC. DIR – це каталог установки OpenLink,
за замовчуванням `/usr/local`. Це те саме, що і iODBC.

**--with-dbmaker[=DIR]**
Увімкнути підтримку DBMaker. DIR - це каталог установки DBMaker,
за промовчанням це місце, де встановлено останню версію DBMaker (наприклад,
`/home/dbmaker/3.6`).

Користувачі Windows повинні включити php_odbc.dll, щоб використовувати
цей модуль.
