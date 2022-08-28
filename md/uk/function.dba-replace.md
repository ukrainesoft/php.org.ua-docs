Перезаписати або вставити запис

-   [« dba\_popen](function.dba-popen.html)
    
-   [dba\_sync »](function.dba-sync.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
-   Перезаписати або вставити запис
    

# dbareplace

(PHP 4, PHP 5, PHP 7, PHP 8)

dbareplace — Перезаписати або вставити запис

### Опис

```methodsynopsis
dba_replace(string|array $key, string $value, resource $dba): bool
```

**dbareplace()** перезаписує або вставляє запис, заданий ключем `key` та значенням `value` до бази даних, визначеної обробником `dba`

### Список параметрів

`key`

Ключ запису, який потрібно замінити.

`value`

Нове значення.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dba\_delete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.html) - Вставляє запис