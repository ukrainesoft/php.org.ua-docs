---
navigation:
  - function.dba-list.md: « dbalist
  - function.dba-open.md: dbaopen »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbanextkey
---
# dbanextkey

(PHP 4, PHP 5, PHP 7, PHP 8)

dbanextkey — Витягує наступний ключ

### Опис

```methodsynopsis
dba_nextkey(resource $dba): string|false
```

**dbanextkey()** повертає наступний ключ із бази даних та переміщає внутрішній покажчик.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.md) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbafirstkey()](function.dba-firstkey.md) - Витягує перший ключ
-   [dbakeysplit()](function.dba-key-split.md) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у [приклади DBA](dba.examples.md)
