---
navigation:
  - function.dba-fetch.md: « dba\_fetch
  - function.dba-handlers.md: dba\_handlers »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_firstkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_firstkey

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_firstkey — Витягує перший ключ

### Опис

```methodsynopsis
dba_firstkey(resource $dba): string|false
```

**dba\_firstkey()** повертає перший ключ із бази даних і скидає внутрішній покажчик. Це дозволяє робити прямий пошук по всій базі.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_nextkey()](function.dba-nextkey.md) \- Витягує наступний ключ
-   [dba\_key\_split()](function.dba-key-split.md) \- Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у[приклади DBA](dba.examples.md)
