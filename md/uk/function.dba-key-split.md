Поділяє ключ, заданий у вигляді рядка і створює масив отриманих частин

-   [« dba\_insert](function.dba-insert.html)
    
-   [dba\_list »](function.dba-list.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
-   Поділяє ключ, заданий у вигляді рядка і створює масив отриманих частин
    

# dbakeysplit

(PHP 5, PHP 7, PHP 8)

dbakeysplit - розділяє ключ, заданий у вигляді рядка і створює масив з отриманих частин

### Опис

```methodsynopsis
dba_key_split(string|false|null $key): array|false
```

**dbakeysplit()** розділяє ключ, заданий у вигляді рядка і створює масив отриманих частин.

### Список параметрів

`key`

Ключ у вигляді рядка.

### Значення, що повертаються

Повертає масив такого виду `array(0 => group, 1 => value_name)`. Ця функція повертає **`false`**, якщо `key` дорівнює **`null`** або **`false`**

### Дивіться також

-   [dba\_firstkey()](function.dba-firstkey.html) - Витягує перший ключ
-   [dba\_nextkey()](function.dba-nextkey.html) - Витягує наступний ключ
-   [dba\_fetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем