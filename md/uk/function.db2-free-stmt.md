---
navigation:
  - function.db2-free-result.md: « db2freeresult
  - function.db2-get-option.md: db2getoption »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2freestmt
---
# db2freestmt

(PECL ibmdb2> = 1.0.0)

db2freestmt — Звільняє ресурси, пов'язані із зазначеним ресурсом виразу

### Опис

```methodsynopsis
db2_free_stmt(resource $stmt): bool
```

Звільняє ресурси системи та бази даних, пов'язані з ресурсом вираження. Ці ресурси неявно звільняються після завершення скрипту, але ви можете викликати **db2freestmt()**, щоб явно звільнити вирази до закінчення роботи скрипта.

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [db2freeresult()](function.db2-free-result.md) - звільняє ресурси, пов'язані з набором результатів
