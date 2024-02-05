---
navigation:
  - ref.dba.md: « Функції DBA
  - function.dba-delete.md: dba\_delete »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_close

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_close — Закриває базу даних DBA

### Опис

```methodsynopsis
dba_close(resource $dba): void
```

**dba\_close()** закриває встановлену базу даних та звільняє всі пов'язані з нею ресурси.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [dba\_open()](function.dba-open.md) \- Відкриває базу даних
-   [dba\_popen()](function.dba-popen.md) \- встановити постійний екземпляр бази даних
