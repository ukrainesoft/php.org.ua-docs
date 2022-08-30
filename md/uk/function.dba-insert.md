Вставляє запис

-   [« dbahandlers](function.dba-handlers.html)
    
-   [dbakeysplit »](function.dba-key-split.html)
    
-   [PHP Manual](index.md)
    
-   [Функції DBA](ref.dba.md)
    
-   Вставляє запис
    

# dbainsert

(PHP 4, PHP 5, PHP 7, PHP 8)

dbainsert — Вставляє запис

### Опис

```methodsynopsis
dba_insert(string|array $key, string $value, resource $dba): bool
```

**dbainsert()** вставляє до бази даних запис заданий параметрами `key` і `value`

### Список параметрів

`key`

Ключ запису для вставки. Якщо такий ключ вже існує у базі даних, функція завершиться з помилкою. Для заміни запису використовуйте функцію [dbareplace()](function.dba-replace.html)

`value`

Значення для вставки.

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaexists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dbadelete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dbareplace()](function.dba-replace.html) - Перезаписати або вставити запис