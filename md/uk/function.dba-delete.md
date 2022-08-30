Видаляє запис бази даних, визначену ключем

-   [« dbaclose](function.dba-close.html)
    
-   [dbaexists »](function.dba-exists.html)
    
-   [PHP Manual](index.html)
    
-   [Функції DBA](ref.dba.html)
    
-   Видаляє запис бази даних, визначену ключем
    

# dbadelete

(PHP 4, PHP 5, PHP 7, PHP 8)

dbadelete — Видалення запису бази даних, визначеної ключем.

### Опис

```methodsynopsis
dba_delete(string|array $key, resource $dba): bool
```

**dbadelete()** видаляє вказаний запис у базі даних.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaexists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dbafetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dbainsert()](function.dba-insert.html) - Вставляє запис
-   [dbareplace()](function.dba-replace.html) - Перезаписати або вставити запис