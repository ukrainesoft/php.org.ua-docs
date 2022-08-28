Вставляє запис

-   [« dba\_handlers](function.dba-handlers.html)
    
-   [dba\_key\_split »](function.dba-key-split.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
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

Ключ запису для вставки. Якщо такий ключ вже існує у базі даних, функція завершиться з помилкою. Для заміни запису використовуйте функцію [dba\_replace()](function.dba-replace.html)

`value`

Значення для вставки.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dba\_delete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dba\_replace()](function.dba-replace.html) - Перезаписати або вставити запис