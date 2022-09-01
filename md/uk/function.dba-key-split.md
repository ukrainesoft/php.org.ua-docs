---
navigation:
  - function.dba-insert.html: « dbainsert
  - function.dba-list.html: dbalist »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbakeysplit
---
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

-   [dbafirstkey()](function.dba-firstkey.html) - Витягує перший ключ
-   [dbanextkey()](function.dba-nextkey.html) - Витягує наступний ключ
-   [dbafetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
