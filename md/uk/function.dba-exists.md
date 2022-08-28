Перевіряє, чи існує ключ

-   [« dba\_delete](function.dba-delete.html)
    
-   [dba\_fetch »](function.dba-fetch.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
-   Перевіряє, чи існує ключ
    

# dbaexists

(PHP 4, PHP 5, PHP 7, PHP 8)

dbaexists — Перевіряє, чи існує ключ

### Опис

```methodsynopsis
dba_exists(string|array $key, resource $dba): bool
```

**dbaexists()** перевіряє, якщо у базі даних заданий ключ `key`

### Список параметрів

`key`

Ключ, що перевіряється.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** якщо ключ існує і **`false`** в зворотньому випадку.

### Дивіться також

-   [dba\_delete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.html) - Вставляє запис
-   [dba\_replace()](function.dba-replace.html) - Перезаписати або вставити запис