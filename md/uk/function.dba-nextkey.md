---
navigation:
  - function.dba-list.md: « dba\_list
  - function.dba-open.md: dba\_open »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_nextkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_nextkey

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_nextkey — Витягує наступний ключ

### Опис

```methodsynopsis
dba_nextkey(resource $dba): string|false
```

**dba\_nextkey()** повертає наступний ключ із бази даних та переміщає внутрішній покажчик.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_firstkey()](function.dba-firstkey.md) \- Витягує перший ключ
-   [dba\_key\_split()](function.dba-key-split.md) \- Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у[приклади DBA](dba.examples.md)
