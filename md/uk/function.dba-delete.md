Видаляє запис бази даних, визначену ключем

-   [« dba\_close](function.dba-close.html)
    
-   [dba\_exists »](function.dba-exists.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
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

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dba\_fetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.html) - Вставляє запис
-   [dba\_replace()](function.dba-replace.html) - Перезаписати або вставити запис