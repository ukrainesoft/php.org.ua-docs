---
navigation:
  - ref.dba.md: « Функції DBA
  - function.dba-delete.md: dbadelete »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbaclose
---
# dbaclose

(PHP 4, PHP 5, PHP 7, PHP 8)

dbaclose — Закриває базу даних DBA

### Опис

```methodsynopsis
dba_close(resource $dba): void
```

**dbaclose()** закриває встановлену базу даних та звільняє всі пов'язані з нею ресурси.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.md) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [dbaopen()](function.dba-open.md) - Відкриває базу даних
-   [dbapopen()](function.dba-popen.md) - встановити постійний екземпляр бази даних
