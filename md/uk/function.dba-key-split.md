---
navigation:
  - function.dba-insert.md: « dba\_insert
  - function.dba-list.md: dba\_list »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_key\_split
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_key\_split

(PHP 5, PHP 7, PHP 8)

dba\_key\_split — розділяє ключ, заданий у вигляді рядка і створює масив отриманих частин

### Опис

```methodsynopsis
dba_key_split(string|false|null $key): array|false
```

**dba\_key\_split()** розділяє ключ, заданий у вигляді рядка і створює масив отриманих частин.

### Список параметрів

`key`

Ключ у вигляді рядка.

### Значення, що повертаються

Повертає масив такого виду `array(0 => group, 1 => value_name)`. Ця функція повертає **`false`**, якщо `key`равен\*\*`null`**или**`false`\*\*

### Дивіться також

-   [dba\_firstkey()](function.dba-firstkey.md) \- Витягує перший ключ
-   [dba\_nextkey()](function.dba-nextkey.md) \- Витягує наступний ключ
-   [dba\_fetch()](function.dba-fetch.md) \- Витягує дані за вказаним ключем
